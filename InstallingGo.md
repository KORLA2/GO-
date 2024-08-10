
We can install Go https://go.dev/doc/install

There are many environment variables go use, mainly GOPATH,GOOS, GoARCH we are concerned about.

<b>When go is installed by default go creates go folder and it has bin,pkg,src folders and it wil be our workspace, any folder containing bin src, pkg folders we can set this folder as our new workspace by setting GOPATH environment variable to our new workspace loaction </b>

By using `export GOPATH="<Loaction to new folder>"`

When we use the go command to build, install, or run Go code, it searches for packages and dependencies within the directories specified by the GOPATH.
If you install a Go package, its source code will be stored in the src directory, and the compiled binary will be placed in the bin directory.
