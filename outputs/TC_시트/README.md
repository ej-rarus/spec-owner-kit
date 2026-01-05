# TC 시트 산출물

> tc-generator 에이전트가 생성하는 TC 시트 파일들

## 생성되는 파일

| 파일 | 용도 |
|------|------|
| `GoogleSheets_TC_Setup.js` | Google Sheets Apps Script |
| `(프로젝트명)_TC.xlsx` | Excel 버전 (선택) |

## Google Sheets 사용법

1. 새 구글 시트 생성: [sheets.new](https://sheets.new)
2. **확장 프로그램** > **Apps Script** 클릭
3. `GoogleSheets_TC_Setup.js` 내용 전체 복사하여 붙여넣기
4. 함수 선택에서 `createAllSheets` 선택
5. ▶️ 실행 버튼 클릭
6. 권한 승인 (최초 1회)

## 생성되는 시트

| 시트명 | 내용 |
|--------|------|
| 변수정의 | 드롭다운 값 목록 |
| MO_테스트케이스 | MO TC 100행 (MO-001 ~ MO-100) |
| PC_테스트케이스 | PC TC 100행 (PC-001 ~ PC-100) |
| 결함현황 | PASS/FAIL/N/T 자동 집계 |

## 커스터마이징

`GoogleSheets_TC_Setup.js` 파일의 `DROPDOWNS` 객체에서 프로젝트별 값 수정:

```javascript
const DROPDOWNS = {
  "기능영역": ["MAIN", "SHOP", ...],  // 프로젝트별 수정
  // 도메인 특화 변수 추가
};
```
