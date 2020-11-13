#### nodejs 설치
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
