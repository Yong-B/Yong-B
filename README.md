<!-- Header -->
<img src="https://capsule-render.vercel.app/api?type=waving&color=0:5B42F3,100:38BDF8&height=160&section=header" width="100%" alt="header" />

<div align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=18&duration=2800&pause=900&color=5B42F3&center=true&vCenter=true&width=600&lines=Backend+Developer;Java+%C2%B7+Spring+Boot+%C2%B7+JPA+%C2%B7+MySQL+%C2%B7+Redis" alt="typing" />

</div>

<br/>

## 🙋‍♂️ About Me

안정적인 흐름과 올바른 설계를 지향하는 백엔드 개발자입니다.

- 💳 **결제 · 환불 · 정산** — PG 재조회로 금액·시각을 대조한 뒤 승인하고, 웹훅은 서명 검증과 중복 차단을 거칩니다. 환불은 상품·수량 단위 부분 환불, 정산은 결제 이력 원장 기반 일별 사전 집계로 처리했습니다.
- 🔒 **동시성** — 비관적 락을 걸었는데도 1차 캐시와 REPEATABLE READ 스냅샷 때문에 예전 상태로 판단하던 문제를, 잠금 조회를 트랜잭션 첫 조회로 두고 flush·refresh로 해결했습니다. (동시 환불 후 재고 16 → 10)
- 📨 **Transactional Outbox** — 구매 확정과 outbox 저장을 한 트랜잭션에 묶어, 커밋 뒤 Kafka 발행이 실패해도 냉장고 입고 이벤트가 사라지지 않게 했습니다. 소비 실패는 재시도 후 DLT로 보내고, order_item_id UNIQUE로 입고는 한 번만 됩니다.
- 🔐 **인증 · 회원** — JWT Access/Refresh 발급·재발급과 Refresh Rotation을 구현했고, 결제·환불이 누적 구매금액을 동시에 바꾸는 Lost Update를 회원별 행 잠금으로 막았습니다.
- ✍️ **Blog** — [atom700.tistory.com](https://atom700.tistory.com)

<br/>

## 📌 Featured Projects

<table>
  <tr>
    <td width="33%" valign="top" align="center">
      <a href="https://github.com/Yong-B/take-care-of-my-fridge"><img src="https://github-readme-stats.vercel.app/api/pin/?username=Yong-B&repo=take-care-of-my-fridge&bg_color=30,5B42F3,38BDF8&title_color=ffffff&text_color=ffffff&icon_color=ffffff&hide_border=true&border_radius=12" width="100%" /></a>
      <br/><b>🧊 냉장고를 부탁해</b><br/>
      <sub>결제 · 환불 · 정산 · 구매 확정 이벤트</sub><br/>
      <sub>비관적 락 · Outbox · Kafka</sub>
    </td>
    <td width="33%" valign="top" align="center">
      <a href="https://github.com/Yong-B/Murder-Help"><img src="https://github-readme-stats.vercel.app/api/pin/?username=Yong-B&repo=Murder-Help&bg_color=30,5B42F3,38BDF8&title_color=ffffff&text_color=ffffff&icon_color=ffffff&hide_border=true&border_radius=12" width="100%" /></a>
      <br/><b>🔍 Murder-Help</b><br/>
      <sub>인증 · 회원 · 리뷰</sub><br/>
      <sub>JWT · 회원 등급 정합성 · 행 잠금</sub>
    </td>
    <td width="33%" valign="top" align="center">
      <a href="https://github.com/Yong-B/commerce-payment"><img src="https://github-readme-stats.vercel.app/api/pin/?username=Yong-B&repo=commerce-payment&bg_color=30,5B42F3,38BDF8&title_color=ffffff&text_color=ffffff&icon_color=ffffff&hide_border=true&border_radius=12" width="100%" /></a>
      <br/><b>💳 commerce-payment</b><br/>
      <sub>결제 · 웹훅</sub><br/>
      <sub>PortOne V2 · 결제 상태 관리</sub>
    </td>
  </tr>
</table>

<br/>

## 🛠 Tech Stack

| 분류 | 기술 |
|:---:|:---|
| **Backend** | <img src="https://img.shields.io/badge/Java-007396?style=flat-square&logo=openjdk&logoColor=white" /> <img src="https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white" /> <img src="https://img.shields.io/badge/Spring_Security-6DB33F?style=flat-square&logo=springsecurity&logoColor=white" /> <img src="https://img.shields.io/badge/Spring_Data_JPA-6DB33F?style=flat-square&logo=spring&logoColor=white" /> <img src="https://img.shields.io/badge/QueryDSL-0769AD?style=flat-square&logoColor=white" /> <img src="https://img.shields.io/badge/JWT-000000?style=flat-square&logo=jsonwebtokens&logoColor=white" /> <img src="https://img.shields.io/badge/WebSocket-010101?style=flat-square&logo=socketdotio&logoColor=white" /> |
| **Data** | <img src="https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white" /> <img src="https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white" /> <img src="https://img.shields.io/badge/Caffeine_Cache-8B5A2B?style=flat-square&logoColor=white" /> <img src="https://img.shields.io/badge/Apache_Kafka-231F20?style=flat-square&logo=apachekafka&logoColor=white" /> <img src="https://img.shields.io/badge/Elasticsearch-005571?style=flat-square&logo=elasticsearch&logoColor=white" /> |
| **Payment** | <img src="https://img.shields.io/badge/PortOne_V2-5B42F3?style=flat-square&logoColor=white" /> <img src="https://img.shields.io/badge/Webhook-38BDF8?style=flat-square&logoColor=white" /> <img src="https://img.shields.io/badge/ShedLock-555555?style=flat-square&logoColor=white" /> |
| **Infra / DevOps** | <img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white" /> <img src="https://img.shields.io/badge/AWS_EC2-FF9900?style=flat-square&logo=amazonec2&logoColor=white" /> <img src="https://img.shields.io/badge/AWS_ECR-FF9900?style=flat-square&logo=amazonaws&logoColor=white" /> <img src="https://img.shields.io/badge/AWS_S3-569A31?style=flat-square&logo=amazons3&logoColor=white" /> <img src="https://img.shields.io/badge/Parameter_Store-232F3E?style=flat-square&logo=amazonaws&logoColor=white" /> <img src="https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white" /> |
| **Test / Docs** | <img src="https://img.shields.io/badge/JUnit5-25A162?style=flat-square&logo=junit5&logoColor=white" /> <img src="https://img.shields.io/badge/Testcontainers-291A3F?style=flat-square&logo=testcontainers&logoColor=white" /> <img src="https://img.shields.io/badge/Swagger-85EA2D?style=flat-square&logo=swagger&logoColor=black" /> |
| **Tools** | <img src="https://img.shields.io/badge/IntelliJ_IDEA-000000?style=flat-square&logo=intellijidea&logoColor=white" /> <img src="https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white" /> <img src="https://img.shields.io/badge/Notion-000000?style=flat-square&logo=notion&logoColor=white" /> |

<br/>

## 📊 GitHub Stats

<div align="center">
  <img src="https://github-profile-summary-cards.vercel.app/api/cards/stats?username=Yong-B&theme=github" height="165" />
  <img src="https://github-profile-summary-cards.vercel.app/api/cards/most-commit-language?username=Yong-B&theme=github" height="165" />
  <br/>
  <img src="https://streak-stats.demolab.com?user=Yong-B&background=FFFFFF&ring=5B42F3&fire=38BDF8&currStreakLabel=5B42F3&hide_border=true" />
</div>

<br/>

<img src="https://github-readme-activity-graph.vercel.app/graph?username=Yong-B&bg_color=ffffff&color=5B42F3&line=38BDF8&point=5B42F3&area=true&hide_border=true" width="100%" alt="activity" />

<!-- Footer -->
<img src="https://capsule-render.vercel.app/api?type=waving&color=0:38BDF8,100:5B42F3&height=120&section=footer" width="100%" alt="footer" />
