# Privacy Policy / 개인정보 처리방침 - UsageMeter for Windows

Last updated: 2026-11-19

## English

UsageMeter shows how much of your Claude, Gemini and Codex (ChatGPT) usage limits remain. It has no server of its own and collects nothing for the developer.

**What stays on your PC**
- **Sign-ins.** You sign in to claude.ai, chatgpt.com and gemini.google.com inside the app's built-in browser (Microsoft Edge WebView2). The resulting cookies stay in the app's WebView2 profile on your PC. The app uses them only to ask those services for your own usage, and keeps them in memory while doing so. They are never written to the app's logs or sent anywhere else.
- **Usage history and settings** are saved in `%APPDATA%\UsageMeter` so charts and alerts work.
- **Local usage logs (optional, off by default).** If you turn this on, the app reads the usage logs that Claude Code and Codex CLI already keep on your PC to show token statistics. Only counts and timestamps are stored; conversation text is not.
- **Diagnostic log.** `%APPDATA%\UsageMeter\usagemeter.log` records app events and errors so problems can be fixed. It contains no cookies, tokens or conversations, and is only shared if you attach it yourself.

**Network access**
The app connects only to the AI services you sign in to (claude.ai, chatgpt.com, gemini.google.com and their sign-in pages) to read your usage. If the Google Antigravity CLI (`agy`) is installed, it may run it locally to read Gemini usage. There is no analytics, advertising or tracking.

**Removing your data**
Sign out of each service from the app's menu, or uninstall the app and delete `%APPDATA%\UsageMeter` and `%LOCALAPPDATA%\com.usagemeter.app`.

**Contact**
https://github.com/WWhaleFe/usagemeter-windows/issues

## 한국어

UsageMeter는 Claude · Gemini · Codex(ChatGPT)의 남은 사용 한도를 보여 줍니다. 앱 자체 서버가 없고, 개발자에게 어떤 정보도 보내지 않습니다.

**이 PC 안에만 저장하는 것**
- **로그인**: claude.ai, chatgpt.com, gemini.google.com에 앱 안의 브라우저(Microsoft Edge WebView2)로 로그인합니다. 그 쿠키는 이 PC의 앱 WebView2 프로필에만 남고, 앱은 내 사용량을 그 서비스에 물어볼 때만 메모리에서 씁니다. 로그 파일에 쓰거나 다른 곳으로 보내지 않습니다.
- **사용량 이력과 설정**: 차트와 알림을 위해 `%APPDATA%\UsageMeter`에 저장합니다.
- **로컬 사용 기록(선택, 기본 꺼짐)**: 켜면 Claude Code와 Codex CLI가 이미 이 PC에 남기는 사용 기록을 읽어 토큰 통계를 보여 줍니다. 개수와 시각만 저장하고 대화 내용은 저장하지 않습니다.
- **진단 로그**: `%APPDATA%\UsageMeter\usagemeter.log`에 앱 동작과 오류를 남깁니다. 쿠키·토큰·대화 내용은 없으며, 직접 첨부하지 않는 한 어디에도 보내지 않습니다.

**네트워크 접속**
로그인한 AI 서비스(claude.ai, chatgpt.com, gemini.google.com과 그 로그인 페이지)에만 접속해 사용량을 읽습니다. Google Antigravity CLI(`agy`)가 설치돼 있으면 Gemini 사용량을 읽으려고 이 PC에서 실행할 수 있습니다. 분석·광고·추적은 없습니다.

**데이터 지우기**
앱 메뉴에서 각 서비스에서 로그아웃하거나, 앱을 삭제한 뒤 `%APPDATA%\UsageMeter`와 `%LOCALAPPDATA%\com.usagemeter.app` 폴더를 지우면 됩니다.

**문의**
https://github.com/WWhaleFe/usagemeter-windows/issues
