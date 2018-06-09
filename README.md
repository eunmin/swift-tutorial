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

## 반복문

- for in 구문

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

- while 구문

```swift
var n = 1
while n < 10 {
  n = n + 1
}
print("\(n)")
```

- repeat while 구문

```swift
var m = 2
repeat {
    m *= 2
} while m < 100
print(m)
```

## 조건문

- if else 구문

```swift
var adult = 19
var age = 21

if age < adult {
  print("당신은 미성년자!")
}

if age >= adult {
  print("당신은 성년자!")
}
```

```swift
var adult = 19
var age = 21

if age < adult {
  print("당신은 미성년자!")
} else {
  print("당신은 성년자!")
}
```

```swfit
var adult = 19
var age = 21
var gender = "M"

if age < adult {
  if gender  == "M" {
    print("당신은 남자 미성년자!")
  } else {
    print("당신은 여자 미성년자!")
  }
} else {
  if gender  == "M" {
    print("당신은 남자 성년자!")
  } else {
    print("당신은 여자 성년자!")
  }
}
```

```swift
if gender == "M" {
  print("남자")
} else if gender == "F" {
  print("여자")
} else {
  print("남자도 여자도 아님")
}
```

- guard 구문

```swift
func divide(base: Int) {
  guard base != 0 else {
    print("0으로 나눌 수 없습니다")
    return
  }

  let result = 100 / base
  print(result)
}
```

- switch 구문

```swift
let val = 2

switch val {
  case 1 :
    print("1이다")
  case 2 :
    print("2이다")
  case 3 :
    print("3이다")
  default:
    print("모르겠다")
}
```

- break 구문

```swift
for row in 0...5 {
  if row > 2 {
    break
  }
  print("\(row) 실행")
}
```

- continue 구문

```swift
for row in 0...5 {
  if row > 2 {
    continue
  }
  print("\(row) 실행")
}
```

## 배열

```swift
var shoppingList = ["catfish", "water", "tulips", "blue paint"]
shoppingList[1] = "bottle of water"

let emptyArray = [String]()

for item in shoppingList {
  print("아이템: \(item)")
}
```

- 추가

```swift
var cities = [String]()

cities.append("Seoul")
cities.append("New York")
cities.insert("Tokyo", at: 1)
cities.append(contentsOf: ["Dubai", "Sydney"])
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
