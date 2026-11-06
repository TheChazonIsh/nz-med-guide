# 🇳🇿 NZ Pharmacy MedGuide (뉴질랜드 일반의약품 성분·증상·병용 가이드)

뉴질랜드 일반 약국(**Chemist Warehouse NZ**, **Unichem Pharmacy**, **Life Pharmacy**)에서 처방전 없이 구할 수 있는 일반의약품(OTC)을 **핵심 성분(Active Ingredient)** 기준으로 정리한 반응형 웹 애플리케이션(PWA 지원)입니다.

## ✨ 주요 기능

1. **🩺 증상별 맞춤 검색 (Symptom Checker)**
   - 발열, 두통, 인후통, 코막힘, 가래, 꽃가루 알레르기(Hayfever), 속쓰림/역류, 위경련, 급성 설사, 변비, 방광염, 멀미 등 증상을 다중 선택하거나 검색하면 최적의 1차 성분과 시너지 병용 조합을 추천합니다.
   - 뉴질랜드 실제 판매 제품 사진, 예상 가격대, 구매 등급(`General Sale`, `Pharmacy Only`, `Pharmacist Only`), 공식 온라인몰 링크를 제공합니다.

2. **🧬 성분 백과 & 작용 기전 (Active Ingredients Encyclopedia)**
   - 18대 핵심 성분군의 약리 기전(왜 효과가 나는지), 발현 및 지속 시간, 표준 복용 간격, 같이 쓰면 좋은 성분(다른 기전 시너지)과 같이 쓰면 안 되는 성분(중복·충돌 금기)을 한눈에 비교합니다.

3. **⚖️ 병용 시너지/금기 자동 판별기 (Combination & Interaction Checker)**
   - 복용하려는 약이나 성분을 2개 이상 선택하면 약리 기전이 달라 시너지가 나는지(`Panadol + Nurofen`, `Zyrtec + Flixonase`, `Losec + Gaviscon`), 혹은 성분 중복(`Panadol + Lemsip/Codral`)이나 동일 계열 충돌(`Nurofen + Voltaren`)로 위험한지 즉시 분석합니다.

4. **💊 NZ 약국 제품 카탈로그 & 나만의 상비약장 (My Med Cabinet)**
   - 집에 보유한 상비약을 체크해 두거나 새로 구매한 약을 직접 추가(`localStorage` 자동 저장)하여 관리할 수 있습니다.
   - 스마트폰 브라우저에서 **'홈 화면에 추가'**를 누르면 네이티브 앱처럼 전체 화면으로 실행됩니다.

---

## 🚀 GitHub Pages로 1분 만에 무료 웹앱 배포하기

### 방법 A: 웹 브라우저에서 파일 업로드로 바로 배포 (가장 쉬운 방법)

1. [GitHub](https://github.com/new)에서 새 저장소(Repository)를 생성합니다.
   - **Repository name**: 예) `nz-med-guide`
   - **Public** 선택 후 **Create repository** 클릭
2. 생성된 저장소 화면에서 **`uploading an existing file`** 링크를 클릭합니다.
3. 압축 해제한 폴더 안의 모든 파일(`index.html`, `manifest.json`, `sw.js`, `icon.svg`, `README.md`, `.nojekyll`, `.github` 폴더)을 드래그 앤 드롭으로 올리고 **`Commit changes`**를 클릭합니다.
4. 저장소 상단 탭에서 **`Settings`** → 왼쪽 메뉴 **`Pages`**로 이동합니다.
5. **Build and deployment** 아래의 **Source**를:
   - `Deploy from a branch` 선택 → Branch를 **`main`** / **`/(root)`**로 설정 후 **Save** 클릭 (또는 `GitHub Actions` 선택)
6. 약 30~60초 후 `https://<내-깃허브-아이디>.github.io/nz-med-guide/` 주소로 언제 어디서나 접속 가능한 웹앱이 열립니다!

### 방법 B: 터미널(Git CLI)로 푸시하여 배포

```bash
unzip nz-otc-med-guide-github-pages.zip -d nz-med-guide
cd nz-med-guide
git init
git branch -M main
git add .
git commit -m "Initial commit: NZ Pharmacy MedGuide PWA"
git remote add origin https://github.com/<내-깃허브-아이디>/<저장소-이름>.git
git push -u origin main
```

---

## 📱 스마트폰에서 앱처럼 설치해서 쓰는 법 (PWA)

배포된 GitHub Pages 주소를 스마트폰으로 접속한 뒤:
- **아이폰 (Safari)**: 하단 **공유 버튼(⬆️)** 탭 → **'홈 화면에 추가(Add to Home Screen)'** 선택
- **안드로이드 (Chrome)**: 우측 상단 **메뉴(⋮)** 탭 → **'앱 설치(Install app)'** 또는 **'홈 화면에 추가'** 선택
