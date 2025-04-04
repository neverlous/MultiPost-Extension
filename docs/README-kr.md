# MultiPost

> 한 번의 클릭으로 여러 소셜 미디어 플랫폼에 콘텐츠를 게시할 수 있는 브라우저 확장 프로그램

![GitHub License](https://img.shields.io/github/license/leaper-one/MultiPost-Extension) ![GitHub Repo stars](https://img.shields.io/github/stars/leaper-one/MultiPost-Extension) ![GitHub commit activity](https://img.shields.io/github/commit-activity/m/leaper-one/MultiPost-Extension) [![Website](https://img.shields.io/website?url=https%3A%2F%2Fmultipost.app)](https://multipost.app)

[English](../README.md) | [中文](README-zh.md) | [日本語](README-jp.md) | [Français](README-fr.md) | [한국어](README-kr.md)

---

## 설치

- [![Chrome Web Store Version](https://img.shields.io/chrome-web-store/v/dhohkaclnjgcikfoaacfgijgjgceofih)](https://chromewebstore.google.com/detail/multipost/dhohkaclnjgcikfoaacfgijgjgceofih) ![Chrome Web Store Users](https://img.shields.io/chrome-web-store/users/dhohkaclnjgcikfoaacfgijgjgceofih) ![Chrome Web Store Last Updated](https://img.shields.io/chrome-web-store/last-updated/dhohkaclnjgcikfoaacfgijgjgceofih)
- [![](https://img.shields.io/badge/dynamic/json?label=edge%20add-on&prefix=v&query=%24.version&url=https%3A%2F%2Fmicrosoftedge.microsoft.com%2Faddons%2Fgetproductdetailsbycrxid%2Fckoiphiceimehjkolnfffgbmihoppgjg)](https://microsoftedge.microsoft.com/addons/detail/multipost/ckoiphiceimehjkolnfffgbmihoppgjg) [![](https://img.shields.io/badge/dynamic/json?label=users&query=%24.activeInstallCount&url=https%3A%2F%2Fmicrosoftedge.microsoft.com%2Faddons%2Fgetproductdetailsbycrxid%2Fckoiphiceimehjkolnfffgbmihoppgjg)](https://microsoftedge.microsoft.com/addons/detail/multipost/ckoiphiceimehjkolnfffgbmihoppgjg)

## 주요 기능

- Zhihu, Weibo, Xiaohongshu, TikTok 등 10개 이상의 주요 플랫폼에 동시 게시 지원
- 로그인 불필요, 등록 불필요, API 키 불필요. 무료!
- 텍스트, 이미지, 동영상 등 다양한 콘텐츠 형식 지원
- 웹 페이지 연동을 지원하여 자체 웹 페이지를 개발하고 확장 프로그램의 게시 기능을 자동화할 수 있습니다:
  - 웹 페이지 콘텐츠 자동 캡처 및 여러 플랫폼에 자동 게시
  - 게시 일정 관리
  - AI 콘텐츠 생성 연동

이 확장 프로그램은 콘텐츠 크리에이터가 여러 플랫폼에 게시할 때 겪는 어려움을 해결합니다. 한 번의 편집으로 모든 플랫폼에 콘텐츠를 동기화하여 게시할 수 있어 작업 효율성을 크게 향상시킵니다.

## 시작하기

먼저 개발 서버를 실행합니다:

```bash
pnpm i

pnpm dev
```

브라우저 확장 프로그램 페이지에서 개발자 모드를 활성화하고 '압축해제된 확장 프로그램을 로드합니다'를 클릭하여 `build/chrome-mv3-dev`를 선택하여 로드합니다.

## 프로덕션 빌드

다음 명령을 실행합니다:

```bash
pnpm build
```

`build` 폴더에서 빌드된 파일을 찾을 수 있습니다.

## 개발 가이드

### 참고 문서

[Chrome Extension API Reference](https://developer.chrome.com/docs/extensions/reference/api)

[Edge Extension](https://learn.microsoft.com/en-us/microsoft-edge/extensions-chromium/)

[Plasmo Docs](https://docs.plasmo.com/)

### 파일 구조

> src/sync: 이 폴더에는 다양한 플랫폼 작업을 위한 코드가 포함되어 있으며, dynamic은 동적 게시 관련, video는 동영상 게시 관련 코드입니다. 추가된 모든 플랫폼은 common.ts에 등록해야 합니다.
> components: 이 폴더에는 프론트엔드 인터페이스 작업을 위한 모든 컴포넌트가 포함되어 있습니다.

### 개발 환경

패키지 관리자로 `pnpm@latest-9` 사용을 권장합니다.
