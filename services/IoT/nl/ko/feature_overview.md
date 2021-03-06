---

copyright:
  years: 2016

---

{:new_window: target="\_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:codeblock: .codeblock}
{:pre: .pre}

# {{site.data.keyword.iot_short_notm}} 기능 개요
{: #feature_overview}

마지막 업데이트 날짜: 2016년 6월 29일
{: .last-updated}

{{site.data.keyword.iot_full}}은 다음 키 영역에서 빌드됩니다.

  1. 연결 - 디바이스를 연결하고 애플리케이션을 개발합니다.
  2. 정보 관리 - 디바이스 데이터를 저장하고 검토하며 {{site.data.keyword.iot_short_notm}}을 다른 서비스와 통합합니다.
  3. 분석 - {{site.data.keyword.iot_short_notm}} 대시보드를 사용하여 실시간 디바이스 데이터를 시각화합니다.
  4. 위험 관리 - 사용자와 애플리케이션에 대한 액세스 제어를 사용하여 보안 연결과 아키텍처를 구성합니다.

## 연결
{: #connect}

{{site.data.keyword.iot_short_notm}} 연결은 {{site.data.keyword.iot_short_notm}} 서비스의 시작점입니다. 디바이스 연결, 애플리케이션 작성, 디바이스 제어 및 써드파티 서비스와 통합은 모두 {{site.data.keyword.iot_short_notm}} 연결에서 사용 가능합니다.

### 게이트웨이 디바이스

게이트웨이가 없으면 인터넷에 연결할 수 없는 {{site.data.keyword.iot_short_notm}}에 디바이스를 연결하는 데 게이트웨이를 사용합니다. 게이트웨이 디바이스는 디바이스와 애플리케이션의 기능을 결합합니다. 게이트웨이는 디바이스와 동일한 방식으로 명령을 받고 디바이스 데이터를 보내지만 애플리케이션과 동일한 방식으로 디바이스에 연결된 다른 디바이스에 명령을 보낼 수도 있습니다.

인터넷에 직접 연결할 수 없는 디바이스를 게이트웨이 디바이스에 연결할 수 있으며 해당 디바이스 데이터를 게이트웨이 디바이스에 보낼 수 있습니다. 그러면 이 데이터가 {{site.data.keyword.iot_short_notm}} 서비스에 전송될 수 있습니다. 

### 디바이스 관리

디바이스 관리 기능은 디바이스 관리 API와 디바이스에 설치된 디바이스 관리 에이전트를 조합하여 제공합니다. 관리 디바이스에서 디바이스 관리 조치를 수행할 수 있으며, 이 조치는 기본 {{site.data.keyword.iot_short_notm}} 대시보드를 통해 트리거할 수 있습니다. 

디바이스 관리를 사용하면 다시 부팅하고 펌웨어 업데이트를 다운로드하여 설치하고 원격으로 디바이스를 팩토리 설정으로 재설정하는 기능이 제공되며, 이 기능은 모두 {{site.data.keyword.iot_short_notm}} 사용자 인터페이스를 통해 제공됩니다.

### 써드파티 서비스 통합

디바이스 위치에서 현재 날씨를 찾을 수 있는 Weather Company 날씨 위치 서비스 지원을 포함하여 써드파티 서비스 통합은 {{site.data.keyword.iot_short_notm}}에 빌드됩니다.

---

## 정보 관리
{: #information_management}

{{site.data.keyword.iot_short_notm}} 정보 관리에서는 {{site.data.keyword.iot_short_notm}} 서비스에 도달한 후 디바이스에서 보낸 데이터를 제어합니다. 정보 관리에는 데이터 스토리지와 변환이 포함됩니다.

### 디바이스 마지막 이벤트 캐시

{{site.data.keyword.iot_short_notm}} 마지막 이벤트 캐시 API를 사용하면 디바이스에서 보낸 마지막 이벤트를 검색할 수 있습니다. 이 작업은 디바이스의 온라인 또는 오프라인 여부에 상관없이 작동하므로, 디바이스의 실제 위치나 사용 상태와 무관하게 디바이스 상태를 검색할 수 있습니다. 디바이스의 마지막 이벤트 데이터는 최대 365일 전에 발생한 특정 이벤트에 대해서만 검색할 수 있습니다.

### 디바이스 이벤트 데이터 저장

{{site.data.keyword.iot_short_notm}} 서비스의 디바이스 이벤트 데이터는 나중에 사용하도록 저장할 수 있습니다. 데이터 저장은 해당 데이터를 통해 이해하기 위해 통찰력 있는 분석을 수행하는 데 중요한 첫 번째 단계입니다. 예를 들어, 오랜 기간 동안 변경사항을 추적하고 Watson API 및 코그너티브 컴퓨팅 사용 등의 강력한 분석 도구와 사용하도록 데이터 세트를 저장할 수 있습니다.

---

## 분석
{: #analytics}

### 실시간 디바이스 데이터 시각화

대시보드 카드를 사용하여 실시간 디바이스 데이터를 시각화하고 표시할 수 있습니다. 대시보드 카드는 실시간으로 디바이스 데이터를 모니터하고 표시하므로, 키 디바이스 또는 디바이스 데이터를 계속 추적할 수 있습니다. 실시간 디바이스 데이터의 컨텍스트와 상태에 신속하게 액세스할 수 있도록 이러한 시각화는 기본 {{site.data.keyword.iot_short_notm}} 대시보드에 표시됩니다.

---

## 위험 관리
{: #risk_management}

### 보안 연결 및 아키텍처

{{site.data.keyword.iot_short_notm}}의 아키텍처는 디바이스가 다른 디바이스로 위장하지 못하게 하므로 디바이스 데이터의 무결성을 유지보수합니다. 디바이스에서 사용자만 아는 클라이언트 ID와 인증 토큰의 조합을 사용하여 {{site.data.keyword.iot_short_notm}}에 연결합니다. 디바이스를 등록하거나 API 키가 생성되고 나면 신임 정보의 보안을 유지보수하기 위해 인증 토큰이 솔트(salt)되고 해시됩니다. TLS v1.2를 통한 연결은 완벽하게 지원됩니다.

---
