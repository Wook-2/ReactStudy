#### nodejs 설치 
우선 나는 .. `$ sudo apt-get install nodejs`명령어에서 패키지 에러가 발생하여 이 방법으로는 설치를 하지 못하였고, 바이너리 파일을 다운받아 압축을 푸는 방법으로 설치를 하였다.
##### linux-x64
- nodejs 공식 홈페이지에서 linux64 바이너리파일 다운로드.
- 압축파일을 풀 폴더 생성
	`$ sudo mkdir -p /usr/local/lib/nodejs`
	
- 환경 변수 설정
	`$ vi ~/.profile` 로 .profile을 열고 가장 하단에 아래 코드 추가하자.
	```
	VERSION = v14.10.0  # 다운받은 파일의 버전을 입력하면됨.
	DISTRO = linux-x64
	export PATH=/usr/local/lib/nodejs/node-$VERSION-$DISTRO/bin:$PATH
	```
- ./profile 새로고침
	`. ~/.profile`
- 설치가 완료되었다. 아래 명령어로 설치가 제대로 되었는지 확인해보자
	`$ node -v`
	`$ npm version`
	`$ npx -v`
	아래와 같은 형식으로 출력되면 제대로 설치된 것!
	```
	➜  node -v
	v14.10.0
	➜  npm version
	{ npm: '6.4.1',
	ares: '1.15.0',
	cldr: '33.1',
	http_parser: '2.8.0',
	icu: '62.1',
	modules: '64',
	napi: '3',
	nghttp2: '1.34.0',
	node: '10.15.1',
	openssl: '1.1.0j',
	tz: '2018e',
	unicode: '11.0',
	uv: '1.23.2',
	v8: '6.8.275.32-node.12',
	zlib: '1.2.11' }
	➜ npx -v
	6.14.8
	```

#### React!
##### 위 설치를 제대로 수행했다는 가정 하에 
1. 프로젝트 폴더로 이동
2. `$ npx create-react-app { app_name }` 명령어를 실행하면 app_name이라는 폴더명을 가진 react 개발을 할 수 있는 폴더(환경)가 생성된다. **wow**<br>


### prop-types
#### 전달하는 props값이 올바른지 확인해주는 패키지(?)
- Install
	- `npm i prop-types` 
- Usage
	Component.js<br>
	``` javascript
	import Proptypes from "prop-types";
	
	Component.proptypes = {
		prop : Proptypes.string.isRequired
	}
	```
	와 같은식으로 사용 하여 전달하려는 값의 타입, 조건 등을 console창에서 체크할 수 있다.


