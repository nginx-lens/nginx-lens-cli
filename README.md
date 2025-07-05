# nginx-lens

**nginx-lens** — современный CLI-инструмент для анализа, диагностики и визуализации конфигураций Nginx.

## Зачем нужен nginx-lens?

- Быстро находит ошибки и потенциальные проблемы в ваших nginx-конфигах.
- Визуализирует маршруты и структуру — легко понять, как устроен ваш nginx.
- Показывает, какой location/server обслуживает конкретный URL.
- Анализирует логи и помогает выявить аномалии.
- Упрощает аудит, миграцию и поддержку сложных инфраструктур.

## Примеры работы

### Справочник утилиты
```bash
nginx-lens --help
```

![nginx-lens --help](docs/demo-help.svg)

### Доступность upstream-серверов
```bash
nginx-lens health <путь_к_конфигу>
```

![nginx-lens health <путь_к_конфигу>](docs/demo-health.svg)

### Древовидная визуализация структуры конфига
```bash
nginx-lens tree <путь_к_конфигу>
```

![nginx-lens tree <путь_к_конфигу>](docs/demo-tree.svg)

### Древовидная визуализация include'ов
```bash
nginx-lens include-tree <путь_к_конфигу>
```

![nginx-lens include-tree <путь_к_конфигу>](docs/demo-includetree.svg)

### Удобный анализатор логов
```bash
nginx-lens logs <путь_к_файлу_лога>
```

![nginx-lens logs <путь_к_файлу_лога>(https://asciinema.org/a/AbCdEfGhIjK.svg)](https://asciinema.org/a/AbCdEfGhIjK)

### Аудит конфигурации
```bash
nginx-lens analyze <путь_к_конфигу>
```

![nginx-lens analyze <путь_к_конфигу>](docs/demo-analyze.svg)

### Визуализация маршрутов
```bash
nginx-lens graph <путь_к_конфигу>
```

![nginx-lens graph <путь_к_конфигу>](docs/demo-graph.svg)

### Поиск маршрута для URL
```bash
nginx-lens route <URL>
```

![nginx-lens route <URL>](docs/demo-route.svg)

### Сравнение конфигов
```bash
nginx-lens diff <путь_к_первому_конфигу> <путь_к_второму_конфигу>
```

![nginx-lens diff <путь_к_первому_конфигу> <путь_к_второму_конфигу>](docs/demo-diff.svg)

### Удобная проверка синтаксиса конфига
```bash
nginx-lens syntax
```

![nginx-lens syntax](docs/demo-syntax.svg)


## Установка и системные требования

- **Python 3.8+**
- Linux/macOS (работает и под Windows WSL)

### Установка с помощью bash-скрипта (Рекомендуется)

```bash
wget https://raw.githubusercontent.com/shelovesuastra/nginx-lens/install-nginx-lens.sh
# или
curl https://raw.githubusercontent.com/shelovesuastra/nginx-lens/install-nginx-lens.sh

chmod +x install-nginx-lens.sh

./install-nginx-lens.sh
# или
sh ./install-nginx-lens.sh
# или
bash ./install-nginx-lens.sh
```

### Установка через PyPI

```bash
pipx install nginx-lens
```
или
```bash
pip install nginx-lens
```

## Автор

[Daniil Astrouski](https://github.com/shelovesuastra)

## Лицензия

MIT