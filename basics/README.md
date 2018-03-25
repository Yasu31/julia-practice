# basics
Based on [Julia language: a concise tutorial](https://www.gitbook.com/book/sylvaticus/julia-language-a-concise-tutorial/details).

* "fast coding	vs.	fast	execution."
* "ArRAyS StArt aT oNe"
## Installation
`$ brew cask install julia`

## Packages
add new with
```julia
Pkg.update()
Pkg.add("Plots")
```
### [PyCall](https://github.com/JuliaPy/PyCall.jl)
can call Python libraries through Julia. Install with `Pkg.add("PyCall")`
```julia
using PyCall
@pyimport math
math.sin(math.pi / 4) - sin(pi / 4)  # returns 0.0
```
### [Conda](https://en.wikipedia.org/wiki/Conda_(package_manager))


### Plots
Error
>ERROR: PyError (ccall(@pysym(:PyImport_ImportModule), PyPtr, (Cstring,), name)
The Python package mpl_toolkits.mplot3d could not be found by pyimport. Usually this means
that you did not install mpl_toolkits.mplot3d in the Python version being used by PyCall.
PyCall is currently configured to use the Julia-specific Python distribution
installed by the Conda.jl package.  To install the mpl_toolkits.mplot3d module, you can
use `pyimport_conda("mpl_toolkits.mplot3d", PKG)`, where PKG is the Anaconda
package the contains the module mpl_toolkits.mplot3d, or alternatively you can use the
Conda package directly (via `using Conda` followed by `Conda.add` etcetera).
Alternatively, if you want to use a different Python distribution on your
system, such as a system-wide Python (as opposed to the Julia-specific Python),
you can re-configure PyCall with that Python.   As explained in the PyCall
documentation, set ENV["PYTHON"] to the path/name of the python executable
you want to use, run Pkg.build("PyCall"), and re-launch Julia.
) <type 'exceptions.ImportError'>
ImportError('No module named mpl_toolkits.mplot3d',)

[Error installing PyPlot: The Python package mpl_toolkits.mplot3d could not be found by pyimport](https://discourse.julialang.org/t/error-installing-pyplot-the-python-package-mpl-toolkits-mplot3d-could-not-be-found-by-pyimport/6372): per user *slowbrain*,
```
run(`install_name_tool -change @rpath/libiomp5.dylib @loader_path/libiomp5.dylib $(Pkg.dir("Conda", "deps/usr/lib/libmkl_intel_thread.dylib"))`)
Conda.update()
Pkg.build("PyCall")
```
### DataFrames

## Documentation
>It	is	a	good	practice	to	document	your	own	functions.	You	can	use	triple	quoted	strings	(""") just	before	the	function	to	document	and	use	Markdown	syntax	in	it.	The	Julia documentation	recommends	that	you	insert	a	simplified	version	of	the	function,	together	with an	 	Arguments		and	an	 	Examples		sessions.
