saploader
=============

This is command line application to extract data from SAP system.  

## How to use
from table

```
saploader <destination> <tablename> <filename> [/c <columns>] [/f <fields>] [/o <options>]
```

from query

```
saploader <destination> <queryname/userGroup> <filename> /q [/o <options>] [/v <query variant>]
```

options

```
/h  : write header
/hc : write header by caption text
```

## Set up
To start `saploader` quickly,download quickstart/saploader.zip and expand it.  
And adjust `ClientSettings` in `saploader.exe.config` to connect your SAP.

## Examples

```
saploader MY_SAP T001 table.txt /t /f BUKRS,BUTXT /o BUKRS=1*
saploader MY_SAP ZQUERY01/MYGROUP query.txt /q /v MY_VARIANT
```
