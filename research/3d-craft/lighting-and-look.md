# 3D 컷의 조명, 렌더 룩, 마무리

조사일: 2026-10-08. 계기: 사용자가 3D는 "진짜 영화 CG처럼, AI 티 없이" 보여야 한다고 했고, 조명을 "최대로" 밀어 달라고 했다. 영상은 만들지 않았다. 이 문서 하나만 썼다.

**상태**: 작업자의 조사와 종합이다. 사용자가 확인하지 않았다. 아래 "규칙 후보"는 후보일 뿐이고, 스킬에 넣기 전에 실제 컷으로 시험해야 한다.

## 요약

어두운 무대 위의 광택 물체는 빛을 받아서가 아니라 **빛나는 면을 비춰서** 모양이 보인다. 자동차 촬영 감독, 제품 사진가, 자동차 CG 조명 도구 회사가 모두 같은 말을 한다. 그래서 조명의 대부분은 "물체가 무엇을 비추는가"를 설계하는 일이다. 머리 위의 큰 면광원 하나가 윗면과 어깨선에 긴 그러데이션을 그리고, 뒤쪽 양옆의 가는 띠 광원이 윤곽선을 따서 검은 배경과 떼어 놓고, 나머지는 일부러 검게 둔다. Blender 5.2에서는 이 설계에 필요한 도구가 전부 코드로 닿는다. 면광원에 노드로 그러데이션을 입힐 수 있고(직접 시험해서 확인), 빛을 특정 물체에만 닿게 할 수 있고(light linking), 빛별로 패스를 나눠 다시 렌더하지 않고 균형을 볼 수 있다(light group). 재질은 조명의 절반이다. 거칠기가 한 값이면 반사가 한 덩어리로 보이고, 모서리가 날카로우면 하이라이트가 안 생긴다. 색 관리는 AgX가 기본이고 Filmic은 공식 문서에서 폐기 예정이다. 마무리(블룸, 색수차, 비네트, 그레인)는 "거의 안 보일 만큼"이 공통 의견이고, 우리 영상은 글자가 나중에 Remotion에서 올라가므로 화면 전체에 걸리는 효과는 Remotion 쪽에 두는 것이 맞다(작업자 판단). 8GB에서 비싼 것은 장면 전체를 채운 안개다. 간단한 시험 장면에서 프레임 시간이 약 4배가 됐고 검은 무대가 회색으로 떴다. Blender 4.5~5.0 사이에 합성 노드 API가 크게 바뀌어서 옛 스크립트는 5.2에서 돌지 않는다. 이 문서의 코드 조각은 이 컴퓨터의 Blender 5.2.2에서 실행해 본 것이다.

## 방법과 한계

- **직접 확인한 것**: 이 컴퓨터의 Blender 5.2.2 LTS(헤드리스, RTX 5060 8GB, OptiX)에서 속성 이름과 기본값을 뽑았고, 작은 시험 장면을 렌더했다. 아래에서 "5.2.2에서 확인"이라고 적은 것이 이것이다. 시험 장면은 정육면체 하나와 바닥뿐이라 실제 컷의 렌더 시간을 대표하지 않는다.
- **원문을 읽은 것**: Blender 5.2 매뉴얼의 해당 쪽(파일로 받아 본문을 읽음). 릴리스 노트와 그 밖의 웹 문서는 요약 도구를 거쳐 읽었다. 인용은 요약 도구가 돌려준 문장이므로 글자 하나까지 정확하다고 보장하지 못한다.
- **검색 요약만 본 것**: 출처 표에 따로 표시했다. 규칙의 유일한 근거로 쓰지 않았다.
- 읽지 못한 것: 유료 강의 본편(Gleb Alexandrov, CG Cookie, Chocofur), 책 『Light: Science & Magic』 본문, ASC의 자동차 광고 조명 글(접속 실패), Evermotion의 Principled 글(403), 스튜디오의 자동차 CG 제작기.
- 작업자는 영상을 재생하지 못한다. 깜빡임, 노이즈의 끓음, 그레인의 느낌은 판단하지 못했다.
- 숫자는 출처가 준 것만 적었다. 출처가 사람 얼굴 조명용으로 준 숫자(조명비)를 제품에 옮겨 쓰는 것은 작업자의 추론이고 그렇게 표시했다.

## 1. 스튜디오 제품·자동차 조명

### 널리 합의된 것 (서로 다른 출처 셋 이상)

| 주장 | 내용 | 출처 |
|---|---|---|
| 광택 물체는 반사를 찍는 것이다 | 차에서 광택이 없는 부분은 타이어뿐이다. 차의 표면에는 주변이 비친다. 조명은 스튜디오의 무엇이 차에 비칠지를 정하는 일이다 | Lightmap(읽음), Bennett ASC(읽음), 사진 포럼(요약) |
| 직접 반사는 광원의 거울상이다 | 반사가 보이느냐는 광원, 물체, 카메라 사이의 각도로 정해진다. 금속은 "비추고 나머지를 어둡게 두거나, 표면 전체가 빛을 비추게 채우거나" 둘 중 하나다 | Light: Science & Magic 강의 요약(읽음), 책 목차(요약) |
| 머리 위의 큰 부드러운 광원 | 스튜디오 자동차 촬영의 표준이다. 차의 선에 반사가 정확히 걸릴 때까지 기울이고 옮긴다 | Lightmap(읽음), Visual Education(읽음) |
| 간접광과 반사판으로 그러데이션을 만든다 | 직접광은 거친 반사를 만든다. 흰 벽이나 판에 빛을 쏘아 그 판이 차에 비치게 하면 그러데이션이 생긴다 | Visual Education(읽음), Lightmap(읽음) |
| 뒤에서 오는 빛이 검은 배경과 물체를 뗀다 | 검은 배경의 검은 제품은 뒤쪽 광원이 만든 가장자리 빛(림)으로 윤곽이 생긴다. 배경으로 새는 빛은 검은 판으로 막는다 | Visual Education 검은 제품(읽음), Lensvid(읽음), Creative Shrimp(읽음) |
| 과하게 비추면 평평해진다 | 그림자가 없으면 형태가 평평해진다. 전부 똑같이 밝으면 아무것도 중요하지 않다 | Blender Guru(읽음), Creative Shrimp(읽음), 조명비 해설(읽음) |
| 광원의 크기가 그림자와 하이라이트의 부드러움을 정한다 | 큰 광원은 그림자와 하이라이트가 부드럽고, 같은 출력이면 더 어둡게 보인다(출력이 넓은 면에 퍼지므로) | Blender 매뉴얼(읽음), Blender Guru(읽음) |

### 구체적인 기법

- **띠 광원(형광등 꼴)**: 단단한 반사선을 만들고 메탈릭 도장을 살린다. 길이가 있어 그림자는 부드럽다. (Lightmap)
- **스폿**: 가까이 두면 작고 센 하이라이트가 생겨 그 주변의 메탈릭 입자가 살아난다. 멀리 두면 햇빛처럼 단단한 그림자가 생겨 차를 바닥에 "심는다". (Lightmap)
- **판 위의 핫스폿**: 흰 판에 스폿 여러 개를 쏘면 반사 안에 밝은 점이 여러 개 생겨 반사가 살아난다. (Lightmap)
- **CG만의 이점**: 조명 효과는 유지한 채 광원을 반사에서 숨길 수 있다. (Lightmap) Blender에서는 물체별 광선 가시성과 light linking이 이 일을 한다.
- **자동차 광고 세트의 실제 구성**: 10×20피트 무명천 판 둘, 12×12피트 검은 판, 띠 광원, 따뜻한 쪽과 차가운 쪽 젤, 지평선 빛. 차는 앞 3/4 각도. 밝은 손전등으로 반사에 문제가 있는 곳을 찾는다. 노출은 반사를 스폿 측광으로 잰다. (Bennett ASC, No Film School 정리)
- **뒤로 뺀 주광(reverse key)**: 주광을 물체 뒤쪽, 카메라 반대편에 둔다. 그림자가 카메라 쪽으로 감기고 하이라이트가 윤곽을 그린다. 정면 쪽 주광은 그림자가 적어 평평하다. 글쓴이 스스로 "만능은 아니다"라고 했다. (Creative Shrimp)
- **색온도**: 실제 빛은 켈빈으로 잰다. 흰 빛만 쓰면 현실감이 떨어진다. (Blender Guru) Blender 5.2의 조명에는 색온도 속성이 따로 있다.
- **빛에 무늬 넣기**: 광원에 텍스처를 입히면 화면 밖에 무언가 있다는 인상을 준다. (Blender Guru, Creative Shrimp)

### 한 사람의 의견

- Karl Taylor(Visual Education)는 자동차 촬영에 소프트박스를 쓰지 않고 판에 반사시킨 빛만 쓴다. 다른 출처는 큰 소프트박스를 표준으로 든다. CG에서는 둘 다 "그러데이션이 있는 큰 발광면"으로 같아진다.
- 검은 차에는 차 길이의 세 배가 넘는 머리 위 소프트박스가 필요하다는 말은 사진 포럼의 글 하나다(검색 요약). 숫자로 쓰지 않는다.
- Chocofur는 제품 렌더에서 면광원보다 스폿을 선호하고, 크롬과 유리에는 HDRI를 "조명이 아니라 반사의 원천"으로 쓴다(검색 요약, 본문은 못 읽음).
- Creative Shrimp의 "모두가 짜증 날 때까지 빛을 더하라"는 네온 도시 장면에 관한 말이다. 어두운 무대의 제품 컷에는 맞지 않는다.

### 어두운 화면에서 형태가 읽히게 하는 법

출처들이 가리키는 것은 같다. 검은 곳을 많이 두되, **물체의 윤곽선과 면이 꺾이는 자리에는 반드시 빛나는 것이 비치게 한다.**

1. 림이 윤곽을 따라 이어져야 한다. 끊긴 곳에서 물체가 배경에 녹는다.
2. 면이 바뀌는 곳마다 밝기가 달라야 한다. 윗면, 옆면, 앞면이 같은 밝기면 덩어리로 보인다.
3. 반사 안에 밝은 곳과 검은 곳이 함께 있어야 한다. 금속을 전부 흰 반사로 채우면 회색 플라스틱처럼 보이고, 전부 검으면 구멍으로 보인다.
4. 조명비는 주광과 보조광의 밝기 차이다. 1스톱이 2:1, 2스톱이 4:1, 3스톱이 8:1이다. 8:1은 "매우 극적이고 양식적"이라고 한다(StudioBinder, 읽음). 다른 요약은 8:1에서 그림자가 거의 검어져 질감과 형태가 숨는다고 했다(검색 요약). 이 숫자는 사람 얼굴 조명용이다. 제품에 그대로 옮기는 것은 추론이다.
5. 아래에서 올려 비추는 빛의 문제를 직접 다룬 출처는 찾지 못했다. 확인하지 못한 것으로 둔다.

### Blender에서 직접 확인한 것

