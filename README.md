# Skins

Добавляет возможность VIP-игрокам устанавливать себе скины.

## Установка и настройка

1. Распаковать архив
2. Разместить все файлы по папкам на сервере.
3. Залить на сервер свои скины
4. Добавить файлы скинов на скачку в `addons/sourcemod/data/vip/modules/downloadlist.txt`
5. Настроить `addons/sourcemod/data/vip/modules/skins.txt`

**Параметры:** (добавить в нужные группы)

```
"Skins"        "Уникальные имена скинов"
// Пример
"Skins"        "z_t;w_all"
// Доступ ко всем скинам
"Skins"        "all"
```

Разделять можно `;` `,` `.` `*` `|`
Любым символом который не встречается в идентификаторе скинов.

Можно указать `"all"` чтобы дать доступ ко всем скинам.


В `vip_modules.phrases.txt` добавить

```
    "Skins"
    {
        "ru"    "Скины"
        "en"    "Skin"
        "fi"    "Skinit"
    }
    "Skins_Menu"
    {
        "ru"    "Выбор скина"
        "en"    "Choose skin"
        "fi"    "Skini valikko"
    }
```

### Настройка skins.txt
```
"Skins"
{
    "z_t"    // Уникальное имя скина (использовать только латинские символы и цифры)
    {
        "name"        "Зобми Т"                // Имя скина в меню
        "model"        "models/player/stenli/splitter_skinny.mdl"    // путь к модели скина
        "arms_model"    "models/player/stenli/specter_arms.mdl"    // путь к модели рук (Только для CS:GO)
        "team"        "t"                    // Команда, за которую доступен скин
    }
    "z_ct"
    {
        "name"        "Зобми CТ"
        "model"        "models/player/stenli/specter.mdl"
        "arms_model"    "models/player/stenli/specter_arms.mdl"
        "team"        "ct"
    }
    "w_all"
    {
        "name"        "The Revenant"
        "model"        "models/player/vad36wolfenstein/revenant.mdl"
        "team"        "all"
    }
}
```

В `"team"` можно указывать:
* `t`, `T` - скин за команду террористов
* `ct`, `CT` - скин за команду контр-террористов
* `ALL`, `all`, не указано - скин доступен за любую команду

