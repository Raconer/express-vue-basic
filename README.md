# Vue.js & Node Express 프로젝트 생성

## 참고

[Vue & Express 참고 블로그](https://velog.io/@choco_sister/Vue-3-Vue-CLI-Vuex-VueRouter-Axios-JWT-%EB%A1%9C%EA%B7%B8%EC%9D%B8%ED%9A%8C%EC%9B%90%EA%B0%80%EC%9E%85-%EA%B8%B0%EB%8A%A5-%EA%B5%AC%ED%98%84-1-BackendAPI%EC%84%9C%EB%B2%84-%EC%83%9D%EC%84%B1 "choco_sister")

## 프로젝트 구성

* Backend
* Frontend

## 프로젝트 생성 순서

### 1. Node Express 프로젝트 생성

1. Node Express 설치
    * > npm install express-generator -g
2. Node Express 프로젝트 생성
    * > express --view=pug backend
    * 'backend' : 프로젝트 이름
3. Node Express 폴더 이동
    * > cd backend
4. Node Express package.json 생성
    * > npm init
5. Node Express 서버 실행
    * > npm start
* 만약 "Error: Cannot find module 'http-errors'" 에러 시
    * > npm install

### 2. Vue-CLI 프로젝트 생성

1. Vue-cli 설치
    * > npm install -g @vue/cli
2. 버전 확인
    * > vue --version
3. 프로젝트 생성
    * > vue create frontend
    * 'frontend' : 프로젝트 이름
    * 현재 Default(Vue3) 선택 후 설치
4. 프로젝트 이동
    * > cd frontend
5. 프로젝트 실행
    * > npm run serve

## 통신 테스트

1. BackEnd 수정
    1. backend > routes > index.js 수정
2. Frontend 수정
    1. backend > frontend > src > components > HelloWorld.vue 수정

## GiT Push

Vue.js 설치시 Git File이 생성 되므로 현재와 같이 모듈로서 Vue.js를 사용할 경우 Vue.js에서 Git 숨긴 파일을 삭제 하면 된다. 