- 면광원의 `normalize`가 켜져 있으면(기본) 크기를 키워도 총 출력이 같다. 그래서 큰 광원일수록 반사에 비친 면이 어둡다. 끄면 크기에 비례해 출력이 는다. 시험: 크기를 2배로 하고 `normalize`를 끄니 확산 구의 평균 밝기가 0.38에서 0.50으로 올랐다(표시 변환 뒤 값).
- 면광원에 노드로 그러데이션을 입히면 거울 반사에 그대로 보인다. 좌표는 `Geometry → Parametric`과 `Texture Coordinate → UV` 둘 다 광원 면을 0~1로 덮는다. 시험: 반사된 광원의 한쪽 끝이 0.075, 가운데가 3.94, 반대쪽 끝이 7.81(선형 값)이었다. 노드가 없을 때는 끝에서 끝까지 7.8~8.0으로 평평했다.
- 조명 물체의 `visible_diffuse = False`는 Cycles에서 동작한다. 확산 구의 평균이 0.373에서 0.039로 떨어졌고 크롬 구의 반사는 남았다. "반사에만 보이는 빛"을 이렇게 만든다.
- 조명 데이터의 `diffuse_factor`와 `specular_factor`를 0으로 해도 Cycles 렌더는 그대로였다. Cycles에서는 쓰지 않는다. 물체 쪽의 `visible_*`를 쓴다.

## 2. HDRI, 면광원, light linking, 고보, 색온도

| 주제 | 내용 | 출처 |
|---|---|---|
| HDRI의 가장 밝은 곳이 가장 중요하다 | 밝은 곳이 잘린(clipped) HDRI는 빛이 어둡고, 색이 빠지고, 반사가 약하다. Poly Haven은 잘리지 않은 것만 올린다 | Poly Haven 블로그(읽음) |
| 조명용 해상도 | 조명만 쓸 때는 4K나 2K로 충분하고, 배경으로도 보일 때 16K가 쓸모 있다 | Poly Haven 블로그(검색 요약) |
| 환경 텍스처 노드 | 이미지 조명에는 Image Texture가 아니라 Environment Texture 노드를 쓴다 | Blender 매뉴얼(읽음) |
| 보이는 배경과 비추는 배경을 나눈다 | Light Path의 Is Camera Ray로 섞으면 카메라에 보이는 배경과 조명·반사에 쓰는 배경을 다르게 할 수 있다 | Blender 매뉴얼 World Settings(읽음) |
| 월드의 광선 가시성 | 월드도 광선 종류별로 보이게, 안 보이게 할 수 있다 | Blender 매뉴얼(읽음), 5.2.2에서 속성 확인 |
| HDRI의 중요도 표본 | 작은 밝은 점이 있는 환경 맵에서 노이즈를 줄인다. 필요 없는 장면에서는 다른 광원의 표본을 뺏는다 | Blender 매뉴얼 Reducing Noise(읽음) |
| HDRI로는 림을 조절하기 어렵다 | 빛의 방향을 마음대로 잡기 어렵다는 것이 HDRI 조명의 어려움으로 꼽힌다 | Gleb Alexandrov 강의 소개(검색 요약) |
| Light linking | 빛이 특정 물체만 비추게 한다. Shadow linking은 어떤 물체가 그 빛을 가릴지 정한다. Blender 4.0의 Cycles에 들어왔다. 매뉴얼의 예가 "인물만 비추고 아무것에도 가리지 않는 림 라이트"다 | 4.0 릴리스 노트(읽음), 5.2 매뉴얼(읽음) |
| Light linking의 비용 | Light tree가 켜져 있을 때 가장 효율적이다. Shadow linking을 쓰면 광선을 더 쏘아 느려질 수 있다. 발광 메시의 light linking은 Cycles에서만 된다 | 5.2 매뉴얼(읽음) |
| 조명 노드 | Cycles에서는 조명을 셰이더 노드로 정의할 수 있고, 텍스처로 광원 면의 색과 세기를 바꿀 수 있다. EEVEE는 조명 노드를 무시한다 | 5.2 매뉴얼(읽음) |
| Spread | 면광원의 빛이 퍼지는 각이다. 작게 하면 격자를 단 소프트박스처럼 빛이 모인다. EEVEE는 지원하지 않는다 | 5.2 매뉴얼(읽음) |
| Light tree의 약점 | 사용자 지정 감쇠, 광선 가시성, 텍스처를 쓴 조명은 light tree가 고려하지 못해 노이즈가 늘 수 있다 | 5.2 매뉴얼 Sampling(읽음) |
| Light group | 빛별로 따로 계산된 Combined 패스를 준다. 합성에서 더하면 전체가 되고, 다시 렌더하지 않고 빛별 색과 세기를 바꿀 수 있다. Cycles 전용 | 5.2 매뉴얼 Passes(읽음), 5.2.2에서 확인 |

**정리(작업자 판단)**: 어두운 무대에서는 HDRI를 주광으로 쓰지 않는다. 배경이 검어야 하고 림의 방향을 정해야 하기 때문이다. 면광원으로 형태를 만들고, 금속과 도장의 반사가 비어 보일 때만 HDRI를 낮은 세기로, 카메라에는 안 보이게 깐다. HDRI는 Z축으로 돌려 밝은 곳이 물체의 원하는 면에 비치게 한다. 고보는 면광원의 노드에 무늬 텍스처를 넣거나, 광원 앞에 구멍 난 판을 두어 만든다. 뒤쪽은 light tree의 약점 때문에 노이즈가 늘 수 있다.

**색온도 대비**: Blender 5.2의 조명에는 `use_temperature`와 `temperature`가 있다(5.2.2에서 확인, 800~20000K, 기본 6500K). 3200K로 두면 `temperature_color`가 (1.68, 0.87, 0.33)으로 나온다. 따뜻한 쪽과 차가운 쪽을 나누는 것은 자동차 광고 세트에서도 쓰는 방법이다(Bennett). 얼마나 벌릴지에 대한 숫자를 준 출처는 없다.

## 3. 공기와 깊이

| 주제 | 내용 | 출처 |
|---|---|---|
| 월드 볼륨 | 월드에 볼륨을 넣으면 월드 표면과 태양광이 듣지 않는다. 안개에는 장면을 감싸는 볼륨 물체가 낫고, 그 크기가 산란과 흡수의 양을 정한다 | 5.2 매뉴얼 World(읽음) |
| 5.0의 볼륨 | 기본 알고리즘이 null scattering으로 바뀌었다. 편향이 없고 겹친 볼륨의 깍두기 흔적이 없으며 step size 설정이 필요 없다. 다만 노이즈가 더 많을 수 있다 | 5.0 릴리스 노트(읽음), 5.2 매뉴얼(읽음) |
| Cycles 볼륨은 느리다 | 볼륨을 EEVEE로 렌더해 Cycles 결과 위에 얹는 방법을 쓴다 | BlenderNation, Martin Klekner(읽음) |
| 따로 렌더하기 | 단단한 물체를 홀드아웃으로 두고 볼륨만 따로 렌더하면 낮은 표본에서도 디노이즈가 잘 된다 | Blender Artists(검색 요약) |
| 필요한 곳에만 | 장면 전체가 아니라 화면에서 필요한 곳에만 볼륨을 둔다 | Volume Forge 소개(검색 요약, 판매 글) |
| 알파 판 | 물리적으로 맞는 볼륨 대신 알파 무늬가 있는 판으로 빛줄기를 흉내 낸다 | Creative Shrimp(읽음) |
| Mist 패스 | 카메라에서 가까운 면까지의 거리를 0~1로 준다. 먼 물체를 흐리게 할 때 쓴다. Z 패스는 피사계 심도나 모션 블러와 함께 쓰면 노이즈가 있다 | 5.2 매뉴얼(읽음) |
| 합성의 Sun Beams | Glare 노드의 한 종류다. 매뉴얼은 완전한 볼륨 조명이 "꽤 힘들고 오래 걸린다"고 적었다. 확산 반사는 입력에서 빼고 가장 밝은 곳만 남겨 빛줄기를 만든 뒤 더한다 | 5.2 매뉴얼 Glare(읽음) |
| 젖은 바닥 | 효과의 90%는 고르지 않은 거칠기다 | Creative Shrimp(읽음) |
| 바닥의 단단한 그림자 | 멀리 둔 스폿의 단단한 그림자가 차를 바닥에 붙인다 | Lightmap(읽음) |
| 먼지 입자 | 투명한 판으로 입자를 흉내 내는 방법이 있다 | Creative Shrimp(읽음, 한 줄 언급) |

**이 컴퓨터에서 잰 것**(정육면체 하나, 1080×1920, 최대 512 표본, 노이즈 한계 0.005, OptiX, OIDN GPU):

| 조건 | 프레임 시간 |
|---|---|
| 기본 | 4.0~4.6초 |
| 8×8×4m 볼륨 상자(Volume Scatter, 밀도 0.03) 추가 | 15.8초 |
| 같은 볼륨, 볼륨 바운스 1 | 22.6초 |
| 모션 블러(회전하는 정육면체) | 4.3초 |
| Bevel 셰이더 노드 | 4.5초 |

볼륨 상자를 넣자 화면 밝기의 중앙값이 0.018에서 0.31로 올랐다(표시 변환 뒤). 검은 무대가 회색이 됐다. 밀도는 임의로 넣은 값이다. 실제 컷에서 몇 배가 되는지는 재지 않았다. 처음 Bevel 노드를 쓴 렌더는 58.8초가 걸렸고 다시 돌리니 4.5초였다. 커널을 처음 올리는 시간으로 보이나 확인하지 않았다.

## 4. 조명의 일부로서의 재질

