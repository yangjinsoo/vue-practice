# practice-vue
- Vue.js 학습용 프로젝트

## Project setup
```
npm install -g @vue/cli
vue.cmd create 프로젝트명
```
- 노드 설치 (npm이용하기 위함)
- vue 설치
- vue create로 프로젝트 생성
    - 보안 오류 뜨면 vue.cmd create

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Lints and fixes files
```
npm run lint
```

### 메모장
```vue
v-for="arr in arrs" :key="arr"
v-for="(arr, i) in arrs" :key="i"
```
- v-for을 사용할 때는 :key가 꼭 필요
- (arr, i)를 통해 python의 enumerate처럼 인덱스도 함께 받아올 수 있음.
***
- 동적 UI 만드는 순서
    - UI를 미리 만들어놓음.
    - UI의 상태를 데이터로 저장해놓음.
    - UI의 상태 변화에 따라 UI가 어떻게 보일지 작성.

- html태그 사이에 데이터 사용하려면 {{데이터}}
- html태그 속성에 데이터 사용하려면 :속성명="데이터"

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).