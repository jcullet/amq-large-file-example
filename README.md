# Large File Transfer Via Red Hat AMQ 7.2

## Requirements

- Red Hat AMQ 7.2
- Maven 3.X

## Preparing

Install the AMQ broker instance:

```
$ ${AMQ_INSTALL_DIR}/bin/artemis create broker
```
Create the input and output file directories that the camel route will utilize.

```
$ mkdir -p files/input
$ mkdir -p files/output
```

## Running the example

```
$ mvn spring-boot:run
```

Generate or otherwise acquire several large files. The default file size for AMQ to consider the message to be a large file is 100kb.

Copy the input file into the files/input directory and observe the log output for the service. Similarly, observe that the file is written out into the files/output directory as well.