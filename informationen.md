---
layout: seite
title: "Informationen zum Seminar"
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
<tr><td>Seminarleitung</td><td>{{ site.lehrende_kurz | default: site.lehrende }}</td></tr>
<tr><td>E-Mail</td><td>{% include email.html %}</td></tr>
{%- assign bu = site.seminar.buero | strip -%}
<tr><td>Büro</td><td>{% if bu != "" %}{{ bu }}{% else %}wird hier ergänzt{% endif %}</td></tr>
{%- assign sp = site.seminar.sprechstunde | strip -%}
<tr><td>Sprechstunde</td><td>{% if sp != "" %}{{ sp }}, außerdem {% endif %}nach Vereinbarung per E-Mail</td></tr>
{%- assign raum = site.seminar.raum | strip -%}
{%- assign sws = site.seminar.sws | strip -%}
{%- assign swp = site.seminar.schwerpunkt | strip -%}
<tr><td><span class="zwei">{{ site.seminar.lehrform }}{% if sws != "" %}<br><span class="sws">({{ sws }})</span>{% endif %}</span></td><td><div class="paare"><span class="f">Termin:</span><span>voraussichtlich {{ site.termine.block }}{% if site.termine.block_hinweis != "" %}; {{ site.termine.block_hinweis }}{% endif %}</span><span class="f">Raum:</span><span>{% if raum != "" %}{{ raum }}{% else %}wird hier ergänzt{% endif %}</span><span class="f">Empfohlen:</span><span>{{ site.seminar.fachsemester | replace: "; ", "<br>" }}</span>{% if swp != "" %}<span class="f">Schwerpunkt:</span><span>{{ swp | replace: "; ", "<br>" }}</span>{% endif %}</div></td></tr>
<tr><td>Anmeldung</td><td><div class="paare"><span class="f">Frist:</span><span>{{ site.termine.anmeldeschluss }}</span><span class="f">per E-Mail:</span><span><span class="zeile"><span class="fi">an:</span>{% include email.html nur="haupt" %}</span><span class="zeile"><span class="fi">cc:</span><a href="mailto:sekretariat.europarecht@uni-leipzig.de">sekretariat.europarecht@uni-leipzig.de</a></span></span></div></td></tr>
{%- assign vb_t = site.termine.vorbesprechung_termin | strip -%}
<tr><td>Vorbesprechung</td><td><div class="paare"><span class="f">Woche:</span><span>{{ site.termine.vorbesprechung }}</span><span class="f">Termin:</span><span>{% if vb_t != "" %}{{ vb_t }}{% else %}wird hier ergänzt{% endif %}</span><span class="f">Ort:</span><span>online</span><span class="f">Zugang:</span><span>{{ site.termine.vorbesprechung_zugang }}</span></div></td></tr>
{%- assign beginn_offen = site.termine.beginn_offen -%}
{%- assign abgabe_offen = site.termine.abgabe_offen -%}
{%- assign beginn = site.termine.bearbeitungsbeginn | strip -%}
{%- assign abg_z = site.termine.abgabe_zulassung | strip -%}
{%- assign abg_p = site.termine.abgabe_pruefung | strip -%}
<tr><td>Bearbeitungszeit</td><td><div class="paare"><span class="f">ZS:</span><span>9 Wochen</span><span class="f">PS:</span><span>8 Wochen</span><span class="f">Beginn:</span><span>{% if beginn != "" %}{{ beginn }}{% else %}{{ beginn_offen | replace: "; ", "<br>" }}{% endif %}</span></div></td></tr>
<tr><td>Umfang</td><td><div class="paare"><span class="f">ZS:</span><span>35.000–50.000 Zeichen, etwa 10–15 Seiten</span><span class="f">PS:</span><span>45.000–65.000 Zeichen, etwa 14–20 Seiten</span></div></td></tr>
<tr><td>Abgabe</td><td><div class="paare breit">{% if abg_z != "" or abg_p != "" %}<span class="f">ZS:</span><span>{% if abg_z != "" %}{{ abg_z }}{% else %}{{ abgabe_offen }}{% endif %}</span><span class="f">PS:</span><span>{% if abg_p != "" %}{{ abg_p }}{% else %}{{ abgabe_offen }}{% endif %}</span>{% else %}<span class="f">Abgabetermin:</span><span>{{ abgabe_offen }}</span>{% endif %}<span class="f">digital:</span><span><span class="zeile">als PDF und docx-Datei</span><span class="zeile"><span class="fi">an:</span><a href="mailto:sekretariat.europarecht@uni-leipzig.de">sekretariat.europarecht@uni-leipzig.de</a></span><span class="zeile"><span class="fi">cc:</span>{% include email.html nur="haupt" %}</span></span><span class="f">gedruckt:</span><span>im Sekretariat der Professur<br>(Burgstraße 21, Raum 1.26)</span></div></td></tr>
{%- assign mo = site.seminar.moodle | strip -%}
<tr><td>Moodle-Kurs</td><td>{% if mo != "" %}<a href="{{ mo }}">{{ mo | remove: "https://" }}</a>{% else %}Der Link wird hier ergänzt{% endif %}</td></tr>
</table>

