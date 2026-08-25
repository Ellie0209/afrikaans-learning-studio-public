AFRIKAANS STUDIO — VERCEL 배포 안내
====================================

권장 프로젝트 이름:
afrikaans-learning-studio-public

권장 공개 주소:
https://afrikaans-learning-studio-public.vercel.app
(해당 이름을 다른 사용자가 이미 사용 중이면 Vercel이 다른 주소를 제안할 수 있습니다.)

이 폴더의 파일을 삭제하거나 다른 하위 폴더에 넣지 말고, 다음 파일들이 프로젝트 최상단에 있도록 배포하세요.

index.html
manifest.webmanifest
sw.js
icon-192.png
icon-512.png
vercel.json

방법 A — Vercel 웹사이트에서 GitHub로 배포
1. GitHub에서 새 저장소(repository)를 만듭니다. 예: afrikaans-learning-studio-public
2. 이 폴더 안의 파일 6개를 저장소의 최상단(root)에 업로드합니다.
3. Vercel Dashboard에서 Add New > Project를 선택합니다.
4. 위 GitHub 저장소를 Import합니다.
5. Project Name을 afrikaans-learning-studio-public 으로 입력합니다.
6. Framework Preset은 Other를 선택합니다.
7. Root Directory는 ./ 그대로 둡니다.
8. Build Command는 비워 둡니다.
9. Output Directory도 비워 둡니다.
10. Deploy를 누릅니다.
11. READY가 표시되면 생성된 *.vercel.app 주소를 엽니다.
12. Settings > Deployment Protection에서 일반 방문자가 로그인 없이 볼 수 있도록 보호 설정이 켜져 있지 않은지 확인합니다.

방법 B — Vercel CLI로 배포
1. Node.js를 설치합니다.
2. 터미널에서 이 폴더로 이동합니다.
3. 다음 명령을 실행합니다.
   npm install -g vercel
4. Vercel에 로그인합니다.
   vercel login
5. 첫 배포 및 프로젝트 연결:
   vercel
6. 질문이 나오면:
   - Set up and deploy? Yes
   - Which scope? 본인 Vercel 계정/팀
   - Link to existing project? No (새 프로젝트라면)
   - Project name? afrikaans-learning-studio-public
   - In which directory is your code located? ./
7. 테스트가 정상이라면 production 배포:
   vercel --prod

배포 후 확인할 항목
- 주소를 시크릿/인코그니토 창에서 열어 로그인 없이 바로 들어가는지 확인
- Android Chrome, iPhone Safari, PC Chrome/Edge에서 각각 열어 보기
- 3D 캐릭터 / 남아공 풍경 테마 전환 확인
- 한국어 / 영어 전환 확인
- A0~C2 레벨 버튼 확인
- 레슨 선택, 퀴즈, Writing Lab 확인
- 새로고침 뒤 테마/진행률이 유지되는지 확인

주의
- 학생 학습 기록은 각 기기의 브라우저 localStorage에 저장됩니다. 따라서 다른 휴대폰/PC로 옮기면 기록이 자동 동기화되지는 않습니다.
- 현재 앱 이미지는 HTML 안에 포함되어 있어 외부 이미지 서버가 끊겨서 깨지는 문제를 최소화했습니다.
- Vercel 프로젝트 주소는 실제 사용 가능 여부에 따라 달라질 수 있습니다.
