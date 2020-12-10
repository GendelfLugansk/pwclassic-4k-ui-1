## Интерфейс Perfect World для 4k мониторов для версии игры 1.3.6 (сервер pwclassic)

Данный UI (интерфейс) предназначен только для мониторов с высоким dpi (разрешением).
Если у вас обычный монитор, элементы интерфейса будут выглядеть увеличенными в 
2 раза и плохо помещаться на экране.

Интерфейс представляет собой классический интерфейс pw с увеличенными элементами
для комфортной игры на мониторах с высоким разрешением.

### Особенности

  * Заменен шрифт чата на более-менее читаемый, так как увеличить его размер 
    не получилось (технические особенности реализации клиента pw)
    
  * Увеличен размер важных элементов интерфейса игры в 2 раза

  * Прогресс-бары каста скилов, копания подняты выше и сделаны перетаскиваемыми

  * Добавлена обводка к тексту в окне отслеживания квестов, сам текст увеличен не 
    в 2 раза, а в 1.8 (чтобы список квестов занимал немного меньше места по высоте)
    
  * Наложено затемнение 50% на мини-карту, так как увеличить размер маркеров игроков
    и пати-мемберов не получилось, и на фоне рельефа их плохо видно\
    
  * Шрифт надписи над головой установлен в Verdana 24 полужирный (для читаемости)

### Известные проблемы

  * На высоких персах имя может быть слишком низко над головой. Иногда в голове.
    К сожалению, найти способ поднять надпись не удалось
    
  * Если включить полоски хп над головами персов, они будут немного на имени.
    Источник проблемы тот же что и в предыдущем пункте

  * Мини-карта рвется на самом маленьком масштабе. Это связано с тем что клиент 
    рассчитан на некоторый максимальный размер карты в пикселях (вероятнее 
    всего 128), который очень мал для 4к-мониторов. Работе радара впрочем
    разрывы не мешают, дефект визуально-эстетический
    
  * Нельзя увеличить маркеры членов группы и других игроков на мини-карте. Размеры
  заданы в исполняемом файле клиента
    
  * Размер шрифта чата достаточно маленький и сносно читается только если установить 
    максимальный размер в настройках. Это также связано с тем как написан клиент. 
    Такая же проблема с маленьким чатом куда пишется опыт/дух
    
  * Не получилось увеличить размер цифр урона, опыта, духа над головой. Судя по всему 
    он задан в пикселях в самом исполняемом файле 
    
  * При разговоре с НИП, высота списка с вариантами ответа задана в исполняемом 
    файле и поэтому появляется прокрутка
    
  

### Сборка (или как получить готовый для установки интерфейс)

Запустить [build.bat](build.bat). В папке build появятся готовые файлы

### Установка

  * Рекомендуется сделать резервную копию всего клиента или хотя бы скопировать файлы 
    configs.pck, interfaces.pck, surfaces.pck и папку fonts из папки element оригинального 
    клиента классики
    
  * Скопировать содержимое папки build в папку element клиента классики с заменой файлов

  * В свойствах elementclient.exe и client.exe выбрать масштабирование средствами 
    приложения:
    
    ![screenshot](dpi_instr.png)

### Разработка / модификация

Все исходники в папке `src`.

Техническая информация находится в файле [заметки_на_полях.md](заметки_на_полях.md).

Кроме того, dtf файлы, назначение которых известно, имеют комментарий в первой строке.

Для тестирования результатов можно использовать[build.bat](build.bat) (для 
полного билда) либо один из [build-configs.bat](build-configs.bat), 
[build-fonts.bat](build-fonts.bat), [build-interfaces.bat](build-interfaces.bat), 
[build-surfaces.bat](build-surfaces.bat) для сборки соответствующего .pck-файла.
Отдельные батники удобны если менялось содержимое только одной папки.

Для тестирования лучше всего создать папку client и скопировать туда содержимое 
папки с клиентом pwclassic. Все батники настроены копировать туда свежесобранные 
файлы

### Поддержать автора

Можно донатом на яндекс-кошелек 
[410018805408316](https://yoomoney.ru/to/410018805408316)