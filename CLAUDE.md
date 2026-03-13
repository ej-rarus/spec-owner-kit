# CLAUDE.md - 치후 테라리움

## 프로젝트 정보

- **사업명**: 치후 테라리움 (ChiHoo Terrarium)
- **주소**: 서울특별시 성북구 삼양로 38 101호
- **운영**: 화-일 10:00-20:00 (월요일 휴무)
- **브랜드 컨셉**: "작은 숲을 품다" — 빈티지 보타니컬 감성

## 폴더 구조

```
CHIHOO/
├── CLAUDE.md
│
├── business/              # 사업 기획
│   ├── class/             #   클래스 기획 (CLASS_SPEC.md, 시즌기획, 커리큘럼)
│   ├── product/           #   상품/굿즈 (SHOP_SPEC.md, 굿즈기획)
│   ├── marketing/         #   마케팅 (블로그, SNS, 이벤트)
│   ├── sales/             #   영업/제휴 (B2B, 학교, 지자체)
│   └── brand/             #   브랜딩 (제품사진, 디자인에셋)
│
├── operations/            # 운영
│   ├── 일지/              #   운영 일지
│   └── 공급처/            #   재료/용기 공급처
│
├── dev/                   # 개발 프로젝트 (각각 독립 git repo)
│   ├── chihoo.com/        #   웹사이트 (Next.js, Supabase)
│   └── chihoo-dashboard/  #   관리자 대시보드
│
├── meetings/              # 회의록
├── reference/             # 참고자료
└── assets/                # 공유 에셋 (PDF, 포스터 등)
```

## 작업 가이드

- `dev/` 하위 프로젝트는 각각 독립 git repo. 해당 프로젝트의 CLAUDE.md·컨벤션을 따를 것.
- `business/` 문서 작성 시 기존 문서(CLASS_SPEC.md, SHOP_SPEC.md)의 톤과 구조를 참조.
- 새 문서 작성 시 파일명에 날짜 포함 권장: `260313_시즌기획_봄.md`
- 회의록은 `meetings/`에, 참고 원본(녹취 등)은 `reference/`에 보관.