| 주제 | 내용 | 출처 |
|---|---|---|
| 모서리 | "모서리를 살짝 둥글리면 현실에서도 보이는 스페큘러 하이라이트가 잡힌다." Bevel 셰이더 노드는 형상을 바꾸지 않고 음영만 바꾼다. 매우 비싸서 렌더가 20% 느려질 수 있으니 굽기와 정지 화면에 권한다. Bevel 모디파이어가 더 빠르지만 지저분한 형상에서 실패한다. 표본 기본값은 4다 | 5.2 매뉴얼 Bevel Node(읽음) |
| 깨끗한 표면은 없다 | 가장 깨끗한 표면에도 흠집과 지문이 있다. 거칠기 맵으로 반사를 깨뜨려야 한다 | Blender Guru 강의 소개(검색 요약), 업계 글 여럿(요약) |
| 생기 없는 재질 | 균일한 텍스처는 깊이가 없어 죽어 보인다 | 건축 시각화 글(검색 요약) |
| 색 값의 상한 | 재질 색 성분을 1.0 가까이 두지 않는다. 0.8 이하로 두고 빛을 더 밝게 한다. 높은 값은 바운스마다 빛이 줄지 않아 노이즈를 만든다 | 5.2 매뉴얼 Reducing Noise(읽음) |
| Coat | 클리어코트, 래커, 자동차 도장용이다. Weight는 물리 기반 재질에서 보통 0이나 1이다. Coat Normal로 거친 표면 위의 매끈한 코팅을 만든다 | 5.2 매뉴얼 Principled(읽음) |
| 자동차 도장 | 밑칠의 거칠기를 높이고(0.4~0.6) 그 위에 코트를 올린다. 입자는 Voronoi로 법선을 흩뜨려 만든다 | 판매 셰이더 문서(검색 요약, 한 사람의 값) |
| 이방성 | 값이 클수록 하이라이트가 탄젠트 방향으로 늘어난다. Cycles 전용이다. Glossy BSDF와 비교하면 방향이 90° 돌아 있어 Rotation에 0.25를 더해 맞춘다 | 5.2 매뉴얼(읽음) |
| 이방성의 쓰임 | 헤어라인 금속, 냄비, 싱크대처럼 갈아 낸 표면 | Blender Guru(읽음) |
| 금속의 가장자리 색 | Specular Tint가 금속의 가장자리를 물들여 금, 구리 같은 복소 굴절률을 흉내 낸다. Metallic BSDF 노드는 물리적 굴절률(IOR, Extinction)과 F82 방식을 고를 수 있다 | 5.2 매뉴얼(읽음), 5.2.2에서 노드 확인 |
| Multiscatter GGX | 미세면 사이의 다중 산란을 넣어 거친 표면이 지나치게 어두워지는 것을 막는다. GGX가 더 빠르다 | 5.2 매뉴얼(읽음) |
| Sheen | 미세한 섬유를 흉내 낸다. 임의의 재질 위의 먼지에도 쓸 수 있다 | 5.2 매뉴얼(읽음) |
| 박막 간섭 | Principled와 Metallic BSDF가 박막 무지갯빛을 지원한다 | 4.2, 5.0 릴리스 노트(읽음) |
| 발광 메시의 표본 | 조명 구실을 하는 발광 메시는 Multiple Importance를 켠다. 조금 빛나는 장식은 끄면 노이즈가 준다 | 5.2 매뉴얼 Reducing Noise(읽음) |
| Poly Haven 텍스처 | 사진 기반이고, 확산·거칠기·법선(OpenGL)·변위·AO·금속 맵으로 이루어진다. 최소 8192 해상도 | Poly Haven 문서(검색 요약) |

**흠을 섞는 법(작업자 판단, 출처의 원칙을 노드로 옮긴 것)**: 기본 거칠기 값에 흠 맵(지문, 얼룩, 미세 흠집)을 더하거나 범위를 다시 잡아 섞는다. 흠 맵은 Non-Color로 읽는다. 물체 크기에 맞는 배율을 쓴다(Poly Haven은 실제 치수를 기록한다). 프로시저 노이즈만으로도 "한 값"은 피할 수 있다. 어느 정도가 맞는지 숫자를 준 출처는 없다.

**피하 산란**: 무대의 물체(금속, 도장, 유리, 칩)에는 거의 해당이 없다. 로봇의 고무와 플라스틱 덮개 정도다. Principled의 Subsurface Weight는 보통 0이나 1이다(매뉴얼).

## 5. 색 관리와 마무리

### 뷰 변환 (5.2 매뉴얼, 읽음. 목록은 5.2.2에서 확인)

| 뷰 | 매뉴얼의 설명 |
|---|---|
| Standard | 표시 장치용 변환만 한다. 비사실적 결과나 이미 룩이 입혀진 영상 편집용 |
| AgX | Filmic을 개선한 톤 매핑. 16.5스톱의 범위. 과다 노출된 색의 채도를 빼 필름의 반응을 흉내 낸다. 4.0부터 새 파일의 기본값 |
| Filmic | "폐기 예정이며 AgX가 대체한다" |
| Khronos PBR Neutral | 재질의 기본색이 출력에 최대한 그대로 나오게 한다. 노출이 잘 맞고 HDR 값이 작은 하이라이트에만 있는 제품 사진용 |
| ACES 1.3 / 2.0 | 영화·TV의 표준. 2.0은 더 중립적이고 중간 톤 대비가 낮고 하이라이트가 더 완만하다. 5.0에서 들어왔다 |
| False Color | 밝기를 색으로 보여 노출을 맞추게 돕는다 |

False Color의 색 구간(매뉴얼): 0.0001~0.05% 파랑, 0.05~0.5% 청록 쪽 파랑, 0.5~5% 청록, 5~16% 녹청, 16~22% 회색, 22~35% 연두, 35~55% 노랑, 55~80% 주황, 80~97% 빨강, 그 위 흰색(잘림), 그 아래 검정(잘림).

- Look: AgX에는 Punchy, Greyscale, Very High Contrast부터 Very Low Contrast까지 일곱 단계의 대비가 있다(5.2.2에서 확인). 어느 것이 좋다는 권고는 매뉴얼에 없다.
- Exposure: `view_settings.exposure`는 뷰 변환 앞에서 2^exposure를 곱한다. `cycles.film_exposure`는 데이터 자체를 바꾼다(매뉴얼).
- 물리적인 조명 값을 넣으면 예상보다 훨씬 밝거나 어둡게 나온다. 눈은 적응하고 렌더 엔진은 적응하지 않기 때문이다. 노출로 맞춘다(매뉴얼).
- AgX를 쓸 때는 주제가 중간 회색에 오도록 노출부터 잡고 대비를 만진다는 조언이 있다(darktable 포럼, 검색 요약, 한 사람의 의견).
- Blender Guru의 옛 글은 가짜 같아 보이는 원인으로 좁은 다이내믹 레인지를 들고 Filmic을 권했다. 지금은 AgX가 그 자리를 잇는다.
- 5.0부터 작업 색 공간을 고를 수 있다(기본 Linear Rec.709, 그 밖에 Linear Rec.2020, ACEScg). sRGB 영상으로 내보내는 우리에게 바꿀 이유가 있다는 근거는 찾지 못했다.

**작업자 판단**: 우리 화면은 어두운 무대에 작은 강한 하이라이트가 있다. Khronos PBR Neutral이 전제하는 "노출이 고른 제품 사진"과 다르다. AgX를 기본으로 두고 Look으로 대비를 고른다. ACES 2.0과 견준 적은 없다.

### 합성 노드의 변화 (4.5~5.2)

| 버전 | 바뀐 것 | 출처 |
|---|---|---|
| 4.5 | 대부분의 노드 옵션이 입력 소켓이 됐다. 옛 옵션 속성은 폐기 예정. Glare에 Clamp 입력 추가. Value, Color Ramp, Mix Color, Map Range, Math 등은 폐기 예정이고 같은 이름의 셰이더 노드를 쓴다 | 4.5 릴리스 노트(읽음) |
| 5.0 | 합성 노드 트리가 독립 데이터 블록이 됐다. Composite 노드가 없어지고 Group Output을 쓴다. Sun Beams 노드가 Glare의 한 종류로 들어갔다. Convolve, Convert to Display 노드 추가. Gamma, Texture 노드 삭제 | 5.0 릴리스 노트(읽음) |
| 5.2 | 아래 표 | 5.2.2에서 확인 |

5.2.2에서 확인한 것:

- `scene.node_tree`가 없다. `scene.compositing_node_group`에 `CompositorNodeTree` 노드 그룹을 넣는다.
- `CompositorNodeComposite`, `CompositorNodeMixRGB`가 없다. 출력은 `NodeGroupOutput`이고, 섞기는 합성 트리에서도 `ShaderNodeMix`를 쓴다.
- Glare의 설정은 전부 입력 소켓이다. Type은 `Bloom, Ghosts, Streaks, Fog Glow, Simple Star, Sun Beams, Kernel`, Quality는 `High, Medium, Low`. 기본 Type이 `Streaks`이므로 반드시 바꾼다. 출력은 `Image, Glare, Highlights`.
- Lens Distortion의 입력은 `Type(Radial, Horizontal), Distortion, Dispersion, Jitter, Fit`. 색수차는 `Dispersion`이다.
- 선명화 전용 노드는 없다. Filter 노드의 Type에 `Box Sharpen, Diamond Sharpen`이 있다.
- 비네트와 필름 그레인 전용 노드는 없다. Ellipse Mask와 Blur, 흰 노이즈 텍스처로 조립해야 한다.
- Color Balance의 Type은 `Lift/Gamma/Gain, Offset/Power/Slope (ASC-CDL), White Point`.
- `Material.use_nodes`와 `World.use_nodes`는 쓰면 "6.0에서 제거 예정" 경고가 나온다.

Glare의 종류(매뉴얼): Bloom은 눈과 렌즈 안의 산란으로 생기는 부드러운 빛 번짐이다. Fog Glow는 "Bloom의 더 물리적으로 정확한 판"이고 계산이 더 든다. Strength가 1보다 작으면 원본과 섞는다. Size 1은 효과가 화면 전체를 덮는다.

### 얼마나가 지나친가

- 초점 흐림은 현실감을 주지만 지나치면 장면이 미니어처처럼 보인다(Blender Guru, 읽음).
- 렌즈 왜곡과 색수차는 전문 사진에서는 대개 없애는 것이다(Blender Guru, 읽음). 넣는다면 아주 조금이다.
- 블룸, 색수차, 비네트, 그레인은 현실감에 쓰이지만 잘못 맞추면 싸구려로 보인다(검색 요약, 여러 글의 공통 의견).
- 디노이저와 클램프가 하이라이트를 깎으면 블룸이 붙을 곳이 없어진다. 매뉴얼은 클램프를 너무 낮추면 "블룸이나 글레어 같은 카메라 효과에 쓸 하이라이트"가 사라진다고 적었다.
- 얼마가 "조금"인지 숫자를 준 출처는 없다.

### Blender에서 할 것과 Remotion에서 할 것 (작업자 판단)

| 효과 | 어디서 | 까닭 |
|---|---|---|
| 뷰 변환, 노출, Look | Blender | 선형 데이터에서 해야 한다 |
| 블룸(Glare) | Blender | 1을 넘는 선형 값이 있어야 한다. 8비트로 내보낸 뒤에는 밝은 값이 잘려 있다 |
| 피사계 심도, 모션 블러 | Blender(렌더) | 매뉴얼은 EEVEE 패스에서는 합성 노드로 흉내 낼 수 있다고 하지만, Cycles에서는 렌더가 직접 한다 |
| 색수차, 렌즈 왜곡 | Blender, 3D 층에만 | Remotion에서 걸면 글자까지 번진다 |
| 비네트, 그레인, 최종 색 보정 | Remotion, 화면 전체에 | 글자와 3D가 같은 화면으로 묶인다. 3D에만 그레인이 있으면 글자가 따로 떠 보인다. 그레인은 영상 압축에서 뭉개질 수 있다(확인하지 않음) |
| 선명화 | 하지 않거나 최소 | 디노이즈된 CG를 선명화하면 윤곽이 딱딱해진다는 것은 일반론이고 출처는 찾지 못했다 |

## 6. 8GB 안에서의 Cycles 품질

