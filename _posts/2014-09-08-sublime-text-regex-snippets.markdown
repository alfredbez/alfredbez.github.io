---
layout: post
status: publish
published: true
title: "(Sublime Text) Regex Snippets"
author:
  display_name: alfredbez
  login: alfredbez
  email: alfred.bez@googlemail.com
  url: ''
author_login: alfredbez
author_email: alfred.bez@googlemail.com
wordpress_id: 55
wordpress_url: http://www.alfredbez.de/?p=55
date: '2014-09-08 15:19:37 +0200'
date_gmt: '2014-09-08 14:19:37 +0200'
categories:
- Workflow
tags: []
comments: []
---
Dies ist in erster Linie eine kleine Snippet-Sammlung für mich. Für Verbesserungsvorschläge und eure eigenen Snippets bin ich trotzdem dankbar.

| Regex | Beschreibung |
| ------------- | ------------- |
| \n[ ]{3,} | markiert (mindestens 3) Leerzeichen am Anfang der Zeile |
| (?<=&lt;h2&gt;).*(?=&lt;h2&gt;) | markiert den Inhalt aller h2-Tags (ohne zusätzliche Attribute) |
| (?<=:)[a-zA-Z0-9]{1,}(?=;) | findet CSS-Werte ohne Leerzeichen davor |
| (?<=\}\n)[ ]{1,} | findet eingerückte CSS-Regeln |
| \{\n[ ]{2}.*;\n\} | findet CSS-Regeln, die nur eine Regel haben (wenn der Code mit 2 Leerzeichen eingerückt ist) |
