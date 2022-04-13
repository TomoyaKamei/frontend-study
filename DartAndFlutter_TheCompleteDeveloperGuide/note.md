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

myName(){
  return "Tomoya";
}
```

### Lecture13. Object Oriented Programming in Dart

### Lecture14. Creating Classes

### Lecture15. Creating Class Instances

### Lecture16. Constuctor Functions

### Lecture17. Review on Constructors


## Section3. Staying on Target with Dart