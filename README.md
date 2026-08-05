# About
This is a simple C/C++ CMake template that just works out of the box.</br>
The CMakeLists.txt and .gitignore are short, and each line is explained.</br>
So if the user wants to learn and later expand on it, they can do so easily.</br>

# Use
/src - All the .c/.cpp files go here.</br>
/include - All the .h/.hpp files go here.</br>
CMakeLists.txt - CMake settings.</br>
.gitignore - A list of ignored/used files while using Git.</br>

# Disclaimer - .gitignore
The .gitignore ignores all files by default because of a design choice that is explained there.</br>
So if you add a new file or directory to the project root, you have to manually say "I use this".</br>
The pre-installed stuff in this repo is already configured to be used, so you may rarely need to use it.</br>

# Disclaimer - Source files
Some IDEs ask to add new .c/.cpp files to the target.</br>
Unless you know what you're doing, don't.</br>
It's recommended to configure the IDE to stop asking that.</br>
