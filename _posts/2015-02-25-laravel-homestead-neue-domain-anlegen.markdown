---
layout: post
status: publish
published: true
title: 'Laravel Homestead: neue Domain anlegen'
author:
  display_name: alfredbez
  login: alfredbez
  email: alfred.bez@googlemail.com
  url: ''
author_login: alfredbez
author_email: alfred.bez@googlemail.com
excerpt: Hier zeige ich, wie man eine neue Domain zu einer bestehenden Homestead-Box hinzufügen kann
wordpress_id: 80
wordpress_url: http://www.alfredbez.de/?p=80
date: '2015-02-25 11:35:53 +0100'
date_gmt: '2015-02-25 10:35:53 +0100'
categories:
- Anleitungen
tags:
- Laravel
comments: []
---
Was ist [Laravel Homestead](http://laravel.com/docs/5.1/homestead)?

Zitat von der offiziellen Seite:
> Laravel Homestead is an official, pre-packaged Vagrant "box" that provides you a wonderful development environment without requiring you to install PHP, HHVM, a web server, and any other server software on your local machine. No more worrying about messing up your operating system! Vagrant boxes are completely disposable. If something goes wrong, you can destroy and re-create the box in minutes!
> Homestead runs on any Windows, Mac, or Linux system, and includes the Nginx web server, PHP 5.6, MySQL, Postgres, Redis, Memcached, and all of the other goodies you need to develop amazing Laravel applications.

Homestead bietet also eine saubere, fertig eingerichtete virtuelle Maschine, die bei der Entwicklung oder auch zum Testen sehr nützlich ist.
Ich nutze Homestead für Projekte aller Art: natürlich Laravel, aber auch TYPO3 und OXID.
Jeffrey Way, <a href="https://twitter.com/monooso/status/458346894927081472" target="_blank">PHP's killer feature<&#47;a>, hat in seinem <a href="https:&#47;&#47;laracasts.com&#47;series&#47;laravel-5-fundamentals&#47;episodes&#47;2" target="_blank">fast 11 Minuten langem (bzw kurzem) Video<&#47;a> das Wichtigste einfach zusammengefasst.
Ich hatte allerdings Probleme beim Hinzufügen von Domains zu einer bestehenden Box gehabt.
In diesem Beispiel zeige ich, wie ich den Ordner <strong>&#47;home&#47;vagrant&#47;Code&#47;neue-seite<&#47;strong> auf die Domain <strong>neue-seite.app<&#47;strong> mappe.
Folgende Schritte haben mir geholfen:
<strong>1. Konfiguration der Box &ouml;ffnen und bearbeiten:<&#47;strong>
Im Terminal<br />
<code>homestead edit<&#47;code><br />
eingeben.
Dies &ouml;ffnet die Datei <em>Homestead.yaml<&#47;em>
Hier legt man unterhalb von <strong>sites<&#47;strong> einen neuen Eintrag an und gibt den entsprechenden Ordner an. Eventuell fügt man unter <strong>folders<&#47;strong> einen neuen Ordner hinzu.
Beispieleintrag:<br />
<code>sites:<br />
&nbsp;&nbsp;&nbsp;&nbsp;- map: neue-seite.app<br />
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;to: &#47;home&#47;vagrant&#47;Code&#47;neue-seite<br />
<&#47;code>
<strong>2. Eintrag in hosts-Datei einfügen:<&#47;strong>
Die hosts-Datei findet ihr hier:
Windows: C:\Windows\System32\Drivers\etc\hosts<br />
Linux&#47;OS X: &#47;etc&#47;hosts
Dort tr&auml;gt man folgendes ein (Beispieleintrag):<br />
<code>192.168.10.10 neue-seite.app<&#47;code>
Die IP-Adresse findet ihr in der <em>Homestead.yaml<&#47;em> (siehe Schritt 1).
<strong>3. Box neu starten:<&#47;strong><br />
Solltet ihr eine SSH Verbindung zu Homestead haben, muss diese unterbrochen werden. Dann muss man diese beiden Befehle ins Terminal eingeben:<br />
<code>homestead destroy<br />
homestead up<br />
<&#47;code>
