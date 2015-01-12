# GXON
GXON Alternative XML Object Notation

The main objective of GXON is to provide an alternative syntaxe for editing XML files. Cleaner as JSON, AXON, YAML, but preserving some XML semantic (e.g. Namespaces).

It is not intended to be used in general XML documents, as an example, it is not intended to be used to create HTML files. It is designed to provid a cleaner alternative to create Object Graphs.

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

It is a working in progress. As soon as possible the first version of an Eclipse Editor will be published. Stay tunned.

