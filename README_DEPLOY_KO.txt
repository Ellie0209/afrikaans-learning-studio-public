Afrikaans Studio · 최종 점검/수정본
====================================

이 폴더의 파일들을 GitHub 저장소의 최상위(root)에 올리면 됩니다.
ZIP 파일 자체를 올리지 말고, 압축을 푼 뒤 아래 파일들을 모두 업로드하세요.

필수 파일
- index.html
- manifest.webmanifest
- sw.js
- vercel.json
- icon-192.png
- icon-512.png
- character.webp
- journey.webp
- lesson-scene.webp
- culture.webp
- README_DEPLOY_KO.txt

이번 수정 사항
1. 모바일에서 '듣기'가 작동하지 않던 원인 수정
   - 기존 setTimeout 기반 연속 재생을 제거했습니다.
   - 모든 문장을 사용자의 탭 이벤트 안에서 SpeechSynthesis 큐에 즉시 등록합니다.
2. Afrikaans 음성 선택 보강
   - af-ZA → 기타 Afrikaans 음성 → South African English 순으로 안전하게 선택합니다.
   - 음성 API가 없는 환경에서는 조용히 실패하지 않고 안내합니다.
3. 개별 스피커 버튼과 전체 듣기 버튼의 모바일 터치 안정성 보강
4. 첫 실행에서 잠긴 두 번째 레슨이 선택되던 상태 오류 수정
5. 오래되거나 잘못 저장된 localStorage 상태를 안전하게 정규화
6. Service Worker 실제 등록 추가 및 캐시 버전 v7로 갱신
7. HTML/아프리칸스 경로를 최신 파일로 재검증하도록 Vercel 캐시 헤더 보강
8. 중복 삽입되어 있던 대형 base64 이미지를 4개의 WebP 파일로 분리/최적화
   - 디자인은 유지하면서 초기 HTML 크기를 약 2.1MB에서 약 130KB로 줄였습니다.
9. A0-C2 7개 레벨, 총 56개 레슨 데이터 구조/퀴즈/문구 배열 검증
10. 모바일 360/390px, 태블릿 768px, 데스크톱 1440px 레이아웃 테스트

Vercel 설정
- Framework Preset: Other
- Root Directory: ./
- Build Command: 비워두기
- Output Directory: 비워두기

배포 후 이전 화면이 남으면
- 새로고침
- 또는 시크릿 모드에서 확인
Service Worker v7이 활성화되면 오래된 캐시는 자동으로 정리됩니다.
