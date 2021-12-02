1.Найдите полный хеш и комментарий коммита, хеш которого начинается на aefea.
Решение:
git show -q aefea
Полный хэш: aefead2207ef7e2aa5dc81a34aedf0cad4c32545
Комментарий: Update CHANGELOG.md

2. Какому тегу соответствует коммит 85024d3
Решение:
git show -q 85024d3
Тег: v0.12.23

3. Сколько родителей у коммита b8d720? Напишите их хеши.
Решение:
git show -q b8d720
Данный коммит образован в результате мержа. Предки 56cd7859e и 9ea88f22f

4. Перечислите хеши и комментарии всех коммитов которые были сделаны между тегами v0.12.23 и v0.12.24.
Решение:
git log v0.12.24 --oneline

33ff1c03b (tag: v0.12.24) v0.12.24
b14b74c49 [Website] vmc provider links
3f235065b Update CHANGELOG.md
6ae64e247 registry: Fix panic when server is unreachable
5c619ca1b website: Remove links to the getting started guide's old location
06275647e Update CHANGELOG.md
d5f9411f5 command: Fix bug when using terraform login on Windows
4b6d06cc5 Update CHANGELOG.md
dd01a3507 Update CHANGELOG.md
225466bc3 Cleanup after v0.12.23 release
85024d310 (tag: v0.12.23) v0.12.23

5. Найдите коммит в котором была создана функция func providerSource, ее определение в коде выглядит так func providerSource(...) (вместо троеточего перечислены аргументы).
Решение:
git log -S 'func providerSource('
commit 8c928e83589d90a031f811fae52a81be7153e82f

6. Найдите все коммиты в которых была изменена функция globalPluginDirs
Решение:
git log --oneline -S 'globalPluginDirs'
35a058fb3 main: configure credentials from the CLI config file
c0b176109 prevent log output during init
8364383c3 Push plugin discovery down into command package

7. Кто автор функции synchronizedWriters
Решение:
Вариант 1. На мой взгляд он плохой т.к. основан на предположении.
git log -S 'synchronizedWriters' показывает в каких коммитах изменялась функция. Предполагаем что она появилась в первом коммите. Автор коммита Martin Atkins <mart@degeneration.co.uk>

Вариант 2.
Найти в каком файле эта функция.
Найти виновника изменений git blame
Не получилось. См. вопрос.