# UsageMeter for Windows

**한국어** · [English](README.en.md)

화면 **테두리에 색 띠**로 Claude · Gemini · Codex(ChatGPT 플랜)의 남은 사용량을 보여 주는 Windows 트레이 위젯입니다.
사용량을 쓸수록 띠가 짧아져서, 창을 열지 않고도 곁눈질로 잔여량을 알 수 있습니다.

이 저장소는 **Microsoft Store에 올리는 Windows 버전**입니다. macOS 버전은 [usagemeter](https://github.com/WWhaleFe/usagemeter)에 있고, 두 버전은 같은 Rust 코드로 만듭니다.

## ⬇️ 설치

- **Microsoft Store**: 출시 준비 중입니다. 출시되면 업데이트는 Store가 알아서 합니다.
- **시험판**: [Releases](https://github.com/WWhaleFe/usagemeter-windows/releases)에서 PC에 맞는 파일을 받습니다.
  - 대부분의 PC: `UsageMeter-<버전>-windows-x64-setup.exe`
  - Snapdragon 같은 ARM PC: `...-windows-arm64-setup.exe` (설정 → 시스템 → 정보 → "시스템 종류"에서 확인)
  - 설치 없이 쓰려면 `-portable.zip`을 풀어 `usagemeter.exe` 실행(Microsoft Edge WebView2 필요, Windows 11에는 기본 포함)
  - 처음 실행할 때 "Windows의 PC 보호" 창이 뜨면 **추가 정보 → 실행**(시험판은 코드 서명 전입니다)
  - 시험판은 Store 앱과 같은 화면으로 빌드합니다(앱 안 업데이트 확인 없음). 새 시험판은 Releases에서 다시 받습니다.

Windows 10/11, x64·ARM64.

## ✨ 기능

- 화면 가장자리에 AI별 색 띠로 남은 사용량(또는 쓴 양) 표시, 세부 항목(5시간·주간·모델별) 겹쳐 보기
- 띠에 커서를 올리면 사용량 정보와 그 선 강조
- 트레이 아이콘: 클릭하면 정보 카드와 미니 차트, 메뉴(클릭 방식은 설정에서 선택)
- 작업 표시줄을 두르는 선(작업 표시줄을 위·아래·왼쪽·오른쪽 어디로 옮겨도 따라감)
- 사용량 알림, 분석 창(사용 추이·요일×시간대 등)
- 한국어 · English · 日本語

## 🔒 개인정보

로그인 정보와 사용량은 이 PC 안에만 저장하고 개발자에게 보내지 않습니다. 자세한 내용은 [PRIVACY.md](PRIVACY.md).

## 🐞 문제 알리기

[Issues](https://github.com/WWhaleFe/usagemeter-windows/issues)에 남겨 주세요. `%APPDATA%\UsageMeter\usagemeter.log`를 붙이면 원인을 빨리 찾을 수 있습니다(쿠키·대화 내용은 기록하지 않습니다).

## 개발

코드는 `rust/`(Tauri 2 + Svelte)에 있고 macOS 버전과 같은 코드입니다. 빌드·패키지는 `.github/workflows/package-windows.yml`, 테스트는 `rust/tools/check.sh`.
