# 무료 3D 에셋: 어디에 있고, 어떻게 고르고, 가져와서 어떻게 고치나

조사일: 2026-10-08 (한국 시간). 계기: 사용자가 "멋진 무료 3D 에셋을 써라. 코드로 만들거나, 무료 에셋을 가져오거나, 가져와서 고쳐서 감탄이 나올 만큼의 디테일로 만들어라"고 했다.

이 문서는 [에셋 스킬](../../.agents/skills/reels-assets/SKILL.md)과 [무료 도구 조사](../asset-generation/free-tools.md)에 없는 것만 더한다. AI 3D 생성 서비스의 한도와 동작 도구는 그쪽에 있다.

**확인 표시**: `열어 봄` = 오늘 그 페이지나 API를 직접 열어 문구를 읽었다. `요약만` = 검색 결과의 요약만 봤다. `못 엶` = 열려고 했지만 막혔다. `돌려 봄` = 이 컴퓨터의 Blender 5.2.2 LTS에서 직접 실행했다. 후보 모델은 하나도 내려받지 않았고 렌더하지 않았다. 품질은 판단하지 않았다.

## 요약

상업적으로 쓸 수 있고 작업자가 로그인 없이 받을 수 있는 무료 재료는 세 갈래다. 재질·환경광·소품은 Poly Haven과 ambientCG(둘 다 CC0), 주인공급 기계와 건물은 Sketchfab의 CC BY 모델, 실제 로봇의 정확한 형상은 로봇 회사가 공개한 시뮬레이션용 모델(MuJoCo Menagerie, BSD·Apache 계열)이다. GrabCAD와 3D ContentCentral의 공학용 CAD는 약관이 상업적 공개 사용을 막고 있어 쓰지 않는다. 받은 모델은 대개 그대로 쓸 수 없다. 이 프로젝트의 옵티머스 모델을 점검해 보니 키가 16미터로 들어오고 재질 여섯 개에 텍스처가 하나도 없었다. 그래서 순서는 "찾는다 → 수치로 점검한다 → 장면 조명에서 렌더해 본다 → 크기·노멀·모서리·재질·흠집·로고를 고친다"가 된다. 반복해서 나오는 열한 가지 물건을 찾아본 결과, 터보팬 엔진·산업용 로봇 팔·컨테이너선·건물·금괴·서버 랙은 쓸 만해 보이는 무료 후보가 있고, 메가팩·신형 아틀라스·웨이퍼·전기차 배터리 팩은 마땅한 것이 없어 가져온 부품에 코드로 만든 부품을 붙여야 한다.

## 1. 어디에 있나 (출처 표)

| 곳 | 잘하는 것 | 라이선스 | 출처 표시 | 작업자가 받을 수 있나 | 확인 | URL |
|---|---|---|---|---|---|---|
| Poly Haven | 실물 재질 866개, 환경광 997개(스튜디오 조명 96개), 모델 521개(공구·통·가구·식물. 산업 분류 97개). 주인공급 기계와 차량은 없다 | CC0. "상업 작업 포함 어떤 목적이든" | 필요 없음 | 된다. API에 키가 필요 없다. 요청에 프로그램 이름을 담은 User-Agent를 넣어야 한다 | 열어 봄(라이선스, API 약관). 개수는 API로 셈 | https://polyhaven.com/license , https://github.com/Poly-Haven/Public-API |
| ambientCG | 재질 2013개, 표면 흠집 맵(SurfaceImperfections, Fingerprints, 긁힘, 얼룩), 데칼 127개, 환경광 433개, 3D 모델 2900개 | CC0 1.0 | 필요 없음 | 된다. API가 있다. 한 사람이 운영해 안정성을 보장하지 않는다고 적혀 있다 | 열어 봄(라이선스, API 안내). 개수는 API로 셈 | https://docs.ambientcg.com/license/ |
| Sketchfab (내려받기 가능 모델) | 주인공급 기계·차량·건물·로봇이 가장 많다. 박물관 스캔도 여기 있다 | 모델마다 다르다. CC BY, CC BY-SA, CC BY-ND, CC BY-NC 계열, CC0, Standard, Editorial | CC0 말고는 필요. 권장 문구: "This work is based on [모델명] by [제작자] licensed under [라이선스]" | 검색 API는 로그인 없이 된다(`downloadable=true&license=by` 또는 `cc0`). 내려받기는 계정 토큰이 필요하다(연결 도구가 맡는다) | 열어 봄(라이선스 도움말, 표기 도움말, Standard·Editorial 문구). 검색 API는 직접 호출함. 내려받기 API 문서는 못 엶 | https://help.sketchfab.com/en/articles/16152217 , https://sketchfab.com/licenses |
| Fab (무료 항목, Megascans) | 스캔한 표면·바위·식물, 게임용 환경 묶음. 2주마다 유료 상품 몇 개가 기간 한정 무료로 풀린다 | Fab Standard License: 상업 사용, 수정, 언리얼 밖의 도구 사용 가능. 에셋만 따로 되팔거나 나눠 주기 금지. 일부 항목은 CC BY | Standard는 필요 없음. CC BY 항목은 필요 | 계정이 있어야 한다(연결 도구가 맡는다). 웹 페이지는 자동 요청을 막는다(403) | 라이선스 요약은 웹 보관소의 2026-09-10 사본으로 읽음. 기간 한정 무료는 포럼 공지(2026-07-28)를 열어 봄. Megascans의 현재 무료 범위는 요약만 | https://www.fab.com/eula |
| BlenderKit (무료 등급) | Blender 전용이라 재질과 수정자가 살아 있는 `.blend`로 온다. 무료 로봇 팔, 컨테이너, 건물이 있다 | Royalty Free: 상업 사용 가능, 표시 불필요, 에셋 자체를 같은 형태로 되파는 것만 금지. 또는 CC0 | 필요 없음 | 검색 API는 로그인 없이 된다(`is_free:true`). 무료 모델 하나의 내려받기 주소도 로그인 없이 받아졌다(파일은 받지 않았다). 자동 내려받기를 약관이 허용하는지는 확인 못 함 | 열어 봄(라이선스 문서. 주소가 blendkit.com으로 넘어간다). API는 직접 호출함 | https://www.blenderkit.com/docs/licenses/ |
| Smithsonian 3D | 박물관 소장품 스캔. 우주선 부품, 유물 | CC0로 표시된 것만 | 필요 없음 | 연결 도구가 있다. 웹 페이지는 403으로 못 엶 | 요약만 | https://3d.si.edu/cc0 |
| NASA 3D Resources | 우주선, 탐사차, 위성, 지형 | "저작권 없음"(저장소 설명). 상업 사용 때 NASA가 보증하는 것처럼 보이면 안 된다. NASA 휘장과 로고는 공개 저작물이 아니다 | 요청 사항 | 된다. GitHub 저장소 | 열어 봄(저장소 설명, 사용 지침) | https://github.com/nasa/NASA-3D-Resources , https://www.nasa.gov/nasa-brand-center/images-and-media/ |
| MuJoCo Menagerie (로봇 회사 공개 모델) | 실제 로봇의 정확한 형상과 관절 구조. Unitree G1·H1, Booster T1, Fourier N1, Apptronik Apollo, Boston Dynamics Spot, UR5e·UR10e, KUKA iiwa 14, Franka. 아틀라스와 옵티머스는 없다 | 모델 폴더마다 다르다. Unitree·KUKA iiwa는 BSD-3-Clause, Booster·Fourier·Franka는 Apache-2.0 | 저작권 고지와 라이선스 글을 함께 보관한다 | 된다. GitHub | 열어 봄(저장소 목록). 모델 파일은 열지 않았다. 시뮬레이션용이라 겉면이 단순할 수 있다 | https://github.com/google-deepmind/mujoco_menagerie |
| Khronos glTF 샘플 | 재질 표현이 정확한 견본(자동차 도장, 탄소 섬유, 시계). 가져오기 점검용으로도 쓴다 | 모델마다 다르다(CC0, CC BY 4.0 등). 폴더의 README에 있다 | 모델마다 | 된다. GitHub | 열어 봄(목록, Car Concept 설명) | https://github.com/KhronosGroup/glTF-Sample-Assets |
| Blender 데모 파일, Blender Studio | Cycles 장면 전체(조명과 재질 공부용), 오픈 무비의 캐릭터와 소품 | 파일마다 CC0, CC BY, CC BY-SA. Studio는 "대체로 CC BY" | CC BY는 필요 | 데모 파일은 된다. Studio 에셋은 유료 구독이 필요한 것이 있다(요약만) | 열어 봄(데모 파일 목록, Studio의 Remixing 안내) | https://www.blender.org/download/demo-files/ , https://studio.blender.org/remixing/ |
| Poly Pizza | 저폴리 모델 10,700여 개 | 모델마다 CC0 또는 CC BY (기존 조사). 라이선스 페이지는 못 엶 | 모델마다 | 연결 도구가 있다 | 첫 화면만 열어 봄 | https://poly.pizza/ |
| Kenney | 저폴리 게임 에셋 | CC0 | 필요 없음. 로고는 쓰지 말 것 | 된다 | 열어 봄 | https://kenney.nl/support |
| Wikimedia Commons 3D (STL) | STL 260개. 색과 재질이 없다. 기계류는 거의 없다 | 파일마다 다르다 | 파일마다 | 된다 | 열어 봄(분류 페이지, 재사용 안내) | https://commons.wikimedia.org/wiki/Category:STL_files |
| Objaverse | Sketchfab 모델 80만여 개를 모은 연구용 묶음 | 객체마다 다르다. CC BY 72만, CC BY-NC 2.5만, CC BY-NC-SA 5.2만, CC BY-SA 1.6만, CC0 3,500 | 객체마다 | 된다(Hugging Face). 하지만 Sketchfab에서 직접 찾는 것과 같은 모델이다 | 열어 봄 | https://huggingface.co/datasets/allenai/objaverse |
| GrabCAD | 공학용 CAD(엔진, 로봇, 기계 부품). 형상은 가장 정확하다 | **쓰지 않는다.** 약관이 "자신의 이익과 비상업적, 내부 사용"으로 한정한다(2016-06-28 개정본) | | 로그인 필요 | 열어 봄 | https://grabcad.com/terms |
| 3D ContentCentral | 제조사 부품 CAD | **쓰지 않는다.** 약관이 콘텐츠의 수정과 "공개적 상업 목적"의 사용을 금지한다 | | 로그인 필요 | 웹 보관소의 2026-09-09 사본으로 읽음 | https://www.3dcontentcentral.com/terms-of-use.aspx |
| TraceParts, 제조사가 직접 주는 CAD | 부품 CAD | 확인 못 함 | | 로그인 필요 | 못 엶 | |
| Thingiverse, Printables | 3D 프린트용 STL. 색과 재질이 없다 | 모델마다 다르다. 비상업 조건이 많다는 글 | 모델마다 | | 요약만(약관은 못 엶) | |

