##[CloseHandle](https://msdn.microsoft.com/en-us/library/windows/desktop/ms724211(v=vs.85).aspx)
Закрывает хэндл (дескриптор) 

__Параметры__ 
* `HANDLE hObject` - хэндл (дескриптор) который будет закрыт

__Возращаемое значение__
* Возвращает не ноль если закрыт (true)
* Иначе ноль (false)

##[CreateToolhelp32Snapshot](https://msdn.microsoft.com/en-us/library/windows/desktop/ms682489(v=vs.85).aspx)
Статический срез данных, таких как, кучи, модули и потоки созданные конкретным процессом

__Параметры__
* `DWORD dwFlags` - Флаг, который указываеь какие даные будут получены в срезе данных
* `DWORD th32ProcessID` - Id процесса для которого будет получен срез данных

__Возращаемое__
* Если удалось получить срез данных, то возвращает его хэндл
* Иначе константу `INVALID_HANDLE_VALUE`

##[EnumThreadWindows]


##ExtractFileName
##ExtractIcon
##GetClassLong
##GetWindowText
##GlobalMemoryStatus
##Heap32First
##Heap32ListFirst
##Heap32ListNext
##Heap32Next
##ImageList_AddIcon
##LoadImage
##Module32First
##Module32Next
##OpenProcess
##Process32First
##Process32Next
##SetPriorityClass
##TerminateProcess
##Thread32First
##Thread32Next
##Toolhelp32ReadProcessMemory
