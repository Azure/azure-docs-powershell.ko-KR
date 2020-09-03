---
title: Azure Stack PowerShell 개요 | Microsoft Docs
description: 설치 및 구성에 대한 설명을 포함한 Azure Stack PowerShell 개요입니다.
author: bganapa
ms.author: bganapa
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 09/21/2018
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 4b72bbd1bda93767251e0ba3d488f798575d9115
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/01/2020
ms.locfileid: "89244316"
---
# <a name="azurerm-module-250"></a>AzureRM 모듈 2.5.0

## <a name="requirements"></a>요구 사항:
지원되는 최소 Azure Stack 버전은 1904입니다.

참고: 이전 버전을 사용하는 경우 1.2.11 버전을 설치하세요.


## <a name="install"></a>설치
```powershell-interactive
# Remove previous versions of AzureStack modules
Uninstall-Module -Name AzureStack -Force 
Uninstall-Module -Name AzureRM -Force 
Uninstall-Module AzureRM.AzureStackAdmin -Force -ErrorAction Continue
Uninstall-Module AzureRM.AzureStackStorage -Force -ErrorAction Continue
Get-Module Azs.* -ListAvailable | Uninstall-Module -Force
Get-Module Azure.* -ListAvailable | Uninstall-Module -Force


# Install the AzureRM.Bootstrapper module. Select Yes when prompted to install NuGet
Install-Module -Name AzureRm.BootStrapper

# Install and import the API Version Profile required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2018-03-01-hybrid -Force

```

## <a name="release-notes"></a>릴리스 정보
* AzureRm.Resources
    * 2019-03-01-hybrid 프로필로 2018-05-01 API 버전을 지원하는 새로운 리소스 모듈
    * PolicyDefinition(2016-12-01) 및 PolicyAssisgment(2017-06-01-preview) 작업은 여전히 이전 API 버전으로 작동합니다.
* AzureRm.Compute
    * 2017-12-01 API 버전을 지원하는 새로운 컴퓨팅 모듈.'


* 이 릴리스는 azurestack 특정 API 프로필 2019-03-01-hybrid에 해당합니다.
* 모든 모듈은 AzureRm.Profile 모듈에 대한 종속성 이상으로 업데이트됩니다.
* 각 모듈이 지원하는 api 버전이 업데이트됩니다. 
    * 컴퓨팅 - 2017-12-30
    * 네트워크 - 2017-10-01
    * 스토리지 - 2016-01-01
    * 리소스 - 2018-02-01
    * Keyvault - 2016-10-01
    * Dns - 2016-04-01
* 각 리소스 종류에 대한 전체 API 버전 맵은 https://github.com/Azure/azure-rest-api-specs/blob/master/profile/2018-03-01-hybrid.json에서 확인할 수 있습니다.

## <a name="content"></a>콘텐츠:
### <a name="azure-bridge"></a>Azure Bridge
Azure의 이미지를 배포할 수 있게 해주는 Azure Stack AzureBridge 관리자 모듈의 미리 보기 릴리스입니다.

### <a name="backup"></a>Backup
관리자가 다음을 수행할 수 있도록 해주는 Backup 관리자 모듈의 미리 보기 릴리스입니다.
- 백업이 저장되는 위치 구성
- 백업 수행
- 완료된 백업 나열 및 복원

### <a name="commerce"></a>상거래
Azure Stack 시스템의 집계 데이터 사용량을 볼 수 있는 방법을 제공하는 Azure Stack Commerce 관리자 모듈의 미리 보기 릴리스입니다.

### <a name="compute"></a>컴퓨팅
컴퓨팅 할당량, 플랫폼 이미지, 관리 디스크 및 가상 머신 확장을 관리하는 기능을 제공하는 Azure Stack Compute 관리자 모듈의 미리 보기 릴리스입니다.

### <a name="fabric"></a>Fabric
관리자가 다음 작업을 위해 인프라 구성 요소를 보고 관리할 수 있게 해주는 Azure Stack Fabric 관리자 모듈의 미리 보기 릴리스입니다.
- 배율 단위 노드의 중지, 시작 및 종료
- FRU 관련 활동에 대한 배율 단위 노드의 배출 및 재개
- 배율 단위 노드의 복구
- 인프라 역할의 다시 시작
- 인프라 역할 인스턴스의 중지, 시작 및 종료
- 새 IP 풀 만들기


### <a name="gallery"></a>갤러리
Azure Stack Marketplace에서 갤러리 항목을 관리하는 기능을 제공하는 Azure Stack Gallery 관리자 모듈의 미리 보기 릴리스입니다.

### <a name="infrastructure-insights"></a>Infrastructure Insights
관리자가 다음을 수행할 수 있는 Infrastructure Insight 관리자 모듈의 미리 보기 릴리스입니다.
- Azure Stack 스탬프 리소스의 상태 보기
- 경고 보기 및 관리

### <a name="keyvault"></a>KeyVault
관리자가 KeyVault 할당량을 볼 수 있는 Azure Stack KeyVault 관리자 모듈의 미리 보기 릴리스입니다.

### <a name="network"></a>네트워크
다음을 수행할 수 있는 Network 관리자 모듈의 미리 보기 릴리스입니다.
- 네트워크 할당량 관리
- 공용 IP 주소, 가상 네트워크, 부하 분산 장치와 같은 할당된 네트워크 리소스 보기
- 관리자 개요를 표시하는 cmdlet을 제공

### <a name="storage"></a>스토리지
Azure Stack Storage 관리자 모듈의 미리 보기 릴리스입니다.  이 릴리스에서는 다음을 수행하기 위한 기능을 제공합니다.
- 스토리지 할당량 관리
- 삭제된 스토리지 리소스 가비지 수집
- 삭제된 스토리지 계정 복원
- 한 공유에서 다른 공유로 컨테이너 마이그레이션
- 개별 스토리지 구성 요소에 대한 정보 보기
- 사용량 및 성능 정보 보기

### <a name="subscription-admin"></a>구독 관리자
Azure Stack Subscription 관리자 모듈의 미리 보기 릴리스입니다.  이 모듈은 관리자가 다음을 수행하기 위한 기능을 제공합니다.
- 계획 및 제안 관리
- 사용량 및 성능 정보 보기
- RBAC 관리

### <a name="subscription"></a>Subscription
Azure Stack Subscription 모듈의 미리 보기 릴리스입니다.  이 모듈은 사용자가 다음을 수행하기 위한 기능을 제공합니다.
- 구독 생성, 삭제 및 업데이트

### <a name="update"></a>업데이트
Azure Stack Update 관리자 모듈의 미리 보기 릴리스입니다.  이 모듈에서 관리자는 다음을 수행할 수 있습니다.
- 사용 가능한 업데이트 나열 및 설치
- 중단된 업데이트 다시 시작
- 설치된 업데이트 보기