읽는 법 몇 가지.

- **Sketchfab의 Editorial**은 "상업, 홍보, 보증, 광고, 상품화 사용"과 "어떤 사람·브랜드·회사와의 후원·제휴 관계를 암시하는 사용"을 금지한다. NC가 붙은 CC도 게시용 릴스에는 못 쓴다. ND는 수정이 금지라 재질을 바꾸거나 부품을 떼어 낼 수 없다. SA는 고친 결과물에 같은 조건이 따라온다. 그래서 검색은 `CC BY`와 `CC0`로만 건다.
- **Sketchfab의 라이선스 표시는 올린 사람의 주장이다.** 오늘 검색 결과에도 게임에서 뽑아낸 모델(FNAF, Star Wars Galaxies)이 CC BY로 올라와 있었다. 올린 사람이 만든 것인지 설명란을 읽는다. (작업자의 판단)
- **Megascans**는 2024년 말까지 Fab에서 전부 무료였고 그 뒤로는 일부만 무료라는 글이 있다. 지금 어떤 것이 무료인지는 요약만 봤다. 쓸 때 연결 도구로 항목의 가격과 라이선스를 본다.
- **라이선스는 저작권만 다룬다.** NASA 지침과 Wikimedia 안내는 상표, 초상권, 사생활 같은 저작권 밖의 제한이 따로 있다고 적는다. CC BY로 받은 테슬라 모델에 찍힌 로고가 그 예다.

## 2. 받은 모델을 어떻게 판단하나

### 무엇을 보나

| 항목 | 왜 보나 | 근거 |
|---|---|---|
| 실제 크기 | 크기가 틀리면 조명, 피사계 심도, 다른 에셋과의 비례가 다 틀어진다. Poly Haven은 사람 크기의 기준 물체를 옆에 두고 비교하라고 한다 | Poly Haven 모델 기준 |
| 면의 상태 | Poly Haven은 N각형, 떠 있는 점, 넓이가 0인 면을 받지 않는다. 이런 면은 매끈하게 다듬을 때와 모서리를 깎을 때 깨진다 | Poly Haven 모델 기준 |
| 노멀 | 뒤집힌 면은 검게 나오거나 빛이 샌다 | Blender 설명서(노멀) |
| 모서리 | 날이 선 모서리에는 반사광이 맺히지 않는다. "모서리를 살짝 둥글리면 현실에서 보는 반사광이 잡힌다" | Blender 설명서(Bevel 노드) |
| 텍스처 해상도 | Poly Haven은 미터당 2048픽셀 이상, 4K 미만 텍스처는 받지 않는다. 이것은 Poly Haven이 자기 라이브러리에 정한 기준이다. 릴스 화면에 필요한 값은 따로 재지 않았다 | Poly Haven 모델 기준 |
| 재질 맵 구성 | glTF의 기본 재질은 바탕색, 금속성, 거칠기, 구운 차폐, 노멀, 발광이다. 바탕색만 있고 거칠기가 없으면 표면이 고르게 번들거린다 | Blender 설명서(glTF) |
| 구워진 조명 | 스캔과 생성 모델의 바탕색에는 찍을 때의 그림자와 반사광이 들어 있다. 다른 조명 아래 놓으면 어긋난다. "구워진 음영은 찌그러진 곳을 형상처럼 보이게 하고, 바탕색에 구워진 조명은 조명을 바꾼 뒤에 드러난다" | Wavect(생성 서비스 업체의 글), Sketchfab 블로그의 조명 제거 글(요약만) |
| 부품 분리 | 한 덩어리로 붙은 모델은 문, 바퀴, 관절을 움직일 수 없다 | 이 프로젝트의 기록(릴스 07 압축기) |
| 로고와 글자 | 상표는 라이선스에 포함되지 않는다. 이 프로젝트의 화면 기준과도 맞춰야 한다 | NASA 지침, Wikimedia 안내 |
| 실물과의 차이 | 팬이 만든 모델은 실물과 다르다. 실물 사진과 같은 각도로 놓고 본다 | 이 프로젝트의 기록(옵티머스) |
| 메모리 | 그래픽 메모리가 차면 Blender가 시스템 메모리를 쓰고 느려진다 | Blender 설명서(GPU 렌더링) |

