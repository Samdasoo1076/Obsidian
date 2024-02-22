#2024-02-19
#2024-02 
#2024- 

django에선 안전하게 데이터를 보내기 위해선 CSRF 토큰 방식으로 보내야함

그러기 위해선 form 태그 안에 csrf_token을 넣어야 한다

```html
<form onsubmit="return flase;">  
    {% csrf_token %}  
<input type="text" id="user-input" placeholder="메시지를 입력하세요...">  
<button id="send-btn" onclick="sendMessage()">전송</button>  
</form>
```

![[Pasted image 20240221141607.png]] url에 토큰이 생긴 모습 