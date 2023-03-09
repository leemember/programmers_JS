## 0309 가운데 글자 가져오기

### 문제설명

단어 s의 가운데 글자를 반환하는 함수, solution을 만들어 보세요.
단어의 길이가 짝수라면 가운데 두글자를 반환하면 됩니다.

### 제한사항

- s는 길이가 1이상, 100이하인 스트링입니다.

### 입출력 예

| s       | return |
| ------- | ------ |
| "abcde" | "c"    |
| "qwer"  | "we"   |

### Code

```
function solution(s) {
    // 올림하는 이유는 나누었을 때 0.5로 떨어지는 수도 있기 때문이다.
    const start = Math.ceil(s.length / 2) -1;

    // 짝수일 경우 2글자 가져오기
    if(s.length % 2 === 0) {
        return s.substr(start, 2)
    } else {
        // 홀수일 경우 1글자만 가져오기
        return s.substr(start, 1)
    }
}
```
