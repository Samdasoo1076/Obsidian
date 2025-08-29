[[2025-08-29 회사]]

### 선언부 
USE [] = 데이터베이스 선택
GO = 배치 구분자 명령 단위 구분
    Ex SET ANSI_NULLS ON = NULL 비교 대신 IS NULL 사용하게함
    Ex SET QUOTED_IDENTIFIER ON = 큰따옴표로 식별자 지정 가능

### 프로시저 정의
ALTER PROCEDURE [스키마명].[프로시저명] (
    @입력받을 파라미터명 VARCHAR(3),
    @입력받을 파라미터명 int(3)
)

### 실행 환경 제어
SET NOCOUNT ON = DML 실행 후 x row(s) affected 메시지 표시 억제(결과 출력문 깔끔)
SET TRANSACTION ISOLATION LEVEL READ UNCOMMITTED = 격리 수준 설정

### 메인 구문
SELECT top 5 = 가장 최신 데이터 5행 가져옴
(SELECT top 1 ...) = 서브쿼리
with(nolock) = 실시간 정합성보다 **가용성/속도**가 더 중요한 **요약/현황** 조회.
convert(변경할 데이터 타입, 변경당할 컬럼명) = 데이터 타입 변환



> [!NOTE] 질문
> 그렇다면 
> SET TRANSACTION ISOLATION LEVEL READ UNCOMMITTED 와
> with(nolock) 차이가 무엇인가
> 전역 사용, 특정 쿼리, 테이블 내에서사용
> 공통점 : 조회가 쓰기에 의해 막히지 않도록 사용
> 도달 : 포틀릿이 많아 속도 우선을 위해서 사용한듯 