### 수치 점검 (돌려 봄)

아래 스크립트는 모델을 빈 장면에 가져와 수치를 찍는다. `blender -b --python audit.py -- <파일>`로 돌린다. Blender 5.2.2 LTS에서 `assets/models/optimus/optimus_mechamaner.glb`에 돌려 확인했다.

```python
import bpy, bmesh, sys
from mathutils import Vector
path = sys.argv[sys.argv.index("--") + 1]
bpy.ops.wm.read_factory_settings(use_empty=True)
ext = path.lower().rsplit(".", 1)[-1]
if ext in ("glb", "gltf"): bpy.ops.import_scene.gltf(filepath=path)
elif ext == "fbx": bpy.ops.wm.fbx_import(filepath=path)
elif ext == "obj": bpy.ops.wm.obj_import(filepath=path)
elif ext in ("usd", "usdz", "usda", "usdc"): bpy.ops.wm.usd_import(filepath=path)
elif ext == "stl": bpy.ops.wm.stl_import(filepath=path)
meshes = [o for o in bpy.context.scene.objects if o.type == "MESH"]
lo = Vector((1e9,) * 3); hi = Vector((-1e9,) * 3)
tot = dict(tris=0, ngons=0, nonmanifold=0, loose=0, zero_area=0, flipped_guess=0)
for o in meshes:
    bm = bmesh.new(); bm.from_mesh(o.data)
    tot["tris"] += sum(len(f.verts) - 2 for f in bm.faces)
    tot["ngons"] += sum(1 for f in bm.faces if len(f.verts) > 4)
    tot["nonmanifold"] += sum(1 for e in bm.edges if not e.is_manifold)
    tot["loose"] += sum(1 for v in bm.verts if not v.link_faces)
    tot["zero_area"] += sum(1 for f in bm.faces if f.calc_area() < 1e-12)
    before = [f.normal.copy() for f in bm.faces]
    bmesh.ops.recalc_face_normals(bm, faces=bm.faces[:])
    tot["flipped_guess"] += sum(1 for f, n in zip(bm.faces, before) if f.normal.dot(n) < 0)
    bm.free()
    for c in o.bound_box:
        w = o.matrix_world @ Vector(c)
        lo = Vector(map(min, lo, w)); hi = Vector(map(max, hi, w))
print("OBJECTS", len(meshes), "unapplied_scale", sum(1 for o in meshes if any(abs(s - 1) > 1e-4 for s in o.scale)))
print("SIZE_m", [round(x, 3) for x in (hi - lo)], "min_z", round(lo.z, 3))
print("MESH", tot)
print("UV_missing", [o.name for o in meshes if not o.data.uv_layers][:10])
for m in bpy.data.materials:
    b = m.node_tree and next((n for n in m.node_tree.nodes if n.type == "BSDF_PRINCIPLED"), None)
    if not b: print("MAT", m.name, "no principled"); continue
    print("MAT", m.name, {i.name: bool(i.is_linked) for i in b.inputs
          if i.name in ("Base Color", "Roughness", "Metallic", "Normal", "Emission Color", "Alpha")})
px = 0
for im in bpy.data.images:
    if im.size[0]:
        px += im.size[0] * im.size[1]
        print("IMG", im.name, tuple(im.size), im.colorspace_settings.name)
print("TEX_MB_uncompressed_8bit_rgba", round(px * 4 / 1024 / 1024, 1))
print("ARMATURES", len([o for o in bpy.context.scene.objects if o.type == "ARMATURE"]), "ACTIONS", len(bpy.data.actions))
```

옵티머스 모델의 결과: 물체 6개, 크기 6.1 × 3.3 × 16.2미터, 삼각형 122,594개, N각형 0, 재질 6개 전부 텍스처 연결 없음(단색), 이미지 0장, 뼈대 0, 동작 0. 사람 키의 로봇이 16미터로 들어온다. 재질은 통째로 새로 입혀야 한다. 걷게 하려면 뼈대부터 넣어야 한다.

읽을 때 주의할 것.

- glTF는 노멀이나 UV가 끊기는 곳마다 점을 따로 저장한다. Blender 설명서에 그렇게 적혀 있고, 가져오기의 Merge Vertices는 "노멀이 다른 점은 합치지 못한다". 그래서 위 결과의 `nonmanifold` 54,382와 `flipped_guess` 63,585는 실제 결함의 수가 아니다. 이 두 값은 거리로 점을 합친 뒤 다시 잰다. 합치기 전에는 뒤집힌 면을 렌더로 본다.
- `TEX_MB`는 압축을 푼 8비트 RGBA로 어림한 값이다. 실제 Cycles 사용량은 렌더 로그의 최대 메모리로 본다.

### 렌더 점검

- **단색 렌더**: 모든 재질을 회색 한 가지로 덮어 형상, 노멀, 모서리만 본다. 재질이 가리던 결함이 보인다.
- **세 거리**: 그 장면의 조명과 구도로 멀리, 중간, 근접을 렌더한다(기존 스킬의 규칙).
- **조명을 돌려 본다**: 환경광을 돌려 두 장을 렌더한다. 그림자가 조명을 따라가지 않고 표면에 붙어 있으면 바탕색에 조명이 구워진 것이다. (작업자의 판단. 근거는 위 표의 구워진 조명 항목)
- **실물 사진과 나란히**: 같은 각도로 놓고 비례와 빠진 부품을 적는다.

## 3. 가져온 모델을 어떻게 고치나

### 형식별로 Blender 5.2에서 달라지는 것 (설명서를 열어 봄, 연산자 이름은 돌려 봄)

| 형식 | 연산자 | 알아 둘 것 |
|---|---|---|
| glTF, GLB | `import_scene.gltf` | 재질을 Principled BSDF 노드로 다시 짠다. 금속성·거칠기 방식과 반사·광택 방식을 다 읽는다. 노멀 맵은 +Y 방식이다. 점이 쪼개져 들어온다(위 참고). 재질이 가장 온전하게 넘어오는 형식이다 |
| FBX | `wm.fbx_import` | 5.x의 기본 가져오기는 새로 만든 것이다. 옛 것은 "FBX (Legacy)"로 남아 있다(`import_scene.fbx`). Scale과 Custom Normals 옵션이 있다. 재질 옵션은 이름 충돌 처리뿐이라 텍스처 연결은 가져온 뒤 확인한다 |
| OBJ | `wm.obj_import` | "기본적인 형상과 재질만 지원한다. 뼈대, 조명, 카메라, 부모 관계, 변환이 없다." 파일마다 크기가 제각각이라 Clamp Bounding Box 옵션이 있다. Forward·Up 축을 고른다. Validate Meshes를 켠다 |
| USD | `wm.usd_import` | 파일의 미터 단위 값과 위쪽 축 정보를 쓴다. 인스턴스를 컬렉션 인스턴스로 가져오는 옵션이 있다. 재질은 Preview Surface 기준이다. 가져오기 쪽 재질 변환의 세부는 읽지 못했다 |
| STL | `wm.stl_import` | 색, 재질, UV가 없다. Facet Normals를 써도 "평평한 음영"이다. Scale과 축, Validate Mesh 옵션이 있다 |
| STEP (CAD) | 확장 "STEP Importer" | Blender 확장 사이트에 무료(GPL-3.0 이상)로 있고 Blender 5.1 이상, 리눅스를 지원한다고 적혀 있다. 곡면을 쪼개는 정밀도를 Draft, Balanced, Fine, Ultra Fine과 직접 입력으로 고른다. 설치해 보지 않았다. 이 컴퓨터에는 FreeCAD, gmsh, CadQuery가 없다(CadQuery 2.8.0은 pip에 있다) |

