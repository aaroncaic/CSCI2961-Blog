## Lab 5 Blog

#### Step 1:
 * Made separate folder for built:
 ```
 aaron@aaron-VirtualBox:~/Documents/Open Source/Lab 5/Build$ cmake ..
-- The C compiler identification is GNU 4.8.2
-- The CXX compiler identification is GNU 4.8.2
-- Check for working C compiler: /usr/bin/cc
-- Check for working C compiler: /usr/bin/cc -- works
-- Detecting C compiler ABI info
-- Detecting C compiler ABI info - done
-- Detecting C compile features
-- Detecting C compile features - done
-- Check for working CXX compiler: /usr/bin/c++
-- Check for working CXX compiler: /usr/bin/c++ -- works
-- Detecting CXX compiler ABI info
-- Detecting CXX compiler ABI info - done
-- Detecting CXX compile features
-- Detecting CXX compile features - done
-- Configuring done
-- Generating done
-- Build files have been written to: /home/aaron/Documents/Open Source/Lab 5/Build
 ```
 
 * Build it:
  ```
aaron@aaron-VirtualBox:~/Documents/Open Source/Lab 5/Build$ make
Scanning dependencies of target Tutorial
[ 50%] Building CXX object CMakeFiles/Tutorial.dir/tutorial.cxx.o
[100%] Linking CXX executable Tutorial
[100%] Built target Tutorial
  ```
 
#### Step 2:
 * Build it:
```
aaron@aaron-VirtualBox:~/Documents/Open Source/Lab 5/Step2/Build$ make
Scanning dependencies of target MathFunctions
[ 25%] Building CXX object MathFunctions/CMakeFiles/MathFunctions.dir/mysqrt.cxx.o
[ 50%] Linking CXX static library libMathFunctions.a
[ 50%] Built target MathFunctions
Scanning dependencies of target Tutorial
[ 75%] Building CXX object CMakeFiles/Tutorial.dir/tutorial.cxx.o
[100%] Linking CXX executable Tutorial
[100%] Built target Tutorial
```
 

#### Step 3:
 * Installed it:
```
aaron@aaron-VirtualBox:~/Documents/Open Source/Lab 5/Step3/Build$ sudo make install
[ 50%] Built target MathFunctions
[100%] Built target Tutorial
Install the project...
-- Install configuration: ""
-- Installing: /usr/local/bin/Tutorial
-- Installing: /usr/local/include/TutorialConfig.h
-- Installing: /usr/local/bin/libMathFunctions.a
-- Installing: /usr/local/include/MathFunctions.h
```

 * Ran `ctests`:
```
aaron@aaron-VirtualBox:~/Documents/Open Source/Lab 5/Step3/Build$ ctest
Test project /home/aaron/Documents/Open Source/Lab 5/Step3/Build
    Start 1: TutorialRuns
1/5 Test #1: TutorialRuns .....................   Passed    0.05 sec
    Start 2: TutorialComp25
2/5 Test #2: TutorialComp25 ...................   Passed    0.03 sec
    Start 3: TutorialNegative
3/5 Test #3: TutorialNegative .................   Passed    0.04 sec
    Start 4: TutorialSmall
4/5 Test #4: TutorialSmall ....................   Passed    0.02 sec
    Start 5: TutorialUsage
5/5 Test #5: TutorialUsage ....................   Passed    0.02 sec

100% tests passed, 0 tests failed out of 5

Total Test time (real) =   0.21 sec
```

#### Step 4:
 * Build it:
```
aaron@aaron-VirtualBox:~/Documents/Open Source/Lab 5/Step4/Build$ cmake ..
-- The C compiler identification is GNU 4.8.2
-- The CXX compiler identification is GNU 4.8.2
...
-- Looking for log
-- Looking for log - not found
-- Looking for exp
-- Looking for exp - not found
...
-- Build files have been written to: /home/aaron/Documents/Open Source/Lab 5/Step4/Build
```

#### Step 5:
 * Build it:
```
aaron@aaron-VirtualBox:~/Documents/Open Source/Lab 5/Step5/Build$ make
Scanning dependencies of target MakeTable
[ 14%] Building CXX object MathFunctions/CMakeFiles/MakeTable.dir/MakeTable.cxx.o
[ 28%] Linking CXX executable MakeTable
[ 28%] Built target MakeTable
[ 42%] Generating Table.h
Scanning dependencies of target MathFunctions
[ 57%] Building CXX object MathFunctions/CMakeFiles/MathFunctions.dir/mysqrt.cxx.o
[ 71%] Linking CXX static library libMathFunctions.a
[ 71%] Built target MathFunctions
Scanning dependencies of target Tutorial
[ 85%] Building CXX object CMakeFiles/Tutorial.dir/tutorial.cxx.o
[100%] Linking CXX executable Tutorial
[100%] Built target Tutorial
```

 * Installed it:
```
aaron@aaron-VirtualBox:~/Documents/Open Source/Lab 5/Step5/Build$ sudo make install
[sudo] password for aaron: 
[ 28%] Built target MakeTable
[ 71%] Built target MathFunctions
[100%] Built target Tutorial
Install the project...
-- Install configuration: ""
-- Installing: /usr/local/bin/Tutorial
-- Installing: /usr/local/include/TutorialConfig.h
-- Installing: /usr/local/bin/libMathFunctions.a
-- Up-to-date: /usr/local/include/MathFunctions.h
```

 * Ran it:
```
aaron@aaron-VirtualBox:~/Documents/Open Source/Lab 5/Step5/Build$ ctest
Test project /home/aaron/Documents/Open Source/Lab 5/Step5/Build
    Start 1: TutorialRuns
1/9 Test #1: TutorialRuns .....................   Passed    0.03 sec
    Start 2: TutorialUsage
2/9 Test #2: TutorialUsage ....................   Passed    0.01 sec
    Start 3: TutorialComp4
3/9 Test #3: TutorialComp4 ....................   Passed    0.02 sec
    Start 4: TutorialComp9
4/9 Test #4: TutorialComp9 ....................   Passed    0.02 sec
    Start 5: TutorialComp5
5/9 Test #5: TutorialComp5 ....................   Passed    0.03 sec
    Start 6: TutorialComp7
6/9 Test #6: TutorialComp7 ....................   Passed    0.02 sec
    Start 7: TutorialComp25
7/9 Test #7: TutorialComp25 ...................   Passed    0.02 sec
    Start 8: TutorialComp-25
8/9 Test #8: TutorialComp-25 ..................   Passed    0.03 sec
    Start 9: TutorialComp0.0001
9/9 Test #9: TutorialComp0.0001 ...............   Passed    0.03 sec

100% tests passed, 0 tests failed out of 9

Total Test time (real) =   0.26 sec
```

 * My `table.h` file:
```
  double sqrtTable[] = {
0,
1,
1.41421,
1.73205,
2,
2.23607,
2.44949,
2.64575,
2.82843,
3,
0};
```
