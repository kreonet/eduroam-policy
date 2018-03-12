---
title: "국가에듀롬 운영약관 v0.1"
subtitle: "eduroam KR NRO Provisions v0.1"
author: "장민석(msjang@kisti.re.kr)"
date: "2018-03-12"
output:
  word_document:
    reference_docx: ref/template-batang.docx
    toc: yes
    toc_depth: 2
  pdf_document:
    toc: yes
    toc_depth: '2'
  html_document:
    toc: yes
    toc_depth: '2'
---

<!--
<h1>대한민국 에듀롬 국가로밍운영기관 운영정책 v0.01</h1>

[TOC]
-->

# 0. 문서 변경 사항

일자       | 버전  | 비고
-----------|-------|--------------------
2018-03-12 |  v0.1 | 초안 작성 by 장민석


# 0. 용어 및 약어

**국문 / 영문 / 약어 표**

국문 | 영문 | 약어
-----|------|-----
국가(대한민국)에듀롬서비스 | eduroam Korea | eduroam KR
계정관리기관 | ID Provider | IdP
서비스제공기관 | Service Provider | SP
로밍운영기관 | Roaming Operator | RO
국가로밍운영기관 | National Roaming Operator | NRO
글로벌에듀롬위원회[^GeGCv1] [^GeGCv2] | Global eduroam Governanace Committee | GeGC
글로벌에듀롬정책[^GeCS] | Global eduroam Compliance Statement | GeCS
범유럽 연구교육망[^GEANT] | GEANT | GEANT
사용제한정책 | Acceptable Use Policy | AUP


