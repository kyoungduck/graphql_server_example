
# GraphQL User+Post

## 개요

Node.js로 구현된 유저 추가,수정,삭제 기능과 유저별로 간단한 글을 적을 수 있는 GraphQL API를 구현한 프로젝트입니다. 유저 인증은 구현되어 있지 않으나 유저 아이디로 글을 적을 수 있으며 유저끼리 친구추가를 하여 관계를 설정할 수 있습니다.

## 목적

이 프로젝트는 GraphQL API로 CRUD를 만들고 그것의 성능을 테스트 하는것에 목적이 있습니다.

## 요구사항

- Node.js(es8+)
- MongoDB
- yarn 또는 npm의 의존성 패키지


### 환경설정
|        Name          |       Description     |        Default       |
| -------------------- | :-------------------: | :------------------: |
|      MONGO_URI       |       MongoDB URI     | mongodb://localhost/ |
|      MONGO_DB        |      MongoDB Path     |         test         |
|      MONGO_DB        | GraphQL Endpoint Path |       /graphql       |
|      MONGO_DB        |       Server Port     |         3000         |

환경설정으로는 .env 파일을 만들어 위의 표와 같이 설정할 수 있습니다.

## 사용법

의존성 패키지 설치

```bash
$ yarn install
```

빌드 및 실행

```bash
$ yarn build
$ yarn start
```

## GraphQL API

### 유저 관련 스키마

|        Name          |      Schema Type      |
| -------------------- | :-------------------: |
|     user             |          QUERY        |
|     userList         |          QUERY        |
|   searchUserByEmail  |          QUERY        |
|     createUser       |         MUTAION       |
|     deleteUser       |         MUTAION       |
|     updateUser       |         MUTAION       |
|     addFriend        |         MUTAION       |
|     deleteFriend     |         MUTAION       |

### 게시글 관련 스키마

|        Name          |      Schema Type      |
| -------------------- | :-------------------: |
|     post             |          QUERY        |
|     postList         |          QUERY        |
|     createPost       |         MUTAION       |
|     deletePost       |         MUTAION       |
|     updatePost       |         MUTAION       |
