### call
```red
USAGE:
     CALL cmd

DESCRIPTION: 
     Executes a shell command to run another process. 
     CALL is a native! value.

ARGUMENTS:
     cmd          [string! file!] "A shell command or an executable file."

REFINEMENTS:
     /wait        => Runs command and waits for exit.
     /show        => Force the display of system's shell window (Windows only).
     /console     => Runs command with I/O redirected to console (CLI console only at present).
     /shell       => Forces command to be run from shell.
     /input       => 
        in           [string! file! binary!] "Redirects in to stdin."
     /output      => 
        out          [string! file! binary!] "Redirects stdout to out."
     /error       => 
        err          [string! file! binary!] "Redirects stderr to err."

RETURNS:
     0 if success, -1 if error, or a process ID.
     [integer!]

```