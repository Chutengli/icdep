# Administration (admin.md): How can we send commands ("SLEEP", "RESTART", "ARE-YOU-THERE", etc) to individual nodes in the network, rather than treat them as pass-through intermediaries?

We can wrap the web information into a web fragment that has a header and body. The header could specify the type of the web fragment and the body could include the actual information. In this case, we could specify the type as `command` in the header and wrap the actual command (e.g. `SLEEP`) into the body. Once the node sees the type in the header as `command`, the node could just execute the command.
