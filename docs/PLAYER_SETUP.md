# Esther Server - 플레이어 설정 가이드

이 가이드를 따라하면 모드가 자동으로 설치되고, 이후 업데이트도 게임 실행만 하면 자동 적용됩니다.

---

## 사전 준비
- Minecraft Java Edition 계정 (1.21.4)
- Java 21 설치 (없으면 [Adoptium](https://adoptium.net/)에서 다운로드)

---

## 1단계: Prism Launcher 설치

1. [prismlauncher.org](https://prismlauncher.org/) 에서 본인 OS에 맞는 버전 다운로드
2. 설치 후 실행
3. 우측 상단 계정 아이콘 → **계정 관리** → **Microsoft 추가** → Microsoft 계정으로 로그인

> **Xbox 프로필이 없다고 나오면?**
> [xbox.com](https://xbox.com)에서 동일한 Microsoft 계정으로 로그인한 뒤 Xbox 프로필(게이머태그)을 무료로 생성하세요. 게임을 다시 구매할 필요 없습니다.

---

## 2단계: 인스턴스 생성

1. **인스턴스 추가** 클릭
2. **바닐라** 선택 → 버전 **`1.21.4`** 선택
3. **모드 로더** 탭 → **NeoForge** 선택 → 버전 **`21.4.156`**
4. 이름을 `Esther Server`로 설정
5. **확인** 클릭

---

## 3단계: 모드 자동 설치 설정

게임 실행 시 자동으로 최신 모드를 다운로드하도록 설정합니다.

### 3-1. packwiz-installer-bootstrap 다운로드

1. [packwiz-installer-bootstrap 릴리스 페이지](https://github.com/packwiz/packwiz-installer-bootstrap/releases) 접속
2. **packwiz-installer-bootstrap.jar** 다운로드

### 3-2. 파일 배치

1. Prism Launcher에서 `Esther Server` 인스턴스 우클릭 → **폴더** → **Minecraft 폴더(.minecraft)** 열기
2. 다운로드한 `packwiz-installer-bootstrap.jar`를 해당 폴더에 넣기

### 3-3. Pre-launch 명령어 설정

1. `Esther Server` 인스턴스 우클릭 → **편집**
2. 좌측 메뉴에서 **설정** 선택
3. **커스텀 명령어** 체크박스 활성화
4. **Pre-launch 명령어**에 다음을 그대로 복사-붙여넣기:

```
"$INST_JAVA" -jar packwiz-installer-bootstrap.jar https://team-for-choco.github.io/esther-modpack/pack.toml
```

5. 닫기

---

## 4단계: 기존 설정 가져오기 (선택)

기존 Minecraft 런처를 사용하고 있었다면, 설정을 가져올 수 있습니다.

### 기존 .minecraft 폴더 위치
| OS | 경로 |
|----|------|
| Windows | `%APPDATA%\.minecraft` (탐색기 주소창에 붙여넣기) |
| macOS | `~/Library/Application Support/minecraft` |

### Prism 인스턴스 .minecraft 폴더 열기
인스턴스 우클릭 → **폴더** → **Minecraft 폴더(.minecraft)**

### 복사할 파일/폴더

| 파일/폴더 | 내용 | 필수 여부 |
|-----------|------|-----------|
| `options.txt` | 키 설정, 그래픽, 소리, 시야 등 게임 설정 | 권장 |
| `servers.dat` | 저장된 서버 목록 | 권장 |
| `resourcepacks/` | 리소스팩 | 선택 |
| `screenshots/` | 스크린샷 | 선택 |
| `saves/` | 싱글플레이 월드 | 선택 |

> 위 파일/폴더를 기존 `.minecraft`에서 복사하여 Prism 인스턴스의 `.minecraft` 폴더에 붙여넣기하면 됩니다.

---

## 5단계: 게임 실행

1. `Esther Server` 인스턴스 선택 → **실행**
2. 첫 실행 시 모드가 자동으로 다운로드됩니다 (약 30초 소요)
3. 게임이 시작되면 **멀티플레이** → **서버 추가** → 서버 주소 입력

---

## 이후 업데이트

**별도 작업이 필요 없습니다.** 게임을 실행할 때마다 자동으로 최신 모드가 적용됩니다.

---

## 문제 해결

### "packwiz-installer-bootstrap.jar를 찾을 수 없습니다"
→ `.minecraft` 폴더에 `packwiz-installer-bootstrap.jar`가 있는지 확인하세요.

### 모드가 다운로드되지 않음
→ Pre-launch 명령어가 정확한지 확인하세요. 특히 URL이 아래와 동일해야 합니다:
```
https://team-for-choco.github.io/esther-modpack/pack.toml
```

### Java 버전 오류
→ Prism Launcher → 인스턴스 편집 → 설정 → Java에서 **Java 21**이 선택되어 있는지 확인하세요.
→ 없으면 [Adoptium](https://adoptium.net/)에서 Java 21을 설치하세요.

### Xbox 프로필 관련 오류
→ [xbox.com](https://xbox.com)에서 게이머태그를 무료로 생성하면 해결됩니다.
