---
layout: post
status: publish
published: true
title: 'Typo3: trustedHostsPattern mit und ohne www'
author:
  display_name: alfredbez
  login: alfredbez
  email: alfred.bez@googlemail.com
  url: ''
author_login: alfredbez
author_email: alfred.bez@googlemail.com
wordpress_id: 57
wordpress_url: http://www.alfredbez.de/?p=57
date: '2014-09-09 11:17:36 +0200'
date_gmt: '2014-09-09 10:17:36 +0200'
categories:
- Anleitungen
- Typo3
tags: []
comments: []
---
<p>Am 22.05.2014 wurde die Konfigurationsoption "trustedHostsPattern" in Typo3 eingef&uuml;hrt. Hierdurch sollen "Host Spoofing"-Attacken verhindert werden. siehe dazu&nbsp;<a title="Multiple Vulnerabilities in TYPO3 CMS" href="http:&#47;&#47;typo3.org&#47;teams&#47;security&#47;security-bulletins&#47;typo3-core&#47;typo3-core-sa-2014-001&#47;" target="_blank">Multiple Vulnerabilities in TYPO3 CMS<&#47;a></p>
<p>Die Host Pattern werden in die localconf.php bzw. LocalConfiguration.php geschrieben.</p>
<p>localconf.php<br />
<strong>$GLOBALS['TYPO3_CONF_VARS']['SYS']['trustedHostsPattern'] = 'deinPattern';<&#47;strong></p>
<p>LocalConfiguration.php (innerhalb des 'SYS'-Arrays)<br />
<strong>'trustedHostsPattern' => 'deinPattern',<&#47;strong></p>
<hr &#47;>
<p>Bei den meisten Projekten ruft man die Seite &uuml;ber www.domain.de bzw. einfach &uuml;ber domain.de (ohne www) auf.<br />
Daf&uuml;r m&uuml;sst ihr als Pattern '<strong>(www\.)?domain\.de<&#47;strong>' w&auml;hlen</p>
<p><strong>UPDATE<&#47;strong> die Extension <a href="http:&#47;&#47;typo3.org&#47;extensions&#47;repository&#47;view&#47;hosts_pattern" title="hosts_pattern" target="_blank">hosts_pattern<&#47;a> generiert den Wert automatisch und spart so Zeit.</p>
