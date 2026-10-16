# 3D 컷의 카메라와 구도

조사일 2026-10-08. 대상은 Blender 5.2 LTS(Cycles), 1080x1920, 24fps, 3~10초짜리 주인공 물체 컷이다.

출처 표기: **[읽음]** 은 그 페이지 본문을 직접 받아 읽은 것, **[검색 요약]** 은 검색 결과의 요약만 본 것, **[실측]** 은 이 컴퓨터의 Blender 5.2.2 LTS를 화면 없이 실행해 값을 확인한 것이다. 숫자는 출처가 준 것만 적었다. "널리 합의됨"과 "한 사람의 의견"을 문장마다 구분했다.

## 요약

실무자들이 공통으로 말하는 것은 하나다. 가상 카메라를 실제 카메라처럼 다룬다. 실제 렌즈의 초점 거리와 조리개를 쓰고, 달리·크레인·손으로 든 카메라가 할 수 있는 움직임만 하고, 움직임에는 가속과 감속이 있다(픽사 촬영감독 Patrick Lin, 애니메이션 12원칙). 원근감은 렌즈가 아니라 카메라와 물체의 거리가 정한다. 그래서 "가까이서 넓게"와 "멀리서 길게"는 같은 크기로 찍어도 다른 그림이다. 차 광고에서는 깔끔한 제품 컷에 27mm 이상을, 속도감 컷에 14.5mm 같은 광각을 쓴다는 촬영감독의 말이 있다. 피사계 심도를 지나치게 얕게 하면 큰 물체가 모형처럼 보인다. 세로 화면에서는 가로 움직임이 과장되므로 좌우 팬을 줄이고, 앞에 걸리는 물체를 두어 깊이를 만든다. Blender 5.2에서 확인한 것 중 코드에 바로 영향을 주는 것은 네 가지다. (1) 세로 해상도에서 기본 센서 맞춤(AUTO)은 36mm를 세로 변에 대므로 50mm 렌즈의 가로 화각이 가로 화면의 89mm와 같다. (2) `shift_y`로 카메라를 기울이지 않고 물체를 가운데 띠로 옮길 수 있다. (3) `action.fcurves`는 5.0에서 없어졌다. (4) 잡음 변조기의 섞기 방식을 ADD로 두면 흔들림이 한쪽으로 치우친다. 조사에서 찾지 못한 것은 Gleb Alexandrov·CG Cookie·Ian Hubert가 카메라 구도에 대해 직접 한 말, 전체 CG 차 광고의 카메라 제작기, 움직임 속도의 숫자 기준이다.

---

## 1. 렌즈 선택

### 확인한 것

- **원근 왜곡은 거리가 만든다(널리 합의됨).** "원근의 변화는 렌즈가 아니라 거리가 만든다. 같은 거리에서 찍은 두 장은 어떤 렌즈를 쓰든 원근 구조가 같다." 가까이서 찍으면 가까운 부분이 비정상적으로 커지고 먼 부분이 작아진다(확장). 멀리서 찍으면 멀리 있는 것들의 크기가 비슷해져 거리 차이를 알 수 없게 된다(압축).
  - https://en.wikipedia.org/wiki/Perspective_distortion [읽음]
  - 자동차 사진가 Robert Hall도 같은 말을 한다. "렌즈가 압축을 조절하는 게 아니라 거리가 한다. 차에서 멀어질수록 차의 각 부분이 서로 정확한 비율로 보인다." https://www.adorama.com/alc/car-photography [읽음]
- **초점 거리 구간별 효과(널리 합의됨).** StudioBinder의 구분: 광각 23~35mm는 "물체 사이의 거리를 과장"하고 카메라 쪽으로 오가는 움직임을 과장한다. 표준 35~55mm는 왜곡이 두드러지지 않는 중립. 망원 55~500mm는 "배경이 피사체에 가까워 보이게 압축"하고 피사체를 배경에서 떼어 내며 옆으로 가는 움직임을 강하게 한다.
  - https://www.studiobinder.com/blog/focal-length-camera-lenses-explained/ [읽음]
- **차 광고의 선택(한 사람의 의견, 촬영감독 Shane Hurlbut, ASC).** 깔끔한 차 광고에는 "27mm 이상이 대개 이상적"이고 이유는 왜곡을 줄여 차의 선을 깨끗하게 보이기 위해서다. 몰입형 액션에는 "14.5mm 같은" 광각을 쓰고 "광각의 왜곡을 속도와 위험의 느낌을 키우는 데 쓸 수 있다"고 한다. 광각은 빠르게 바뀌는 주변 풍경을 더 많이 담아 속도감을 키운다.
  - https://www.filmmakersacademy.com/blog-lenses-car-cinematography/ [읽음]
- **차 영상의 렌즈 역할 분담(한 사람의 의견, Chris Luong).** 14mm는 실내 전용, 35mm는 기본, 50mm는 "35mm보다 조금 더 압축이 필요한 세부 컷", 85mm는 클로즈업과 긴 렌즈 컷.
  - https://blog.sigmaphoto.com/2023/sigma-cine-prime-lenses-for-automotive-cinematography/ [읽음]
- **차 사진에서 너무 멀거나 너무 가까울 때(한 사람의 의견, 사진가 Karl Taylor).** "긴 렌즈로 너무 멀리서 찍으면 차가 뭉툭해(chunky) 보이고, 광각으로 너무 가까이서 찍으면 불룩해(bulbous) 보인다." 초점 거리가 촬영 거리와 화각을 정하고 그것이 원근을 바꾼다. 구도는 조명 전에 정한다. 조명을 시작한 뒤에는 구도를 바꿀 수 없다.
  - https://visualeducation.com/10-car-photography-tips/ [읽음]
  - https://visualeducation.com/class/professional-car-photography-3-4-front-view/ [읽음]
- **왜곡을 피하는 범위(출처 약함).** TutKit의 자동차 사진 강의는 "35~50mm가 왜곡을 피하기에 가장 좋다"고 한다. 글쓴이 이름이 없다.
  - https://tutkit.com/en/text-tutorials/21046-masterclass-in-automotive-photography-positioning-and-composition [읽음]
- **Blender의 기본값 [실측].** 새 카메라는 `lens=50.0`, `sensor_width=36.0`, `sensor_height=24.0`, `sensor_fit='AUTO'`, `clip_start=0.1`, `clip_end=1000.0`, `dof.use_dof=False`, `dof.aperture_fstop=2.8`이다.
- **세로 화면에서 초점 거리가 뜻하는 것 [실측, 이 프로젝트에 중요].** 1080x1920에서 `sensor_fit='AUTO'`는 36mm를 긴 변(세로)에 댄다. 그래서 같은 mm라도 가로 화각이 가로 화면보다 훨씬 좁다.

  | `lens` (센서 36, AUTO, 1080x1920) | 가로 화각 | 세로 화각 | 가로 화각이 같은 가로 화면(36mm 폭) 렌즈 |
  |---|---|---|---|
  | 24mm | 45.7° | 73.7° | 43mm |
  | 35mm | 32.3° | 54.4° | 62mm |
  | 50mm | 22.9° | 39.6° | 89mm |
  | 85mm | 13.6° | 23.9° | 151mm |
  | 135mm | 8.6° | 15.2° | 240mm |

  `sensor_fit='HORIZONTAL'`로 바꾸면 50mm의 가로 화각이 39.6°(가로 화면의 50mm와 같음), 세로 화각이 65.2°가 된다. 위 실무자들의 mm 숫자는 가로 화면 기준이므로, 그 숫자를 옮겨 쓸 때는 `sensor_fit='HORIZONTAL'`로 두거나 위 표로 환산한다.

