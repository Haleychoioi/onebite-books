# 📚 ONEBITE BOOKS

이 프로젝트는 인프런의 '한 입 크기로 잘라먹는 Next.js(v15)' 강의를 참고하여 제작한 Next.js 학습용 프로젝트입니다. 페이지 라우터(Page Router)를 중심으로 Next.js의 핵심 기능들을 직접 구현해 보며 익히는 것을 목표로 만들어졌습니다.

**배포 URL**: https://onebite-books-kappa.vercel.app/

---

### 🛠️ 주요 기능

-   **정적 사이트 생성 (SSG)**
    -   메인 페이지 (`/`): `getStaticProps`를 사용하여 빌드 시점에 모든 도서 목록과 추천 도서 목록을 미리 가져와 정적 페이지를 생성합니다.
    -   도서 상세 페이지 (`/book/[id]`): `getStaticPaths`와 `getStaticProps`를 활용해 미리 정의된 도서 페이지를 정적으로 생성합니다.

-   **증분적 정적 재생성 (ISR)**
    -   `pages/api/revalidate.ts` 경로의 API 엔드포인트를 통해 페이지를 재빌드할 수 있습니다.

-   **클라이언트 측 데이터 페칭**
    -   검색 페이지 (`/search`): `useRouter`와 `useEffect`를 사용하여 클라이언트 측에서 검색어에 맞는 데이터를 동적으로 불러와 보여줍니다.

---

### 💻 시작 방법

프로젝트를 로컬 환경에서 실행하려면 아래 명령어를 순서대로 입력해 주세요.

-   **의존성 패키지 설치**
    ```bash
    npm install
    ```
-   **개발 서버 실행**
    ```bash
    npm run dev
    ```
