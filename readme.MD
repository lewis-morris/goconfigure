# GoConfigure

Go configure is a simple to use config parser which attempts to preserve data types and comments.

## Example config 

```ini
[TEST]

#string val
val=my_string
#string with spaces
val1=my string with spaces
#float
float_val=21.56
#integer
int_val=2
#bool
bool=True
#bool2
bool_other=true

```
## Example usage
```python

from GoConf import GoConfigure
go = GoConfigure("test.conf")
#reading values
print(go["TEST"]["val"])
#setting values
go["TEST"]["val"] = "this"
#adding new values (always write the changes if you want them to be stored)
go["TEST"]["val_new"] = "my new value"
go.write()

```

## Installation

```
pip install goconfigure
```
