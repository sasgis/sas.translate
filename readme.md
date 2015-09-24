## Описание ##
В этом репозитории находятся файлы локализаций для программы SAS.Планета.

Имена файлов локализации соответствуют двухбуквенным кодам [ISO 639-1](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes):
`fr.po` - Французский
`ru.po` - Русский
`uk.po` - Украинский

Файл `default.po` содержит все строки на Английском языке, которые используются в программе SAS.Планета. Этот файл генерируется автоматически при помощи скрипта `GetTranslate.cmd` в исходниках SAS (см. ниже).

Файл `mergetranslate.cmd` - скрипт для актуализации файлов локализации (добавляет новые строки из `default.po`).


## Инструкция для переводчиков ##
1. Установить [TortoiseHG](http://tortoisehg.bitbucket.org/)
2. Установить [dxgettext](http://dxgettext.po.dk/) и [poEdit](https://poedit.net/)
3. Создать папку проекта, например: `sas_dev`
4. Клонировать репозиторий с исходниками SAS в папку проекта:
`hg clone https://bitbucket.org/sas_team/sas.planet.src`
5. Зарегистрироваться на https://bitbucket.org/ 
6. Сделать форк репозитория https://bitbucket.org/sas_team/sas.translate
7. Клонировать ваш форк к себе в папку проекта (замените `%you_name%` на имя вашего логина на bitbucket.org):
`hg clone https://bitbucket.org/%you_name%/sas.translate`
8. В папке с исходниками SAS запустите скрипт `sas.planet.src\Tools\GetTranslate.cmd`
9. В папке с локализациями запустите скрипт `sas.translate\mergetranslate.cmd`
10. Откройте интересующий файл локализации (*.po) в poEdit и внесите изменения в перевод. Если вы создаёте новый перевод, то скопируйте с переименованием файл `default.po` в файл с именем в соответствии с [ISO 639-1](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes).
11. Сделайте коммит в ваш локальный репозиторий:
`hg commit -m "Update localization"`
12. Отправьте изменения в ваш форк на bitbucket.org:
`hg push https://bitbucket.org/%you_name%/sas.translate`
13. Создайте пул-реквест на bitbucket.org с вашего форка в наш репозиторий


----------


Шаги 1-7 выполняются только один раз. Впоследствии, вместо этих пунктов, вам нужно просто обновлять изменения в существующих репозиториях командами:
- для sas.planet.src
    - `hg pull https://bitbucket.org/sas_team/sas.planet.src`
    - `hg update -C`
- для sas.translate
    - обновить свой форк на сайте bitbucket.org
    - `hg pull https://bitbucket.org/%you_name%/sas.translate`
    - `hg update -C`    