### 기본 50mm·눈높이가 아마추어처럼 보이는 까닭

이것을 직접 말한 실무자의 글은 찾지 못했다. 확인한 사실로 말할 수 있는 범위는 이렇다. 50mm와 눈높이는 Blender와 사람의 기본값이라 선택의 결과가 아니다. StudioBinder는 눈높이를 "우월하지도 열등하지도 않은 중립"이라고 적는다(2절). 중립은 물체에 대해 아무 말도 하지 않는다. 아래는 조사자의 추론이다: 실무자들은 컷마다 렌즈와 높이를 뜻에 맞춰 고르므로, 모든 컷이 같은 렌즈와 같은 높이면 고르지 않았다는 표시가 된다.

---

## 2. 카메라 높이와 각도

### 확인한 것

- **각도의 뜻(널리 합의됨, StudioBinder).**
  - 눈높이: "중립적인 시점(우월하지도 열등하지도 않음)".
  - 로우 앵글: "우월함을 알리거나 두려움을 일으키는 데 알맞다".
  - 하이 앵글: "대개 열등함, 내려다보는 느낌".
  - 더치 앵글: "방향 감각 상실, 불안정한 심리, 긴장".
  - 오버헤드(버즈아이): "중립 또는 신의 시점".
  - 항공: "경외와 규모".
  - https://www.studiobinder.com/blog/types-of-camera-shot-angles-in-film/ [읽음]
- **차의 높이 선택(한 사람의 의견, Karl Taylor).** 3/4 앞모습에서 "높은 각도는 보닛을 더 보여 주고 차체를 덜 보여 주며, 낮은 각도는 더 위압적인 느낌을 준다".
  - https://visualeducation.com/class/professional-car-photography-3-4-front-view/ [읽음]
- **차의 높이 선택(출처 약함, TutKit).** "낮은 높이는 스포티한 디자인을 강조하고 높은 시점은 육중한 차를 강조한다."
  - https://tutkit.com/en/text-tutorials/21046-masterclass-in-automotive-photography-positioning-and-composition [읽음]
- **3/4 뷰(널리 합의됨).** Robert Hall: "보통 '앞 3/4'나 '뒤 3/4'를 찍는다. 차의 한 면 가운데에 서지 않고 모서리를 담는다. 한 컷에 두 면을 보여 주기 위해서다." TutKit: 옆면 3분의 2, 앞면 3분의 1. 일반 렌더 구도 정리에서도 "45도에서 찍어 물체의 여러 면을 보여 입체감을 낸다"가 항목으로 있다.
  - https://www.adorama.com/alc/car-photography [읽음]
  - https://blog.habrador.com/2022/06/render-blender-composition-techniques-photography.html [읽음]
- **지평선 위치(한 사람의 의견, Vertical Film Festival 공동 창립자 Adam Sébire).** 세로 화면에서 지평선은 "가운데보다 위나 아래로 옮기는 것을 고려하라. 50/50이 구도 전략이 아니라면".
  - https://www.adamsebire.info/vertical-film-festival/9-16-tips-and-tricks/ [읽음]
- **높은 각도의 부작용.** 축소 모형처럼 보이게 하는 사진은 "높은 각도에서 찍어 모형을 내려다보는 효과를 흉내 낸다". 큰 물체를 높은 각도와 얕은 심도로 함께 찍으면 모형처럼 보일 수 있다.
  - https://en.wikipedia.org/wiki/Miniature_faking [읽음]
- **렌즈 시프트 [Blender 설명서 5.2 LTS, 읽음].** Shift는 "소실점을 조정"하고, 시프트를 쓰면 "수평선이 완전히 수평으로 유지된다". 카메라를 위로 기울이면 세로 선이 모이지만, 시프트로 화면만 옮기면 모이지 않는다.
  - https://docs.blender.org/manual/en/latest/render/cameras.html

### 찾지 못한 것

"휠 허브 높이에 카메라를 둔다"는 조언은 검색 요약에만 있었고 원문을 특정하지 못했다. 규칙으로 쓰지 않는다.

---

## 3. 피사계 심도

### 확인한 것

- **Blender의 설정 [설명서 5.2 LTS, 읽음 / 실측].**
  - Focus Object: "초점을 정할 물체를 고른다. 물체를 연결하면 거리 값은 비활성화된다." (`dof.focus_object`)
  - Focus Distance: 초점 물체가 없을 때의 초점 거리. (`dof.focus_distance`, 기본 10.0)
  - F-Stop: "흐림의 양을 정한다. 낮은 값이 강한 심도 효과를 준다." (`dof.aperture_fstop`, 기본 2.8)
  - Blades: 흐려진 점의 모양을 다각형으로 바꾸는 조리개 날 수. (`dof.aperture_blades`, 기본 0 = 원, 설명에 "최소 3")
  - Rotation: 날의 회전. (`dof.aperture_rotation`)
  - Ratio: "아나모픽 보케 효과를 흉내 내는 왜곡의 양. 1.0은 왜곡 없음." (`dof.aperture_ratio`, 기본 1.0)
  - https://docs.blender.org/manual/en/latest/render/cameras.html
- **심도가 얕으면 모형처럼 보인다(널리 합의됨).** 촬영감독 Art Adams: "큰 물체를 찍으면서 심도를 좁은 조각으로 줄이면 사진이 모형처럼 보인다. 모형을 속임수 없이 찍으면 심도가 아주 좁기 때문이다." 위키백과: 흐림이라는 단서가 익숙한 크기 정보를 "덮어써서 물체가 모형이나 장난감처럼 보인다". "배율이 커질수록 심도는 줄어든다."
  - https://www.provideocoalition.com/fake_tilt_shift_cinematography/ [읽음]
  - https://en.wikipedia.org/wiki/Miniature_faking [읽음]
- **심도를 정하는 것(널리 합의됨).** 초점 거리, 피사체 거리, 허용 착란원, 조리개. 근사식은 DOF ≈ 2u²Nc/f² (u 피사체 거리, N 조리개 값, c 허용 착란원, f 초점 거리). 심도는 거리의 제곱에 비례하고 초점 거리의 제곱에 반비례한다. 35mm 영화의 허용 착란원은 전통적으로 0.05mm, 현대 실무에서는 0.025mm.
  - https://en.wikipedia.org/wiki/Depth_of_field [읽음]
- **실제 차 촬영의 조리개(한 사람의 의견).** Robert Hall: 광각에서는 f/5.6 정도, 초점 거리가 길수록 f/8이나 f/11. Karl Taylor: 차는 몇 미터 길이라 심도를 확인해야 하고 "f/11이나 f/16에서 충분한 심도를 얻을 수 있다".
  - https://www.adorama.com/alc/car-photography [읽음]
  - https://visualeducation.com/10-car-photography-tips/ [읽음]
- **초점 이동(랙 포커스)(널리 합의됨).** "초점면을 화면 안의 한 물체에서 다른 물체로 옮겨" 관객의 시선을 옮긴다. "언제나 동기가 있어야 한다." 심도가 얕을수록 이동이 눈에 띈다.
  - https://www.studiobinder.com/blog/rack-focus-shot-camera-movement-angle/ [읽음]