## Anmeldung und Themenvergabe <a href="#seitenanfang" class="hoch" aria-label="Zum Seitenanfang">↑</a> {#anmeldung}

Das Seminar steht Studierenden aller Schwerpunktbereiche als Zulassungsseminar (ZS) offen. Als Prüfungsseminar (PS) ist es dem Schwerpunktbereich 4 zugeordnet; eine Zuordnung zu anderen Schwerpunktbereichen ist nach Absprache möglich. Für das Zulassungsseminar ist die Teilnahme ab dem 5. Fachsemester empfohlen, für das Prüfungsseminar ab dem 6.

Die Anmeldung ist ab sofort bis **{{ site.termine.anmeldeschluss }}** möglich, per E-Mail an mich ({% include email.html nur="haupt" %}), in Kopie an <a href="mailto:sekretariat.europarecht@uni-leipzig.de">sekretariat.europarecht@uni-leipzig.de</a>.

Bitte geben Sie dabei Folgendes an:

- Name, Matrikelnummer, Fachsemester und E-Mail-Adresse
- Schwerpunktbereich, gegebenenfalls den voraussichtlichen
- ob Sie ein Zulassungs- oder ein Prüfungsseminar schreiben
- bis zu drei Themenwünsche mit Nummer und Titel, in der Reihenfolge Ihrer Präferenz
- ob Sie zugleich einen Schlüsselqualifikationsnachweis erwerben möchten

Für das Prüfungsseminar brauchen Sie die Zulassung zur Schwerpunktbereichsprüfung; diese erteilt das Studienbüro. Das Formular zur Anmeldung des Prüfungsseminars können Sie nachreichen.

Melden sich mehr Interessierte, als Themen zur Verfügung stehen, gilt folgende Reihenfolge: Teilnahme am Prüfungsseminar, Zugehörigkeit zum Schwerpunktbereich, Zeitpunkt der Anmeldung.

Über die Themenvergabe verständigen wir uns in der Vorbesprechung. Manche Themen lassen mehr als eine Bearbeitung zu; in diesen Fällen wird der Zuschnitt bei der Vergabe festgelegt.

Wenn Sie sich für ein Thema interessieren oder Fragen zur Themenwahl haben, schreiben Sie mir gerne schon vorher unter {% include email.html nur="haupt" %}.

## Vorbesprechung <a href="#seitenanfang" class="hoch" aria-label="Zum Seitenanfang">↑</a> {#vorbesprechung}

Die Vorbesprechung findet in der Woche vom **{{ site.termine.vorbesprechung }}** online statt. Der genaue Termin wird hier bekanntgegeben; die Zugangsdaten erhalten Sie nach Ablauf der Anmeldefrist per E-Mail.

Die Anwesenheit in der Vorbesprechung ist Voraussetzung für die Teilnahme am Seminar. Wenn Sie verhindert sind, melden Sie sich bitte vorab bei mir.

## Seminararbeit <a href="#seitenanfang" class="hoch" aria-label="Zum Seitenanfang">↑</a> {#arbeit}

### Formalia: Umfang, Fristen und Abgabe

| | Zulassungsseminar | Prüfungsseminar |
|---|---|---|
| Bearbeitungszeit | 9 Wochen | 8 Wochen |
| Umfang | 35.000 bis 50.000 Zeichen<br>(etwa 10 bis 15 Seiten) | 45.000 bis 65.000 Zeichen<br>(etwa 14 bis 20 Seiten) |

