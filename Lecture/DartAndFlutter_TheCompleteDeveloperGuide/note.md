# Dart and Flutter: The Complete Developer's Guide



## Section1. Let's dive in!


## Section2. A Dart introduction


### Lecture5. Dart Overview

### Lecture6. The Dartpad Editor

### Lecture7. Our First Program
- 関数定義は、```戻り型 関数名(引数型 引数名){～}```となっている。
```dart
void main(){
  var name = myName();
  print('My name is $name');
}

String myName(){
  return "Tomoya";
}
```

### Lecture8. Pulling the Pieces Apart
- varは、型を使用しない変数定義に使用される。

```dart
void main(){
  var name = myName();
  print('My name is $name');
}

String myName(){
  return "Tomoya";
}
```

### Lecture9. Functions in Dart
- main関数は定義する必要がある。
```dart
void main(){
  var name = myName();
  print('My name is $name');
}

String myName(){
  return "Tomoya";
}
```

### Lecture10. Introduction to Types
- Dartのvarを使用した場合、初期化した型から変更する事は出来ない。
- dynamic型は全ての型を意味する。
- 関数は戻り値に型を付ける必要がない。
```dart
void main(){
  var name = myName();
  name = 123; // エラー
  
  print('My name is $name');
}

myName(){
  return "Tomoya";
}

```


### Lecture11. Why use types?
- 型は以下のものが存在する。
    - String
    - int
    - double
    - dynamic
- 型は以下の利点を持つ。
    1. データ構造の可読性が高い。
    2. コードが高速化する。
    3. 単体テストの数を減らせる。

```dart
void main(){
  var name = myName();
  var len = name.length; 
  
  print('My name is $name and my age is $len');
}

myName(){
  return "Tomoya";
}

```

### Lecture12. String Interpolation
- $は()で囲う事で複雑な表現に対応できる。
```dart 
void main(){
  var name = myName();
  var len = name.length; 
  
  print('My name is $(name.length) and my age is $len');
}

String myName(){
  return "Tomoya";
}
```

### Lecture13. Object Oriented Programming in Dart
```dart


```

### Lecture14. Creating Classes
```dart
class Person{
  String firstName;

  void printName(){
    print(firstName);
  }
}

void main(){
  var david = new Person();
  david.firstName = "David";
  david.printName();
}
```


### Lecture15. Creating Class Instances
```dart
class Person{
  String firstName;

  void printName(){
    print(firstName);
  }
}

void main(){
  var david = new Person();
  david.firstName = "David";
  david.printName();
}
```

### Lecture16. Constuctor Functions
```dart
class Person{
  String firstName;

  Person(this.firstName);

  void printName(){
    print(firstName);
  }
}

void main(){
  var david = new Person("David");
  david.printName();
}
```

### Lecture17. Review on Constructors


## Section3. Staying on Target with Dart

### Lecture18. app description

### Lecture19. OOP Design Flow
 
### Lecture20. Adding Fields to Classes
```dart
class Deck{
  List<Card> cards;

  Deck()

  List<Card> makeDeck(){}
  void printCards(){}
  void Shuffle(){}
  List<Card> cardsWithSuit(String suit){}
  List<Card> deal(Int cardNum){}
  void removeCard(Card card){}
}

class Card{
  String suit;
  String rank;

  Card(this.suit, this.rank);

  void print(){
    print("$suit of $rank");
  }
}

void main(){
}
```

### Lecture21. Associated with Constructors

### Lecture22. More Initialization with Constructors
```dart
void main(){
  var deck = new Deck();

}

class Deck{
  List<Card> cards = [];

  Deck(){
    var ranks = ["Ace", "Two", "Three", "Four", "Five", "Six", "Seven", "Eight", "Nine", "Ten", "Jack", "Queen", "King"];
    var suits = ["Hearts", "Diamonds", "Spades", "Clubs"]

    for (var suit in suits){
      for (var rank in ranks){
        cards.add(new Card(suit, rank));
      }
    }
  }

  List<Card> makeDeck(){}
  void printCards(){}
  void Shuffle(){}
  List<Card> cardsWithSuit(String suit){}
  List<Card> deal(Int cardNum){}
  void removeCard(Card card){}
}

class Card{
  String suit;
  String rank;

  Card(this.suit, this.rank);

  void print(){
    print("$suit of $rank");
  }
}
```

### Lecture23. For Loops
```dart
void main(){
  var deck = new Deck();

}

class Deck{
  List<Card> cards = [];

  Deck(){
    var ranks = ["Ace", "Two", "Three", "Four", "Five", "Six", "Seven", "Eight", "Nine", "Ten", "Jack", "Queen", "King"];
    var suits = ["Hearts", "Diamonds", "Spades", "Clubs"]

    for (var suit in suits){
      for (var rank in ranks){
        cards.add(new Card(suit, rank));
      }
    }
  }

  List<Card> makeDeck(){}
  void printCards(){}
  void Shuffle(){}
  List<Card> cardsWithSuit(String suit){}
  List<Card> deal(Int cardNum){}
  void removeCard(Card card){}
}

class Card{
  String suit;
  String rank;

  Card(this.suit, this.rank);

  void print(){
    print("$suit of $rank");
  }
}
```