### 고치는 순서

1. **크기와 원점.** 실물 치수를 찾아 경계 상자에 맞추고, 바닥을 z=0에 놓고, 회전과 크기를 적용한다. Poly Haven은 "원점에 자연스럽게 놓고 회전과 크기를 적용한 상태"를 요구한다.
2. **점 합치기와 노멀.** 거리로 점을 합치고, 노멀을 바깥으로 다시 계산한다. 그다음 Weighted Normal 수정자를 쓴다. 이 수정자는 넓은 면의 노멀에 무게를 더 줘서 "어떤 면들이 아주 평평하게 보이게" 한다. Polycount 위키는 같은 방법을 "모서리를 깎고 넓은 평면의 노멀을 수직으로 맞추면 음영이 작은 깎인 면에서만 섞인다"고 설명한다.
3. **모서리.** 두 가지 길이 있다. Bevel 수정자는 빠르지만 "복잡하거나 지저분한 형상에서는 실패하기도 한다". Bevel 셰이더 노드는 형상을 건드리지 않고 음영만 둥글린다. 대신 Cycles 전용이고 "렌더를 20% 느리게 할 수 있어 굽기나 정지 화면에 권한다". 삼각형으로 쪼개진 모델에는 노드 쪽이 안전하다. (뒤 문장은 작업자의 판단)
4. **재질 바꾸기.** 단색 재질은 Poly Haven이나 ambientCG의 실물 재질로 바꾼다. UV가 없거나 엉망이면 상자 투영으로 입힌다. Poly Haven 소품 작업 글은 "바탕 재질에서 시작해 닳은 자국, 먼지, 녹, 잔 긁힘과 표면 먼지를 층으로 쌓는다"고 적는다.
5. **거칠기에 흠집 층.** ambientCG의 SurfaceImperfections, Fingerprints, 긁힘 맵을 거칠기 값에 섞는다. 바탕색은 건드리지 않는다. 깨끗한 표면은 실제로 없다는 것이 흠집 맵을 파는 쪽과 쓰는 쪽의 공통된 설명이다(요약만).
6. **색과 도장.** 일반 로봇이나 컨테이너를 실제 제품처럼 보이게 하려면 재질 칸별로 색을 바꾸고, 띠와 표지는 데칼로 올린다. 실제 회사의 로고를 넣을지는 이 프로젝트의 화면 기준을 따른다.
7. **데칼.** 경고 표지, 일련번호, 패널 선을 얇은 평면에 알파 텍스처로 올려 표면에 붙인다. Polycount 위키가 Star Citizen의 데칼 방식을 소개한다. ambientCG에 데칼 127개가 있다.
8. **작은 부품.** 볼트, 손잡이, 배선은 한 개를 만들어 컬렉션 인스턴스나 지오메트리 노드로 뿌린다. Poly Haven 기준: "작고 윤곽에 영향이 없는 디테일은 노멀 맵으로 한다. 모서리 깎기는 예외로 대부분 형상에 넣는다."
9. **부품 나누기와 축.** 움직일 부품을 떨어진 조각이나 재질 기준으로 나누고, 원점을 회전축에 놓고, 부모 관계를 건다. 릴스 07의 터빈이 이렇게 했다.
10. **배경용 줄이기.** Decimate 수정자의 Collapse는 형상을 보며 점을 합친다. Planar는 "평평한 면이 대부분인 형상"에 맞고 UV 경계와 재질 경계를 지키는 옵션이 있다. Un-Subdivide는 격자 구조에만 맞는다. Poly Haven의 단계 기준은 LOD1이 원본의 절반 이하, LOD2가 그 절반이다.
11. **8GB에 맞추기.** 렌더 설정의 Simplify에 텍스처 크기 한도(`scene.cycles.texture_limit_render`)와 카메라 밖 물체 제외(`use_camera_cull`), 거리 제외(`use_distance_cull`)가 있다. 속성 이름은 5.2.2에서 확인했다. 원본 텍스처를 줄여 저장하는 것보다 먼저 이 한도를 쓴다. 원본이 남기 때문이다. (뒤 문장은 작업자의 판단)

## 4. 여러 에셋을 붙여 복잡한 물체 만들기

- **실물 참고에서 시작한다.** id Software의 콘셉트 아티스트 Gavin Manners는 Gnomon 강의에서 "실물 참고로 설계 범위를 분명히 정해야 범위가 늘어나거나 어디서 본 듯한 결과가 되는 것을 피한다"고 한다. 공장 라인이면 그 공장의 사진에서 반복되는 단위(기둥 간격, 컨베이어 높이, 로봇 간격)를 먼저 적는다.
- **크기와 겉모습의 일관성이 먼저다.** 같은 강의: "처음 구상을 지키는 것보다 크기의 일관성과 시각적 통일이 더 중요하다." 가져온 부품을 전부 미터 단위 실제 크기로 맞춘 뒤 붙인다.
- **재질을 통일한다.** 출처가 다른 부품은 재질의 결이 다르다. 붙인 뒤 같은 재질 묶음(같은 도장 금속, 같은 고무, 같은 흠집 층)으로 덮어 한 공장에서 나온 것처럼 만든다. (작업자의 판단. 근거는 위의 통일 원칙)
- **마감은 데칼과 닳은 자국으로.** 같은 강의: "기술적 완벽함보다 읽히는 설계와 만들어진 물건다움을 앞에 두고, 대기 효과, 데칼, 풍화로 깊이를 만든다."
- **반복은 인스턴스로.** 같은 로봇 셀을 열 번 놓을 때 컬렉션 인스턴스를 쓴다(기존 스킬).
- **라이선스가 쌓인다.** 한 물체에 CC BY 모델 셋을 쓰면 셋 다 표시한다. SA가 하나라도 섞이면 그 조건이 결과물에 따라온다. `assets/CREDITS.md`에 조립한 물체 한 줄을 만들고 그 아래에 부품별 출처, 라이선스, 고친 내용을 적는다. 릴스 07의 압축기 줄이 본이다.
- **무료 조립 부품 묶음.** CC0나 CC BY가 확인된 것을 찾지 못했다. 검색에 나온 무료 묶음은 라이선스가 적혀 있지 않았다. 대신 Poly Haven의 산업 소품 97개와 BlenderKit의 무료 모델을 부품으로 쓴다.

## 5. 스캔과 AI 생성 모델은 어디까지 쓸 수 있나

