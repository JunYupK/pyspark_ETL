# ETL 파이프라인 구축하기
ETL 파이프 라인 구축과 이를 Kafka + pyspark를 활용하여 실시간 스트리밍 데이터 처리를 해보기 위한 프로젝트입니다.

기본적인 ETL 파이프라인 구축 후 Kafka와 결합하여 실시간 스트리밍 데이터 수집을 할 예정입니다.
어떤 데이터를 실시간 처리할지 추후 결정 후 연결 할 예정입니다.

[현재 프로젝트의 아키텍쳐]
![kafka-spark-arch](https://github.com/user-attachments/assets/ba964459-b77c-4cd6-a5f3-ca26a671b790)


<br>
[Issues]

* 대규모 데이터 스트리밍에 더 적합한 방식은 크롤링 서버 > Kafka > ETL 파이프라인 (Postgresql => Pyspark => MySQL)라고 생각되어 해당 방식으로 아키텍처 변경 예정

* Crwal4AI를 활용하여 웹 크롤링을 진행 예정 더 유연한 LLM 연결, 동적 크롤링 등 더 많은 이점이 있는 것으로 판단됨

* Crwal4AI의 schema 추출법을 명시하는 것이지 결국 Result에는 해당 페이지의 전문 HTML을 가져오며, 후에 extracted_content를 실행할때 해당 데이터 추출 스키마에 따라 데이터 추출이 가능하다, 한 result에 여러 스키마를 정의하여 데이터       추출이 가능한지는 추후 알아봐야 할 것
