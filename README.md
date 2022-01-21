![MIMI](https://user-images.githubusercontent.com/88940298/150443569-03c1dfc1-5d17-48bb-8b42-36308d964076.png)


# MIMI 
- 블록체인의 블록 채굴 개념(Pow) 학습을 위한 채굴 체험 웹페이지



##
## 4차 프로젝트 :1월 6일 ~ 1월 21일 (조기발표 1월 18일)

p.s. 현재 서버를 닫은 관계로 실행이 되지 않습니다

---   

👨‍👩‍👦‍👦Member.  MIMI 의 팀원들입니다


한경현(kyunghyun Han):[깃허브](https://github.com/kyunghyunHan).     
이성재(SeongJae Lee):[깃허브](https://github.com/seongjae-Leee).  
이성현(SeongHyun Lee):[깃허브](https://github.com/coolmarvel)

**기간** : 1월 6일 ~ 1월 21일 (조기발표 1월 18일)

**전반적인 프로젝트 진행절차**
- ~1/10 : 디렉토리 구조 나누기. 서버 빌드
- 1/11 : 기능 구현 확인(지갑 생성, 거래내역, 블록 생성, 유효성 검사)
- 1/12 : 리액트 컴포넌트 구성
- 1/13 : 리액트 컴포넌트 상태 변환
- 1/14 : DB
- 1/15 : p2p
- 1/16 : 곱창구매샵 구현
- 1/17 : 임의로 코인 구현

---------------------------------------------------------------------------------------------------------------------------------------
- 1/5 ~ 1/9  : 디렉토리 구조 설정 및 빌드 과정 최종 논의
- ~ 1/13  : server 및 지갑 생성 기능 구현
- ~ 1/15  : 블록 채굴 및 시각화
- ~ 1/16  : 부가적인 기능 추가 및 통합
- ~ 1/19  : 최종결과물 피드백 및 발표 준비




# 목차
[1.개요](#개요)

[2.목적](#목적)

- 기존 서비스와의 차별점

[3.전체 소스 코드](#전체-소스-코드-click)

[4.사용한 기술](#사용한-기술)

[5.주요 기능](#주요-기능)

[6.발생한 이슈 & 해결 방법](#발생한-이슈--해결-방법)

[7.상세 설명](#상세-설명)

 - DB 구조 (ERD)

 - 전체 흐름도
 
 - 프로젝트 설명 PPT

***

### 개요

- 블록체인~~~ 
  

### 목적

> 블록체인 

> 블록체인

- **기존 서비스와의 차별점**

   - nosql mysql 의 각각의 장점을 부각시키고 단점을 보안
   - REDUX 활용 AUTH 진행
   - 커플 연결 서비스 진행 (관계쿼리)
   

### 👬 전체 소스 코드 [클라이언트](https://github.com/MiMigibletss/MIMI/tree/main/src)  or [서버](https://github.com/MiMigibletss/MIMI/tree/main/server1)


### 🛠 사용한 기술

- 웹 화면 구성 : `REACT` 
- DB 액션 처리 : `Sequelize` `mongoose`
- DBMS : `MySQL`
- 개발 Tool :`PostMan` `Visual Studio Code``github`
- AWS 배포 : `RDS`
- 로그인 구현 : `UBUNTU`
- 프레임워크 : `NodeJs` `REACT`
- 프로젝트 관리 Tool : `Google Drive` `GitHub` `notion`

### 🔎  깃 브랜치 활용

코드 병합시 오류를 최소화 하기위해 깃브런치 


✔ main - 개발 완료하고 최종 코드 올리는 브랜치


# 🔥발생한 이슈 & 해결 방법

### "CORS 정책에 의한 에러"

[상황]  
![콜스 에러](https://user-images.githubusercontent.com/90792916/143545407-1d5a53ca-7a6b-442d-94d9-72ea41138cdf.png)  

[문제] 

서버는 포트가 5000 번이고,

클라이언트는 포트가 3000 번으로 다른데 서로 주고 받으려고 하면,

CORS 정책에 의해 막혀버린다.

[해결] 

npm i http-proxy-middleware 모듈을 설치하고
```
const { createProxyMiddleware } = require('http-proxy-middleware');

module.exports = function(app) {
  app.use(
    '/api',
    createProxyMiddleware({
      target: 'http://localhost:5000',  //  노드 서버가 5000 번이므로 target 도 같게한다.
      changeOrigin: true,
    })
  );
};
```
프록시 서버를 이용하여 에러를 해결했다.

### "Auth로 2가지 DB(MongoDB와 MySqlDB) 모두 사용할 수 있는 방법을 고민"

[상황] 2 가지(MongoDB와 MySqlDB) DB를 동시에 사용하기 때문에,  2 가지 DB를 충돌없이 사용할 수 있는 방안

[문제] 

SNS(MySqlDB)로 로그인 하여도 커플상점(MongoDB)를 이용할 수 있도록 하여야 함.
일부 공통된 DB가 필요한 상황이 발생하여, 2 가지 DB의 충돌없이 사용할 수 있도록 고민.

[해결] 

Auth.js에서 if문을 사용하여 MySql와 Monggo 이용에 조건을 부여함.

![KakaoTalk_20211125_153528603](https://user-images.githubusercontent.com/88923210/143395201-9da11fc9-96a8-4dcc-a0ba-da667f3eaf1d.png)



### "env파일의 중요성 "


[상황] gitignore에 올라가 있는 env파일이 없어 DB접속 불가

[문제] 

GitHub사용할 때 Git branch 전환 시에 
gitignore에 올라가 있는 env파일이 없어 DB접속 불가

![KakaoTalk_20211125_153121946](https://user-images.githubusercontent.com/88923210/143392535-7d0b32c1-0d26-448c-8a4d-250c18c8e8b8.png)

[해결] 

env파일의 존재를 인지하고 env파일을 추가하여 DB접속 성공.  
  
    
      
      

### "Redux 관련 auth 충돌문제 "


[상황] MusicPlayer 및 auth에러발생 

[문제] 

auth 와 musicplyer간 충돌로 인한 음악 재생 및 로그인 에러발생



[해결] 

음악재생을 유튜브 url로 변경하여 충돌방지
  
    
      






### "property "


[상황] gitignore에 올라가 있는 env파일이 없어 DB접속 불가

[문제]   
<img width="693" alt="KakaoTalk_20211125_124522181" src="https://user-images.githubusercontent.com/88940298/143390995-430a4520-9e35-4f19-9698-ffc1ec7dce0c.png">  


[해결] 

```
{Products.length === 0 ? (
            <div className="no_item">
              <h2>등록된 아이템이 없읍니다</h2>
            </div>
          ) : (
            <div className="shop-main-content-item_list">{renderCards}</div>
          )}
```
상품이 없을 경우를 추가했다





### "React 렌더링중 에러발생 "

[상황] React 렌더링중 에러발생 

[문제] 

![KakaoTalk_20211125_124542194](https://user-images.githubusercontent.com/88940298/143390699-22493ae8-1850-44a4-88ed-9ecf51093222.png)

[해결] 
```
  const userInfo = useSelector(state => state.user);
  const [User, setUser] = useState({});
  
  useEffect(() => {
    if (userInfo) {
      if (userInfo.userData) {
        setUser(userInfo.userData);
        if (userInfo.userData.couple_code) {
          setCoupleCode(userInfo.userData.couple_code);
        }
      }
    }
  }, [userInfo.userData]);
```

useEffect 를 사용하여 유저정보를 state담아 문제를 




### "React 배포에서의 문제점 파악 ,db및 구조설계 "

[상황] 배포도중 에러발생 

[문제] 
```
Error: error:0308010C:digital envelope routines::unsupported
    at new Hash (node:internal/crypto/hash:67:19)
    at Object.createHash (node:crypto:130:10)
    at module.exports (/Users/user/Programming Documents/WebServer/untitled/node_modules/webpack/lib/util/createHash.js:135:53)
    at NormalModule._initBuildHash (/Users/user/Programming Documents/WebServer/untitled/node_modules/webpack/lib/NormalModule.js:417:16)
    at handleParseError (/Users/user/Programming Documents/WebServer/untitled/node_modules/webpack/lib/NormalModule.js:471:10)
    at /Users/user/Programming Documents/WebServer/untitled/node_modules/webpack/lib/NormalModule.js:503:5
    at /Users/user/Programming Documents/WebServer/untitled/node_modules/webpack/lib/NormalModule.js:358:12
    at /Users/user/Programming Documents/WebServer/untitled/node_modules/loader-runner/lib/LoaderRunner.js:373:3
    at iterateNormalLoaders (/Users/user/Programming Documents/WebServer/untitled/node_modules/loader-runner/lib/LoaderRunner.js:214:10)
    at iterateNormalLoaders (/Users/user/Programming Documents/WebServer/untitled/node_modules/loader-runner/lib/LoaderRunner.js:221:10)
/Users/user/Programming Documents/WebServer/untitled/node_modules/react-scripts/scripts/start.js:19
  throw err;
  ^
```

react 배포 중 에러발생. 이는 nodejs 버전이 높아서 생기는 문제다.

[해결] export 옵션 
```
export NODE_OPTIONS=--openssl-legacy-provider 
```
사용하여 문제해결

또는 pakage json 에서 

```
// 변경 전
"start": "react-scripts start"

// 변경 후
"start": "react-scripts --openssl-legacy-provider start"
```

각 관계에 맞게 관계쿼리 생성 
image의 경우 sns 및 사진첩 에서 동시에 사용하기 때문에 관계를 엮어 사용



### 프로젝트 기획안
[구글 기확안/회의록 파일](https://drive.google.com/drive/folders/16mA6-jiUT15Sxzz4jaZQ-ap9a9bkzwb2)   



