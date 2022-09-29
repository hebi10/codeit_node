### 사이트 만들기
// http 서버 api 모듈 생성
const http = require('http');

// 서버 통신 응답 하겠다. 요청이 오면 응답으로 보낼 코드(response), 요청을 다루는 코드(request)
let server = http.createServer(function(request, response){
  response.end('<h1>Hello, World</h1>');
});

// 3000번 포트로 통신한다
server.listen(3000); 

// 사이트 확인하는 방법
127.0.0.1:3000 // 내 컴퓨터의 3000번 포트를 사용하여 통신한다.

### express 다운
// 서드파티 모듈 - 내장된 모듈이 아닌 다운 받는 모듈
// 가장 많이 사용한다 알려짐

### express 사용
app.get('/', (request, response) => {
  response.end("<h1>Welcome!</h1>");
});

app.get('/users', (request, response) => {
  response.end(`<h1>${users}</h1>`);
});

app.get('/users/:id', (request, response) => {
  const userName = users[request.params.id - 1];
  response.end(`<h1>${userName}</h1>`);
});

app.get('*', (request, response) => {
  response.end("<h1>Page Not Available</h1>");
});

app.listen(3000);

### nodemon 설치
// npm install -g nodemon
// 변화를 자동으로 감지하고 변화시켜줌