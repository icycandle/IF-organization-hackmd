# IF Introduction with C4 model

## 組織與環境脈絡 (Context)

```plantuml
@startuml C4_Elements
!include https://raw.githubusercontent.com/plantuml-stdlib/C4-PlantUML/master/C4_Container.puml

System(ifAlias, "(IF) 想像朋友寫作會", "非營利組織")

System(prizeAlias, "文學獎", "國內外競賽型文學獎、年度書獎")
System(eduAlias, "學院系統", "初階創作能力訓練")
System(govAlias, "政府政策", "創作補助/產業政策/教育政策")
System(busiAlias, "商業環境", "出版社/課程/")

Rel(ifAlias, eduAlias, "社群資源", "中階訓練")
Rel(eduAlias, ifAlias, "人力資源", "基礎訓練")

Rel(prizeAlias, ifAlias, "社會證明")
Rel(ifAlias, prizeAlias, "參賽文本")

Rel(govAlias, ifAlias, "宏觀資源")
Rel(ifAlias, govAlias, "實務能動性")

Rel(ifAlias, busiAlias, "人力資源")
Rel(busiAlias, ifAlias, "經濟回報")


@enduml
```