| 주제 | 내용 | 출처 |
|---|---|---|
| 기본값 | 표본 4096, 노이즈 한계 0.01, 적응 표본 켜짐, 디노이즈 켜짐(OIDN, Albedo+Normal, Accurate), 간접 클램프 10, 직접 클램프 0(끔), 바운스 전체 12·확산 4·광택 4·투과 12·볼륨 0·투명 8, Filter Glossy 1.0 | 5.2.2에서 확인 |
| 노이즈 한계 | 보통 0.1에서 0.001 사이다. 낮을수록 품질이 좋고 오래 걸린다. 0이면 표본 수에 맞춰 자동으로 잡는다 | 5.2 매뉴얼(읽음) |
| 디노이저 | OIDN이 "보통 가장 높은 품질"이다. OptiX는 OIDN의 GPU 가속이 안 되는 옛 NVIDIA 카드에서 쓴다 | 5.2 매뉴얼(읽음) |
| 디노이즈 입력 | 패스를 많이 줄수록 낫다. None은 낮은 표본에서 디테일을 뭉갠다 | 5.2 매뉴얼(읽음) |
| Prefilter | None은 디테일을 가장 많이 남기지만 보조 패스에 노이즈가 없어야 한다. Accurate가 Fast보다 디테일이 낫다 | 5.2 매뉴얼(읽음) |
| OIDN의 GPU 사용 | CPU보다 훨씬 빠르지만 GPU 메모리를 더 쓴다. 큰 장면에서는 끌 수 있다. RTX 전 기종이 지원한다 | 5.2 매뉴얼(읽음) |
| OIDN은 시간축을 보지 않는다 | 프레임마다 따로 디노이즈하므로 표본이 적으면 프레임 사이에 얼룩이 흔들린다. 해법은 표본을 늘리는 것이다 | 포럼 글 여럿(검색 요약) |
| 애니메이션 시드 | 매뉴얼은 애니메이션에서 시드를 프레임마다 바꾸라고 권한다. 바뀌는 노이즈가 덜 눈에 띈다 | 5.2 매뉴얼(읽음) |
| 표본 무늬 | 기본은 Blue-Noise다. 낮은 표본에서 더 매끈해 보인다. Scrambling Distance와 함께 쓸 수 없다 | 5.2 매뉴얼(읽음), 4.2 릴리스 노트(읽음) |
| 간접 클램프 | 반딧불(firefly)을 줄이되 밝은 곳도 함께 어두워진다. 카메라에 직접 보이는 하이라이트를 지키려면 간접만 클램프한다 | 5.2 매뉴얼(읽음) |
| 커스틱 | 반딧불의 흔한 원인이다. 끄면 빛이 빠진다. Filter Glossy가 "거친 반사 너머로 보이는 날카로운 반사"의 노이즈를 줄인다 | 5.2 매뉴얼(읽음) |
| 바운스 | 확산은 적어도 되고 광택은 조금 더, 유리는 가장 많이 필요하다 | 5.2 매뉴얼(읽음) |
| 가까운 광원의 반딧불 | 거리가 0에 가까우면 세기가 무한대로 간다. Light Falloff 노드의 Smooth가 줄인다 | 5.2 매뉴얼(읽음) |
| Path guiding | CPU 전용이다. GPU 렌더에는 쓸 수 없다 | 5.2 매뉴얼(읽음) |
| Persistent Data | 렌더 데이터를 메모리에 남겨 애니메이션과 다시 렌더가 빨라진다. 메모리를 더 쓴다 | 5.2 매뉴얼(읽음) |
| 텍스처 메모리 | 8K, 4K, 2K, 1K 텍스처는 각각 256MB, 64MB, 16MB, 4MB를 쓴다 | 5.2 매뉴얼 GPU Rendering(읽음) |
| 텍스처 크기 제한 | Simplify의 Texture Size Limit가 텍스처를 자동으로 줄인다 | 5.2 매뉴얼(읽음) |
| 텍스처 캐시 | 5.2에 들어왔다. 필요한 타일과 해상도만 읽는 `.tx` 파일로 메모리와 시작 시간을 줄인다 | 5.2 릴리스 노트(읽음), 매뉴얼(읽음) |
| 메모리 초과 | GPU 메모리가 차면 시스템 메모리를 쓴다. 느려지지만 대개 CPU 렌더보다는 빠르다 | 5.2 매뉴얼(읽음) |
| 타일 | 기본 2048이다. 메모리가 모자라면 1024나 512로 낮춘다 | 5.2 매뉴얼(읽음) |
| 5.1의 속도 | GPU 렌더가 여러 장면에서 5~10% 빨라졌다 | 5.1 릴리스 노트(읽음) |
| 모션 블러의 한계 | 조명의 움직임은 모션 블러에 반영되지 않는다. 카메라와 조명을 함께 움직이면 틀린 블러가 생긴다 | 5.2 매뉴얼(읽음) |
| OptiX 드라이버 | 5.2는 드라이버 575 이상이 필요하다 | 5.2 매뉴얼(읽음) |

**인스턴싱**: 코인 더미, 배터리 컨테이너, 공장 기둥처럼 같은 물체를 여러 번 쓸 때는 메시 데이터를 공유하는 복제(링크 복제나 컬렉션 인스턴스)가 메모리를 아낀다는 것은 일반 지식이다. 5.2 릴리스 노트는 형상 메모리를 Blender와 더 많이 공유해 줄였다고 했다. 얼마나 아끼는지 잰 출처는 읽지 않았다.

### EEVEE (5.2 매뉴얼의 한계 목록, 읽음)

- 조명 노드 트리를 지원하지 않는다. 고보와 그러데이션 광원이 안 된다.
- 면광원의 Spread를 지원하지 않는다.
- 화면 공간 효과는 화면 안에 있는 것만 본다. 화면 가장자리에서 반사가 사라지고, 가려진 물체는 반사에 나오지 않는다.
- 볼륨은 카메라 광선에만 렌더된다. 반사와 굴절에는 나오지 않는다. 단일 산란만 한다.
- 모든 BSDF가 근사라서 Cycles와 조금씩 다르다.
- 발광 메시의 light linking은 Cycles에서만 된다.

우리 컷은 "광택 바닥과 광택 물체에 화면 밖의 광원이 비치는 것"이 핵심이다. EEVEE의 화면 공간 한계가 바로 그 지점이다. 레이 트레이싱 옵션(`eevee.use_raytracing`)이 얼마나 메우는지는 시험하지 않았다. 볼륨만 EEVEE로 렌더해 얹는 방법은 3절의 출처(BlenderNation)가 권한다.

## 7. 아마추어 같거나 AI 같아 보이는 표시와 전문가의 확인법

| 표시 | 근거 |
|---|---|
| 고르게 평평한 빛, 그림자 없음 | Blender Guru, Creative Shrimp, 건축 시각화 글 |
| 전부 같은 밝기라 시선이 갈 곳이 없음 | Blender Guru |
| 림이 없어 윤곽이 배경에 녹음 | 검은 제품 촬영 글 둘, Creative Shrimp |
| 금속이 전부 흰 반사거나 전부 검은 반사 | Light: Science & Magic 강의 요약 |
| 한 값의 거칠기, 너무 깨끗한 표면 | Blender Guru 강의 소개, 업계 글 |
| 날카로운 모서리(하이라이트가 안 잡힘) | Blender 매뉴얼 |
| 흰 빛만 씀 | Blender Guru |
| 지나친 블룸, 색수차, 초점 흐림 | Blender Guru, 업계 글 |
| 물체가 바닥에서 떠 보임(접지 그림자 없음) | Lightmap이 "바닥 그림자가 차를 심는다"고 한 것의 반대. 이 표시를 직접 든 출처는 찾지 못했다 |
| 좁은 다이내믹 레인지(Standard 뷰로 하이라이트가 탐) | Blender Guru, Blender 4.0 릴리스 노트 |

"AI 같아 보인다"를 조명 용어로 풀어 준 출처는 찾지 못했다. 위 표는 "아마추어 CG"에 관한 것이다. AI 그림의 표시와 겹친다고 보는 것은 작업자의 가설이다.

**확인법**

- **False Color 뷰**: 노출을 색으로 본다(매뉴얼). 위의 구간표로 "주제가 어느 구간에 있는가"를 숫자로 말할 수 있다.
- **스폿 측광**: 자동차는 반사의 노출을 잰다(Bennett). 렌더에서는 반사 영역의 픽셀 값을 읽는 것이 같은 일이다.
- **빛별 패스**: Light group으로 빛 하나만 켠 화면을 다시 렌더하지 않고 본다(매뉴얼). 각 빛이 하는 일이 없으면 뺀다. 제품 사진가들도 빛을 하나씩 켜서 각자의 몫을 본다(Visual Education).
- **클레이 렌더**: 재질을 전부 중간 회색으로 바꿔 빛의 균형만 본다(검색 요약). `view_layer.material_override`가 이 일을 한다(5.2.2에서 속성 확인).
- **흑백 값 확인**: 색을 빼고 밝기만 본다. AgX에 `AgX - Greyscale` Look이 있다(5.2.2에서 확인). 이 방법을 권하는 원문은 읽지 못했다(검색 결과에 제목만 있었다).
- **손전등**: 세트에서 반사에 문제가 있는 곳을 찾는 방법이다(Bennett). CG에서는 작은 밝은 발광 구를 움직여 어느 면이 무엇을 비추는지 보는 것이 같은 일이다(작업자의 옮김).

## 8. bpy 구현 메모 (Blender 5.2.2에서 실행해 확인)

### 장치와 Cycles

```python
import bpy, math
s = bpy.context.scene
s.render.engine = 'CYCLES'          # 가능한 값: BLENDER_EEVEE, BLENDER_WORKBENCH, CYCLES
prefs = bpy.context.preferences.addons['cycles'].preferences
prefs.compute_device_type = 'OPTIX'
prefs.get_devices()
for d in prefs.devices:
    d.use = (d.type == 'OPTIX')     # CPU와 CUDA 항목은 끈다
s.cycles.device = 'GPU'

c = s.cycles
c.samples = 512                      # 값은 예시다. 컷마다 정한다
c.use_adaptive_sampling = True
c.adaptive_threshold = 0.01          # 매뉴얼: 보통 0.1~0.001
c.use_denoising = True
c.denoiser = 'OPENIMAGEDENOISE'      # 또는 'OPTIX'
c.denoising_input_passes = 'RGB_ALBEDO_NORMAL'
c.denoising_prefilter = 'ACCURATE'   # NONE, FAST, ACCURATE
c.denoising_use_gpu = True           # 기본은 False다
c.sample_clamp_direct = 0.0          # 0은 끔. 직접 하이라이트를 지킨다
c.sample_clamp_indirect = 10.0       # 기본값
c.blur_glossy = 1.0                  # Filter Glossy
c.caustics_reflective = False
c.caustics_refractive = False
c.max_bounces, c.diffuse_bounces, c.glossy_bounces = 8, 3, 4   # 예시
c.transmission_bounces, c.volume_bounces = 4, 0
c.use_animated_seed = True
s.render.use_simplify = True         # 텍스처 크기 제한은 매뉴얼의 Simplify 패널에 있다
c.texture_limit_render = '2048'      # OFF,128,...,8192
s.render.use_persistent_data = True
s.render.use_motion_blur = True      # 모션 블러는 scene.render에 있다
s.render.motion_blur_shutter = 0.5   # 기본값
```

