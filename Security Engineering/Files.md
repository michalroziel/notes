
programs need a reference to a file 
they cnanot use the file name on each write operation 

## Standard File Descriptors

- stdin: standard input
- stdout: standard output
- stderr: standard error
- stdin is a file descriptor that is used to read input from the user
- stdout is a file descriptor that is used to write output to the user
- stderr is a file descriptor that is used to write error messages to the user

## Pipes 

### Pipes : Examples 

### Pipes : xargs transfors stdin to command line args

```

```

## The Filey Type 

- regular file [-]
- directory [d]
- link [l]
- socket [s]
- pipe [p]
- block device [b]
- character dervice [c]

## Defaukt Protection of a New File 

```

$ umask 022

010
rwx 

```
die umask Einstellung sort dafür, dass die Zugriffsrechte nach dem anlegen eines Directories vorhanden sind 


