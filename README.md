# 백엔드 개발자

#### 안녕하세요, 건강관리와 기분관리를 잘하는 백엔드 개발자 주건정입니다.

##### Technical Skills: Typescript, Nodejs, React.js, Mysql, AWS

---

<!-- <br/> -->

<h2 style="color:#267CB9;">경력</h2>

---

<span style="font-size: 1.3rem">올바른코드</span><br/>
<sub><span style="color:gray;">서버개발자 | 개발2팀</span></sub><br/>
<sub><span style="color:gray;">2021.09. ~ 2024.04. (2년 8개월)</span></sub>

**[주요 역할]**<br/>
REST API 설계 및 개발, AWS 기반 인프라 설계·구축, 관리자 페이지 개발 등 백엔드 전반을 담당, 10회 이상의 서비스 배포를 통해 다양한 비즈니스 경험

- 팀의 서버 개발을 담당하고 기존에 없던 ERD, 시퀀스 다이어그램, 상태 다이어그램 등 **문서화 도입**
- 기존 엑셀 기반의 체크리스트를 관리자 페이지 내 게시판으로 개발로 QA팀 만족도 향상 (**타개발팀 시행**)
- **React.js**로 자사, 클라이언트 홈페이지 및 랜딩페이지 개발

**[프로젝트]**<br/>

1. 걸음 기부 서비스<br/>
   개인 및 기업 직원들의 걸음 데이터를 활용한 기부 플랫폼 운영 (회원수 4만)
   - 트랜잭션 기반 동시성 제어와 스케줄링 도입으로 중복 데이터 관리 효율화
   - PHP 레거시 시스템을 **React.js로 전환**, UX 개선 및 **업무 효율성 30% 향상**
   - EC2, RDS 모니터링으로 인스턴스 관리 **비용 30% 절감**
   - 클라이언트와 직접 소통하며 기획 단계부터 참여해 업무 효율성 극대화
2. 스파&마사지 예약 서비스<br/>
   14개 오프라인 매장의 예약 관리 플랫폼 운영

   - 개발 초기단계에서 인수 후, 환경 설정과 작업 방식 표준화를 통해 안정적인 서비스 배포 완료 (**기여도 80%**)
   - docker, 개발문서가 없는 인수인계 과정 중, 효율을 높이고자 담당 개발자 방문
   - 모든 매장의 스케줄 조회 속도를 **4초에서 0.9초로 개선 (약 77% 단축)**
   - 스키마 변경으로 인한 데이터 손실 발생 시, AWS RDS 스냅샷을 활용해 복구

3. 물류 배송 관리 서비스<br/>
   장례식장, 세척장, 배송기사 간 식판, 컵 등 세척 용기 추적 관리 플랫폼 개발
   - 팀의 담당 서버개발자로 첫 기획 참여 (**기여도 80%**)
   - 기획 담당자의 퇴사로 기존 메모장 정리를 시퀀스 다이어그램, 상태 다이어그램, ERD 문서화 도입
   - 각 룰에 따른 관리자페이지 개발 (**기여도 100%**)

---

### LNC컴퍼니

<sub><span style="color:gray;">대리 | 물류영업팀</span></sub><br/>
<sub><span style="color:gray;">2016.09. ~ 2020.11. (4년 3개월)</span></sub>

거래처와 일정 조율, 신규 업장 DP, 물류 관리, 제품 관리

<br/>

<h2 style="color:#267CB9;">프로젝트</h2>

---

### 콘서트 대기열 서비스 [LINK](https://github.com/JuGeonjeong/hhp-concert)

개인  
2024.10. ~ 2025.01.  
**nestjs, typescript, typeorm, mysql, docker, kafka, redis, jest**

현 서비스 업체에서 중요하게 다루는 부분을 직접 경험하고자, 콘서트예매 시 발생하는 동시 접속자 관리와 대기열 처리, 그리고 티켓 예매 기능을 효과적으로 제공하는 프로젝트를 구상했습니다. 이를 위해 사용하지 못했던 기술들을 일부 도입해 서비스 운영에 대한 학습을 목표로 삼았습니다.

