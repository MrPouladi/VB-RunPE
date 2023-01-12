# VBS-RunPE
A script that is undetected and demonstrates how malware hides in a legitimate process. Disclaimer: this program has been uploaded to be analyzed for prevention use at your own risk and make sure to have permission if using on another device. This tool is for educational purposes only!

Here are some things to keep in mind:

The key parts of the RunPE technique here are:

    Import of "CreateProcess" API, which creates a new process and its primary thread
    Import of "NtUnmapViewOfSection" API, which unmaps a view of a section from the address space of a process
    Import of "VirtualAllocEx" API, which reserves or commits a region of memory within the virtual address space of a process
    Import of "WriteProcessMemory" API, which writes data to the memory of a specified process
    Import of "ResumeThread" API, which increments the suspend count of the specified thread, enabling the thread to execute

This gives the ability to load and execute a second program in the memory of another process, allowing the original process to continue running.
