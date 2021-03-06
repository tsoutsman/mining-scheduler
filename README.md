A program that stops and starts a process based on other, currently open, processes. It was initially designed to stop and start a crypto-miner depending on whether a game was open, but it can be applied to any other use case.

# Usage
`mining-scheduler schedule [FLAGS] <MINER> <CONFIG>` where `<MINER>` is the path to the miner, and `<CONFIG>` is an absolute or relative path to a text file which contains the names of the processes, that when running, should cause the miner to be shutdown. There should be one process name on each line of the file. If the `-i` flag is set, the processes are treated in a case insensitive manner. `schedule` also has two optional parameters: `-v [1-3]`, which sets the verbosity level (the higher, the more verbose), and `-t [uint]`, which specifies how often the program checks the running processes.

To make it easier to find process names, the `processes` subcommand can be called (`mining-scheduler processes`), which will list the names of all currently running processes.
