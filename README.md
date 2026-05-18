# MyProject – простое консольное приложение на C#

Этот проект создан в рамках учебного задания по работе с Git в Visual Studio. Программа выводит приветствие в консоль.

## Содержание
- [О программе](#о-программе)
- [Требования](#требования)
- [Сборка и запуск](#сборка-и-запуск)
- [Управление версиями (Git)](#управление-версиями-git)
- [История изменений](#история-изменений)

## О программе

`Program.cs` – простейшее консольное приложение на C#. Оно выводит одну строку. Изначально текст был:
Console.WriteLine("Hello, World!");

text
После создания ветки `feature` и последующего слияния в `main` программа выводит:
Console.WriteLine("Hello, Feature!");

text

## Требования

- [.NET SDK](https://dotnet.microsoft.com/download) (версия 6.0 или новее)
- Visual Studio 2022 (рекомендуется) или любая другая IDE с поддержкой C#
- Git (для клонирования и управления версиями)

## Сборка и запуск

### Через Visual Studio
1. Откройте файл решения `MyProject.sln` (если есть) или просто папку с проектом.
2. Нажмите `Ctrl+F5` для запуска без отладки.

### Через командную строку
```bash
# Перейдите в папку проекта
cd MyProject

# Скомпилируйте и запустите
dotnet run
Управление версиями (Git)
Репозиторий содержит следующие ветки:

main – основная ветка, в которой находится финальная версия программы после слияния.

feature – ветка, созданная для изменения приветствия.

Выполненные действия (кратко)
bash
git init
git add Program.cs
git commit -m "Initial commit with Program.cs"
git checkout -b feature
# изменён Program.cs (Hello, World! -> Hello, Feature!)
git add Program.cs
git commit -m "Update greeting to Feature"
git checkout main
git merge feature
Просмотр истории
В Visual Studio: Git Changes → Просмотр истории.
В командной строке: git log --oneline --graph --all

История изменений
Дата	Ветка	Изменение
-	main	Начальный коммит: Console.WriteLine("Hello, World!");
-	feature	Изменено на Console.WriteLine("Hello, Feature!");
-	main	Влита ветка feature – программа теперь выводит Hello, Feature!
Проект выполнен в учебных целях. 