- **아나모픽.** 픽사는 토이 스토리 4에서 Cooke 아나모픽 렌즈를 본뜬 가상 렌즈로 타원 보케, 가로 플레어, 얕은 심도를 냈다(No Film School의 Patrick Lin 인터뷰). 타원 보케가 가로 2:1 압축에서 나온다는 설명은 검색 요약으로만 확인했다.
  - https://nofilmschool.com/toy-story-4-pixar-cinematography [읽음]
  - https://www.adorama.com/alc/anamorphic-lens [검색 요약]

### 숫자로 확인하는 법 [실측]

위 근사식의 원식(과초점 거리 H = f²/(Nc) + f, 가까운 한계 = Hs/(H + s − f), 먼 한계 = Hs/(H − (s − f)))으로 심도 범위를 계산할 수 있다. 4.4m 길이의 상자를 6.5m 거리에서 볼 때의 계산 결과:

| 렌즈, 조리개 (c = 0.025mm) | 선명한 범위 | 4.4m 물체가 다 들어가는가 |
|---|---|---|
| 35mm, f/5.6 | 3.76m ~ 25.12m | 들어간다 |
| 85mm, f/1.4 | 6.34m ~ 6.75m | 41cm만 선명하다 |

주의: 이 계산은 표준 광학식이다. Cycles가 같은 장면 단위에서 같은 흐림을 내는지는 렌더로 대조하지 않았다(확인하지 못한 것 참조).

---

## 4. 카메라 움직임

### 확인한 것

- **움직임의 뜻(널리 합의됨, StudioBinder).**
  - 푸시 인: "관객을 피사체에 가까이 끌어 긴장이나 친밀함을 키운다."
  - 풀 아웃: "주변과 떨어뜨려 고립감을 만든다", "배경과 인물을 드러낸다".
  - 아크: "피사체를 돌며 정적인 장면에 역동을 더한다."
  - 붐/크레인: "장소를 소개하는 큰 설정 컷".
  - 틸트: "규모나 지배력", "경외와 장관".
  - 팬: "새 정보를 드러내거나 따라가거나 에너지를 더한다."
  - 휩 팬: "에너지를 더한다."
  - 롤: "방향 감각을 잃게 하거나 불안을 키운다", 매우 의도적인 움직임.
  - 줌: "인위적이거나 부자연스러운" 효과.
  - 핸드헬드: "날것의 몰입감", "혼란스럽거나 친밀한 장면에 효과적".
  - 고정: 방해 없이 보여 준다.
  - https://www.studiobinder.com/blog/different-types-of-camera-movements-in-film/ [읽음]
- **달리와 줌의 차이.** 달리는 카메라가 실제로 움직여 가까운 것과 먼 것이 다른 속도로 움직이고(시차), 줌은 모든 것을 같은 비율로 키워 시차가 없다. 여러 사이트가 같은 설명을 한다.
  - https://melies.co/cinematic-techniques/camera-movement/dolly [검색 요약]
- **가상 카메라는 실제 카메라처럼(픽사, 널리 인용됨).** Patrick Lin: "카메라를 어떻게 세우고 어떤 렌즈와 각도를 쓰는지는 실사든 애니메이션이든 기법이 같다." 핸드헬드 느낌은 어깨에 멘 장비의 움직임을 추적해 얻었다. 인사이드 아웃에서는 실제 렌즈(ARRI Zeiss Ultra Prime, Cooke S4)의 왜곡 곡선까지 옮겼다.
  - https://nofilmschool.com/toy-story-4-pixar-cinematography [읽음]
  - 픽사가 "실제 카메라가 물리적으로 할 수 없는 것은 하지 않으려 하고, 불완전함을 넣는다"는 정리는 검색 요약으로만 봤다. https://kottke.org/19/10/pixars-fake-real-cameras [검색 요약]
- **가속과 감속(널리 합의됨, 애니메이션 12원칙).** "현실의 물체는 가속하고 감속하는 데 시간이 필요하다." "자연스러운 움직임은 대개 호를 그린다. 기계적인 물체는 예외로 대개 직선으로 움직인다."
  - https://en.wikipedia.org/wiki/Twelve_basic_principles_of_animation [읽음]
- **Blender의 보간 [설명서 5.2 LTS, 읽음].** Linear는 "값의 급변은 막지만 속도의 급변은 막지 못한다". Bezier는 기본값이고 "값과 속도 모두 부드럽다". Ease In Out은 "처음에 느리고 가운데에서 빨라지고 끝에서 다시 느려진다".
  - https://docs.blender.org/manual/en/latest/editors/graph_editor/fcurves/properties.html
- **손떨림.**
  - Blender 설명서는 잡음 변조기를 "카메라 흔들림 같은 효과에 쓸모 있다"고 소개한다. https://docs.blender.org/manual/en/latest/editors/graph_editor/fcurves/modifiers.html [읽음]
  - Ian Hubert와 Nathan Vegdahl의 Camera Shakify는 무작위 잡음이 아니라 "녹화한 데이터를 이음매 없이 반복하게 만든" 실제 카메라 흔들림을 얹는다. 여러 흔들림을 겹치고 영향도를 애니메이션할 수 있다. Blender 4.4 이상, 0.5.1(2026-02-07)이 5.0의 API 변경에 맞춘 수정판이다. 코드는 GPL v3, 흔들림 데이터는 CC0.
    - https://extensions.blender.org/add-ons/camera-shakify/ [읽음]
    - https://github.com/EatTheFuture/camera_shakify [읽음]
    - Hubert가 직접 찍고 추적해 만들었다는 경위는 https://80.lv/articles/free-camera-shake-add-on-for-blender [검색 요약]
  - 세로 화면에서 해가 되는 경우(한 사람의 의견, Adam Sébire): 세로 형식은 "가로 움직임을 과장하는 경향"이 있고 "중간 빠르기의 팬도 관객을 어지럽게 할 수 있다". 손으로 들 때는 흔들림을 줄이라고 한다.
    - https://www.adamsebire.info/vertical-film-festival/9-16-tips-and-tricks/ [읽음]
- **모션 블러와 셔터.**
  - 180도 셔터(널리 합의됨): 셔터가 프레임 시간의 절반 동안 열린다. 24fps에서 약 1/48초. Iain Anderson: 180도는 "우리 눈이 보는 것에 가까운 보기 좋은 모션 블러를 준다". 같은 글의 주장(한 사람의 의견): 규칙을 고집하지 말고 "노출 시간은 프레임 속도가 아니라 피사체의 속도를 반영해야 한다".
    - https://provideocoalition.com/the-180-shutter-angle-rule-is-broken [읽음]
  - Cycles [설명서 5.2 LTS, 읽음 / 실측]: Shutter는 "셔터가 열리기 시작해 완전히 닫힐 때까지의 시간(프레임 단위)". `scene.render.motion_blur_shutter` 기본 0.5, `use_motion_blur` 기본 False, `motion_blur_position` 기본 'CENTER'(START, CENTER, END). 0.5프레임은 프레임 시간의 절반이므로 180도와 같다(이 환산은 단위에서 나오는 계산이다). 제약: "직교 카메라에서는 카메라 모션 블러가 동작하지 않는다", "조명의 움직임은 반영하지 않는다", 입자와 물리는 렌더 전에 굽는다.
    - https://docs.blender.org/manual/en/latest/render/cycles/render_settings/motion_blur.html
  - 물체별 설정 [실측]: `obj.cycles.use_motion_blur`(기본 True), `obj.cycles.motion_steps`(기본 1), `obj.cycles.use_deform_motion`. 롤링 셔터는 `scene.cycles.rolling_shutter_type`(기본 'NONE').