### Lecture24. Adding Elements to Lists
```dart
void main(){
  var deck = new Deck();

}

class Deck{
  List<Card> cards = [];

  Deck(){
    var ranks = ["Ace", "Two", "Three", "Four", "Five", "Six", "Seven", "Eight", "Nine", "Ten", "Jack", "Queen", "King"];
    var suits = ["Hearts", "Diamonds", "Spades", "Clubs"]

    for (var suit in suits){
      for (var rank in ranks){
        cards.add(new Card(suit, rank));
      }
    }
  }

  List<Card> makeDeck(){}
  void printCards(){}
  void Shuffle(){}
  List<Card> cardsWithSuit(String suit){}
  List<Card> deal(Int cardNum){}
  void removeCard(Card card){}
}

class Card{
  String suit;
  String rank;

  Card(this.suit, this.rank);

  void print(){
    print("$suit of $rank");
  }
}
```

### Lecture25. MOre on Variable Initialization
```dart
void main(){
  var deck = new Deck();
}

class Deck{
  List<Card> cards = [];

  Deck(){
    var ranks = ["Ace", "Two", "Three", "Four", "Five", "Six", "Seven", "Eight", "Nine", "Ten", "Jack", "Queen", "King"];
    var suits = ["Hearts", "Diamonds", "Spades", "Clubs"]

    for (var suit in suits){
      for (var rank in ranks){
        cards.add(new Card(suit, rank));

      }
    }
  }

  List<Card> makeDeck(){}
  void printCards(){}
  void Shuffle(){}
  List<Card> cardsWithSuit(String suit){}
  List<Card> deal(Int cardNum){}
  void removeCard(Card card){}
}

class Card{
  String suit;
  String rank;

  Card(this.suit, this.rank);

  void print(){
    print("$suit of $rank");
  }
}
```

### Lecture26. Customizing Print Statements
```dart
void main(){
  var deck = new Deck();
}

class Deck{
  List<Card> cards = [];

  Deck(){
    var ranks = ["Ace", "Two", "Three", "Four", "Five", "Six", "Seven", "Eight", "Nine", "Ten", "Jack", "Queen", "King"];
    var suits = ["Hearts", "Diamonds", "Spades", "Clubs"]

    for (var suit in suits){
      for (var rank in ranks){
        var card = new Card(rank, suit);
        cards.add(card);
      }
    }
  }

  String toString(){
    return cards.toString()
  }

  List<Card> makeDeck(){}
  void printCards(){}
  void Shuffle(){}
  List<Card> cardsWithSuit(String suit){}
  List<Card> deal(Int cardNum){}
  void removeCard(Card card){}
}

class Card{
  String suit;
  String rank;

  Card(this.suit, this.rank);

  void print(){
    print("$suit of $rank");
  }

  String toString(){
    return "$rank of $suit";
  }
}
```

### Lecture27. ToString on Cards
```dart
void main(){
  var deck = new Deck();
}

class Deck{
  List<Card> cards = [];

  Deck(){
    var ranks = ["Ace", "Two", "Three", "Four", "Five", "Six", "Seven", "Eight", "Nine", "Ten", "Jack", "Queen", "King"];
    var suits = ["Hearts", "Diamonds", "Spades", "Clubs"]

    for (var suit in suits){
      for (var rank in ranks){
        var card = new Card(rank, suit);
        cards.add(card);
      }
    }
  }

  String toString(){
    return cards.toString()
  }

  List<Card> makeDeck(){}
  void printCards(){}
  void Shuffle(){}
  List<Card> cardsWithSuit(String suit){}
  List<Card> deal(Int cardNum){}
  void removeCard(Card card){}
}

class Card{
  String suit;
  String rank;

  Card(this.suit, this.rank);

  void print(){
    print("$suit of $rank");
  }

  String toString(){
    return "$rank of $suit";
  }
}
```

### Lecture28. Shuffling a List
```dart
void main(){
  var deck = new Deck();
}

class Deck{
  List<Card> cards = [];

  Deck(){
    var ranks = ["Ace", "Two", "Three", "Four", "Five", "Six", "Seven", "Eight", "Nine", "Ten", "Jack", "Queen", "King"];
    var suits = ["Hearts", "Diamonds", "Spades", "Clubs"]

    for (var suit in suits){
      for (var rank in ranks){
        var card = new Card(rank, suit);
        cards.add(card);
      }
    }
  }

  String toString(){
    return cards.toString()
  }

  void shuffle(){
    cards.shuffle();
  }
  List<Card> cardsWithSuit(String suit){}
  List<Card> deal(Int cardNum){}
  void removeCard(Card card){}
}

class Card{
  String suit;
  String rank;

  Card(this.suit, this.rank);

  void print(){
    print("$suit of $rank");
  }

  String toString(){
    return "$rank of $suit";
  }
}
```

