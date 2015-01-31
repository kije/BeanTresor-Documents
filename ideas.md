# Ideas

- SQLLite DB as Application format
- - Operations performed on a in-mermory DB
- - On save, export it via backup api (?), encrypt it and write it to file
- - Or use an encryption extension (licences?, portability?)
- - C Core Library should take care of this, but should not write to file (return a binary blob?)
- - - Fileoperations shoul be done on platform-level (Android SDK, iOS SDK, etc...)
- C Core Library shoul be a independent library, which can also be used by third-party developers to build their own pw manager (C-Library = Format reader & writer)

## Architecture
https://github.com/kije/CppAndroidIosExample
- C/C++ Core Library (Platform-independent, contains logic, file format handling and everything else, which has not be performed platform-dependent)
- Wrapper for other Languages (Java JNI, etc...)
- Platform-Wrapper (Java, Objective-C, etc...)
- Platform-Dependent Code (Networking, File I/O, Services & Providers, UI, etc...)

