<div align="center">

<img src="assets/rashnova-banner.png" alt="Rashnova, die Blackbox für Ihren Laptop, von Alcyone Secure" width="100%">

# Rashnova

### Ein manipulationserkennender Aktivitätsrekorder für Windows

**Geben Sie Ihren PC ab. Bekommen Sie ihn mit einem versiegelten Protokoll dessen zurück, was damit gemacht wurde.**

[![Latest release](https://img.shields.io/github/v/release/sathvik-zoldyck/rashnova?style=flat-square&label=release&labelColor=111111&color=F25C05)](https://github.com/sathvik-zoldyck/rashnova/releases/latest)
[![Downloads](https://img.shields.io/github/downloads/sathvik-zoldyck/rashnova/total?style=flat-square&labelColor=111111&color=F25C05)](https://github.com/sathvik-zoldyck/rashnova/releases)
[![Platform](https://img.shields.io/badge/Windows-10%20%7C%2011%20%28x64%29-F25C05?style=flat-square&labelColor=111111)](#requirements)
[![Price](https://img.shields.io/badge/price-free-F25C05?style=flat-square&labelColor=111111)](#download)
[![Licence](https://img.shields.io/badge/licence-proprietary-555555?style=flat-square&labelColor=111111)](LICENSE)

[**Download**](https://github.com/sathvik-zoldyck/rashnova/releases/latest) ·
[**Website**](https://www.alcyonesecure.com) ·
[**Bekannte Grenzen**](KNOWN_LIMITS.md) ·
[**Datenschutz**](#privacy) ·
[**Sicherheit**](SECURITY.md)

</div>

> **Sprachen** &nbsp;·&nbsp; [English](README.md) · [हिन्दी](README.hi.md) · [ಕನ್ನಡ](README.kn.md) · [മലയാളം](README.ml.md) · [Español](README.es.md) · [Français](README.fr.md) · **Deutsch** · [Português](README.pt.md) · [日本語](README.ja.md) · [Bahasa Indonesia](README.id.md) · [עברית](README.he.md)

---
> [!NOTE]
> Diese Seite ist aus dem Englischen übersetzt. Die Rashnova-App selbst ist auf Englisch, daher stehen Namen von
> Schaltflächen und Fenstern hier auf Englisch. Weichen diese Seite und die [englische Fassung](README.md) voneinander ab, gilt die englische Fassung.


Rashnova zeichnet auf, was auf einem Windows-PC passiert, während jemand anderes ihn hat: in der Werkstatt, in der
IT-Abteilung oder bei jedem, dem Sie ihn überlassen. Starten Sie vor der Übergabe eine **Repair session**. Wenn der PC
zurückkommt, beenden Sie sie, und Rashnova gibt Ihnen ein Urteil und einen Bericht darüber, was geöffnet, kopiert,
umbenannt und gelöscht wurde, welche Programme liefen und welche USB-Laufwerke angeschlossen wurden.

Jeder Eintrag wird mit dem vorherigen versiegelt. So zeigt das Protokoll, ob etwas darin verändert oder entfernt
wurde, und es zeigt jede Zeitspanne, in der nichts aufgezeichnet werden konnte. Alles bleibt auf Ihrem Computer. Kein
Konto, keine Cloud, keine Telemetrie.


> [!NOTE]
> In diesem Repository wird Rashnova **veröffentlicht**: Installer, Versionshinweise, bekannte Grenzen und
> Sicherheitsrichtlinie. Rashnova ist proprietäre Software von [Alcyone Secure](https://www.alcyonesecure.com); der
> Quellcode wird hier nicht veröffentlicht.


## Inhalt

- [Warum es Rashnova gibt](#why)
- [Was es tut](#what-it-does)
- [Was es nie aufzeichnet](#never)
- [So funktioniert es](#how)
- [Download und Installation](#download)
- [Systemvoraussetzungen](#requirements)
- [Datenschutz](#privacy)
- [Bekannte Grenzen](#limits)
- [Updates](#updates)
- [Hilfe und Sicherheit](#support)
- [Lizenz](#licence)

<a name="why"></a>
## Warum es Rashnova gibt

Flugzeuge, Züge und Schiffe haben eine Blackbox. Ein Computer, der Ihre Hände verlässt, hat nichts, und wer ihn in
der Hand hat, kommt an alles darauf heran.

Und dieser Zugriff wird genutzt. In einer [Studie von Forschenden der University of Guelph aus dem Jahr 2022](https://arxiv.org/abs/2211.05824)
(veröffentlicht beim IEEE Symposium on Security and Privacy 2023) wurden Laptops mit eingeschalteter Protokollierung über
Nacht in 12 Werkstätten gelassen. Techniker in sechs davon griffen auf die persönlichen Daten darauf zu, und zwei
kopierten Daten vom Laptop. Virenschutz und Endpoint-Werkzeuge wurden nie dafür gebaut, das zu bemerken: Dieser Person
wurden die Schlüssel übergeben.

Rashnova ist keine Prävention. Es ist ein Beweis, damit sich prüfen lässt, was passiert ist, statt darüber zu
streiten.

> *Vertrauen ist gut. Beweise sind besser.*

<a name="what-it-does"></a>
## Was es tut

<table>
<tr>
<td width="50%" valign="top">

**Repair Mode (Reparaturmodus).** Eine überwachte Sitzung, die Sie vor der Übergabe mit Ihrer PIN starten und nach
der Rückgabe mit Ihrer PIN beenden. Sie zeichnet geöffnete, erstellte, umbenannte, kopierte und gelöschte Dateien auf,
gestartete Programme, ausgeführte PowerShell-Befehle, Anmeldungen und angeschlossene USB-Speicher, einschließlich jeder
darauf geschriebenen Datei. Ein Neustart, ein Herunterfahren oder der Energiesparmodus beenden die Sitzung nie: Der
Bericht zeigt jede Unterbrechung und wie lange sie dauerte.

</td>
<td width="50%" valign="top">

<img src="assets/screenshots/session-summary.png" alt="Sitzungszusammenfassung: ein Urteil, die wichtigsten Ereignisse und die Kettenprüfung">

</td>
</tr>
<tr>
<td width="50%" valign="top">

<img src="assets/screenshots/session-explorer.png" alt="Sitzungs-Explorer: jedes Ereignis im Zeitverlauf, nach Programm und nach Ordner">

</td>
<td width="50%" valign="top">

**Ein Protokoll, das Sie prüfen können.** Jede Sitzung endet mit einem Urteil und einem Bericht, den Sie als PDF,
Webseite oder Tabelle speichern können. Der Sitzungs-Explorer zeigt jedes Ereignis im Zeitverlauf, nach Programm und nach
Ordner, und die Kettenprüfung sagt Ihnen, ob das Protokoll unversehrt ist. Was Sie speichern, ist eine Kopie; das
Original bleibt, wo Rashnova es aufbewahrt.

</td>
</tr>
<tr>
<td width="50%" valign="top">

**Das wöchentliche Readout.** Ihre Woche in einem Urteil, mit höchstens ein paar Dingen, die einen Blick wert
sind. Markieren Sie jedes mit "that was me" (das war ich) oder "that wasn't me" (das war ich nicht). Es sagt auch in
einfachen Worten, was Rashnova sehen kann und was nicht.

</td>
<td width="50%" valign="top">

<img src="assets/screenshots/weekly-readout.png" alt="Das wöchentliche Readout: ein Urteil für die Woche, Dinge, die einen Blick wert sind, Aktivität pro Tag">

</td>
</tr>
<tr>
<td width="50%" valign="top">

<img src="assets/screenshots/always-on-choice.png" alt="Die Wahl zwischen Aufzeichnung nur in Sitzungen und dauerhafter Aufzeichnung">

</td>
<td width="50%" valign="top">

**Dauerhafte Aufzeichnung (always-on), nur wenn Sie es wählen.** Aus, bis Sie sie einschalten. Sie behält das
Unumkehrbare und das Alarmierende (endgültige Löschungen, sensibel wirkende Dateien, alles, was auf ein Wechsellaufwerk
gelangt oder es verlässt), nicht Ihre alltägliche Nutzung Ihrer eigenen Dateien. Ausschalten ist ein Klick im
Infobereich oder in Settings und braucht nie Ihre PIN.

</td>
</tr>
<tr>
<td width="50%" valign="top">

**Aus dem Infobereich.** Sehen Sie, dass eine Sitzung aufzeichnet, beenden Sie sie, starten Sie eine 30-Sekunden-
Stichprobe der aktuellen Dateiaktivität (Monitor Now) oder öffnen Sie den letzten Bericht.

</td>
<td width="50%" valign="top" align="center">

<img src="assets/screenshots/quick-panel.png" alt="Das Schnellfenster im Windows-Infobereich" width="70%">

</td>
</tr>
</table>

<sub>Die Screenshots zeigen Rashnova mit einer Beispielsitzung (eine fiktive Nutzerin, "Riya").</sub>

**Neu in 1.2.0:** Handover Mode, wenn Sie Ihren PC der Familie, einem Freund oder einem Kollegen überlassen, mit
demselben versiegelten Bericht; das Blockieren von USB-Speichern; und Start with Windows. Siehe das [Änderungsprotokoll](CHANGELOG.md).

<a name="never"></a>
## Was es nie aufzeichnet

Rashnova zeichnet auf, **dass** etwas passiert ist, nicht, was auf dem Bildschirm war. Es zeichnet nicht auf:

- Tastenanschläge
- Inhalte der Zwischenablage
- Ihren Bildschirm, weder als Bild noch als Video
- Ihre Kamera oder Ihr Mikrofon
- den Inhalt Ihrer Dokumente, Fotos, E-Mails oder Nachrichten
- die Webseiten, die Sie besuchen, oder was darauf steht

Zwei Dinge, die es aufzeichnet, sollten Sie kennen. Während einer Repair session werden PowerShell-Befehle bei der
Ausführung aufgezeichnet, ebenso die vollständige Startzeile jedes Programms, das eine Person startet; ein Browser, der
über einen Link geöffnet wurde, zeigt also diesen Link.

Ein Bericht sagt zum Beispiel, dass `Bank_Statement_Aug2026.pdf` um 15:01:16 aus `Documents\Finance` mit
Microsoft Edge geöffnet wurde. Er sagt nicht, was im Kontoauszug stand.

<a name="how"></a>
## So funktioniert es

1. **Installieren.** Der Installer installiert Rashnova und seinen Hintergrundrekorder.
2. **PIN festlegen.** Die PIN prüft der Rekorder, nicht das App-Fenster.
3. **Vor der Übergabe:** **Repair Mode > Activate**, dann Ihre PIN.
4. **Übergeben.** Alles unter "Was es tut" wird in ein versiegeltes Protokoll geschrieben.
5. **Bei der Rückgabe:** **Deactivate**, dann Ihre PIN. Sie erhalten ein Urteil, einen Bericht und die Kettenprüfung.

Der Rekorder läuft als Windows-Dienst. Er zeichnet also weiter auf, ob jemand das Rashnova-Fenster öffnet oder
nicht, und startet nach einem Neustart von selbst wieder.

**Jede Sitzung endet mit einem von vier Urteilen:**

| Urteil | Bedeutung |
| --- | --- |
| **Quiet** | Das Protokoll ist geprüft und vollständig, und nichts von hoher Bedeutung ist passiert. |
| **Notable** | Mindestens ein hohes (high) oder kritisches (critical) Ereignis: lesenswert. |
| **Compromised** | Der Rekorder von Rashnova wurde angehalten, während Windows weiterlief, oder das Protokoll zeigt einen Eingriff, kann also nicht für die ganze Sitzung bürgen. Ein Neustart, ein Herunterfahren oder der Energiesparmodus wird mit seiner Dauer angezeigt und zählt nicht gegen die Sitzung. |
| **Chain broken** | Das Protokoll lässt sich nicht verifizieren. Alles wird trotzdem angezeigt, als ungeprüft markiert. |

<a name="download"></a>
## Download und Installation

| Datei | Wofür |
| --- | --- |
| **`Rashnova-1.2.1.msi`** | Für alle. Installiert Rashnova mit einer eigenen Kopie von .NET 10, sodass vorher nichts anderes installiert werden muss. |
| `SHA256SUMS.txt` | Der SHA-256 jeder Datei, um Ihren Download zu prüfen. |

1. Laden Sie `Rashnova-1.2.1.msi` aus der [neuesten Version](https://github.com/sathvik-zoldyck/rashnova/releases/latest) herunter. Meldet Ihr Browser, dass die Datei nicht häufig heruntergeladen wird, wählen Sie **Keep** (die Schritte für jeden Browser stehen in den [bekannten Grenzen](KNOWN_LIMITS.md)).
2. **Prüfen Sie die Datei** (empfohlen). In PowerShell:
   ```powershell
   Get-FileHash "$env:USERPROFILE\Downloads\Rashnova-1.2.1.msi"
   ```
   Der Hash muss exakt mit dem in `SHA256SUMS.txt` und in den Versionshinweisen übereinstimmen.
3. Starten Sie sie. Windows SmartScreen zeigt **"Windows protected your PC"** mit unbekanntem Herausgeber an, weil
   der Installer noch nicht digital signiert ist (siehe [bekannte Grenzen](KNOWN_LIMITS.md)). Wählen Sie
   **More info**, dann **Run anyway**.
4. Akzeptieren Sie die [Lizenzbedingungen](https://www.alcyonesecure.com/terms), installieren Sie und öffnen Sie Rashnova.
5. Legen Sie eine PIN fest und wählen Sie, ob Sie bei der Aufzeichnung nur in Sitzungen bleiben (Standard) oder die
   dauerhafte Aufzeichnung einschalten.


> [!IMPORTANT]
> Eine vergessene PIN lässt sich nicht wiederherstellen, weder von uns noch von sonst jemandem. Notieren Sie sie an einem sicheren Ort.
> Das Ausschalten der dauerhaften Aufzeichnung braucht nie die PIN.


**Sie kommen von 1.1.0?** Installieren Sie 1.2.1 darüber; Ihr Protokoll, Ihre PIN und Ihre Einstellungen bleiben erhalten. **Sie kommen von BlackBox 1.0.1?** Rashnova ist der neue Name von BlackBox. Laden Sie 1.2.1 herunter und installieren Sie es.

<a name="requirements"></a>
## Systemvoraussetzungen

- Windows 10 oder Windows 11, 64 Bit (getestet unter Windows 10)
- Sonst nichts: Rashnova bringt eine eigene Kopie von Microsoft .NET 10 mit
- Administratorfreigabe zur Installation, weil der Rekorder als Windows-Dienst läuft

<a name="privacy"></a>
## Datenschutz

- **Nur lokal.** Das Protokoll wird auf Ihrem Computer geschrieben und aufbewahrt. In dieser Version gibt es kein Konto und
  keine Cloud, und Rashnova sendet keine Nutzungsdaten.
- **Zwei kleine Anfragen,** keine mit Inhalten aus Ihrem Protokoll: eine tägliche Prüfung auf alcyonesecure.com, ob es
  eine neue Version gibt, und während einer Repair session ein Zeitabgleich mit Microsofts Zeitserver.
- **Wer das Protokoll lesen kann.** Das Windows-Konto, das die PIN festgelegt hat, und die Administratoren des
  Computers. Die zweite Kopie ist verschlüsselt, und Rashnova öffnet sie erst, nachdem Ihre PIN geprüft wurde. Die
  Administratoren des Computers können sie trotzdem lesen.
- **Sagen Sie es den Menschen, die Ihren PC nutzen.** Die dauerhafte Aufzeichnung gilt für den ganzen Computer, auch
  für Menschen, die Rashnova nie öffnen.
- **Eine Windows-Einstellung, offen gesagt.** Während einer Repair- oder Handover-Sitzung schaltet Rashnova die
  PowerShell-Skriptprotokollierung von Windows ein und stellt sie am Ende der Sitzung wieder so her, wie sie war. Eine
  Einstellung, die jemand anderes eingeschaltet hat, schaltet es nie aus.

<a name="limits"></a>
## Bekannte Grenzen

Wir veröffentlichen, was Rashnova nicht tut, damit Sie anhand der Fakten entscheiden können. Das Wichtigste:

- **Während der Computer aus ist, schläft oder neu startet, kann nichts aufgezeichnet werden.** Die Sitzung läuft
  weiter, und der Bericht zeigt jede Unterbrechung und ihre Dauer.
- **Administratoren können das Protokoll lesen.** Kein Programm kann seine Dateien vor einem Windows-Administrator verbergen.
- **Der Installer ist noch nicht digital signiert,** daher können Ihr Browser und Windows SmartScreen vor dem Start warnen.
- **Das Blockieren von USB-Speichern stoppt USB-Laufwerke, nicht jeden Weg, Dateien zu bewegen.** Telefone, im Computer
  eingebaute SD-Kartenleser und Netzlaufwerke werden nicht blockiert, und ein bereits eingestecktes Laufwerk funktioniert
  weiter, bis es abgezogen wird.

Die vollständige Liste, mit dem Grund für jede Grenze und dem Geplanten (auf Englisch): **[KNOWN_LIMITS.md](KNOWN_LIMITS.md)**.

<a name="updates"></a>
## Updates

Einmal am Tag prüft Rashnova auf alcyonesecure.com, ob es eine neue Version gibt, und sagt es Ihnen. Sie laden sie
selbst herunter und installieren sie; Ihr Protokoll, Ihre PIN und Ihre Einstellungen bleiben erhalten. Jede Version
wird hier mit Versionshinweisen und SHA-256 veröffentlicht. Siehe das [Änderungsprotokoll](CHANGELOG.md).

<a name="support"></a>
## Hilfe und Sicherheit

- **Hilfe:** siehe [SUPPORT.md](SUPPORT.md) oder schreiben Sie an **support@alcyonesecure.com**.
- **Fehler:** [Issue eröffnen](https://github.com/sathvik-zoldyck/rashnova/issues/new/choose). Veröffentlichen Sie in
  einem Issue nie Ihr Protokoll, Dateinamen oder etwas Persönliches.
- **Sicherheitslücken:** Eröffnen Sie kein öffentliches Issue. Folgen Sie [SECURITY.md](SECURITY.md).

<a name="licence"></a>
## Lizenz

Rashnova ist proprietäre Software, kostenlos auf Geräten, die Ihnen gehören oder die Sie überwachen dürfen. Siehe
[LICENSE](LICENSE) und die [Bedingungen](https://www.alcyonesecure.com/terms) (auf Englisch; diese sind maßgeblich). Die
Dokumente und Bilder in diesem Repository sind © Alcyone Secure.

---

<div align="center">

<img src="assets/rashnova-icon.png" alt="Rashnova" width="72">

**Alcyone Secure** · Entwickelt in Bengaluru, Indien · [alcyonesecure.com](https://www.alcyonesecure.com)

*Sicherheit ist nicht nur Prävention. Sicherheit ist Verantwortlichkeit.*

</div>