### Lecture29. Annotating Argument Types
```dart
void main(){
  var deck = new Deck();
}

class Deck{
  List<Card> cards = [];

  Deck(){
    var ranks = ["Ace", "Two", "Three", "Four", "Five", "Six", "Seven", "Eight", "Nine", "Ten", "Jack", "Queen", "King"];
    var suits = ["Hearts", "Diamonds", "Spades", "Clubs"]

    for (var suit in suits){
      for (var rank in ranks){
        var card = new Card(rank, suit);
        cards.add(card);
      }
    }
  }

  String toString(){
    return cards.toString()
  }

  void shuffle(){
    cards.shuffle();
  }
  List<Card> cardsWithSuit(String suit){
    List<Card> result = [];

    for (card in cards){
      if card.suit == suit{
        result.add(card)
      }
    }
    return card
  }
  List<Card> deal(Int cardNum){}
  void removeCard(Card card){}
}

class Card{
  String suit;
  String rank;

  Card(this.suit, this.rank);

  void print(){
    print("$suit of $rank");
  }

  String toString(){
    return "$rank of $suit";
  }
}
```

### Lecture30. Filtering Lists
```dart
void main(){
  var deck = new Deck();
}

class Deck{
  List<Card> cards = [];

  Deck(){
    var ranks = ["Ace", "Two", "Three", "Four", "Five", "Six", "Seven", "Eight", "Nine", "Ten", "Jack", "Queen", "King"];
    var suits = ["Hearts", "Diamonds", "Spades", "Clubs"]

    for (var suit in suits){
      for (var rank in ranks){
        var card = new Card(rank, suit);
        cards.add(card);
      }
    }
  }

  String toString(){
    return cards.toString()
  }

  void shuffle(){
    cards.shuffle();
  }
  List<Card> cardsWithSuit(String suit){
    List<Card> result = [];

    return cards.where((card){
      return card.suit == suit;
    });
  }
  List<Card> deal(Int cardNum){}
  void removeCard(Card card){}
}

class Card{
  String suit;
  String rank;

  Card(this.suit, this.rank);

  void print(){
    print("$suit of $rank");
  }

  String toString(){
    return "$rank of $suit";
  }
}
```

### Lecture31. Annotating Argument Types
```dart
void main(){
  var deck = new Deck();
}

class Deck{
  List<Card> cards = [];

  Deck(){
    var ranks = ["Ace", "Two", "Three", "Four", "Five", "Six", "Seven", "Eight", "Nine", "Ten", "Jack", "Queen", "King"];
    var suits = ["Hearts", "Diamonds", "Spades", "Clubs"]

    for (var suit in suits){
      for (var rank in ranks){
        var card = new Card(rank, suit);
        cards.add(card);
      }
    }
  }

  String toString(){
    return cards.toString()
  }

  void shuffle(){
    cards.shuffle();
  }

  List<Card> cardsWithSuit(String suit){
    // (引数) => 処理
    // (引数){return 戻り値} は同じシンタックスとなる。
    return cards.where((card) => card.suit == suit);
  }

  List<Card> deal(Int cardNum){

  }

  void removeCard(Card card){}
}

class Card{
  String suit;
  String rank;

  Card(this.suit, this.rank);

  void print(){
    print("$suit of $rank");
  }

  String toString(){
    return "$rank of $suit";
  }
}
```

### Lecture32. Filtering Lists


### Lecture33. Shorthand Function Syntax
```dart
void main(){
  var deck = new Deck();
}

class Deck{
  List<Card> cards = [];

  Deck(){
    var ranks = ["Ace", "Two", "Three", "Four", "Five", "Six", "Seven", "Eight", "Nine", "Ten", "Jack", "Queen", "King"];
    var suits = ["Hearts", "Diamonds", "Spades", "Clubs"]

    for (var suit in suits){
      for (var rank in ranks){
        var card = new Card(rank, suit);
        cards.add(card);
      }
    }
  }

  String toString(){
    return cards.toString()
  }

  void shuffle(){
    cards.shuffle();
  }

  List<Card> cardsWithSuit(String suit){
    // (引数) => 処理
    // (引数){return 戻り値} は同じシンタックスとなる。
    return cards.where((card) => card.suit == suit);
  }

  List<Card> deal(int handSize){
    var hand = cards.sublist(0, handSize);
    cards = cards.sublist(handSize);

    return hand;
  }
  
  void removeCard(String suit, String rank){
      cards.removeWhere((card) => card.suit == suit && card.rank == rank);
  }
}

class Card{
  String suit;
  String rank;

  Card(this.suit, this.rank);

  void print(){
    print("$suit of $rank");
  }

  String toString(){
    return "$rank of $suit";
  }
}
```

### Lecture34. Removing Individual Records
```dart
```

### Lecture35. RemoveCard Implementation
```dart
```

### Lecture36. Named Parameter
```dart
```