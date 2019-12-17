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

  <b>1. Kommentare</b>
<p>Kommentare sollen den Code für Andere leichter verständlich machen. Dabei sollten man sie in einer angemessenen Menge einsetzen, weil ein Überschuss an Kommentaren wiederrum zu Unübersichtlichkeit führt. Die Formulierung der Kommentaren selbst sollte für Menschen verständlich sein</p>

```c#
// Calling function 
        Message(msg); 
```

  <b>2. Zu lange Methoden</b>
<p>Eine Methode (Funktion, Prozedur) ist zu lang.</p>

```c#
  void Start()
    {
        varA = 5;
        varB = 4;
        AddNumbers(varA, varB);
        AddNumbers(4, 7);
        Debug.Log("in Start: " + AddNumbers(varA, varB));
        Debug.Log("in Start: " + AddNumbers(4, 7));
        Debug.Log(10 - AddNumbers(varA, varB));
        Debug.Log(100 - AddNumbers(4, 7));
        
    }
```



<b>3. Zu komplexe/verwirrende Namensgebung</b>
<p>Um Zeit und Verwirrung zu sparen sollten die vergebenen Namen immer Sinn ergeben und nach einem einheitlichen System ausgewählt sein.</p>

```c#
 public void _RstTheRslt1(){}
public void retTheresult(){}
```


<b>4. Zu lange Namensgebung</b>
<p>Um Zeit und Verwirrung zu sparen sollten die vergebenen Namen immer relativ kurz und aussagekräftig sein</p>

```c#
public string = thisVariableIsAStringAndIsItsNameIsMaybeABitTooLong;
```

<b>5. Zu kurze Namensgebung</b>
<p>Auch zu kurze Namen können zu Unklarheit führen und sollten vermieden werden.</p>

```c#
public GameObject = gO;
```


  
<b>6. Doppelter Code</b>
<p>Manche Schritte können einfach zusammengefasst werden, wodurch man an Zeit sparen kann und einen übersichtlicheren Code verfasst.</p>

```c#
protected void SetBlueBoxVisibility(bool blueBoxVisibility)
    {
        Project project = LoadProject();
        project.ShowBlueBox = blueBoxVisibility
        ReDrawSomeThings();
        ShowBlueBoxPanel(blueBoxVisibility);
        RaiseStatusUpdated();
    }

    protected void SetRedBoxVisibility(bool redBoxVisibility)
    {
        Project project = LoadProject();
        project.ShowRedBox = redBoxVisibility
        ReDrawSomeThings();
        ShowRedBoxPanel(redBoxVisibility);
        RaiseStatusUpdated();
    }
```


<b>7. Unbenutzte NameSpaces</b>
<p>Unnötige NameSpaces sollten möglichst gelöscht werden, um Verwirrung und Probleme zu vermeiden.</p>

```c#
using UnityEngine;
using UnityEngine.UI;
using System;
using System.Collections;
``

<b>8. Unerreichbarer Code</b>
<p>Unbenutzer Code verschwendet Rechenzeit und Speicher.</p>


```c#
public int Add(int x, int y)
{
    return x + y;
    return 2 + 2;
}
```

<b>9. Unbenutzte Parameter</b>
<p>Wenn Parameter in der Methode angegeben werden, müssen sie darin auch Verwendung finden.</p>

```c#
public int Add(int x, int y, int z)
{
    return x + y;
}
```

<b>10. Tiefe Verschachtelungen</b>
<p>Zu tiefe Verschachtelungen führen zu Verwirrung und Unverständlichkeit. </p>

```c#
do 
{   
    statement(s);
    do 
    {  
        statement(s);
        do
	{
	    statement(s)
	}
	while(condition);
    }
    while(condition);
}
while(condition);
```
<p></p>

Copyright by Kathrin König & Leo Martinusic
