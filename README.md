# Objective-C KVO and Memory Management Bug

This repository demonstrates a potential bug in Objective-C related to Key-Value Observing (KVO) and memory management. Failure to properly remove KVO observers before the observed object is deallocated can lead to crashes or undefined behavior.

The `bug.m` file contains code that reproduces the bug. The `bugSolution.m` file shows how to fix the issue.

## How to reproduce

1. Clone the repository.
2. Open the project in Xcode.
3. Run the `bug.m` file. Observe the crash.
4. Run the `bugSolution.m` file. Observe the correct behavior.

## Solution

Always ensure that KVO observers are removed using `removeObserver:` before the observed object is deallocated.  Proper cleanup is crucial for preventing unexpected behavior and crashes related to KVO.