[^AARNetPolicy2015]: [2016-11-25, National eduroam Federation Policy v0.01, AARNet, Neil Witheridge](https://wiki.aarnet.edu.au/download/attachments/9110088/NationalEduroamPolicy_001.pdf?version=1&modificationDate=1448414135094&api=v2)

[^GeGCv1]: [2010-09-22, Global eduroam Governance, GEANT(TERENA)](https://www.geant.org/Innovation/SIG_TF/PublishingImages/Pages/GeGC/TSec%2810%29015-GlobaleduroamGovernance-ConsensusVersion.pdf)

[^GeGCv2]: [2016-12-09, Global eduroam Governance Committee Charter v2.0](https://www.eduroam.org/wp-content/uploads/GeGC_Charter_v2.pdf)

[^GeCS]: [2011-10-04, eduroam Compliance Statement v1.0, GEANT(TRRENA) TSec(11)043](https://www.geant.org/Innovation/SIG_TF/PublishingImages/Pages/GeGC/eduroam_Compliance_Statement_v1_0.pdf)

[^GEANT]: GEANT은 유럽의 국가연구교육망(NREN) 연합체이다. 2002년 GEANT의 전신인 TERENA의 태스크포스팀 TF-Mobility로부터 eduroam이 시작되었다. eduroam의 기술적인 사항은 [RFC7593 - The eduroam Architecture for Network Roaming](https://tools.ietf.org/html/rfc7593)에 기술되어 있다.


**에듀롬(eduroam)**

에듀롬(eduroam)은 전세계 연구교육망의 연계를 통해 각 네트워크의 구성원들에게 범세계적 인터넷을 제공하는 서비스이다.

에듀롬 사용자는 소속기관에서 사용중인 인증정보(로그인 정보, ID/PW)을 이용하여 전세계 에듀롬에 접속하여 인터넷을 이용할 수 있다. 인증은 인증정보의 로밍을 통해 사용자의 소속기관(계정관리기관, IdP)에서 수행된다. 인증이 성공하면, 방문기관(서비스제공기관, SP)은 사용자에게 인터넷 접속을 허가한다.

에듀롬은 무선 또는 유선 네트워크로 제공된다. 무선 네트워크는 SSID "eduroam"을 통해 제공된다. 자격증명을 포함하여 인증정보를 1회 설정하면, 사용자는 모든 SP에서 에듀롬을 자동으로 이용할 수 있다.


**인증정보(Credentials)**

인증정보는 사용자를 식별할 수 있는 정보로, 아이디와 비밀번호로 구성된다. OTP와 같은 2차 인증수단도 추가될 수 있다. 계정관리기관(IdP)이 발급/관리한다.


**계정관리기관(Identity Provider, IdP)**

계정관리기관(Identity Provider, IdP)은 사용자에게 에듀롬 접속을 위한 인증정보를 발급하고 관리하는 기관이다. 서비스제공기관(SP)으로부터 인증정보가 포함된 인증요청을 전달받아 판별하고 응답한다. 소속기관(Home Institute)으로도 불린다.

다수의 계정관리기관은 기존에 사용중인 인증정보를 에듀롬과 연동하여 이용하고 있다. 이 경우 사용자는 기존에 이용중인 인증정보로 에듀롬을 이용할 수 있다. 하지만 기관 내 정책에 따라 에듀롬 서비스를 요청한 이용자에 한하여 별도의 인증정보를 발급할 수도 있다. 이 경우 사용자는 별도의 암호로 에듀롬을 이용할 수 있다.


**1.1.5. 서비스제공기관(Service Provider, SP)**
서비스제공기관(Service Provider, SP)은 IdP를 통해 인증된 사용자들에게 인터넷 서비스를 제공하는 기관이다. 사용자로부터 인증정보를 받아 계정관리기관(IdP)에 인증요청을 하고, 유효한 인증에 대해 인터넷 접속을 허가한다. 방문기관(Visited Institute)으로도 불린다.


**1.1.6. 소속기관(Home Institute)**

소속기관(Home Institute)은 사용자가 속한 기관이다. 소속기관은 사용자에게 인증정보를 발급/관리하는 IdP의 기능을 수행한다. 또한 소속기관 내/외의 에듀롬 사용자에게 인터넷 서비스를 제공하는 SP의 기능도 수행한다.


**방문기관(Visited Institute)**

방문기관(Visited Institute)은 사용자가 방문한 기관이다. 방문기관은 사용자에게 인터넷 서비스를 제공하는 SP의 기능을 수행한다.


**로밍운영기관(Roaming Operator, RO)**

로밍운영기관(Roaming Operator, RO)은 NRO에서 위임받아 그 역할을 수행하는 기관이다. 다수의 IdP와 SP를 연계하여 인증요청/응답을 전달하여 인증정보의 로밍을 제공한다. RO 내부에서 처리할 수 없는 인증요청은 NRO로 보내거나 폐기한다.


**국가로밍운영기관(National Roaming Operator, NRO)**

국가로밍운영기관(National Roaming Operator, NRO)은 글로벌에듀롬위원회로부터 한 국가의 에듀롬 운영을 위임받은 기관이다. RO부터 수신한 인증요청/응답을 다른 RO나 다른 국가의 NRO로 전달한다. 타 국가의 NRO에서 수신한 요청/응답도 이와 유사하게 처리한다.


# 1. 연동기관 및 일반규칙

## 1.1. 국가에듀롬, 국가로밍운영기관(NRO)

**(구성)**

1.1.1. 국가에듀롬(대한민국에듀롬, eduroam KR)은 대한민국 기관들의 참여로 구성된 에듀롬이다.

1.1.2. 대한민국의 각 기관은 국가에듀롬 가입신청을 통해 글로벌에듀롬을 이용할 수 있다.

1.1.3. RO와 국가에듀롬에 가입한 기관은 NRO의 정책을 준수해야 한다.

**(운영)**

1.1.4. NRO는 국가에듀롬을 운영한다.

1.1.5. NRO는 대한민국의 실정법에 따라 GeCS를 수정/보완하여 새로운 운영정책을 수립/적용할 수 있다.

1.1.6. NRO는 기관간 협약을 통해 NRO를 대리할 여러 RO를 지정할 수 있다.

1.1.7. NRO는 국가수준의 RO 및 SP와 IdP의 상호운용을 위해 국가에듀롬기반시설을 운영한다.

**(국가에듀롬의 운영주체)**

1.1.8. 국가에듀롬의 NRO는 대한민국의 국가연구망(NREN) 인 국가과학기술연구망(KREONET)을 운영하는 한국과학기술정보연구원(KISTI)이 2012년도부터 그 역할을 수행하고 있다. (이후 본 문서에서 언급되는 NREN은 KREONET을 의미한다.)


## 1.2. 부문에듀롬, 로밍운영기관(RO)

**(설립)**

1.2.1. RO는 참여기관의 지리적, 기능별, 성격별로 설립되어 국가에듀롬에 참여할 수 있다.

**(구성)**

1.2.2. RO는 국가에듀롬을 대리하여 설립목적에 맞는 기관을 모집할 수 있다.

1.2.3. RO에 가입한 기관은 NRO와 RO의 정책을 준수해야 한다.

**(운영)**

1.2.4. RO는 부문에듀롬을 운영한다.

1.2.5. RO는 부문수준의 SP와 IdP의 상호운용을 위해 부문에듀롬기반시설을 운영한다.

**(국가에듀롬의 RO)**

1.2.6. 국가에듀롬의 RO는 다음과 같다;
(1) 국공립고등교육RO : 고등교육기관(대학/대학교) 담당,  
(2) 공공연구RO : 출연연 담당,  
(3) 기타RO : 나머지 기관 담당

1.2.7. 국가에듀롬의 국공립고등교육RO는 2015년부터 전남대에서 그 역할을 수행하고 있다.

1.2.8. 국가에듀롬의 공공연구RO와 기타RO는 KISTI에서 그 역할을 수행하고 있다.

## 1.3. 글로벌에듀롬과 국가에듀롬

1.3.1. KREONET/KISTI는 2012년 GeGC와 GeCS 협약 조인을 통해 국가(대한민국)에듀롬을 대표하며, KREONET은 국가(대한민국)에듀롬의 NRO로서 기능적 역할을 수행한다.

1.3.2. 본 정책은 KISTI가 소유/관리한다. 본 정책은 GeCS의 필수사항을 만족하며, 국가(대한민국)에듀롬의 NRO 및 참여기관의 역할과 의무에 관한 필수사항과 권고사항을 명시한다.

1.3.3. 국가(대한민국)에듀롬의 RO 및 참여기관은 반드시 본 정책을 준수해야 한다.

## 1.4. 권한, 준수, 정책 개정

1.4.1. 본 정책의 권한은 NRO에게 있다. NRO는 RO와 참여기관이 본 정책의 필수/권고사항을 준수하도록 모니터링할 의무가 있다.

1.4.2. NRO가 운용하는 국가에듀롬기반시설에 연결하는 참여기관은 본 정책을 동의한 것으로 간주되며, 참여기관은 본 정책을 준수해야 한다.

1.4.3. 본 정책의 위반사항이 발견될 경우, NRO는 관련 참여기관의 에듀롬관리자에게 위반사항을 고지하고 해결방안을 권고한다. 기한 내 통지사항이 조치되지 않을 경우, NRO는 해당 참여기관의 에듀롬 참여를 제한할 권리가 있다.

1.4.4. NRO가 본 정책의 위반사항에 대해 즉각적인 조치가 필요하다고 판단한 경우, NRO는 에듀롬의 무결성과 보안을 위해 해당 참여기관의 사전통보 없이 에듀롬 참여를 즉시 제한할 권리가 있다.

1.4.5. RO 및 참여기관의 협의 및 차후 승인을 위해, 본 정책 개정안은 국가에듀롬 운영위원회에 제출되기 이전에 NRO의 내부검토와 승인이 필요하다.

1.4.6. 개정된 국가에듀롬 정책은 국가에듀롬 운영위원회의 승인 이후 모든 국가에듀롬 참여기관에 배포된다. 참여기관은 정책반영을 위한 2개월 이내의 과도기간 이후, 개정된 국가에듀롬 정책의 수용여부를 알린다.

1.4.7. 참여기관은 과도기간 중에도 현재 정책을 준수해야 한다. 현재 정책 항목이 개정된 정책 항목에 의해 대체되는 경우, 둘 중 한 가지를 준수한다. 최종결론을 내린 참여기관은 수정된 정책을 준수해야 한다.

1.4.8. 과도기관이 종료된 후 개정안에 승인을 거부한 참여기관은 국가에듀롬의 참여기관에서 제외된다.

1.4.9. NRO는 참여기관의 보안을 위해 즉각적인 조치가 필요한 경우, 국가에듀롬 서비스를 즉각 중지하고 필요한 조치를 취할 수 있다. 특정 위협에 의해 본 정책의 수정이 필요하면, NRO는 본 정책에 명시되지 않은 절차를 적용할 권리가 있다.

## 1.5. 에듀롬 상표와 로고

**(글로벌에듀롬의 상표권 보유)**

1.5.1. GEANT은 유럽연합의 에듀롬의 상표권 eduroam®을 보유하고 있다.

**(국가(대한민국)에듀롬의 상표권 보유)**

1.5.2. GeGC의 권고에 따라 2015년 KREONET은 국가(대한민국)에듀롬을 위한 에듀롬 상표와 로고를 등록하였다.

# 2. 참여기관 및 참여자격

## 2.1. 참여기관의 일반규칙

2.1.1. IdP를 운영하는 기관은 반드시 SP를 운영해야 한다.

## 2.2. 참여기관 범주

**(IdP+SP)**

2.2.1. IdP+SP는 IdP와 SP를 모두 운영하는 국가에듀롬 참여기관이다.

2.2.2. IdP+SP는 반드시 RADIUS서버를 운영해야 한다.

2.2.3. IdP+SP는 에듀롬 인증 및 사용자의 인터넷 트래픽을 참여기관이 가입한 NREN을 통해 전송해야 한다.

**(SP-Only)**

2.2.4. SP-Only는 SP만 운영하는 국가에듀롬 참여기관이다.

2.2.5. SP-Only는 직접 RADIUS서버를 운영할 수도 있고, 다른 기관의 RADIUS서버를 이용할 수 있다.

2.2.6. SP-Only가 직접 운영하는 RADIUS서버는 국가에듀롬기반시설에 다음과 같은 방식으로 연결된다;  
(1) 참여기관이 가입한 NREN을 통한 직접 연결,  
(2) NREN에 가입한 다른 참여기관을 통해 간접 연결,  
(3) ISP를 통한 간접 연결

2.2.7. SP-Only는 에듀롬 인증 및 사용자의 인터넷 트래픽을 SP-Only가 가입한 NREN을 통해 전송하거나, ISP를 통해 전송해야 한다.

**(NRO)**

2.2.8. NRO는 국가에듀롬 참여기관이 본 정책을 적용 및 운영하기 위한 지원을 제공해야 한다. 이는 모니터링 및 관리기능을 포함하며, 부록C에 기술되어 있다.

## 2.3. IdP+SP의 참가자격 및 규칙

2.3.1. IdP+SP의 참가자격은 NREN 정관에 동의한 NREN 회원기관으로 제한한다.

2.3.2. IdP+SP는 본 정책에 기술된 IdP와 SP의 정책(역할, 의무, 운영에 관한 필수/권고사항 등)을 모두 준수해야 한다.

2.3.3. IdP+SP으로 새로 참여하는 기관은 NREN이 제정/관리하는 국가에듀롬 가입절차를 따라야 한다.

2.3.4. IdP+SP는 에듀롬을 위한 네트워크 접속비용을 부담해야 한다.


## 2.4. SP-Only의 참가자격 및 규칙

2.4.1. SP-Only의 참가자격은 IdP+SP의 사용자에게 네트워크를 제공하기 위해 소정의 필수사항을 만족하는 국가 내 모든 기관에게 열려있다.

2.4.2. SP-Only는 본 정책에 기술된 SP의 정책(역할, 의무, 운영에 관한 필수/권고사항 등)을 모두 준수해야 한다.

2.4.3. SP-Only으로 새로 참여하는 기관은 NREN이 제정/관리하는 국가에듀롬 가입절차를 따라야 한다.

2.4.4. SP-Only는 에듀롬을 위한 네트워크 접속비용을 충당하기 위해 다른 참여기관들과 합의할 수 있다.


## 2.5. NRO 및 참여기관의 책임과 의무

2.5.1. GeCS를 따르는 국가에듀롬 NRO와 참여기관은 본 정책을 준수하여  가능한한 최선의 서비스를 제공한다.

2.5.2. GeCS를 따르는 다른 국가의 국가에듀롬 NRO와 참여기관은, 해당 국가의 국가에듀롬 정책을 따르며 최선의 서비스(Best Effort)를 제공한다.

2.5.3. 국가에듀롬 NRO와 참여기관은 에듀롬 서비스를 제공하고 사용함에 있어 에듀롬 서비스의 손실, 중단, 사용 등 모든 측면에 대한 법적 책임이 있다.


# 3. 참여기관의 역할과 책임

## 3.1. IdP

3.1.1. IdP의 역할은 사용자의 신원과 인증정보를 관리하며, 사용자를 인증하는 것이다. 에듀롬을 통한 사용자 인증으로 SP의 네트워크에 접속하는 사용자는 SP의 NREN 접속규정을 준수해야 한다.

3.1.2. IdP는 부록A에 명시된 IdP에 관한 GeCS의 관리 및 기술 필수사항을 준수해야 한다.

3.1.3. IdP는 IdP의 네트워크 AUP를 공지하고, 사용자가 이를 준수할 수 있도록 동의를 구해야 한다.

3.1.4. IdP는 사용자의 단말과 상호인증을 위한 RADIUS 서버를 구성해야 한다. 상호인증은 사용자의 단말이 RADIUS 서버의 X.509 인증서를 승인하여 이루어진다. 만약, 서버인증서를 발급한 인증기관(CA)의 루트 또는 중간 인증서가 사용자의 단말에 자동으로 설치되지 않는다면, 이를 이용가능하도록 해야 한다.

3.1.5. IdP는 사용자가 기관 외부에서 에듀롬을 사용하기 앞서, 기관 내부에서 에듀롬 인증을 설정 하고, 인증 성공 여부를 확인시켜 줄 수 있어야 한다.

3.1.6. IdP는 에듀롬 사용에 관한 최종사용자 의무사항을 사용자에게 고지해야 한다. IdP는 IdP가 인증한 사용자의 행위에 대한 책임이 있다. 최종사용자 의무사항은 다음을 포함한다:

* 에듀롬을 통해 SP의 네트워크에 접속할 때, 사용자는 IdP의 AUP와 SP의 AUP를 모두 준수해야 한다. 두 AUP가 다르거나 상충될 경우, 더 제한적인 규정이 적용된다. (SP는 AUP를 준수하지 않는 사용자의 접속을 거부할 수 있으며, 위반사항을 사용자의 IdP에 통지할 수 있다.)
* 사용자가 에듀롬을 처음으로 사용할 경우, 에듀롬 인증 설정과 확인은 사용자의 소속기관에서 수행할 것을 추천한다.
* IdP의 인증 구성은 상호인증을 권장한다. 상호인증은 사용자의 기기에서 IdP의 RADIUS 서버인증서를 승인하여 구성된다.
* 사용자의 인증정보는 보호되어야 하고 공유되지 않아야 한다.
* 의심되거나 확인된 자격증명 분실 및 손실은 IdP의 에듀롬 관리자에게 신속히 보고되어야 한다.
* 에듀롬을 사용하면서 발생하는 결함과 문제점은 IdP, SP, 또는 IdP와 SP 모두에게 보고되어야 한다.
* 사용자 기기의 보안은 최신으로 관리되어야 한다. 예를들어, 적절한 보안 패치와 안티바이러스 백신이 설치되어야 한다. 보안 취약점이 발견된 기기는 SP에 의해 네트워크 접속이 거부될 수 있다.

3.1.7. IdP는 SP가 보고한 사용자의 위반사항에 대해 적절한 조치를 취할 수 있으며, 사용자의 에듀롬 인증을 거부할 수 있다.


## 3.2. SP

3.2.1. SP의 역할은 에듀롬 인증이 성공한 사용자에게 네트워크 접속을 제공하는 것이다.

3.2.2. SP는 부록B에 명시된 SP에 관한 GeCS의 관리 및 기술 필수사항을 준수해야 한다.

3.2.3. SP는 SP의 AUP를 사용자에게 공지해야 한다.

3.2.4. 에듀롬 사용자에게 VLAN을 통해 SP의 기관네트워크와 분리된 전용 네트워크 접속 서비스를 제공하는것을 권장한다.

3.2.5. (L2 isolation) 사용자 기기의 보안 취약점을 SP나 SP의 다른 사용자에게 노출하지 않는 기능이 활성화된 격리된 VLAN을 구성할 것을 권장한다.

3.2.6. SP는 SP의 AUP를 위반한 사용자에게 네트워크 접속거부를 포함한 적합한 조치를 취할 수 있으며, 사용자의 IdP에 위반사항을 통지할 수 있다.


# 4. 참여기관 지원을 위한 협조사항

## 4.1. 운용성 시험 및 감시

4.1.1. IdP는 NRO에게 에듀롬 시험계정(ID/PW)을 제공한다. 이를 통해 NRO는 IdP의 운용성 시험, 감사, 모니터링을 수행한다. 시험계정의 ID는 test라는 문자열이 포함되어, 에듀롬사용보고서에서 자동으로 제외될 수 있도록 해야 한다. 시험계정을 사용할 수 없거나, 비밀번호가 변경되면 IdP는 NRO에 즉시 통지해야 한다.

4.1.2. SP는 SP의 RADIUS 서버에 NRO의 에듀롬 모니터(모니터링 서버)를 신뢰할 수 있는 클라이언트로 설정하여, 모니터의 인증요청이 국가에듀롬기반시설에 전달될 수 있도록 설정해야 한다. 이를 통해 NRO는 SP의 RADIUS에 인증요청을 발행하여 SP의 운용성 테스트, 감사, 모니터링 업무를 수행한다.

## 4.2. 지원 및 문제해결

4.2.1. 참여기관은 GeCS의 부록A와 B에 각각 명시된 바, 최종사용자 지원을 제공하고, 문제사항을 상위기관에 전달해야 한다.

4.2.2. SP는 에듀롬을 통해 SP의 네트워크 접속 서비스가 필요한, 국가에듀롬 및 글로벌에듀롬의 IdP 사용자를 지원해야 한다.

4.2.3. 참여기관의 에듀롬관리자는 참여기관에서 해결할 수 없는 최종사용자 또는 기반시설의 문제에 대해 NRO의 에듀롬담당자에게 지원을 요청할 수 있다.

4.2.4. 참여기관은 최종사용자 또는 참여기관 지원을 위한 NREN의 에듀롬 운용성 시험에 협조해야 한다.

## 4.3. 참여기관 연락처

4.3.1. 참여기관은 NREN에 최소 2인의 전담 기술담당자의 연락처를 제공해야 한다. 그 중 하나는 그룹 이메일 주소를 제공하는 것을 권장한다.

4.3.2. 참여기관은 NREN에 보안문제를 통지하기 위한 전담 보안담당자 1인의 연락처를 제공해야 한다. 이 인원은 기술인력과 동일한 사람일 수도 있다.

4.3.3. 참여기관은 NREN에 전담 관리담당자 1인의 연락처를 제공해야 한다. 이 인원은 NREN으로부터 1)정책문제, 2)본 정책에 대한 참여기관의 위반사항, 3)사용자의 AUP 위반사항을 통지받는다.

4.3.4. 참여기관의 연락처에 변동이 있을 경우, NREN에 즉시 통지해야 한다.

4.3.5. 참여기관은 최소 1인 이상의 기술담장자를 국가에듀롬 메일링리스트에 참여시켜야 한다.

## 4.4. 인증 트랜젝션과 네트워크 접속 로깅

4.4.1. 참여기관은 부록A와 B에 명시된 모든 인증요청을 로깅해야 한다.

4.4.2. 참여기관은 RADIUS 서버를 설정하여 시간(timestamp)을 정확하게 기록해야 한다. 시간(timestamp)은 UTC로 기록하는 것을 권장한다.

4.4.3. 인증 트랜젝션 로그는 사용자 비밀번호를 포함해서는 안된다.

4.4.4. 참여기관은 에듀롬 웹페이지를 통해 사용자에게 IdP, SP, NREN이 사용자 인증을 로깅하고 있음을 통지해야 한다.

4.4.5. 참여기관은 에듀롬 웹페이지를 통해 SP가 네트워크 접속 로그를 수집하고 있음을 통지하고, 이 로그는 인증 트랜잭션 로그와 연계되어 사용자의 IdP가 네트워크 접속을 수행하는 사용자를 식별할 수 있음을 통지해야 한다.

4.4.6. 참여기관은 에듀롬 웹페이지를 통해 국가의 법률을 준수하기 위한 로그의 저장 및 보호 방법에 대해 명시해야 한다.

4.4.7. 참여기관은 에듀롬 인증처리 또는 네트워크 접속 로그에 접속할 수 있는 사람을 인가된 직원으로 제한해야 한다. 로그는 정책적 문제와 AUP 위반사항을 해결하기 위해 NREN 및 다른 참여기관에 제공될 수 있고, 국가 에듀롬 운영을 위해 NREN이 이용될 수 있다.

## 4.5. 참여기관 에듀롬 웹페이지

4.5.1. 참여기관은 에듀롬 웹페이지를 통해 다음의 정보를 게제한다;  
(1) 본 정책의 준수 (국가에듀롬 웹사이트에 게재된 본 정책의 링크 포함)  
(2) 참여기관의 네트워크 접속에 대한 AUP 링크  
(3) 에듀롬 지원을 위한 기관 내부 연락처  
(4) 국가에듀롬 웹사이트 링크

4.5.2. IdP는 에듀롬 웹페이지를 통해 다음의 정보를 게재한다;  
(1) 사용자의 소속기관에서 에듀롬 인증을 설정을 권장하는 내용  
(2) 에듀롬 인증정보(ID/비밀번호)에 대한 안내와 국가에듀롬 인증방식에 대한 짧은 설명  
(3) IdP 서버인증서를 검증하는데 사용되는 인증기관(CA)의 루트 또는 중간 인증서 링크  
(4) 플랫폼 별 사용자 기기 설정 방법 또는 NREN이 제공하는 일반적인 설정방법에 대한 링크

4.5.3. IdP는 에듀롬 웹페이지를 통해 다음의 정보를 게재한다;  
(1) 에듀롬 SSID; 전세계 공용으로 `eduroam`이 이용되며, AP의 커버리지가 중복되는 경우 `eduroam-영문기관약어`가 이용됨  
(2) 지원하는 무선 암호화 프로토콜 (WPA2/AES 지원 필수)  
(3) 에듀롬 서비스 지도  
(4) 에듀롬사용자가 사용 가능한 네트워크 서비스 (프로토콜, 포트, 설명 등)


## 4.6. 통지 및 경보 

4.6.1. NREN은 NRO 웹사이트, 국가에듀롬 메일링 리스트, 전화 등을 통해 참여기관에게 보안경보를 통지할 수 있다. 참여기관은 24시간 이내에 NREN이 제시한 예방조치를 준수하고, 보안경보 확인 및 준수 여부를 메일을 통해 NREN에게 통지해야 한다.

4.6.2. 참여기관은 국가에듀롬 담당자의 이메일을 통해 다음의 사고를 24시간 이내에 통지해야 한다(국가에듀롬 담당자: eduroam@kreonet.re.kr);  
(1) 보안 위협  
(2) 오용 및 위반  
(3) 인증 및 접속 제한  
(4) 서버 오류

4.6.3. NREN은 임의의 사고, 서비스 중단, 서비스 변경 등에 대해 영향을 받는 참여기관에게 직접 통지하거나, NREN의 국가에듀롬 메일링리스트를 통해 모든 참여기관에게 통지해야 한다.


# 부록 A : IdP의 관리 및 기술 준수 사항

GeCS[^GeCS] Appendix A 에서 발췌

A.1. IdP는 eduroam 라우팅 패브릭에 연결하기 위한 RADIUS 인터페이스를 구현해야 한다.

A.2. IdP는 유뮤선 네트워크를 위한 EAP method를 구현해야 하며, 상호인증과 종단 간암호화를 지원해야 한다.

A.3. IdP는 접속요청을 수신한 유효한 인증된 로컬사용자에 대해 RADIUS 접속허용메시지를 전송해야 한다.

A.4. IdP는 유효하지 않은 사용자와 인증되지 않은 사용자에게 RADIUS 접속허용메시지를 전송하면 안된다.

A.5. IdP는 사용자 지원을 제공해야 한다. 지원 문제는 조정과 해결을 위해 NRO와 RO로 이관될 수 있다.

A.6. IdP는 모든 인증시도를 기록해야 한다. 다음 정보를 반드시 기록해야 한다:  
* 인증요청 및 해당응답의 시간(timestamp)  
* 인증요청에 포함된 외부 EAP identity (User-Name attribute)  
* 내부 EAP identity (actual user identifier)  
* 연결중인 클라이언트의 MAC 주소 (Calling-Station-Id attribute)  
* 인증응답유형 (예 : 수락 또는 거부)  
국가규정에서 규정하지 않으면 최소보유기간은 6개월 입니다.


# 부록 B : SP의 관리 및 기술 준수 사항

GeCS[^GeCS] Appendix B 에서 발췌

B.1. SP의 네트워크는 에듀롬 인프라에 연결하기 위한 802.1X와 RADIUS 인터페이스를 구현해야 한다.

B.2. SP의 무선네트워크(WiFi, IEEE 802.11)는 반드시 SSID로 `eduroam`을 브로드캐스트 해야 한다. 동일한 위치에 두개 이상의 SP가 있는 경우, `eduroam-`로 시작하는 SSID를 사용할 수 있다.

B.3. SP의 무선네트워크(WiFi, IEEE 802.11)는 반드시 WPA2/AES를 지원해야 하며, 레거시 하드웨어 사용자를 위해 WPA/TKIP를 추가로 지원할 수 있다.

B.4. SP의 네트워크는 IP주소와 DNS를 자동으로 구성하는 인프라를 제공해야 한다.

B.5. SP의 네트워크는 라우팅 가능한 IP 주소를 제공해야 하며, NAT 변환을 제공할 수도 있다.

B.6. SP는 에듀롬 인프라를 통해 에듀롬 참여기관으로 모든 EAP를 수정 없이 전달해야 한다.

B.7. SP는 SP의 네트워크에 접속한 에듀롬 사용자 또는 IdP에게 요금을 부과해서는 안된다.

B.8. SP의 서비스는 SP의 로컬 정책에 기반한다. 하지만, 사용자 연결에 대한 수정(예 : 액세스 목록, 임의의 포트를 거부하는 방화벽 필터 규칙, 어플리케이션 프록시 등)은 권장하지 않으며, 반드시 해당 NRO에 고지해야 한다.

B.9. SP는 다음과 같이 충분한 로깅 정보를 유지하여 로그인 한 사용자의 IdP를 식별할 수 있어야 한다 :  
* 인증요청 및 해당응답의 시간(timestamp)  
* 인증요청에 포함된 외부 EAP identity (User-Name attribute)  
* 연결중인 클라이언트의 MAC 주소 (Calling-Station-Id attribute)  
* 인증응답유형 (예 : 수락 또는 거부)  
* 공인IP가 사용된 경우, 접속 이후 클라이언트에게 발행된 L2 MAC 주소와 L3 IP주소의 연관관계 정보(예 : ARP 스니핑 로그, DHCP 로그)  
국가규정에서 규정하지 않으면 최소보유기간은 6개월 입니다.


# 부록 C : NRO의 역할과 책임

C.1. NREN은 GeCS[^GeCS]를 최선을 다해(best-effort) 준수해야 한다.

C.2. NRO는 본 정책을 수립하고 관리하며, 본 정책이 지속적으로 GeCS를 만족하도록 해야 하며, 참여기관들이 본 정책을 준수하도록 장려하고 모니터링 해야 한다.

C.3 NRO의 역할은 국가에듀롬기반시설을 제공하고 유지하는 것이다. 이를 통해 국내 참여기관간 상호운용 뿐만 아니라, 글로벌에듀롬인프라를 통한 참여기관의 국제적 상호운용이 가능하게 해야 한다.

C.4 NRO의 국가에듀롬 운영목표는 다음과 같은 과업을 달성하는 것을 포함한다 :  
(1) 자격을 갖춘 기관이 IdP+SP기관과 SP-Only기관으로 국가에듀롬에 가입 할 수 있도록 하는 프로세스를 정의하고 구현한다.  
(2) 본 정책에 따른 기관의 운영 준수를 평가하기 위한 감사 프로세스를 정의하고 구현한다. 운영감사의 수행은 NRO 또는 기관에 의해 요청될 수 있으며, 근무일 기준 10일의 통지기간을 두고 언제든지 요청될 수 있다. 통지기간 이후 NRO는 10일 이내에 감사를 수행하도록 노력해야 한다.  
(3) 기관의 실시간 에듀롬 운용성 모니터링을 제공하기 위해 국가에듀롬 모니터링 메커니즘 및 프로세스를 정의하고 구현한다.  
(4) 국가연동서버와 기관의 에듀롬 로그로부터 국가에듀롬 사용량 통계를 생성하고 안전한 웹사이트에 게시한다.  
(5) 국가에듀롬과 글로벌에듀롬에 사용될 참여기관 운영정보와 서비스 배포정보를 GeGC에 정의된 형식으로 유지한다.  
(6) NRO의 RADIUS 로그를 6개월 이상 안전하게 수집 및 보관한다. 로그는 다음을 포함한다: timestamp, 사용자의 외부 identity, 사용자 realm, 사용자 기기 MAC 주소, SP 서버, 인증 결과. 다음은 제외한다: 사용자 비밀번호.  
(7) 전담 기술인원을 통해 참여기관을 지원하며, 국가에듀롬에 적용된 다양한 기술에 대한 전문지식과 가이드도 제공한다.  
(8) 이메일(eduroam@kreonet.net)을 통해 고객 서비스 요청을 제출하고, 요청 처리 및 고객 상호작용 추적을 용이하게하는 이슈추적시스템을 제공한다.  
(9) 기술과 정책에 대한 논의를 촉진하고 올바른 대상에게 메시지를 전달하기 위한 메일링 리스트를 제공한다.  
(10) 보안문제를 판별하기 위해 보안권고사항을 모니터링 하고 기술 메일링 리스트에 가입한다. 그리고 에듀롬 서비스의 무결성과 보안을 유지하기 위해 기관에게 권고하며 필요한 조치를 요청한다.  
(11) 전용 NRO 웹사이트를 유지하고, 참여기관 관리자와 최종사용자를 위해 국가에듀롬서비스와 운영정보를 제공한다.  
(12) 표준플랫폼에서 일반적으로 eduroam을 구성하는 지침을 게시한다.  
(13) 글로벌에듀롬의 정보(링크)를 포함하여, 기관이 에듀롬을 도입하기 위한 정보를 게시한다.  
(14) 에듀롬 도입 정보를 제공하고, 행사와 컨퍼런스에서 에듀롬 서비스를 장려한다.  
(15) 국가에듀롬 워킹그룹과 위원회를 지속적으로 유지한다.  
(16) GeGC, 국제 컨퍼런스, 행사 참석 등을 통해 글로벌에듀롬 커뮤니티와 관계를 유지한다.  
(17) APAC 지역의 타 NRO에 필요한 직접적인 도움을 제공하고, 글로벌에듀롬인프라와 APAC 지역의 에듀롬서비스인프라에 기여한다.  
(18) 국내외 에듀롬 서비스의 발전에 기여한다.

