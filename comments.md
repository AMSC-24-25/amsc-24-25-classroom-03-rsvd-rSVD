
# comments

The code is nice, well written, using modern c++ construct. And I did not know of CUR! So, I have learned something new. I have however some comments:

1. You have decided to use a complex package manager, which is very heavy on Linux. I tried to compile your code but I had to stop because vcpkg was taking ages to install a lot of stuff that I have already on my computer! A simpler cmake file would have done the job easily since your code is essentially a header only libary + some tools for test and profiling.  Probably vcpcg works better on MACOS or Windows, but on Linux is a nightmare. Or, maybe I am not doing the right things, but I tried to follow your documentation. Maybe vcpkg is meant to work on WLS, but I do not have WLS. I have a real Linux machine.
2. I would have expected a different organization of the code to make it more usable as a library. For example, I would have expected a cmake file to install the library in the system, and then tools to test the library. Tipycally, if the libeary is a header only library, the install process copies the hreader files in an include directory, eventualy specified by the user.
3. The documentation of the code is rather good and the report is well done. I could not find majorIt's a pity I could not compile and test myself.

A think that I do not understand. Who has told you to qualify as const a returned value of a function? I do not see any reason to do that. The returned value is a temporary object, so it is not possible to modify it anyway. So, why to qualify it as const? Moreover doing that may block move semantics since a const rvalue is not movable. And maybe you want move semantics in your code to optimize memory usage. So, I would remove the const qualifier from the returned values.

Sometimes you return the object as reference with a `return *this` statement. Why is that?

A part for those critics, it is a good job. I have learned something new and I have seen a well written code. I have see you have all worked.


