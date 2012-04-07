# День первый

## Представляемся

Меня зовут Тимур Вафин, вместе со мной занятия проводит Евгений Петров. Мы работаем в компании Flatsoft.
Занимаемся разработкой проектов на Ruby и Ruby On Rails.

Мы будем вести занятия вместе, либо по очереди, возможно будем приглашать на отдельные занятия кого то еще.

## Описание факультатива

Наш факультатив называется "Введение в Ruby и Ruby On Rails".

Он будет состоять примерно из 8 занятий.

Мы постараемся рассказать о фундаментальных вещах, необходимых для понимания работы веб-приложений, расскажем поверхностно о Ruby, научимся делать простое приложение на RubyOnRails.

Для того, чтобы разобраться и понять, что мы рассказываем вам будет достаточно желания разобраться. Мы с удовольствием ответим на вопросы и поможем, если что то не будет получаться.

Цель наших курсов зародить в вас интерес к Ruby, пригласить на спец курс в 4 семестре, если вы студен, либо на более продвинутый мастер-класс, либо к нам в лабораторию, либо в идеале на стажировку к нам в компанию.

Занятия будут проходить по возможности по субботам в 11:30.

## Анкеты

Пожалуйста, заполните анкеты, чтобы могли лучше ориентироваться на ваш уровень, чтобы, возможно, подстроить соответствующим образом курс.

## Вопросы в зал

* Кто знает как включать компьютер?
* Кто как нибудь использовал компьютер раньше?
* Кто умеет пользоваться Эксель?
* Кто использовался браузером?
* Кто когда либо создавал какую либо веб страницу?
* Кто когда либо что-нибудь программировал?
* Кто нибудь программировал на PHP раньше?
* Кто нибудь программировал на других языках, Java, Perl, C/C++, Python, Ruby?

## План на сегодня

* История Ruby и Rails
* Пример простого приложения
* Как работает Веб
* Что такое Ruby
* RubyTry
* Задание

# История Ruby

Ruby был написан, чтобы сделать работу программиста проще и не заботиться о сложности работы программистом. В этот кратком введении мы рассмотрим поверхностно основные функции языка, необходимые для домашнего задания.

Многие считают, что Ruby - это новый язык программирования, но на самом деле от был создан в 1994 году разработчиком под ником Матц. - Якохиро Мацумото, японский программист. Он хотел создать язык такой же гибкий и мощный как Перл, но с большей выразительностью - более того, хотел сделать так, чтобы код был читаемым английским.

Руби родился в 94 и его аудитория быстро росла - в Японии. До 2000 года не было никакой документации кроме как на японском языке, так что если вы хотели изучить Руби, то вы могли бы рассчитывать только на себя. Дейв Томас, первопроходец гибкого программирования, был очарован Руби и решил создать документацию на английском. Он написал книгу, которую часто называют "Киркой" - библию рубли программиста, которая открыла Руби англоговорящим программистам и всему миру.

С этого момента популярность начала расти, хотя и медленно. Он стал популярным среди системных администраторов для написания различных скриптов, для различных вещей для которых используют часто Перл. Американское сообщество исчислялось сотнями с 2000-2005.

Примерно в 2004-2005 году в Чикаго компания 37 сигналов наняла молодого разработчика для разработка веб приложения. Ему дали полную свободы в выборе средств разработки, единственное он был ограничен дизайном и пользовательским интерфейсом. В то время преобладающими технологиями были PHP, Java’s JSP, and Microsoft’s ASP. Они были от части неудобными для реализации проекта, так что Девид, известный сегодня как DHH, пошел своим путем.

Он написал приложение на Руби. Он опирался на язык и на несколько библиотек, но в основном весь стек создал сам. Он и 37 сигналов и  работали над приложением, известное как Бейзкамп, и выпустили его в итоге.

Потом, когда Бейзкамп был создан, DHH выпилил веб фреймворк из приложения. Это был кардинально отличный подход от тех, что использовали обычно Сан и Майкрософт, когда фреймворк приходил в реальный мир из лабораторий. Вместо этого Рельсы были выпилены из реального рабочего приложения. Фреймворк пытался решить только необходимые проблемы, какие то дополнительный функционал реализовывался только, когда он был действительно необходим.

Такой подход выстрелил и сообщество вокруг Рельсов начало расти и растет до сих пор. Сейчас у нас есть тонны книг, куча конференций, и сотни людей нанятые разрабатывать приложения на Руби и Рельсах в таких компаниях как Ат&Ти, Наса, Гугл, Твиттр.

## Установка Руби и Рельсов

* Ссылка на слайдах http://links.flatsoft.com/ruby-env-setup
* Просто на Линукс и Маках
* Сначала просто и на Винде тоже, но когда начинаешь ставить библиотеки, связанные с нативными библиотеками, то начинаются сложности. Если есть возможность, то используйте Убунту в Виртуал Бокс.

* Демонстрация Scaffold
  создание проекта на основе уже существующих гемов.
   * пройти мимо rvm, rubygems, bundler, git, github
   * rails new
   * продемонстрировать что приложение работает по 3000 порту
   * rails generate scaffold article name:string  title:string body:text
   * rm -f public/index.html
   * показать что появились article
   * поменять что нибудь

