# mtconnect-adapter

MTConnect adapter framework

To build this for Fanuc FOCAS the Fwlib libraries were imported from https://github.com/strangesast/fwlib. This is added as
a git submodule.

# Usage

The adapter uses an ini file - default `adapter.ini`.
This file can contain the following settings:

    [adapter]
    port = 7878
    service = MTC Focus 1
    scandelay = 100
    dnc = yes

    [focus]
    host = 10.211.55.5
    port = 8193

    [macros]
    ?

    [pmc]
    SspeedOvr = 30
    Fovr = 12

Otherwise to run the adapter directly use
`fanuc.exe [debug|run] [<machine ip> <machine port> <adapter port> | <adapter ini file>]`

To install as a service use
`fanuc.exe install [<machine ip> <machine port> <adapter port> | <adapter ini file>]`
