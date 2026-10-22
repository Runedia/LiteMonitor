# <img src="./resources/screenshots/logo.png"  width="28" style="vertical-align: middle; margin-top: -4px;" /> LiteMonitor
가볍고 자유롭게 꾸밀 수 있는 오픈 소스 데스크톱 하드웨어 모니터입니다. CPU, GPU, 메모리, 디스크, 네트워크 등 시스템 상태를 실시간으로 보여 줍니다.

세로/가로/작업 표시줄 표시, 테마 전환, 다국어, 투명도, 3단계 색상 경고를 지원합니다. 화면은 단순하고 설정 항목은 세밀합니다.

> ℹ️ 이 저장소는 [Diorser/LiteMonitor](https://github.com/Diorser/LiteMonitor)를 기반으로 한 수정판입니다.
> - **웹 모니터(HTTP/WebSocket 서버), 플러그인 시스템, 자동 업데이트를 제거했습니다.** 외부로 나가는 통신은 사용자가 승인한 드라이버/FPS 구성 요소 다운로드와 메뉴에서 실행하는 속도 테스트만 남습니다.
> - UI 문구를 한국어로 정리했고, 첫 실행 언어는 한국어입니다.


![LiteMonitor 메인 화면](./resources/screenshots/overview.png)

###  🟢 가로 막대 모드 / 작업 표시줄 모드
![LiteMonitor 가로/작업 표시줄 표시](./resources/screenshots/overview3.png)


# 🖥️ 모니터링 항목

| 분류 | 항목 |
|------|-----------|
| 💻 **프로세서(CPU)** | 사용률, 온도, 클럭, 전력, 팬, 수랭 펌프 |
| 🎮 **그래픽카드(GPU)** | 사용률, 코어 온도, VRAM, 클럭, 전력, 팬. NVIDIA / AMD / Intel 지원 |
| 💾 **시스템(HOST)** | 메모리 사용량, FPS, 디스크 온도, 메인보드 온도, 케이스 팬 |
| 🔋 **배터리(Battery)** | 충전 상태, 잔량, 전력, 전류, 전압 |
| 📀 **디스크(Disk)** | 읽기/쓰기 속도(KB/s, MB/s). 자동/수동 디스크 선택 |
| 🌐 **네트워크(Network)** | 업로드/다운로드 속도(KB/s, MB/s). 자동/수동 네트워크 어댑터 선택 |
| 📈 **트래픽 통계(Traffic)** | 일·주·월·분기·연 단위 업로드/다운로드 사용량 |
| 🔧 **하드웨어 센서(Sensors)** | 하드웨어 상세 창에서 모든 센서 값 조회 |

---

###  🟢 네트워크 속도 테스트
![LiteMonitor 속도 테스트](./resources/screenshots/overview4.png)  👉 ![LiteMonitor 메뉴](./resources/screenshots/overview5.jpg)

###  🟢 하드웨어 추이
![LiteMonitor 하드웨어 추이](./resources/screenshots/overview9.png)

###  🟢 트래픽 통계
![LiteMonitor 트래픽 통계](./resources/screenshots/overview7.png)

---

# 기능

| 기능 | 설명 |
|---|---|
| 🎨 사용자 테마 | JSON으로 색상, 글꼴, 간격, 모서리 반경을 정의합니다. 내장 테마 편집기를 제공합니다. |
| 🟥🟨🟩 **3단계 색상 경고** | 임계값에 따라 막대와 값의 색이 바뀝니다. 네트워크/디스크는 임계값을 따로 둘 수 있습니다. |
| 🌍 다국어 | 한국어, 영어, 일본어, 중국어(간체/번체), 독일어, 스페인어, 프랑스어, 러시아어 |
| 📊 항목 표시 관리 | CPU, GPU, VRAM, 메모리, 디스크, 네트워크 등을 골라서 표시합니다. |
| 🧮 **가로 모드** | 열별 너비, 단위 자동 서식, 2줄 표시, 패널 너비 자동 계산 |
| 🔠 **UI 배율** | DPI 자동 대응과 사용자 배율 |
| 🎞️ **부드러운 갱신** | 값 변화를 애니메이션으로 완화합니다. 속도는 조절할 수 있습니다. |
| 🪟 창 표시 | 둥근 모서리, 투명도, 그림자, 고품질 글꼴 렌더링 |
| 🧭 가장자리 자동 숨김 | 화면 가장자리에 붙이면 접히고, 마우스를 가져가면 펼쳐집니다. 다중 모니터 지원 |
| 🧲 **화면 밖 이동 제한** | 켜면 창을 화면 밖으로 끌어낼 수 없습니다. |
| 👆 클릭 통과 | 켜면 창이 마우스 입력을 가로채지 않습니다. |
| 🧹 메모리 정리 | 메뉴에서 프로세스 작업 집합을 정리합니다. |
| 🚀 자동 시작 | 작업 스케줄러로 관리자 권한 자동 시작을 등록합니다. |
| 📂 설정 저장 | 모든 설정을 실행 파일 옆 `settings.json`에 저장합니다. |

---

## 📦 설치와 사용

1. 소스를 빌드하거나(아래 "빌드" 참고) 빌드된 파일을 받습니다.
2. **일반 사용자가 쓸 수 없는 폴더**(예: `C:\Program Files\LiteMonitor`)에 둡니다.
3. `LiteMonitor.exe`를 실행합니다. 첫 실행 언어는 한국어이며, 설정에서 바꿀 수 있습니다.

### 권한과 드라이버
- 이 프로그램은 **항상 관리자 권한으로 실행**됩니다. CPU 온도·클럭·전력, 메인보드 온도·팬, 디스크 SMART 온도, FPS 측정에 필요합니다.
- CPU 센서를 읽으려면 서명된 커널 드라이버 **PawnIO**가 필요합니다. 없으면 설치 여부를 묻습니다.
- 관리자 권한으로 실행되므로, 일반 사용자가 쓸 수 있는 폴더에 두면 다른 프로그램이 실행 파일을 바꿔 권한을 얻을 수 있습니다. 설치 위치를 꼭 지켜 주세요.

### 업데이트
자동 업데이트 기능은 없습니다. 새 버전은 소스를 받아 다시 빌드한 뒤, 실행 파일과 `resources` 폴더를 교체하세요. `settings.json`, `TrafficHistory.json`, `HardwareHistory.json`은 그대로 두면 설정과 기록이 유지됩니다.

---

## 🎨 테마

테마 파일은 `resources/themes/` 폴더에 있습니다.

예시:
```json
{
  "name": "DarkFlat_Classic",
  "layout": { "rowHeight": 40, "cornerRadius": 10 },
  "color": {
    "background": "#202225",
    "textPrimary": "#EAEAEA",
    "barLow": "#00C853"
  }
}
```

> - 레이아웃 필드는 단순하고 일관됩니다.
> - 글꼴과 레이아웃은 따로 배율이 적용됩니다.
> - 모든 레이아웃은 `Theme.Scale`이 자동으로 처리합니다.

---

## ⚙️ 설정 파일(settings.json)

| 필드 | 설명 |
|------|------|
| `Skin` | 현재 테마 이름 |
| `PanelWidth` | 패널 너비(세로/가로 모드 각각) |
| `UIScale` | UI 배율 |
| `Opacity` | 투명도(0.1 ~ 1.0) |
| `Language` | 현재 언어(비어 있으면 한국어) |
| `TopMost` | 항상 위 |
| `AutoStart` | 자동 시작 |
| `AutoHide` | 가장자리 자동 숨김 |
| `ClampToScreen` | 화면 밖 이동 제한 |
| `ClickThrough` | 클릭 통과 |
| `RefreshMs` | 갱신 간격 |
| `AnimationSpeed` | 값 애니메이션 속도 |
| `HorizontalMode` | 가로/세로 모드 |
| `PreferredNetwork` | 수동 선택 네트워크 어댑터(비어 있으면 자동) |
| `PreferredDisk` | 수동 선택 디스크(비어 있으면 자동) |
| `MonitorItems` | 모니터링 항목별 표시 설정 |

---

## 🧩 구조

| 파일 | 역할 |
|------|------|
| `MainForm_Transparent.cs` | 메인 창, 드래그, 트레이 메뉴, 자동 숨김, 투명도, 위치 저장 |
| `UIController.cs` | 테마 로드, DPI/UIScale 배율, 레이아웃 재구성, 렌더링, 주기 갱신 |
| `UIRenderer.cs` | 세로 모드 렌더러(그룹, 막대, 제목) |
| `HorizontalRenderer.cs` | 가로 모드 렌더러(2줄 레이아웃, 라벨과 값) |
| `UILayout.cs` | 세로 모드 레이아웃 계산 |
| `HorizontalLayout.cs` | 가로 모드 열 너비와 패널 너비 계산 |
| `ThemeManager.cs` | 테마 로드, 색상 해석, 글꼴 생성 |
| `LanguageManager.cs` | 언어 파일 로드, 평탄화된 키 조회 |
| `HardwareMonitor.cs` | CPU/GPU/MEM/NET/DISK 수집, 자동/수동 장치 선택 |
| `DriverInstaller.cs` | PawnIO 드라이버와 FPS 구성 요소 설치 |
| `AutoStart.cs` | 작업 스케줄러 등록으로 자동 시작 관리 |
| `AboutForm.cs` | 정보 창 |

---

## 🛠️ 빌드

### 요구 사항
- Windows 10 / 11
- .NET 8 SDK
- Visual Studio 2022 또는 Rider

### 명령
```powershell
git clone <이 저장소 주소>
cd LiteMonitor
dotnet build LiteMonitor.csproj -c Release
```

출력 파일:
```
bin/Release/net8.0-windows/LiteMonitor.exe
```

언어 파일(`resources/lang`)과 테마(`resources/themes`)는 같은 출력 폴더에 함께 복사됩니다. 배포할 때는 출력 폴더 전체를 옮기세요.

PawnIO 드라이버(`driver.zip`)와 FPS 구성 요소(`LiteMonitorFPS.exe`)는 출력에 포함되지 않습니다. 필요할 때 설치 여부를 물은 뒤 원본 저장소 미러(Gitee, litemonitor.cn, GitHub)에서 받습니다. 저장소의 `resources/assets`에도 같은 파일이 들어 있습니다.

### 회귀 테스트
```powershell
dotnet run --project test/ReleaseReview/ReleaseReview.csproj -c Release
dotnet run --project test/SecurityRegression/SecurityRegression.csproj
```

---

## 📄 라이선스
**MIT License**를 따릅니다. 자유롭게 사용, 수정, 배포할 수 있습니다.

---

## 📬 원본 프로젝트
**원작자**: Diorser
**원본 저장소**: [https://github.com/Diorser/LiteMonitor](https://github.com/Diorser/LiteMonitor)
