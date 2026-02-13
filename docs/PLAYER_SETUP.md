# Esther Server - 플레이어 설정 가이드

## 사전 준비
- Minecraft Java Edition 구매 (1.21.4)
- [Prism Launcher](https://prismlauncher.org/) 설치

## 1단계: Prism Launcher 설치 및 로그인
1. [prismlauncher.org](https://prismlauncher.org/)에서 다운로드 후 설치
2. Prism Launcher 실행
3. 우측 상단 계정 아이콘 → Microsoft 계정으로 로그인

## 2단계: 인스턴스 생성
1. **인스턴스 추가** 클릭
2. **바닐라** 선택 → 버전 `1.21.4` 선택
3. **모드 로더** 탭 → **NeoForge** 선택 → 버전 `21.4.156`
4. 이름을 `Esther Server`로 설정
5. **확인** 클릭

## 3단계: packwiz-installer 설정
packwiz-installer는 게임 실행 시 자동으로 최신 모드를 다운로드합니다.

### packwiz-installer 다운로드
1. [packwiz-installer 릴리스 페이지](https://github.com/packwiz/packwiz-installer/releases)에서 `packwiz-installer.jar` 다운로드

### 인스턴스에 설정
1. 생성한 `Esther Server` 인스턴스 우클릭 → **편집**
2. **설정** → **커스텀 명령어**
3. **Pre-launch 명령어**에 다음 입력:

```
"$INST_JAVA" -jar packwiz-installer.jar https://team-for-choco.github.io/esther-modpack/pack.toml
```

4. 다운로드한 `packwiz-installer.jar`를 인스턴스의 `.minecraft` 폴더에 복사
   - 인스턴스 우클릭 → **폴더** → **Minecraft 폴더** 열기
   - 해당 폴더에 `packwiz-installer.jar` 넣기

## 4단계: 실행
1. `Esther Server` 인스턴스 선택 → **실행**
2. 첫 실행 시 모드가 자동으로 다운로드됨
3. 멀티플레이 → 서버 추가 → 서버 주소 입력

## 업데이트
별도 작업 없이 게임을 실행할 때마다 자동으로 최신 모드가 적용됩니다.

## 문제 해결

### "packwiz-installer.jar를 찾을 수 없습니다"
- `packwiz-installer.jar`가 `.minecraft` 폴더에 있는지 확인

### 모드가 다운로드되지 않음
- 인터넷 연결 확인
- Pre-launch 명령어가 정확한지 확인
- URL이 `https://team-for-choco.github.io/esther-modpack/pack.toml`인지 확인

### Java 버전 오류
- Prism Launcher 설정에서 Java 21이 선택되어 있는지 확인
- 필요 시 [Adoptium](https://adoptium.net/)에서 Java 21 설치
