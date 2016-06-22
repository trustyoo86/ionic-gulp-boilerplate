Ionic Demo
=====================

## 개요

ionic 개발을 위해서 www 폴더 내에서 직접 개발이 아닌, public folder에서 개발 후, build만 www 폴더에서 하도록 변경한 데모입니다.

## 주의점

현재 모든 개발 소스는 public 폴더에서 관리하고 있습니다. 기타 라이브러리는 bower로 설치하되, bower_components에서 소스를 불러오고, 이를 vender.js라는 파일로 빌드해서 사용하기 때문에, www폴더를 바라보고 있지 않습니다. (ionic도 포함입니다.)

## 사용법

### 1) gulp task 실행

개발 후에, public 폴더에서 www 폴더로 빌드하기 위해서, 다음과 같은 커맨드를 실행합니다.

#### 1.1) 개발 모드
개발모드에서는 각각의 file들을 watch 상태로 확인하게 됩니다. 확인해서 변경되는 파일은 www 폴더로 build합니다.


`
$gulp dev
`

#### 1.2) 배포 모드
배포모드에서는 따로 파일 변경을 감지하지 않으며, 각각의 파일에 대한 minify를 실행합니다.

`
$gulp prod
`

### 2) 실행

#### 2.1) browser에서 test 모드로 실행

브라우저에서 테스트모드로 실행합니다. (개발 중일 경우입니다.)

`
$ionic serve
`