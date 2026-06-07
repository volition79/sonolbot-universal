# Sonolbot Universal

Windows와 macOS용 Sonolbot 보안강화 배포 패키지입니다.

일반 사용자는 소스코드를 빌드하지 말고 GitHub Releases에서
`sonolbot_universal.zip`을 다운로드하세요.

## 다운로드

- 최신 릴리스: https://github.com/volition79/sonolbot-universal/releases/latest
- 현재 버전: `0.1.17`
- 패키지 파일: `sonolbot_universal.zip`

## 실행 순서

압축을 푼 뒤 본인 컴퓨터에 맞는 하위 폴더로 들어가 1번부터 실행하세요.

### Windows 64-bit

```text
sonolbot_universal/windows-amd64/
1.사전점검.bat
2.설치하기.bat
3.코덱스로그인.bat 또는 4.클로드코드로그인.bat
5.제미나이로그인.bat 는 현재 미지원/비활성 안내만 표시
6.컨트롤패널.bat
```

### macOS Apple Silicon

```text
sonolbot_universal/macos-arm64/
1.사전점검.command
2.설치하기.command
3.코덱스로그인.command 또는 4.클로드코드로그인.command
5.제미나이로그인.command 는 현재 미지원/비활성 안내만 표시
6.컨트롤패널.command
```

### macOS Intel

```text
sonolbot_universal/macos-amd64/
1.사전점검.command
2.설치하기.command
3.코덱스로그인.command 또는 4.클로드코드로그인.command
5.제미나이로그인.command 는 현재 미지원/비활성 안내만 표시
6.컨트롤패널.command
```

## macOS Gatekeeper 안내

현재 패키지는 Apple notarization을 적용하지 않은 내부/소수 사용자용 배포입니다.
macOS에서 "확인되지 않은 개발자" 또는 quarantine 차단이 나오면,
해당 하위 폴더에서 터미널로 아래 명령을 실행한 뒤 다시 여세요.

```bash
xattr -dr com.apple.quarantine .
```

## 보안 구성

- 실행 바이너리는 `garble` 기반 obfuscated release build입니다.
- 개인 토큰, 봇 설정, 작업 기록, 로그, runtime 상태는 포함하지 않습니다.
- 서버 artifact와 내부 개발자 문서는 포함하지 않습니다.
- 업데이트/활성화 정책은 Sonolbot 서버의 signed update 경로를 기준으로 운영합니다.

## 무결성 확인

릴리스의 `SHA256SUMS.txt` 또는 이 저장소의 `SHA256SUMS.txt`를 확인하세요.

