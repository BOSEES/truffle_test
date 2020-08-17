# 트러플 공식문서로 연습해보기
## 트러플의 개요
Ethereum Virtual Machine (EVM)을 사용하는 블록 체인을위한 세계적 수준의 개발 환경, 테스트 프레임 워크 및 자산 파이프 라인은 개발자로서의 삶을보다 쉽게 ​​만드는 것을 목표로합니다. Truffle을 사용하면 다음을 얻을 수 있습니다.
  - 내장 된 스마트 계약 컴파일, 연결 , 배포 및 바이너리 관리
  - 신속한 개발을 위한 자동화된 계약 테스트
  - 스크립트 가능하고 확장 가능한 배포 및 마이그레이션 프레임워크이다.
  - 임의의 수의 공용 및 사설 네트워크에 배포하기 위한 네트워크 관리
  - ERC190 표준을 사용하여 EthPM 및 NPM으로 패키지 관리.
  - 직접적인 계약 커뮤니케이션을 위한 대화 형 콘솔.
  - 긴밀한 통홥을 지원하는 구성 가능한 빌드 파이프 라인
  - 트러플 환견에서 스크립트를 실행하는 외부 스크립트 실행기

## 트러플 구축 환경 설정
  - NodeJS v8.9.4 이상
  - Windows, linux, Mac OS

## 프로젝트 시작하기
### 트러플 프로젝트를 위한 새 디렉토리를 만들자.(항상 비어있어야 함. 그러지않으면 truffle init && truffle unbox 를 사용할수 없다.)
    mkdir MetaCoin
    cd MetaCoin
### 메타코인 예제(상자) 다운로드
    truffle unbox metacoin
## 트러플 예제 디렉토리구조
### contract/: 솔리디티 컨트렉트 디렉토리
### migrations/: 스크립트 가능한 배포 파일 용 디렉토리
### test/: 애플리케이션 미 계약 테스트를 위한 테스트 파일용 디렉토리
### truffle-config.js: 트러플 구성파일 (중요!!!)

## 스마트컨트렉트 컴파일
    truffle compile
### 후속 실행시 트러플을 마지막 컴파일 이후 변경된 계약만 컴파일한다.이 동작을 재 정의 하려면
    truffle comppile --all
### 컴파일 된 아티팩트는 build/contracts/ 디렉토리를 생성하고 배치된다. 이러한 아티팩트는 트러플의 내부 작업에 필수적이며 응용 프로그램을 성공적으로 배포하는데 중요한 역할을 한다. 이러한 파일은 계약 컴파일 및 배포에 의해 덮어 쓰기 때문에 편집을해서는 절대 절대 안된다.

## 마이그레이션 실행하기
### 마이그레이션은 이더리움 네트워크에 계약을 배포하는데 도움이 되는 javaScript 파일이다. 이러한 파일은 배포작업 준비를 담당하며 배포 요구사항이 시간이 지남에 따라 변경된다는 가정하에 작성 된다. 단순히 말해서 마이그레이션은 단순히 관리되는 배포 스크립트의 집합이다.
    truffle migrate
### 만약 새 마이그레이션을 실행 할 경우
    truffle migrate --reset

# NPM 을 통한 패키지 관리 (이번 프로젝트에서 클레이튼을 과 함께 사용하게될 방법)
### 트러플로 생성된 프로젝트는 기본적으로 패키지로 사용할 수 있는 특정 레이아웃이 있다. 이 레이아웃은 필수는 아니지만 일반적인 규칙 또는 "사실상 표준" 으로 사용하면 NPM을 통한 계약 및 dapp 배포가 훨씬 쉽다

### 트러플 패키지에서 가장 중요한 디렉토리는 다음과 같다.
  - /contracts
  - /build (/build/contrats 트러플로 컴파일한거 포함)

## 설치 방법
    cd my_project
    npm install example-truffle-library

# 트러플 명령어 모음

  - truffle build
  - truffle compile [--list <filter>] [--all] [--network <name>] [--quiet]
  - truffle config [--enable-analytics|--disable-analytics] [[<get|set> <key>]      [<value-for-set>]]
  - truffle console [--network <name>] [--verbose-rpc]
  - truffle create <artifact_type> <ArtifactName>
  - truffle debug [<transaction_hash>] [--network <network>] [--fetch-external]
  - truffle develop [--log]
  - truffle exec <script.js> [--network <name>] [--compile]
  - truffle init [--force]
  - truffle install <package_name>[@<version>]
  - truffle migrate [--reset] [--f <number>] [--to <number>] [--network <name>] [--compile-all] [--verbose-rpc] [--dry-run] [--interactive] [--skip-dry-run] [--describe-json]
  - truffle networks [--clean]
  - truffle obtain [--solc <version>]
  - truffle opcode <contract_name>
  - truffle publish
  - truffle run <command>
  - truffle test [<test_file>] [--compile-all[-debug]] [--network <name>] [--verbose-rpc] [--show-events] [--debug] [--debug-global <identifier>] [--bail] [--stacktrace[-extra]]
  - truffle unbox <box_name> [<destination_path>] [--force]
  - truffle version
  - truffle watch

