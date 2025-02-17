## 구현 기능 목록

1. 정답 생성하기
    - `Set`과 `MissionUtils`를 이용해 `1 ~ 9` 범위의 서로 다른 임의의 수 3개 고르기
    
2. 유저가 입력한 값이 유효한지 체크하기

    - `1 ~ 9`범위의 숫자로 이뤄져 있는지? 
        - `0`이 포함되면 안됨
    - 서로 다른 숫자 3개로 이뤄져 있는지? 
        - 길이가 `2` 이하면 안됨 ex) `12`, `54`
        - 중복된 숫자가 있으면 안됨 ex) `322`, `191`
3. 유저의 입력값이 올바르지 않을 때 `alert`로 상황에 맞는 오류 메시지 띄우기

4. 유저의 입력값이 올바르다면 `1`에서 생성한 정답과 비교하기
    - 같은 수가 같은 자리에 있을 때 - 스트라이크
    - 같은 수가 다른 자리에 있을 때 - 볼
    - 같은 수가 없을 때 - 낫싱
        - `reduce` 메서드를 이용해 위 조건대로 스트라이크 카운트와 볼 카운트를 반환 
        
5. 스트라이크 카운트와 볼 카운트를 상황에 맞게 화면에 출력하기

    - 스트라이크 카운트와 볼 카운트 둘 다 있을 때 - x볼 x스트라이크
    - 스트라이크 카운트만 있을 때 - x스트라이크
    - 볼 카운트만 있을 때 - x볼
    - 둘 다 없을 때 - 낫싱
    
6. 정답을 맞췄을 때 `[게임 재시작]` 버튼 출력하기

7. 게임 재시작 버튼을 눌렀을 때 재시작하기
    - 유저 `input`창과 `[게임 재시작]` 버튼 숨기기
    - 정답 재생성하기
    
## 폴더 구조

```
│  LICENSE
│  README.md
│      
├─src
│  │  index.js -> 게임을 초기화하는 모듈
│  │  
│  ├─asset
│  │      constant.js -> 각종 상수를 선언한 모듈
│  │      
│  ├─computer
│  │      computer.js -> 컴퓨터의 기능을 클래스화 시킨 모듈
│  │      
│  └─user
│          user.js -> 유저의 기능을 클래스화 시킨 모듈
```