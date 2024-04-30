# GccCompileScript

I use the gcc/g++ compiler to compile my C++ code. And the basic way of doing this is to run:

```
g++ <filename.cpp> -o <executableName> && chmod +x <executableName> && ./executableName
```

to avoid writing such a command, i made an alias for this in my shell rc file

```
cmain="g++ main.cpp -o main && chmod +x main && ./main"
```

the problem with this is that it only compiles the main.cpp file. If the target file wasn't named main.cpp, then the alias wouldn't compile the target, obviously. As a CS student who studies cpp, this alias has been really handy! but when i recieve files that aren't named main, then i'll have to write the long long compiling command to compile and run code. So this script, I made it and hopefully will improve, will be used to compile my code better and much more easily.
