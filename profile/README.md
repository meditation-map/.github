# 명상 웰니스 지도

**가까운 곳에서, 나에게 맞는 명상을**

동네 명상 센터와 명상 선생님을 지도에서 찾아보세요. 어떤 프로그램이 열리는지, 누가 가르치는지 한곳에서 보고, 마음에 드는 곳은 찜해 둘 수 있어요. 휴대폰 브라우저에서 바로 여는 명상 장소·전문가 지도 웹앱입니다.

👉 [healingmedit.kr](https://healingmedit.kr)

<table>
  <tr>
    <td align="center" width="33%"><b>처음 만나기</b></td>
    <td align="center" width="33%"><b>지도에서 찾기</b></td>
    <td align="center" width="33%"><b>선생님 알아보기</b></td>
  </tr>
  <tr>
    <td><img src="images/welcome.png" alt="회원인지 처음인지 묻는 대화형 시작 화면"></td>
    <td><img src="images/region-map.png" alt="명상 장소가 마커로 표시된 지도와 검색창"></td>
    <td><img src="images/expert-detail.png" alt="전문 분야·학위·경력·클래스가 보이는 명상 전문가 화면"></td>
  </tr>
</table>

<sub>2026.11.18 최신 코드의 테스트용 화면을 캡처했습니다. 지도 타일과 사진은 비워 두었고, 화면 속 장소·전문가는 예시입니다.</sub>

## 이런 걸 할 수 있어요

- **동네에서 찾기** — 지역을 고르면 근처 명상 장소가 지도에 표시돼요. 이름·주소·기관명·태그로 검색할 수도 있어요.
- **장소 살펴보기** — 프로그램과 강사, 이용 요금, 유의사항, 다녀온 사람들의 후기를 확인해요.
- **선생님 알아보기** — 전문 분야, 학위·자격, 경력, 1:1·그룹 클래스, 활동 지역을 보고 나에게 맞는 선생님을 찾아요.
- **찜해 두기** — 가 보고 싶은 곳은 찜해 두었다가 언제든 다시 꺼내 봐요.
- **앱처럼 쓰기** — 설치 없이 열리고, 홈 화면에 추가하면 앱처럼 쓸 수 있어요.

## 저장소

| 저장소 | 하는 일 |
|---|---|
| **meditation-map-fe** | 웹앱 화면 |
| **meditation-map-be** | API 서버 |
| **meditation-map-obs** | 지표·트레이스 수집과 장애 경보 |
| **meditation-map-mobile** | 모바일 앱 (준비 중) |

## 로컬 실행

**프론트엔드**: Node.js

```bash
npm ci
npm run dev
```

`VITE_API_BASE_URL`에 백엔드 주소를 넣어 주세요. 예: `http://localhost:8080`

**백엔드**: Java 17, Docker

```bash
docker compose up -d   # MySQL(3307) · Redis
./gradlew bootRun --args='--spring.profiles.active=local --server.port=8080'
```

**기술:** React · TypeScript · Vite · Spring Boot · MySQL · Redis · AWS · OpenTelemetry
