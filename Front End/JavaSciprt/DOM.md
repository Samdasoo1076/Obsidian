#2024-04-26  [[2024-04-26 회사]]
## **Document Object Model** : 문서 객체 모델
 └ 문서 객체를 인식하는 방식

트리 구조 
![[Pasted image 20240426170818.png]]


p, b, br 태그 예시로 본 그림
![[Pasted image 20240426171055.png]]

## **node** : tree 구조에서 root 노드를 포함한 모든 개체


아래는 JavaScript를 추가한 코드입니다. (여기서는 <script>태그의 위치가 <body>태그보다 위이기 때문에 onload 메소드를 사용하지 않으면 에러가 나기 때문에 사용하고 있습니다.))


``` html
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title> 문서객체 모델(DOM)</title >
<script type= "text/javascript">
    window.onload = function(){
       //1. 문서 객체 생성
       var header = document.createElement('h2'); //h2 태그를 생성해주는 것
       var textNode = document.createTextNode('Hello DOM');

       //2. 노드(요소/텍스트)를 연결.
       header.appendChild(textNode);

       //3. body 문서 객체에 header 문서 객체를 추가.
       document.body.appendChild(header);
    };
</script>
</head>
<body>
   <h1 id ="header_1" name= "" >HEADER-1 </h1 >
   <div >
      <h1 id = "header_2">HEADER-2</h1 >
   </div >
   <hr >
   <h1 id = "clock"></h1>
</body>
</html>
```