- `c.sampling_pattern`: `AUTOMATIC, TABULATED_SOBOL, BLUE_NOISE`.
- `c.use_guiding`은 속성은 있으나 GPU에서는 듣지 않는다(매뉴얼).
- `c.volume_biased`가 False면 null scattering이다. `volume_step_rate`와 `volume_max_steps`는 `volume_biased`가 True일 때만 쓰인다.
- `texture_limit_render`가 `use_simplify` 없이 듣는지는 시험하지 않았다.

### 색 관리

```python
vs = s.view_settings
vs.view_transform = 'AgX'    # Standard, ACES 1.3, ACES 2.0, Khronos PBR Neutral, AgX, Filmic, Filmic Log, False Color, Raw
vs.look = 'AgX - Medium High Contrast'   # None, AgX - Punchy, AgX - Greyscale, AgX - Very High Contrast ... AgX - Very Low Contrast
vs.exposure = 0.0            # 스톱. 뷰 변환 앞에서 2^exposure
s.display_settings.display_device = 'sRGB'
```

Look의 목록은 뷰 변환에 따라 달라진다. 뷰 변환을 먼저 정한다. 문자열이 틀리면 `TypeError`가 가능한 값을 알려 준다.

### 면광원

```python
def area(name, loc, rot_deg, sx, sy, watts, kelvin, spread_deg=180):
    d = bpy.data.lights.new(name, 'AREA')
    d.shape = 'RECTANGLE'            # SQUARE, RECTANGLE, DISK, ELLIPSE
    d.size, d.size_y = sx, sy        # 미터
    d.energy = watts                 # 복사 출력(W). 전구의 소비 전력이 아니다
    d.use_temperature = True
    d.temperature = kelvin           # 800~20000, 기본 6500
    d.spread = math.radians(spread_deg)   # 작을수록 격자 단 소프트박스
    d.normalize = True               # False면 크기에 비례해 총 출력이 는다
    d.exposure = 0.0                 # 2^exposure를 곱한다. 스톱 단위로 조절할 때 편하다
    o = bpy.data.objects.new(name, d)
    o.location = loc
    o.rotation_euler = [math.radians(a) for a in rot_deg]
    bpy.context.scene.collection.objects.link(o)
    return o
```

- 매뉴얼의 출력 표: 촛불 0.05W, 800lm LED 전구 2.1W, 1000lm 전구 2.9W, 자동차 전조등(5000lm) 22W(스폿, 125°). 태양은 W/m²이고 맑은 하늘이 1000이다. 이 값을 쓰면 노출로 맞춰야 한다.
- `d.cycles.use_multiple_importance_sampling`(기본 True), `d.cycles.max_bounces`, `d.cycles.is_portal`이 있다.
- 광선 가시성은 물체에 있다: `o.visible_camera, o.visible_diffuse, o.visible_glossy, o.visible_transmission, o.visible_volume_scatter, o.visible_shadow`.
- `d.diffuse_factor`, `d.specular_factor`는 Cycles 렌더에 영향이 없었다.

### 그러데이션 광원

```python
d = light.data
d.use_nodes = True
nt = d.node_tree                       # 기본 노드: ShaderNodeEmission → ShaderNodeOutputLight
em = next(n for n in nt.nodes if n.type == 'EMISSION')
geo = nt.nodes.new('ShaderNodeNewGeometry')
sep = nt.nodes.new('ShaderNodeSeparateXYZ')
ramp = nt.nodes.new('ShaderNodeMapRange')      # 0~1을 원하는 세기 범위로
nt.links.new(geo.outputs['Parametric'], sep.inputs[0])
nt.links.new(sep.outputs['X'], ramp.inputs['Value'])   # X는 광원의 한 변을 따라 0→1
nt.links.new(ramp.outputs['Result'], em.inputs['Strength'])
```

시험에서 `Parametric`의 X를 Strength에 바로 넣었을 때 반사가 한쪽 끝에서 반대쪽 끝까지 고르게 밝아졌다. Map Range를 끼운 꼴은 실행만 확인했고 값은 재지 않았다. 매뉴얼은 텍스처가 있는 조명을 light tree가 고려하지 못한다고 했으니 노이즈를 본다.

### Light linking과 light group

```python
col = bpy.data.collections.new('LL_hero')     # 장면에 링크하지 않아도 된다
col.objects.link(hero)
rim.light_linking.receiver_collection = col   # 이 빛은 hero만 비춘다
rim.light_linking.blocker_collection = bpy.data.collections.new('LL_rim_blockers')  # 비어 있으면 아무것도 이 빛을 가리지 않는지는 시험하지 않았다
col.collection_objects[0].light_linking.link_state = 'INCLUDE'   # INCLUDE, EXCLUDE

vl = bpy.context.view_layer
vl.lightgroups.add(name='key'); vl.lightgroups.add(name='rim')
key.lightgroup = 'key'; rim.lightgroup = 'rim'
# 렌더 뒤 Render Layers 노드에 'Combined_key', 'Combined_rim' 출력이 생긴다
```

### 월드: 반사 전용 HDRI

```python
w = bpy.data.worlds.new('World'); s.world = w
w.use_nodes = True                     # 5.2에서는 폐기 예정 경고가 나온다
nt = w.node_tree
bg = next(n for n in nt.nodes if n.type == 'BACKGROUND')
tc = nt.nodes.new('ShaderNodeTexCoord')
mp = nt.nodes.new('ShaderNodeMapping')
env = nt.nodes.new('ShaderNodeTexEnvironment')
env.image = bpy.data.images.load(hdr_path)
mp.inputs['Rotation'].default_value[2] = math.radians(90)   # Z축으로 돌린다
nt.links.new(tc.outputs['Generated'], mp.inputs['Vector'])
nt.links.new(mp.outputs['Vector'], env.inputs['Vector'])
nt.links.new(env.outputs['Color'], bg.inputs['Color'])
bg.inputs['Strength'].default_value = 0.2    # 예시
w.cycles_visibility.camera = False     # camera, diffuse, glossy, transmission, shadow, scatter
w.cycles_visibility.diffuse = False    # 반사에만 쓴다
```

노드 연결은 실행해 확인했다. `cycles_visibility.diffuse = False`의 렌더 결과는 재지 않았다.

### 재질

Principled BSDF의 입력 이름(5.2.2): `Base Color, Metallic, Roughness, IOR, Alpha, Thin Wall, Normal, Diffuse Roughness, Subsurface Weight, Subsurface Radius, Subsurface Scale, Subsurface IOR, Subsurface Anisotropy, Specular IOR Level, Specular Tint, Anisotropic, Anisotropic Rotation, Tangent, Transmission Weight, Coat Weight, Coat Roughness, Coat IOR, Coat Tint, Coat Normal, Sheen Weight, Sheen Roughness, Sheen Tint, Emission Color, Emission Strength, Thin Film Thickness, Thin Film IOR`. 옛 이름(`Clearcoat`, `Subsurface`, `Transmission`, `Emission`)은 없다. `distribution`은 `GGX, MULTI_GGX`.

```python
# 거칠기를 한 값으로 두지 않는다
nz = nt.nodes.new('ShaderNodeTexNoise')            # 출력 이름은 'Factor'와 'Color'다('Fac'이 아니다)
mr = nt.nodes.new('ShaderNodeMapRange')
mr.inputs['To Min'].default_value, mr.inputs['To Max'].default_value = 0.08, 0.30   # 예시
nt.links.new(nz.outputs['Factor'], mr.inputs['Value'])
nt.links.new(mr.outputs['Result'], bsdf.inputs['Roughness'])

# 모서리: 모디파이어가 먼저다
bev = obj.modifiers.new('bevel', 'BEVEL'); bev.width = 0.02; bev.segments = 3   # 값은 예시
# 형상이 지저분해 모디파이어가 깨질 때만 셰이더 노드
bn = nt.nodes.new('ShaderNodeBevel'); bn.inputs['Radius'].default_value = 0.02; bn.samples = 4
nt.links.new(bn.outputs['Normal'], bsdf.inputs['Normal'])
```

그 밖에 확인한 노드: `ShaderNodeBsdfMetallic`(입력 `Base Color, Edge Tint, IOR, Extinction, Roughness, Anisotropy, Rotation, Tangent, Thin Film Thickness, Thin Film IOR`, `fresnel_type`은 `PHYSICAL_CONDUCTOR, F82`), `ShaderNodeBlackbody`, `ShaderNodeLightFalloff`(출력 `Quadratic, Linear, Constant`, 입력 `Smooth`), `ShaderNodeTexGabor`, `ShaderNodeVolumeScatter`(`phase`: `HENYEY_GREENSTEIN, FOURNIER_FORAND, DRAINE, RAYLEIGH, MIE`), `ShaderNodeAmbientOcclusion`.

### 합성

```python
ng = bpy.data.node_groups.new('Finish', 'CompositorNodeTree')
s.compositing_node_group = ng
ng.interface.new_socket(name='Image', in_out='OUTPUT', socket_type='NodeSocketColor')
rl = ng.nodes.new('CompositorNodeRLayers')
gl = ng.nodes.new('CompositorNodeGlare')
ld = ng.nodes.new('CompositorNodeLensdist')
out = ng.nodes.new('NodeGroupOutput')
gl.inputs['Type'].default_value = 'Bloom'        # 기본은 'Streaks'
gl.inputs['Quality'].default_value = 'High'
gl.inputs['Threshold'].default_value = 1.0       # 기본값
gl.inputs['Strength'].default_value = 0.3        # 예시. 1보다 작으면 원본과 섞는다
gl.inputs['Size'].default_value = 0.4            # 예시. 1이면 화면 전체
ld.inputs['Dispersion'].default_value = 0.01     # 예시
ng.links.new(rl.outputs['Image'], gl.inputs['Image'])
ng.links.new(gl.outputs['Image'], ld.inputs['Image'])
ng.links.new(ld.outputs['Image'], out.inputs[0])
s.render.use_compositing = True
s.render.compositor_device = 'GPU'               # CPU, GPU
```

이 트리로 `bpy.ops.render.render(write_still=True)`가 오류 없이 PNG를 썼다. 메뉴 소켓에 틀린 문자열을 넣으면 `TypeError`가 가능한 값을 알려 준다.

### 확인용 설정

```python
# 클레이 렌더
clay = bpy.data.materials.new('clay')            # 기본 Principled를 중간 회색으로
bpy.context.view_layer.material_override = clay
# False Color
s.view_settings.look = 'None'; s.view_settings.view_transform = 'False Color'
# 패스
vl.use_pass_mist = True                          # s.world.mist_settings.start, .depth, .falloff
vl.cycles.denoising_store_passes = True          # Noisy Image, Denoising Albedo, Denoising Normal
vl.use_pass_glossy_direct = True; vl.use_pass_diffuse_direct = True
```

## 규칙 후보

AI가 bpy 코드를 쓸 때 따를 수 있게 적었다. 각 규칙에 (가) 할 일, (나) 렌더한 정지 화면이나 숫자로 확인하는 법, (다) 출처를 붙였다. 확인법의 "통과 값"은 대부분 비워 두었다. 숫자를 준 출처가 없기 때문이다. 사용자가 좋다고 한 프레임을 재서 기준으로 삼아야 한다.

### 조명 설계

**R1. 광택 물체는 반사를 설계한다.**
(가) 조명을 놓기 전에 카메라에서 본 물체의 주요 면마다 "이 면이 무엇을 비추는가"를 정한다. 면광원은 그 면의 반사 방향에 둔다. 빛이 닿는지가 아니라 비치는지를 본다.
(나) 금속과 도장 재질의 물체 마스크 안에서 Glossy Direct 패스가 0이 아닌 픽셀의 비율을 잰다. 주요 면에 반사가 하나도 없으면 실패다. 손전등 방법: 작은 발광 구를 움직여 가며 어느 면에 비치는지 찍어 본다.
(다) Lightmap, Bennett ASC, Light: Science & Magic 강의 요약.

**R2. 머리 위에 큰 면광원 하나를 두고 물체의 선에 맞게 기울인다.**
(가) 물체보다 큰 직사각 면광원을 위에 두고, 반사가 어깨선과 윗면의 꺾이는 곳에 걸리도록 기울기와 위치를 정한다.
(나) 정지 화면에서 윗면과 어깨선에 끊기지 않은 긴 밝은 띠가 있는지 본다. 띠가 물체 밖으로 잘리거나 사각형 모서리가 반사에 그대로 보이면 광원을 키우거나 그러데이션을 입힌다(R3).
(다) Lightmap, Visual Education.

**R3. 큰 광원의 반사에는 그러데이션을 넣는다.**
(가) 주광과 큰 반사용 광원에는 노드로 한 방향 그러데이션을 입힌다(`Geometry → Parametric`). 균일한 면광원은 광택 면에 평평한 흰 사각형으로 비친다.
(나) 반사된 광원을 가로지르는 한 줄의 선형 픽셀 값을 읽는다. 끝에서 끝까지 값이 한 방향으로 변해야 한다. 시험에서 균일 광원은 7.8~8.0으로 평평했고 그러데이션 광원은 0.08에서 7.8까지 변했다.
(다) Visual Education(간접광으로 그러데이션을 만든다), Lightmap, Blender 매뉴얼(조명 노드), 5.2.2 시험.

**R4. 뒤쪽 양옆에 가는 띠 광원으로 윤곽을 딴다.**
(가) 물체 뒤, 카메라 반대편 좌우에 세로로 긴 면광원을 두고 물체 쪽을 향하게 한다. light linking으로 주인공 물체만 비추게 하고, 배경과 바닥으로 새지 않게 한다.
(나) 물체 마스크의 경계를 따라 안쪽 몇 픽셀의 밝기와 바깥쪽 배경의 밝기를 견준다. 안쪽이 더 밝은 경계의 비율을 보고한다. 림이 끊긴 구간(안쪽과 바깥쪽이 같은 구간)의 위치를 적는다. Light group으로 림만 켠 패스를 따로 본다.
(다) Visual Education 검은 제품, Lensvid, Creative Shrimp reverse key, Blender 매뉴얼 Light Linking.

**R5. 주광을 카메라 쪽에 두지 않는다.**
(가) 주광은 옆이나 뒤쪽 위에 둔다. 카메라 축에서 비추는 빛은 보조광으로만, 약하게 쓴다.
(나) 클레이 렌더(R20)에서 물체의 카메라 쪽 면에 그림자 쪽과 빛 쪽이 둘 다 있는지 본다. 물체 마스크 안의 밝기 분포가 한 덩어리가 아니라 두 덩어리 이상인지 히스토그램으로 본다.
(다) Creative Shrimp reverse key, Blender Guru(과하게 비추면 평평해진다).

**R6. 면이 바뀌면 밝기가 바뀐다.**
(가) 물체의 인접한 큰 면(위, 옆, 앞)이 서로 다른 밝기가 되게 광원의 위치와 세기를 잡는다. 보조광을 주광과 같은 세기로 두지 않는다.
(나) 클레이 렌더에서 큰 면마다 평균 밝기를 재서 표로 낸다. 인접한 두 면의 값이 같으면 실패다. 주광 쪽과 그림자 쪽의 차이를 스톱으로 적는다(2:1이 1스톱, 8:1이 3스톱).
(다) StudioBinder, Blender Guru. 스톱 수의 목표값은 출처가 없다.

**R7. 검은 곳은 두되 형태가 없는 검정은 두지 않는다.**
(가) 그림자 쪽 면에도 약한 반사나 가장자리 빛이 하나는 있게 한다. 금속을 전부 검게도, 전부 희게도 두지 않는다.
(나) False Color 뷰로 렌더해 물체 마스크 안에서 "아래 잘림(검정)" 구간에 든 픽셀의 비율을 잰다. 배경이 아니라 물체 안의 비율이다. 표시 변환 뒤 값으로는 물체 마스크 안의 1%와 5% 백분위 밝기를 적는다.
(다) Blender 매뉴얼 False Color 표, Light: Science & Magic 강의 요약.

**R8. 주인공이 가장 밝다.**
(가) 화면에서 가장 밝은 큰 영역이 주인공 물체에 있게 한다. 배경의 장식 조명과 발광체는 주인공보다 어둡게 둔다.
(나) 화면을 격자로 나눠 칸마다 평균 밝기를 내고 가장 밝은 칸들이 주인공 마스크와 겹치는지 본다. 화면 위 1/3은 글자가 올라가므로 그 구역의 평균 밝기와 대비도 따로 적는다.
(다) Blender Guru("전부 같게 비추면 아무것도 중요하지 않다"). 글자 구역에 관한 부분은 작업자 판단이다.

**R9. 따뜻한 빛과 차가운 빛을 나눈다.**
(가) 조명의 색은 RGB가 아니라 `use_temperature`와 `temperature`로 준다. 주광과 림 또는 좌우 림의 색온도를 다르게 한다.
(나) 스크립트의 조명 표를 출력해 색온도가 모두 같은 값이 아닌지 본다. Light group 패스별 평균 색의 R/B 비를 적는다.
(다) Blender Guru, Bennett ASC, Blender 5.2.2. 얼마나 벌릴지는 출처가 없다.

**R10. 광원의 크기를 바꿀 때 `normalize`를 정한다.**
(가) 반사에 비치는 밝기를 유지하며 크기만 바꾸려면 `normalize = False`로 두고 세기를 맞춘다. 켜 둔 채 크기를 키우면 반사가 어두워진다.
(나) 크기를 바꾸기 전과 후에 같은 반사 영역의 선형 값을 읽어 견준다.
(다) Blender 5.2 매뉴얼, 5.2.2 시험.

**R11. HDRI는 반사 채우기로만 쓴다.**
(가) 어두운 무대 컷에서는 월드의 `cycles_visibility.camera`를 끄고 세기를 낮춘다. 밝은 곳이 물체의 원하는 면에 오도록 Mapping의 Z 회전을 정한다. 잘리지 않은 HDRI를 쓴다. 조명용으로는 2K나 4K를 쓴다.
(나) 월드를 Light group에 넣어 월드만 켠 패스를 본다. 월드 패스가 물체의 확산 면을 눈에 띄게 밝히면 세기가 과하다. 배경 픽셀이 검은지 확인한다.
(다) Poly Haven, Blender 매뉴얼 World Settings, Chocofur(검색 요약).

**R12. 빛마다 Light group을 주고 하나씩 본다.**
(가) 주광, 림, 보조, 월드, 장식을 각각 Light group에 넣는다. 초안 렌더 한 번으로 빛별 패스를 낸다.
(나) 패스마다 화면 평균 밝기와 주인공 마스크 안의 평균을 적는다. 전체에 더하는 것이 거의 없는 빛은 뺀다. 패스를 더한 것이 Combined와 같은지 확인한다.
(다) Blender 5.2 매뉴얼 Passes, Visual Education(빛 하나하나의 몫을 본다), 5.2.2 시험.

### 바닥, 공기, 깊이

**R13. 물체는 바닥에 붙어 있어야 한다.**
(가) 물체와 바닥이 만나는 곳에 접지 그림자가 생기게 한다. 주광이 넓고 부드러우면 접지가 약해지므로, 멀리 둔 좁은 광원 하나로 단단한 그림자를 더한다. 광택 바닥에는 물체의 반사가 보이게 한다.
(나) 물체 밑면 바로 아래 바닥 띠의 밝기와 한 뼘 떨어진 바닥의 밝기를 견준다. 밑이 더 어두워야 한다. 바닥에 물체의 반사가 있는지 Glossy 패스로 본다.
(다) Lightmap. 이 표시를 "떠 보인다"로 직접 든 출처는 없다.

**R14. 바닥의 거칠기는 한 값이 아니다.**
(가) 바닥 재질의 Roughness에 저주파 노이즈나 얼룩 맵을 넣는다. 젖은 바닥은 웅덩이 모양의 마스크로 거칠기를 낮춘다.
(나) 바닥에 비친 띠 광원의 반사가 구간마다 선명도가 다른지 본다. 스크립트에서 Roughness 입력에 링크가 있는지(`bsdf.inputs['Roughness'].is_linked`) 확인한다.
(다) Creative Shrimp("젖은 바닥은 90%가 고르지 않은 거칠기").

**R15. 장면 전체를 볼륨으로 채우지 않는다.**
(가) 안개와 빛줄기는 필요한 곳에만 작은 볼륨 물체로 두거나, 알파 판, 합성의 Sun Beams, Mist 패스로 만든다. 장면 전체 볼륨은 검은 배경을 띄우고 렌더를 느리게 한다. 꼭 필요하면 볼륨만 따로 렌더해 얹는다.
(나) 볼륨을 켠 프레임과 끈 프레임의 렌더 시간과 배경의 5% 백분위 밝기를 나란히 적는다. 시험 장면에서는 시간이 4.0초에서 15.8초가 됐고 밝기 중앙값이 0.018에서 0.31이 됐다.
(다) Blender 매뉴얼(World, Glare), BlenderNation, Creative Shrimp, 5.2.2 시험.

### 재질

**R16. 주인공 물체의 눈에 보이는 모서리는 둥글린다.**
(가) Bevel 모디파이어를 먼저 쓴다. 형상이 지저분해 깨질 때만 Bevel 셰이더 노드를 쓴다(표본 4).
(나) 모서리를 따라 가는 밝은 선이 있는지 확대한 정지 화면으로 본다. 모디파이어 스택을 출력해 Bevel이 있는지 확인한다. 셰이더 노드를 썼으면 쓰기 전과 후의 프레임 시간을 적는다(매뉴얼은 20%까지 느려질 수 있다고 했고, 시험 장면에서는 4.0초가 4.5초가 됐다).
(다) Blender 5.2 매뉴얼 Bevel Node.

