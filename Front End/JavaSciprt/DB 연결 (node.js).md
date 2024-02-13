[[2024-02-13 회사]]

#2024-02-13
#프론트엔드

``` JavaScript
const express = require('express'); // express 연결
const mysql = require('mysql'); // MariaDB는 mysql로 연결

// MariaDB 연결 설정
const connection = mysql.createConnection({
  host: 'localhost',
  user: 'root',
  password: '1234',
  database: 'test' 
});

app.get('/data', (req, res) => {  //데이터 가져오기
  const query = 'SELECT * FROM Chart_data'; // 실행할 쿼리 담기
  connection.query(query, (error, results) => { //쿼리 오류날 경우 오류문
    if (error) { // 쿼리 에러 날시 에러 출력
      console.error("Error executing query:", error); //콘솔로 띄워줌
      res.status(500).send("Error fetching data from database"); 
      return;
    }
    res.json(results); //값 담기
  });
});

app.use(express.static(__dirname)); // html 위치 알아서 찾기

// 서버 시작
const PORT = process.env.PORT || 3000; //포트 로컬호스트 설정
app.listen(PORT, () => { //서버 열고 콘솔 출력시 링크 띄움
  console.log(`Server is running on port ${PORT}`, `http://localhost:3000/index.html`);

});
```


