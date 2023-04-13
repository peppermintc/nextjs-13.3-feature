# Next.js 13.0

- [Next.js 13 blog link](https://nextjs.org/blog/next-13)
- 출시일: 2023년 4월 7일
- Next js 13 stable 버전 출시 [Next.js Conf](https://nextjs.org/conf)
- 신규 기능 요약

  - `app` 디렉토리 (베타 버전): 쉽고 빠르고 자바스크립트 코드 감소
    - Layouts
    - React Server Components
    - Streaming
  - Turbopack (알파 버전)
    - 약 700배 가까이 더 빠른 Webpack 대체 Rust based 툴
  - New `next/image`: native browser lazy loading과 성능 향상
  - New `@next/font` (beta): Automatic self-hosted font & zero layout shift
  - Improved `next/link`: 심플한 Automatic `<a>` API

- New App Directory (Beta)

  - routing & layout 경험 개선
  - [Layouts RFC](https://nextjs.org/blog/layouts-rfc) 반영
  - 아직 production 사용은 권장하지 않음
    - pages 폴더, next/image, next/link 사용하다가 추후 선택적으로 app 폴더 사용 권장
  - app 디렉토리 기능
    - 요약
      - Layouts: UI를 routes간 공유 & 상태 보존 & 리렌더링 방지
        Server Components: Making server-first the default for the most dynamic applications.
      - Streaming: 즉시 로딩 상태들을 표시 & 로딩을 기다리지 않고 UI를 스트리밍
      - Support for Data Fetching: async Server Components & extended fetch API 컴포넌트 레벨 fetching을 가능하게함
    - Layouts:
      - app 폴더에서 page.js를 통해 페이지를 만들 수 있고 components, tests, styles 같은 폴더들도 함께 위치시킬 수 있음
      - layout.js 파일을 통해 layout UI를 만들 수 있음
      -
    - [App Router Demo](https://vercel.com/templates/next.js/app-directory)
    - [App Router Docs(beta)](https://beta.nextjs.org/docs/routing/fundamentals)
