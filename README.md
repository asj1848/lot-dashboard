# LOT 품질 관리 · 공정 모니터링 데모

AID 해커톤 C주제 MVP 시안입니다. 모든 수치는 가상 데이터입니다.

## 화면

| 파일 | 내용 |
|---|---|
| `start.html` | 시작 화면 (모든 화면 입구) |
| `index.html` | LOT 품질 관리도 대시보드 (CSV 업로드, 이상 판정) |
| `test.html` | 판정 규칙 테스트 시나리오 |
| `live.html` | 휴대폰용 LOT 품질 알림 앱 (이탈 예고 포함) |
| `process.html` | 공정 변수 CCR 콘솔 + 현장 작업자 단말 미리보기 |
| `process.html?role=worker` | 현장 작업자 단말 (휴대폰) |
| `how.html` | 구현 방식 — CCR에서 현장까지 어떻게 연결하나 |
| `qr.html` | 휴대폰 접속 QR |

## 온라인(GitHub Pages)과 발표 PC의 차이

- 온라인 버전은 어느 네트워크에서든 모든 화면을 볼 수 있습니다.
- CCR 콘솔과 휴대폰 단말이 **실시간으로 주고받는 기능**은 서버가 필요합니다. 발표 PC에서 아래처럼 서버를 띄우고, 같은 Wi-Fi의 휴대폰으로 `http://<PC IP>/w` 에 접속하세요.

```powershell
powershell -ExecutionPolicy Bypass -File .\serve.ps1
```

짧은 주소: `/w` 현장 단말, `/q` 품질 알림, `/c` CCR 콘솔, `/d` 대시보드, `/qr` 접속 QR.
