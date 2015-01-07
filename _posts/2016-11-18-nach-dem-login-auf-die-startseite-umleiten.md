---
layout: post
title:  "[OXID] Nach dem Login auf die Startseite umleiten"
date:   2016-11-18 10:38:00
categories: oxid
---

In einem aktuellen Projekt bauen wir einen Shop auf, in dem das *Private Sales Login* aktiviert ist. Der Kunde landet hierbei nach dem Login auf der Seite *Mein Konto*.

Meine Aufgabe war es, den Kunden nach dem Login auf die Startseite umzuleiten.

Das geht ganz einfach, man muss nur den gewünschten Controller im Formular angeben, in unserem Fall also der Controller `start`.

Dazu muss man in folgender Datei eine Anpassung vornehmen:

* azure: [Application/views/azure/tpl/form/login_account.tpl](https://github.com/OXID-eSales/oxideshop_ce/blob/ea93033ae0fc887be2f468c3342092341a642125/source/Application/views/azure/tpl/form/login_account.tpl#L12)
* flow: [Application/views/flow/tpl/form/login_account.tpl](https://github.com/OXID-eSales/flow_theme/blob/8b756d9412054999a6ef380808b25eb6c4769681/tpl/form/login_account.tpl#L13)

(Die Anpassung sollte man natürlich nicht direkt im `azure` oder `flow` Theme machen, sondern in dem jeweiligen Child-Theme).

**original:**
{% highlight html %}<input type="hidden" name="cl" value="[{$oViewConf->getActiveClassName()}]">{% endhighlight %}
**geändert:**
{% highlight html %}<input type="hidden" name="cl" value="start">{% endhighlight %}
