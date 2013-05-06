This is my custom fork of Mono.Cxxi that aims to replace the GCC-XML parser
with a Clang-based one, and remove all the C++-ABI specific code for things
like object layout and name mangling from the runtime library while replacing
it with metadata generated by Clang (it already provides all the needed info).


Directory structure
-------------------

Manual.md
  Work-in-progress documentation for this tool.

src/
  Runtime
    Helper runtime library to bridge the C++ standard library
  Bridge
    Contains the needed classes to bridge the Clang parser to .NET
  Parser
    C++/CLI based wrapper around the C++ Clang libraries.    
  Generator
    The Clang-based binding generator

tests/
  Regression tests

examples/
  Hello
    Small, Hello, World! example