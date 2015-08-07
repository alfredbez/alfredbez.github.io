---
layout: post
status: publish
published: true
title: Einstieg in SASS
author:
  display_name: alfredbez
  login: alfredbez
  email: alfred.bez@googlemail.com
  url: ''
author_login: alfredbez
author_email: alfred.bez@googlemail.com
excerpt: "In dieser Einleitung gebe ich anhand einiger Code-Beispiele einen Einstieg
  in SASS (Syntactically Awesome Stylesheets)\r\n\r\n<blockquote>Sass is the most
  mature, stable, and powerful professional grade CSS extension language in the world.<&#47;blockquote>\r\n\r\nIch
  empfehle jedem, der SASS lernen will, einen Blick in den <i><a href=\"http:&#47;&#47;sass-lang.com&#47;guide\"
  traget=\"_blank\">Guide<&#47;a><&#47;i> und die <i><a href=\"http:&#47;&#47;sass-lang.com&#47;documentation&#47;file.SASS_REFERENCE.html\"
  target=\"_blank\">Dokumentation<&#47;a><&#47;i> zu werfen.\r\n\r\n"
wordpress_id: 70
wordpress_url: http://www.alfredbez.de/?p=70
date: '2014-12-12 11:12:39 +0100'
date_gmt: '2014-12-12 10:12:39 +0100'
categories:
- Anleitungen
tags: []
comments: []
---
<p>In dieser Einleitung gebe ich anhand einiger Code-Beispiele einen Einstieg in SASS (Syntactically Awesome Stylesheets)</p>
<blockquote><p>Sass is the most mature, stable, and powerful professional grade CSS extension language in the world.<&#47;blockquote></p>
<p>Ich empfehle jedem, der SASS lernen will, einen Blick in den <i><a href="http:&#47;&#47;sass-lang.com&#47;guide" traget="_blank">Guide<&#47;a><&#47;i> und die <i><a href="http:&#47;&#47;sass-lang.com&#47;documentation&#47;file.SASS_REFERENCE.html" target="_blank">Dokumentation<&#47;a><&#47;i> zu werfen.</p>
<p><a id="more"></a><a id="more-70"></a></p>
<p>Die Beispiele, die ich hier zeige, habe ich mit <a href="http:&#47;&#47;sassmeister.com&#47;" target="_blank">SassMeister<&#47;a> erstellt. Dort kann man ganz einfach Sass Code eingeben und sofort sehen, wie dieser in CSS umgewandelt wird. Man kann dort auch HTML schreiben, um den geschriebenen Code zu testen.</p>
<p><strong>Variablen<&#47;strong><br />
$variablenname: wert;</p>
<p class="sassmeister" data-gist-id="4e6b5b7e23aa755b0aa9" data-height="320" data-theme="tomorrow"><&#47;p><script src="http:&#47;&#47;cdn.sassmeister.com&#47;js&#47;embed.js" async><&#47;script></p>
<hr>
<p><strong>(Farb-)Funktionen<&#47;strong><br />
Eine komplette Liste der Funktionen findet man <a href="http:&#47;&#47;sass-lang.com&#47;documentation&#47;Sass&#47;Script&#47;Functions.html#lighten-instance_method" target="_blank">hier<&#47;a></p>
<p class="sassmeister" data-gist-id="7b770e04da4b436aa2c5" data-height="320" data-theme="tomorrow"><a href="http:&#47;&#47;sassmeister.com&#47;gist&#47;7b770e04da4b436aa2c5">Play with this gist on SassMeister.<&#47;a><&#47;p><script src="http:&#47;&#47;cdn.sassmeister.com&#47;js&#47;embed.js" async><&#47;script></p>
<hr>
<p><strong>Verschachtelung<&#47;strong><br />
Beim Verschachteln bitte darauf achten, dass ihr nicht mehr als drei Ebenen im resultierenden CSS habt.</p>
<p class="sassmeister" data-gist-id="041dcd36d3768b877c01" data-height="320" data-theme="tomorrow"><a href="http:&#47;&#47;sassmeister.com&#47;gist&#47;041dcd36d3768b877c01">Play with this gist on SassMeister.<&#47;a><&#47;p><script src="http:&#47;&#47;cdn.sassmeister.com&#47;js&#47;embed.js" async><&#47;script></p>
<hr>
<p><strong>Verschachtelung (2. Beispiel)<&#47;strong></p>
<p>Bei verschachtelten Elementen wird in der Regel ein Leerzeichen zwischen die Selektoren eingef&uuml;gt. Um dies zu verhindern, muss man vor den gew&uuml;nschten Selektor ein '&' einf&uuml;gen. (Stickwort 'Pseudo-Elemente' oder 'Pseudo-Klassen')</p>
<p class="sassmeister" data-gist-id="1c4e535ebf914251afe4" data-height="320" data-theme="tomorrow"><a href="http:&#47;&#47;sassmeister.com&#47;gist&#47;1c4e535ebf914251afe4">Play with this gist on SassMeister.<&#47;a><&#47;p><script src="http:&#47;&#47;cdn.sassmeister.com&#47;js&#47;embed.js" async><&#47;script></p>
<hr>
<p><strong>Mixins<&#47;strong></p>
<p>Eigene <i>Funktionen<&#47;i> in SASS</p>
<p class="sassmeister" data-gist-id="fa96e696bbcd72b0bf8f" data-height="320" data-theme="tomorrow"><a href="http:&#47;&#47;sassmeister.com&#47;gist&#47;fa96e696bbcd72b0bf8f">Play with this gist on SassMeister.<&#47;a><&#47;p><script src="http:&#47;&#47;cdn.sassmeister.com&#47;js&#47;embed.js" async><&#47;script></p>
<hr>
<p><strong>extend<&#47;strong></p>
<p>CSS-Regeln k&ouml;nnen 'vererbt' und mit eigenen Werten erweitert&#47;&uuml;berschrieben werden.</p>
<p class="sassmeister" data-gist-id="fe0a9a2ee15422bb6db3" data-height="320" data-theme="tomorrow"><a href="http:&#47;&#47;sassmeister.com&#47;gist&#47;fe0a9a2ee15422bb6db3">Play with this gist on SassMeister.<&#47;a><&#47;p><script src="http:&#47;&#47;cdn.sassmeister.com&#47;js&#47;embed.js" async><&#47;script></p>
<hr>
<p><strong>extend (placeholder)<&#47;strong></p>
<p>Placeholder verhalten sich so wie CSS-Regeln, die allerdings nicht im gerenderten CSS vorhanden sind. Placeholder sind nur f&uuml;r @extend gedacht.</p>
<p class="sassmeister" data-gist-id="a2788a58a0d9c23a5d9d" data-height="320" data-theme="tomorrow"><a href="http:&#47;&#47;sassmeister.com&#47;gist&#47;a2788a58a0d9c23a5d9d">Play with this gist on SassMeister.<&#47;a><&#47;p><script src="http:&#47;&#47;cdn.sassmeister.com&#47;js&#47;embed.js" async><&#47;script></p>
<hr>
<p><strong>Operatoren<&#47;strong></p>
<p>SASS bietet eine Reihe von Operatoren. <a href="http:&#47;&#47;sass-lang.com&#47;documentation&#47;file.SASS_REFERENCE.html#operations" target="_blank">siehe Dokumentation<&#47;a></p>
<ul>
<li>Number Operations<&#47;li>
<li>Color Operations<&#47;li>
<li>String Operations<&#47;li>
<li>Boolean Operations<&#47;li>
<li>List Operations<&#47;li><br />
<&#47;ul></p>
<p class="sassmeister" data-gist-id="0afb593d7aef40df5a22" data-height="320" data-theme="tomorrow"><a href="http:&#47;&#47;sassmeister.com&#47;gist&#47;0afb593d7aef40df5a22">Play with this gist on SassMeister.<&#47;a><&#47;p><script src="http:&#47;&#47;cdn.sassmeister.com&#47;js&#47;embed.js" async><&#47;script></p>
<hr>
<p><strong>Operatoren (erweitertes Beispiel)<&#47;strong></p>
<p class="sassmeister" data-gist-id="935bfb3d4821d8f0a574" data-height="320" data-theme="tomorrow"><a href="http:&#47;&#47;sassmeister.com&#47;gist&#47;935bfb3d4821d8f0a574">Play with this gist on SassMeister.<&#47;a><&#47;p><script src="http:&#47;&#47;cdn.sassmeister.com&#47;js&#47;embed.js" async><&#47;script></p>