- **스캔**: 형상과 표면의 결은 진짜다. 문제는 바탕색에 찍을 때의 조명이 남는 것이다. 조명을 지운 스캔(Poly Haven, Megascans)은 주인공으로도 쓴다. 조명을 지우지 않은 박물관 스캔과 개인 스캔은 찍은 조명과 비슷한 조명에서, 중간 거리나 배경으로 쓴다. 스캔은 삼각형이 많고 부품이 나뉘어 있지 않아 움직이는 물체로는 쓰지 못한다. (조명 제거가 필요하다는 것은 Sketchfab 블로그의 글을 요약만 봤다. 거리 구분은 작업자의 판단)
- **AI 생성 모델**: 생성 서비스 업체인 Wavect의 글(2026-08-13)이 스스로 적은 구분은 이렇다. 잘 맞는 것은 "정지한 소품, 콘셉트, 임시 모형"이고, 가장 약한 것은 "변형되는 주인공 캐릭터, 치수가 정확해야 하는 부품, 돌려쓰는 조립 부품 묶음"이다. 이유로 "참고 이미지는 뒷면, 아랫면, 숨은 관절을 보여 주지 않는다. 그럴듯한 앞모습이 지어낸 형상을 가린다"를 든다. 다른 업체 3D AI Studio도 "정확한 치수나 특정한 형상이 필요하면 출발점일 뿐"이라고 적는다. 둘 다 파는 쪽의 글이다. 이 프로젝트의 직접 검증(TripoSG: 소품 통과, 주인공 차량 탈락)과 방향이 같다.
- 그래서 기계가 주인공인 이 프로젝트에서 생성 모델은 배경 소품과 중간 거리까지다. 가까이 비추는 기계는 사람이 만든 모델이나 코드로 만든다.

## 6. 정하는 순서

아래는 출처의 사실과 이 프로젝트의 조건(작업자가 혼자 받고 고친다, 8GB, 게시용)을 묶은 **작업자의 판단**이다.

1. 물건의 역할을 먼저 정한다: 주인공(가까이, 오래), 중간, 배경, 수량.
2. `assets/README.md`와 지난 영상의 `assets/`에 있는지 본다.
3. 실제 제품이면 그 제품의 공개 모델을 본다: MuJoCo Menagerie(로봇), NASA(우주), 제조사 저장소. 형상이 정확하고 관절이 나뉘어 있다.
4. Sketchfab을 `CC BY`, `CC0`로 검색한다. 이름을 바꿔 가며 찾는다(영어 일반명, 제품명, 상위 분류). 결과에서 삼각형 수, 동작 유무, 설명란을 본다.
5. BlenderKit 무료, Fab 무료와 보유 목록, Poly Haven, ambientCG 모델을 본다.
6. 후보가 나오면 2절의 수치 점검과 렌더 점검을 한다. 떨어뜨릴 때는 이유를 적는다.
7. **가져와서 고친다**를 고르는 때: 윤곽과 큰 부품이 실물과 맞고, 틀린 것이 크기·재질·모서리·로고·빠진 작은 부품일 때. 이것들은 3절로 고쳐진다.
8. **코드로 만든다**를 고르는 때: 물건이 상자·원통·판의 조합일 때(컨테이너, 서버 랙, 금괴, 웨이퍼, 배터리 팩), 치수와 발광을 제어해야 할 때, 부품이 따로 움직여야 하는데 후보가 한 덩어리일 때. 이때도 Poly Haven·ambientCG 재질, 흠집 층, 모서리, 데칼을 입힌다.
9. **섞는다**를 고르는 때: 어려운 부품(날개 줄, 로봇 손목, 차체 곡면)만 가져오고 나머지를 코드로 붙인다. 릴스 07의 터빈이 이 방식이다.
10. 찾기를 멈추는 때: 3~5번의 곳을 이름을 바꿔 가며 다 찾았고, 남은 후보가 6번에서 떨어졌을 때. 시간으로 정한 한도는 근거를 찾지 못해 정하지 않았다. 찾아본 곳과 결과는 `storyboard.md`의 에셋 표에 "없음"까지 적는다(기존 스킬).
11. AI 생성은 배경 소품과 중간 거리의 복잡한 소품에 쓴다(5절).

## 7. 자주 나오는 물건의 후보

Sketchfab 공개 검색 API(`downloadable=true`, `license=by`와 `cc0`, 좋아요 순)와 BlenderKit 검색 API(`is_free:true`), MuJoCo Menagerie 목록을 2026-10-08에 직접 조회했다. 라이선스는 그 응답에 적힌 값이다. **모델을 내려받거나 렌더하지 않았다.** 삼각형 수와 좋아요 수는 품질이 아니다. Fab은 로그인이 필요해 찾지 못했다. 쓰기 전에 모델 페이지에서 라이선스와 설명을 다시 본다.

