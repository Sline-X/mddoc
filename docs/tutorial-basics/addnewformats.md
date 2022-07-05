---
sidebar_position: 7
---

# Добавление новых форматов

В текущей архитектуре приложения есть особенность при добавлении новых форматов конвертаций.

Формат добавляется в HLBlock FilesFormat (Форматы файлов в админке).

Новые форматы можно добавить вручную из админки, либо миграцией

*Пример миграции*
***
> Поле UF_MIME и UF_PROGRAMS_LIST являются множественным, необходимо сериализовать 

*** 
```bash
public function up(): void
    {
        $jfifFormatData = [
            'UF_FORMAT'           => 'jfif',
            'UF_FORMAT_LIMIT'     => 30720,
            'UF_FORMAT_FULL_NAME' => 'JPEG File Interchange Format',
            'UF_CATEGORY'         => 2,
            'UF_PROGRAMS_LIST'    => serialize(['Microsoft Windows Photo Gallery Viewer']),
            'UF_VENDOR'           => 'The JPEG Committee',
            'UF_MIME'             => serialize(['image/jpeg']),
            'UF_SORT'             => 500,
            'UF_TOP'              => false,
            'UF_FORMAT_TO'        => [261, 160]
        ];
        
        FilesFormatTable::add($jfifFormatData);
    }
```

* sadasd
* asdasd
* dfgdfg

> Привет
> Серёга
> 


Это встроенная [ссылка с title элементом](http://example.com/link "Я ссылка"). Это — [без title](http://example.com/link).

А вот [пример][1] [нескольких][2] [ссылок][id] с разметкой как у сносок. Прокатит и [короткая запись][] без указания id.


Картинка без `alt` текста

![](//img/docusaurus.png)

Картинка с альтом и тайтлом:

![Alt text](//img/docusaurus.png "Можно задать title")

Запомнить просто: синтаксис как у ссылок, только перед открывающей квадратной скобкой ставится восклицательный знак.



Картинки-ссылки:

[![Alt text](//img/docusaurus.png)](https://xakep.ru/wp-content/uploads/2022/03/374986/MechKeyboard-h.jpg)



|Name                              | Command                     | 
|:---------------------------------|:----------------------------|
|Open Recent                       |Ctrl+Shift+O                 |
|Redo                              |Ctrl+Shift+Z                 |
|                                  |Alt+Shift+Backspace          |
|                                  |Ctrl+Y                       |
|Terminal                          |Alt+F12 Alt+2                |
|GIT                               |Alt+9' 'Alt+Shift+9' 'Alt+3' |
|Close                             |Ctrl+F4' 'Ctrl+W'            |
|Edit                              |Enter' 'Alt+Enter'           |
|Open Recent                       |Ctrl+Shift+O'                |
|Redo                              |Ctrl+Y'                      |
|File Structure                    |Ctrl+F12' 'Ctrl+R'           |
|Find Action                       |Ctrl+Shift+A' 'Ctrl+Shift+P' |
|Go to File                        |Ctrl+Shift+N' 'Ctrl+P'       |
|Next Highlighted Error            |Ctrl+Alt+End'                |
|Previous Next Highlighted Error   |Shift+F2' 'Ctrl+Alt+Home'    |
|New Scratch File                  |Ctrl+Alt+Insert'             |  
|Rename                            |F2'                          |
|Find→Replace                      |Ctrl+H'                      |
|Show in files                     |Ctrl+NumPad-0'               |
|Add Selection for Next Occurrence |Alt+J' 'Ctrl+Shift+D'        |
|Surround With 		               |Ctrl+Alt+T'                  |   
|					               |Ctrl+Alt+Q'                  |
|Surround with Emmet               |Ctrl+Shift+G'                |

- [ ] Mercury
- [x] Venus




