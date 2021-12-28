---
title: "VirtualBox: как получить доступ к гостевой машине из хоста"
date: 2021-12-28T22:47:28+05:00
categories:
  - development
tags:
  - virtualbox
---
Иногда я использую VirtualBox для экспериментов с различными операционными системами, фреймворками или языками. И бывают
 ситуации, когда нужно получить доступ к виртуальной машине из основной. Например, установили в Windows VirtualBox,
 развернули в какой-нибудь Linux в котором подняли RubyOnRails/Symfony/Django, набросали веб приложение и хочется из
 браузера в Windows посмотреть на то, что получилось.

1. Выключаем виртуальную машину, если она включена
2. Идём в настройки ![vm-settings](/assets/images/2021-12-28-access-from-host-to-guest-in-virtualbox/vm-settings.jpg)
3. В разделе **"Сеть"** выбираем первый свободный сетевой адаптер, включаем и настраиваем его как **"Виртуальный адаптер хоста"** ![vm-settings](/assets/images/2021-12-28-access-from-host-to-guest-in-virtualbox/virtual-host-adapter.jpg)

Настраивал в Windows 10 с VirtualBox 6.1.