**R17. 광택 재질의 Roughness에 상수를 넣지 않는다.**
(가) 주인공의 금속, 도장, 유리의 Roughness에는 흠 맵이나 노이즈를 연결한다. 맵은 Non-Color로 읽고 물체의 실제 크기에 맞는 배율로 편다.
(나) 장면의 모든 Principled 노드를 돌며 Roughness가 연결돼 있지 않은 주인공 재질의 목록을 출력한다. 반사된 띠 광원의 가장자리가 구간마다 다르게 흐려지는지 확대해 본다.
(다) Blender Guru 강의 소개(검색 요약), Poly Haven 문서(검색 요약), 업계 글. 흠의 세기는 출처가 없다.

**R18. 도장은 코트로, 갈아 낸 금속은 이방성으로 만든다.**
(가) 자동차 도장: 밑칠은 거칠게, `Coat Weight` 1, `Coat Roughness`는 낮게. 메탈릭 입자는 밑칠의 Normal에만 넣고 `Coat Normal`은 매끈하게 둔다. 헤어라인 금속: `Anisotropic`과 `Tangent`를 준다. Glossy BSDF 기준과 90° 다르므로 방향을 렌더로 확인한다.
(나) 도장에 반사가 두 겹(넓고 부드러운 것과 좁고 선명한 것)으로 보이는지 확대해 본다. 헤어라인 금속의 하이라이트가 결의 직각 방향으로 늘어나는지 본다.
(다) Blender 5.2 매뉴얼 Principled, Blender Guru 이방성, 판매 셰이더 문서(검색 요약).

**R19. 재질 색을 1.0에 두지 않는다.**
(가) Base Color의 성분을 0.8 이하로 두고 모자라는 밝기는 빛으로 채운다.
(나) 모든 재질의 Base Color 기본값에서 0.8을 넘는 성분을 찾아 목록으로 낸다.
(다) Blender 5.2 매뉴얼 Reducing Noise(0.8이라는 숫자의 출처).

### 확인

**R20. 재질을 입히기 전에 클레이로 빛을 본다.**
(가) `view_layer.material_override`에 중간 회색 재질을 넣고 조명만으로 형태가 읽히는지 먼저 렌더한다.
(나) 클레이 렌더에서 물체의 윤곽과 큰 면의 구분이 보이는지 본다. R6의 면별 밝기 표를 여기서 낸다. 다만 클레이는 반사를 보여 주지 못하므로 금속 물체는 R1의 확인을 따로 한다.
(다) 클레이 렌더 해설(검색 요약), Blender 5.2.2.

**R21. 노출은 False Color로 잰다.**
(가) 컷마다 한 프레임을 False Color 뷰로 렌더해 주인공의 빛 받는 면, 그림자 면, 배경, 하이라이트가 어느 구간인지 적는다.
(나) 구간별 픽셀 비율을 표로 낸다. "위 잘림(흰색)"은 작은 하이라이트에만 있어야 하고 넓은 면에 있으면 노출이 과하다. 통과 구간은 사용자가 좋다고 한 프레임에서 정한다.
(다) Blender 5.2 매뉴얼 Displays and Views, Bennett ASC(반사를 측광한다).

### 색 관리와 마무리

**R22. 뷰 변환은 AgX, Standard와 Filmic은 쓰지 않는다.**
(가) `view_transform = 'AgX'`로 두고 Look으로 대비를 고른다. 노출을 먼저 맞추고 Look을 정한다. 한 편 안의 모든 컷이 같은 뷰 변환과 Look을 쓴다.
(나) 렌더 스크립트가 시작할 때 `view_transform`, `look`, `exposure`를 출력하게 한다. 컷 사이에 값이 다르면 실패다. 밝은 색 하이라이트가 원색으로 타지 않고 흰 쪽으로 빠지는지 본다.
(다) Blender 5.2 매뉴얼, 4.0 릴리스 노트. 컷 사이의 일관성은 작업자 판단이다.

**R23. 블룸은 Blender에서, 조금만, 선형 값에서.**
(가) Glare의 Type을 `Bloom`이나 `Fog Glow`로 명시한다(기본은 `Streaks`다). 문턱은 1 근처에 두어 정말 밝은 하이라이트에만 붙게 한다. Strength는 1보다 작게 둔다.
(나) Glare를 켠 프레임과 끈 프레임의 차이 이미지를 만들어, 차이가 하이라이트 주변에만 있고 화면 전체의 검정을 띄우지 않는지 본다. 배경의 5% 백분위 밝기가 Glare를 켜도 그대로인지 숫자로 견준다.
(다) Blender 5.2 매뉴얼 Glare, Blender Guru(과하지 않게). Strength의 값은 출처가 없다.

**R24. 화면 전체 효과는 Remotion에, 렌즈 효과는 3D 층에만.**
(가) 비네트, 그레인, 최종 색 보정은 Remotion에서 글자까지 포함한 화면에 건다. 색수차와 렌즈 왜곡은 넣는다면 Blender에서 3D에만, 아주 약하게 건다. 선명화는 기본으로 하지 않는다.
(나) 최종 합성 프레임에서 글자의 가장자리에 색 번짐이 없는지 확대해 본다. 색수차를 켠 프레임과 끈 프레임을 나란히 놓고 화면 가운데의 물체에서는 차이가 보이지 않는지 본다.
(다) 작업자 판단. 근거는 Blender Guru(전문 사진은 이런 흠을 없앤다)와 우리 합성 구조.

**R25. 5.2의 합성 API로 쓴다.**
(가) `scene.compositing_node_group`에 `CompositorNodeTree` 그룹을 넣고, 출력은 `NodeGroupOutput`, 섞기는 `ShaderNodeMix`, 노드 설정은 `node.inputs['이름'].default_value`로 한다. `scene.node_tree`, `CompositorNodeComposite`, `CompositorNodeMixRGB`, `glare.glare_type` 같은 옛 이름을 쓰지 않는다.
(나) 스크립트를 헤드리스로 한 번 돌려 `AttributeError`와 "undefined" 오류가 없는지 본다. 합성을 켠 결과와 끈 결과가 실제로 다른지 한 프레임을 견준다.
(다) 4.5, 5.0 릴리스 노트, Blender 5.2.2.

### 렌더 품질

**R26. 디노이저는 OIDN, 입력은 Albedo+Normal.**
(가) `denoiser = 'OPENIMAGEDENOISE'`, `denoising_input_passes = 'RGB_ALBEDO_NORMAL'`, `denoising_prefilter = 'ACCURATE'`, `denoising_use_gpu = True`. GPU 메모리가 모자라면 `denoising_use_gpu`를 끈다.
(나) 한 프레임을 디노이즈를 켜고, 끄고 렌더해 주인공의 흠 맵과 미세한 무늬가 디노이즈 뒤에도 남아 있는지 확대해 견준다. 이어진 세 프레임을 렌더해 움직이지 않는 영역의 프레임 간 차이를 잰다. 차이가 눈에 띄는 얼룩이면 표본을 올린다.
(다) Blender 5.2 매뉴얼 Sampling, 포럼(검색 요약: OIDN은 시간축을 보지 않는다).

**R27. 직접 클램프는 끄고 간접만 클램프한다.**
(가) `sample_clamp_direct = 0`, `sample_clamp_indirect`는 기본값(10)에서 시작한다. 반딧불이 남으면 간접 값을 낮추기 전에 커스틱을 끄고, Filter Glossy를 올리고, 광원과 물체 사이의 거리를 본다.
(나) 디노이즈를 끈 프레임에서 주변보다 훨씬 밝은 외톨이 픽셀의 수를 센다. 클램프를 바꾸기 전과 후에 하이라이트 영역의 최댓값(선형)을 견줘 하이라이트가 깎이지 않았는지 본다.
(다) Blender 5.2 매뉴얼 Light Paths, Reducing Noise.

**R28. 표본은 노이즈 한계로 조절하고, 프레임 시간을 기록한다.**
(가) 적응 표본을 켜고 `adaptive_threshold`를 매뉴얼의 범위(0.1~0.001) 안에서 정한다. 최대 표본은 상한으로만 둔다. 컷의 첫 프레임, 가운데 프레임, 마지막 프레임을 먼저 렌더해 시간을 잰 뒤 전체를 돌린다.
(나) 프레임마다 렌더 시간을 기록한다. `pass_debug_sample_count`를 켜면 픽셀별 표본 수를 볼 수 있다(속성은 확인했고 써 보지는 않았다). 디노이즈를 끈 프레임의 어두운 영역 표준편차를 한계값별로 적는다.
(다) Blender 5.2 매뉴얼 Sampling.

**R29. 8GB를 넘지 않게 텍스처와 형상을 잰다.**
(가) 주인공 물체에만 4K를 쓰고 나머지는 2K 이하로 둔다. 같은 물체는 메시 데이터를 공유하는 복제로 늘린다. `use_persistent_data`를 켠다. 텍스처가 많으면 Simplify의 텍스처 크기 제한이나 텍스처 캐시를 쓴다.
(나) 렌더 전에 장면의 이미지 목록과 해상도를 출력하고 매뉴얼의 환산(8K 256MB, 4K 64MB, 2K 16MB, 1K 4MB)으로 합계를 낸다. 렌더하는 동안 `nvidia-smi`의 메모리 사용량 최댓값을 기록한다. 8GB에 닿으면 시스템 메모리로 넘어가 느려진다.
(다) Blender 5.2 매뉴얼 GPU Rendering, Simplify, Performance.

**R30. EEVEE는 주인공 컷에 쓰지 않는다.**
(가) 광택 바닥과 광택 물체가 화면 밖의 광원을 비추는 컷은 Cycles로 렌더한다. EEVEE는 볼륨 층이나 배경 층처럼 반사가 중요하지 않은 것에만 쓴다.
(나) EEVEE를 쓴 층이 있으면, 같은 프레임을 Cycles로도 한 장 렌더해 화면 가장자리의 반사와 가려진 물체의 반사를 견준다.
(다) Blender 5.2 매뉴얼 EEVEE Limitations. 레이 트레이싱 옵션은 시험하지 않았다.

## 출처

### 원문을 읽은 것

Blender 5.2 매뉴얼(파일로 받아 본문을 읽음):

