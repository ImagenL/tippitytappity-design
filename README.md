# tippitytappity-design

tippitytappity is a program to practice typing


## Data model

```mermaid
classDiagram
  ExampleParent <|-- ExampleChild
  previousTest --> user
  allPhrases --> typingTest
  class ExampleParent{
        - name: string
        - email: string
        - password: string
        + login(user: string, pass: string) boolean
        + get_email() string
  }
  class ExampleChild{
        - badges vector~string~
        + add_badge(title: string)
        + get_badges() vector~string~
  }

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
