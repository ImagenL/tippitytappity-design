# tippitytappity-design

tippitytappity is a program to practice typing


## Data model

```mermaid
classDiagram
  ExampleParent <|-- ExampleChild
  previousTest --> user
  allPhrases --> typingTest
  class allPhrases{
        - phrases: vector~vector~string~~
        + randPhrases(length: int) vector~vector~string~~
  }
  class typingTest{
      - startTime: int
      - endTime: int
      - usedPhrases: vector~vector~string~~
      - userInput: string
      + compareTyped(userInput: string) int
      + getPhrases(length: int) vector~vector~string~~
      + setStartTime()
      + setEndTime()
  }
  class previousTest{
      - accuracy: int
      - speed: int
      + displayAccuracy()
      + displaySpeed()
  }
  class user{
      - userID: int
      - previousTests: vector~previousTest~

  }

```
