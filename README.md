
# 네이버 부동산 매물 정보 스크래핑 
웹페이지 - https://rnrrmr.github.io




# 1. 작업환경 및 도구
[![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=rnrrmr)](https://github.com/anuraghazra/github-readme-stats)

# 2. 데이터 스크래핑

# 3. 웹 페이지 생성 및 호스팅

# 4. 평가 및 결과

## 문제사항
1. 매물을 클릭해서 나오는 상세페이지에서
1-1. 상단 이미지가 없어서 div 구조가 바뀌는 경우
    처음에 이미지가 있는지 없는지 if로 나눠서 접근
    -> 메종슈에뜨처럼 위에 이미지는 있는데 소재지가 없는 애들은 제대로 처리되어 나옴
1-2. table에 소재지가 존재하지 않아서 div 구조가 바뀌는 경우
    table에서 소재지 text가 초반에 존재하는지 확인
    -> 에러 제거없이 정상작동


2. 월세 전세 구분
구분해서 엑셀에 표현 완료
근데 이거를 전세나 월세 하나만 값을 가져와서 그 값을 기준으로 데이터를 정리하거나 해야할것같아
2-1 월세/전세 중 하나의 값만 찾아서 출력
    -> 나온 결과값의 비교가 쉬워짐
    -> 월세만 가져온다고 가정할 경우
        - 평수를 계산한다고 하고 근데 이게 의미가 없지 젤 싼방을 찾는게 아니니까

3. 이미지를 가져와야하나 말아야하나
    - 이미지가 없는 데이터가 있어서 어려울듯
    - 이거는 일단 보류

4. 가져온 이 데이터들로 어떤 통계자료나 그래프를 만들어서 의미를 부여 
- 월세가격 평균
- 전세가격 평균
- 지역별로 비교?


프로그램
인터넷 페이지
적당한 구성은 지도 홈페이지에 네이버지도를 구현해놓고 위치를 변경할 수 있게 해 놓고
변경한 위치를 기준으로 밑에 버튼으로 이 위치를 기준으로 매물 찾기를 가능하게 하고싶음
이 버튼을 누르면 지도 밑에 텍스트로 일단 매물들이 나올 수 있게 하고싶고
나올 텍스트는 코드로 구현

지도로 위치를 불러오는게 어려울경우
특정 위치 몇개를 마커로 저장해놓고
그 위치의 주소를 데이터에 입력
주소데이터의 '구'와 '동'을 기준으로 부동산 데이터를 검색 후
밑에 엑셀 형태로 화면에 뿌려줌

지도 하단에 엑셀 형식으로? 일단 데이터 정렬


소재지 필요 있나없나, 일단 소재지가 등록 안된 데이터도 많아서 굳이 의미가 있나 싶음
그리고 월세전세 둘중에 하나만 표현해주는게 더 나을 것 같기도하다는 생각이 듭니다.

좋은건 월세 매물보기랑 전세 매물보기를 따로 설정해서 두 버전으로 데이터를 확인할 수 있게 해주면 제일 좋겠지만 지금 하나도 막막한데 일단 하나라도 되게 해야지
그냥 문자중에 쉼표가 있으면 강제로 쉼표를 삭제?
그 후에 처리가 더 쉬울것같긴해


# 5. REFERENCE
- https://www.selenium.dev/documentation/
- https://guide.ncloud-docs.com/docs/ko/maps-web-sdk
- https://guide.ncloud-docs.com/docs/ko/maps-reversegeocoding-api
- https://getbootstrap.kr/docs/5.3/content/


