## Programming in R
* Assignment (can use "=" as well, but "<-" is more general):
```
x <- 5
```
* Comments using "##"
* _:_ operators returns a vector in integer!!!
* _Na_ is different from _NaN_; _Na_ is a subset of _NaN_
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

