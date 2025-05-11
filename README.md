# Домашнее задание к занятию "`Инструменты Git`" - `Татаринцев Алексей`

---

### Задание 



1. `Клонирую репозиторий на свой копьютер`

```
git clone https://github.com/hashicorp/terraform.git
cd terraform
```

2. `Полный хеш и комментарий коммита, хеш которого начинается на aefea`
```
git show aefea --format="%H %s"
```
![1](https://github.com/Foxbeerxxx/tools_git/blob/main/img/1.png)`

3. `Какому тегу соответствует коммит 85024d3?`
```
git tag --contains 85024d3

# этот коммит присутствует в нескольких тегах
```
![2](https://github.com/Foxbeerxxx/tools_git/blob/main/img/2.png)`

4. `Сколько родителей у коммита b8d720? Напишите их хеши.`
```
git show --pretty=%P b8d720

# есть 2 родителя, это их хеши:
56cd7859e05c36c06b56d013b55a252d0bb7e158 и 9ea88f22fc6269854151c571162c5bcf958bee2b

```
![3](https://github.com/Foxbeerxxx/tools_git/blob/main/img/3.png)`

5. `Перечислите хеши и комментарии всех коммитов между тегами v0.12.23 и v0.12.24`
```
git log v0.12.23..v0.12.24 --oneline


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
```
![4](https://github.com/Foxbeerxxx/tools_git/blob/main/img/4.png)`

6. Коммит, в котором была создана функция func providerSource(...)
```
git log -S 'func providerSource(' --oneline

# Коммит 8c928e8358 (самый ранний в списке).
```
![5](https://github.com/Foxbeerxxx/tools_git/blob/main/img/5.png)`

7. Все коммиты, в которых была изменена функция globalPluginDirs
```
git log -S 'func globalPluginDirs(' --oneline
```
![6](https://github.com/Foxbeerxxx/tools_git/blob/main/img/6.png)`

8. Кто автор функции synchronizedWriters?
```
git log -S 'func synchronizedWriters(' --pretty=format:"%an"

# Автор — Martin Atkins
```
![7](https://github.com/Foxbeerxxx/tools_git/blob/main/img/7.png)`

