# C++
C++ Foundations

# Visual Code Extensions
- Code Runner by Jun Han
- c/c++ by Microsoft
# Config MSVC compiler
- open developer PowerShell for VS 2022
- cd working directory
- open proyect with .code
- open terminal within VSCode
- Verify cl.exe does work
- In VSCode go to Terminal Menu>Configure Tasks>Select C/C++: cl.exe compiler
- In task.json update the following lines:
```
  {
            "type": "cppbuild",
            "label": "Build with MSVC",
            "command": "cl.exe",
            "args": [
                "/Zi",
                "/std:c++latest",
                "/EHsc",
                "/nologo",
                "/Fe${fileDirname}\\${fileBasenameNoExtension}.exe",
                "${file}"
            ],
            "options": {
                "cwd": "${fileDirname}"
            },
            "problemMatcher": [
                "$msCompile"
            ],
            "group": "build",
            "detail": "compiler: cl.exe"
        }
```
- Terminal Menu>Run a task>Select Build with MSVC
- Command Palette>C/C++ Edit Configuration(UI)
Adjust:
- Compiler path
- ../bin/Hostx64/x64/cl.exe
- C standard > 23
- C++ standard > 23


