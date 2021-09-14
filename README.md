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


# Adding CppWinRT package dependecies remain same as above

# Using DLL delay loading and CppWinRT package afects dependecies list:

Microsoft (R) COFF/PE Dumper Version 14.29.30038.1
Copyright (C) Microsoft Corporation.  All rights reserved.


Dump of file C:\Users\Mihai Udrea\DelayLoadingIssueCppWinRT\Debug\DelayLoadingIssueCppWinRT.exe

File Type: EXECUTABLE IMAGE

  Image has the following dependencies:

    KERNEL32.dll
    USER32.dll
    api-ms-win-core-sysinfo-l1-1-0.dll
    api-ms-win-core-memory-l1-1-0.dll
    api-ms-win-core-libraryloader-l1-2-0.dll
    VCRUNTIME140D.dll
    ucrtbased.dll

  Image has the following delay load dependencies:

    gdiplus.dll


# The following API sets appear as dependencies only when the CppWinRT package is preset. How can this be prevented (but still using DLL delay loading) ?

    api-ms-win-core-sysinfo-l1-1-0.dll
    api-ms-win-core-memory-l1-1-0.dll
    api-ms-win-core-libraryloader-l1-2-0.dll