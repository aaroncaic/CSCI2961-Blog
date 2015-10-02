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
 

#### Step 3:
Results:
```
aaron@aaron-VirtualBox:~/Downloads/cmake-3.3.2/Tests/Tutorial/Step3/build$ ctestTest project /home/aaron/Downloads/cmake-3.3.2/Tests/Tutorial/Step3/build
    Start 1: TutorialRuns
1/7 Test #1: TutorialRuns .....................   Passed    0.04 sec
    Start 2: TutorialComp25
2/7 Test #2: TutorialComp25 ...................   Passed    0.03 sec
    Start 3: TutorialNegative
3/7 Test #3: TutorialNegative .................   Passed    0.03 sec
    Start 4: TutorialSmall
4/7 Test #4: TutorialSmall ....................   Passed    0.04 sec
    Start 5: TutorialUsage
5/7 Test #5: TutorialUsage ....................   Passed    0.03 sec
    Start 6: TutorialComp-25
6/7 Test #6: TutorialComp-25 ..................   Passed    0.03 sec
    Start 7: TutorialComp64
7/7 Test #7: TutorialComp64 ...................   Passed    0.04 sec

100% tests passed, 0 tests failed out of 7

Total Test time (real) =   0.26 sec

```

#### Step 4:

#### Step 5:
