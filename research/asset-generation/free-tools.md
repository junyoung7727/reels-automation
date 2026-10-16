# 무료로 쓸 수 있는 제작 도구

조사일: 2026-10-02. 계기: 사용자가 "앞으로는 무료로 쓸 수 있는 것을 더 자세히 조사하라"고 했고, 트리포와 메시를 둘 다 써야 하는지, 동작을 만드는 도구는 무엇이 있는지 물었다.

**확인 범위**: 전부 검색 결과의 요약으로 확인했다. 각 서비스의 요금 페이지를 직접 열어 보지 않았고, 계정을 만들어 실제로 써 본 것도 없다. 무료 한도와 라이선스는 자주 바뀌므로 쓰기 직전에 해당 서비스의 요금·라이선스 페이지를 열어 다시 확인한다. 이 프로젝트의 릴스는 게시용이라 **상업적 사용**으로 보고 판단한다.

## AI 3D 생성

| 도구 | 무료 한도 | 무료분의 사용 조건 | 강점 | 이 프로젝트에서 |
|---|---|---|---|---|
| Meshy | 매달 100크레딧(모델 약 5개). 내려받기는 월 10개, 이전 세대(Meshy 5) 결과만 | CC BY 4.0. 출처를 밝히면 상업적 사용 가능 | 질감(PBR)이 좋다. 자동 리깅과 동작 500여 개가 무료 | 무료로 쓰기에 조건이 가장 분명하다. 최신 세대(Meshy 6) 결과는 유료여야 내려받는다 |
| Tripo | 매달 200~300크레딧(모델 약 13개). 내보내기 15개, 동시에 한 작업 | 요금 페이지는 무료분을 "공개, 비상업"으로 표시한다는 글과 CC BY 4.0이라는 글이 엇갈린다 | 빠르다. 차량, 기계, 건축처럼 반듯한 물체의 메시 구조가 낫다는 평가 | 무료분을 게시용 영상에 써도 되는지 불분명하다. 쓰기 전에 요금 페이지를 직접 확인한다 |
| Hyper3D Rodin | 가입 시 10크레딧. 한 번 생성에 0.5~4크레딧 | 확인 못 함 | 손질 없이 제작에 넣을 수 있는 품질이라는 평가가 가장 많다 | 한 번 받는 양이라 주인공 물체 두세 개에 아껴 쓴다 |
| TRELLIS.2 (Microsoft) | 로컬 실행. 무제한 | MIT 라이선스 | 오픈소스 중 품질 평가가 높다 | 8GB 그래픽카드에서는 가장 낮은 해상도(256)만 된다는 글이 있다. 직접 돌려 보지 않았다 |
| Hunyuan3D (Tencent) | 웹에서 하루 30회라는 글 | **라이선스가 한국, EU, 영국을 제외한다** | | 한국에서 쓸 수 없다. 쓰지 않는다 |
| TripoSG (로컬) | 무제한 | MIT | 소품은 통과, 주인공 차량은 탈락 | [직접 검증함](evaluation.md) |

### 트리포와 메시를 둘 다 써야 하나

둘 다 쓸 필요는 없다. 한 물체를 두 서비스에서 만들어 섞는 방식이 아니고, 물체마다 맞는 쪽을 고른다.

- 비교 글들의 평가는 엇갈린다. 넷이즈와 텐센트의 3D 아티스트 대상 블라인드 평가에서 Meshy 6이 63.8% 선호됐다는 글이 있고(메시 쪽 자료), 반듯한 물체의 메시 구조는 Tripo가 낫다는 글도 있다. 두 회사가 각자 낸 비교 자료가 섞여 있어 그대로 믿기 어렵다.
- 무료 범위에서는 조건이 다르다. 메시는 무료분도 출처 표시로 상업적 사용이 되지만 최신 세대를 못 내려받는다. 트리포는 무료 크레딧이 더 많지만 상업적 사용이 불분명하다.
- **권장**: 기본은 메시(조건이 분명함), 주인공급 물체 두세 개는 Rodin 무료 크레딧, 트리포는 라이선스를 확인한 뒤 차량과 기계에만. 어느 것이 실제로 나은지는 같은 물체를 넣어 렌더로 비교해 정한다. 사양이나 평판으로 정하지 않는다.

## 사람이 만든 모델과 재료 (무료)

| 종류 | 곳 | 조건 | 연결 상태 |
|---|---|---|---|
| 모델 | Sketchfab 내려받기 가능 모델 | 모델마다 다름. CC BY가 많다 | 연결됨. 릴스 04의 옵티머스를 여기서 받았다 |
| 모델, 스캔 | Fab (Megascans 포함) | 무료 항목이 있고 조건은 항목마다 다름 | 연결 도구는 있음. 계정 확인 필요 |
| 재질, 환경광, 일부 모델 | Poly Haven | CC0 | 연결됨 |
| 재질 | ambientCG | CC0 | 연결됨 |
| 저폴리 모델 | Poly Pizza, Kenney | CC0 또는 CC BY | 연결됨 |
| 박물관 스캔 | Smithsonian | CC0 | 연결됨 |

