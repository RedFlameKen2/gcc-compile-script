# GccCompileScript

## Intro 
I use the gcc/g++ compiler to compile my C++ code. And the basic way of doing this is to run:

```
g++ <filename.cpp> -o <executableName> && chmod +x <executableName> && ./executableName
```

to avoid writing such a command, i made an alias for this in my shell rc file

```
cmain="g++ main.cpp -o main && chmod +x main && ./main"
```

the problem with this is that it only compiles the main.cpp file. If the target file wasn't named main.cpp, then the alias wouldn't compile the target, obviously. As a CS student who studies cpp, this alias has been really handy! but when i recieve files that aren't named main, then i'll have to write the long long compiling command to compile and run code. So this script, I made it and hopefully will improve, will be used to compile my code better and much more easily.

## Usage

if the cpp files are in the current working directory, run:
```
ccom
```

but for when the source files are in a different directory like *src/*, you may use the **-n** flag to specify where:
```
ccom -n src/<insert executable name here>
```

**NOTE:** You will need to specify the name of your executable here, probably a bad way to write this script but this will do for now. so if for example the executable's name is **main**, then use this command:

```
ccom -n src/main
```

what this will do is compile your c++ code for linux as this'll use the plain g++ compiler. to compile for windows, you must use the **-w** or **--windows** flag to compile for windows:

```
ccom -n src/main --windows
```
