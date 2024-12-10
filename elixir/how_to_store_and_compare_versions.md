## Versions. One of many solutions

### Store outside of DB
Major.Minor.Patch as a string OR better as an Ecto.Type


### Store inside DB
An integer as a result of an exuality function:
major * 10000 + minor * 100 + patch


Decompose the integer into major, minor, patch:
major = version / 10000
minor = (version - major * 10000) / 100
patch = version - major * 10000 - minor * 100
