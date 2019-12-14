# home-codeingStandardsRefactoring-lmartinusic
 <h1>
 Ausarbeitung Refactoring:
  </h1>
  <p></p>
 <h2>
  <li>Was ist Refactoring Definition in eigenen Worten?</li>
   </h2>
<p></p>
<p>Der Vorgang, ein Softwaresystem so zu ändern, dass es das äußere Verhalten des Codes nicht verändert und dennoch seine interne Struktur verbessert. Es ist ein disziplinierter Weg, um Code zu bereinigen, der das Risiko von Fehlern minimiert.</p>
 <h2>
<li>Welche Vorteile/Nachteile birgt Refactoring?</li>
    </h2>
<p></p>
<p>-Lesbarkeit, so dass möglichst viele Programmierer verstehen, was der Code tatsächlich macht</p>
<p>-Modularität und Redundanz, so dass konkrete Problemlösungen von anderer Stelle genutzt werden können und nicht mehrfach implementiert sind</p>
<p>-Kopplung und Kohäsion, damit zukünftige Änderungen nur lokale Auswirkungen haben</p>
<p>-Testbarkeit , so dass es möglich wird, die korrekte Arbeitsweise des Codes für die Zukunft durch Regressionstests abzusichern</p> 
<p></p>
 <h2>
<li>Was sind die Refactoring-Schritte?</li>
    </h2>
<p></p>
1)Testfall definieren (optimal automatisiert) 
<p></p>
2) Stellen Sie sicher, dass das Programm funktioniert? Commiten
<p></p>
3) Nehmen Sie eine einzelne Änderung vor, um einen Code-Smell zu beheben
<p></p>
4) Überprüfen Sie, ob das Programm noch funktioniert
<p></p>
5) Commiten
<p></p>
 <h2>
<li>Prinzipien von gutem Code?</li>
    </h2>
<p></p>
<p>-Lesbarkeit</p>
<p>-Verständlichkeit</p>
<p>-Testbarkeit</p>
<p>-Wartbarkeit</p>
<p>-Erweiterbarkeit</p>
<p></p>
   <h2>
<li>Was versteht man unter Code Smell?</li>
    </h2>
<p></p>
<p>Funktionierender, aber schlecht strukturierter Quellcode.</p>
<p></p>
     <h2>
<li>Recherche von 10 Code Smells die Eure Projekt betreffen können, inkl. Beschreibung und Beispiel.</li>
    </h2>
<p></p>

  <b>Code-Duplizierung</b>
<p>Der gleiche Code kommt an verschiedenen Stellen vor.</p>

  <b>Lange Methode</b>
<p>Eine Methode (Funktion, Prozedur) ist zu lang.</p>

<b>Große Klasse</b>
<p>Eine Klasse ist zu umfangreich, umfasst zu viele Instanzvariablen und duplizierten Code. Siehe auch Gottobjekt.</p>

<b>Lange Parameterliste</b>
<p>Anstatt ein Objekt an eine Methode zu übergeben, werden Objekt-Attribute extrahiert und der Methode als lange Parameterliste übergeben.</p>

<b>Divergierende Änderungen</b>
<p>Für eine Änderung muss eine Klasse an mehreren Stellen angepasst werden.</p>
  
<b>Datenklumpen</b>
<p>Eine Gruppe von Objekten kommt häufig zusammen vor: als Felder in einigen Klassen und als Parameter vieler Methoden.</p>

<b>Parallele Vererbungshierarchien</b>
<p>Zu jeder Unterklasse in der einen Hierarchie gibt es immer auch eine Unterklasse in einer anderen Hierarchie.</p>

<b>Faule Klasse</b>
<p>Eine Klasse leistet zu wenig, um ihre Existenz zu rechtfertigen.</p>

<b>Spekulative Allgemeinheit</b>
<p>Es wurden alle möglichen Spezialfälle vorgesehen, die gar nicht benötigt werden; solch allgemeiner Code braucht Aufwand in der Pflege, ohne dass er etwas nützt.</p>

<b>Temporäre Felder</b>
<p>Ein Objekt verwendet eine Variable nur unter bestimmten Umständen – der Code ist schwer zu verstehen und zu debuggen, weil das Feld scheinbar nicht verwendet wird. </p>
