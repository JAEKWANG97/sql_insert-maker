# 수집한 데이터(csv파일) SQL Insert 문 생성기

이 Python 스크립트는 웹 크롤링으로 수집한 데이터를 데이터베이스에 삽입하기 위한 SQL INSERT 문을 생성하는 도구입니다.

## 결과물

![image](https://github.com/user-attachments/assets/a625638f-2bba-4083-a9db-2e77cc7de20b)

해당 수집된 데이터에서 생성된 Insert문

![image](https://github.com/user-attachments/assets/b02ef3e7-3dd2-4fa8-8098-81c493356961)



## 목적

웹에서 크롤링한 데이터를 서버의 데이터베이스에 업로드하기 전에 필요한 SQL INSERT 문을 자동으로 생성합니다. 이를 통해 크롤링 데이터의 데이터베이스 적재 과정을 간소화합니다.

## 기능

- 크롤링한 데이터가 저장된 CSV 파일을 읽습니다.
- 사용자 입력을 받아 대상 테이블 이름과 컬럼을 지정합니다.
- 각 데이터 행에 대한 SQL INSERT 문을 생성합니다.
- 생성된 SQL 문을 파일로 저장합니다.
- SQL 문자열 내 특수 문자(작은따옴표)를 자동으로 이스케이프 처리합니다.

## 사용 방법

1. 크롤링한 데이터를 CSV 형식으로 저장합니다.
2. 이 스크립트를 실행합니다.
3. 프롬프트에 따라 다음 정보를 입력합니다:
   - 데이터를 삽입할 테이블 이름
   - 사용할 컬럼 이름 (쉼표로 구분)
   - 크롤링 데이터가 저장된 CSV 파일 경로 (기본값: ./output.csv)
   - 생성될 SQL 파일 경로 (기본값: ./output_sql.txt)
4. 스크립트 실행이 완료되면 지정된 경로에 SQL INSERT 문이 포함된 파일이 생성됩니다.

## 요구 사항

- Python 3.x
- pandas 라이브러리

## 주의사항

- CSV 파일은 UTF-8 인코딩이어야 합니다.
- 생성된 SQL 파일은 UTF-8 인코딩으로 저장됩니다.
- 대량의 데이터를 처리할 경우, 생성된 SQL 파일의 크기가 매우 클 수 있으므로 주의가 필요합니다.
- 실제 데이터베이스에 적용하기 전에 생성된 SQL 문을 검토하는 것이 좋습니다.
