---
layout: seite
title: "Anmeldung, Termine und Formalia"
permalink: /informationen/
---

<nav class="sprung" markdown="0">
<div><a href="#anmeldung">Anmeldung und Themenvergabe</a>
<a href="#vorbesprechung">Vorbesprechung</a></div>
<div><a href="#arbeit">Seminararbeit</a>
<a href="#vortrag">Seminarablauf und Vortrag</a>
<a href="#betreuung">Betreuung</a></div>
</nav>

## Kontakt und die wichtigsten Informationen im Überblick {#ueberblick}

<table class="termine" markdown="0">
{%- assign bu = site.seminar.buero | strip -%}
{%- assign sp = site.seminar.sprechstunde | strip -%}
<tr><td>Kontakt</td><td><div class="paare"><span class="f">Seminarleitung:</span><span>{{ site.lehrende_kurz | default: site.lehrende }}</span><span class="f">E&#8209;Mail:</span><span>{% include email.html form="zeilen" %}</span><span class="f">Büro:</span><span>{% if bu != "" %}{{ bu }}{% else %}wird hier ergänzt{% endif %}</span><span class="f">Sprechstunde:</span><span>{% if sp != "" %}{{ sp }}, außerdem {% endif %}nach Vereinbarung per E&#8209;Mail</span></div></td></tr>
{%- assign raum = site.seminar.raum | strip -%}
{%- assign sws = site.seminar.sws | strip -%}
{%- assign swp = site.seminar.schwerpunkt | strip -%}
<tr><td><span class="zwei">{{ site.seminar.lehrform }}{% if sws != "" %}<br><span class="sws">({{ sws }})</span>{% endif %}</span></td><td><div class="paare"><span class="f">Termin:</span><span>voraussichtlich {{ site.termine.block }}{% if site.termine.block_hinweis != "" %}; {{ site.termine.block_hinweis }}{% endif %}</span><span class="f">Raum:</span><span>{% if raum != "" %}{{ raum }}{% else %}wird hier ergänzt{% endif %}</span><span class="f">Empfohlen:</span><span>{{ site.seminar.fachsemester | replace: "; ", "<br>" }}</span>{% if swp != "" %}<span class="f">Schwerpunkt:</span><span>{{ swp | replace: "; ", "<br>" }}</span>{% endif %}</div></td></tr>
<tr><td>Anmeldung</td><td><div class="paare"><span class="f">Frist:</span><span>{{ site.termine.anmeldeschluss }}</span><span class="f">Wohin:</span><span>per E&#8209;Mail<span class="zeile"><span class="fi">an:</span>{% include email.html nur="haupt" %}</span><span class="zeile"><span class="fi">cc:</span><a href="mailto:sekretariat.europarecht@uni-leipzig.de">sekretariat.europarecht@<wbr>uni-leipzig.de</a></span></span></div></td></tr>
{%- assign vb_t = site.termine.vorbesprechung_termin | strip -%}
<tr><td>Vorbesprechung</td><td><div class="paare"><span class="f">Woche:</span><span>{{ site.termine.vorbesprechung }}</span><span class="f">Termin:</span><span>{% if vb_t != "" %}{{ vb_t }}{% else %}wird hier ergänzt{% endif %}</span><span class="f">Ort:</span><span>online</span><span class="f">Zugang:</span><span>{{ site.termine.vorbesprechung_zugang }}</span></div></td></tr>
{%- assign beginn_offen = site.termine.beginn_offen -%}
{%- assign abgabe_offen = site.termine.abgabe_offen -%}
{%- assign beginn = site.termine.bearbeitungsbeginn | strip -%}
{%- assign abg_z = site.termine.abgabe_zulassung | strip -%}
{%- assign abg_p = site.termine.abgabe_pruefung | strip -%}
<tr><td>Bearbeitungszeit</td><td><div class="paare"><span class="f">Beginn:</span><span>{% if beginn != "" %}{{ beginn }}{% else %}{{ beginn_offen | replace: "; ", "<br>" }}{% endif %}</span><span class="f">ZS:</span><span>9&nbsp;Wochen</span><span class="f">PS:</span><span>8&nbsp;Wochen</span></div></td></tr>
<tr><td>Umfang</td><td><div class="paare"><span class="f">ZS:</span><span>35.000–50.000&nbsp;Zeichen, etwa 10–15&nbsp;Seiten</span><span class="f">PS:</span><span>45.000–65.000&nbsp;Zeichen, etwa 14–20&nbsp;Seiten</span></div></td></tr>
<tr><td>Abgabe</td><td><div class="paare">{% if abg_z != "" or abg_p != "" %}<span class="f">ZS:</span><span>{% if abg_z != "" %}{{ abg_z }}{% else %}{{ abgabe_offen }}{% endif %}</span><span class="f">PS:</span><span>{% if abg_p != "" %}{{ abg_p }}{% else %}{{ abgabe_offen }}{% endif %}</span>{% else %}<span class="f">Termin:</span><span>{{ abgabe_offen }}</span>{% endif %}<span class="f">Wohin:</span><span>als PDF und docx<span class="zeile"><span class="fi">an:</span><a href="mailto:sekretariat.europarecht@uni-leipzig.de">sekretariat.europarecht@<wbr>uni-leipzig.de</a></span><span class="zeile"><span class="fi">cc:</span>{% include email.html nur="haupt" %}</span>gedruckt im Sekretariat der Professur<br>(Burgstraße&nbsp;21, Raum&nbsp;1.26)</span></div></td></tr>
{%- assign mo = site.seminar.moodle | strip -%}
</table>

