# DelayLoadingIssueCppWinRT
This is a test case repository to show that when CppWinRT package is added to a project that uses DLL delay loading, additional dependencies appear

# Without CppWinRT dependecies are like this:

Microsoft (R) COFF/PE Dumper Version 14.29.30038.1
Copyright (C) Microsoft Corporation.  All rights reserved.


Dump of file Debug\DelayLoadingIssueCppWinRT.exe

File Type: EXECUTABLE IMAGE

  Image has the following dependencies:

    gdiplus.dll
    KERNEL32.dll
    USER32.dll
    VCRUNTIME140D.dll
    ucrtbased.dll
