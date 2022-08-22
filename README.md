# Qpid Proton PyPI

[![main](https://github.com/ssorj/qpid-proton-pypi/workflows/main/badge.svg)](https://github.com/ssorj/qpid-proton-pypi/actions?query=workflow%3Amain)

## The Windows build problem

~~~
C:\Program Files\Microsoft Visual Studio\2022\Enterprise\VC\Tools\MSVC\14.32.31326\bin\HostX86\x64\cl.exe
/c /nologo /Ox /W3 /GL /DNDEBUG /MD -DPROTON_DECLARE_STATIC
-Ibuild\include
-IC:\Users\RUNNER~1\AppData\Local\Temp\pip-install-waf9zgty\python-qpid-proton_48e9e2f4138e47f18015f287bc08b3f6\include
-IC:\Users\RUNNER~1\AppData\Local\Temp\pip-install-waf9zgty\python-qpid-proton_48e9e2f4138e47f18015f287bc08b3f6\src
"-IC:\Program Files\Microsoft Visual Studio\2022\Enterprise\VC\Tools\MSVC\14.32.31326\include"
"-IC:\Program Files\Microsoft Visual Studio\2022\Enterprise\VC\Tools\MSVC\14.32.31326\ATLMFC\include"
"-IC:\Program Files\Microsoft Visual Studio\2022\Enterprise\VC\Auxiliary\VS\include"
"-IC:\Program Files (x86)\Windows Kits\10\include\10.0.22621.0\ucrt"
"-IC:\Program Files (x86)\Windows Kits\10\\include\10.0.22621.0\\um"
"-IC:\Program Files (x86)\Windows Kits\10\\include\10.0.22621.0\\shared"
"-IC:\Program Files (x86)\Windows Kits\10\\include\10.0.22621.0\\winrt"
"-IC:\Program Files (x86)\Windows Kits\10\\include\10.0.22621.0\\cppwinrt"
"-IC:\Program Files (x86)\Windows Kits\NETFXSDK\4.8\include\um"
/TcC:\Users\RUNNER~1\AppData\Local\Temp\pip-install-waf9zgty\python-qpid-proton_48e9e2f4138e47f18015f287bc08b3f6\src\core\autodetect.c
/Fobuild\temp.win-amd64-3.7\Release\Users\RUNNER~1\AppData\Local\Temp\pip-install-waf9zgty\python-qpid-proton_48e9e2f4138e47f18015f287bc08b3f6\src\core\autodetect.obj
[linebreak]
autodetect.c
C:\Users\RUNNER~1\AppData\Local\Temp\pip-install-waf9zgty\python-qpid-proton_48e9e2f4138e47f18015f287bc08b3f6\src\core\autodetect.c : fatal error C1083: Cannot open compiler generated file: '': Invalid argument
error: command 'C:\\Program Files\\Microsoft Visual Studio\\2022\\Enterprise\\VC\\Tools\\MSVC\\14.32.31326\\bin\\HostX86\\x64\\cl.exe' failed with exit status 1
[end of output]
~~~

### Related links

- https://stackoverflow.com/questions/34074925/vs-2015-cannot-open-compiler-generated-file-invalid-argument
- https://stackoverflow.com/questions/1880321/why-does-the-260-character-path-length-limit-exist-in-windows?noredirect=1&lq=1
- https://docs.microsoft.com/en-us/windows/win32/fileio/maximum-file-path-limitation?tabs=registry
- https://github.com/puppetlabs/puppetlabs-zfs_core/actions/runs/355898807/workflow
- https://stackoverflow.com/questions/8745215/best-way-to-resolve-file-path-too-long-exception
- https://developercommunity.visualstudio.com/t/clexe-compiler-driver-cannot-handle-long-file-path/975889
- https://stackoverflow.com/questions/69082543/how-to-make-long-windows-paths-work-with-cl-exe
- https://docs.microsoft.com/en-us/windows/win32/fileio/naming-a-file?redirectedfrom=MSDN#namespaces
