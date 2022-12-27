# React Native?

react + react native 조합으로 react native 기반의 ios, android용 모바일 앱을 구축할 수 있다.

react + react-dom을 통해 웹앱을 구현하지만 react 라이브러리 자체는 플랫폼에 구애받지 않음. -> React는 상태를 관리하고 가상의 컴포넌트 트리를 구축하는 툴일 뿐

쉽게 말해 react native는 react-dom의 대안, react native에 내장된 컴포넌트들은 ios, android 플랫폼을 위해 네이티브 UI 요소로 컴파일된다.

결국 react native는 react-dom과 비슷하지만 플랫폼 대상이 웹브라우저가 아닌 ios와 android이며 해당 플랫폼과 상호 작용하고 플랫폼을 위한 앱을 구축하기 위한 모든 컴포넌트와 API를 제공.

## React Native의 내부 살펴보기

react native에서는 내장된 `<TextInput>` 컴포넌트(react-dom에서는 `<input>`) 를 통해 Android를 위해 EditText나 ios를 위해 UITextField로 컴파일한다.

즉, react native는 재사용 가능한 컴포넌트를 매핑하고 컴파일한다.
이때 UI elements가 아닌 JS 로직은 컴파일되지 않고 구축한 네이티브 앱 안에서 react native가 호스트한대로 JS 스레드에서 실행된다. -> react native는 간단한 JS 프로세스를 구축하고 있는 네이티브 앱의 일부로 만들어 자동으로 프로세스를 관리하고 네이티브 플랫폼과 상호작용할 수 있도록 한다. (JS가 구축한 네이티브 앱 안에서 그대로 실행하면서 react native를 통해 언어의 장벽을 넘어 android 혹은 ios 플랫폼과 상호작용한다.)

## 개발환경설정

### Expo CLI vs React Native CLI

- Expo CLI가 기본값 (CLI란 Command Line Interface: 명령 행 인터페이스)
- 두 가지 툴 모두 React Native 프로젝트를 생성하고 테스팅 기기 및 시뮬레이터에 React Native 앱을 실행할 뿐만 아니라 React Native 앱을 구축하는데 사용되어 앱스토어에 앱을 배포할수 있도록 한다.
- Expo CLI와 Expo가 제공하는 몇 가지 툴을 이용해 네이티브 앱을 작성하면 Expo없이 React native CLI만 사용하는 것 보다 훨씬 편리하고 과정이 수월해지기 때무에 Expo 사용을 추천 (사용하다 언제든 중지 가능)
- React Native CLI는 Expo가 생기기전에 존재했으며 기초적인 React native 개발 설정 제공. 하지만 추가적인 구성 및 설정을 직접 해야하며 편리한 기능도 적고 카메라 등 특정 네이티브 기기 기능을 활용하기가 Expo보다 작업이 번거로움, 하지만 Java, swfit, kotlin 과 같은 네이티브 소스 코드와 통합하기가 비교적 쉽다는 장점이 있음. (하지만 애초에 React Native를 사용하는 이유가 이 과정을 생략하기 위함이라 큰 장점이라 볼 순 없음)
