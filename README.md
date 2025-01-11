<h1 align="center">Markdown Cheatsheet</h1>

# Type here...
Type here...

## Type here...

Type here...

### Type here...
Type here...
-
# Tables
### 2 Column Table
| Month    | Savings |
| -------- | ------- |
| January  | $250    |
| February | $80     |
| March    | $420    |

### 3 Column Table
| Item              | In Stock | Price |
| :---------------- | :------: | ----: |
| Python Hat        |   True   | 23.99 |
| SQL Hat           |   True   | 23.99 |
| Codecademy Tee    |  False   | 19.99 |
| Codecademy Hoodie |  False   | 42.99 |

### 3 Column Table with Images
|Content    |Example1    |Example2    |
| --- | --- | --- |
| <img width="200" atl="ball1" src="https://github.com/user-attachments/assets/569decce-86c8-40e4-a145-d6182cb8ca74"> | <img width="200" atl="ball2" src="https://github.com/user-attachments/assets/569decce-86c8-40e4-a145-d6182cb8ca74"> | <img width="200" atl="ball3" src="https://github.com/user-attachments/assets/569decce-86c8-40e4-a145-d6182cb8ca74">|
| <img width="200" atl="ball4" src="https://github.com/user-attachments/assets/569decce-86c8-40e4-a145-d6182cb8ca74"> | <img width="200" atl="ball5" src="https://github.com/user-attachments/assets/569decce-86c8-40e4-a145-d6182cb8ca74"> | <img width="200" atl="ball6" src="https://github.com/user-attachments/assets/569decce-86c8-40e4-a145-d6182cb8ca74"> |
| <img width="200" atl="ball7" src="https://github.com/user-attachments/assets/569decce-86c8-40e4-a145-d6182cb8ca74"> | <img width="200" atl="ball8" src="https://github.com/user-attachments/assets/569decce-86c8-40e4-a145-d6182cb8ca74"> | <img width="200" atl="ball9" src="https://github.com/user-attachments/assets/569decce-86c8-40e4-a145-d6182cb8ca74"> |  

### Table Alignment
- :-- means the column is left aligned.
- --: means the column is right aligned.
- :-: means the column is center aligned.
-
# How to add graphs -> Mermaid
The best way to add graphs in Markdown is with [Mermaid](https://mermaid.js.org/). It is a JavaScript-based diagramming and charting tool that integrates seamlessly with Markdown. It allows users to create visually appealing diagrams, such as flowcharts, sequence diagrams, Gantt charts, and more, directly within Markdown documents using a simple and intuitive syntax. By embedding Mermaid code blocks in Markdown, you can dynamically generate diagrams that are easy to maintain and share, making it a popular choice for documentation and technical writing.

<p>You can make many types of graphs, from diagrams to flow chart.</p>

### Pie Chart
```mermaid
%%{init: {"pie": {"textPosition": 0.5}, "themeVariables": {"pieOuterStrokeWidth": "5px"}} }%%
pie showData
    title Key elements in Product X
    "Calcium" : 42.96
    "Potassium" : 50.05
    "Magnesium" : 10.01
    "Iron" :  5
```
### Bar Chart
```mermaid
    xychart-beta
    title "Sales Revenue"
    x-axis [jan, feb, mar, apr, may, jun, jul, aug, sep, oct, nov, dec]
    y-axis "Revenue (in $)" 4000 --> 11000
    bar [5000, 6000, 7500, 8200, 9500, 10500, 11000, 10200, 9200, 8500, 7000, 6000]
    line [5000, 6000, 7500, 8200, 9500, 10500, 11000, 10200, 9200, 8500, 7000, 6000]
 ```   
### Diagram
```mermaid
  graph TD;
      A-->B;
      A-->C;
      B-->D;
      C-->D;
```
```mermaid
sequenceDiagram
    participant dotcom
    participant iframe
    participant viewscreen
    dotcom->>iframe: loads html w/ iframe url
    iframe->>viewscreen: request template
    viewscreen->>iframe: html & javascript
    iframe->>dotcom: iframe ready
    dotcom->>iframe: set mermaid data on iframe
    iframe->>iframe: render mermaid
```
### Mindmap
```mermaid
 mindmap
  root((mindmap))
    Origins
      Long history
      ::icon(fa fa-book)
      Popularisation
        British popular psychology author Tony Buzan
    Research
      On effectivness<br/>and features
      On Automatic creation
        Uses
            Creative techniques
            Strategic planning
            Argument mapping
    Tools
      Pen and paper
      Mermaid
```
### User Journey Chart
```mermaid
 journey
    title My working day
    section Go to work
      Make tea: 5: Me
      Go upstairs: 3: Me
      Do work: 1: Me, Cat
    section Go home
      Go downstairs: 5: Me
      Sit down: 3: Me
```
### Block Chart
```mermaid
 block-beta
    columns 3
    doc>"Document"]:3
    space down1<[" "]>(down) space

  block:e:3
          l["left"]
          m("A wide one in the middle")
          r["right"]
  end
    space down2<[" "]>(down) space
    db[("DB")]:3
    space:3
    D space C
    db --> D
    C --> db
    D --> C
    style m fill:#d6d,stroke:#333,stroke-width:4px
    
```
### Git Hierarchy Graph
```mermaid
 gitGraph
    commit
    commit
    branch develop
    checkout develop
    commit
    commit
    checkout main
    merge develop
    commit
    commit
```
### Packet Graph
```mermaid
 ---
title: "TCP Packet"
---
packet-beta
  0-15: "Source Port"
  16-31: "Destination Port"
  32-63: "Sequence Number"
  64-95: "Acknowledgment Number"
  96-99: "Data Offset"
  100-105: "Reserved"
  106: "URG"
  107: "ACK"
  108: "PSH"
  109: "RST"
  110: "SYN"
  111: "FIN"
  112-127: "Window"
  128-143: "Checksum"
  144-159: "Urgent Pointer"
  160-191: "(Options and Padding)"
  192-255: "Data (variable length)"
```
### Class Diagram
```mermaid
 classDiagram
    Animal <|-- Duck
    Animal <|-- Fish
    Animal <|-- Zebra
    Animal : +int age
    Animal : +String gender
    Animal: +isMammal()
    Animal: +mate()
    class Duck{
      +String beakColor
      +swim()
      +quack()
    }
    class Fish{
      -int sizeInFeet
      -canEat()
    }
    class Zebra{
      +bool is_wild
      +run()
    }
```
### Quadrant Chart
```mermaid
quadrantChart
    title Reach and engagement of campaigns
    x-axis Low Reach --> High Reach
    y-axis Low Engagement --> High Engagement
    quadrant-1 We should expand
    quadrant-2 Need to promote
    quadrant-3 Re-evaluate
    quadrant-4 May be improved
    Campaign A: [0.3, 0.6]
    Campaign B: [0.45, 0.23]
    Campaign C: [0.57, 0.69]
    Campaign D: [0.78, 0.34]
    Campaign E: [0.40, 0.34]
    Campaign F: [0.35, 0.78]  
```
### ER Chart
```mermaid
 erDiagram
    CUSTOMER }|..|{ DELIVERY-ADDRESS : has
    CUSTOMER ||--o{ ORDER : places
    CUSTOMER ||--o{ INVOICE : "liable for"
    DELIVERY-ADDRESS ||--o{ ORDER : receives
    INVOICE ||--|{ ORDER : covers
    ORDER ||--|{ ORDER-ITEM : includes
    PRODUCT-CATEGORY ||--|{ PRODUCT : contains
    PRODUCT ||--o{ ORDER-ITEM : "ordered in"
```
