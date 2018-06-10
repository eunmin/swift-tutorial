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
var cities = ["Seoul", "New York", "LA", "Santiago"]

cities[0]
cities[1]
cities[10]
cities.count

let length = cities.count

for i in 0..<length {
  print("\(i)번째 배열 원소는 \(cities[i])입니다.")
}

for city in cities {
  print("배열 원소는 \(city)입니다.")
}
```

- 초기화

```swift
var cities = [String]()

var cities = [String]

cities = []

cities.isEmpty
```

- 추가

```swift
var cities = [String]()

cities.append("Seoul")
cities.append("New York")
cities.insert("Tokyo", at: 1)
cities.append(contentsOf: ["Dubai", "Sydney"])
```

```swift
cities[0...2]
```

## 집합 (Set)

```swift
var genres : Set = ["Classic", "Rock", "Balad"]

genres.contains("Rock")
```

## 튜플

```swift
var t = (100, 200)

var t : (Int, Int) = (100, 200)

t.0
t.1

var (x, y) = t
x
y

var (x, _) = t
x
```

## 딕셔너리

```swift
var capital = ["KR":"Seoul", "EN":"London", "FR":"Paris"]

capital["KR"]

capital["XX"]

var c = capital["XX"] // Optional(String)

c?.capitalized
```

- 초기화

```swift
var capital = [String : String]()

var capital : [String : String]

capital = [:]

capital.isEmpty
```

- 값 추가

```swift
capital["JP"] = "Tokyo"
```

- 순회 탐색

```swift
for row in capital {
  let (k, v) = row
  print("키는 \(k), 값은 \(v)입니다.")
}

for (k, v) in capital {
  print("키는 \(k), 값은 \(v)입니다.")
}
```

## 옵셔널

```swift
let num = Int("123")

let num = Int("Swift")

num + 1
```

- 옵셔널 타입 선언하기

```swift
var num : Int

num = 1

num = nil

var num : Int?

num = nil

var cites : [String]?
```

- 옵셔널 값 사용하기 (unwrapping)

```swift
var num : Int? = 1

num! + 1

var num : Int? = nil

num! + 1

if num != nil {
  var result = num! + 1
  print("결과는 \(result) 입니다.")
} else {
  print("실패!")
}

var str = "1"

if let num = Int(str) {
  var result = num! + 1
  print("결과는 \(result) 입니다.")
} else {
  print("실패!")
}
```

- 옵셔널 자동 해제

```swift
var num : Int? = nil

if num == 2 {

}
```

- 해제를 신경 안써도 되는 옵셔널 타입

형식상 옵셔널로 정의해야 하지만, 실제로 사용할 때는 절 때 nil 값이 대입될 가능성이 없는 변수 일때

```swift
var num : Int! = 1

num + 1
```

## 함수

- 함수 만들기

```swift
func 함수명(매개변수1: 타입, 매개변수2: 타입 ...) -> 반환타입 {
  내용
  내용
  ...
  return 반환값
}
```

```swift
func s0110() {
  print("사당역 5번 출구")
}

s0110()
```

```swift
func printHello() {
  print("안녕하세요")
}

func getHello() -> String {
  return "안녕하세요"
}

func printHelloWithName(name: String) {
  println("\(name)님, 안녕하세요")
}

func getHelloWithName(name: String) -> String {
  return "\(name)님, 안녕하세요"
}

printHelloWithName(name: "뭉뭉이")

func add(x: Int, y: Int) -> Int {
  return x + y
}

add(x: 1, y: 2)

add(x:y:)(1, 2)

func add(a x: Int, b y: Int) -> Int {
  return x + y
}

add(a: 1, b: 2)

func add(_ x: Int, _ y: Int) -> Int {
  return x + y
}

add(1, 2)
```

## 타입 엘리어스

```swift
typealias UserName = String

var x : UserName

x = "뭉뭉이"

typealias Point = (Int, Int)
```

## 변수의 범위

```swift
var a = 1

if a == 1 {
    var a = 2
    print(a)
}

print(a)
```
