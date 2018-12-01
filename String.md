# 문자열

## 문자열 합치기

```swift
let hello = "안녕"
let world = "세상"
let message = hello + " " + world + "!" // "안녕 세상!"

var s = "안녕"
s = s + " 친구야" // "안녕 친구야"
s += "!!"       // "안녕 친구야!!"
```

## 문자열 길이

```swift
let s = "문자열 길이"
s.count // 6
```

## 문자열 인덱스

```swift
let i = String.Index(encodedOffset: 0)
```

## 문자열 일부 가져오기

```swift
let s = "스위프트는 참 좋다"
let i = String.Index(encodedOffset: 0)
s[i] // "스" : Character

let from = String.Index(encodedOffset: 0)
let to = String.Index(encodedOffset: 3)
s[from...to] // "스위프트" : [Substring]

// Substring을 String으로 만들기
let s2 : String = String(s[from...to])
```

## 문자열을 배열로 만들기

```swift
let s = "안녕 세상아"
let arr = Array(s) // ["안", "녕", " ", "세", "상", "아"]
```

## 문자열 바꾸기 

```swift
let s = "안녕 세상아"
let to = String.Index(encodedOffset: 1)
s.replaceSubrange(s.startIndex...to, with: "Hej") // "Hej 세상아"
s // "Hej 세상아"
```
