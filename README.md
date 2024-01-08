### 📆 JavaScript Time

> 연도와 달, 날짜까지 표시되는 시계 기능 구현

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