- Sampling: https://docs.blender.org/manual/en/latest/render/cycles/render_settings/sampling.html
- Light Paths: https://docs.blender.org/manual/en/latest/render/cycles/render_settings/light_paths.html
- Reducing Noise: https://docs.blender.org/manual/en/latest/render/cycles/optimizations/reducing_noise.html
- Light Objects: https://docs.blender.org/manual/en/latest/render/lights/light_object.html
- Light Settings (Cycles): https://docs.blender.org/manual/en/latest/render/cycles/light_settings.html
- Light Linking: https://docs.blender.org/manual/en/latest/render/lights/light_linking.html
- World Environment: https://docs.blender.org/manual/en/latest/render/lights/world.html
- World Settings (Cycles): https://docs.blender.org/manual/en/latest/render/cycles/world_settings.html
- Object Settings (Cycles, Visibility): https://docs.blender.org/manual/en/latest/render/cycles/object_settings/object_data.html
- Displays and Views: https://docs.blender.org/manual/en/latest/render/color_management/displays_views.html
- Glare Node: https://docs.blender.org/manual/en/latest/compositing/types/filter/glare.html
- Lens Distortion Node: https://docs.blender.org/manual/en/latest/compositing/types/transform/lens_distortion.html
- Denoise Node: https://docs.blender.org/manual/en/latest/compositing/types/filter/denoise.html
- Bevel Node: https://docs.blender.org/manual/en/latest/render/shader_nodes/input/bevel.html
- Principled BSDF: https://docs.blender.org/manual/en/latest/render/shader_nodes/shader/principled.html
- Passes(Light Groups, Mist, Denoising Data): https://docs.blender.org/manual/en/latest/render/layers/passes.html
- Volumes: https://docs.blender.org/manual/en/latest/render/cycles/render_settings/volumes.html
- Performance: https://docs.blender.org/manual/en/latest/render/cycles/render_settings/performance.html
- Simplify: https://docs.blender.org/manual/en/latest/render/cycles/render_settings/simplify.html
- Motion Blur: https://docs.blender.org/manual/en/latest/render/cycles/render_settings/motion_blur.html
- Film: https://docs.blender.org/manual/en/latest/render/cycles/render_settings/film.html
- GPU Rendering: https://docs.blender.org/manual/en/latest/render/cycles/gpu_rendering.html
- EEVEE Limitations: https://docs.blender.org/manual/en/latest/render/eevee/limitations/limitations.html

Blender 릴리스 노트(요약 도구를 거쳐 읽음):

- 4.0 Color Management: https://developer.blender.org/docs/release_notes/4.0/color_management/
- 4.0 Cycles: https://developer.blender.org/docs/release_notes/4.0/cycles/
- 4.1 Cycles: https://developer.blender.org/docs/release_notes/4.1/cycles/
- 4.2 Cycles: https://developer.blender.org/docs/release_notes/4.2/cycles/
- 4.5 Compositor: https://developer.blender.org/docs/release_notes/4.5/compositor/
- 5.0 Compositor: https://developer.blender.org/docs/release_notes/5.0/compositor/
- 5.0 Cycles: https://developer.blender.org/docs/release_notes/5.0/cycles/
- 5.0 Color Management: https://developer.blender.org/docs/release_notes/5.0/color_management/
- 5.1 Cycles: https://developer.blender.org/docs/release_notes/5.1/cycles/
- 5.2 Cycles: https://developer.blender.org/docs/release_notes/5.2/cycles/

실무자의 글(요약 도구를 거쳐 읽음):

- Lightmap, Lighting for Automotive Rendering: https://www.lightmap.co.uk/blog/lighting-for-automotive-rendering/
- Visual Education(Karl Taylor), How to Light and Photograph Cars in a Studio: https://visualeducation.com/?p=48699
- Visual Education, Black-on-Black Product Photography Using Two Lights: https://visualeducation.com/?p=50348
- Lensvid, Shooting Black Products on a Black Background: https://lensvid.com/technique/shooting-black-products-on-a-black-background/
- No Film School, How to Light a Car Commercial(Bill Bennett ASC): https://nofilmschool.com/2017/03/how-to-light-car-commercial
- StudioBinder, Lighting Ratios: https://www.studiobinder.com/blog/lighting-ratios/
- City Tech 강의 노트(Light: Science & Magic 요약): https://openlab.citytech.cuny.edu/comd3330he10fall2021/2021/11/30/food-photography-and-direct-reflection/
- Blender Guru, 6 Tips for Better Lighting: https://www.blenderguru.com/posts/6-tips-for-better-lighting
- Blender Guru, Achieving Photorealism in Blender: https://www.blenderguru.com/posts/achieving-photorealism-in-blender
- Blender Guru, Introduction to Anisotropic Shading: https://www.blenderguru.com/posts/an-introduction-to-anisotropic-shading
- Creative Shrimp(Gleb Alexandrov), Reverse Key Lighting: https://www.creativeshrimp.com/reverse-key-lighting-tutorial.html
- Creative Shrimp, Realistic Lighting in Blender: 11 Hacks(강의 목차): https://www.creativeshrimp.com/realistic-lighting-in-blender.html
- Creative Shrimp, Lighting and Visual Overstimulation: https://www.creativeshrimp.com/lighting-tutorial-and-visual-overstimulation.html
- Poly Haven, What is Clipping?: https://blog.polyhaven.com/what-is-clipping/
- BlenderNation, Faster Volumetrics in Blender: https://www.blendernation.com/2021/07/06/faster-volumetrics-in-blender/

### 검색 요약만 본 것

- Light: Science & Magic(책): https://routledge.com/product/isbn/9780367860271
- Poly Haven 텍스처 기준: https://docs.polyhaven.com/en/technical-standards/textures (본문이 열리지 않음)
- Poly Haven HDRI 기준과 해상도 글: https://docs.polyhaven.com/en/technical-standards/hdris , https://blog.polyhaven.com/?p=140
- Blender Guru의 "The Secret Ingredient to Photorealism": https://www.blenderguru.com/posts/secret-ingredient-photorealism
- Secrets of Photorealism in Blender(강의 소개): https://superhivemarket.com/products/secrets-of-photorealism-in-blender
- Chocofur 스튜디오 설정: https://chocofur.com/page/studio-rendering-setup-in-blender-2-79 (접속 실패)
- Gleb Alexandrov HDR Lighting 강의 소개: https://gleb-alexandrov.gumroad.com/l/hdr-lighting
- CG Cookie, Fundamentals of Digital Lighting(강의 목차): https://cgcookie.com/course/fundamentals-of-digital-lighting-in-blender
- 검은 차 조명(사진 포럼): https://www.talkphotography.co.uk/threads/lighting-a-black-car.229440/
- OIDN과 애니메이션 깜빡임(포럼): https://blenderartists.org/t/flickering-noise-on-cycles-animation/1383040 , https://www.blendernation.com/2022/01/10/optix-temporal-denoising-support-added-to-blender-3-1-alpha/
- 볼륨을 따로 렌더하기(포럼): https://blenderartists.org/t/cycles-render-with-volume-to-capture-god-rays/1546606
- 자동차 도장 셰이더 문서(판매 글): https://superhivemarket.com/products/car-paint-shader-flakesiridescence/docs
- AgX 원 저장소와 darktable 포럼: https://github.com/EaryChow/AgX , https://discuss.pixls.us/t/blender-agx-in-darktable-proof-of-concept/48697
- 가짜 같아 보이는 렌더(업계 글): https://blog.renderahouse.com/blog/why-renders-look-fake-6-common-problems-solved , https://archvisinsider.substack.com/p/avoid-these-5-cgi-mistakes-and-improve
- 클레이 렌더: https://7cgi.com/blog/what-is-clay-render
- ASC, Car Commercial Lighting: https://theasc.com/?p=33362 (접속 실패)
- Evermotion, Blender Principled Shader Unleashed: https://evermotion.org/tutorials/show/10869/blender-principled-shader-unleashed (403)
- BlenderNation, 색수차를 CGI에 넣는 까닭과 방법: https://www.blendernation.com/2024/12/02/why-and-how-to-add-chromatic-aberration-to-cgi-in-blender/ (접속 실패)

## 확인하지 못한 것

**버전과 API**

- Glare 노드가 정확히 어느 버전에서 지금의 꼴(Bloom, Strength, Saturation, Tint)이 됐는지. 4.5와 5.0의 노트만 읽었다. 4.2~4.4의 합성 노트는 읽지 않았다.
- 5.1과 5.2의 합성 릴리스 노트는 읽지 않았다. 5.2의 합성 노드 이름과 입력은 릴리스 노트가 아니라 실행해서 확인한 것이다.
- 조명의 `use_temperature`, `exposure`, `normalize`가 어느 버전에서 들어왔는지.
- OptiX 시간축 디노이즈가 5.2에서 쓸 수 있는지, bpy로 어떻게 부르는지. 3.1 알파에 들어왔다는 검색 요약만 봤다.
- `texture_limit_render`가 `use_simplify` 없이 듣는지. 텍스처 캐시(`.tx`)를 bpy로 켜는 속성 이름과 실제로 줄어드는 메모리.
- `blocker_collection`을 빈 컬렉션으로 두면 "아무것도 가리지 않는다"가 되는지. 속성 대입만 확인했다.
- `cycles_visibility.diffuse = False`인 월드, 비네트 노드 조합(Ellipse Mask, Blur, Mix), 흰 노이즈로 만든 그레인은 렌더해 보지 않았다.
- `Material.use_nodes`가 없어진 뒤(6.0 예정) 새 재질을 만드는 올바른 방법.

**품질과 비용**

- 우리 실제 컷(자동차, 터빈, 로봇, 공장)에서의 표본 수, 노이즈 한계, 프레임 시간. 시험은 정육면체 하나였다.
- OIDN의 프레임 간 얼룩이 우리 표본 수에서 보이는지. 작업자는 영상을 재생하지 못한다. 프레임 간 차이를 숫자로 잴 수는 있으나 재지 않았다.
- 시드를 프레임마다 바꾸는 것과 고정하는 것 중 디노이즈 뒤에 어느 쪽이 덜 거슬리는지. 매뉴얼은 바꾸라고 하지만 디노이저와 함께 쓴 경우를 다룬 출처는 읽지 않았다.
- EEVEE의 레이 트레이싱 옵션이 광택 바닥 컷에서 Cycles와 얼마나 다른지. EEVEE가 이 컴퓨터에서 헤드리스로 도는지도 시험하지 않았다.
- 볼륨만 EEVEE로 렌더해 얹는 방법, 홀드아웃으로 볼륨만 따로 렌더하는 방법을 직접 해 보지 않았다.
- Light linking과 텍스처 조명이 light tree에서 노이즈를 얼마나 늘리는지.
- 처음 Bevel 노드를 쓴 렌더가 58.8초 걸린 까닭.
- 16비트 PNG로 낸 어두운 그러데이션이 Remotion과 H.264를 거친 뒤 띠(banding)가 생기는지, 그레인이 압축에서 살아남는지.
- AgX와 ACES 2.0 중 우리 화면에 어느 쪽이 나은지. 견준 출처도 없고 시험도 하지 않았다.

**조명 지식**

- 아래에서 올려 비추는 빛의 문제를 다룬 출처.
- 제품과 자동차 조명에서 쓰는 조명비의 숫자. 찾은 숫자는 전부 얼굴 조명용이다.
- 스튜디오(The Mill, Recom Farmhouse 등)의 자동차 CG 제작기. 검색에서 구체적인 조명 설명이 있는 글을 찾지 못했다.
- 블룸, 색수차, 비네트, 그레인의 "적당한 세기". 숫자를 준 출처가 없다. 사용자가 여러 안에서 골라야 한다.
- "AI 같아 보인다"를 조명과 재질의 용어로 정의한 출처. 7절의 표는 아마추어 CG에 관한 것이고, 둘이 겹친다는 것은 가설이다.
- 광원의 "상대 크기"(물체에서 본 각 크기)와 부드러움의 관계를 수식으로 준 출처. 매뉴얼과 Blender Guru는 크기가 클수록 부드럽다고만 한다.
- Gleb Alexandrov, CG Cookie, Chocofur의 유료 강의 본편. 목차와 소개만 봤다.
