- ### **사용방법**

> #### 1. 유튜브 접속
>
> #### 2. 구독 버튼 클릭
>
> #### 3. 관리 버튼 클릭
>
> #### 4. f12버튼을 눌러 개발자 도구의 Console창 클릭
>
> #### 5. 아래 Script Code를 복사하고 index의 값만 변경하여 원하는 알람 설정 (0: 전체, 1: 맞춤설정, 2: 없음)

<br><br>

- ### **Script Code**

```javascript
// 알람 설정 버튼을 모두 가져온다.
let notify = document.querySelectorAll(
  ".style-scope ytd-channel-renderer ytd-subscription-notification-toggle-button-renderer"
);

//알람 설정 버튼을 눌렀을 때 나오는 작은 창을 가져온다.
await notify[0].click();
let status = Array.from(
  document.querySelectorAll("ytd-popup-container paper-item")
);

//알람을 어떻게 받고싶은지 설정한다.
// 0 : 전체
// 1 : 맞춤 설정
// 2 : 없음
let index = 2;

//모든 구독 채널에 대해서 알람설정 변경
for (var i = 0; i < notify.length; i++) {
  await notify[i].click();
  status[index].click();
}
```

<br><br>

- ### **만든 계기**

> 유튜브에 알람 기능을 한번에 여러개 제어하는 방법이 없어서 javascript를 이용해 만들어보았다.

<br><br>

- ### **유튜브 시연 영상 링크**
  [바로가기](https://www.youtube.com/watch?v=s_UY_t-lfWc&feature=youtu.be)
