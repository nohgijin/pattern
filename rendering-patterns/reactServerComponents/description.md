## React Server Components
### 개요
- React개발팀에서는 zero bundle size를 통해 모던 UX를 구현하는데 초점이 맞춰져 있으며, 번들 사이즈를 작게 만들 수 있음
### 서버사이드 렌더링의 제약사항
- Javascript는 서버에서 HTML문자열로 렌더링이 되지만, 수화 단계를 거치므로 Javascript를 다시 가져와야 함
- 서버사이드 렌더링은 최초 페이지 로드 이후에는 추가적으로 사용되지 않음
- 인터렉션을 하는 경우에는 어쩔수없이 client측으로 코드를 보내야 함
- React Server Component 를 사용 시 컴포넌트를 정기적으로 받아올 수 있고, 새로운 데이터가 있을 때 서버에서 앱의 컴포넌트를 리렌더링해줌
### 서버 컴포넌트
- 추상화된 포멧에 렌더링 데이터를 포함하여 내려받는 방법으로 자바스크립트를 추가로 받지 않으므로 서버 사이드 렌더링을 보완
- SSR을 대체하지는 않음
### 자동 코드 스플리팅
- client component에서는 lazy 를 써야하고, 지연이 있어 UX에 영향을 미칠 수 있음
- server component에서는 일반 import 문을 사용할 수 있음
### 서버 컴포넌트가 Next.js의 SSR 대체 가능할까?
- 서버 컴포넌트 코드는 클라이언트에 전송이 안됨
- 서버 컴포넌트는 어디든지 백엔드 접근 가능 (Next는 getServerProps로만 접근 가능)
- 클라이언트 상태 유지한 채 서버로 받아올 수 있음
### 참고
- https://yceffort.kr/2022/01/how-react-server-components-work