### 찾지 못한 것

움직임의 속도에 대한 숫자 기준(초당 몇 도, 몇 미터)을 주는 실무자 출처는 찾지 못했다. 휩 팬이 모션 블러에 기대어 컷을 잇는다는 설명도 원문을 읽지 못했다(StudioBinder 해당 주소 404).

---

## 5. 9:16 세로 화면의 구도

### 확인한 것

- **가운데 축(한 사람의 의견, Adrian / AP Creative Community).** "가운데 선을 닻으로 써서" 시각적 무게를 가운데에 두면 화면이 깨끗하고 안정된다.
  - https://omgadrian.beehiiv.com/p/master-vertical-video-framing [읽음]
- **3분할은 세로에서도 통한다(한 사람의 의견, Adam Sébire).** "대칭은 역동성이 부족하고 3분할은 여전히 적용된다." 위 Adrian의 말과 방향이 다르다. 둘 다 개인 의견이다.
  - https://www.adamsebire.info/vertical-film-festival/9-16-tips-and-tricks/ [읽음]
- **3분할과 대칭(널리 합의됨, StudioBinder).** 3분할: 교차선 위에 둔다. 대칭: "완벽한 대칭으로 3분할을 깨는 것은 아주 구체적인 이유가 있을 때 쓴다." 가운데 구도는 긴장을 만들고 시선을 모은다.
  - https://www.studiobinder.com/blog/rules-of-shot-composition-in-film/ [읽음]
- **앞에 걸리는 물체와 층(한 사람의 의견 둘이 일치).** Adrian: 세로 영상이 납작해 보이는 것은 모든 것이 한 평면에 있어서다. "카메라 가까이에 무언가를 두라. 앞에 물체 하나만 있어도" 영화처럼 보이는 정도가 달라진다. 렌더 구도 정리(habrador): "주 피사체 앞에 물체를 두어 깊이와 규모를 준다", "틀 안에 관심 지점을 넣어 시선을 모은다".
  - https://omgadrian.beehiiv.com/p/master-vertical-video-framing [읽음]
  - https://blog.habrador.com/2022/06/render-blender-composition-techniques-photography.html [읽음]
- **깊은 공간 구도(널리 합의됨, StudioBinder).** "중요한 요소를 카메라 가까이와 멀리에 함께 둔다." 모두 선명할 필요는 없다.
  - https://www.studiobinder.com/blog/rules-of-shot-composition-in-film/ [읽음]
- **이끄는 선(널리 합의됨).** "화면 안의 실제 선이나 상상의 선이 핵심 요소로 시선을 이끈다."
  - 같은 StudioBinder 글 [읽음]
- **글자 자리.** Adrian: 아래 3분의 1 밑에 놓인 중요한 것은 "묻힌다". 사용자 이름, 캡션, 자막이 그 자리를 차지하기 때문이다. Sébire: 중요한 세부와 글자는 가장자리, 특히 위아래에서 떨어뜨린다. "아래 15~25%"라는 숫자는 검색 요약에만 있었고 원문을 특정하지 못했다.
- **세로에 맞는 피사체와 움직임(한 사람의 의견, Sébire).** 세로 요소가 강한 피사체(선 사람, 건물, 나무)를 고른다. "대부분의 액션은 가로로 일어나고 가로 움직임은 세로의 강점이 아니다."
- **초점 요소·구조·균형(Blender Guru, 검색 요약).** Andrew Price의 "Understanding Composition"은 초점 요소, 구조(3분할, 대칭, 황금비, 피라미드, 화면을 다 쓰기), 균형의 세 단계로 설명한다. 영상을 보지 못했고 장 제목과 요약만 확인했다.
  - https://www.diyphotography.net/?p=15187 [검색 요약]
- **규모의 단서(널리 합의됨).** Darren Rowse: "우리는 평균적인 사람의 크기를 잘 안다. 사람을 넣으면 곧바로 기준점이 생긴다." 사람이 물체 가까이 있을수록 효과가 크다는 말은 검색 요약으로만 봤다.
  - https://digital-photography-school.com/using-the-human-form-in-your-images-to-give-a-sense-of-scale-with-examples/ [읽음]
- **컷 크기의 종류와 대비(널리 합의됨, StudioBinder).** 설정 컷은 장소를 보여 주고, 익스트림 와이드는 피사체를 장소에 비해 작게 보이게 하고, 와이드는 피사체와 주변의 균형, 클로즈업은 중요한 순간, 익스트림 클로즈업은 "다른 크기에서는 보기 어려운 작은 세부"를 보여 준다. "컷 크기의 대비 없이 관객에게 무엇을 알릴 수 있겠는가."
  - https://www.studiobinder.com/blog/types-of-camera-shot-sizes-in-film/ [읽음]
- **같은 크기를 이어 붙이지 않는다(검색 요약).** "같은 크기와 배치의 컷을 연달아 쓰지 않는다", 비슷한 컷을 이으면 튀는 컷(점프 컷)이 된다. 30도 규칙은 이어지는 컷 사이에 카메라 각도를 30도 이상 바꾸라는 것이다. 둘 다 원문을 읽지 못했다.
  - https://gomlab.com/en/blog/230 [검색 요약]
  - https://filmlifestyle.com/what-is-the-30-degree-rule/ [검색 요약]

### 이 프로젝트에 맞춘 해석(조사자의 추론, 출처 없음)

- 위 3분의 1은 글자, 아래는 자막이므로 주인공은 가운데 띠에 있어야 한다. 깊이를 가로로 펼 자리가 없으니 세로로 쌓는다: 아래에 앞쪽 바닥이나 걸리는 물체, 가운데에 주인공, 위에 어두운 배경(글자 자리).
- "슬라이드 쇼 같다"는 느낌에 대해 직접 말한 출처는 없다. 위 두 요약(같은 크기 연속 금지, 30도 규칙)과 StudioBinder의 "컷 크기의 대비"가 가장 가까운 근거다.

---

## 6. bpy 구현 (Blender 5.2.2 LTS에서 실행해 확인)

아래 코드는 모두 `blender -b --factory-startup --python`으로 실행해 오류 없이 돌았다.

### 6.1 확인한 API