<p class="mehr" markdown="0">{% if mo != "" %}<a href="{{ mo }}">Zum Moodle-Kurs des Seminars <span class="weiterpfeil">→</span></a>{% else %}Der Link zum Moodle-Kurs wird hier ergänzt{% endif %}</p>

## Anmeldung und Themenvergabe <a href="#seitenanfang" class="hoch" aria-label="Zum Seitenanfang">↑</a> {#anmeldung}

Das Seminar steht Studierenden aller Schwerpunktbereiche als Zulassungsseminar (ZS) offen. Als Prüfungsseminar (PS) ist es dem Schwerpunktbereich&nbsp;4 zugeordnet; eine Zuordnung zu anderen Schwerpunktbereichen ist nach Absprache möglich. Für das Zulassungsseminar ist die Teilnahme ab dem 5.&nbsp;Fachsemester empfohlen, für das Prüfungsseminar ab dem 6.

Die Anmeldung ist ab sofort bis **{{ site.termine.anmeldeschluss }}** per E&#8209;Mail möglich:

<div class="paare schmal" markdown="0"><span class="f">an:</span><span>{% include email.html nur="haupt" %}</span><span class="f">cc:</span><span><a href="mailto:sekretariat.europarecht@uni-leipzig.de">sekretariat.europarecht@<wbr>uni-leipzig.de</a></span></div>

Bitte geben Sie dabei Folgendes an:

- Name, Matrikelnummer, Fachsemester und E&#8209;Mail Adresse
- Schwerpunktbereich, gegebenenfalls den voraussichtlichen
- ob Sie ein Zulassungs- oder ein Prüfungsseminar schreiben
- bis zu drei Themenwünsche mit Nummer und Titel, in der Reihenfolge Ihrer Präferenz
- ob Sie zugleich einen Schlüsselqualifikationsnachweis erwerben möchten

Für das Prüfungsseminar brauchen Sie die Zulassung zur Schwerpunktbereichsprüfung; diese erteilt das Studienbüro. Das Formular zur Anmeldung des Prüfungsseminars können Sie nachreichen.

Melden sich mehr Interessierte, als Themen zur Verfügung stehen, gilt folgende Reihenfolge: Teilnahme am Prüfungsseminar, Zugehörigkeit zum Schwerpunktbereich, Zeitpunkt der Anmeldung.

Über die Themenvergabe verständigen wir uns in der Vorbesprechung. Manche Themen lassen mehr als eine Bearbeitung zu; in diesen Fällen wird der Zuschnitt bei der Vergabe festgelegt.

Wenn Sie sich für ein Thema interessieren oder Fragen zur Themenwahl haben, schreiben Sie mir gerne schon vorher unter {% include email.html nur="haupt" %}.

## Vorbesprechung <a href="#seitenanfang" class="hoch" aria-label="Zum Seitenanfang">↑</a> {#vorbesprechung}

Die Vorbesprechung findet in der Woche vom **{{ site.termine.vorbesprechung }}** online statt. Der genaue Termin wird hier bekanntgegeben; die Zugangsdaten erhalten Sie nach Ablauf der Anmeldefrist per E&#8209;Mail.

Die Anwesenheit in der Vorbesprechung ist Voraussetzung für die Teilnahme am Seminar. Wenn Sie verhindert sind, melden Sie sich bitte vorab bei mir.

## Seminararbeit <a href="#seitenanfang" class="hoch" aria-label="Zum Seitenanfang">↑</a> {#arbeit}

### Formalia: Umfang, Fristen und Abgabe

<div class="formalia" markdown="0">
<div><p class="typ">Zulassungsseminar (ZS)</p><dl><dt>Bearbeitungszeit</dt><dd>9&nbsp;Wochen</dd><dt>Umfang</dt><dd>35.000–50.000&nbsp;Zeichen<br>(etwa 10–15&nbsp;Seiten)</dd></dl></div>
<div><p class="typ">Prüfungsseminar (PS)</p><dl><dt>Bearbeitungszeit</dt><dd>8&nbsp;Wochen</dd><dt>Umfang</dt><dd>45.000–65.000&nbsp;Zeichen<br>(etwa 14–20&nbsp;Seiten)</dd></dl></div>
</div>

