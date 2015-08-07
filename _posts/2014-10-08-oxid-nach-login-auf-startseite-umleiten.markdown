---
layout: post
status: publish
published: true
title: 'OXID: nach Login auf Startseite umleiten'
author:
  display_name: alfredbez
  login: alfredbez
  email: alfred.bez@googlemail.com
  url: ''
author_login: alfredbez
author_email: alfred.bez@googlemail.com
wordpress_id: 63
wordpress_url: http://www.alfredbez.de/?p=63
date: '2014-10-08 08:15:41 +0200'
date_gmt: '2014-10-08 07:15:41 +0200'
categories:
- OXID eShop
- Anleitungen
tags: []
comments: []
---
<p>In einem aktuellen Projekt&nbsp;bauen wir einen Shop auf, in dem das 'Private Sales Login' aktiviert ist. Der Kunde landet hierbei nach dem Login auf der Seite 'Mein Konto'.</p>
<p>Meine Aufgabe war es, den Kunden nach dem Login auf die Startseite umzuleiten.</p>
<hr &#47;>
<p>Dazu habe ich die Datei&nbsp;<strong>application&#47;views&#47;azure&#47;tpl&#47;form&#47;login_account.tpl<&#47;strong> bearbeitet.</p>
<p><strong>Zeile 12 (original):<&#47;strong></p>
<pre><input type="hidden" name="cl" value="[{ $oViewConf->getActiveClassName() }]" &#47;><&#47;pre><br />
<strong>Zeile 12 (ge&auml;ndert):<&#47;strong></p>
<pre><input type="hidden" name="cl" value="start" &#47;><&#47;pre></p>