| 항목 | 5.2.2 LTS에서의 상태 |
|---|---|
| `cam.data.lens`, `sensor_width`, `sensor_height`, `sensor_fit`, `shift_x`, `shift_y`, `clip_start`, `clip_end` | 있음 [실측] |
| `cam.data.dof.use_dof`, `focus_object`, `focus_subtarget`, `focus_distance`, `aperture_fstop`, `aperture_blades`, `aperture_rotation`, `aperture_ratio` | 있음 [실측] |
| `scene.render.use_motion_blur`, `motion_blur_shutter`, `motion_blur_position`, `motion_blur_shutter_curve` | 있음 [실측]. Cycles 전용 속성이 아니라 `scene.render`에 있다 |
| `obj.constraints.new('TRACK_TO')`, `'DAMPED_TRACK'`, `'LOCKED_TRACK'`, `'FOLLOW_PATH'` | 있음 [실측]. 새 Track To의 기본값은 `TRACK_NEGATIVE_Z`, `UP_Y`(코드로 만든 경우) |
| `Object.camera_fit_coords(depsgraph, coordinates)` | 있음 [실측]. 위치 벡터와 직교 배율을 돌려준다. 회전은 바꾸지 않는다 |
| `bpy_extras.object_utils.world_to_camera_view(scene, obj, coord)` | 있음 [실측]. (0,0)이 왼쪽 아래, (1,1)이 오른쪽 위. z는 카메라 축 위의 깊이, 음수면 카메라 뒤. `shift_x/y`, 화각, 센서 크기를 반영한다(함수 설명문) |
| `Keyframe.interpolation`, `Keyframe.easing` | 있음 [실측]. 보간: CONSTANT, LINEAR, BEZIER, SINE, QUAD, CUBIC, QUART, QUINT, EXPO, CIRC, BACK, BOUNCE, ELASTIC. 이징: AUTO, EASE_IN, EASE_OUT, EASE_IN_OUT |
| `fcurve.modifiers.new('NOISE')` | 있음 [실측]. 속성: `blend_type`(기본 REPLACE), `scale`, `strength`, `phase`, `offset`, `depth`, `lacunarity`, `roughness`, `use_legacy_noise`, `use_restricted_range`, `frame_start`, `frame_end`, `blend_in`, `blend_out`, `influence` |
| **`action.fcurves`** | **없음** [실측: AttributeError]. 5.0 릴리스 노트: "옛 Action API를 제거했다"(`action.fcurves`, `action.groups`, `action.id_root`). `bpy_extras.anim_utils.action_get_channelbag_for_slot(action, slot)`의 `.fcurves`를 쓴다. https://developer.blender.org/docs/release_notes/5.0/python_api/ [읽음] |

### 6.2 실행해서 알게 된 것 [실측]

1. **`shift_y`의 방향과 단위.** `sensor_fit='AUTO'`, 1080x1920에서 `shift_y`를 +0.1 하면 물체가 화면에서 **아래로** 화면 높이의 0.1만큼 내려간다(상자의 세로 범위 0.342~0.683 → 0.242~0.583). −0.1이면 그만큼 올라간다. `sensor_fit='HORIZONTAL'`에서는 같은 0.1이 화면 높이의 0.0563만큼만 옮긴다(단위가 화면 폭이기 때문, 0.1 × 1080/1920).
2. **Track To는 수평을 지키고 Damped Track은 지키지 않는다.** 같은 표적을 볼 때 Track To 카메라의 가로축은 수평(z 성분 0.0)이었고 Damped Track 카메라의 가로축은 z 성분 −0.655로 크게 기울었다. 설명서도 Damped Track은 "추적 축 둘레의 회전을 줄이는 순수 스윙 회전"이라고 하고, Track To는 "표적 바로 위에 가까우면 불안정해지므로 그때는 Damped Track을 권한다"고 한다.
   - https://docs.blender.org/manual/en/latest/animation/constraints/tracking/track_to.html [읽음]
   - https://docs.blender.org/manual/en/latest/animation/constraints/tracking/damped_track.html [읽음]
3. **Track To가 걸린 카메라에 회전 잡음을 넣어도 움직이지 않는다.** `delta_rotation_euler`에 잡음을 넣어도 세 프레임의 방향이 같았다. 동작하는 방법은 둘이다. (a) 빈 물체(리그)에 Track To를 걸고 카메라를 자식으로 둔 뒤 카메라의 `rotation_euler`에 잡음을 넣는다. (b) 표적 빈 물체의 `location`에 잡음을 넣는다.
4. **잡음의 섞기 방식.** 값이 0인 곡선에 `strength=1`로 넣고 재면 REPLACE는 −0.33~+0.33, 평균 0.000이었고 ADD는 0.17~0.83, 평균 0.500이었다. ADD는 카메라를 한쪽으로 밀어 놓는다. 흔들림에는 REPLACE(기본값)를 쓴다. 설명서의 범위 표기(Replace [−0.5, 0.5], Add [0, 1])와 방향이 같다.
5. **`camera_fit_coords`는 위치만 준다.** Track To가 걸린 카메라를 그 위치로 옮기면 표적을 다시 조준하면서 화면이 달라진다. 테스트에서 옮긴 뒤 상자의 가로 범위가 0.033~1.034로 오른쪽이 넘쳤다. 옮긴 뒤 반드시 `world_to_camera_view`로 다시 잰다.
6. **Follow Path.** `use_fixed_location=True`로 두고 `offset_factor`(0~1)에 키를 넣으면 곡선 위의 위치를 프레임과 무관하게 직접 움직일 수 있다. 이징도 이 값에 건다.

### 6.3 리그와 검사 코드

```python
import bpy, math
from mathutils import Vector
from bpy_extras import anim_utils
from bpy_extras.object_utils import world_to_camera_view

scene = bpy.context.scene

def fcurves_of(idblock):
    """Blender 5.x: action.fcurves 가 없다."""
    ad = idblock.animation_data
    return anim_utils.action_get_channelbag_for_slot(ad.action, ad.action_slot).fcurves

def ease(idblock, interpolation='SINE', easing='EASE_IN_OUT'):
    for fc in fcurves_of(idblock):
        for kp in fc.keyframe_points:
            kp.interpolation = interpolation
            kp.easing = easing
        fc.update()

def make_rig(name, cam_loc, aim_loc, lens):
    """rig(위치, Track To) > cam(흔들림만) / aim(보는 곳이자 초점)."""
    aim = bpy.data.objects.new(name + "_aim", None)
    rig = bpy.data.objects.new(name + "_rig", None)
    cam = bpy.data.objects.new(name + "_cam", bpy.data.cameras.new(name))
    for o in (aim, rig, cam):
        scene.collection.objects.link(o)
    aim.location, rig.location = aim_loc, cam_loc
    cam.parent = rig
    con = rig.constraints.new('TRACK_TO')
    con.target, con.track_axis, con.up_axis = aim, 'TRACK_NEGATIVE_Z', 'UP_Y'
    cam.data.lens = lens
    cam.data.dof.use_dof = True
    cam.data.dof.focus_object = aim
    scene.camera = cam
    return rig, cam, aim

def add_shake(cam, rot_deg, period_frames, seed=0.0):
    """자식 카메라의 회전에만 건다. blend_type 은 REPLACE(기본) 그대로 둔다."""
    cam.keyframe_insert("rotation_euler", frame=scene.frame_start)
    for fc in fcurves_of(cam):
        if fc.data_path != "rotation_euler":
            continue
        m = fc.modifiers.new('NOISE')
        m.scale = period_frames
        m.strength = math.radians(rot_deg)
        m.phase = seed + 17.3 * fc.array_index   # 축마다 다른 잡음
```

`rot_deg`와 `period_frames`에 넣을 값은 출처가 없다. 사용자가 고를 수 있게 여러 안을 렌더한다.

```python
def frame_box(cam, objs):
    """물체들의 경계 상자가 화면에서 차지하는 범위. 0~1, 원점은 왼쪽 아래."""
    bpy.context.view_layer.update()
    pts = [o.matrix_world @ Vector(c) for o in objs for c in o.bound_box]
    ndc = [world_to_camera_view(scene, cam, p) for p in pts]
    return dict(x0=min(p.x for p in ndc), x1=max(p.x for p in ndc),
                y0=min(p.y for p in ndc), y1=max(p.y for p in ndc),
                zmin=min(p.z for p in ndc))   # zmin <= 0 이면 카메라 뒤에 걸린다

def fit_to_band(cam, objs, band):
    """카메라를 기울이지 않고 shift_y 만으로 물체 중심을 띠의 중심에 맞춘다.
    sensor_fit='AUTO' 이고 세로 화면일 때 shift_y 1.0 == 화면 높이."""
    for _ in range(20):
        b = frame_box(cam, objs)
        err = (b['y0'] + b['y1']) / 2 - (band[0] + band[1]) / 2
        if abs(err) < 1e-4:
            break
        cam.data.shift_y += err
    return frame_box(cam, objs)
```

