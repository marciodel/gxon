
![GXON](images/gxon.png)

# GXON
Alternative XML Object Notation

The main objective of GXON is to provide an alternative syntaxe for editing XML files. Cleaner as JSON, AXON, YAML, but preserving some XML semantic (e.g. Namespaces).

There are two notation options (but they integrate perfectly).

The first notation is not intended to be used in general XML documents, as an example, it is not intended to be used to create HTML files. It is designed to provide a cleaner alternative to create Object Graphs.

FXML Document - XML Version:
```xml
<?xml version="1.0" encoding="UTF-8"?>
<?import java.lang.*?>
<?import javafx.scene.*?>
<?import javafx.scene.control.*?>
<?import javafx.scene.layout.*?>

<AnchorPane id="AnchorPane" prefHeight="200" prefWidth="320" xmlns:fx="http://javafx.com/fxml" 
            fx:controller="temp.Temp">
  <children>
    <Button fx:id="button" layoutX="126" layoutY="90" text="Click Me!" onAction="#handleButtonAction"  />
    <Label fx:id="label" layoutX="126" layoutY="120" minHeight="16" minWidth="69" prefHeight="16" prefWidth="69" />
  </children>
</AnchorPane>
```

FXML Document - GXON Version:

```
[?import java.lang.*]
[?import java.lang.*]
[?import javafx.scene.*]
[?import javafx.scene.control.*]
[?import javafx.scene.layout.*]

[AnchorPane id="AnchorPane" prefHeight=200 prefWidth=320 xmlns:fx="http://javafx.com/fxml"   
            fx:controller="temp.Temp"
  [children
    [Button fx:id="button"layoutX=126 layoutY=90 text="Click Me!" onAction=#handleButtonAction ]
    [Label fx:id="label" layoutX=126 layoutY=120 minHeight=16 minWidth=69 prefHeight=16 prefWidth=69 ]
  ]
]
```

The second notation is based on identation.

```
?import java.lang.*
?import java.lang.*
?import javafx.scene.*
?import javafx.scene.control.*
?import javafx.scene.layout.*

AnchorPane id="AnchorPane" prefHeight=200 prefWidth=320 xmlns:fx="http://javafx.com/fxml"   
  fx:controller="temp.Temp"
  children
     Button fx:id="button"layoutX=126 layoutY=90 text="Click Me!" onAction=#handleButtonAction 
     Label fx:id="label" layoutX=126 layoutY=120 minHeight=16 minWidth=69 prefHeight=16 prefWidth=69 
  
```


It could be used to crate HTML/XHTML files two:

```
<!DOCTYPE html>
<html>
<body>

<h1>My First Heading</h1>

<p>My first paragraph.</p>

</body>
</html>
```

Can be writen as in GXON as:

```
!DOCTYPE html
html
   body
      h1 |My first Heading
      p  |My first paragraph.
```

And they can be used together:

```
!DOCTYPE html
html
   body
      h1 |My first [b\i| Heading]
      p  |My first paragraph.
```

```
!DOCTYPE html
[html /* Brackets demarcation */
   \body /* Indentation demarcation */
      h1 |My first [b\i| Heading]
      [p  |My first paragraph. /* Brackets demarcation */ ]
]
```


It is a working in progress. As soon as possible the first version of the specification and an Eclipse Editor will be published. Stay tunned.

