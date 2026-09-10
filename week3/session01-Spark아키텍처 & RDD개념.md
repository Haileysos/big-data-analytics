# MapReduce 의 한계 ▶ Spark 의 등장  
| MapReduce의 한계 | Spark의 등장 |  
|------------------|--------------|  
| 디스크 I/O 병목 <br> `각 단계마다 HDFS 읽기/쓰기로 인한 성능 저하` | 인메모리 처리 속도 <br> `MapReduce 대비 100배 이상 빠른 성능` |  
| 반복 알고리즘 비효율 <br> `머신러닝 등 반복 연산 시 매번 디스크 접근` | 통합된 API 환경 <br> `배치, 스트리밍, SQL, ML, 그래프를 하나의 엔진으로` |  
| 복잡한 파이프라인 <br> `코드 구현 난이도가 높고 유지보수 어려움` | 높은 사용 편의성 <br> `Python, Scala, Java, R 등 다양한 언어 지원` | 

<br><br>  

# Spark 발전 과정  

<br><br>

# Spark 아키텍처 구조도  

<br><br>

# RDD 핵심 개념  
###### Resilient Distributed Dataset을 지탱하는 4가지 기술적 특징    
1. 불변성 (Immutability)   
> 한 번 생성된 RDD는 수정 불가능 (Read-Only)   
> 데이터 변경이 필요하면 새로운 RDD를 생성해야 함    
> 이를 통해 일관성과 안전성 보장     

2. 분산처리 (Distributed)   
> 데이터셋은 여러 파티션으로 나뉘어 클러스터의 여러 노드에 분산 저장됨    
> 각 노드에서 병렬로 연산이 수행됨  

3. 장애복구 (Resilience)  
> 데이터 유실 시 리니지(Lineage)정보를 통해 유실된 파티션만 다시 계산해 복구  
> 데이터 복제를 하지 않아 메모리 효율적임  

4. 지연실행 (Lazy Evaluation)  
> Transformation 연산은 즉시 실행되지 않고 실행 계획(DAG)만 생성  
> Action이 호출되는 시점에 최적화된 경로로 연산이 수행됨  

## Transformation vs Action  
###### 지연실행(Lazy Evaluation)과 즉시실행(Eager Execution)의 비교  
