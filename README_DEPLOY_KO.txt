Afrikaans Studio · Final v8
============================

최종 구성
- A0–C2, 레벨별 8개 레슨 (총 56개)
- 한국어 / 영어 UI
- 3D Character / South Africa Journey 테마
- Afrikaans 브라우저 TTS (af-ZA 우선)
- 개별 문장 듣기 + 레슨 전체 듣기
- 레슨별 Grammar Focus + 문화/맥락 설명
- Culture Atlas + 출처 표시
- Grammar Lab + 예문 듣기
- South African Phrasebook + 표현 듣기
- 퀴즈, 북마크, Writing Lab, 학습 진도 저장
- 모바일 전용 학습 도구 메뉴
- PWA / 오프라인 핵심 화면 캐시
- 모바일 / 태블릿 / PC 반응형

배포 주소
- 권장 공개 경로: /afrikaans

GitHub + Vercel 배포
1. 이 폴더 안의 파일을 ZIP 상태가 아니라 압축 해제한 파일 상태로 저장소 최상위에 업로드합니다.
2. 기존 같은 이름의 파일은 새 파일로 교체합니다.
3. GitHub에서 Commit changes를 누릅니다.
4. 연결된 Vercel 프로젝트가 자동 재배포됩니다.
5. Production 상태가 READY가 된 뒤 /afrikaans 경로를 확인합니다.

필수 파일
- index.html
- manifest.webmanifest
- sw.js
- vercel.json
- character.webp
- journey.webp
- lesson-scene.webp
- culture.webp
- icon-192.png
- icon-512.png
- README_DEPLOY_KO.txt

캐시 안내
- Service Worker 캐시 버전: afrikaans-studio-v8
- 새 배포 후 이전 화면이 잠시 남으면 모든 기존 탭을 닫고 다시 열거나 시크릿 모드에서 확인하세요.

음성 안내
- 듣기는 기기의 Web Speech / TTS 엔진을 사용합니다.
- Afrikaans (af-ZA) 음성이 있으면 우선 선택합니다.
- Afrikaans 음성이 없을 경우 남아공 영어(en-ZA) 또는 시스템 af-ZA 설정을 사용합니다.

최종 코드 점검 항목
- JavaScript 문법 검사
- Service Worker 문법 검사
- manifest / vercel JSON 검사
- HTML 중복 ID 검사
- 정적 DOM ID 참조 검사
- 한국어/영어 번역 키 누락 검사
- A0–C2 56개 레슨 데이터 구조 검사
- 각 레슨 4개 표현 및 퀴즈 정답 구조 검사
- 로컬 이미지/아이콘 파일 존재 및 크기 검사
- /afrikaans → /index Vercel rewrite 구성 점검