| 물건 | 후보 (제작자, 면 수) | 라이선스 | 메모 |
|---|---|---|---|
| 인간형 로봇 (아틀라스 같은) | Unitree G1·H1, Booster T1, Fourier N1, Apptronik Apollo — https://github.com/google-deepmind/mujoco_menagerie | G1·H1 BSD-3-Clause, T1·N1 Apache-2.0, Apollo는 폴더의 LICENSE | 실제 제품의 형상과 관절. 시뮬레이션용이라 겉면 디테일은 열어 봐야 안다. 아틀라스는 없다 |
| | "Unitree G1 humanoid (Yes Rigged bone)" KenzoDkohno22T, 629,314면 — https://sketchfab.com/3d-models/a993950a01714f0f801a685449cee1fb | CC BY | 뼈대가 있다고 적혀 있다 |
| | "Atlas robot" bruhepic925, 38,805면 — https://sketchfab.com/3d-models/1b582669d125496882d96a8ac3e373ea | CC BY | 좋아요 6. 어느 세대의 아틀라스인지 확인 못 함 |
| | "Sci-Fi Humanoid Robot" yur1_val, 435,616면 — https://sketchfab.com/3d-models/12ad786ecde246e5854a61fd4f67ed49 | CC BY | 실제 제품이 아닌 일반 로봇 |
| | "Animated humanoid robot" pinguinoconpulgares, 10,794면, 동작 4개 — https://sketchfab.com/3d-models/8993602ca91f4c499e690e5dae19f978 | CC BY | 면이 적다. 배경용 |
| 전력망 배터리 컨테이너 (메가팩 같은) | "集成箱式储能系统 - Integrated Box Energy Storage System" mrdt.club, 317,755면 — https://sketchfab.com/3d-models/4b2d126ea84f4634899d885befe96394 | CC BY | |
| | "battery energy storage system (BESS),container" rexnewgeek4, 387,951면 — https://sketchfab.com/3d-models/03b728aca41648a09f850d2fc84396b5 | CC BY | |
| | "Tesla Powerwall 2" spsvision, 25,070면 — https://sketchfab.com/3d-models/685ca14d035347dd91c79b19c34a1a8e | CC BY | 가정용. 메가팩이 아니다 |
| | **메가팩 자체는 찾지 못했다.** 상자 모양이라 코드로 만들고 위 모델에서 문, 환기구, 배선함을 참고한다 | | |
| 가스터빈, 제트 엔진 | "Turbine \| Turbofan Engine \| Jet Engine" blenderbirb, 235,986면 — https://sketchfab.com/3d-models/74c6aceed86b4a41aaad3b93afc3e262 | CC BY | 좋아요 674. 같은 제작자의 다른 판(315,186면): https://sketchfab.com/3d-models/349790f8fdbe4d82bbd04240d8c9a5fb |
| | "GAS TURBINE AND TRANSFORMER" arnaudbanner, 331,018면 — https://sketchfab.com/3d-models/600ec765b34c49ccb91dcf0c5c7b6592 | CC BY | 발전용 가스터빈과 변압기 |
| | "QE2 Starboard High Pressure Turbine Pattern" ScottishMaritimeMuseum, 42,603면 — https://sketchfab.com/3d-models/8e135c1a917c476a98f011a48c4192c7 | CC0 | 박물관 스캔. 증기 터빈의 목형이다 |
| | "Jet Engine" (BlenderKit 무료, 25c26b39-f3ac-4242-85a1-c31159c5a2c2) | Royalty Free | |
| | 이미 있는 것: 릴스 07의 축류 압축기(ygorprangel, CC BY 4.0) | | |
| 산업용 로봇 팔 | "Black Honey - Robotic Arm" re1monsen, 73,213면, 동작 1 — https://sketchfab.com/3d-models/c50671f2a8e74de2a2e687103fdc93ab | CC BY | 좋아요 1,174 |
| | "Industrial robot arm" olofunot, 85,156면, 동작 1 — https://sketchfab.com/3d-models/b4b5931851754747a734f72234c87e38 | CC BY | |
| | "Robotic Manipulator" makke3d, 37,900면 — https://sketchfab.com/3d-models/0fd88ae6662745c9a73e28afc9991be4 | CC BY | |
| | "Industrial robots from KUKA (manipulator)" hrofti, 18,940면, 동작 1 — https://sketchfab.com/3d-models/312c66b067084dedb2d6542021156466 | CC BY | 상표가 있다 |
| | UR5e, UR10e, KUKA LBR iiwa 14, Franka — MuJoCo Menagerie | iiwa BSD-3-Clause, Franka Apache-2.0, UR은 폴더의 LICENSE를 읽을 것(이번에 읽지 못함) | 협동 로봇. 자동차 공장의 대형 로봇은 아니다 |
| | "Robotic Arm" ReWork3D, "Robot KUKA Iiwa 14 on KMP1500" (BlenderKit 무료) | Royalty Free | 무료 로봇 팔 검색 결과 18개 |
| | "Robot UR10 Robotiq Palletizing Solution" (BlenderKit 무료, 8ae5cb54-43a4-40ab-bd17-a743b6398515) | CC0 | 컨베이어가 딸려 있다 |
| 반도체 웨이퍼, 칩 | "Simplified Silicon Wafer" the_boat17, 312,500면 — https://sketchfab.com/3d-models/788ebb01cd01484f9d18da16918588aa | CC BY | 좋아요 3 |
| | "Processor Intel Core i5-12400 (CPU)" Medvedev_MArS, 1,044,909면 — https://sketchfab.com/3d-models/cea1626ddf284761b0d6d045d4c4e67a | CC BY | 면이 많다. 상표가 있다 |
| | "CMOS (Twin Well) Cross Section" edry_hu, 10,428면 — https://sketchfab.com/3d-models/b5149c0b090d4a10b105466cec3c30ad | CC BY | 단면 설명용 |
| | Poly Haven `circuit_board` | CC0 | 기판 |
| | **마땅한 것이 없다.** 웨이퍼는 원판과 칩 격자라 코드로 만든다 | | |
| 컨테이너선 | "Container Ship" RM02, 188,711면 — https://sketchfab.com/3d-models/aaa41cca946b4a08bc08cf692b7757be | CC BY | 좋아요 411 |
| | "Cargo ship" hungry_drifter, 73,448면 — https://sketchfab.com/3d-models/b7c97df584824ca682d26daabf401f87 | CC BY | 좋아요 469 |
| | "Container scan No. 8" Dystopia, 109,115면 — https://sketchfab.com/3d-models/f237d79d2a934a7589b9d9f1bdc42638 | CC BY | 컨테이너 한 개의 스캔 |
| | "Shipping container", "Shipping crane" (BlenderKit 무료) | Royalty Free | |
| 공장 컨베이어, 조립 라인 | "Small conveyor belt scene" brendanwood872, 12,704면, 동작 6 — https://sketchfab.com/3d-models/8758fecf3bd346d189957a6ed00469f4 | CC BY | |
| | "Conveyer Belts" Adsuitte, 22,134면 — https://sketchfab.com/3d-models/7dba44c77c774e239d42f1a082b28140 | CC BY | |
| | "Industrial Conveyer Roller (modular)" parabatharva4, 2,434면 — https://sketchfab.com/3d-models/4736d0c18e7047969639988883f0ad56 | CC BY | 조립식 |
| | "Low Poly Factory Assets" paolo.mercoglia, 18,238면 — https://sketchfab.com/3d-models/981b9b8fbdf14bb4a846dda0a2176ed9 | CC BY | 저폴리. 이 프로젝트의 화면과 결이 다를 수 있다 |
| | **조립 라인 전체는 찾지 못했다.** 컨베이어와 로봇 팔을 붙여 만든다(4절) | | |
| 도시 건물, 고층 건물 | "[FREE] Atlanta, Corperate Office Building" 99.Miles, 37,290면 — https://sketchfab.com/3d-models/d96380fb001345cca9a9be121f3e43d5 | CC BY | 좋아요 3,403 |
| | "Realistic chicago buildings" 99.Miles, 11,643면 — https://sketchfab.com/3d-models/c4a3993ef1e84e6d9d5a15c78da88aae | CC BY | |
| | "Procedural Hong Kong building" udayjeet, 197,097면 — https://sketchfab.com/3d-models/528a732e84c44fd49c4726f341014a23 | CC BY | |
| | "CCity Building Set 1" neberkenezer, 18,372면 — https://sketchfab.com/3d-models/a2d5c7bfcc2148fb8994864c43dfcc97 | CC BY | 좋아요 4,340 |
| | "City" jeandiz, 80,408면 — https://sketchfab.com/3d-models/1f50f0d6ec5a493d8e91d7db1106b324 | CC BY | |
| | "Skyline Vista Tower" 등 (BlenderKit 무료 7개) | Royalty Free | |
| 동전, 금괴 | "Fine Gold Bar" incg5764, 684면 — https://sketchfab.com/3d-models/0d1ff6b3e6d045cba78889caf7f5bc6e | CC BY | 좋아요 626 |
| | "Gold Coins Material" chrisg4919, 261,120면 — https://sketchfab.com/3d-models/a334ce7cfb8e449391a181c2738ecd00 | CC BY | 좋아요 929 |
| | "Pile of Coins (4)" SebastianSosnowski, 86,360면 — https://sketchfab.com/3d-models/d7036943cf8047519481e985fc999418 | CC BY | |
| | "Gold Ingot - Pristine Bar" (BlenderKit 무료, fd1fffbc-c5b4-426d-99c9-67933ffa6580) | Royalty Free | |
| 서버 랙, 데이터 센터 | "Server Racking System" mcpanayides, 299,604면 — https://sketchfab.com/3d-models/6fe2cacf836b4aed96c650b286db5486 | CC BY | 좋아요 396 |
| | "Server rack" Crysis007-94, 29,711면 — https://sketchfab.com/3d-models/5320622f6c0741b7aed399bfa2965dc4 | CC BY | |
| | "Server Rack" nashalanandas, 74,823면 — https://sketchfab.com/3d-models/c144d837358d446998c7b63cd1bdf825 | CC BY | |
| | BlenderKit 무료에는 없다(0개). 데이터 센터 방 전체도 찾지 못했다. 랙을 인스턴스로 줄 세운다 | | |
| 전기차 차대, 배터리 팩 | "Tesla ModelX chassis" beyond.zht, 46,151면 — https://sketchfab.com/3d-models/c33162ad8de946f98ff604017f71b2da | CC BY | 좋아요 124. 다른 계정(davidmarton1987)에 면 수가 같은 모델이 있다. 누가 원작자인지 본다 |
| | "Car Inner Frame with Differential Gear" Aakash.jsx, 284,810면 — https://sketchfab.com/3d-models/e0c8be463be546ab93c107fab5b4a7b3 | CC BY | 전기차 차대인지 확인 못 함 |
| | **배터리 팩은 찾지 못했다.** 판, 셀 줄, 냉각 판의 조합이라 코드로 만든다 | | |