Der Umfang versteht sich einschließlich Fußnoten und Leerzeichen. Titelseite, Gliederung und Verzeichnisse zählen nicht mit. Maßgeblich ist die Zeichenzahl; die Seitenangaben sind nur Anhaltspunkte und gehen von 12&nbsp;Punkt bei 1,5&#8209;zeiligem Abstand aus. Die Bearbeitungszeit beginnt mit der endgültigen Themenzuteilung.

Eine Verlängerung der Bearbeitungszeit für die Prüfungsseminararbeit kann unter Nennung besonderer Gründe auf Antrag gewährt werden. Richten Sie solche Anträge bitte per E&#8209;Mail an mich ({% include email.html nur="haupt" %}).

Die Arbeit reichen Sie **als PDF und als docx-Datei** per E&#8209;Mail ein:

<div class="paare schmal" markdown="0"><span class="f">an:</span><span><a href="mailto:sekretariat.europarecht@uni-leipzig.de">sekretariat.europarecht@<wbr>uni-leipzig.de</a></span><span class="f">cc:</span><span>{% include email.html nur="haupt" %}</span></div>

Die gedruckte Ausfertigung geben Sie bitte im Sekretariat der Professur ab (Burgstraße&nbsp;21, Raum&nbsp;1.26).

Wird die Arbeit als Prüfungsleistung erbracht, ist dies bei der Themenvergabe anzuzeigen und auf dem Deckblatt der Arbeit anzugeben. Hierzu muss die Zulassung zur Schwerpunktbereichsprüfung vorliegen; das für die Anmeldung zum Prüfungsseminar erforderliche Formular ist nachzureichen.

### Was inhaltlich erwartet wird

Die Themen sind bewusst weit gefasst. Sie erfordern eine Eingrenzung, und welchen Ausschnitt Sie wählen, ist bereits Teil der wissenschaftlichen Leistung. Die auf den Themenseiten verlinkten Kurzbeiträge sind als Einstieg gedacht: Sie verschaffen einen Überblick über die Fragen und Streitpunkte und verweisen häufig auf die einschlägige Literatur und die Grundsatzentscheidungen. Von dort aus setzen Sie eigene Schwerpunkte und ziehen weitere Literatur heran.

Die Arbeit ist selbstständig zu erstellen. Erwartet wird keine erschöpfende Darstellung, sondern eine eigene Fragestellung und eine durchgeführte Argumentation. Arbeiten Sie dafür mit den Primärquellen und mit der Sekundärliteratur und setzen Sie sich mit den Gegenpositionen auseinander. Eine eigene Position ist ausdrücklich willkommen; sie muss nichts Neues erfinden, sondern nachvollziehbar begründet sein. Die Zitierweise ist frei, sollte aber einheitlich sein. Wichtiger als das System ist, dass man Ihren Nachweisen folgen kann.

Einige der verlinkten Kurzbeiträge liegen hinter einer Bezahlschranke. Wenn Sie Zugang benötigen und ihn über die Universität Leipzig nicht bekommen, melden Sie sich gerne bei mir. Das gilt nicht nur für die verlinkten Beiträge, sondern für Literatur allgemein: Wenn Sie an etwas nicht herankommen, schreiben Sie mir, wir finden meist eine Lösung.

## Seminarablauf und Vortrag <a href="#seitenanfang" class="hoch" aria-label="Zum Seitenanfang">↑</a> {#vortrag}

Das Seminar findet als Blockveranstaltung statt, voraussichtlich **{{ site.termine.block }}**. Die genauen Termine und der Raum werden hier bekanntgegeben.

Im Seminar stellen Sie den Inhalt Ihrer Arbeit in einem mündlichen Vortrag vor und verteidigen ihn in der anschließenden Diskussion. Der Vortrag dauert **20&nbsp;bis&nbsp;25&nbsp;Minuten**.

Für das Blockseminar besteht grundsätzlich **Anwesenheitspflicht**; wenn Sie verhindert sind, melden Sie sich bitte vorab bei mir. Auch die Teilnahme an den Diskussionen der anderen Vorträge gehört zur Seminarleistung.

## Betreuung <a href="#seitenanfang" class="hoch" aria-label="Zum Seitenanfang">↑</a> {#betreuung}

Für Rücksprachen stehe ich Ihnen nach Terminvereinbarung per E&#8209;Mail zur Verfügung ({% include email.html nur="haupt" %}). Eine erste Rücksprache ist sinnvoll, wenn Sie sich einen Überblick verschafft und eine erste Eingrenzung vorgenommen haben.

Wenn Sie eine Rückmeldung zu Ihrer Gliederung möchten, schicken Sie sie mir gerne. Am sinnvollsten ist das, solange Sie noch nicht schreiben, denn an der Gliederung zeigt sich früh, ob der Zuschnitt trägt.
