#Intro

Null ein ursprünglich von Modder erstelltes Zwietrachtthema . Die verwendete Originalversion calcund CSS-Variablen basieren auf HSL. Farbton basierend auf einem Farbkreis, Sättigung für einen Grauton (0%) bis zur Vollfarbe (100%) vom Farbton und Helligkeit ist die Lichtmenge, die die Farbe für Schwarz 0%, für Weiß 100% hat. Dieses Thema ist eine Neufassung des Originals, um dem Benutzer viel mehr Variablen zur Verfügung zu stellen, mit denen er den Farbunterschied ändern oder eine bestimmte Farbe monoton halten kann. Eine Anleitung zum Bearbeiten der Variablen von null.

#Versionen

Derzeit werden 2 Hauptversionen unterstützt:

NullDies kann dazu führen, dass Benutzer die Addon-Importe entfernen, wenn dies gewünscht wird. Dies wird höchstwahrscheinlich weitere Aktualisierungen und Änderungen in der Zukunft erhalten. Diese Version wird als Dunkelgrau und Akzentfarben voreingestellt. null herunterladen
Null ClearEine transparente Voreinstellungsversion der Nulldatei enthält keine Addon-Importe. Allerdings wird das Thema vorgegeben wie Nullmit farbigen Kanälen, Tooltips usw. null klar herunterladen

Dark Nullwird das Setup zu imitieren das Original Discord Gefühl sein , so dass keine Akzentfarben auf Tooltips, Kanäle, Blurple Elemente erwähnt / Kanäle usw. dunkel null herunterladen

Die dritte Version ist zu Fehlen eines „sonst nur eine dunklere Version von Discord nichts“ ansprechen . Diese Version könnte offensichtlich leicht daraus gemacht werden, Dinge aus der ersten Datei zu ändern; Es ist jedoch ideal, die Forderung nach nur einer dunklen Zwietracht auch mit einer detaillierten Readme-Datei zu beseitigen.
Hinweis: Ich bin mir der Idee von Themen und der Idee bewusst, Importe zu verwenden, Variablen zu ändern und sie als "Themen" zu bezeichnen. Null ist ein Thema, bei dem bereits verschiedene Versionen voreingestellt sind, um zu vermeiden, dass Tausende einfacher Fragen gestellt werden.



#Hauptvariablen

Hauptvariablen - Variablen in der Themendatei

  - Farbton : 217 ;
  - Sättigung : 0 % ;
  - Helligkeit : 15 % ;
  - Alpha : 1 ;
--hueist der Farbton, --saturationist die Sättigung (%), --lightnessist die Lichtmenge (%) Die Farbtonwerte basieren auf einem Grad des Farbrads, sodass 0 rot, 120 grün und 240 blau ist (Hinweis: RGB und Hex können konvertiert werden) in to hsl) Sättigung ist der Grauton, also 0% ist grau, während 100% die volle Farbe ist. Helligkeit ist das Licht der Farbe. 0% ist schwarz, während 100% weiß ist

Die Sättigung sollte unter einem Wert von 40% bleiben, um visuelle Probleme zu vermeiden, insbesondere die Helligkeit unter 20%. --alphaist das Alpha / die Deckkraft der Farbe. Ändern Sie den Wert nur als Dezimalzahl (z. B. 0,25), wenn Sie eine Änderung der Transparenz wünschen

Wenn Sie bei Verwendung von Transparenz eine hellere Farbe und / oder ein helleres Bild wünschen, kopieren Sie alle .theme-darkund alle Variablen (AUSSER --text-normalund --text-muted) und fügen Sie sie am Ende der Datei ein und benennen Sie sie .theme-darkin um .theme-light. Wenn Sie diesen Teil nicht verstehen, sind Sie mit einem anderen Thema besser dran

#Additionsvariablen
Diese Variablen sind die Addition / Multiplikation, um den Stil der Farbpalette des ursprünglichen dunklen Themas der Zwietracht nachzuahmen. Wenn Sie --hue-additionanfänglich 0diesen Wert ändern, --saturation-additionändert sich der Farbton / die Farbe bestimmter Elemente, die Sättigung --lightness-addition bestimmter Elemente und die Helligkeit bestimmter Elemente. Diese Option wird nur verwendet, um die --alpha-additionDeckkraft bestimmter Elemente zu erhöhen, wenn für ein transparentes Thema Null geändert wird. --multiplierist in bestimmten Bereichen auch an diese Variablen gebunden, wenn Sie den Multiplikator entfernen und dann seinen Wert auf setzen möchten1

