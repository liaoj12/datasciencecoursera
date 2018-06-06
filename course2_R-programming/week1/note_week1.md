## Programming in R
* Assignment (can use "=" as well, but "<-" is more general):
```
x <- 5
```
* Comments using "##"
* _:_ operators returns a vector in integer!!!
* _Na_ is different from _NaN_; _NaN_ is a subset of _Na_
* Attributes of an object can be accessed with _attributes()_ function
* Objects in R:
1. "atomic":
- character
- numeric (real numbers)
- integer:
  + _1L_ explicitly gives an integer
  + special number: _Inf_
  + _NaN_ stands for undefined value
- complex
2. "container":
- logical (True/False)
- vector:
  + can only contain elements of the same class
  + create with either _c()_ or _vector()_
  + if coercion(mixing classes in vector) occurs, then the rest of elements will be casted automatically in the same class of the first element in the vector
  + explicit coersion using: _as.*_ functions, ex: _as.numeric(x)_
- list:
  + similar to vector, but can contain elements of different classes
  + each element is a vector of its class
- factors:
  + can be thought as an integer vector where each integer has a label
  + treated specially by modelling functions like _lm()_ and _glm()_
  + order of the levels
- matrices:
  + create with _matrix()_ function or with _cbind()_ and _rbind()_
  + elements in each column have to be the same class
- data frames:
  + elements in each column can be different classes
  + usually created with _read.table()_ or _read.csv()_
* Reading Data
  + _read.table_,_read.csv_ for reading tabular data, with options often used:
    - _file_
    - _header_
    - _sep_
    - _colClasses_
    - _nrows_
    - _comment.char_
    - _skip_
    - _stringsAsFactors_
  + _readLines_ for reading lines of a text file
  + _source_ for reading in R code files
  + _dget_ for reading in R code files
  + _load_ for reading in saved workspaces
  + _unserialize_ for reading single R objects in binary form
* Writing Data
  + _write.table_, _writeLines_, _dump_, _dput_, _save_ and _serialize_
* Reading in Large Datasets
  + read the help page, which contains many hints
  + estimate needed memory for the dataset
  + set _comment.char=""_ if there are no commented lines in file
  + use _colClasses_ so that R doesn't need to figure out the data types itself
* Subsetting
  + _[_ always returns an object of the same class as the original
  + _[[_ is used to extract element of a list or a data frame
  + _$_ is used to extract element of a list or data frame by name
