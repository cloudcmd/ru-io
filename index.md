---
layout: default
---
Cloud Commander 0.7.0 [![NPM version][NPMIMGURL]][NPMURL] [![Dependency Status][DependencyStatusIMGURL]][DependencyStatusURL] [![Build Status][BuildStatusIMGURL]][BuildStatusURL]
===============
###[Главная][MainURL] [Блог][BlogURL] Демо(![IO][IO_LIVE_IMG] [IO][IOURL], ![JitSu][JitSu_LIVE_IMG] [JitSu][JitSuURL], ![Heroku][Heroku_LIVE_IMG] [Heroku][HerokuURL] ![RunKite][RunKite_LIVE_IMG] [RunKite][RunKiteURL])
[NPMIMGURL]:                https://badge.fury.io/js/cloudcmd.png
[BuildStatusIMGURL]:        https://secure.travis-ci.org/coderaiser/cloudcmd.png?branch=master
[DependencyStatusIMGURL]:   https://gemnasium.com/coderaiser/cloudcmd.png
[FlattrIMGURL]:             http://api.flattr.com/button/flattr-badge-large.png
[NPMURL]:                   http://badge.fury.io/js/cloudcmd
[BuildStatusURL]:           http://travis-ci.org/coderaiser/cloudcmd  "Build Status"
[DependencyStatusURL]:      https://gemnasium.com/coderaiser/cloudcmd "Dependency Status"
[FlattrURL]:                https://flattr.com/submit/auto?user_id=coderaiser&url=github.com/coderaiser/cloudcmd&title=cloudcmd&language=&tags=github&category=software
[NPM_INFO_URL]:             https://npmjs.org/package/cloudcmd "npm"
[MainURL]:                  http://cloudcmd.io "Главная"
[BlogURL]:                  http://blog.cloudcmd.io "Блог"
[DemoURL]:                  http://io.cloudcmd.io "Демо"
[IOURL]:                    http://io.cloudcmd.io "IO"
[JitSuURL]:                 http://cloudcmd.jit.su "JitSu"
[HerokuURL]:                http://cloudcmd.herokuapp.com/ "Heroku"
[RunKiteURL]:               http://cloudcmd.apps.runkite.com/ "RunKite"
[RunKiteURL]:               http://cloudcmd.apps.runkite.com/ "RunKite"
[IO_LIVE_IMG]:              https://status-ok.cloudcmd.io/host/io.cloudcmd.io/fs?json "IO"
[JitSu_LIVE_IMG]:           https://status-ok.cloudcmd.io/host/cloudcmd.jit.su/fs?json "JitSu"
[HEROKU_LIVE_IMG]:          https://status-ok.cloudcmd.io/host/cloudcmd.herokuapp.com/fs?json "Heroku"
[RunKite_LIVE_IMG]:         https://status-ok.cloudcmd.io/host/cloudcmd.apps.runkite.com/fs?json "RunKite"

**Cloud Commander** - облачный файловый менеджер с консолью и редактором.

