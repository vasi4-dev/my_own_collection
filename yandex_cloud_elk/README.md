# My Own Module Collection Documentation

## Описание

### NameSpace: **my_own_namespace** <br>

### CollectionName: **yandex_cloud_elk**

Коллекция, состоящая из плейбука, роли и модуля.
Модуль создаёт файл и пишет туда содержимое по заданным входным параметрам.

### Протестировано успешно.

на локалхосте - локально и через плейбук / роль

## Требования

- **ansible >= 2.7**
- **ВМ с ssh доступом или localhost**
- **python2** или **python3**

## Параметры

`path` - тип 'str' (строка) - необходимый для запуска модуля параметр, содержащий полный путь (включая название) к новому текстовому файлу.
`content` - тип 'str' (строка) - необходимый для запуска модуля параметр, содержащий содержимое для записи в файл

## Структура файлов

`/docs` - директория с документацией по коллекции
`/meta` - директория с идентификационными данными по коллекции
`/plugins` - директория с плагинами
`/roles` - директория с ролями
`playbook.yml` -плейбук для запуска роли для запуска модуля
`/plugins/modules/my_own_module.py` - сам модуль
`/roles/own` - роль для запуска модуля

## Установка из Galaxy

При помощи командной строки - в Ansible Galaxy :

```bash
ansible-galaxy collection install my_own_namespace.yandex_cloud_elk
```

Также включите её в `requirements.yml` и введите `ansible-galaxy collection install -r requirements.yml`, примерно как:

```yaml
---
collections:
  - name: my_own_namespace.yandex_cloud_elk
```

При установке коллекции из Ansible Galaxy, она не будет обновляться при обновлении `ansible` пакета. Чтобы обновить колекцию, введите:

```bash
ansible-galaxy collection install my_own_namespace.yandex_cloud_elk --upgrade
```

также пример вызова коллекции специальной версии, например, `1.0.0`:

```bash
ansible-galaxy collection install Nmy_own_namespace.yandex_cloud_elk:==1.0.0
```

Также можно установить из локального архива:

```bash
ansible-galaxy collection install <archivename>.tar.gz
```

См. [ документацию Ansible collections](https://docs.ansible.com/ansible/devel/user_guide/collections_using.html) по всем коллекциям

## Поддержка коллекции

The current maintainers are listed in the [MAINTAINERS](MAINTAINERS) file. If you have questions or need help, feel free to mention them in the proposals.

To learn how to maintain/become a maintainer of this collection, refer to the [Maintainer guidelines](https://docs.ansible.com/ansible/devel/community/maintainers.html).

It is necessary for maintainers of this collection to be subscribed to:

- The collection itself (the `Watch` button -> `All Activity` in the upper right corner of the repository's homepage).
- The [news-for-maintainers repository](https://github.com/ansible-collections/news-for-maintainers).

They also should be subscribed to Ansible's [The Bullhorn newsletter](https://docs.ansible.com/ansible/devel/community/communication.html#the-bullhorn).

## Release notes

Ссылка на [changelog](https://github.com/ansible-collections/REPONAMEHERE/tree/main/CHANGELOG.rst).

## Лицензирование

<!-- Include the appropriate license information here and a pointer to the full licensing details. If the collection contains modules migrated from the ansible/ansible repo, you must use the same license that existed in the ansible/ansible repo. See the GNU license example below. -->

GNU General Public License v3.0 иил более поздняя.

Лицензия [LICENSE](https://www.gnu.org/licenses/gpl-3.0.txt)