릴스 04에서는 Poly Haven과 ambientCG의 재질과 환경광을 쓰지 않았다. 화면이 모형처럼 보인 원인 중 하나다.

## 동작 만들기

| 도구 | 하는 일 | 무료 범위 | 메모 |
|---|---|---|---|
| Mixamo (Adobe) | 사람 모양 모델에 뼈대를 자동으로 넣고, 걷기·달리기·작업 동작 수천 개를 입힌다 | 무료. Adobe 계정 필요 | 사람 모양만 된다. 옵티머스 같은 인간형 로봇에 쓸 수 있다. 웹에서 사람이 올리고 받아야 해서 작업자가 직접 자동화하지 못한다 |
| Meshy 리깅·동작 | 생성한 모델에 뼈대와 동작 500여 개 | 무료 플랜에 포함이라는 글 | 메시에서 만든 모델에 바로 쓴다 |
| Cascadeur | 자세 몇 개만 잡으면 물리에 맞게 사이를 채운다. 모션캡처 다듬기 | 무료 등급, 기간 제한 없음 | 설치형 프로그램. 사람이 조작한다 |
| Rokoko Vision | 웹캠이나 영상에서 동작을 뽑는다 | 무료 | 한 사람, 카메라 하나 |
| QuickMagic | 영상 또는 글에서 몸·손·얼굴 동작을 만든다 | 무료 플랜 | 설치 없음 |
| FreeMoCap | 영상에서 동작을 뽑는 오픈소스 | 무료 | 로컬 실행 |
| Blender 기본 기능 | 키프레임, 경로 따라가기, 뼈대 | 무료 | 작업자가 코드로 직접 다룰 수 있는 유일한 방식. 로봇 팔, 차량, 부품처럼 단단한 물체의 동작에는 충분하다 |

글에서 동작을 만드는 오픈소스 모델(로컬 실행)은 이번에 확인하지 못했다. 필요해지면 따로 조사한다.

### 동작에서 작업자가 할 수 있는 것

- 단단한 물체(차, 로봇 팔, 프레스, 부품)의 동작은 지금처럼 코드로 만든다.
- 사람이나 인간형 로봇이 걷고 물건을 집는 동작은 뼈대가 든 모델과 동작 파일이 필요하다. Mixamo처럼 웹에서 받는 것은 사용자가 내려받아 줘야 한다. 받은 FBX 파일은 작업자가 Blender로 가져와 쓸 수 있다.
- 릴스 04의 옵티머스는 뼈대가 없는 정지 모델이라 줄지어 미끄러지듯 지나간다. 걷게 하려면 뼈대가 든 모델(Sketchfab에 "rigged" 무료 모델이 있음)과 걷기 동작이 필요하다.

## 출처

- [Tripo AI Free Plan 2026 (costbench)](https://costbench.com/software/ai-3d-generation/tripo-ai/free-plan/)
- [Tripo AI Review 2026: Fast 3D Models, Tight Free Tier](https://medium.com/@theovarn/tripo-ai-review-2026-fast-3d-models-tight-free-tier-a8d140045f4a)
- [Meshy: What Is Included on the Free Plan](https://help.meshy.ai/en/articles/15696428-what-is-included-on-the-free-plan)
- [Meshy: Can I Use Meshy Assets Commercially](https://help.meshy.ai/en/articles/9992001-can-i-use-meshy-assets-commercially-license-copyright-explained)
- [Meshy AI Pricing 2026 (stacksheriff)](https://stacksheriff.com/ai-tools/meshy-ai-pricing/)
- [Meshy vs Tripo (Meshy 자료)](https://www.meshy.ai/compare/meshy-vs-tripo), [Tripo vs Meshy (Tripo 자료)](https://www.tripo3d.ai/compare/tripo-vs-meshy), [Tripo AI vs Meshy AI 2026 (OnyxRanked)](https://onyxranked.com/tripo-ai-vs-meshy-ai-2026/)
- [Is Rodin (Hyper3D) Free? (costbench)](https://costbench.com/software/ai-3d-generation/rodin-hyper3d/free-plan/)
- [Hunyuan3D-2.1 LICENSE](https://huggingface.co/tencent/Hunyuan3D-2.1/blob/main/LICENSE)
- [microsoft/TRELLIS.2](https://github.com/microsoft/TRELLIS.2), [Is Trellis 2 Free?](https://www.3daistudio.com/blog/is-trellis-2-free-pricing-how-to-get-started)
- [AI MoCap Free: Best Free AI Motion Capture Tools 2026](https://aimocapfree.com/), [QuickMagic](https://www.quickmagic.ai/), [Free Motion Capture Animation Tools (Krikey)](https://www.krikey.ai/learn/free-motion-capture-animation-tools)