![Cloud Commander](http://cloudcmd.io/img/logo/cloudcmd.png "Cloud Commander")

[![Flattr][FlattrIMGURL]][FlattrURL]

Преимущества
---------------
- Открытый код.
- Две классические панели.
- Работает под Windows, Linux и Mac OS.
- Может использоваться локально или удаленно.
- Имеет консоль и редактор.
- Написан на JavaScript/Node.js.

Установка
---------------
[![NPM_INFO][NPM_INFO_IMG]][NPM_INFO_URL]

Установить **Cloud Commander** очень просто (проще простого).
Всё что вам нужно сделать: 

- установить [node.js](//nodejs.org/ "node.js")
- [скачать](https://github.com/coderaiser/cloudcmd/archive/master.zip)
и распокавать или просто клонировать репозиторий с github:

```
    git clone git://github.com/coderaiser/cloudcmd.git
    cd cloudcmd
    node cloudcmd
```
или установить в npm:
```
    npm i cloudcmd -g
    cloudcmd
```

Гарячие клавиши
---------------
Гарячие клавии работают во всех современных веб браузерах (кроме IE - он особенный).
Вот краткий список:

- **F1**                - помощ
- **F2**                - переименовать текущий файл
- **F3**                - просмотр
- **F4**                - редактировать
- **F5**                - копировать
- **F6**                - переименовать/переместить
- **F7**                - новая папка
- **F8, Delete**        - удалить текущий файл
- **F9**                - меню
- **Ctrl + r**          - обновить содержимое папки
- **Ctrl + d**          - очистить (локальный) кэш(включая содержимое папки (папок?!))
- **Alt  + q**          - отключить привязку клавиш
- **Alt  + s**          - вернуть все привязки клавиш
- **Ctrl + A**          - выбрать(выделить) все файлы на панели
- **up, down, enter**   - перемещение по файловой системе
- **Tab**               - переключение между панелями
- **Page Up**           - вверх на одну страницу
- **Page Down**         - вниз на одну страницу
- **Home**              - в начало списка
- **End**               - в конец списка
- **Shift + Delete**    - удалить без запроса о подтверждении
- **Insert**            - выбрать(выделить) текущий файл
- **Shift + F10**       - контекстное меню
- **~**                 - консоль

Гарячие клавиши просмотра
---------------
- **F3**                - открыть
- **Esc**               - закрыть

Гарячие клавиши редактирования
---------------
- **F4**                - открыть
- **Ctrl + s**          - сохранить
- **Esc**               - закрыть

Меню
---------------
Щелчок правой кнопкой мыши вызывает контекстное меню с такими пунктами:

- Просмотр
- Правка (редактирование)
- Переименовать
- Удалить
- Выгрузить в (Dropbox, Github, GDrive)
- Загрузить
- Новый (Файл, Папка, с облака)

Настройки
---------------
Все основные настройки, можна осуществлять в config.json.

```js
{
    "api_url"   :"/api/v1",
    "appcache"  : false,            /* html5 feature appcache                   */
    "cache"     : true,             /* cashing on a client                      */
    "minification" : {              /* minification of js,css,html and img      */
        "js"    : false,            /* minify module neaded                     */
        "css"   : false,            /* npm i minify                             */
        "html"  : true,
        "img"   : false
    },
    "show_keys_panel" : true,       /* show classic panel with buttons of keys  */
    "server"    : true,             /* server mode or testing mode              */
    "logs"      : false,            /* logs or console ouput                    */
    "socket"    : true              /* enable web sockets                       */
    "port"      : 80,               /* http port or null(default)               */
    "sslPort"   : 443,              /* https port or null(default)              */
    "ip"        : "127.0.0.1",      /* ip or null(default)                      */
    "ssl"       : true              /* should use https?                        */
    "rest"      : true              /* enable rest interface                    */
}
```

Server
---------------
Standard practices say no non-root process gets to talk to
the Internet on a port less than 1024. Anyway I suggest you
to start Cloud Commander as non-root. How it could be solved?
There is a couple easy and fast ways. One of them is port forwarding by iptables.
Just run [shell/addtables.sh](shell/addtables.sh) for default options.

    @:/tmp/cloudcmd (dev) $ sudo iptables -t nat -L # look rules before
    @:/tmp/cloudcmd (dev) $ sudo iptables -t nat -A PREROUTING -p tcp --dport 80 -j REDIRECT --to-ports 8000
    @:/tmp/cloudcmd (dev) $ sudo iptables -t nat -A PREROUTING -p tcp --dport 443 -j REDIRECT --to-ports 4430
    @:/tmp/cloudcmd (dev) $ sudo iptables -t nat -L # look reles after

You should see somethins like this ( **8000** and **4430** should be in config as **port** and **sslPort** )

    target     prot opt source               destination
    REDIRECT   tcp  --  anywhere             anywhere             tcp dpt:http redir ports 8000
    REDIRECT   tcp  --  anywhere             anywhere             tcp dpt:https redir ports 4430

Если захотите все вернуть на свои места, просто очистите правила ( **1** and **2** it's rules numbers,
in your list they could differ).

```sh
@:/tmp/cloudcmd (dev) $ sudo iptables -t nat -D PREROUTING 1
@:/tmp/cloudcmd (dev) $ sudo iptables -t nat -D PREROUTING 2
```

To run Cloud Commander as daemon in linux you could set **log** to true in config and
do something like this:
    
    nohup node cloudcmd

Authorization
---------------
Thru openID Cloud Commander could authorize clients on GitHub.
All things that should be done is must be added **id** and **secret** of application
from github settings page and added to **config.json** (id just) and env varible (secret)
with names: *github_id*, *github_secret*, *dropbox_key*, *dropbox_secret* etc.
For more information see **config.json** and **shell/seret.bat** *(on win32)*
or **shell/secret.sh** *(on nix)*.


Запуск
---------------
Что бы запустить **Cloud Commander** нужна всего одна команда:
    
    node cloudcmd

для windows:

    cloudcmd

После чего Cloud Commander прочитает конфигурационный файл **config.json** и запустит сервер
на 80-ом порту, if none of port varibles(*cloud9*, *cloudfoundry* and *nodester*)
isn't exist.
Затем набирайте в браузере

    http://127.0.0.1
    
или

    http://localhost

Обновление
---------------
**Cloud Commander** обновляется часто.
Обновление происходит автоматически, так же это можно сделать в ручную
вводя несколько команд в папке cloudcmd:

    git pull
    
или проверить доступность новой версии в npm

    npm info cloudcmd

и затем, если новая версия доступна

    npm r cloudcmd
    npm i cloudcmd

Дополнительные модули
---------------
**Серверная Сторона Cloud Commander** не использует дополнительных модулей для основного функционала.
Но для минификации и оптимизации можна назначить (и установить) следующие модули:
[Minify] (https://github.com/coderaiser/minify "Minify")
и [socket.io] (https://github.com/LearnBoost/socket.io "Socket.IO").

Что бы установить дополнительные модули (наберите в папке **Cloud Commander**):

    npm i

Расширения
---------------
**Cloud Commander** desinged to easily porting extensions.
Для расширения основного функционала Cloud Commander использует следующие модули:

- [Ace]                     [AceURL]
- [FancyBox]                [FancyBoxURL]
- [jQuery-contextMenu]      [jQuery-contextMenuURL]
- [jq-console]              [jq-consoleURL]
- [github]                  [githubURL]
- [dropbox-js]              [dropbox-jsURL]
- [jquery]                  [jqueryURL]

[AceURL]:                   //ace.ajax.org/ "Ace"
[FancyBoxURL]:              //github.com/fancyapps/fancyBox "FancyBox"
[jQuery-contextMenuURL]:    //github.com/medialize/jQuery-contextMenu "jQuery-contextMenu"
[jq-consoleURL]:            //github.com/replit/jq-console‎ "jq-console"
[githubURL]:                //github.com/michael/github "github"
[dropbox-jsURL]:            //github.com/dropbox/dropbox-js "dropbox-js"
[jqueryURL]:                //jquery.com

Присоединиться к проэкту
---------------
Если вы желаете присоединиться к проэкту - направьте pull запрос в dev ветку.
Получение dev версии **Cloud Commander**:

    git clone git://github.com/coderaiser/cloudcmd.git
    git checkout dev

Возможно Вам понадобится dev версия Minify,
в таком случае наберите следующие команды:

    cd node_modules
    rm -rf minify
    git clone git://github.com/coderaiser/minify
    git checkout dev

История версий
---------------
- *2013.12.09*, **[v0.7.0](//github.com/cloudcmd/archive/raw/master/cloudcmd-v0.7.0.zip)**
- *2013.11.08*, **[v0.6.0](//github.com/cloudcmd/archive/raw/master/cloudcmd-v0.6.0.zip)**
- *2013.10.17*, **[v0.5.0](//github.com/cloudcmd/archive/raw/master/cloudcmd-v0.5.0.zip)**
- *2013.11.08*, **[v0.6.0](//github.com/cloudcmd/archive/raw/master/cloudcmd-v0.6.0.zip)**
- *2013.10.17*, **[v0.5.0](//github.com/cloudcmd/archive/raw/master/cloudcmd-v0.5.0.zip)**
- *2013.09.27*, **[v0.4.0](//github.com/cloudcmd/archive/raw/master/cloudcmd-v0.4.0.zip)**
- *2013.07.01*, **[v0.3.0](//github.com/cloudcmd/archive/raw/master/cloudcmd-v0.3.0.zip)**
- *2013.04.22*, **[v0.2.0](//github.com/cloudcmd/archive/raw/master/cloudcmd-v0.2.0.zip)**
- *2013.03.01*, **[v0.1.9](//github.com/cloudcmd/archive/raw/master/cloudcmd-v0.1.9.zip)**
- *2012.12.12*, **[v0.1.8](//github.com/cloudcmd/archive/raw/master/cloudcmd-v0.1.8.zip)**
- *2012.10.01*, **[v0.1.7](//github.com/cloudcmd/archive/raw/master/cloudcmd-v0.1.7.zip)**
- *2012.08.24*, **[v0.1.6](//github.com/cloudcmd/archive/raw/master/cloudcmd-v0.1.6.zip)**
- *2012.08.06*, **[v0.1.5](//github.com/cloudcmd/archive/raw/master/cloudcmd-v0.1.5.zip)**
- *2012.07.27*, **[v0.1.4](//github.com/cloudcmd/archive/raw/master/cloudcmd-v0.1.4.zip)**
- *2012.07.19*, **[v0.1.3](//github.com/cloudcmd/archive/raw/master/cloudcmd-v0.1.3.zip)**
- *2012.07.14*, **[v0.1.2](//github.com/cloudcmd/archive/raw/master/cloudcmd-v0.1.2.zip)**
- *2012.07.11*, **[v0.1.1](//github.com/cloudcmd/archive/raw/master/cloudcmd-v0.1.1.zip)**
- *2012.00.00*, **[v0.1.0](//github.com/cloudcmd/archive/raw/master/cloudcmd-v0.1.0.zip)**

Лицензия
---------------
MIT [license](LICENSE "лицензия").

Особая благодарность:
---------------
- [Polietilena](http://polietilena.github.io/ "Polietilena") за [logo](img/logo/cloudcmd.png "logo") и [favicon](img/favicon/favicon.png "favicon").
- [Elec-ua](https://github.com/elec-ua) за [Русский](http://ru.cloudcmd.io "Русский") и [Украинский](http://ua.cloudcmd.io "Украинский") переводы.