`band`는 프로젝트가 정한다(글자가 위 3분의 1이면 상한은 0.667 이하, 하한은 자막 높이에 맞춘다). 시험 실행: 4.4 x 1.8 x 1.4m 상자, 35mm, 카메라 (4.2, −5.0, 0.45)에서 `band=(0.30, 0.66)`으로 맞추니 세로 범위 0.363~0.670이 0.327~0.633으로 옮겨졌고 `shift_y`는 0.037이었다. 같은 실행에서 가로 범위가 −0.041~1.177로 화면을 넘는다는 것도 숫자로 드러났다. 이 검사가 잡아야 하는 경우다.

```python
def dof_limits(cam, c_mm=0.025):
    """선명한 범위(m). c_mm 은 허용 착란원. 0.025mm 는 위키백과가 적은 35mm 영화의 현대 실무값."""
    d = cam.data
    f, N = d.lens, d.dof.aperture_fstop
    bpy.context.view_layer.update()
    if d.dof.focus_object:
        s = -(cam.matrix_world.inverted() @ d.dof.focus_object.matrix_world.translation).z * 1000.0
    else:
        s = d.dof.focus_distance * 1000.0
    H = f * f / (N * c_mm) + f
    near = H * s / (H + (s - f))
    far = H * s / (H - (s - f)) if H > (s - f) else float('inf')
    return near / 1000.0, far / 1000.0

def roll_deg(cam):
    """화면의 기울기. Track To 리그에 흔들림이 없으면 0 이어야 한다."""
    return math.degrees(math.asin(cam.matrix_world.col[0].normalized().z))

def max_centre_step(cam, obj, f0, f1):
    """프레임 사이에 물체 중심이 화면에서 움직인 최대 거리(화면 비율)."""
    prev, worst = None, 0.0
    for f in range(f0, f1 + 1):
        scene.frame_set(f)
        b = frame_box(cam, [obj])
        c = Vector(((b['x0'] + b['x1']) / 2, (b['y0'] + b['y1']) / 2))
        if prev is not None:
            worst = max(worst, (c - prev).length)
        prev = c
    return worst
```

```python
# 푸시 인: 리그의 위치에 키 두 개, 이징
rig.keyframe_insert("location", frame=1)
rig.location = (3.4, -4.0, 0.5)
rig.keyframe_insert("location", frame=96)
ease(rig)

# 초점 이동: 초점 물체를 비우고 거리에 키
cam.data.dof.focus_object = None
cam.data.dof.focus_distance = 2.0
cam.data.dof.keyframe_insert("focus_distance", frame=1)
cam.data.dof.focus_distance = 8.0
cam.data.dof.keyframe_insert("focus_distance", frame=48)
ease(cam.data)        # 카메라 데이터의 액션은 물체의 액션과 따로다

# 궤도: 원 곡선 + Follow Path
path = ...            # bpy.ops.curve.primitive_bezier_circle_add 로 만든 곡선
fp = rig.constraints.new('FOLLOW_PATH')
fp.target, fp.use_fixed_location = path, True
fp.offset_factor = 0.0; fp.keyframe_insert("offset_factor", frame=1)
fp.offset_factor = 0.2; fp.keyframe_insert("offset_factor", frame=96)

# 모션 블러: 180도 셔터
scene.render.use_motion_blur = True
scene.render.motion_blur_shutter = 0.5
scene.render.motion_blur_position = 'CENTER'
```

제약 조건의 순서: Follow Path를 Track To보다 먼저 추가해야 위치를 정한 뒤 조준한다. 이 순서 의존은 제약 조건이 위에서 아래로 계산된다는 일반 동작에 따른 것이고, 위 조합의 순서를 바꿔 따로 시험하지는 않았다.

### 6.4 렌더한 정지 프레임을 확인하는 명령

`ffmpeg`가 이 컴퓨터에 있다(`~/.local/bin/ffmpeg`). ImageMagick은 없다.

```bash
# 회색조 + 작은 그림(명암 구조와 축소 가독성)
ffmpeg -i frame.png -vf "format=gray,scale=135:240" check_gray_thumb.png
# 실눈 대용: 흐리게
ffmpeg -i frame.png -vf "gblur=sigma=20" check_blur.png
```

실루엣은 Blender에서 물체 마스크(Object Index 또는 Cryptomatte 패스)를 내어 검은 모양으로 확인한다. 이 절차는 실행해 보지 않았다.

---

## 7. 아마추어·AI 티가 나는 카메라와 전문가의 확인 방법

### 티가 나는 것

직접 "AI 티"를 다룬 실무자 출처는 없다. 아래는 위 출처들이 말한 것을 뒤집어 정리한 것이고, 근거 절을 붙였다.

| 티 | 근거 |
|---|---|
| 실제 장비로 불가능한 움직임(물체를 뚫고 지나감, 끝없이 가속하는 비행) | 픽사의 원칙(4절, 일부 검색 요약). "CG 카메라가 물리적으로 있을 수 없는 곳에 있으면 가짜로 느낀다"는 정리는 검색 요약 |
| 일정한 속도로 시작하고 멈추는 움직임(Linear 보간) | 12원칙의 가속·감속, Blender 설명서의 Linear 설명(4절) |
| 큰 물체에 지나치게 얕은 심도 | Art Adams, 위키백과(3절) |
| 큰 물체를 높은 곳에서 내려다봄 | 위키백과 Miniature faking(2절) |
| 광각으로 너무 가까이 가서 제품이 불룩함, 너무 멀어 뭉툭함 | Karl Taylor(1절) |
| 모든 컷이 같은 크기, 같은 각도 | StudioBinder 컷 크기 대비, 30도 규칙(5절, 일부 검색 요약) |
| 모든 것이 한 평면 | Adrian, StudioBinder 깊은 공간(5절) |
| 세로 화면에서 빠른 좌우 팬 | Adam Sébire(4절) |
| 한쪽으로 치우치거나 주기가 보이는 기계적 흔들림 | 6.2의 실측(ADD), Camera Shakify가 녹화 데이터를 쓰는 이유(4절) |
| 모션 블러 없는 빠른 움직임 | 180도 셔터가 관례인 까닭(4절) |
| 까닭 없는 더치 앵글이나 롤 | StudioBinder: 불안과 혼란을 뜻한다(2절, 4절) |

### 확인 방법(널리 쓰임, 화가 Dan Scott의 정리)

- **실눈 검사**: "그림과 대상을 실눈으로 보고 눈에 띄는 문제를 찾는다." 큰 모양과 명암을 본다.
- **작은 그림 검사**: 작은 그림으로 봐도 그럴듯하면 기본이 맞은 것이다.
- **회색조 검사**: 회색조로 바꾸면 명암 구조가 드러난다. 가장 밝은 곳, 가장 어두운 곳, 밝고 어두운 덩어리의 배치를 본다.
  - https://drawpaintacademy.com/painting-tests/ [읽음]
