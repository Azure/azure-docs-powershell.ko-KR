---
title: Azure Stack Admin PowerShell 개요 | Microsoft Docs
description: 설치 및 구성에 대한 설명을 포함한 Azure Stack Admin PowerShell 개요입니다.
author: bganapa
ms.author: bganapa
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 09/21/2018
ms.openlocfilehash: afa83a6258e57e961576b328e67fad634704dddf
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/05/2020
ms.locfileid: "63053361"
---
# <a name="azure-stack-module-150"></a>Azure Stack 모듈 1.5.0

## <a name="requirements"></a>요구 사항:
최소 지원 Azure Stack 버전은 1808입니다.

참고: 이전 버전을 사용하는 경우 1.4.0 버전을 설치하세요.

## <a name="known-issues"></a>알려진 문제:

- New-AzsOffer는 상태를 공개하여 제안을 만들 수 없습니다. 상태를 변경하려면 Set-AzsOffer cmdlet을 나중에 호출해야 합니다.
- 재배포하지 않고는 IP 풀을 제거할 수 없습니다.

## <a name="install"></a>설치
```
# Remove previous versions of AzureStack modules
Uninstall-Module -Name AzureStack -Force 
Uninstall-Module AzureRM.AzureStackAdmin -Force
Uninstall-Module AzureRM.AzureStackStorage -Force
Get-Module Azs.* -ListAvailable | Uninstall-Module -Force


# Install the AzureRM.Bootstrapper module. Select Yes when prompted to install NuGet
Install-Module -Name AzureRm.BootStrapper

# Install and import the API Version Profile required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2018-03-01-hybrid -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.5.0
```

## <a name="release-notes"></a>릴리스 정보
* 모든 Azure Stack Admin 모듈은 AzureRm.Profile 모듈에 대한 종속성 이상으로 업데이트됩니다.
* 모든 모듈의 중첩된 리소스 이름 처리에 대한 지원
* ErrorActionPreference를 Stop으로 재정의되는 모든 모듈에서 버그 수정
* Azs.Compute.Admin 모듈
    * 새 할당량 속성이 추가되어 관리 디스크를 지원
    * 디스크 마이그레이션 관련 cmdlet 또한 추가
    * 플랫폼 이미지 및 VM 확장 개체의 추가 속성
* Azs.Fabric.Admin 
    * 배율 단위 노드를 추가하는 새 cmdlet
* Azs.Backup.Admin
    * Set-AzsBackupShare는 이제 cmdlet Set-AzsBackupConfiguration에 대한 별칭입니다.
    * Get-AzsBackupLocation은 이제 cmdlet Get-AzsBackupConfiguration에 대한 별칭입니다.
    * Set-AzsBackupConfiguration, BackupShare 매개 변수는 이제 매개 변수 경로에 대한 별칭입니다.
* Azs.Subscriptions
    * Get-AzsDelegatedProviderOffer, OfferName 매개 변수는 이제 제안에 대한 별칭입니다.
* Azs.Subscriptions.Admin
    * Get-AzsDelegatedProviderOffer, OfferName 매개 변수는 이제 제안에 대한 별칭입니다.

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
