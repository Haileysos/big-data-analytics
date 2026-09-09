# Data Lake vs Data Warehouse  
현대 데이터 아키텍처의 두 가지 핵심 저장소 모델 및 특성 비교  
|          | Data Lake | Data Warehouse |   
|:--------:|:---------:|:--------------:| 
| 스키마 접근 | Schema-on-Read 읽는 시점에서 구조 정의, 저장 시 원본 유지| Schema-on-Write 저장 시점에 엄격한 구조 정의 및 검증 |  
| 데이터 타입 | 모든 데이터(정형, 반정형, 비정형) | 정제된 정형 데이터(Structured) |  
| 비용/성능 | 저비용 스토리지, 대량 저장 유리 | 고비용, 고성능 쿼리 최적화 |  
| 주요 목적 | 데이터 탐색, 실험, 머신러닝 | 비즈니스 인텔리전스, 정기 리포팅 |  
| 유연성/거버넌스 | 높은 유연성, 약한 거버넌스 | 낮은 유연성, 강한 거버넌스 |  

<br>

Data Lake : 무엇을 분석할지 모를 때, 모든 데이터를 저장해 탐색과 실험을 하는데에 적합  
Data Warehouse : 무엇을 분석할지 명확할 때, 신뢰할 수 있는 고품질 데이터를 제공하는 데에 적합  

<br>  

## 핵심 트레이드오프  
저장비용 vs 쿼리속도  
> Lake : Object Storage로 저비용  
> Warehouse : 컴퓨팅+스토리지 결합으로 고속응답 제공  

유연성 vs 거버넌스  
> Lake : 자유로운 탐색 보장 but 품질 관리 어려움   
> Warehouse : 엄격한 품질 보장 but 변경 어려움  

실험 vs 표준화
> Lake : 데이터 사이언티스트의 실험적 분석에 적합  
> Warehouse : 경영진의 의사결정을 위한 표준 지표에 적합
 
<br><br>   

# Lake House  
###### Data Lake + Data Warehouse  