- **실루엣 검사(검색 요약)**: 안쪽 세부를 지우고 검게 채운 모양만으로 무엇인지, 무엇을 하는지 읽혀야 한다. 애니메이션의 "연출(staging)" 원칙에 딸린 검사로 소개된다. 원문을 읽지 못했다.
- **구도는 조명 전에 정한다(Karl Taylor)**: 조명을 시작한 뒤 구도를 바꾸면 조명도 다시 해야 한다.

---

## 규칙 후보

각 규칙은 (가) 할 일, (나) 확인 방법, (다) 근거 순이다. "합의"는 여러 출처가 같은 말을 하는 것, "의견"은 한 사람의 말, "실측"은 Blender에서 확인한 것이다.

1. **컷마다 렌즈·높이·거리를 고른 까닭을 한 줄로 적는다. 기본값(50mm, `shift` 0, 눈높이)을 그대로 둔 컷을 만들지 않는다.**
   (나) 스크립트에서 컷별 `lens`, 카메라 높이, 물체까지의 거리를 표로 출력한다. 값이 모두 같으면 실패.
   (다) StudioBinder 눈높이 = 중립, 초점 거리별 효과 [합의]. 기본값이 아마추어처럼 보인다는 직접 출처는 없음(추론).

2. **실무자의 mm 숫자를 쓸 때는 `sensor_fit='HORIZONTAL'`로 두거나 1절의 표로 환산한다.**
   (나) `cam.data.view_frame(scene=scene)`으로 가로 화각을 계산해 로그에 남긴다.
   (다) [실측] 세로 AUTO에서 50mm의 가로 화각은 22.9°(가로 화면의 89mm).

3. **제품의 모양을 깨끗하게 보일 컷은 멀리서 길게, 위압감·속도감 컷은 가까이서 넓게 찍는다. 같은 화면 크기를 유지하면서 거리와 렌즈를 함께 바꾼다.**
   (나) 컷별 거리와 `lens`를 출력한다. 정지 프레임에서 가까운 쪽 바퀴와 먼 쪽 바퀴의 화면 크기 비를 `world_to_camera_view`로 잰다(광각 근접일수록 비가 크다).
   (다) 위키백과 Perspective distortion, Robert Hall [합의]. Hurlbut: 깔끔한 차 광고 27mm 이상, 액션 14.5mm [의견].

4. **차와 상자형 물체의 기본 주인공 컷은 3/4 뷰로 두 면을 보인다.**
   (나) 정지 프레임에서 앞면과 옆면이 둘 다 보이는지 본다. 카메라 방위각을 출력한다.
   (다) Robert Hall, TutKit(옆 2/3, 앞 1/3), habrador의 45도 [합의].

5. **높이로 뜻을 정한다. 낮게 = 위압·힘, 높게 = 내려다봄·작아 보임, 바로 위 = 중립·도식, 눈높이 = 중립. 큰 물체를 작아 보이게 할 뜻이 없으면 높은 각도와 얕은 심도를 함께 쓰지 않는다.**
   (나) 카메라 z와 조준점 z의 차, 내려다보는 각을 출력한다.
   (다) StudioBinder, Karl Taylor [합의]. 위키백과 Miniature faking.

6. **물체를 가운데 띠로 옮길 때 카메라를 기울이지 않고 `shift_y`를 쓴다.**
   (나) `frame_box()`의 y0, y1이 프로젝트가 정한 띠 안에 있는지 모든 키 프레임에서 검사한다. x0 ≥ 0, x1 ≤ 1, zmin > 0도 검사한다(의도해서 화면을 넘기는 클로즈업은 예외로 적어 둔다).
   (다) Blender 설명서 Shift [읽음], `shift_y`의 방향과 단위 [실측].

7. **수평을 지킬 컷은 Track To(`TRACK_NEGATIVE_Z`, `UP_Y`)를 쓴다. Damped Track은 바로 위에서 내려다보는 컷에만 쓴다.**
   (나) `roll_deg(cam)`이 흔들림을 끈 상태에서 0인지 확인한다.
   (다) Blender 설명서 [읽음], 실측(Damped Track은 가로축이 기울었다).

8. **기울기(더치·롤)는 불안이나 혼란을 말하려는 컷에만 쓴다.**
   (나) `roll_deg(cam)`이 0이 아닌 컷에 대본의 까닭이 적혀 있는지 본다.
   (다) StudioBinder [합의].

9. **초점은 빈 물체(`dof.focus_object`)로 잡고, 물체 전체가 선명해야 하는 컷은 `dof_limits()`로 물체의 앞뒤가 범위에 드는지 계산한다. 세부 클로즈업에서만 얕게 한다.**
   (나) `dof_limits()`의 near, far와 `frame_box()`의 깊이 범위를 비교한다. 정지 프레임에서 물체의 가장 먼 모서리가 선명한지 본다.
   (다) Art Adams, 위키백과 [합의]. 실제 차 촬영 f/5.6~f/16 [의견: Hall, Taylor]. Cycles와의 대조는 하지 않음.

10. **초점 이동은 시선을 옮길 까닭이 있을 때만 하고, `focus_distance`에 키를 넣어 이징한다.**
    (나) 시작과 끝 프레임에서 각각 선명한 물체가 다른지 정지 프레임으로 본다.
    (다) StudioBinder rack focus [합의].

11. **카메라는 실제 장비가 할 수 있는 움직임 하나만 한다(푸시 인, 풀 아웃, 아크, 크레인, 트럭). 물체를 뚫지 않는다. 움직임마다 뜻을 적는다.**
    (나) 리그의 위치 곡선이 직선이나 호 하나인지 본다. 모든 프레임에서 `zmin > clip_start`이고 카메라 위치가 다른 물체의 경계 상자 안에 들어가지 않는지 검사한다.
    (다) Patrick Lin [읽음], StudioBinder 움직임의 뜻 [합의]. "불가능한 움직임이 가짜로 보인다"는 검색 요약.

12. **움직임의 처음과 끝에 가속·감속을 넣는다. Linear 보간으로 시작하고 멈추지 않는다. 컷이 움직임 도중에 잘리는 경우는 예외로 적는다.**
    (나) 리그의 키 프레임 `interpolation`을 출력해 LINEAR와 CONSTANT가 없는지 본다. `max_centre_step()`을 프레임별로 뽑아 처음과 끝이 가운데보다 작은지 본다.
    (다) 12원칙, Blender 설명서 [합의].

13. **깊이는 시차로 만든다. 줌(`lens` 애니메이션)이 아니라 카메라를 옮기고, 앞에 걸리는 물체를 하나 둔다.**
    (나) 첫 프레임과 끝 프레임에서 앞 물체와 주인공의 화면 위치 변화량이 다른지 `world_to_camera_view`로 잰다. 같으면 시차가 없다.
    (다) Adrian, habrador, StudioBinder 깊은 공간 [의견 여럿이 일치]. 달리와 줌의 차이는 검색 요약.

14. **세로 화면에서는 좌우 팬과 빠른 가로 이동을 줄이고, 앞뒤(푸시·풀)와 위아래(크레인·틸트) 움직임을 먼저 고른다.**
    (나) 컷별로 물체 중심의 화면 이동을 x와 y로 나눠 출력한다.
    (다) Adam Sébire [의견]. 속도의 숫자 기준은 없음.

