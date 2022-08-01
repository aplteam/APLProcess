# APLProcess

## Overview

This class is useful in case you need to fire up another APL session from within Dyalog APL, for example for test cases, or a fully automated "Test & Make" procedure.

The class is designed to run on all major platforms: Windows, Linux and Mac-OS. However, it was tested only on Windows and Linux. 

By default the same version of Dyalog APL is instanciated `APLProcess` is running in. This can be changed by creating a parameter space, making the necessary adjustments and then pass this space as an argument to the constructor.

Alternatively you can pass a simple text vector to the constructor. This can be used to specify a workspace name and parameters like `MAXWS` and the likes. However, you **cannot** specify "session_file" this way.

Note that by default the instance does not have a session file (DSE).


## Scope and limitations

`APLProcess`' main purpose is to start APL session for testing etc. It is therefore limited in scope; for example, you cannot start an APL process on a different machine.