## 규칙 후보

각 줄은 (가) 할 일, (나) 확인하는 법, (다) 근거다.

1. **검색은 CC BY와 CC0로만 건다.** (가) Sketchfab에서 NC, ND, Editorial을 빼고 찾는다. SA는 결과물에 조건이 따라오므로 피한다. (나) 받기 직전에 모델 페이지의 라이선스를 읽고 날짜와 함께 CREDITS에 적는다. (다) Sketchfab 라이선스 도움말, Editorial 문구.
2. **GrabCAD와 3D ContentCentral의 모델은 쓰지 않는다.** (가) 형상 참고로만 본다. (나) 에셋 표에 이 두 곳에서 온 파일이 없는지 본다. (다) GrabCAD 약관 "non-commercial, internal use", 3D ContentCentral 약관 "any public commercial purpose" 금지.
3. **올린 사람이 만든 것인지 본다.** (가) 설명란과 제작자의 다른 모델을 보고, 게임이나 다른 곳에서 가져온 것이면 쓰지 않는다. (나) CREDITS에 "제작자가 직접 만들었다고 적음" 또는 "미확인"을 적는다. (다) 작업자의 판단. 오늘 검색에 게임 추출 모델이 CC BY로 나왔다.
4. **실제 로봇은 회사가 공개한 모델을 먼저 본다.** (가) MuJoCo Menagerie에서 그 제품을 찾는다. (나) 모델 폴더의 LICENSE를 읽고 고지문을 함께 보관한다. (다) Menagerie 저장소 목록.
5. **받은 모델은 쓰기 전에 수치 점검을 돌린다.** (가) 2절의 스크립트를 돌린다. (나) 크기, 삼각형 수, 재질별 맵 연결, 이미지 크기, 뼈대 수를 에셋 표에 적는다. (다) 옵티머스 모델에서 16미터, 텍스처 0장이 나왔다(돌려 봄).
6. **크기를 실물 치수에 맞춘다.** (가) 실물의 길이를 찾아 경계 상자를 맞추고 바닥을 z=0에 놓고 변환을 적용한다. (나) 점검 스크립트의 `SIZE_m`이 실물과 맞고 `unapplied_scale`이 0이다. (다) Poly Haven 모델 기준.
7. **단색 렌더를 먼저 본다.** (가) 재질을 회색으로 덮어 한 장 렌더한다. (나) 검은 면, 각진 곡면, 반사광이 없는 모서리가 있는지 본다. (다) Blender 설명서(노멀, Bevel 노드).
8. **조명을 돌려 구워진 그림자를 찾는다.** (가) 환경광을 돌려 두 장 렌더한다. (나) 그림자가 조명을 따라 움직이지 않으면 그 텍스처의 바탕색을 쓰지 않는다. (다) Wavect의 글. 방법 자체는 작업자의 판단.
9. **모서리에 반사광이 맺히게 한다.** (가) Bevel 수정자를 걸고, 형상이 깨지면 Bevel 셰이더 노드를 쓴다. (나) 근접 렌더에서 모서리에 밝은 선이 보인다. 노드를 쓰면 렌더 시간을 전후로 잰다. (다) Blender 설명서(Bevel 노드: 20% 느려질 수 있음, 수정자는 지저분한 형상에서 실패).
10. **평면이 울어 보이면 Weighted Normal을 건다.** (가) 점을 합친 뒤 수정자를 추가한다. (나) 단색 렌더에서 넓은 면의 얼룩이 사라진다. (다) Blender 설명서, Polycount 위키.
11. **단색 재질은 실물 재질로 바꾼다.** (가) 점검에서 맵 연결이 없는 재질을 Poly Haven·ambientCG 재질로 바꾼다. (나) 점검을 다시 돌려 주요 재질의 Roughness와 Normal이 연결돼 있다. (다) glTF 재질 구성(Blender 설명서), 기존 스킬.
12. **거칠기에 흠집 층을 섞는다.** (가) ambientCG의 SurfaceImperfections나 Fingerprints를 거칠기에만 섞는다. (나) 근접 렌더에서 반사가 고르지 않다. 바탕색은 그대로다. (다) Poly Haven 소품 작업 글, ambientCG 목록.
13. **작은 디테일은 인스턴스와 데칼로 더한다.** (가) 볼트와 손잡이는 인스턴스로, 표지와 패널 선은 데칼로 올린다. (나) 근접 화면을 실물 사진과 나란히 놓고 빠진 것을 센다. (다) Poly Haven 기준(윤곽에 영향 없는 디테일), Gnomon 강의.
14. **조립한 물체는 부품을 실제 크기로 맞추고 재질을 통일한다.** (가) 붙이기 전에 부품마다 6번을 하고, 붙인 뒤 같은 재질 묶음으로 덮는다. (나) 조립한 물체의 중간 렌더에서 부품의 출처가 구별되지 않는다. (다) Gnomon 강의("크기의 일관성과 시각적 통일").
15. **부품별 출처를 한 줄씩 남긴다.** (가) CREDITS에 조립한 물체와 그 아래 부품별 출처, 라이선스, 고친 내용을 적는다. CC BY는 "고쳤음"을 밝힌다. (나) 영상의 출처 장면에 있는 이름 수와 CREDITS의 CC BY 부품 수가 같다. (다) Sketchfab 표기 도움말, 이 프로젝트의 릴스 07 기록.
16. **로고와 상표는 따로 판단한다.** (가) 받은 모델의 로고를 찾아 남길지 지울지 정한다. (나) 근접 렌더에서 글자와 로고를 읽어 본다. (다) NASA 지침, Wikimedia 안내.
17. **배경 인스턴스는 줄인 판을 쓴다.** (가) Decimate로 절반씩 줄인 판을 만들어 먼 줄에 쓴다. (나) 먼 거리 렌더에서 원본과 구별되지 않는다. 삼각형 수를 적는다. (다) Blender 설명서(Decimate), Poly Haven의 LOD 기준.
18. **메모리가 차면 텍스처 한도부터 건다.** (가) Simplify의 텍스처 크기 한도와 카메라 밖 제외를 켠다. (나) 렌더 로그의 최대 메모리를 전후로 적는다. (다) Blender 설명서(Simplify, GPU 렌더링).
19. **스캔과 생성 모델은 중간 거리까지만 쓴다.** (가) 가까이 비추는 기계에는 쓰지 않는다. (나) 스토리보드에서 그 물체가 나오는 컷의 거리를 본다. (다) Wavect의 글, 이 프로젝트의 TripoSG 검증.
20. **상자·원통·판으로 된 물건은 찾기보다 만든다.** (가) 컨테이너, 랙, 금괴, 웨이퍼, 배터리 팩은 코드로 만들고 11~13번을 적용한다. (나) 근접 렌더가 실물 사진과 나란히 놓였을 때 모형처럼 보이지 않는다. (다) 작업자의 판단. 7절에서 이 물건들의 후보가 약했다.

## 확인하지 못한 것

