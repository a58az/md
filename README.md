##[CloseHandle](https://msdn.microsoft.com/en-us/library/windows/desktop/ms724211(v=vs.85).aspx)
Закрывает хэндл (дескриптор) 

__Параметры__ 
* `HANDLE hObject` - хэндл (дескриптор) который будет закрыт

__Возращаемое значение__
* Возвращает не ноль если удалось закрыт (true)
* Иначе ноль (false)

##[CreateToolhelp32Snapshot](https://msdn.microsoft.com/en-us/library/windows/desktop/ms682489(v=vs.85).aspx)
Статический срез данных, таких как, кучи, модули и потоки созданные конкретным процессом

__Параметры__
* `DWORD dwFlags` - Флаг, который указываеь какие даные будут получены в срезе данных
* `DWORD th32ProcessID` - Id процесса для которого будет получен срез данных

__Возращаемое значение__
* Если удалось получить срез данных, то возвращает его хэндл
* Иначе константу `INVALID_HANDLE_VALUE`

##[EnumThreadWindows](https://msdn.microsoft.com/ru-ru/library/windows/desktop/ms633495(v=vs.85).aspx)
Перебирает все не дочерние окна связаны с указаным потоком, передавая в пользовательскую callback функцию хэндл (дескриптор) каждого окна. 
EnumThreadWindows продолжается до тех пор, пока не будет возвращен false

__Параметры__ 
* `DWORD dwThreadId` - Id потока
* `WNDENUMPROC lpfn` - Указатель на пользовательскую функцию
* `LPARAM lParam` - Передаваемый параметр в пользовательскую функцию

__Возращаемое значение__
* Возвращает true для всех окон текущего потока
* Возвращает false если нет окон у текущего потока

##[ExtractIcon](https://msdn.microsoft.com/en-us/library/windows/desktop/ms648068(v=vs.85).aspx)
Получает хэндл иконки из исполняемого файла (exe), динамически загружаемой библиотеки (DLL) или файла иконки.

__Параметры__
* `HINSTANCE hInst` - Хэндл (дескриптор) на экземпляр приложения, которое вызывает функцию
* `LPCTSTR lpszExeFileName` - Имя сполняемого файла (exe), динамически загружаемой библиотеки (DLL) или файла иконки
* `UINT nIconIndex` - Индекс иконки, которую необходимо получить (начинается с 0)

__Возращаемое значение__
* Возвращает хэндл (дескриптор) иконки.
* Возвращает 1, если файл не был исполняемым (exe), динамически загружаемой библиотеки (DLL) или иконкой
* Возвращает 0, если в файле не была найдена иконка

##[GetClassLong](https://msdn.microsoft.com/en-us/library/windows/desktop/ms633580(v=vs.85).aspx)
Получает 32-битное (4 байта) значение из структуры WNDCLASSEX, связанной с указанным окном.

__Параметры__
* `HWND hWnd` - Хэндл (дескриптор) на окно, и косвенно на класс которому принадлежит окно
* `int  nIndex` - Извлекаемое число, значение устанавливается при помощи одной из [констант](https://msdn.microsoft.com/en-us/library/windows/desktop/ms633580(v=vs.85).aspx)

__Возращаемое значение__
* Возвращает значение, если кго удалось получить
* Иначе возвращает 0

##[GetWindowText]()
Копирует текст заголовка заданого окна (если окно имеет его) в буфер

__Параметры__
* `HWND hWnd` - Хэндл (дескриптор) окна или контрола которое содержит заголовок
* `LPTSTR lpString` - Буфер в который будет помещен текст
* `int nMaxCount` - Максимальное кол-во символов, вместе с символом окончания строки, которое будут скопированы в буфер

__Возращаемое значение__
* Возвращает кол-во скопированых символов в буфер
* Возвращает 0, если возникла ошибка или контрол или окно не содержали текст

##[GlobalMemoryStatus](https://msdn.microsoft.com/en-us/library/windows/desktop/aa366586(v=vs.85).aspx)
Возвращает текущую системную информацию об текущем использовании физической и виртуальной памяти

__Параметры__
* `LPMEMORYSTATUS lpBuffer` - Указатель на структуру, в которую будет записина информация о памяти

__Возращаемое значение__
* __Функция не возвращает значене__


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