Der Umfang versteht sich einschließlich Fußnoten und Leerzeichen. Titelseite, Gliederung und Verzeichnisse zählen nicht mit. Maßgeblich ist die Zeichenzahl; die Seitenangaben sind nur Anhaltspunkte und gehen von 12 Punkt bei 1,5-zeiligem Abstand aus. Die Bearbeitungszeit beginnt mit der endgültigen Themenzuteilung.

Eine Verlängerung der Bearbeitungszeit für die Prüfungsseminararbeit kann unter Nennung besonderer Gründe auf Antrag gewährt werden. Richten Sie solche Anträge bitte per E-Mail an mich ({% include email.html nur="haupt" %}).

Die Arbeit reichen Sie **als PDF und als docx-Datei** per E-Mail ein, an <a href="mailto:sekretariat.europarecht@uni-leipzig.de">sekretariat.europarecht@uni-leipzig.de</a> und in Kopie an mich ({% include email.html nur="haupt" %}). Die gedruckte Ausfertigung geben Sie bitte im Sekretariat der Professur ab (Burgstraße 21, Raum 1.26).

Wird die Arbeit als Prüfungsleistung erbracht, ist dies bei der Themenvergabe anzuzeigen und auf dem Deckblatt der Arbeit anzugeben. Hierzu muss die Zulassung zur Schwerpunktbereichsprüfung vorliegen; das für die Anmeldung zum Prüfungsseminar erforderliche Formular ist nachzureichen.

### Was inhaltlich erwartet wird

Die Themen sind bewusst weit gefasst. Sie erfordern eine Eingrenzung, und welchen Ausschnitt Sie wählen, ist bereits Teil der wissenschaftlichen Leistung. Die auf den Themenseiten verlinkten Kurzbeiträge sind als Einstieg gedacht: Sie verschaffen einen Überblick über die Fragen und Streitpunkte und verweisen häufig auf die einschlägige Literatur und die Grundsatzentscheidungen. Von dort aus setzen Sie eigene Schwerpunkte und ziehen weitere Literatur heran.

Die Arbeit ist selbstständig zu erstellen. Erwartet wird keine erschöpfende Darstellung, sondern eine eigene Fragestellung und eine durchgeführte Argumentation. Arbeiten Sie dafür mit den Primärquellen und mit der Sekundärliteratur und setzen Sie sich mit den Gegenpositionen auseinander. Eine eigene Position ist ausdrücklich willkommen; sie muss nichts Neues erfinden, sondern nachvollziehbar begründet sein. Die Zitierweise ist frei, sollte aber einheitlich sein. Wichtiger als das System ist, dass man Ihren Nachweisen folgen kann.

Einige der verlinkten Kurzbeiträge liegen hinter einer Bezahlschranke. Wenn Sie Zugang benötigen und ihn über die Universität Leipzig nicht bekommen, melden Sie sich gerne bei mir. Das gilt nicht nur für die verlinkten Beiträge, sondern für Literatur allgemein: Wenn Sie an etwas nicht herankommen, schreiben Sie mir, wir finden meist eine Lösung.

## Seminarablauf und Vortrag <a href="#seitenanfang" class="hoch" aria-label="Zum Seitenanfang">↑</a> {#vortrag}

Das Seminar findet als Blockveranstaltung statt, voraussichtlich **{{ site.termine.block }}**. Die genauen Termine und der Raum werden hier bekanntgegeben.

Im Seminar stellen Sie den Inhalt Ihrer Arbeit in einem mündlichen Vortrag vor und verteidigen ihn in der anschließenden Diskussion. Der Vortrag dauert **20 bis 25 Minuten**.

Für das Blockseminar besteht grundsätzlich **Anwesenheitspflicht**; wenn Sie verhindert sind, melden Sie sich bitte vorab bei mir. Auch die Teilnahme an den Diskussionen der anderen Vorträge gehört zur Seminarleistung.

## Betreuung <a href="#seitenanfang" class="hoch" aria-label="Zum Seitenanfang">↑</a> {#betreuung}

Für Rücksprachen stehe ich Ihnen nach Terminvereinbarung per E-Mail zur Verfügung ({% include email.html nur="haupt" %}). Eine erste Rücksprache ist sinnvoll, wenn Sie sich einen Überblick verschafft und eine erste Eingrenzung vorgenommen haben.

Wenn Sie eine Rückmeldung zu Ihrer Gliederung möchten, schicken Sie sie mir gerne. Am sinnvollsten ist das, solange Sie noch nicht schreiben, denn an der Gliederung zeigt sich früh, ob der Zuschnitt trägt.
