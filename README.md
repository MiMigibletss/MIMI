![143427874-c9a2c28d-789d-4af2-ab4e-0aece9a16349-removebg-preview](https://user-images.githubusercontent.com/88923210/143464419-fc7cb9e8-bb30-40b1-ba0d-c5d776866ada.png)

# 👨‍❤️‍💋‍👨'Play & Love to Happy in PL2H World!' 
- 사랑하는 연인과의 행복을 PL2H World에서 마음껏 즐겨보세요!
- 싸이월드 감성이 여러분의 추억을 더욱 아름답게 해 줄 것입니다.
- 연인을 위한 선물을 구매하고 싶으신가요? 저희가 오픈한 상점으로 구경오세요!
- 앗! 솔로시라구요? 괜찮습니다~ 저희 상점은 누구에게나 열려있답니다~


##
## 3차 프로젝트 :2021-11-05 ~ 2021-11-22

## 👜👢🧢[**서비스로 이동**](http://13.124.13.37:3000/)



p.s. 현재 서버를 닫은 관계로 실행이 되지 않습니다

![KakaoTalk_Image_2021-11-24-16-41-43](https://user-images.githubusercontent.com/88940298/143195627-412b8a3c-a61c-4842-b135-564b50293f44.gif)


---   

👨‍👩‍👦‍👦Member.  Pl2h의 팀원들입니다

![화면 캡처 2021-11-25 194708](https://user-images.githubusercontent.com/88940298/143427874-c9a2c28d-789d-4af2-ab4e-0aece9a16349.png)

한경현(kyunghyun Han):[깃허브](https://github.com/kyunghyunHan)SNS Frontend     
이민주(Minjoo Lee):[깃허브](https://github.com/codecocos)SNS Backend      
이상민(ssangMin Lee):[깃허브](https://github.com/LeessangMin)Shop Frontend   
박준혁(jun hyuk Park):[깃허브](https://github.com/berrypjh)Shop Backend  

**기간** :  2021-11-05 ~ 2021-11-22

**전반적인 프로젝트 진행절차**
1. 프로젝트 파트별로 진행(커플상점 부분과 SNS부분)
2. 오프라인 위주의 팀 작업
3. 오프라인이 불가능할 경우 온라인으로 팀 작업을 진행하며 서로의 코드 상황 브리핑 및 회의
4. 각 파트별 진행 상황을 수시로 공유 - 개발 중 예상치 못한 이슈가 있는지, 다른 파트의 지원이 필요한 부분은 없는지

---------------------------------------------------------------------------------------------------------------------------------------

**1주차** 
>-1일차 : 서로의 프로젝트 아이디어 공유 및 정리
>
>-2일차 : 아이디어 세부사항 및 db관계쿼리 정리
>
>-3일차 부터 프로젝트 진행

**2주차** 
-프로젝트 파트별 진행, 중간 에러확인, 파트별 진행률을 확인하면서 앞으로의 진행일정 조율.

**3주차**
-프로젝트 파트별 마무리 및 배포진행

**배포 후**
>
3주간 진행하였던 프로젝트의 결과물에 대해 좋았던 점과  개선해야 할 점을 생각하고 공유합니다. 
각자 맡은 부분에 대해 설명하며, 그 외에도 서비스의 가치나 방향성에 대한 의견을 주고 받으며 서로의 생각을 나누었습니다.
지난 프로젝트의 진행과정을 기록으로 남기며 정리합니다.


![KakaoTalk_20211125_195813474](https://user-images.githubusercontent.com/88940298/143429808-f5a10b4d-f7c0-4945-953a-e2b069671d21.png)




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

최근 싸이월드 출시소식관련 하여, 싸이월드 감성과 네이버 커플페이지를 접목시키고, 더불어 SNS를 이용하는 커플들을 대상으로 아이템들을 판매하는 상점를 통한 복합서비스를 구상해보았습니다.

커플상점과 SNS에서 사용하는 DB를 MongoDB와 MySql로 분류하여 더욱더 많은 공부가 될 수 있게 하였고,
  
  관련자료  

네이버 커플페이지 [관련자료](https://blog.naver.com/PostList.naver?blogId=sum-lab&categoryNo=51&parentCategoryNo=51&skinType=&skinId=&from=menu&userSelectMenu=true)  
싸이월드 [관련자료](https://newsis.com/view/?id=NISX20211123_0001661075&cID=13001&pID=13000)

위의 자료들을 바탕으로 감성과 기능이 함께하는 서비스를 제공하고자 노력했습니다.

### 목적

> 커플 전용 SNS 및 SHOP 활성화
> 1. 커플 기능 구현활용 SNS 활성화
> 2. RDS(Mysql),Atlas(MongoDB) 동시 활용 프로젝트 활용
> 3. 결제서비스 구현 숙달
> 4. sns 페이지 구성
> 5. 배포 서비스 구현 공부 (ec2,s3,nginx)

- **기존 서비스와의 차별점**

   - nosql mysql 의 각각의 장점을 부각시키고 단점을 보안
   - REDUX 활용 AUTH 진행
   - 커플 연결 서비스 진행 (관계쿼리)
   

### 👬 전체 소스 코드 [클라이언트](https://github.com/pl2hteam/pl2hproject/tree/main/client)  or [서버](https://github.com/pl2hteam/pl2hproject/tree/main/server)


### 🛠 사용한 기술

![KakaoTalk_20211125_174239334](https://user-images.githubusercontent.com/88940298/143418476-feff562d-e665-4d09-a100-0e0dccb38f3b.png)



- 웹 화면 구성 : `REACT` 
- DB 액션 처리 : `Sequelize` `mongoose`
- DBMS : `MySQL` `Mongo` 
- 개발 Tool :`PostMan` `Visual Studio Code``github`
- AWS 배포 : `EC2` `RDS` `Atlas`
- 로그인 구현 :  `REDUX`
- 프레임워크 : `NodeJs` `REACT`
- 결제: `PAY PAL`
- 프로젝트 관리 Tool : `Google Drive` `GitHub` `notion`
- 사용 모듈(Client) : `
- "@material-ui/core": "^4.12.3",  
    "@material-ui/icons": "^4.11.2",  
    "@material-ui/lab": "^4.0.0-alpha.60",  
    "@mui/icons-material": "^5.1.0",  
    "@mui/styles": "^5.1.0",  
    "antd": "^3.26.20",  
    "axios": "^0.19.2",  
    "axios-mock-adapter": "^1.20.0",  
    "bootstrap": "^5.1.3",  
    "components": "^0.1.0",  
    "core-js": "^3.6.4",    
    "d3": "^7.1.1",   
    "formik": "^1.5.8",    
    "html-react-parser": "^1.4.0",    
    "postcss-loader": "^6.2.0",    
    "react": "^16.8.6",    
    "react-app-polyfill": "^1.0.6",  
    "react-carousel-minimal": "^1.4.1",  
    "react-copy-to-clipboard": "^5.0.4",  
    "react-dom": "^16.8.6", 
    "react-dropzone": "^11.4.2",  
    "react-elastic-carousel": "^0.11.5",  
    "react-flip-move": "^3.0.4",  
    "react-hook-form": "^7.19.0",  
    "react-icons": "^3.7.0",  
    "react-image-gallery": "^1.2.7",  
    "react-image-shadow": "^1.1.3",  
    "react-infinite-scroll-component": "^6.1.0", 
    "react-instagram-zoom-slider": "^1.4.0",  
    "react-material-ui-carousel": "^3.0.4",  
    "react-moment": "^1.1.1",  
    "react-paypal-express-checkout": "^1.0.5",  
    "react-redux": "^7.1.0-rc.1",  
    "react-responsive-carousel": "^3.2.22",  
    "react-router-dom": "^5.0.1",  
    "react-scripts": "3.4.1",  
    "react-show-more-text": "^1.5.0",  
    "react-slick": "^0.28.1",  
    "react-spring": "^9.3.0",  
    "react-swift-slider": "^7.0.1",  
    "react-use-gesture": "^9.1.3",  
    "redux": "^4.0.0",  
    "redux-promise": "^0.6.0", 
    "redux-thunk": "^2.3.0",  
    "styled-reset": "^4.3.4",  
    "webpack": "^4.42.0",  
    "yarn": "^1.22.17",  
    "yup": "^0.27.0"  

-  사용 모듈(Server) :`  
  - "async": "^3.2.2",      
    "bcrypt": "^5.0.1",      
    "body-parser": "^1.18.3",      
    "cookie-parser": "^1.4.5",      
    "cors": "^2.8.5",      
    "debug": "^4.1.1",      
    "dotenv": "^10.0.0",      
    "express": "^4.17.1",      
    "express-session": "^1.17.2",      
    "fluent-ffmpeg": "^2.1.2",      
    "jsonwebtoken": "^8.5.1",      
    "mongoose": "^5.4.20",      
    "morgan": "^1.10.0",      
    "multer": "^1.4.3",      
    "mysql2": "^2.3.3",      
    "passport": "^0.5.0",      
    "passport-local": "^1.0.0",      
    "promise": "^8.1.0",      
    "sequelize": "^6.9.0",      
    "sequelize-cli": "^6.3.0"  
    ` 

### 🌱주요 기능

- 로그인 : 일반 로그인, `Sequelize` `passport` `mysql` `REDUX` 
- 회원가입 : `Sequelize` `passport` `mysql` `mongo` `mongoose` `REDUX`
- 회원정보변경 :`Sequelize` `mysql` `mongo` `mongoose`
- 장바구니 : `Sequelize` `mysql` `mongo` `mongoose`
- 결제 : `Sequelize` `passport` `PAYTAL` `mongo` `mongoose`
- 마이페이지 : `Sequelize` `mysql` `RDS`
- SNS:`Sequelize` `mysql` `RDS`
- 놀거리 :`Sequelize` `mysql` `RDS`
- 편지:`Sequelize` `mysql` `RDS`
- 놀거리 :`Sequelize` `mysql` `RDS`
- MUSIC PLAYER :`styled-componets`
- 관리자모드(상품등록 및 삭제) :`mongo` `mongoose`
- 물품 필터 (검색): `mongo` `mongoose` 
- 모달:`Sequelize` `mysql` `RDS`



### 🔎  깃 브런치 활용

코드 병합시 오류를 최소화 하기위해 깃브런치 

```
✔ main - 개발 완료하고 최종 코드 올리는 브랜치


✔ SNS  sns 파트 깃브런치


   - diaryhyun (sns 파트 프론트 브런치)
   
   - diarymin (sns 파트 깃 브런치)
   
✔ SHOP  shop 파트 깃브런치


   - ssangmin (shop 파트 프론트 브런치)
   
   - parkjh (shop 파트 깃 브런치)

  

```

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



### DB구조 
![KakaoTalk_20211125_114838306](https://user-images.githubusercontent.com/88940298/143371203-28d2aa41-7894-442c-a505-594b6f10506c.png)


각 관계에 맞게 관계쿼리 생성 
image의 경우 sns 및 사진첩 에서 동시에 사용하기 때문에 관계를 엮어 사용



### 프로젝트 기획안 PPT
[구글 프레젠테이션 파일](https://docs.google.com/presentation/d/13yVkx7W7bpqiPpieAJCAUgyme5Hsj_4gum353ISTyi4/edit#slide=id.p)   
[구글 프리젠테이션 파일 기획안 2](https://drive.google.com/file/d/17_Bz_mce2lQwyWdOZ9gFvuxifBwlwVXD/view?usp=sharing)



