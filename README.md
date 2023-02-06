# Visualize to protect the Elderly from traffic danger
노인 교통안전에 대한 문제점과 현재 부족한 대처 방식을 데이터로 시각화함으로써   
사실적으로 현 상황을 보여주고 개선방안을 제시하는 프로젝트입니다.
## Production period
- 2023.02.01 ~ 2023.02.03
## Participants and a major role
`김경목`: API 를 이용한 위도, 경도 데이터 추출 계획 설계, 데이터 전처리       
`윤규헌`: 지도 데이터 시각화, 데이터 전처리  
`맹지호`: 지도 시각화 디자인 설계, 데이터 전처리  
`민병창`: 그래프 시각화 설계, 데이터 크롤링, 데이터 전처리, 코드 종합
`신제우`: 데이터 전처리, 데이터 크롤링, 그래프 시각화 설계, 감독  
#### 모든 파트에 전반적으로 서로를 서포팅하는 팀 운영이 이루어졌습니다.
## Tech Stacks
<div align=center>
    <img src="https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=Pandas&logoColor=white">  
    <img src="https://img.shields.io/badge/Matplotlib-006c66?style=for-the-badge&logo=Matplotlib&logoColor=white">
    <br>
    <img src="https://img.shields.io/badge/Folium-77B829?style=for-the-badge&logo=folium&logoColor=white">
    <img src="https://img.shields.io/badge/BeautifulSoup-4A154B?style=for-the-badge&logo=BeautifulSoup&logoColor=white">
    <img src="https://img.shields.io/badge/Selenium-43B02A?style=for-the-badge&logo=Selenium&logoColor=white">
    <br>
    <img src="https://img.shields.io/badge/KaKao API-FFCD00?style=for-the-badge&logo=API&logoColor=white">
    <img src="https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=Git&logoColor=white">
    <img src="https://img.shields.io/badge/Github-181717?style=for-the-badge&logo=GitHub&logoColor=white">
</div>

## References

TMACS, [서울시 사고다발지점 전체 사고 데이터], 2021,사고누적지 사고지표  
TMACS, [서울시 교통약자다발지점 고령자 사고 데이터], 2021 ,교통약자다발지점 사고지표  
통계청, [2022 고령자 통계], 2022-09-29  
서울 열린데이터 광장, [서울시 노인, 장애인 보호구역 지정 현황],2022.03.17  
행정안전부, [빅데이터 분석으로 노인 교통사고 줄인다], 2022.10.11  

### 초기 의견들
1.버스운행정보를 활용하여 지역별 운행편의성점수 매겨보기
- 지하철 정보도 활용해서 지하철이 있는 지역에 추가 점수 부여
- 인구랑 대중교통 이용 데이터는 있는지 못봤는데 , 있다면 대중교통 사용 인구수 비례하여 
  점수를 메기면 좋을 것 같기도
- km 이동거리 당 걸리는 시간을 점수로 메기고, 배차간격에 대한 점수를 메기는 등..
- 점수 메기는 기준을 우리가 설정해야 한다는 어려움이 있을듯
2.대한민국 CCTV 정보를 활용한 범죄률확인 및 추가 CCTV 건의 지역

### 크롤링 실패
- TMACS의 데이터가 각 지역구별로 따로따로 csv파일저장을 해야했기에 데이터 획득을 위해 크롤링을 시도했다. 
  아래 사진을 보면 TMACS의 웹 페이지에서 스크롤 안에 스크롤이 존재함을 알 수 있다.  
![image](https://user-images.githubusercontent.com/43203949/216940081-17868715-af0e-42fc-b922-1f248fe5e2ce.png)
- TMAC의 웹 페이지 구성 형태가 매 스크롤시 마다 초기화 되는 방식이었고, CSS단위로 묶기도 어려운 형태였다 크롤링을 전문적으로 배워본 적 없이 잠시 공부하여 시도를 했고, 5시간을 들였지만 결국 데이터 획득에 실패했다. 이는 팀 전체에 민폐가 되는 행동이었으며 지도데이터 시각화를 돕지 못한 원인이 되었다. 
- 그래도 시도해본 것에 의의를 두며 데이터 획득 및 전처리의 어려움에 대해 확실히 알게 된 프로젝트였따.
