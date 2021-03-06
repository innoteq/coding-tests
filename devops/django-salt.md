# Цель

Написать простое Django приложение и развернуть его с помощью SaltStack (основной акцент на развёртывание).

# Требования к Django приложению

* Оформить в виде репозитория на Github, с историей коммитов отражающей процесс разработки, добавить README
* Одна страница на простом HTML (требования к дизайну отсутствуют)
* В верхней части страницы форма - текстовое поле и кнопка "Опубликовать"
* Под формой - список опубликованных текстовых сообщений с датами их публикации, отсортированные по дате в порядке убывания (последние сверху)
* База данных - любая на выбор (sqlite, postgres, mysql)
* Код должен содержать docstrings и осмысленные комментарии, там где это уместно

# Требования к процедуре развёртывания

* Оформить в виде второго репозитория на Github, с историей коммитов отражающей процесс разработки, добавить README описывающий как разворачивать
* Среда где должно работать приложение - одна виртуалка Ubuntu 16.04 Server, настройки максимально близкие к дефолтным (по сути нужна минимальная базовая система + ssh)
* Django приложение запускаем под uwsgi, в качестве frontend сервера используем Nginx
* Развёртывание с помощью Salt SSH
* Исходники должны автоматом браться из первого репозитория
* На сервере желательно разворачивать приложение в virtualenv, но это требование не критичное
* Рецепты должны содержать осмысленные комментарии, там где это уместно

# Ожидания

* Коммуникации текстом в Slack канале
* Вопросы на понимание задания или уточнение выбранных вами вариантов реализации приветствуются
* Вы проактивно держите нас в курсе хода работ (не пропадаете надолго), например можете прислать ссылку на черновой вариант Django приложения
* Если у вас есть опыт использования указанных технологий, то больше чем один-два вечера задание у вас занять не должно. Если вы обнаружите что это занимает много времени, то вероятно вы либо осваиваете всё с нуля, либо "закапываетесь" и тогда лучше обсудить ситуацию с нами (см. предыдущий пункт)
* Комментарии и README - предпочтительно на хорошем русском нежели на плохом английском (т.е. критерий - понятность и полезность)

# Как будем смотреть задание

* Созваниваемся в Google Hangouts Meet в удобное для вас время, с вашей стороны должен работать шаринг экрана (возможно потребуется для совместного обсуждения кода)
* Mы где-то (локальная VM или какой-то хостинг провайдер) поднимаем образ Ubuntu 16.04 с известным паролем для root, и далее по инструкции из README выполняем что там написано, указав Salt'у адрес виртуалки для доступа по SSH. В итоге должны зайти на IP адрес виртуалки и увидеть работающее Django приложение.
* Закоммитив что-то в репозиторий приложения, мы должны иметь возможность с помощью определённой описанной в README процедуры иметь возможность выкатить новую версию Django приложения на виртуалку с мягким рестартом uwsgi
* Задаём вопросы, обсуждаем решение
