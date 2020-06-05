---
title: Azure PowerShell 변경 로그
description: Azure PowerShell에 대한 최신 릴리스의 변경 내용입니다.
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 2/20/2018
ms.openlocfilehash: cf8d1fc76feb07e075339255de63e09f59187dc6
ms.sourcegitcommit: 9f5c7d231b069ad501729bf015a829f3fe89bc6a
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/28/2020
ms.locfileid: "84122063"
---
# <a name="azure-powershell-release-notes"></a>Azure PowerShell 릴리스 정보

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

Azure PowerShell에 대한 릴리스의 변경 내용 목록입니다.

---

## <a name="azure-powershell-570"></a>Azure PowerShell 5.7.0

Azure PowerShell 5.7.0 설치 관리자: [링크](https://github.com/Azure/azure-powershell/releases/download/v5.7.0-April2018/azure-powershell.5.7.0.msi)

ARM Cmdlet용 갤러리 모듈: [링크](https://www.powershellgallery.com/packages/AzureRM/5.7.0)

PowerShell 갤러리에서 `AzureRM`을 설치하려면 다음 명령을 실행합니다.

```powershell-interactive
Install-Module -Name AzureRM -Repository PSGallery -Force
```

이전 버전의 `AzureRM`에서 업데이트하려면 다음 명령을 실행합니다.

```powershell-interactive
Update-Module -Name AzureRM
```

### <a name="changes-since-last-release"></a>마지막 릴리스 이후 변경 내용

#### <a name="general"></a>일반
* 최신 버전의 Azure ClientRuntime으로 업데이트됨

#### <a name="azurestorage"></a>Azure.Storage
* FIPS 정책을 사용하는 컴퓨터에서 Blob 업로드 및 파일 업로드 cmdlet이 실패하는 문제를 해결합니다.
    - Set-AzureStorageBlobContent
    - Set-AzureStorageFileContent

#### <a name="azurermbilling"></a>AzureRM.Billing
* 새로운 Cmdlet Get-AzureRmEnrollmentAccount
  - 등록 계정을 검색하는 cmdlet

#### <a name="azurermcognitiveservices"></a>AzureRM.CognitiveServices
* Cognitive Services Management SDK 버전 4.0.0과 통합됩니다.
* Get-AzureRmCognitiveServicesAccountUsage 작업을 추가하세요.

#### <a name="azurermcompute"></a>AzureRM.Compute
* `Get-AzureRmVmssDiskEncryptionStatus`는 데이터 디스크 수준에서 암호화 상태를 지원합니다.
* `Get-AzureRmVmssVmDiskEncryptionStatus`는 데이터 디스크 수준에서 암호화 상태를 지원합니다.
* 영역 복원력에 대한 업데이트
* 'New-AzureRmVm' 및 'New-AzureRmVmss'(간단한 매개 변수 집합)가 가용성 영역을 지원합니다.

#### <a name="azurermcontainerregistry"></a>AzureRM.ContainerRegistry
* Commands.Resources.Rest 및 ARM/Storage SDK에 대한 의존성을 분리합니다.

#### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* 디버그 기능 추가
* ADLS 데이터플레인 SDK 버전을 1.1.2로 업데이트
* Export-AzureRmDataLakeStoreItem - PerFileThreadCount, ConcurrentFileCount 매개 변수가 사용되지 않으며 Concurrency 매개 변수가 도입되었습니다.
* Import-AzureRMDataLakeStoreItem - PerFileThreadCount, ConcurrentFileCount 매개 변수가 사용되지 않으며 Concurrency 매개 변수가 도입되었습니다.
* Get-AzureRMDataLakeStoreItemContent - 4MB를 초과하는 콘텐츠에 대한 말단 동작이 수정되었습니다.
* Set-AzureRMDataLakeStoreItemExpiry - 상대 만료 시간을 설정하는 새로운 매개 변수 집합 SetRelativeExpiry가 도입되었습니다.
* Remove-AzureRmDataLakeStoreItem - Clean 매개 변수가 사용되지 않습니다.

#### <a name="azurermeventhub"></a>AzureRM.EventHub
* New-AzureRmEventHubGeoDRConfiguration의 AlternameName이 수정되었습니다.

#### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* 파이핑 시나리오를 포함하도록 cmdlet이 업데이트되었습니다.
* 향후 호환성이 손상되는 변경 릴리스에 대한 사용 중단 메시지 추가

#### <a name="azurermnetwork"></a>AzureRM.Network
* Network cmdlet 관련 오류 메시지 수정

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* customproperties를 지원하기 위해 Rules의 CorrelationFilter에 'properties'가 추가되었습니다.
* New-AzureRmServiceBusGeoDRConfiguration 도움말이 업데이트되고 Rules cmdlet 출력이 수정되었습니다.
* New-AzureRmServiceBusQueue 및 New-AzureRmServiceBusSubscription cmdlet의 auto-forward 속성이 수정되었습니다.

#### <a name="azurermsql"></a>AzureRM.Sql
* 탄력적 풀에서 비동기 작업의 취소를 지원하기 위해 새로운 cmdlet 'Stop-AzureRmSqlElasticPoolActivity' 추가
* 자세한 정보를 반영하도록 Get-AzureRmSqlDatabaseActivity 및 Get-AzureRmSqlElasticPoolActivity cmdlet에 대한 응답 업데이트

마지막 릴리스 이후 변경 내용: https://github.com/Azure/azure-powershell/compare/v5.6.0-March2018...v5.7.0-April2018

## <a name="560---march-2018"></a>5.6.0 - 2018년 3월

#### <a name="general"></a>일반
* CloudShell의 기본 리소스 그룹 문제 수정
* 모듈 가져오는 중에 잘못된 시작 스크립트가 실행되는 문제 수정

#### <a name="azurermprofile"></a>AzureRM.Profile
* 지원되지 않는 시나리오에서 MSI 인증 사용
* 사용자 정의 관리 서비스 ID 지원 추가

#### <a name="azurermanalysisservices"></a>AzureRM.AnalysisServices
* 빌드 시 스크립트 정리 문제 수정됨

#### <a name="azurermcdn"></a>AzureRM.Cdn
* 빌드 시 스크립트 정리 문제 수정됨

#### <a name="azurermcompute"></a>AzureRM.Compute
* 'New-AzureRmVM' 및 'New-AzureRmVMSS'가 데이터 디스크를 지원합니다.
* 'New-AzureRmVM' 및 'New-AzureRmVMSS'가 이름별 또는 ID별로 사용자 지정 이미지를 지원합니다.
* 로그 분석 기능
    - 'Export-AzureRmLogAnalyticRequestRateByInterval' cmdlet 추가됨
    - 'Export-AzureRmLogAnalyticThrottledRequests' cmdlet 추가됨

#### <a name="azurermcontainerinstance"></a>AzureRM.ContainerInstance
* 컨테이너 레지스트리 및 Azure 파일 볼륨 마운트에 대한 매개 변수 세트 문제 수정

#### <a name="azurermdatafactoryv2"></a>AzureRM.DataFactoryV2
* ADF .Net SDK를 다음과 같은 변경 사항이 포함된 버전 0.6.0-preview로 업데이트했습니다.
    - 새로운 AzureDatabricks LinkedService 및 DatabricksNotebook Activity 추가됨
    - HDInsightOnDemand LinkedService의 headNodeSize 및 dataNodeSize 속성 추가됨
    - SalesforceMarketingCloud에 대한 LinkedService, Dataset, CopySource 추가됨
    - 모든 작업에서 SecureOutput에 대한 지원 추가됨
    - ForEach 작업에서 실행될 동시 작업 수를 제어하는 새로운 BatchCount 속성 추가됨
    - 새 필터 작업 추가됨
    - 연결된 서비스 매개 변수 지원 추가됨

#### <a name="azurermdns"></a>AzureRM.Dns
* 프라이빗 DNS 영역 지원(공개 미리 보기)
    - 연결된 가상 네트워크에만 표시되는 DNS 영역을 만들 수있는 기능을 추가합니다.

#### <a name="azurermnetwork"></a>AzureRM.Network
* DNS cmdlet과의 호환성을 위해 모델 형식 업데이트.

#### <a name="azurermrecoveryservicessiterecovery"></a>AzureRM.RecoveryServices.SiteRecovery
* ASR Azure-Azure Site Recovery에 대한 변경 사항(cmdlet은 현재 Enterprise-Enterprise, Enterprise-Azure, HyperV-Azure, VMware - Azure에 대한 작업을 지원)
    - New-AzureRmRecoveryServicesAsrProtectionContainer
    - New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig
    - Remove-AzureRmRecoveryServicesAsrProtectionContainer
    - Update-AzureRmRecoveryServicesAsrProtectionDirection

#### <a name="azurermstorage"></a>AzureRM.Storage
* new 및 set Storage Account cmdlet에서 다음 매개 변수는 사용되지 않습니다. Encryption at Rest는 기본적으로 활성화되며 비활성화할 수 없으므로 EnableEncryptionService 및 DisableEncryptionService
    - New-AzureRmStorageAccount
    - Set-AzureRmStorageAccount

#### <a name="azurermwebsites"></a>AzureRM.Websites
* Remove-AzureRmWebAppSlot에 대한 도움말 수정됨

## <a name="550---march-2018"></a>5.5.0 - 2018년 3월
#### <a name="azurermprofile"></a>AzureRM.Profile
* 별칭 가져오기 문제 해결
* 6\.0.8 버전과 병렬로 Newtonsoft.Json 버전 10.0.3 로드

#### <a name="azurestorage"></a>Azure.Storage
* 일시 삭제 기능 지원
    - Enable-AzureStorageDeleteRetentionPolicy
    - Enable-AzureStorageDeleteRetentionPolicy
    - Get-AzureStorageBlob

#### <a name="azurermanalysisservices"></a>AzureRM.AnalysisServices
* 별칭 가져오기 문제 해결
* 2017-08-01 API 버전 지원 및 방화벽과 쿼리 스케일 아웃 기능 지원 추가

#### <a name="azurermautomation"></a>AzureRM.Automation
* 별칭 가져오기 문제 해결

#### <a name="azurermcdn"></a>AzureRM.Cdn
* 별칭 가져오기 문제 해결

#### <a name="azurermcognitiveservices"></a>AzureRM.CognitiveServices
* notice.txt 및 알림 메시지 업데이트

#### <a name="azurermcompute"></a>AzureRM.Compute
* 'New-AzureRmVMSS'가 자세한 정보 표시 모드로 연결 문자열 인쇄
* 'New-AzureRmVmss'가 공용 IP 주소, 부하 분산 규칙, 인바운드 NAT 규칙 지원
* WriteAccelerator 기능
    - 새 스위치 매개 변수인 WriteAccelerator가 추가된 cmdlet은 다음과 같습니다. Set-AzureRmVMOSDisk Set-AzureRmVMDataDisk Add-AzureRmVMDataDisk Add-AzureRmVmssDataDisk
    - 새 스위치 매개 변수인 OsDiskWriteAccelerator가 추가된 cmdlet은 다음과 같습니다.     Set-AzureRmVmssStorageProfile.
    - 새 부울 매개 변수인 OsDiskWriteAccelerator가 추가된 cmdlet은 다음과 같습니다.     Update-AzureRmVM     Update-AzureRmVmss

#### <a name="azurermdatafactories"></a>AzureRM.DataFactories
* 일부 암호화 작업에 대해 의미 없는 오류를 일으키는 자격 증명 암호화 문제 해결
* 데이터 팩터리 전체에서 공유 가능하도록 통합 런타임 활성화

#### <a name="azurermdatafactoryv2"></a>AzureRM.DataFactoryV2
* "Set-AzureRmDataFactoryV2IntegrationRuntime" cmd용 매개 변수 "SetupScriptContainerSasUri" 및 "Edition"을 추가하여 사용자 지정 설치 및 버전 선택 기능 활성화
* 일부 암호화 작업에 대해 의미 없는 오류를 일으키는 자격 증명 암호화 문제 해결
* 데이터 팩터리 전체에서 공유 가능하도록 통합 런타임 활성화

#### <a name="azurermhdinsight"></a>AzureRM.HDInsight
* 별칭 가져오기 문제 해결

#### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* Set-AzureRmKeyVaultAccessPolicy용 예제 수정

#### <a name="azurermnetwork"></a>AzureRM.Network
* 별칭 가져오기 문제 해결

#### <a name="azurermoperationalinsights"></a>AzureRM.OperationalInsights
* 별칭 가져오기 문제 해결

#### <a name="azurermrecoveryservices"></a>AzureRM.RecoveryServices
* 별칭 가져오기 문제 해결

#### <a name="azurermrecoveryservicessiterecovery"></a>AzureRM.RecoveryServices.SiteRecovery
* 별칭 가져오기 문제 해결

#### <a name="azurermresources"></a>AzureRM.Resources
* 별칭 가져오기 문제 해결

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* 큐에 EnableBatchedOperations 속성 추가됨
* 구독에 DeadLetteringOnFilterEvaluationExceptions 속성 추가됨

#### <a name="azurermservicefabric"></a>AzureRM.ServiceFabric
* Service Fabric cmdlet 새로 고침
  - ARM 템플릿 업데이트됨
  - 실패한 작업이 더 이상 롤백되지 않음
  - Add-AzureRmServiceFabricNodeType
    - 관리 디스크에 대한 VM 기본값
    - 기존 VMSS 서브넷 사용됨
    - 모든 작업은 idempotent임
  - Remove-AzureRmServiceFabricNodeType 정리가 부분적으로 VMSS 및/또는 클러스터 노드 유형 생성
  - 복합 속성 유형에 대한 PSCluster 개체의 출력 수정

#### <a name="azurermsql"></a>AzureRM.Sql
* 별칭 가져오기 문제 해결
* Get-AzureRmSqlServer, New-AzureRmSqlServer 및 Remove-AzureRmSqlServer 응답이 FullyQualifiedDomainName 속성에 포함됨.

#### <a name="azurermwebsites"></a>AzureRM.Websites
* 별칭 가져오기 문제 해결
* New-AzureRMWebApp - 로컬 Git 리포지토리 지원과 함께 간소화된 WebApp 생성을 위한 매개 변수 집합이 추가되었습니다.

## <a name="540---february-2018"></a>5.4.0 - 2018년 2월
#### <a name="azurermautomation"></a>AzureRM.Automation
* New-AzureRmAutomationModule의 별칭이 Import-AzureRmAutomationModule에 추가됨

#### <a name="azurermcompute"></a>AzureRM.Compute
* 일부 Get cmdlet에 대한 ErrorAction 문제 해결

#### <a name="azurermcontainerinstance"></a>AzureRM.ContainerInstance
* Azure Container Instance SDK 2018-02-01 적용
    - DNS 이름 레이블 지원

#### <a name="azurermdevtestlabs"></a>AzureRM.DevTestLabs
* 이전에 작동하지 않았던 모든 GET cmdlet이 수정되었습니다.

#### <a name="azurermeventhub"></a>AzureRM.EventHub
* Get-AzureRmEventHubGeoDRConfiguration 도움말의 버그 수정

#### <a name="azurermnetwork"></a>AzureRM.Network
* 새 연결 모니터를 만드는 cmdlet이 추가됨
    - New-AzureRmNetworkWatcherConnectionMonitor
* 연결 모니터를 업데이트하는 cmdlet이 추가됨
    - Set-AzureRmNetworkWatcherConnectionMonitor
* 연결 모니터 또는 연결 모니터 목록을 가져오는 cmdlet이 추가됨
    - Get-AzureRmNetworkWatcherConnectionMonitor
* 연결 모니터를 쿼리하는 cmdlet이 추가됨
    - Get-AzureRmNetworkWatcherConnectionMonitorReport
* 연결 모니터를 시작하는 cmdlet이 추가됨
    - Start-AzureRmNetworkWatcherConnectionMonitor
* 연결 모니터를 중지하는 cmdlet이 추가됨
    - Stop-AzureRmNetworkWatcherConnectionMonitor
* 연결 모니터를 제거하는 cmdlet이 추가됨
    - Remove-AzureRmNetworkWatcherConnectionMonitor
* 사용되지 않는 예제를 제거하기 위해 Set-AzureRmApplicationGatewayBackendAddressPool 설명서가 업데이트됨
* Application Gateway에 EnableHttp2 플래그가 추가됨
    - 업데이트된 New-AzureRmApplicationGateway: 선택적 매개 변수 추가됨 -EnableHttp2
* PublicIpAddress에 IpTags 추가
    - 업데이트된 New-AzureRmPublicIpAddress: IpTags 추가됨
    - Iptag를 추가하는 New-AzureRmPublicIpTag
* RouteTable 및 effectiveRoute에 DisableBgpRoutePropagation 속성을 추가합니다.

#### <a name="azurermresources"></a>AzureRM.Resources
* Register-AzureRmProviderFeature: 문서에 누락된 예제가 추가됨
* Register-AzureRmResourceProvider: 문서에 누락된 예제가 추가됨

#### <a name="azurermstorage"></a>AzureRM.Storage
* new 및 set Storage Account cmdlet에서 다음 매개 변수는 사용되지 않습니다. Encryption at Rest는 기본적으로 활성화되며 비활성화할 수 없으므로 EnableEncryptionService 및 DisableEncryptionService
    - New-AzureRmStorageAccount
    - Set-AzureRmStorageAccount


## <a name="530---february-2018"></a>5.3.0 - 2018년 2월
### <a name="azurermprofile"></a>AzureRM.Profile
* PowerShell 3 및 4에 대한 사용 중단 경고가 추가되었습니다.
* `Add-AzureRmAccount`는 `Connect-AzureRmAccount`로 이름이 변경되었습니다. 이전 cmdlet 이름에 대한 별칭이 추가되었고 다른 별칭(`Login-AzAccount` 및 `Login-AzureRmAccount`)이 새 cmdlet 이름으로 리디렉션되었습니다.
* `Remove-AzureRmAccount`는 `Disconnect-AzureRmAccount`로 이름이 변경되었습니다. 이전 cmdlet 이름에 대한 별칭이 추가되었고 다른 별칭(`Logout-AzAccount` 및 `Logout-AzureRmAccount`)이 새 cmdlet 이름으로 리디렉션되었습니다.
* `Login-AzureRmAccount` 대신 `Connect-AzureRmAccount`를 사용하도록 리소스 문자열이 수정되었습니다.
* `Add-AzureRmEnvironment` 및 `Set-AzureRmEnvironment`
  - OperationalInsights 데이터 평면 RP와 함께 사용할 매개 변수로 `-AzureOperationalInsightsEndpoint` 및 `-AzureOperationalInsightsEndpointResourceId`가 추가되었습니다.

### <a name="azurermanalysisservices"></a>AzureRM.AnalysisServices
* `Connect-AzureRmAccount`를 사용하도록 `Login-AzureRmAccount`의 사용법이 수정되었습니다.

### <a name="azurermcompute"></a>AzureRM.Compute
* 간소화된 매개 변수 집합 `New-AzureRmVM`에 `-AvailabilitySetName` 매개 변수가 추가되었습니다.
* `Connect-AzureRmAccount`를 사용하도록 `Login-AzureRmAccount`의 사용법이 수정되었습니다.
* VM 및 VM 확장 집합에 대한 사용자 할당 ID가 지원됩니다.
    - `New-AzureRmVMConfig`, `New-AzureRmVmssConfig`, `Update-AzureRmVM`, `Update-AzureRmVmss`에 `-IdentityType` 및 `-IdentityId` 매개 변수가 추가되었습니다.
* `-EnableIPForwarding` 매개 변수가 `Add-AzureRmVmssNetworkInterfaceConfig`에 추가됨
* `-Priority` 매개 변수가 `New-AzureRmVmssConfig`에 추가됨

### <a name="azurermdatalakeanalytics"></a>AzureRM.DataLakeAnalytics
* `Connect-AzureRmAccount`를 사용하도록 `Login-AzureRmAccount`의 사용법이 수정되었습니다.

### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* `Connect-AzureRmAccount`를 사용하도록 `Login-AzureRmAccount`의 사용법이 수정되었습니다.
* `Login-AzureRmAccount`를 사용하여 로그인하지 않고 이 cmdlet을 실행하는 경우 오류 메시지 `Test-AzureRmDataLakeStoreAccount`가 수정되었습니다.

### <a name="azurermeventgrid"></a>AzureRM.EventGrid
* 2018-01-01 API 버전을 사용하도록 업데이트되었습니다.

### <a name="azurermeventhub"></a>AzureRM.EventHub

* 지역 재해 복구 작업에 대한 아래의 새 명령이 추가되었습니다.
  - 새 별칭(재해 복구 구성)을 만드는 중입니다.
    - `New-AzureRmEventHubGeoDRConfiguration`
  - 새 별칭(재해 복구 구성)을 검색합니다.
    - `Get-AzureRmEventHubGeoDRConfiguration`
  - 재해 복구를 사용하지 않고 기본 네임스페이스에서 보조 네임스페이스로의 변경 사항 복제 중지
    - `Set-AzureRmEventHubGeoDRConfigurationBreakPair`
  - 재해 복구 장애 조치(failover)를 호출하고 별칭이 보조 네임스페이스를 가리키도록 다시 구성
    - `Set-AzureRmEventHubGeoDRConfigurationFailOver`
  - 별칭 삭제(재해 복구 구성)
    - `Remove-AzureRmEventHubGeoDRConfiguration`
* 네임스페이스 이름 및 GeoDr 구성 이름 - 별칭 가용성을 검사하는 아래의 새 명령이 추가되었습니다.
  - 네임스페이스 이름의 가용성 이름 또는 별칭(재해 복구 구성) 이름을 확인합니다.
    - `Test-AzureRmEventHubName`

### <a name="azurerminsights"></a>AzureRM.Insights
* `Connect-AzureRmAccount`를 사용하도록 `Login-AzureRmAccount`의 사용법이 수정되었습니다.

### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* `Connect-AzureRmAccount`를 사용하도록 `Login-AzureRmAccount`의 사용법이 수정되었습니다.

### <a name="azurermnetwork"></a>AzureRM.Network
* '리소스를 덮어쓰시겠습니까?'라는 덮어쓰기 메시지가 해결되었습니다.

#### <a name="azurermoperationalinsights"></a>AzureRM.OperationalInsights
* `Invoke-AzureRmOperationalInsightsQuery`를 통해 V2 API 쿼리에 대한 지원이 추가되었습니다. 새로운 API에 대한 보다 자세한 내용은 [https://dev.loganalytics.io/](https://dev.loganalytics.io/)을 참조하세요.

### <a name="azurermresources"></a>AzureRM.Resources
* `Get-AzureRmADServicePrincipal`: SPN 매개 변수 설정과 중복되는 기본 빈 매개 변수 설정에서 `-ServicePrincipalName`이 제거되었습니다.

### <a name="azurermservicebus"></a>AzureRM.ServiceBus

* `Remove-AzureRmServiceBusRule` 및 `Get-AzureRmServiceBusKey`에 대한 기능 수정이 추가되었습니다.
* 지역 재해 복구 작업에 대한 아래의 새 commandlet이 추가되었습니다.
  - 새 별칭(재해 복구 구성)을 만드는 중입니다.
    - `New-AzureRmServiceBusDRConfigurations`
  - 새 별칭(재해 복구 구성)을 검색합니다.
    - `Get-AzureRmServiceBusDRConfigurations`
  - 재해 복구를 사용하지 않고 기본 네임스페이스에서 보조 네임스페이스로의 변경 사항 복제 중지
    - `Set-AzureRmServiceBusDRConfigurationsBreakPairing`
  - 재해 복구 장애 조치(failover)를 호출하고 별칭이 보조 네임스페이스를 가리키도록 다시 구성
    - `Set-AzureRmServiceBusDRConfigurationsFailOver`
  - 별칭 삭제(재해 복구 구성)
    - `Remove-AzureRmServiceBusDRConfigurations`
* 지역 재해 복구 - 별칭 이름 확인 가용성 작업을 지원하도록 `Test-AzureRmServiceBusName` commandlet이 업데이트되었습니다.
  - 네임스페이스 이름의 가용성 이름 또는 별칭(재해 복구 구성) 이름을 확인합니다.
    - `Test-AzureRmServiceBusName`

### <a name="azurermusageaggregates"></a>AzureRM.UsageAggregates
* `Connect-AzureRmAccount`를 사용하도록 `Login-AzureRmAccount`의 사용법이 수정되었습니다.

## <a name="520---january-2018"></a>5.2.0 - 2018년 1월
#### <a name="azurermprofile"></a>AzureRM.Profile
* 현재 구독에서 리소스 그룹을 통해 탭 완성 기능을 허용하는 -ResourceGroup 매개 변수에 ResourceGroup Completer를 추가했습니다.
* Add-AzureRmAccount
  * 현재 VM/서비스에 있는 관리 서비스 ID의 자격 증명을 사용하여 인증하기 위해 -MSI 로그인을 추가했습니다.
  * 사용자 제공 액세스 토큰을 사용하여 로그인할 때 KeyVault 인증을 수정했습니다.

#### <a name="azurestorage"></a>Azure.Storage
* Storage 서비스 속성을 가져오고 설정하는 cmdlet을 추가했습니다.
    - Get-AzureStorageServiceProperty
    - Update-AzureStorageServiceProperty

#### <a name="azurermanalysisservices"></a>AzureRM.AnalysisServices
* 현재 구독에서 리소스 그룹을 통해 탭 완성 기능을 허용하는 -ResourceGroup 매개 변수에 ResourceGroup Completer를 추가했습니다.

#### <a name="azurermapimanagement"></a>AzureRM.ApiManagement
* 유효한 위치를 통해 탭 완성 기능을 허용하는 -Location 매개 변수에 Location Completer를 추가했습니다.
* 현재 구독에서 리소스 그룹을 통해 탭 완성 기능을 허용하는 -ResourceGroup 매개 변수에 ResourceGroup Completer를 추가했습니다.
* New-AzureRmApiManagementProperty, Set-AzureRmApiManagementProperty 및 New-AzureRmApiManagement에 -Tag를 사용하는 -Tags를 사용하지 않습니다.

#### <a name="azurermapplicationinsights"></a>AzureRM.ApplicationInsights
* 유효한 위치를 통해 탭 완성 기능을 허용하는 -Location 매개 변수에 Location Completer를 추가했습니다.
* 현재 구독에서 리소스 그룹을 통해 탭 완성 기능을 허용하는 -ResourceGroup 매개 변수에 ResourceGroup Completer를 추가했습니다.

#### <a name="azurermautomation"></a>AzureRM.Automation
* 유효한 위치를 통해 탭 완성 기능을 허용하는 -Location 매개 변수에 Location Completer를 추가했습니다.
* 현재 구독에서 리소스 그룹을 통해 탭 완성 기능을 허용하는 -ResourceGroup 매개 변수에 ResourceGroup Completer를 추가했습니다.
* Set-AzureRmAutomationRunbook에 -Tag를 사용하는 -Tags를 사용하지 않습니다.

#### <a name="azurermbackup"></a>AzureRM.Backup
* 유효한 위치를 통해 탭 완성 기능을 허용하는 -Location 매개 변수에 Location Completer를 추가했습니다.
* 현재 구독에서 리소스 그룹을 통해 탭 완성 기능을 허용하는 -ResourceGroup 매개 변수에 ResourceGroup Completer를 추가했습니다.

#### <a name="azurermbatch"></a>AzureRM.Backup
* 유효한 위치를 통해 탭 완성 기능을 허용하는 -Location 매개 변수에 Location Completer를 추가했습니다.
* 현재 구독에서 리소스 그룹을 통해 탭 완성 기능을 허용하는 -ResourceGroup 매개 변수에 ResourceGroup Completer를 추가했습니다.

#### <a name="azurermcdn"></a>AzureRM.Cdn
* 유효한 위치를 통해 탭 완성 기능을 허용하는 -Location 매개 변수에 Location Completer를 추가했습니다.
* 현재 구독에서 리소스 그룹을 통해 탭 완성 기능을 허용하는 -ResourceGroup 매개 변수에 ResourceGroup Completer를 추가했습니다.
* New-AzureRmCdnEndpoint 및 New-AzureRmCdnProfile에 -Tag를 사용하는 -Tags를 사용하지 않습니다.

#### <a name="azurermcognitiveservices"></a>AzureRM.CognitiveServices
* Cognitive Services Management SDK 버전 3.0.0과 통합합니다.

#### <a name="azurermcompute"></a>AzureRM.Compute
* New-AzureRmVmss에 간소화된 매개 변수 집합이 추가되었습니다. 따라서 스마트 기본값을 사용하여 Virtual Machine Scale Set과 필요한 모든 리소스가 만들어집니다.
* 유효한 위치를 통해 탭 완성 기능을 허용하는 -Location 매개 변수에 Location Completer를 추가했습니다.
* 현재 구독에서 리소스 그룹을 통해 탭 완성 기능을 허용하는 -ResourceGroup 매개 변수에 ResourceGroup Completer를 추가했습니다.
* New-AzureRmVm 및 Update-AzureRmVm에 -Tag를 사용하는 -Tags를 사용하지 않습니다.
* 영역이 제한에 포함될 때 Get-AzureRmComputeResourceSku cmdlet을 수정했습니다.
* Azure Monitor 동기화 지원을 위해 진단 에이전트 구성 스키마를 업데이트했습니다.

#### <a name="azurermcontainerinstance"></a>AzureRM.ContainerInstance
* 유효한 위치를 통해 탭 완성 기능을 허용하는 -Location 매개 변수에 Location Completer를 추가했습니다.
* 현재 구독에서 리소스 그룹을 통해 탭 완성 기능을 허용하는 -ResourceGroup 매개 변수에 ResourceGroup Completer를 추가했습니다.

#### <a name="azurermcontainerregistry"></a>AzureRM.ContainerRegistry
* 유효한 위치를 통해 탭 완성 기능을 허용하는 -Location 매개 변수에 Location Completer를 추가했습니다.
* 현재 구독에서 리소스 그룹을 통해 탭 완성 기능을 허용하는 -ResourceGroup 매개 변수에 ResourceGroup Completer를 추가했습니다.

#### <a name="azurermdatafactories"></a>AzureRM.DataFactories
* 모든 데이터 저장소 연결 서비스에 대해 Azure Key Vault 지원을 활성화했습니다.
* Azure SSIS 통합 런타임에 라이선스 형식 속성을 추가했습니다.
* 유효한 위치를 통해 탭 완성 기능을 허용하는 -Location 매개 변수에 Location Completer를 추가했습니다.
* 현재 구독에서 리소스 그룹을 통해 탭 완성 기능을 허용하는 -ResourceGroup 매개 변수에 ResourceGroup Completer를 추가했습니다.
* New-AzureRmDataFactory에 -Tag를 사용하는 -Tags를 사용하지 않습니다.

#### <a name="azurermdatafactoryv2"></a>AzureRM.DataFactoryV2
* 모든 데이터 저장소 연결 서비스에 대해 Azure Key Vault 지원을 활성화했습니다.
* Azure SSIS 통합 런타임에 라이선스 형식 속성을 추가했습니다.
* 유효한 위치를 통해 탭 완성 기능을 허용하는 -Location 매개 변수에 Location Completer를 추가했습니다.
* 현재 구독에서 리소스 그룹을 통해 탭 완성 기능을 허용하는 -ResourceGroup 매개 변수에 ResourceGroup Completer를 추가했습니다.
* AHUB 기능을 사용하도록 "Set-AzureRmDataFactoryV2IntegrationRuntime" cmd에 "LicenseType" 매개 변수를 추가했습니다.

#### <a name="azurermdatalakeanalytics"></a>AzureRM.DataLakeAnalytics
* 유효한 위치를 통해 탭 완성 기능을 허용하는 -Location 매개 변수에 Location Completer를 추가했습니다.
* 현재 구독에서 리소스 그룹을 통해 탭 완성 기능을 허용하는 -ResourceGroup 매개 변수에 ResourceGroup Completer를 추가했습니다.
* New-AzureRmDataLakeAnalyticsAccount 및 Set-AzureRmDataLakeAnalyticsAccount에 -Tag를 사용하는 -Tags를 사용하지 않습니다.

#### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* 유효한 위치를 통해 탭 완성 기능을 허용하는 -Location 매개 변수에 Location Completer를 추가했습니다.
* 현재 구독에서 리소스 그룹을 통해 탭 완성 기능을 허용하는 -ResourceGroup 매개 변수에 ResourceGroup Completer를 추가했습니다.
* New-AzureRmDataLakeStoreAccount 및 Set-AzureRmDataLakeStoreAccount에 -Tag를 사용하는 -Tags를 사용하지 않습니다.

#### <a name="azurermdevtestlabs"></a>AzureRM.DevTestLabs
* 현재 구독에서 리소스 그룹을 통해 탭 완성 기능을 허용하는 -ResourceGroup 매개 변수에 ResourceGroup Completer를 추가했습니다.

#### <a name="azurermdns"></a>AzureRM.Dns
* 현재 구독에서 리소스 그룹을 통해 탭 완성 기능을 허용하는 -ResourceGroup 매개 변수에 ResourceGroup Completer를 추가했습니다.

#### <a name="azurermeventgrid"></a>AzureRM.EventGrid
* 다음과 같은 새 cmdlet을 추가했습니다.
  - Update-AzureRmEventGridSubscription
    - Event Grid 이벤트 구독의 속성을 업데이트합니다.
* 유효한 위치를 통해 탭 완성 기능을 허용하는 -Location 매개 변수에 Location Completer를 추가했습니다.
* 현재 구독에서 리소스 그룹을 통해 탭 완성 기능을 허용하는 -ResourceGroup 매개 변수에 ResourceGroup Completer를 추가했습니다.

#### <a name="azurermeventhub"></a>AzureRM.EventHub
* 유효한 위치를 통해 탭 완성 기능을 허용하는 -Location 매개 변수에 Location Completer를 추가했습니다.
* 현재 구독에서 리소스 그룹을 통해 탭 완성 기능을 허용하는 -ResourceGroup 매개 변수에 ResourceGroup Completer를 추가했습니다.

#### <a name="azurermhdinsight"></a>AzureRM.HDInsight
* 유효한 위치를 통해 탭 완성 기능을 허용하는 -Location 매개 변수에 Location Completer를 추가했습니다.
* 현재 구독에서 리소스 그룹을 통해 탭 완성 기능을 허용하는 -ResourceGroup 매개 변수에 ResourceGroup Completer를 추가했습니다.

#### <a name="azurerminsights"></a>AzureRM.Insights
* 유효한 위치를 통해 탭 완성 기능을 허용하는 -Location 매개 변수에 Location Completer를 추가했습니다.
* 현재 구독에서 리소스 그룹을 통해 탭 완성 기능을 허용하는 -ResourceGroup 매개 변수에 ResourceGroup Completer를 추가했습니다.

#### <a name="azurermiothub"></a>AzureRM.IotHub
* IoTHub cmdlet에 인증서 지원을 추가합니다.
* 유효한 위치를 통해 탭 완성 기능을 허용하는 -Location 매개 변수에 Location Completer를 추가했습니다.
* 현재 구독에서 리소스 그룹을 통해 탭 완성 기능을 허용하는 -ResourceGroup 매개 변수에 ResourceGroup Completer를 추가했습니다.

#### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* 유효한 위치를 통해 탭 완성 기능을 허용하는 -Location 매개 변수에 Location Completer를 추가했습니다.
* 현재 구독에서 리소스 그룹을 통해 탭 완성 기능을 허용하는 -ResourceGroup 매개 변수에 ResourceGroup Completer를 추가했습니다.
* 장기 실행 KeyVault cmdlet에 대한 -AsJob 지원이 추가되었습니다. 선택된 cmdlet을 백그라운드에서 실행하고 작업을 반환하여 진행률을 추적 및 제어할 수 있습니다.
  * 영향을 받는 cmdlet은 다음과 같습니다. Remove-AzureRmKeyVault
* AAD 필터가 UPN 설정이 아닌 SPN을 제공된 UPN으로 설정하는 Set-AzureRmKeyVaultAccessPolicy에서 버그를 수정했습니다.
  - 보다 자세한 내용은 다음 문제를 참조하세요. https://github.com/Azure/azure-powershell/issues/5201

#### <a name="azurermlogicapp"></a>AzureRM.LogicApp
* 유효한 위치를 통해 탭 완성 기능을 허용하는 -Location 매개 변수에 Location Completer를 추가했습니다.
* 현재 구독에서 리소스 그룹을 통해 탭 완성 기능을 허용하는 -ResourceGroup 매개 변수에 ResourceGroup Completer를 추가했습니다.

#### <a name="azurermmachinelearning"></a>AzureRM.MachineLearning
* 유효한 위치를 통해 탭 완성 기능을 허용하는 -Location 매개 변수에 Location Completer를 추가했습니다.
* 현재 구독에서 리소스 그룹을 통해 탭 완성 기능을 허용하는 -ResourceGroup 매개 변수에 ResourceGroup Completer를 추가했습니다.
* Update-AzureRmMlCommitmentPlan에 -Tag를 사용하는 -Tags를 사용하지 않습니다.

#### <a name="azurermmachinelearningcompute"></a>AzureRM.MachineLearningCompute
* Remove-AzureRmMlOpCluster cmdlet에 IncludeAllResources 매개 변수를 추가합니다.
  - 이 스위치 매개 변수를 사용하면 원래 클러스터를 사용하여 만든 모든 리소스를 제거합니다.
* 유효한 위치를 통해 탭 완성 기능을 허용하는 -Location 매개 변수에 Location Completer를 추가했습니다.
* 현재 구독에서 리소스 그룹을 통해 탭 완성 기능을 허용하는 -ResourceGroup 매개 변수에 ResourceGroup Completer를 추가했습니다.

#### <a name="azurermmedia"></a>AzureRM.Media
* 유효한 위치를 통해 탭 완성 기능을 허용하는 -Location 매개 변수에 Location Completer를 추가했습니다.
* 현재 구독에서 리소스 그룹을 통해 탭 완성 기능을 허용하는 -ResourceGroup 매개 변수에 ResourceGroup Completer를 추가했습니다.
* Set-AzureRmMediaService 및 New-AzureRmMediaService에 -Tag를 사용하는 -Tags를 사용하지 않습니다.

#### <a name="azurermnetwork"></a>AzureRM.Network
* 장기 실행 Network cmdlet에 대한 -AsJob 지원이 추가되었습니다. 선택된 cmdlet을 백그라운드에서 실행하고 작업을 반환하여 진행률을 추적 및 제어할 수 있습니다.
* 유효한 위치를 통해 탭 완성 기능을 허용하는 -Location 매개 변수에 Location Completer를 추가했습니다.
* 현재 구독에서 리소스 그룹을 통해 탭 완성 기능을 허용하는 -ResourceGroup 매개 변수에 ResourceGroup Completer를 추가했습니다.

#### <a name="azurermnotificationhubs"></a>AzureRM.NotificationHubs
* 유효한 위치를 통해 탭 완성 기능을 허용하는 -Location 매개 변수에 Location Completer를 추가했습니다.
* 현재 구독에서 리소스 그룹을 통해 탭 완성 기능을 허용하는 -ResourceGroup 매개 변수에 ResourceGroup Completer를 추가했습니다.
* New-AzureRmNotificationHubsNamespace 및 Set-AzureRmNotificationHubsNamespace에 -Tag를 사용하는 -Tags 사용하지를 않습니다.

#### <a name="azurermoperationalinsights"></a>AzureRM.OperationalInsights
* 유효한 위치를 통해 탭 완성 기능을 허용하는 -Location 매개 변수에 Location Completer를 추가했습니다.
* 현재 구독에서 리소스 그룹을 통해 탭 완성 기능을 허용하는 -ResourceGroup 매개 변수에 ResourceGroup Completer를 추가했습니다.
* New-AzureRmOperationalInsightsSavedSearch, Set-AzureRmOperationalInsightsSavedSearch, New-AzureRmOperationalInsightsWorkspace 및 Set-AzureRmOperationalInsightsWorkspace에 -Tag를 사용하는 -Tags 사용하지를 않습니다.

#### <a name="azurermpowerbiembedded"></a>AzureRM.PowerBIEmbedded
* 유효한 위치를 통해 탭 완성 기능을 허용하는 -Location 매개 변수에 Location Completer를 추가했습니다.
* 현재 구독에서 리소스 그룹을 통해 탭 완성 기능을 허용하는 -ResourceGroup 매개 변수에 ResourceGroup Completer를 추가했습니다.

#### <a name="azurermrecoveryservices"></a>AzureRM.RecoveryServices
* 유효한 위치를 통해 탭 완성 기능을 허용하는 -Location 매개 변수에 Location Completer를 추가했습니다.
* 현재 구독에서 리소스 그룹을 통해 탭 완성 기능을 허용하는 -ResourceGroup 매개 변수에 ResourceGroup Completer를 추가했습니다.

#### <a name="azurermrecoveryservicesbackup"></a>AzureRM.RecoveryServices.Backup
* 현재 구독에서 리소스 그룹을 통해 탭 완성 기능을 허용하는 -ResourceGroup 매개 변수에 ResourceGroup Completer를 추가했습니다.
* Restore-AzureRmRecoveryServicesBackupItem cmdlet에 -UseOriginalStorageAccount 옵션을 추가했습니다.
  - 이 플래그를 사용하면 사용자가 원래 VM과 최대한 가까운 복원된 VM의 구성이 유지하도록 원래 스토리지 계정에 디스크를 복원하게 됩니다.
  - 복원 작업의 성능을 향상시키는 데에도 도움이 됩니다.

#### <a name="azurermrediscache"></a>AzureRM.RedisCache
* 유효한 위치를 통해 탭 완성 기능을 허용하는 -Location 매개 변수에 Location Completer를 추가했습니다.
* 현재 구독에서 리소스 그룹을 통해 탭 완성 기능을 허용하는 -ResourceGroup 매개 변수에 ResourceGroup Completer를 추가했습니다.
* 방화벽 규칙에 대한 새로운 3개의 cmdlet을 추가했습니다.
* 지리적 복제에 대한 새로운 3개의 cmdlet을 추가했습니다.
* 영역 및 태그에 대한 지원을 추가했습니다.
* 가능하면 ResourceGroup을 선택 사항으로 만듭니다.

#### <a name="azurermrelay"></a>AzureRM.Relay
* 유효한 위치를 통해 탭 완성 기능을 허용하는 -Location 매개 변수에 Location Completer를 추가했습니다.
* 현재 구독에서 리소스 그룹을 통해 탭 완성 기능을 허용하는 -ResourceGroup 매개 변수에 ResourceGroup Completer를 추가했습니다.

#### <a name="azurermresources"></a>AzureRM.Resources
* 유효한 위치를 통해 탭 완성 기능을 허용하는 -Location 매개 변수에 Location Completer를 추가했습니다.
* 현재 구독에서 리소스 그룹을 통해 탭 완성 기능을 허용하는 -ResourceGroup 매개 변수에 ResourceGroup Completer를 추가했습니다.
* 장기 실행 Resources cmdlet에 대한 -AsJob 지원을 추가했습니다. 선택된 cmdlet을 백그라운드에서 실행하고 작업을 반환하여 진행률을 추적 및 제어할 수 있습니다.
* 명명 규칙을 준수하도록 Get-AzureRmProviderOperation에서 Get-AzureRmResourceProviderAction에 별칭을 추가했습니다.

#### <a name="azurermscheduler"></a>AzureRM.Scheduler
* 유효한 위치를 통해 탭 완성 기능을 허용하는 -Location 매개 변수에 Location Completer를 추가했습니다.
* 현재 구독에서 리소스 그룹을 통해 탭 완성 기능을 허용하는 -ResourceGroup 매개 변수에 ResourceGroup Completer를 추가했습니다.

#### <a name="azurermservermanagement"></a>AzureRM.ServerManagement
* 유효한 위치를 통해 탭 완성 기능을 허용하는 -Location 매개 변수에 Location Completer를 추가했습니다.
* 현재 구독에서 리소스 그룹을 통해 탭 완성 기능을 허용하는 -ResourceGroup 매개 변수에 ResourceGroup Completer를 추가했습니다.
* New-AzureRmServerManagementNode 및 New-AzureRmServerManagementGateway에 -Tag를 사용하는 -Tags를 사용하지 않습니다.

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* 유효한 위치를 통해 탭 완성 기능을 허용하는 -Location 매개 변수에 Location Completer를 추가했습니다.
* 현재 구독에서 리소스 그룹을 통해 탭 완성 기능을 허용하는 -ResourceGroup 매개 변수에 ResourceGroup Completer를 추가했습니다.

#### <a name="azurermservicefabric"></a>AzureRM.ServiceFabric
* 유효한 위치를 통해 탭 완성 기능을 허용하는 -Location 매개 변수에 Location Completer를 추가했습니다.
* 현재 구독에서 리소스 그룹을 통해 탭 완성 기능을 허용하는 -ResourceGroup 매개 변수에 ResourceGroup Completer를 추가했습니다.

#### <a name="azurermsiterecovery"></a>AzureRM.SiteRecovery
* 유효한 위치를 통해 탭 완성 기능을 허용하는 -Location 매개 변수에 Location Completer를 추가했습니다.
* 현재 구독에서 리소스 그룹을 통해 탭 완성 기능을 허용하는 -ResourceGroup 매개 변수에 ResourceGroup Completer를 추가했습니다.

#### <a name="azurermsql"></a>AzureRM.Sql
* 감사 명령 매개 변수 설명을 업데이트합니다.
* 유효한 위치를 통해 탭 완성 기능을 허용하는 -Location 매개 변수에 Location Completer를 추가했습니다.
* 현재 구독에서 리소스 그룹을 통해 탭 완성 기능을 허용하는 -ResourceGroup 매개 변수에 ResourceGroup Completer를 추가했습니다.
* 장기 실행 cmdlet에 -AsJob 매개 변수 추가
* Get-AzureRmSqlServiceObjective에서 -DatabaseName 매개 변수를 사용하지 않습니다.

#### <a name="azurermstorage"></a>AzureRM.Storage
* 유효한 위치를 통해 탭 완성 기능을 허용하는 -Location 매개 변수에 Location Completer를 추가했습니다.
* 현재 구독에서 리소스 그룹을 통해 탭 완성 기능을 허용하는 -ResourceGroup 매개 변수에 ResourceGroup Completer를 추가했습니다.
* -EnableEncryptionService None 매개 변수를 사용하여 New-AzureRMStorageAccount 실행 cmdlet의 null 참조 문제를 해결합니다.
* 장기 실행 Storage cmdlet에 대한 -AsJob 지원이 추가되었습니다. 선택된 cmdlet을 백그라운드에서 실행하고 작업을 반환하여 진행률을 추적 및 제어할 수 있습니다.
    - 영향을 받는 cmdlet은 스토리지 계정 및 네트워크 규칙에 대한 New-, Remove-, Add- 및 Update-입니다.

#### <a name="azurermstreamanalytics"></a>AzureRM.StreamAnalytics
* 유효한 위치를 통해 탭 완성 기능을 허용하는 -Location 매개 변수에 Location Completer를 추가했습니다.
* 현재 구독에서 리소스 그룹을 통해 탭 완성 기능을 허용하는 -ResourceGroup 매개 변수에 ResourceGroup Completer를 추가했습니다.

#### <a name="azurermtrafficmanager"></a>AzureRM.TrafficManager
* 유효한 위치를 통해 탭 완성 기능을 허용하는 -Location 매개 변수에 Location Completer를 추가했습니다.
* 현재 구독에서 리소스 그룹을 통해 탭 완성 기능을 허용하는 -ResourceGroup 매개 변수에 ResourceGroup Completer를 추가했습니다.

#### <a name="azurermwebsites"></a>AzureRM.Websites
* 유효한 위치를 통해 탭 완성 기능을 허용하는 -Location 매개 변수에 Location Completer를 추가했습니다.
* 현재 구독에서 리소스 그룹을 통해 탭 완성 기능을 허용하는 -ResourceGroup 매개 변수에 ResourceGroup Completer를 추가했습니다.
* 장기 실행 Websites cmdlet에 대한 -AsJob 지원을 추가했습니다. 선택된 cmdlet을 백그라운드에서 실행하고 작업을 반환하여 진행률을 추적 및 제어할 수 있습니다.
     - 영향을 받는 cmdlet은 WebApps, AppServicePlan 및 Slots에 대한 New-, Remove-, Add- 및 Set-입니다.

## <a name="2017128-version-511"></a>2017.12.8 버전 5.1.1
* AnalysisServices
  - 모든 클라우드가 지원되도록 위치 확인 집합을 동적 조회로 변경합니다.
* Automation
  - Import-AzureRMAutomationRunbook으로 업데이트
    - 이제 Python2 Runbook에 대한 지원이 제공됩니다.
* Batch
  - 리소스 그룹이 없는 계정 작업으로 리소스 그룹을 자동 검색하지 못하는 버그가 수정되었습니다.
* 컴퓨팅
  - Get-AzureRmComputeResourceSku가 영역 정보를 보여 줍니다.
  - 문제 https://github.com/Azure/azure-powershell/issues/5038 의 수정을 위해 Disable-AzureRmVmssDiskEncryption 업데이트
  - 장기 실행 Compute cmdlet에 대한 -AsJob 지원이 추가되었습니다. 선택된 cmdlet을 백그라운드에서 실행하고 작업을 반환하여 진행률을 추적 및 제어할 수 있습니다.
    - 영향을 받는 cmdlet은 다음과 같습니다. Virtual Machines 및 Virtual Machine Scale Sets에 대한 New-, Update-, Set-, Remove-, Start-, Restart-, Stop- cmdlet입니다.
    - 단순한 매개 변수 집합이 New-AzureRmVM에 추가되었습니다. 따라서 스마트 기본값을 사용하여 Virtual Machine과 필요한 모든 리소스가 만들어집니다.
* ContainerInstance
  - Azure Container Instance SDK 2017-10-01 적용
    - 컨테이너 실행 완료 지원
    - Azure 파일 볼륨 탑재 지원
    - 공용 IP에 대한 여러 포트 열기 지원
* ContainerRegistry
  - 지역에서 복제 및 웹후크에 대한 새로운 cmdlet
    - Get/New/Remove-AzureRmContainerRegistryReplication
    - Get/New/Remove/Test/Update-AzureRmContainerRegistryWebhook
* DataFactories
    - 이제 자격 증명 암호화 기능은 "원격 액세스"가 사용된 경우(네트워크 사용) 및 "원격 액세스"가 사용되지 않는 경우(로컬 컴퓨터) 모두에서 작동합니다.
* DataFactoryV2
  - 두 개의 새로운 cmdlet이 추가되었습니다. Update-AzureRmDataFactoryV2 및 Stop-AzureRmDataFactoryV2PipelineRun
* DataLakeAnalytics
  - Submit-AzureRmDataLakeAnalyticsJob에 ScriptParameter라는 매개 변수가 추가됨
    - ScriptParameter에 대한 자세한 정보는 Submit-AzureRmDataLakeAnalyticsJob에서 Get-Help를 사용하여 확인할 수 있습니다.
  - New-AzureRmDataLakeAnalyticsAccount의 경우 MaxDegreeOfParallelism 매개 변수가 MaxAnalyticsUnits로 변경됨
    - MaxAnalyticsUnits 매개 변수에 대한 별칭이 추가됨: MaxDegreeOfParallelism
  - New-AzureRmDataLakeAnalyticsComputePolicy의 경우 MaxDegreeOfParallelismPerJob 매개 변수가 MaxAnalyticsUnitsPerJob으로 변경됨
    - MaxAnalyticsUnitsPerJob 매개 변수에 대한 별칭이 추가됨: MaxDegreeOfParallelismPerJob
  - Set-AzureRmDataLakeAnalyticsAccount의 경우 MaxDegreeOfParallelism 매개 변수가 MaxAnalyticsUnits로 변경됨
    - MaxAnalyticsUnits 매개 변수에 대한 별칭이 추가됨: MaxDegreeOfParallelism
  - Submit-AzureRmDataLakeAnalyticsJob의 경우 DegreeOfParallelism 매개 변수가 AnalyticsUnits로 변경됨
    - AnalyticsUnits 매개 변수에 대한 별칭이 추가됨: DegreeOfParallelism
  - Update-AzureRmDataLakeAnalyticsComputePolicy의 경우 MaxDegreeOfParallelismPerJob 매개 변수가 MaxAnalyticsUnitsPerJob으로 변경됨
    - MaxAnalyticsUnitsPerJob 매개 변수에 대한 별칭이 추가됨: MaxDegreeOfParallelismPerJob
* MachineLearningCompute
  - Set-AzureRmMlOpCluster 추가
    - 클러스터의 에이전트 개수 또는 SSL 구성 업데이트
  - 오케스트레이터 속성은 선택 사항입니다.
    - 서비스에서 서비스 주체를 생성하므로(제공되지 않은 경우) 오케스트레이터 속성은 선택 사항입니다.
* PowerBIEmbedded
  - Power BI Embedded Capacity cmdlet에 대한 지원 추가
  - 새 Cmdlet Get-AzureRmPowerBIEmbeddedCapacity - PowerBI Embedded Capacity에 대한 정보를 가져옵니다.
  - 새 Cmdlet New-AzureRmPowerBIEmbeddedCapacity - 새 PowerBI Embedded Capacity를 만듭니다.
  - 새 Cmdlet Remove-AzureRmPowerBIEmbeddedCapacity - PowerBI Embedded Capacity의 인스턴스를 삭제합니다.
  - 새 Cmdlet Resume-AzureRmPowerBIEmbeddedCapacity - PowerBI Embedded Capacity의 인스턴스를 다시 시작합니다.
  - 새 Cmdlet Suspend-AzureRmPowerBIEmbeddedCapacity - PowerBI Embedded Capacity의 인스턴스를 일시 중단합니다.
  - 새 Cmdlet Test-AzureRmPowerBIEmbeddedCapacity - PowerBI Embedded Capacity 인스턴스의 존재 여부를 테스트합니다.
  - 새 Cmdlet Update-AzureRmPowerBIEmbeddedCapacity - PowerBI Embedded Capacity의 인스턴스를 수정합니다.
* 프로필
  - USGovernmentActiveDirectoryEndpoint가 https://login.microsoftonline.us/ 로 업데이트됨
    - Azure Government 엔드포인트 매핑에 대한 보다 자세한 내용은 다음을 참조하세요. https://docs.microsoft.com/azure/azure-government/documentation-government-developer-guide#endpoint-mapping
    - cmdlet에 대한 -AsJob 지원이 추가됨. 선택된 cmdlet을 사용하여 백그라운드에서 실행하고 작업을 반환하여 진행률 추적 및 제어
    - -AsJob 매개 변수가 Get-AzureRmSubscription cmdlet에 추가됨
* RecoveryServices.Backup
  - 버그 수정됨 - Get-AzureRmRecoveryServicesBackupItem은 컨테이너 이름 필터에 대해 대/소문자를 구분하지 않는 비교를 수행합니다.
  - 버그 수정됨 - AzureVmItem에는 백업 작업이 마지막으로 발생한 시간(LastBackupTime)을 보여 주는 속성이 있습니다.
* 리소스
  - Get-AzureRMRoleAssignment가 사용자 지정 역할에 대한 roledefiniton 이름 없이 할당하는 문제가 해결되었습니다.
    - 이제 사용자는 역할 유형에 관계없이 roledefinition이 있는 할당으로 Get-AzureRMRoleAssignment를 사용할 수 있습니다.
  - assignablescopes에 새 범위가 있을 때 RD를 throw하는 데 사용된 Set-AzureRMRoleRoleDefinition이 오류를 찾을 수 없는 문제가 해결되었습니다.
    - 이제 사용자는 범위의 위치와 관계없이 새 범위를 포함하여 할당 가능한 범위로 Set-AzureRMRoleRoleDefinition을 사용할 수 있습니다.
  - 범위를 "/"로 끝내도록 허용
    - 사용자는 이제 API 및 CLI와 일치하고 범위가 "/"로 끝나는 RoleDefinition 및 RoleAssignment commandlet을 사용할 수 있습니다.
  - 사용자가 위임 플래그를 사용하여 RoleAssignment를 만들도록 허용
    - 사용자는 위임 플래그를 추가하는 옵션과 함께 New-AzureRMRoleAssignment를 사용할 수 있습니다.
  - RoleAssignment가 범위 매개 변수를 따르도록 수정
  - New-AzureRmRoleAssignment Commandlet에서 ServicePrincipalName에 대한 별칭 추가
    - 사용자가 New-AzureRmRoleAssignment Commandlet을 사용할 때 ServicePrincipalName 대신 ApplicationId를 사용할 수 있습니다.
* SiteRecovery
  - 향후 주요 변경 릴리스에 대한 준비에서, 이 모듈의 모든 cmdlet에 대한 사용 중단 경고를 추가합니다.
    - AzureRM에서 cmdlet을 마이그레이션하는 방법에 대한 자세한 내용은 다음 주요 변경 사항 가이드를 참조하세요.
* Sql
  - Set-AzureRmSqlDatabase를 사용하여 데이터베이스 이름을 바꾸는 기능이 추가됨
  - 문제 https://github.com/Azure/azure-powershell/issues/4974 해결
    - 감사 cmdlet에 대해 유효하지 않은 AUDIT_CHANGED_GROUP 값을 제공하면 더 이상 오류가 발생하지 않으며 향후 릴리스에서 제거됩니다.
  - 문제 https://github.com/Azure/azure-powershell/issues/5046 해결
    - 감사 cmdlet의 AuditAction 매개 변수가 더 이상 무시되지 않습니다.
  - '보조' StorageKeyType이 제공된 경우 감사 cmdlet에서 문제가 해결되었습니다.
    - Blob 감사를 설정할 때, StorageKeyType 매개 변수에 '보조' 값을 제공할 때 보조 키 대신, 주 스토리지 계정 키가 사용되었습니다.
  - Set-AzureRmSqlServerTransparentDataEncryptionProtector에서 확인 메시지의 문구 변경
* Azure(RDFE)
    - 모든 RemoteApp Cmdlet 제거
* Azure.Storage
    - Azure Storage 클라이언트 라이브러리 8.6.0 및 Azure Storage DataMovement 라이브러리 0.6.5로 업그레이드

## <a name="20171110-version-501"></a>2017.11.10 버전 5.0.1
* 다음과 같은 모듈에서 실행할 때 몇 가지 cmdlet이 실패하는 어셈블리 로딩 문제 해결:
  - AzureRM.ApiManagement
  - AzureRM.Backup
  - AzureRM.Backup
  - AzureRM.Compute
  - AzureRM.DataFactories
  - AzureRM.HDInsight
  - AzureRM.KeyVault
  - AzureRM.RecoveryServices
  - AzureRM.RecoveryServices.Backup
  - AzureRM.RecoveryServices.SiteRecovery
  - AzureRM.RedisCache
  - AzureRM.SiteRecovery
  - AzureRM.Sql
  - AzureRM.Storage
  - AzureRM.StreamAnalytics

## <a name="2017118---version-500"></a>2017.11.8 - 버전 5.0.0
* 참고:  이는 호환성이 손상되는 변경 릴리스입니다. 중요 변경 사항의 전체 목록은 마이그레이션 가이드(https://aka.ms/azps-migration-guide) )를 참조하세요.
* AzureRM의 모든 cmdlet는 이제 온라인 도움말을 지원합니다.
  - -Online 매개 변수와 함께 Get-Help를 실행하여 기본 인터넷 브라우저에서 온라인 도움말을 엽니다.
* AnalysisServices
  * 동기화를 위해 새로운 AsAzure REST API로 작동하도록 Synchronize-AzureAsInstance 명령 수정
* ApiManagement
  * 이 릴리스의 ApiManagement에 대한 중요 변경 사항은 마이그레이션 가이드를 참조하세요.
  * 문제 https://github.com/Azure/azure-powershell/issues/4510 의 수정을 위해 Cmdlet Get-AzureRmApiManagementUser 업데이트
  * [https://github.com/Azure/azure-powershell/issues/4069](https://github.com/Azure/azure-powershell/issues/4069 )의 경로가 비어 있는 API 생성을 위해 Cmdlet New-AzureRmApiManagementApi 업데이트
* ApplicationInsights
  * applicaiton insights 리소스를 가져오기/만들기/제거하기 위해 명령 추가
    - Get AzureRmApplicationInsights
    - Get AzureRmApplicationInsights
    - Get AzureRmApplicationInsights
  * application insights 리소스의 가격 책정/일일 상한선을 가져오기/업데이트하기 위해 명령 추가
    - Get-AzureRmApplicationInsights -IncludeDailyCap
    - Set-AzureRmApplicationInsightsPricingPlan
    - Set-AzureRmApplicationInsightsDailyCap
  * applicaiton insights 리소스의 연속 내보내기를 가져오기/만들기/업데이트하기/제거하기 위해 명령 추가
    - Get-AzureRmApplicationInsightsContinuousExport
    - Set-AzureRmApplicationInsightsContinuousExport
    - New-AzureRmApplicationInsightsContinuousExport
    - Remove-AzureRmApplicationInsightsContinuousExport
  * applicaiton insights 리소스의 api 키를 가져오기/만들기/제거하기 위해 명령 추가
    - Get-AzureRmApplicationInsightsApiKey
    - New-AzureRmApplicationInsightsApiKey
    - Remove-AzureRmApplicationInsightsApiKey
* AzureBatch
  * `New-AzureRmBatchAccount`에 새 매개 변수를 추가했습니다.
    - `PoolAllocationMode`: 배치 계정에서 풀을 만드는 데 사용하는 할당 모드입니다. 사용자의 구독에서 풀 노드를 할당하는 배치 계정을 만들려면 이를 `UserSubscription`으로 설정합니다.
    - `KeyVaultId`: 배치 계정과 연결된 Azure Key Vault의 리소스 ID입니다.
    - `KeyVaultUrl`: 배치 계정과 연결된 Azure Key Vault의 URL입니다.
  * 매개 변수를 `New-AzureBatchTask`로 업데이트했습니다.
    - `RunElevated` 스위치를 제거했습니다. `UserIdentity` 매개 변수가 `RunElevated`를 대체하기 위해 추가되었으며, 아래와 같이 `PSUserIdentity`를 구성하여 동등한 동작을 얻을 수 있습니다.
      - $autoUser = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoUserSpecification -ArgumentList @("Task", "Admin")
      - $userIdentity = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserIdentity $autoUser
    - `AuthenticationTokenSettings` 매개 변수를 추가했습니다. 이 매개 변수를 사용하면 실행할 때 일괄 처리 서비스가 인증 토큰을 작업에 제공하도록 요청할 수 있어, 일괄 처리 서비스에 요청을 발행하기 위해 배치 계정 키를 작업에 전달할 필요가 없게 됩니다.
    - `ContainerSettings` 매개 변수를 추가했습니다.
      - 이 매개 변수를 사용하면 일괄 처리 서비스가 컨테이너 내의 작업을 실행하도록 요청할 수 있습니다.
    - `OutputFiles` 매개 변수를 추가했습니다.
      - 이 매개 변수를 사용하면 완료된 후 Azure Storage에 파일을 업로드하는 작업을 구성할 수 있습니다.
  * 매개 변수를 `New-AzureBatchPool`로 업데이트했습니다.
    - `UserAccounts` 매개 변수를 추가했습니다.
      - 이 매개 변수는 풀의 각 노드에서 만든 사용자 계정을 정의합니다.
    - `TargetLowPriorityComputeNodes`를 추가하고 `TargetDedicated`의 이름을 `TargetDedicatedComputeNodes`으로 변경했습니다.
      - `TargetDedicatedComputeNodes` 매개 변수에 대해 `TargetDedicated` 별칭이 만들어졌습니다.
    - `NetworkConfiguration` 매개 변수를 추가했습니다.
      - 이 매개 변수를 사용하면 풀 네트워크 설정을 구성할 수 있습니다.
  * 매개 변수를 `New-AzureBatchCertificate`로 업데이트했습니다.
    - `Password` 매개 변수가 이제 `SecureString`이 되었습니다.
  * 매개 변수를 `New-AzureBatchComputeNodeUser`로 업데이트했습니다.
    - `Password` 매개 변수가 이제 `SecureString`이 되었습니다.
  * 매개 변수를 `Set-AzureBatchComputeNodeUser`로 업데이트했습니다.
    - `Password` 매개 변수가 이제 `SecureString`이 되었습니다.
  * `Get-AzureBatchNodeFile`, `Get-AzureBatchNodeFileContent`, 및 `Remove-AzureBatchNodeFile`에서 `Name` 매개 변수의 이름이 `Path`로 변경되었습니다.
    - `Path` 매개 변수에 대해 `Name` 별칭이 만들어졌습니다.
  * 개체에 대한 변경 사항
    - 전체 목록은 일괄 처리 변경 로그를 참조하세요.
  * Azure Active Directory 기반 인증에 대한 지원이 추가되었습니다.
    - Azure Active Directory 인증을 사용하려면 `Get-AzureRmBatchAccount` cmdlet를 사용하여 `BatchAccountContext` 개체를 검색하고 이 `BatchAccountContext`를 일괄 처리 서비스 cmdlet의 `-BatchContext` 매개 변수에 제공합니다. Azure Active Directory 인증은 `PoolAllocationMode = UserSubscription`이 있는 계정에 필수입니다.
    - 기존 계정 또는 `PoolAllocationMode = BatchService`로 만든 새 계정의 경우, `Get-AzureRmBatchAccoutKeys` cmdlet를 사용하는 `BatchAccountContext` 개체를 검색하여 공유 키 인증을 계속 사용할 수 있습니다.
* 컴퓨팅
  * Azure Disk Encryption 확장 명령
    - 'Set-AzureRmVmDiskEncryptionExtension'에 대한 새 매개 변수': '-EncryptFormatAll' 암호화 형식 데이터 디스크
    - 'Set-AzureRmVmDiskEncryptionExtension'에 대한 새로운 매개 변수: '-ExtensionPublisherName' 및 '-ExtensionType'이 다른 확장 버전으로 전환 허용
    - 'Disable-AzureRmVmDiskEncryption'에 대한 새로운 매개 변수: '-ExtensionPublisherName' 및 '-ExtensionType'이 다른 확장 버전으로 전환 허용
    - 'Get-AzureRmVmDiskEncryptionStatus'에 대한 새로운 매개 변수: '-ExtensionPublisherName' 및 '-ExtensionType'이 다른 확장 버전으로 전환 허용
* DataLakeAnalytics
  * 이 릴리스의 DataLakeAnalytics에 대한 중요 변경 사항은 마이그레이션 가이드를 참조하세요.
  * Get-AzureRmDataLakeAnalyticsAccount의 두 가지 OutputTypes 중 하나를 변경
    - 목록\<DataLakeAnalyticsAccount>에서 목록\<PSDataLakeAnalyticsAccountBasic>으로
    - PSDataLakeAnalyticsAccountBasic의 속성은 DataLakeAnalyticsAccount 속성의 엄격한 하위 집합입니다.
    - DataLakeAnalyticsAccount에 있는 추가 속성은 서비스에 의해 반환되지 않습니다.  따라서 이 변경 사항은 이를 정확하게 반영합니다. 이러한 추가 속성은 PSDataLakeAnalyticsAccountBasic에 여전히 있지만, Obsolete로 태그가 지정됩니다.
  * Get-AzureRmDataLakeAnalyticsJob의 두 가지 OutputTypes 중 하나를 변경
    - 목록\<JobInformation>에서 목록\<PSJobInformationBasic>으로
    - PSJobInformationBasic 속성은 JobInformation 속성의 엄격한 하위 집합입니다.
    - JobInformation에 있는 추가 속성은 서비스에 의해 반환되지 않습니다.  따라서 이 변경 사항은 이를 정확하게 반영합니다. 이러한 추가 속성은 PSJobInformationBasic에 여전히 있지만, Obsolete로 태그가 지정됩니다.
* DataLakeStore
  * 이 릴리스의 DataLakeStore에 대한 중요 변경 사항은 마이그레이션 가이드를 참조하세요.
  * Get-AzureRmDataLakeStoreAccount의 두 가지 OutputTypes 중 하나를 변경
    - 목록\<PSDataLakeStoreAccount>에서 목록\<PSDataLakeStoreAccountBasic>으로
    - PSDataLakeStoreAccountBasic의 속성은 PSDataLakeStoreAccount 속성의 엄격한 하위 집합입니다.
    - PSDataLakeStoreAccount에 있는 추가 속성은 서비스에 의해 반환되지 않습니다.  따라서 이 변경 사항은 이를 정확하게 반영합니다. 이러한 추가 속성은 PSDataLakeStoreAccountBasic에 여전히 있지만, Obsolete로 태그가 지정됩니다.
* Dns
  * Azure DNS의 CAA 레코드 종류에 대한 지원
    - CAA 레코드 종류에서 모든 작업 지원
* EventHub
  * 이 릴리스의 EventHub에 대한 중요 변경 사항은 마이그레이션 가이드를 참조하세요.
* 자세한 정보
  * 이 릴리스의 Insights에 대한 중요 변경 사항은 마이그레이션 가이드를 참조하세요.
* 네트워크
  * 이 릴리스의 Network에 대한 중요 변경 사항은 마이그레이션 가이드를 참조하세요.
  * 지정된 Azure 지역에 대해 사용 가능한 인터넷 서비스 공급자를 나열하는 cmdlet이 추가됨
    - Get-AzureRmNetworkWatcherReachabilityProvidersList
  * 지정된 위치에서 Azure 지역까지 인터넷 서비스 공급자에 대한 상대적 대기 시간 점수를 얻기 위한 cmdlet이 추가됨
    - Get-AzureRmNetworkWatcherReachabilityReport
* 프로필
  - Set-AzureRmDefault
    - 이 cmdlet을 사용하여 기본 리소스 그룹을 설정합니다.  이렇게 하면 일부 cmdlet에 대해 -ResourceGroup 매개 변수가 선택 사항이 되고 리소스 그룹이 지정되지 않은 경우 기본값이 사용됩니다.
    - ```Set-AzureRmDefault -ResourceGroupName "ExampleResourceGroup"```
    - 구독에 지정된 리소스 그룹이 있으면 이 리소스 그룹은 기본값으로 설정됩니다.  그렇지 않은 경우 리소스 그룹이 만들어진 다음 기본값으로 설정됩니다.
  - Get-AzureRmDefault
    - 이 cmdlet을 사용하여 현재 기본 리소스 그룹(및 나중의 다른 기본값)을 가져옵니다.
    - ```Get-AzureRmDefault -ResourceGroup```
  - Clear-AzureRmDefault
    - 이 cmdlet을 사용하여 현재 기본 리소스 그룹을 제거합니다.
    - ```Clear-AzureRmDefault -ResourceGroup```
  - Add-AzureRmEnvironment 및 Set-AzureRmEnvironment
    - 일괄 처리 서비스에 대한 인증 토큰을 얻을 때 사용할 Azure Batch Active Directory 대상을 지정할 수 있는 BatchAudience 매개 변수를 추가합니다.
* RecoveryServices.Backup
  * 즉시 파일 복구를 수행하기 위해 cmdlet을 추가했습니다.
    - Get-AzureRmRecoveryServicesBackupRPMountScript
    - Disable-AzureRmRecoveryServicesBackupRPMountScript
  * RecoveryServices.Backup SDK 버전을 최신 버전으로 업데이트됨
  * 테스트 실행에 필요한 모든 설정이 테스트 자체에서 지정되도록 Azure VM 워크로드에 대한 테스트를 업데이트했습니다.
  * [https://github.com/Azure/azure-powershell/issues/3164](https://github.com/Azure/azure-powershell/issues/3164 ) 수정
* RecoveryServices.SiteRecovery
  * ASR VMware의 Azure Site Recovery에 대한 변경 사항(cmdlet은 현재 Enterprise-Enterprise, Enterprise-Azure, HyperV-Azure에 대한 작업을 지원)
    - New-AzureRmRecoveryServicesAsrPolicy
    - New-AzureRmRecoveryServicesAsrProtectedItem
    - Update-AzureRmRecoveryServicesAsrPolicy
    - Update-AzureRmRecoveryServicesAsrProtectionDirection
  * AAD 기반 자격 증명 모음에 대한 지원이 추가됨
  * VCenter 리소스를 관리하기 위해 cmdlet이 추가됨
    - Get-AzureRmRecoveryServicesAsrVCenter
    - New-AzureRmRecoveryServicesAsrVCenter
    - Remove-AzureRmRecoveryServicesAsrVCenter
    - Update-AzureRmRecoveryServicesAsrVCenter
  * 다른 cmdlet 추가
    - Get-AzureRmRecoveryServicesAsrAlertSetting
    - Get-AzureRmRecoveryServicesAsrEvent
    - New-AzureRmRecoveryServicesAsrProtectableItem
    - Set-AzureRmRecoveryServicesAsrAlertSetting
    - Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob
    - Start-AzureRmRecoveryServicesAsrSwitchProcessServerJob
    - Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob
    - Update-AzureRmRecoveryServicesAsrMobilityService
* ServiceBus
  - 이 릴리스의 ServiceBus에 대한 중요 변경 사항은 마이그레이션 가이드를 참조하세요.
* Sql
  * 목록에 대한 지원 추가 및 데이터베이스에서 비동기 updatelo 작업 취소
    - 기존 cmdlet Get-AzureRmSqlDatabaseActivity를 업데이트하여 DB updateslo를 작업 상태로 반환합니다.
    - 새 cmdlet Stop-AzureRmSqlDatabaseActivity를 추가하여 데이터베이스에서 비동기 updateslo 작업을 취소합니다.
  * 데이터베이스 및 탄성 풀에 대한 영역 중복 지원 추가
    - New-AzureRmSqlDatabase에 ZoneRedundant 스위치 매개 변수 추가
    - Set-AzureRmSqlDatabase에 ZoneRedundant 스위치 매개 변수 추가
    - New-AzureRmSqlElasticPool에 ZoneRedundant 스위치 매개 변수 추가
    - Set-AzureRmSqlElasticPool에 ZoneRedundant 스위치 매개 변수 추가
  * 서버 DNS 별칭에 대한 지원 추가
    - 서버 및 별칭 이름별 서버 DNS 별칭 또는 Azure SQL Server에 대한 서버 DNS 별칭의 목록을 가져오는 Get-AzureRmSqlServerDnsAlias cmdlet 추가
    - 지정된 Azure SQL Server에 대한 새 서버 DNS 별칭을 만드는 New-AzureRmSqlServerDnsAlias cmdlet 추가
    - 서버 DNS 별칭이 가리키는 Azure SQL Server의 업데이트를 허용하는 Set-AzurermSqlServerDnsAlias cmlet 추가
    - Azure SQL Server에 대한 새 서버 DNS 별칭을 제거하는 Remove-AzureRmSqlServerDnsAlias cmdlet 추가
* Azure.Storage
  * Azure Storage 클라이언트 라이브러리 8.5.0 및 Azure Storage DataMovement 라이브러리 0.6.3으로 업그레이드
  * 파일 공유 스냅샷 지원 기능 추가
    - Get-AzureStorageShare에 'SnapshotTime' 매개 변수 추가
    - Remove-AzureStorageShare에 'IncludeAllSnapshot' 매개 변수 추가