1. **프로젝트 설계서 & API 문서화**  
   프로젝트 진행 과정에서 시퀀스 다이어그램, ERD, API 명세서를 설계해 전체적인 흐름을 명확히 파악하고 예기치 않은 문제를 미리 예상하고 최소화할 수 있었습니다.

2. **클린 아키텍처, TDD 방식으로 개발**  
   모듈 간의 구분으로 코드를 작성하여 코드 간의 결합을 최소화했습니다. 코드 변경이나 개발 시 기존 코드에 영향을 받지 않아 확장성 높았고 테스트코드를 통해 요구사항을 정의하고 성공하는 테스트를 작성 후 코드에 에러가 없음을 입증했습니다.

3. **대기열을 위한 동시성 최적화:** [데이터베이스 락](https://github.com/JuGeonjeong/hhp-concert/blob/main/doc/report/lock.report.md) · [Redis](https://github.com/JuGeonjeong/hhp-concert/blob/main/doc/report/redis.report.md) <br/>
   요구사항에 맞는 비관적락, 낙관적락을 구현했고 도메인 특성상 성능의 한계가 있었습니다. Redis 작업을 추가로 최적화 작업을 진행했습니다. Sorted set + Hash 작업으로 전환 **(처리율 50% 향상)**

4. **k6를 활용해 실제 서비스와 유사한 트래픽 환경을 구성하여 테스트를 진행**  
   대기열 구현 시, 쿠키를 이용해 토큰을 내려주는 방식과 Redis의 인메모리 데이터를 활용한 최적화 전략을 비교하기 위해 [k6 모의 테스트](https://github.com/JuGeonjeong/hhp-concert/blob/main/doc/report/k6.test.md)를 진행했습니다. 실전과 유사하게 **점진적으로 트래픽을 증가시키며** 테스트한 결과, **안정성을 높이고 불안 요소를 효과적으로 줄일 수 있었습니다.**

<br/>

<h2 style="color:#267CB9;">자기소개</h2>

---

협업을 통해 성장하고 싶은 백엔드 개발자, 주건정입니다. 저는 혼자보다는 팀과 함께 일하며 시너지를 내는 것을 즐기고, 취미로 단체 스포츠를 좋아합니다. 서로 생각을 공유하며 돕고 성장하는 과정에서 큰 보람을 느끼며, 이러한 가치를 팀에서도 실천하고자 노력해왔습니다. 단순한 협업을 넘어 팀 전체의 효율성과 환경까지 고민하며 더 나은 방향을 함께 만들어가는 데 힘써왔습니다.

저는 팀의 작업 환경을 유심히 관찰하며 비효율적인 부분을 개선하는 데서 보람을 느낍니다. 개발 업무 외에도 함께 사용하는 공간에서 불편함이 보이면 외면하지 않고 적극적으로 해결하려 노력했습니다. 예를 들어, 정리되지 않은 창고와 얽힌 케이블, 반복적으로 발생하는 소음 같은 사소한 문제들을 개선하며 팀원들이 업무에 더 집중할 수 있는 환경을 만들었습니다. 2년 반의 개발 경력 동안 이러한 태도를 바탕으로 비효율적인 프로세스를 개선하며 팀의 생산성을 높이는 데 기여했습니다. 저는 ‘괜찮은 개발자’란 코드뿐 아니라 함께 일하는 환경까지 배려하는 사람이라고 믿으며, 앞으로도 팀과 함께 성장하며 더 나은 가치를 창출하는 개발자가 되겠습니다.

<br/>

<h2 style="color:#267CB9;">학력</h2>

---

### 인덕대학교

<sub><span style="color:gray;">대학교(전문학사) | 비즈니스영어과</span></sub>  
<sub><span style="color:gray;">2018.03. ~ 2021.03. | 졸업</span></sub>