## Как работает Веб
* WEB
  * Всемирную паутину образуют миллионы веб-серверов сети Интернет, расположенных по всему миру. Веб-сервер является программой, запускаемой на подключённом к сети компьютере и использующей протокол HTTP для передачи данных.
  * Для определения местонахождения ресурсов в сети используются единообразные локаторы ресурсов URL (англ. Uniform Resource Locator). Такие URL-локаторы сочетают в себе технологию идентификации URI и систему доменных имён DNS или непосредственно IP-адрес. 
  * DNS-сервера. способы ручного определения ip адреса. dig. 
  * файл /etc/hosts. localhost. порт 80, 8080, 443
  * curl?
  * картинка демонстрирующая все описанное

* HTTP
  * HTTP — протокол прикладного уровня передачи данных. Основой HTTP является Технология «клиент-сервер», то есть предполагается существование потребителей (клиентов), которые инициируют соединение и посылают запрос, и поставщиков (серверов), которые ожидают соединения для получения запроса, производят необходимые действия и возвращают обратно сообщение с результатом.
  * стек TCP/IP.
    * IP объединяет сегменты сети в единую сеть, обеспечивая доставку данных между любыми узлами сети. Он классифицируется как протокол третьего уровня по сетевой модели OSI. IP не гарантирует надёжной доставки пакета до адресата. версии IPv4 & IPv6;
    * TCP — это транспортный механизм, предоставляющий поток данных, с предварительной установкой соединения, за счёт этого дающий уверенность в достоверности получаемых данных, осуществляет повторный запрос данных в случае потери данных и устраняет дублирование при получении двух копий одного пакета.
  * запрос. через браузер. через curl. 
  * ответ. имитация сервера через net-cap; nc -l 5000
  * features of HTTP:
    * different types of request. GET, POST, PUT, DELETE
    * обход stateless - cookies

* HTML
* REST

### Ключевые моменты

* Request/Response cycle
* DNS Lookup
* Network ports

### Ссылки

* HTTP Status Codes: http://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html
* Apache HTTP Server: http://httpd.apache.org/
* Example HTTP Request/Response: http://www.jmarshall.com/easy/http/#requestline

## Как запустить код (1. Instructions & Interpreters)

There are two ways to run Ruby code. You can write one or more instructions in a file then run that file through the Ruby interpreter. When you’re writing a "real" program, this is the way to do it. We might have a file named my_program.rb like this:

* Слайд

Then we could run the program like this:

* Слайд

Ruby is called a scripting language or an interpreted language because it doesn’t run on the computer’s hardware directly, it first goes through the Ruby interpreter. When you run ruby my_program.rb you’re actually loading the ruby program which in turn loads your my_program.rb.

The second option is to use the Interactive Ruby Shell – IRB. When I’m programming I always have IRB open. IRB has all the same features as the regular Ruby interpreter, but it allows you to easily evaluate one or a handful of instructions and instantly see their results. I use IRB mostly for experimenting. In a regular program I might write a hundred lines of instructions. But if there’s one thing I’m not sure about I’ll flip over to IRB to test it out. Start IRB by opening a Terminal (Mac) or Command Prompt (Win) and typing irb.

## Переменные (2. Variables)

Everything needs a name so we can refer to it. A variable, like in math, is just a name for a piece of data. In Ruby, variables are very flexible and can be changed at any time. Variables are assigned using a single equals sign (=) where the right side of the equals sign is evaluated first, then the value is assigned to the variable named on the left side of the equals. 

* Слайд

The first few lines are simple if you’ve worked with any programming language before, but the last few get interesting when combining strings and numbers.

## Все объект (3. Objects, Attributes, and Methods)

In Ruby, everything is an object. Objects know information, called attributes, and they can do actions, called methods.

For an example of an object, think about you as a human being. You have attributes like height, weight, and eye color. You have methods like "walk", "run", "wash dishes", and "daydream." Different kinds of objects have different attributes and methods. 

A class is an abstract idea, it defines what all objects of that type can know and do. Think of the chair you’re sitting in. It’s not an abstract chair, it is an actual chair. We’d call this actual chair an instance - it is a realization of the idea chair. It has measurable attributes like height, color, weight. The class chair, on the other hand, has an abstract weight, color, and size – we can’t determine them ahead of time.

## Что такое строки (4. Strings)

In Ruby a string is defined as a quote (") followed by zero or more letters, numbers, or symbols and followed by another quote ("). 

Strings can be anything from "", the empty string, to really long sets of text. This whole tutorial, for instance, is stored in a string. Strings have a few important methods that we’ll use.

* length
  Call length on a string to get back the number of characters in the string. For instance "hello".length would give you back 5.
* delete
  Delete lets you specify a set of characters that should be removed from the original string. For instance, "hello".delete("l") would give you back "heo" after deleting all occurrences of "l", or "Good Morning!".delete("on") would give you "Gd Mrig"
* gsub
  Call gsub to replace a substring with a different string. For instance, "hello".gsub("ll","y yo") would give you back "hey yoo".
* split
  The split method is somewhat complex because it’s used to break a single string into a set of strings. For instance, I could call "Welcome to Ruby".split(" ") and it would find the two occurrences of " " (a blank space) and split the string at those points, giving you back a set like this: ["Welcome","to","Ruby"]

## RubyTry

* Пройти до части "Hey, Summary #1 Already"
