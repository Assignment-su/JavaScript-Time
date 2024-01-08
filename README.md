### 📆 JavaScript Time

> 연도와 달, 날짜까지 표시되는 시계 기능 구현


![2024-01-08-15_35_48](https://github.com/Assignment-su/JavaScript-Time/assets/99783474/2383b84c-28cb-46cb-a7ba-964ca2c9e22f)

```javascript
function updateClock() {
        // 현재 시간을 가져오기
        var currentTime = new Date();

        // 시, 분, 초 가져오기
        var hours = currentTime.getHours();
        var minutes = currentTime.getMinutes();
        var seconds = currentTime.getSeconds();

        // 시간이 한 자리 수일 경우 앞에 0을 추가
        hours = (hours < 10) ? "0" + hours : hours;
        minutes = (minutes < 10) ? "0" + minutes : minutes;
        seconds = (seconds < 10) ? "0" + seconds : seconds;

        // 시간을 표시할 요소에 텍스트 설정
        var clockElement = document.getElementById("clock");
        clockElement.textContent = hours + ":" + minutes + ":" + seconds;

    }

    // 1초마다 updateClock 함수 호출
    setInterval(updateClock, 1000);

    function toPadStart(num){
        return String(num).padStart(2,'0')
        }

        function updateClock() {
        const now = new Date();
        const year = now.getFullYear();
        const month = now.getMonth() + 1;
        const date = now.getDate();
        const hours = now.getHours();
        const minutes = now.getMinutes();
        const seconds = now.getSeconds();
        const clock = document.getElementById("clock");
        clock.innerHTML = `${year}년 ${toPadStart(month)}월
                           ${toPadStart(date)}일 ${toPadStart(hours)}시
                           ${toPadStart(minutes)}분 ${toPadStart(seconds)}초`;
        // 1초마다 시간을 업데이트합니다.
        setTimeout(updateClock, 1000);
    }
```

---


* API : API는 응용 프로그램 프로그래밍 인터페이스(Application Programming Interface)의 약자로, 각각의 소프트웨어가 서로 통신하고 상호작용할 수 있도록 설계된 규격이다.

*  비동기 처리(Asynchronous processing)

> 프로그램이 여러 작업을 동시에 처리하도록 설계된 방식
>
> 이는 작업이 독립적으로 실행되어서, 한 작업의 완료를 기다리지 않고 다른 작업을 시작할 수 있는 구조를 의미한다.
>
> 비동기 처리는 프로그램의 효율성과 성능을 높이는 데 도움이 된다.
>
> 비동기 처리 방식에서는 파일 업로드가 진행되는 동안에도 사용자가 애플리케이션의 다른 부분을 사용하거나 새로운 작업을 시작할 수 있다.
>
> 비동기 처리는 자바스크립트와 같은 프로그래밍 언어에서 콜백 함수, 프로미스(Promise), async/await와 같은 기능을 통해 구현이 가능하다.
