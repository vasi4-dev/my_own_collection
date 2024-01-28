## Нащвание роли

# OWN

## Требования

- **ansible >= 2.7**
- **ВМ с ssh доступом или localhost**
- **python2** или **python3**

## Переменные

`defaults/main.yml` :

`own-path` - тип 'str' (строка) - необходимый для запуска модуля параметр, содержащий полный путь (включая название) к новому текстовому файлу.
`own-content` - тип 'str' (строка) - необходимый для запуска модуля параметр, содержащий содержимое для записи в файл

## Dependencies

нет

## Example Playbook

Пример таски для выполнения модуля:

```yaml
- name: Check Module
  ansible.builtin.my_own_module:
    path: "/home/vs4/somefile.txt"
    content: "Hello World! Yeah! File is filled! "
```

## License

BSD

## Author Information

Github: [Vasily T.](https://github.com/vasi4-dev)