- **후보 모델의 품질.** 7절의 모델은 하나도 내려받지 않았고 렌더하지 않았다. 재질 맵이 있는지, 부품이 나뉘어 있는지 모른다.
- **Fab의 EULA 전문과 Megascans의 현재 무료 범위.** fab.com이 자동 요청을 막았다(403). 라이선스 요약은 웹 보관소의 2026-09-10 사본으로 읽었다. Megascans가 지금 얼마나 무료인지는 검색 요약뿐이다. Fab에서 7절의 물건을 찾아보지도 못했다.
- **Smithsonian의 약관.** si.edu와 3d.si.edu가 403이었다. CC0라는 것은 검색 요약과 기존 조사다.
- **Sketchfab 내려받기 API의 인증 조건.** 문서 페이지가 열리지 않았다.
- **BlenderKit을 스크립트로 내려받아도 되는지.** 무료 모델 하나의 주소가 로그인 없이 나왔지만 약관 페이지를 열지 못했다. 파일도 받지 않았다. 라이선스 문서의 주소가 blendkit.com으로 넘어가는 까닭도 확인하지 못했다.
- **CC BY 4.0의 원문.** creativecommons.org에 연결되지 않았다. "고쳤음을 밝힌다"는 이 프로젝트의 기존 기록을 따랐다.
- **TraceParts, 제조사 CAD, Printables, Thingiverse의 약관.** 열지 못했다.
- **Poly Pizza의 라이선스 페이지.** 404였다.
- **STEP 가져오기.** 확장을 설치하지 않았고 STEP 파일을 변환해 보지 않았다. FreeCAD 위키는 자동 요청을 막았다. 정밀도 값에 따른 곡면 품질은 모른다.
- **Blender Studio 에셋의 구독 조건.** 요약만 봤다.
- **USD 가져오기의 재질 변환.** 설명서의 내보내기 쪽만 읽혔다.
- **Sketchfab 블로그의 스캔 조명 제거 글.** 본문이 열리지 않아 요약만 봤다.
- **CC0나 CC BY가 확인된 무료 조립 부품 묶음.** 찾지 못했다.
- **릴스 화면에 필요한 텍스처 해상도와 삼각형 수.** Poly Haven의 기준(미터당 2048픽셀, 소품 크기별 삼각형 수)은 그 라이브러리의 기준이다. 1080×1920 화면과 8GB에서의 값은 재지 않았다.
- **찾기에 쓸 시간 한도.** 근거가 되는 출처를 찾지 못했다.

## 출처

열어 본 것(2026-10-08).

- Poly Haven: [라이선스](https://polyhaven.com/license), [API 약관](https://github.com/Poly-Haven/Public-API/blob/master/ToS.md), [모델 기준](https://docs.polyhaven.com/en/technical-standards/models), [소품 작업 글](https://blog.polyhaven.com/simple-prop-workflow/)
- ambientCG: [라이선스](https://docs.ambientcg.com/license/), [API 안내](https://docs.ambientcg.com/api/)
- Sketchfab: [내려받기 라이선스 도움말](https://help.sketchfab.com/en/articles/16152217), [표기 도움말](https://help.sketchfab.com/en/articles/16152215-crediting-users-for-3d-model-downloads), [Standard·Editorial](https://sketchfab.com/licenses), 검색 API `https://api.sketchfab.com/v3/search`
- Fab: [EULA 요약](https://www.fab.com/eula)(웹 보관소 2026-09-10 사본), [기간 한정 무료 공지](https://forums.unrealengine.com/t/fab-limited-time-free-content/2738884)
- BlenderKit: [라이선스](https://www.blenderkit.com/docs/licenses/), 검색 API `https://www.blenderkit.com/api/v1/search/`
- NASA: [3D Resources 저장소](https://github.com/nasa/NASA-3D-Resources), [사용 지침](https://www.nasa.gov/nasa-brand-center/images-and-media/)
- [MuJoCo Menagerie](https://github.com/google-deepmind/mujoco_menagerie), [Khronos glTF Sample Assets](https://github.com/KhronosGroup/glTF-Sample-Assets), [Objaverse](https://huggingface.co/datasets/allenai/objaverse)
- [Blender 데모 파일](https://www.blender.org/download/demo-files/), [Blender Studio Remixing](https://studio.blender.org/remixing/), [Kenney](https://kenney.nl/support), [Wikimedia 재사용 안내](https://commons.wikimedia.org/wiki/Commons:Reusing_content_outside_Wikimedia), [STL 분류](https://commons.wikimedia.org/wiki/Category:STL_files)
- [GrabCAD 약관](https://grabcad.com/terms), [3D ContentCentral 약관](https://www.3dcontentcentral.com/terms-of-use.aspx)(웹 보관소 2026-09-09 사본)
- Blender 5.2 LTS 설명서: [glTF](https://docs.blender.org/manual/en/5.2/addons/scene_gltf2.html), [FBX](https://docs.blender.org/manual/en/latest/files/import_export/fbx.html), [OBJ](https://docs.blender.org/manual/en/latest/files/import_export/obj.html), [USD](https://docs.blender.org/manual/en/latest/files/import_export/usd.html), [STL](https://docs.blender.org/manual/en/latest/files/import_export/stl.html), [Bevel 노드](https://docs.blender.org/manual/en/latest/render/shader_nodes/input/bevel.html), [Weighted Normal](https://docs.blender.org/manual/en/latest/modeling/modifiers/normals/weighted_normal.html), [Decimate](https://docs.blender.org/manual/en/latest/modeling/modifiers/generate/decimate.html), [Simplify](https://docs.blender.org/manual/en/latest/render/cycles/render_settings/simplify.html), [GPU 렌더링](https://docs.blender.org/manual/en/latest/render/cycles/gpu_rendering.html)
- [Polycount 위키: Face weighted normals](http://wiki.polycount.com/wiki/Face_weighted_normals)
- [Gnomon Workshop: Designing a Custom Kitbash Library (Gavin Manners)](https://www.thegnomonworkshop.com/workshops/designing-a-custom-kitbash-library) — 강의 소개 글만 읽었다
- [Wavect: AI 3D model generators for game development 2026](https://wavect.io/blog/ai-3d-model-generators-game-development-2026/), [3D AI Studio: Can AI Generate Game-Ready 3D Models?](https://3daistudio.com/3d-generator-ai-comparison-alternatives-guide/can-ai-generate-game-ready-3d-models) — 둘 다 생성 서비스 업체의 글
- [STEP Importer 확장](https://extensions.blender.org/add-ons/step-importer/)

요약만 본 것.

- [Sketchfab 블로그: De-Lighting 3D Scans in Unity (Pete McNally)](https://sketchfab.com/blogs/community/de-lighting-3d-scans-in-unity-by-pete-mcnally)
- [80.lv: Megascans no longer free after 2024](https://80.lv/articles/megascans-no-longer-free-after-2024/), [Unreal Engine: Free content for creators](https://www.unrealengine.com/fabfreecontent)
- [CG Channel: Get 2,000 free 3D models from the Smithsonian collection](https://www.cgchannel.com/2020/03/get-2000-free-3d-models-from-the-smithsonian-collection/)
- [All3DP: Selling 3D printed items, a legal guide](https://all3dp.com/1/things-to-3d-print-and-sell-a-legal-guide/)
- [BlenderNation: Realistic Touch – Surface Imperfection](https://www.blendernation.com/2023/11/24/realistic-touch-surface-imperfection-a-revolution-for-3d-renders-promoted/)