Additionsvariablen können auch negative Interger (ex --saturation-addition: -6%;) sein, um einen dunkleren Kontrast zu erzielen .

#Akzente
Akzente, Tooltips, Erwähnungen usw. --accentsind die Akzentfarben, die für viele Regionen gelten, z. B. Pings, Benachrichtigungspunkte und unscharfe Elemente (Zwietrachtblau). Benutzer können die Änderungen zurücksetzen, da in der Datei Standardeinstellungen angegeben sind, um alle Variablen zurückzusetzen. Es kann jedoch besser sein, Dark Null zu ändern, wenn Sie die geringsten Änderungen der Akzente wünschen.

--tooltip-background, --blurple, --is-mention, --is-mention-bg, --unread, Und --guild-selectedalle verwenden die Variable--accent

- Kanal ausgewählt : linearer Gradient ( 6 Grad ,  var (- Kanal-Gradient-prim ) ,   var (- Kanal-Gradient-Sek ) ,   var (- Kanal-Gradient-Tri ));
wurde als Hintergrundbild-Farbverlauf eingerichtet. Der Benutzer kann den gesamten Farbverlauf löschen und ersetzen, wenn er zum normalen Kanalmodifikator zurückkehren möchte. Beispiel:

--channel-selected : var ( --background-modifier-selected );
#Addons
gibt nur vor Null; Importe können jedoch zu allen Themen hinzugefügt werden, nicht nur zu Nullversionen. (Wichtiger Hinweis: Das Hinzufügen dieser Importe zu anderen Themen funktioniert möglicherweise nicht ordnungsgemäß.) Hinweis: Importe werden über allen anderen CSS-Dateien in einer Datei platziert

Importe sind Thesen:

@import  url ( 'https://asteria5675.github.io/addons/Bigger_Chat_Avatars.css' );
Dieses Add - on macht Avatare im Chat größer --avatar-sizeund auch können sie Platz machen --avatar-roundness: 0;und

@import  url ( 'https://asteria5675.github.io/addons/null_addons.css' );
Dieses Addon ändert ein Popout- und Kontextmenü in ein Blockdesign, nichts Dramatisches. Erwarten Sie, dass dieses Import-Addon hinzugefügt wird.

Falls gewünscht, können beide Addon-Importe von null gelöscht werden. Hinweis: Wenn Sie diese Importe verwenden, überprüfen Sie das CSS, um die Variablen zu verstehen, wenn Sie bestimmte CSS anpassen möchten.

Vollständiger Import von Popout-Benutzern

 @import  url ( 'https://asteria5675.github.io/addons/full_popout_avatars.css' );

#Schlussbemerkungen
Bitte lesen Sie diese Readme-Datei, um die unzähligen Möglichkeiten zur Änderung dieses Themas vollständig zu verstehen.

Der Grund, warum ich null wiederbelebt und neu geschrieben habe, war, dass es eines der wenigen wirklich frühen grundlegenden Dark-Mode-Themen war, das das Zwietrachtgefühl kaum verändert hat. Das Original war jedoch schnell veraltet und stand nie im Rampenlicht für das einzigartige Konzept des Themas.

Support Server hier. Hinweis: Ich mache diese Themen in meiner Freizeit. Verlange KEINE einfachen Änderungen, die für dich vorgenommen wurden. Verwenden Sie diese Readme-Datei und lesen Sie sie auch, um sie zu verstehen.

Apropos diese Themen kostenlos zu machen, wenn Sie wirklich für mich spenden wollten, damit ich von ein oder zwei weiteren Energy Drinks leben kann, dann fordern Sie den Spendenlink genug auf meinem Server an und ich könnte einen machen, der es weiß. Ich ziehe es jedoch vor, solche nicht zu bewerben :)

Liesmich
wieder einmal heißt es readmeaus einem Grund. Beginnen Sie hier, um zu verstehen, wie Sie dieses Thema in die gewünschte Hintergrundfarbe / das gewünschte Bild ändern können. Diese Readme-Datei wurde für alle möglichen Fragen erstellt. Lesen Sie sie oder die Themendatei mit Beispielen / Erklärungen. Wenn Sie von hier aus nichts verstehen können, sind Sie mit einem anderen Thema besser dran.
text by https://github.com/Asteria5675/ ich habe nur ihr theme verändet und will es ihr nicht steheln usw
