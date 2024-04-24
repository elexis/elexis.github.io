---
layout: page
title: Fehler auf der Website 
language: de 
order: 8 
language_reference: error 
published: true
---

{{ page.title }} {#title}
----------

Fehler/Anregung können Sie an den Betreuer dieser Webseite [Niklaus Giger](mailto:niklaus.giger@member.fsf.org) schicken.


Es ist auch möglich, den Quellcode dieser Seite zu betrachten und grössere Anpassungen lokal zu testen. Dazu brauchen Sie installierte Versionen von ruby und git auf Ihrem Computer.

Danach sollten Sie mit folgenden Befehlen auf der Kommandozeile eine lauffähige Kopie erstellen. Vorausgesetzt wird eine Ruby-Version >= 2.5 und bundler.

```
git clone https://github.com/elexis/elexis.github.com.git
cd elexis.github.com
bundle install
bundle exec jekyll serve
```
Wenn alles gut geht, können Sie auf [http://127.0.0.1:4000](http://127.0.0.1:4000) eine lokale Kopie dieser Seite sehen.

Zum Übersetzen verwendet Niklaus häufig [https://www.deepl.com](https://www.deepl.com).

* Installation auf srv.elexis.info

Auf srv.elexis.info läuft ein Debian Buster und die apt-Pakete ruby und bundler sind installiert.

jekyll.service Datei nach /etc/systemd/system/jekyll.service kopiert

    git clone https://github.com/elexis/elexis.github.com.git /home/srv/elexis.info
    chown -R www-data:www-data /home/srv/elexis.info
    sudo -u www-data git pull
    cd /home/srv/elexis.info
    sudo -u www-data bundle install --path vendor/bundles
    systemctl start jekyll
    systemctl status jekyll

As jekyll-polyglot is not supported by github, we always see build failures in the github commit history which can be safely ignored, if the changes show up under elexis.info.
