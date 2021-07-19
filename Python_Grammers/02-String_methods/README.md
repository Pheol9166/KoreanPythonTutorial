# 문자열의 편리한 기능들
파이썬의 문자열은 더 편리하게 다루기 위한 여러 기능들을 알아봅시다.

## 1. 따옴표 이스케이프 문자
문자열을 사용할 때, 문자열 기호 (작은따옴표`'` 또는 큰따옴표`"`)를 문자열 내부에서 사용해야 할 때가 있습니다. 하지만, 그냥 문자열 기호를 사용하게 되면 문자열이 끝난걸로 인식되어 오류가 발생하게 됩니다.
```python
text = "그는 "안녕하세요" 라고 말했다."
```
그렇다면, 문자열 내부에서 따옴표는 어떻게 써야 할까요?
**`이스케이프 문자`** 를 사용해 이 문제를 해결할 수 있습니다.
```python
text = "그는 \"안녕하세요\" 라고 말했다."
```
이스케이핑 문자는 **`\`** 문자를 사용합니다. 한글 키보드로는 `￦` 키를 눌러 사용할 수 있습니다.
이스케이핑 문자는 따옴표 표현 이외에도 여러가지가 있습니다. 자세한 내용은 [이스케이프 문자 알아보기](https://zetawiki.com/wiki/%EC%9D%B4%EC%8A%A4%EC%BC%80%EC%9D%B4%ED%94%84_%EB%AC%B8%EC%9E%90) 를 참고해 주세요.

## 2. 문자열 자르기
문자열 타입인 **`str`**은 문자열을 분할하기 위한 메소드인 split을 제공합니다.
```python
text = 'Hello This Is Python!'
print(text.split(" "))
```
> ['Hello', 'This', 'Is', 'Python!]

split() 메소드는 자르기 위한 기준이 되는 문자열을 인자로 받습니다. 위 예제에서는, 띄어쓰기 (` `) 를 기준으로 자르기 위해
`text.split(' ')` 처럼 사용했습니다.

## 3. 문자열의 시작, 끝 검사하기
문자열 타입인 **`str`**은 문자열의 앞, 뒤에 특정 문자열이 위치하는지 검사하는 메소드를 제공합니다.
```python
text = "Hello Python!"
if text.startswith("Hello"):
    print("Hello!")
if text.endswith("!"):
    print("!!!")
```
**`startswith()`** 메소드는 이 문자열이 인자로 전달받은 문자열로 시작하는지 확인해, True 또는 False를 반환합니다. 
위 코드에서는 text 변수에 저장된 문자열이 `"Hello"` 라는 문자열로 시작되는지 확인하기 위해, `text.startswith("Hello")` 를 사용했습니다.

**`endswith()`** 메소드는 이 문자열이 인자로 전달받은 문자열로 끝나는지 확인해, True 또는 False를 반환합니다.
위 코드에서는 text 변수에 저장된 문자열이 `"!"` 라는 문자열로 끝나는지 확인하기 위해, `text.endswith("!")` 를 사용했습니다.

## 4. 문자열을 대문자로, 소문자로 바꾸기
```python
text = "hello"
print(text.capitalize())
print(text.upper())
print(text.lower())
```
capitalize() 메소드는 문자열의 첫 글자를 대문자로, 나머지 글자를 소문자로 만드는 메소드입니다.

upper() 메소드는 문자열의 모든 글자를 대문자로 만드는 메소드입니다.

lower() 메소드는 문자열의 모든 글자를 소문자로 만드는 메소드입니다.

```python
text = "HELLO"
print(text.isupper())
print(text.islower())
```
isupper() 메소드는 이 문자열이 모두 대문자로 이루어져있을때 True를 반환하는 메소드입니다.

islower() 메소드는 이 문자열이 모두 소문자로 이루어져있을때 True를 반환하는 메소드입니다.