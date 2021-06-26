## Rest API? (Application Programming Interface)

- HTTP 요청을 보낼때 어떤 URI에 어떤 메소드를 사용할지 개발자들 사이에 널리 지켜지는 약속, 형식

- HTTP method : GET, Post, PUT, DELETE

## GraphQL

### 이점

1. 필요한 정보들만 선택하여 볃아 올 수 있음, overfetching(쓸모없는 정보들) 문제 해결, 데이터 전송량 감소
2. 여러 계층의 정보들을 한번에 받아올 수 있음, Underfetcing(서버로 많은 request 보냄) 문제 해결, 요청(request) 횟수 감소
3. 하나의 endpoint에서 모든 요청을 처리함. 하나의 URI에서 POST로 모든 요청가능

### 구조

query : 데이터 정보를 받아올때 사용

```graphql
query {
  team {
    id
    manager
  }
}
```

mutation : 데이터를 추가, 수정, 삭제 할때 사용한다.

```graphql
mutation{

}
```

### resolver

query는 DB에서 문제 같은 것이고, 이것을 해결 하기 위한 것이 resolve.

## Apollo

- GraphQL을 구현할 솔루션, GraphQL은 명세, 형식임
- 백엔드에서 정보를 제공 및 처리
- 프론트엔드에서 요청 전송
- GraphQL.js, GraphQL Yoga, AWS Amplify, Relay등의 서비스가 있다.

- 백엔드와 프론트엔드 모두 제공
- 간편하고 쉬운 설정과 풍성한 기능등을 제공
- Apollo Server는 백엔드 서버 제작할때 사용
- Apollo Client와 React를 이용하여 프론트 엔드 웹제작 가능
