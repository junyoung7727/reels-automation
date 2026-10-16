# Remotion에 깔아 둔 그리기 라이브러리 (2026-10-08)

사용자가 p5.js 같은 프로젝트를 쓸 수 있는지 물었고, 작업자가 낸 표에서 "중간부터 높음까지 깔고 스킬 적절히 배치"하라고 했다. 규칙은 [제작 스킬](../../../.agents/skills/reels-production/SKILL.md#아-깔려-있는-그리기-도구)에 있고, 이 폴더는 실제로 돌려 본 본보기다.

- sample.tsx (`sample.tsx`; 로컬 자료·배포 제외): 아래 전부를 한 장면에 쓴 시험 코드. `npx tsc --noEmit` 통과, `npx remotion still … --gl=angle`로 8, 30, 52번 프레임을 렌더했다.
- sample-frames.png (`sample-frames.png`; 로컬 자료·배포 제외): 그 세 프레임.

| 깐 것 | 버전 | 시험에서 확인한 것 | 확인하지 못한 것 |
|---|---|---|---|
| `d3-shape`, `d3-scale`, `d3-array`, `d3-interpolate` | 최신 | 릴스 11의 주가 자료로 선과 면 차트, `evolvePath`로 그어지기 | |
| `d3-geo`, `topojson-client`, `world-atlas` | 최신 | 돌아가는 지구본, 서울에서 오스틴으로 자라는 호 | 50m 자료의 속도 |
| `@remotion/noise` | 4.0.532 | 노이즈로 떠다니는 점 160개 | |
| `@remotion/three`, `three`, `@react-three/fiber` | 4.0.532 | 금속 상자가 숫자만큼 늘며 도는 장면, GLSL 셰이더 평면 | 환경광 맵, 그림자, 긴 구간의 렌더 시간 |
| `@remotion/motion-blur` | 4.0.532 | `Trail`로 가로지르는 별의 잔상 | `CameraMotionBlur` |
| `@remotion/transitions` | 4.0.532 | `TransitionSeries`와 `wipe`가 오류 없이 렌더됨 | 전환 중간 프레임을 눈으로 보지 않았다 |
| `@remotion/shapes` | 4.0.532 | `Star` | |
| `roughjs` | 최신 | `generator().toPaths()`를 SVG로, 시드 고정, 그어지기 | |
| `@remotion/lottie`, `lottie-web` | 4.0.532 | import와 타입 검사만 | 실제 파일 재생 |
| `@remotion/rive`, `@rive-app/canvas` | 4.0.532 | import와 타입 검사만 | 실제 파일 재생 |

깔지 않은 것: p5.js(앞 프레임의 상태를 이어 그리는 방식이라 프레임을 따로 렌더하는 Remotion과 안 맞는다. 알고리즘만 참고한다), GSAP, Manim, Matter.js.

설치 위치는 `production/reel-01/remotion/`(다른 편의 `node_modules`는 이곳을 가리키는 링크). `@remotion/*`는 `remotion`과 같은 버전이어야 한다. `npm install`이 취약점 경고 10건을 냈고 살펴보지 않았다.