15. **손떨림은 넣을 때만 넣는다. 자식 카메라의 회전에 REPLACE 잡음으로 넣고, 세기는 여러 안을 렌더해 사용자가 고른다. 삼각대·달리 컷으로 읽혀야 하는 제품 컷에는 넣지 않는다.**
    (나) 잡음 곡선을 `fc.evaluate()`로 뽑아 평균이 0에 가까운지 본다. Track To가 걸린 물체가 아니라 자식 카메라에 걸렸는지 본다.
    (다) [실측] ADD는 평균 0.5로 치우침, Track To 카메라의 회전 잡음은 무효. Blender 설명서, Camera Shakify. 넣을지 말지의 기준은 StudioBinder(핸드헬드 = 날것·혼란·친밀) [합의].

16. **모션 블러를 켜고 셔터를 0.5프레임(180도)으로 둔다. 다른 값은 까닭이 있을 때만 쓴다.**
    (나) `scene.render.use_motion_blur is True`, `motion_blur_shutter == 0.5`. 빠른 컷의 정지 프레임에서 움직이는 가장자리가 번지는지 본다.
    (다) Blender 설명서, Iain Anderson [합의]. 직교 카메라와 움직이는 조명은 제약.

17. **이어지는 컷의 크기를 바꾼다(전체 → 중간 → 세부 삽입). 같은 크기·같은 각도의 컷을 연달아 두지 않는다.**
    (나) 컷별로 `frame_box()`의 넓이(물체가 화면에서 차지하는 비율)와 카메라 방위각을 표로 출력해 이웃한 컷끼리 비교한다.
    (다) StudioBinder 컷 크기 대비 [읽음]. "같은 크기 연속 금지", 30도 규칙은 검색 요약.

18. **가운데 구도는 뜻이 있을 때 쓴다(정면 대칭, 위압). 그 밖에는 물체를 3분할 선 쪽으로 옮기되, 세로 화면에서는 가운데 세로축에 무게를 두는 것도 통한다. 두 방식을 컷마다 정해 적는다.**
    (나) `frame_box()`의 중심 x가 0.5인지 3분의 1 근처인지 출력한다. 카메라 보기에서 `cam.data.show_composition_thirds`를 켜 확인할 수 있다.
    (다) StudioBinder [합의]. Adrian(가운데)과 Sébire(3분할)는 서로 다른 의견.

19. **큰 물체의 규모는 크기를 아는 것(사람, 문, 차)을 물체 가까이에 두어 보인다.**
    (나) 정지 프레임에 기준 물체가 보이고 주인공과 같은 깊이에 있는지 본다.
    (다) Darren Rowse [읽음]. 가까이 둘수록 효과가 크다는 말은 검색 요약.

20. **구도와 카메라를 먼저 정하고 조명을 한다. 카메라를 바꾸면 조명을 다시 확인한다.**
    (나) 낮은 샘플의 회색 재질 렌더로 구도를 먼저 뽑아 검사한 뒤 조명 단계로 간다.
    (다) Karl Taylor [의견].

21. **정지 프레임마다 세 가지를 본다. 회색조 축소본에서 주인공이 가장 대비가 큰 곳인가, 흐리게 했을 때 큰 모양이 읽히는가, 검게 채운 실루엣만으로 무엇인지 아는가.**
    (나) 6.4의 `ffmpeg` 명령으로 회색조 축소본과 흐린 그림을 만들어 본다. 실루엣은 마스크 패스로 본다.
    (다) Dan Scott [읽음]. 실루엣 검사는 검색 요약.

22. **애니메이션 곡선은 `anim_utils.action_get_channelbag_for_slot()`으로 얻는다. `action.fcurves`를 쓰지 않는다.**
    (나) 스크립트를 5.2에서 실행해 AttributeError가 없는지 본다.
    (다) 5.0 릴리스 노트 [읽음], 실측.

23. **`camera_fit_coords`로 옮긴 뒤에는 화면 범위를 다시 잰다.**
    (나) 옮긴 뒤 `frame_box()`를 다시 계산한다.
    (다) [실측] Track To와 함께 쓰면 옮긴 뒤 다시 조준해 화면이 달라진다.

---

## 확인하지 못한 것

- **Gleb Alexandrov, CG Cookie, Ian Hubert가 카메라와 구도에 대해 직접 한 말.** 검색에서 조명 강의와 Camera Shakify만 나왔다. Blender Guru의 구도 강의는 장 제목과 요약만 확인했고 영상은 보지 못했다(이 작업 환경에서는 영상을 재생하지 못한다).
- **ASC의 글.** theasc.com의 두 글(Toy Story 4의 가상 Cooke 렌즈, 아나모픽 광학)은 접속이 끊겨 읽지 못했다. 같은 내용 일부를 No Film School의 Patrick Lin 인터뷰로 대신했다.
- **전체 CG 차 광고의 카메라 제작기.** The Mill의 Blackbird 기사는 검색 요약만 봤고 카메라 선택에 대한 내용은 없었다. 차 광고의 렌즈 숫자는 실사 촬영감독(Hurlbut, Luong)의 것이다.
- **픽사가 "실제 카메라가 못 하는 것은 하지 않는다"고 한 원문.** kottke.org와 AWN 글을 읽지 못했다(접속 끊김, 403). 검색 요약으로만 확인했다.
- **움직임 속도, 흔들림 세기, 컷 길이의 숫자 기준.** 출처를 찾지 못했다. 문서에 기준 숫자를 적지 않았다.
- **"기본 50mm·눈높이가 아마추어처럼 보인다", "같은 크기의 컷이 이어지면 슬라이드 쇼 같다"를 직접 말한 출처.** 가까운 근거만 있다. 문서에서 추론으로 표시했다.
- **자막 안전 영역의 비율("아래 15~25%").** 검색 요약에만 있고 원문을 특정하지 못했다. 가운데 띠의 경계는 프로젝트의 실제 글자 배치로 정해야 한다.
- **"휠 허브 높이", "35~70mm"라는 자동차 사진 조언의 원문.** 검색 요약에만 있었다.
- **휩 팬과 달리 컷에 대한 StudioBinder 글.** 주소가 404였다. 달리와 줌의 시차 차이, 30도 규칙, 실루엣 검사, 아나모픽 보케의 원리는 검색 요약만 봤다.
- **Cycles의 심도가 표준 광학식과 같은 값을 내는지.** `dof_limits()`는 식으로 계산한 값이고 렌더와 대조하지 않았다. 장면 단위 배율(`unit_settings.scale_length`)이 흐림에 주는 영향도 확인하지 않았다.
- **렌더 결과로 확인하지 않은 것.** 이번 조사에서 렌더는 하지 않았다. `aperture_ratio`의 타원 보케 모양, 모션 블러의 실제 모습, 마스크 패스로 실루엣을 뽑는 절차, Follow Path와 Track To의 순서 의존은 실행해 보지 않았다.
- **Blender API 온라인 문서.** docs.blender.org/api/current의 해당 페이지는 너무 길어 본문을 받지 못했다. 대신 설치된 5.2.2 LTS에서 속성과 함수를 직접 조회하고 실행했다. 5.0과 5.1에서의 동작은 확인하지 않았다(`action.fcurves` 제거는 5.0 릴리스 노트로 확인).
- **Camera Shakify의 5.2 동작.** 확장 페이지는 "4.4 이상"이라고 하고 0.5.1이 5.0의 변경에 맞춘 것까지 확인했다. 5.2에 설치해 돌려 보지는 않았다.
