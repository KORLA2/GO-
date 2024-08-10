
We can install Go https://go.dev/doc/install

There are many environment variables go use, mainly GOPATH,GOOS, GoARCH we are concerned about.

<b>When go is installed by default go creates go folder and it has bin,pkg,src folders and it wil be our workspace, any folder containing bin src, pkg folders we can set this folder as our new workspace by setting GOPATH environment variable to our new workspace loaction </b>

By using `export GOPATH="<Loaction to new folder>"`

When we use the go command to build, install, or run Go code, it searches for packages and dependencies within the directories specified by the GOPATH.
If you install a Go package, its source code will be stored in the src directory, and the compiled binary will be placed in the bin directory.

- src Directory

The src directory is where your Go source code resides. Inside src, you organize your code into packages based on their import paths.
For example, if your project is hosted on GitHub at github.com/yourusername/yourproject, your source code would be located in the src/github.com/yourusername/yourproject directory. Each package typically has its own subdirectory under src. For example, the main package of your project might be in src/github.com/yourusername/yourproject/cmd/main.

- pkg Directoy
  
The pkg directory stores compiled package object files (.a files) generated during the build process.
These package object files are intermediate artifacts representing precompiled versions of your packages. They are stored in a directory structure that reflects the target architecture and operating system.
This directory is created to speed up the build process by avoiding the recompilation of unchanged packages. It helps in achieving parallel builds and reduces rebuild times.

