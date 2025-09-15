# API를 이용한 협업 웹 제작 프로젝트
<p align="center">
<img width="554" height="117"  alt="logo" src="https://github.com/user-attachments/assets/ee9196c1-a378-453f-a262-ed885714b888" />
</p>

> Next.js, Node.js, Convex를 이용하여 협업 웹 사이트를 제작



---

## 🧠 프로젝트 개요
### 📌 목표
서버사이드 렌더링을 지원하는 Next.js를 사용하여 협업 웹 사이트를 만드는 것을 목표로 했습니다. 기존에 MySQL 등 관계형 데이터 베이스만을 사용해봤기 때문에, Convex로 비관계형 DB를 경험을 하려고 했습니다.
### 🛠️ **사용 기술**
- Next.js 15.2.4v
- Node.js 22.18.0v
- Convex 1.23.0v
- Express 5.1.0v
- WebRTC
### 👉 **환경**
- Window 11 Home
- Visual Studio Code
- AMD Ryzen 7 7735HS with Radeon Graphics
- Ram 32GB

---

## 📁 프로젝트 구조
```
📦 Coope
├─ .gitignore
├─ .gitmessage.txt
├─ README.md
├─ app
│  ├─ (auth)
│  │  └─ (routes)
│  │     ├─ layout.tsx
│  │     ├─ sign-in
│  │     │  └─ [[...sign-in]]
│  │     │     └─ page.tsx
│  │     └─ sign-up
│  │        └─ [[...sign-up]]
│  │           └─ page.tsx
│  ├─ (main)
│  │  ├─ (routes)
│  │  │  ├─ friends
│  │  │  │  └─ page.tsx
│  │  │  └─ workspace
│  │  │     └─ [workspaceId]
│  │  │        ├─ documents
│  │  │        │  ├─ [documentId]
│  │  │        │  │  └─ page.tsx
│  │  │        │  └─ page.tsx
│  │  │        └─ friends
│  │  │           └─ page.tsx
│  │  ├─ _components
│  │  │  ├─ WebRtcComponent.tsx
│  │  │  ├─ addFriend.tsx
│  │  │  ├─ banner.tsx
│  │  │  ├─ callModal.tsx
│  │  │  ├─ callPreJoinModal.tsx
│  │  │  ├─ document-list.tsx
│  │  │  ├─ friend.tsx
│  │  │  ├─ friendRequestList.tsx
│  │  │  ├─ invite-button.tsx
│  │  │  ├─ item.tsx
│  │  │  ├─ menu.tsx
│  │  │  ├─ messageListenert.tsx
│  │  │  ├─ miniCallPopup.tsx
│  │  │  ├─ navbar.tsx
│  │  │  ├─ navigation.tsx
│  │  │  ├─ title.tsx
│  │  │  ├─ trash-box.tsx
│  │  │  ├─ user-item.tsx
│  │  │  └─ userList.tsx
│  │  └─ layout.tsx
│  ├─ (marketing)
│  │  ├─ (routes)
│  │  │  ├─ csAdmin
│  │  │  │  └─ page.tsx
│  │  │  ├─ customerService
│  │  │  │  └─ page.tsx
│  │  │  ├─ function
│  │  │  │  └─ page.tsx
│  │  │  ├─ inquiryPage
│  │  │  │  └─ page.tsx
│  │  │  ├─ inquiryWrite
│  │  │  │  └─ page.tsx
│  │  │  ├─ introduction
│  │  │  │  └─ page.tsx
│  │  │  ├─ notice
│  │  │  │  └─ page.tsx
│  │  │  ├─ noticeEditPage
│  │  │  │  └─ page.tsx
│  │  │  ├─ noticePage
│  │  │  │  └─ page.tsx
│  │  │  └─ support
│  │  │     └─ page.tsx
│  │  ├─ _components
│  │  │  ├─ ScrollToTop.tsx
│  │  │  ├─ answerWrite.tsx
│  │  │  ├─ answers.tsx
│  │  │  ├─ commentForm.tsx
│  │  │  ├─ commentList.tsx
│  │  │  ├─ faq.tsx
│  │  │  ├─ footer.tsx
│  │  │  ├─ heading.tsx
│  │  │  ├─ heroes.tsx
│  │  │  ├─ imageModal.tsx
│  │  │  ├─ logo.tsx
│  │  │  ├─ modal.tsx
│  │  │  ├─ navbar.tsx
│  │  │  ├─ noticeWrite.tsx
│  │  │  ├─ policy.tsx
│  │  │  └─ term.tsx
│  │  ├─ admin
│  │  │  ├─ SearchUsers.tsx
│  │  │  ├─ _actions.ts
│  │  │  └─ page.tsx
│  │  ├─ layout.tsx
│  │  └─ page.tsx
│  ├─ api
│  │  ├─ chat
│  │  │  └─ route.ts
│  │  ├─ edgestore
│  │  │  └─ [...edgestore]
│  │  │     └─ route.ts
│  │  ├─ stt
│  │  │  └─ route.ts
│  │  └─ summary
│  │     └─ route.ts
│  ├─ error.tsx
│  ├─ globals.css
│  ├─ invite
│  │  └─ page.tsx
│  └─ layout.tsx
├─ components.json
├─ components
│  ├─ ai-chat-modal.tsx
│  ├─ chat-context.tsx
│  ├─ cover.tsx
│  ├─ editor.tsx
│  ├─ icon-picker.tsx
│  ├─ modals
│  │  ├─ confirm-modal.tsx
│  │  ├─ cover-image-modal.tsx
│  │  ├─ invite-modal.tsx
│  │  └─ settings-modal.tsx
│  ├─ mode-toggle.tsx
│  ├─ providers
│  │  ├─ convex-provider.tsx
│  │  ├─ modal-provider.tsx
│  │  └─ theme-provider.tsx
│  ├─ search-command.tsx
│  ├─ single-image-dropzone.tsx
│  ├─ spinner.tsx
│  ├─ toolbar.tsx
│  └─ ui
│     ├─ accordion.tsx
│     ├─ alert-dialog.tsx
│     ├─ alert.tsx
│     ├─ avatar.tsx
│     ├─ button.tsx
│     ├─ card.tsx
│     ├─ command.tsx
│     ├─ dialog.tsx
│     ├─ dropdown-menu.tsx
│     ├─ form.tsx
│     ├─ input.tsx
│     ├─ label.tsx
│     ├─ pagination.tsx
│     ├─ popover.tsx
│     ├─ radio-group.tsx
│     ├─ resizable.tsx
│     ├─ scroll-area.tsx
│     ├─ separator.tsx
│     ├─ skeleton.tsx
│     ├─ table.tsx
│     └─ textarea.tsx
├─ convex
│  ├─ README.md
│  ├─ _generated
│  │  ├─ api.d.ts
│  │  ├─ api.js
│  │  ├─ dataModel.d.ts
│  │  ├─ server.d.ts
│  │  └─ server.js
│  ├─ aiChat.ts
│  ├─ chat.ts
│  ├─ client.ts
│  ├─ comments.ts
│  ├─ documents.ts
│  ├─ friends.ts
│  ├─ http.ts
│  ├─ inquiries.ts
│  ├─ notices.ts
│  ├─ rooms.ts
│  ├─ schema.ts
│  ├─ tsconfig.json
│  ├─ users.ts
│  └─ workspace.ts
├─ coope-stt-637f9fa4c1bb.json
├─ dist
│  └─ server.js
├─ eslint.config.mjs
├─ hooks
│  ├─ use-cover-image.tsx
│  ├─ use-invite.tsx
│  ├─ use-scroll-top.tsx
│  ├─ use-search.tsx
│  ├─ use-settings.tsx
│  └─ useMoveScroll.tsx
├─ lib
│  ├─ action.ts
│  ├─ edgestore.ts
│  ├─ generated
│  │  └─ prisma
│  │     ├─ client.d.ts
│  │     ├─ client.js
│  │     ├─ default.d.ts
│  │     ├─ default.js
│  │     ├─ edge.d.ts
│  │     ├─ edge.js
│  │     ├─ index-browser.js
│  │     ├─ index.d.ts
│  │     ├─ index.js
│  │     ├─ package.json
│  │     ├─ query_engine-windows.dll.node
│  │     ├─ runtime
│  │     │  ├─ edge-esm.js
│  │     │  ├─ edge.js
│  │     │  ├─ index-browser.d.ts
│  │     │  ├─ index-browser.js
│  │     │  ├─ library.d.ts
│  │     │  ├─ library.js
│  │     │  ├─ react-native.js
│  │     │  └─ wasm.js
│  │     ├─ schema.prisma
│  │     ├─ wasm.d.ts
│  │     └─ wasm.js
│  ├─ pb.ts
│  └─ utils.ts
├─ middleware.ts
├─ next.config.ts
├─ package-lock.json
├─ package.json
├─ postcss.config.mjs
├─ prisma
│  └─ schema.prisma
├─ public
│  ├─ chat.png
│  ├─ documents-dark.png
│  ├─ documents.png
│  ├─ empty-dark.png
│  ├─ empty.png
│  ├─ error-dark.png
│  ├─ error.png
│  ├─ example1.png
│  ├─ example2.png
│  ├─ file.svg
│  ├─ fonts
│  │  └─ PretendardVariable.woff2
│  ├─ functionPeople.png
│  ├─ globe.svg
│  ├─ icons
│  │  └─ favicon.ico
│  ├─ introduction.png
│  ├─ logo-dark.png
│  ├─ logo-dark.svg
│  ├─ logo.png
│  ├─ logo.svg
│  ├─ moon.png
│  ├─ mountain.jpg
│  ├─ next.svg
│  ├─ reading-dark.png
│  ├─ reading.png
│  ├─ robot.png
│  ├─ robot_dark.png
│  ├─ support1.png
│  ├─ universe.jpg
│  ├─ vercel.svg
│  └─ window.svg
├─ sampleData.jsonl
├─ server
│  └─ server.ts
├─ styles
│  └─ globals.css
├─ tailwind.config.ts
├─ tsconfig.json
├─ tsconfig.server.json
├─ types
│  └─ globals.d.ts
└─ utils
   ├─ audioUtils.ts
   └─ roles.ts
```
©generated by [Project Tree Generator](https://woochanleee.github.io/project-tree-generator)

---
## 실행 방법
- convex 회원가입
### 1. 패키지 설치
- node install


### 3. 실행
- npx convex dev
- npm run dev
- npm run server

---

## 🧪예시 결과
(수정중)

---

## 🧩구현 내용 요약
(수정중)

---

## 🛠️ 개발 중 겪은 문제 & 해결 방법
(수정중)
---
## 🔧 추후 보완점
(수정중)
- 프론트와 백엔드를 큰 프로젝트로 해보는 것이 처음이라 폴더 구조를 나누는 것에 미숙했습니다. 이후에는 폴더나 파일들을 좀 더 세세하게 나누려고 합니다
- 화면 크기에 따른 반응형 사이트로 리팩토링 진행
- 오류 발생 코드 수정

---
## 🔗 참고 자료
(수정중)
## 📃 라이선스
MIT License
