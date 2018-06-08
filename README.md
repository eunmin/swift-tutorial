# swift 공부

## 변수와 상수

- var
- let

```swift
var 이름 = 값
let 이름 = 값

var x = 1
let y = 2

x = 2
```

- 타입

```swift
var a = "a"

a = 1
```

- 사용할 수 없는 이름

```swift
var 1a = 1

var class = 1
var enum = 2
```

## 자료형

```swift
var a : String = "hello"
```

- Int
- UInt
- Float
- Double
- Bool

```swift
var a : Bool = true
```

- String

```swift
var a : String = "aaa"
```

- Character

```swift
var a : Character = "a"
```

## 타입 추론

```swift
var a = 1

var b

b = 2

var a : UInt = 1
```

## 타입 변환

```swift
var a = String(1)
var b = Int("1")
```

## 문자열 템플릿

```swift
var a = 1
var b = 2
var c = "하하하하 \(a) \(b)"
```

## 여러줄의 문자열

```swift
var d = """
한줄
두줄
세줄
"""
```

## 연산자

```swift
-2
1 + 1
2 - 1
x * y
x / y
10 % 3
```

## 비교 연산자

```swift
2 > 1
2 < 1
2 <= 1
2 >= 1
2 == 1
2 != 1
```

```swift
!(2 > 1)
1 == 1 && 2 == 2
1 == 1 || 2 == 2
```

## 범위

```swift
1 ... 5
1 ..< 5
```

## 대입 연산자

```swift
a = 1
a += 1
a -= 1
a *= 1
a /= 1
a %= 1
```

## 배열

```swift
var shoppingList = ["catfish", "water", "tulips", "blue paint"]
shoppingList[1] = "bottle of water"

let emptyArray = [String]()
```

## 딕셔너리

```swift
var occupations = [
    "Malcolm": "Captain",
    "Kaylee": "Mechanic",
]
occupations["Jayne"] = "Public Relations"

let emptyDictionary = [String: Float]()
```

## 반복문

```swift
for i in 1 ... 10 {
  print(i)
}
```

```swift
for _ in 1 ... 10 {
  print("뭉뭉이")
}
```

```swift
for i in 1 ... 10 {
  for j in 1 .. 2 {
    print("\(i) , \(j)")
  }
}
```

```swift
var n = 1
while n < 10 {
  n = n + 1
}
print("\(n)")
```

```swift
var m = 2
repeat {
    m *= 2
} while m < 100
print(m)
```

```swift
let interestingNumbers = [
    "Prime": [2, 3, 5, 7, 11, 13],
    "Fibonacci": [1, 1, 2, 3, 5, 8],
    "Square": [1, 4, 9, 16, 25],
]
var largest = 0
for (kind, numbers) in interestingNumbers {
    for number in numbers {
        if number > largest {
            largest = number
        }
    }
}
print(largest)
```
