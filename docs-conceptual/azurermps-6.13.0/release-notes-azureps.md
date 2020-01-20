---
title: Azure PowerShell 변경 로그 | Microsoft Docs
description: Azure PowerShell에 대한 최신 릴리스의 변경 내용입니다.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 08/28/2018
ms.openlocfilehash: eecd66ddf433cc2543ceeaef1519d69179f2f099
ms.sourcegitcommit: bbd3f061cac3417ce588487c1ae4e0bc52c11d6a
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/11/2019
ms.locfileid: "65534448"
---
# <a name="release-notes"></a>릴리스 정보

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

Azure PowerShell에 대한 릴리스의 변경 내용 목록입니다.

---
## <a name="6130---november-2018"></a>6.13.0 - 2018년 11월
#### <a name="azurermprofile"></a>AzureRM.Profile
* ClientRuntime의 최신 버전을 사용하도록 일반적인 코드를 업데이트합니다.

#### <a name="azurermapimanagement"></a>AzureRM.ApiManagement
* 형식 매핑 문제에 대한 종속성 업데이트

#### <a name="azurermautomation"></a>AzureRM.Automation
* Azure Automation cmdlet 기반 Swagger
* 업데이트 관리 cmdlet 추가
* 소스 제어 cmdlet 추가
* Remove-AzureRmAutomationHybridWorkerGroup cmdlet 추가
* DSC 노드 등록 명령 수정

#### <a name="azurermcompute"></a>AzureRM.Compute
* SystemAssigned ID에 대한 ID 문제 수정
* 형식 매핑 문제에 대한 종속성 업데이트

#### <a name="azurermcontainerinstance"></a>AzureRM.ContainerInstance
* 형식 매핑 문제에 대한 종속성 업데이트

#### <a name="azurermmarketplaceordering"></a>AzureRM.MarketplaceOrdering
* 마켓플레이스 cmdlet에 대한 예제 설명 업데이트

#### <a name="azurermnetwork"></a>AzureRM.Network
* New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError cmdlet 추가
* 지원되는 AzureFirewall 네트워크 프로토콜에 ICMP 다시 추가
* Test-AzureRmNetworkWatcherConnectivity cmdlet을 업데이트하여 대상 ID, 주소 및 포트 유효성 검사를 추가합니다. 
* VirtualNetwork 맵의 메모리 사용 문제 해결

#### <a name="azurermrecoveryservicesbackup"></a>AzureRM.RecoveryServices.Backup
* 보호된 파일 공유에 대한 정책을 수정하는 것에 대해 수정합니다.
* 정책 표준 시간대를 대문자로 변환했습니다.

#### <a name="azurermrecoveryservicessiterecovery"></a>AzureRM.RecoveryServices.SiteRecovery
* New-AzureRmRecoveryServicesAsrProtectableItem의 예제 정정
* 형식 매핑 문제에 대한 종속성 업데이트

#### <a name="azurermrelay"></a>AzureRM.Relay
* 선택적 매개 변수 -KeyValue를 New-AzureRmRelayKey cmdlet에 추가하여 사용자가 KeyValue를 제공할 수 있습니다.

#### <a name="azurermresources"></a>AzureRM.Resources
* `New-AzureRmPolicyAssignment` 및 `Set-AzureRmPolicyAssignment`의 자원 ID 관련 매개 변수에 대한 도움말 문서를 업데이트함
* -Metadata를 사용하는 New-AzureRmPolicyDefinition에 대한 예제 추가
* NetStandard의 태그 키에서 대소문자 보존을 허용하도록 수정: #7678 #7703

#### <a name="azurermservicefabric"></a>AzureRM.ServiceFabric
* 향후 호환성이 손상되는 변경에 대한 사용 중단 메시지 추가

#### <a name="azurermsql"></a>AzureRM.Sql
* Azure Sql Database Managed Instance 및 Azure Sql Managed Database에 CRUD 작업을 위한 새 cmdlet 추가
    - Get-AzureRmSqlInstance
    - New-AzureRmSqlInstance
    - Set-AzureRmSqlInstance
    - Remove-AzureRmSqlInstance
    - Get-AzureRmSqlInstanceDatabase
    - New-AzureRmSqlInstanceDatabase
    - Restore-AzureRmSqlInstanceDatabase
    - Remove-AzureRmSqlInstanceDatabase
* 서버 또는 데이터베이스에서 확장 감사 정책 관리를 활성화했습니다.
    - 새 매개 변수(PredicateExpression)가 감사 로그 필터링을 사용하도록 추가되었습니다.
    - Cmdlet이 레거시 클라이언트 대신 SQL 클라이언트를 사용하도록 수정되었습니다.
    - Set-AzureRmSqlServerAuditing.
    - Get-AzureRmSqlServerAuditing.
    - Set-AzureRmSqlDatabaseAuditing.
    - Get-AzureRmSqlDatabaseAuditing.
* 스토리지 계정 이름 매개 변수가 설정된 Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings를 사용할 때의 문제 해결

## <a name="6120---november-2018"></a>6.12.0 - 2018년 11월
#### <a name="azurermprofile"></a>AzureRM.Profile
* ClientRuntime의 최신 버전을 사용하도록 일반적인 코드를 업데이트합니다.
* Connect-AzureRmAccount cmdlet의 매개 변수 TenantId 이름을 Tenant로 바꾸고 TenantId의 별칭을 추가합니다
* Connect-AzureRmAccount의 업데이트된 TenantId 설명
* 테넌트 도메인을 제공할 때 실패한 로그인에 대한 오류 메시지 수정
    - https://github.com/Azure/azure-powershell/issues/6936
* 테넌트에 구독이 없는 계정의 컨텍스트 이름 충돌 문제 수정
    - https://github.com/Azure/azure-powershell/issues/7453
* MSI를 사용할 때 DataLake 엔드포인트 문제 수정
    - https://github.com/Azure/azure-powershell/issues/7462
* 연결되지 않은 경우 'Disconnect-AzureRmAccount'가 throw하는 문제 수정
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azurermautomation"></a>AzureRM.Automation
* cmdlet DLL 파일 이름이 Microsoft.Azure.Commands.Automation.dll로 변경됨

#### <a name="azurermcognitiveservices"></a>AzureRM.CognitiveServices
* Get-AzureRmCognitiveServicesAccountSkus 작업을 추가합니다.

#### <a name="azurermcompute"></a>AzureRM.Compute
* Add-AzureRmVmssVMDataDisk 및 Remove-AzureRmVmssVMDataDisk cmdlet를 추가합니다
* Get-AzureRmVMImage는 AutomaticOSUpgradeProperties를 표시합니다
* 수정된 SetAzureRmVMChefExtension -BootstrapOptions 및 -JsonAttribute option 값이 json 형식으로 설정하지 않습니다.

#### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* DataLake 패키지를 1.1.10으로 업데이트합니다.
* 기본 동시성을 다중 스레드 작업에 추가합니다.

#### <a name="azurerminsights"></a>AzureRM.Insights
* 해결된 문제 #7267(자동 크기 조정 영역)
    - 열거된 매개 변수를 제대로 설정하지 않은 새 자동 크기 조정 규칙을 만드는 데 문제가 있습니다(이를 항상 기본값으로 설정함).
* 해결된 문제 # 7513[자세한 정보] Set-AzureRMDiagnosticSetting은 설정을 생성하는 동안 범주를 명시적으로 지정해야 합니다
    - 이제 cmdlet은 생성 중에 사용할 범주를 명시적으로 표시할 필요가 없습니다. 즉, 문서화된대로 작동합니다

#### <a name="azurermnetwork"></a>AzureRM.Network
* 다음 cmdlet에 대해 PeeringType을 필수 매개 변수로 변경했습니다.
    - Get-AzureRmExpressRouteCircuitRouteTable
    - Get-AzureRmExpressRouteCircuitARPTable
    - Get-AzureRmExpressRouteCircuitRouteTableSummary
    - Get-AzureRMExpressRouteCrossConnectionArpTable
    - Get-AzureRMExpressRouteCrossConnectionRouteTable
    - Get-AzureRMExpressRouteCrossConnectionRouteTableSummary

#### <a name="azurermpolicyinsights"></a>AzureRM.PolicyInsights
* 추가된 정책 재구성 cmdlet

#### <a name="azurermrecoveryservicesbackup"></a>AzureRM.RecoveryServices.Backup
* 복구 서비스에 Azure 파일 공유 지원 추가.

#### <a name="azurermresources"></a>AzureRM.Resources
* https://github.com/Azure/azure-powershell/issues/7402 에 대한 수정
    - 'Get-AzureRmResource'에 대해 '-ResourceId' 매개 변수를 사용하여 리소스 나열 허용

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* 마이그레이션 상태를 알 수 있도록 PSServiceBusMigrationConfigurationAttributes에 MigrationState 읽기 전용 속성 추가.

#### <a name="azurermservicefabric"></a>AzureRM.ServiceFabric
* Linux Vmss에 인증서 추가 수정.
* 'Add-AzureRmServiceFabricClusterCertificate' 수정
    - 새 인증서(Azure/service-fabric-issues#932)에서 올바른 지문을 사용.
    - 올바르게 예외 표시(Azure/service-fabric-issues#1054).
* Vmss CreateOrUpdate 작업을 시작하기 전에 'Update-AzureRmServiceFabricDurability'를 수정하여 클러스터 구성 업데이트.

## <a name="6110---october-2018"></a>6.11.0 - 2018년 10월
#### <a name="azurermprofile"></a>AzureRM.Profile
* CloudShell에서 Get-AzureRmSubscription을 사용하여 문제를 해결합니다.
* ClientRuntime의 최신 버전을 사용하도록 일반적인 코드를 업데이트합니다.

#### <a name="azurermbackup"></a>AzureRM.Backup
* Azure Backup cmdlet이 사용되지 않습니다.

#### <a name="azurermcompute"></a>AzureRM.Compute
* 'New-AzureRmVm'에 대해 간단한 매개 변수를 사용하는 경우 가속화된 네트워킹을 설정하기 위해 새 크기가 VM 크기의 허용 목록에 추가되었습니다.
* 모든 cmdlet에 ResourceName 인수 완성자가 추가되었습니다.

#### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* Virtual Network 규칙에 대한 지원 추가
    - Get-AzureRmDataLakeStoreVirtualNetworkRule: Azure Data Lake Store 가상 네트워크 규칙을 가져오거나 나열합니다.
    - Add-AzureRmDataLakeStoreVirtualNetworkRule: 지정된 Data Lake Store 계정에 가상 네트워크 규칙을 추가합니다.
    - Set-AzureRmDataLakeStoreVirtualNetworkRule: 지정된 Data Lake Store 계정에 지정된 가상 네트워크 규칙을 수정합니다.
    - Remove-AzureRmDataLakeStoreVirtualNetworkRule: Azure Data Lake Store 가상 네트워크 규칙을 삭제합니다.

#### <a name="azurermnetwork"></a>AzureRM.Network
* Test-AzureRmNetworkWatcherConnectivity cmdlet을 업데이트하고, 백 엔드에 프로토콜 값을 전달합니다.
* 모든 cmdlet에 ResourceName 인수 완성자가 추가되었습니다.

#### <a name="azurermresources"></a>AzureRM.Resources
* (기본 프로필에 구독이 없고 범위가 지정되지 않은 경우) 시나리오에서 의미 있는 예외를 추가하여 Get-AzureRMRoleDefinition이 인식할 수 없는 예외를 throw하는 문제를 수정합니다. 또한 기본 매개 변수 집합을 'RoleDefinitionNameParameterSet'으로 설정합니다.

## <a name="6100---october-2018"></a>2018년 10월 - 6.10.0
#### <a name="azurestorage"></a>Azure.Storage
* 대상에 메타데이터가 있을 때 Blob/파일이 메타 데이터를 복사하지 않는 문제 수정
    - Start-AzureStorageBlobCopy
    - Start-AzureStorageFileCopy

#### <a name="azurermcognitiveservices"></a>AzureRM.CognitiveServices
* 기존 계정이 없는 Get-AzureRmCognitiveServicesAccountSkus를 지원

#### <a name="azurermcompute"></a>AzureRM.Compute
* Get-AzureRmVM -ResourceGroupName <rg>가 필요한 경우 50개가 넘는 결과를 반환하도록 수정
* 'SimpleParameterSet' 예제가 New-AzureRmVmss cmdlet 도움말에 추가됨
* Azure Disk Encryption 진행률 메시지의 오타를 수정

#### <a name="azurermdatafactoryv2"></a>AzureRM.DataFactoryV2
* ADF.Net SDK 버전을 2.3.0으로 업데이트

#### <a name="azurermnetwork"></a>AzureRM.Network
* NetworkProfile 기능 추가 추가된 새 cmdlet은 다음과 같습니다.
    - Get-AzureRMNetworkProfile
    - New-AzureRMNetworkProfile
    - Remove-AzureRMNetworkProfile
    - Set-AzureRMNetworkProfile
    - New-AzureRMContainerNicConfig
    - New-AzureRmContainerNicConfigIpConfig
* 서브넷 모델에 서비스 연결 링크 추가
* New-AzureRmVirtualNetworkTap, Get-AzureRmVirtualNetworkTap, Set-AzureRmVirtualNetworkTap, Remove-AzureRmVirtualNetworkTap cmdlet 추가
* Set-AzureRmNEtworkInterfaceTapConfig, Get-AzureRmNEtworkInterfaceTapConfig, Remove-AzureRmNEtworkInterfaceTapConfig cmdlet 추가

#### <a name="azurermrediscache"></a>AzureRM.RedisCache
* 모든 문자열을 Size 매개 변수로 진행되도록 허용 PSArgumentCompleter 팝업에 P5 추가

#### <a name="azurermresources"></a>AzureRM.Resources
* -Mode 매개 변수를 Set-AzureRmPolicyDefinition에 추가
* 사용자가 포함된 Origin 작업에서 Get-AzureRmProviderOperation commandlet 버그 수정

#### <a name="azurermsql"></a>AzureRM.Sql
* 일부 백업 cmdlet이 현재 azure 구독을 인식하지 않는 문제 해결

#### <a name="azurermstorage"></a>AzureRM.Storage
* 특정 위치의 스토리지 리소스 사용을 지원하고 글로벌 스토리지 리소스 사용 가져오기는 더 이상 사용되지 않는다는 경고 메시지를 추가합니다.
    - Get-AzureRmStorageUsage

#### <a name="azurermwebsites"></a>AzureRM.Websites
* 새 cmdlet Get-AzureRMWebAppContainerContinuousDeploymentUrl - 컨테이너 지속적인 배포 Webhook URL을 가져옵니다.
* 새 cmdlet New-AzureRMWebAppContainerPSSession 및 Enter-WebAppContainerPSSession -  windows 컨테이너 앱에 PowerShell 원격 세션을 시작합니다.

## <a name="690---september-2018"></a>6.9.0 - 2018년 9월
#### <a name="general"></a>일반
* AzureRM.SignalR이 AzureRM 롤업 모듈에 추가되었습니다.

#### <a name="azurermprofile"></a>AzureRM.Profile
* 스토리지 일반 코드에 대한 약간의 변경
* 전체 매개 변수 형식을 포함하도록 도움말 파일이 업데이트되었습니다.
* -ServicePrincipal을 필수가 아닌 것으로 ServicePrincipalCertificateWithSubscriptionId 매개변수 집합에서 변경 

#### <a name="azurestorage"></a>Azure.Storage
* OAuth를 사용하여 스토리지 컨텍스트를 만드는 것을 지원합니다. 
    - New-AzureStorageContext

#### <a name="azurermcdn"></a>AzureRM.Cdn
* Cdn 가격 책정 sku에서 Standard_Microsoft를 추가했습니다. 

#### <a name="azurermcompute"></a>AzureRM.Compute
* Keyvault 및 Storage에서 종속성을 일반 종속성으로 이동
* AEM cmdlet에 더 많은 가상 머신 크기에 대한 지원 추가
* PublicIPPrefix 매개 변수를 New-AzureRmVmssIpConfig에 추가
* Invoke-AzureRmVMRunCommand cmdelt에 ResourceId 매개 변수 추가
* Invoke-AzureRmVmssVMRunCommand cmdlet 추가

#### <a name="azurermdns"></a>AzureRM.Dns
* Dns 레코드를 만드는 동안 별칭 레코드에 대한 지원 추가

#### <a name="azurerminsights"></a>AzureRM.Insights
* #6833 및 #7102 문제 수정(진단 설정 영역)
    - 기본 이름, 즉 'service'에 진단 설정의 목록 생성 및 가져오는 동안에 문제가 있습니다.
    - 범주를 사용하는 진단 설정 만들기 문제
* 메트릭 시간 조직 매개 변수에 대한 사용 중단 메시지 추가
    - Timegrains 매개 변수는 여전히 받아들여지고 있습니다(이것은 호환성이 손상되는 변경이 아닙니다). 그러나 PT1M만 유효하므로 백엔드에서 무시됩니다.

#### <a name="azurermnetwork"></a>AzureRM.Network
* LoadBalancer cmdlet에 대한 변경
  - LoadBalancerInboundNatPoolConfig: IdleTimeoutInMinutes, EnableFloatingIp 및 EnableTcpReset 매개 변수 추가
  - LoadBalancerInboundNatRuleConfig: EnableTcpReset 매개 변수 추가
  - LoadBalancerRuleConfig: EnableTcpReset 매개 변수 추가
  - LoadBalancerProbeConfig: 매개 변수 프로토콜에 대해 "Https" 값에 대한 지원 추가
* 새 LoadBalancer의 하위 리소스OutboundRule에 대한 새 명령이 추가됨
  - Add-AzureRmLoadBalancerOutboundRuleConfig
  - Get-AzureRmLoadBalancerOutboundRuleConfig
  - New-AzureRmLoadBalancerOutboundRuleConfig
  - Set-AzureRmLoadBalancerOutboundRuleConfig
  - Remove-AzureRmLoadBalancerOutboundRuleConfig
* PSNetworkInterface에 대한 새 HostedWorkloads 속성 추가
* 기능에 대한 새 cmdlet 추가: ARM을 통한 Azure Firewall
  - Get-AzureRmFirewall 추가
  - Set-AzureRmFirewall 추가
  - New-AzureRmFirewall 추가
  - Remove-AzureRmFirewall 추가
  - New-AzureRmFirewallApplicationRuleCollection 추가
  - New-AzureRmFirewallApplicationRule 추가
  - New-AzureRmFirewallNatRuleCollection 추가
  - New-AzureRmFirewallNatRule 추가
  - New-AzureRmFirewallNetworkRuleCollection 추가
  - New-AzureRmFirewallNetworkRule 추가
* Application Gateway에서 신뢰할 수 있는 루트 인증서 및 크기 자동 조정 구성에 대한 지원이 추가되었습니다.
  - 추가된 새 cmdlet은 다음과 같습니다.
      - Add-AzureRmApplicationGatewayTrustedRootCertificate
      - Get-AzureRmApplicationGatewayTrustedRootCertificate
      - New-AzureRmApplicationGatewayTrustedRootCertificate
      - Remove-AzureRmApplicationGatewayTrustedRootCertificate
      - Set-AzureRmApplicationGatewayTrustedRootCertificate
      - Get-AzureRmApplicationGatewayAutoscaleConfiguration
      - New-AzureRmApplicationGatewayAutoscaleConfiguration
      - Remove-AzureRmApplicationGatewayAutoscaleConfiguration
      - Set-AzureRmApplicationGatewayAutoscaleConfiguration
  - 옵션 매개 변수를 사용하도록 업데이트된 Cmdlet-TrustedRootCertificate
      - New-AzureRmApplicationGateway
      - Set-AzureRmApplicationGateway
      - New-AzureRmApplicationGatewayBackendHttpSetting
      - Set-AzureRmApplicationGatewayBackendHttpSetting
  - 옵션 매개 변수를 사용하도록 업데이트된 Cmdlet-AutoscaleConfiguration
      - New-AzureRmApplicationGateway
      - Set-AzureRmApplicationGateway
* 인터페이스 엔드포인트 Get-AzureInterfaceEndpoint에 대한 cmdlet 추가
* 서브넷에서 여러 주소 접두사에 대한 지원이 추가되었습니다. 다음 Cmdlet이 업데이트 되었습니다.
  - New-AzureRmVirtualNetworkSubnetConfig
  - Set-AzureRmVirtualNetworkSubnetConfig
  - Add-AzureRmVirtualNetworkSubnetConfig
  - Get-AzureRmVirtualNetworkSubnetConfig
  - Add-AzureRmApplicationGatewayAuthenticationCertificate
  - Add-AzureRmApplicationGatewayFrontendIPConfig
  - New-AzureRmApplicationGatewayFrontendIPConfig
  - Set-AzureRmApplicationGatewayFrontendIPConfig
  - Add-AzureRmApplicationGatewayIPConfiguration
  - New-AzureRmApplicationGatewayIPConfiguration
  - Set-AzureRmApplicationGatewayIPConfiguration
  - Add-AzureRmNetworkInterfaceIpConfig
  - New-AzureRmNetworkInterfaceIpConfig  - Set-AzureRmNetworkInterfaceIpConfig
  - New-AzureRmVirtualNetworkGatewayIpConfig
  - Add-AzureRmVirtualNetworkGatewayIpConfig
  - Set-AzureRmLoadBalancerFrontendIpConfig
  - Add-AzureRmLoadBalancerFrontendIpConfig
  - New-AzureRmLoadBalancerFrontendIpConfig
  - New-AzureRmNetworkInterface
* 서브넷 위임에 대한 cmdlet을 추가합니다.
  - New-AzureRmDelegation: 서브넷에 추가할 수 있는 새 위임을 만듭니다.
  - Remove-AzureRmDelegation: 서브넷에서 가져와서 해당 서브넷에서 제공된 위임 이름을 제거합니다.
  - Add-AzureRmDelegation: 서브넷에서 사용 및 제공된 서비스 이름을 해당 서브넷에 대한 위임으로 추가합니다
  - Get-AzureRmDelegation
  - Get-AzureRmAvailableServiceDelegations

#### <a name="azurermrecoveryservicessiterecovery"></a>AzureRM.RecoveryServices.SiteRecovery
* 관리되는 관리 디스크에 대한 지원

#### <a name="azurermrediscache"></a>AzureRM.RedisCache
* 인사이트 종속성이 업데이트되었습니다.

#### <a name="azurermresources"></a>AzureRM.Resources
* New-AzureRmResourceGroupDeployment를 RollbackAction 새 매개 변수를 사용하여 업데이트
    - 새 매개 변수를 사용하여 OnErrorDeployment에 대한 지원을 추가합니다.
* 정책 할당에서 관리되는 ID를 지원합니다.
* 'New-AzureRmPolicyAssignment'를 사용하여 정책을 할당할 때 기본값이 있는 매개 변수는 더 이상 필요하지 않습니다.
* 정책 별칭을 검색하기 위한 새 cmdlet Get-AzureRmPolicyAlias 추가

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* #7161 문제 해결

#### <a name="azurermsignalr"></a>AzureRM.SignalR
* SKU 이름을 Free_F1 및 Standard_S1로 업데이트
* 버전 필드를 PSSignalRResource 개체에 추가하고 연결 문자열을 PSSignalRKeys개체에 추가합니다.

#### <a name="azurermstorage"></a>AzureRM.Storage
* AzureRm.Storage에서 불변성 정책 지원 
    - Remove-AzureRmStorageAccountNetworkRule
    - Get-AzureRmStorageContainer
    - Update-AzureRmStorageContainer
    - New-AzureRmStorageContainer
    - Remove-AzureRmStorageContainer
    - Add-AzureRmStorageContainerLegalHold
    - Remove-AzureRmStorageContainerLegalHold
    - Set-AzureRmStorageContainerImmutabilityPolicy
    - Get-AzureRmStorageContainerImmutabilityPolicy
    - Remove-AzureRmStorageContainerImmutabilityPolicy
    - Lock-AzureRmStorageContainerImmutabilityPolicy

#### <a name="azurermwebsites"></a>AzureRM.Websites
* 두 개의 새로운 cmdlet이 추가되었습니다. Get-AzureRmDeletedWebApp 및 Restore-AzureRmDeletedWebApp
* New-AzureRmAppServicePlan -HyperV 스위치가 창 컨테이너가 있는 앱 서비스 계획 작성용으로 추가되었습니다.
* New-AzureRmWebApp/New-AzureRmWebAppSlot/Set-AzureRmWebApp/ Set-AzureRmWebAppSlot - Windows 컨테이너 앱을 만들고 관리하기 위한 새 매개 변수(-ContainerRegistryUser 문자열 -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment)가 추가되었습니다.

## <a name="681---august-2018"></a>6.8.1 - 2018년 8월
#### <a name="general"></a>일반
* 기본 리소스 그룹이 설정되지 않는 문제를 해결했습니다.
* 공용 런타임 어셈블리가 업데이트됨

#### <a name="azurermapimanagement"></a>AzureRM.ApiManagement
* 기본 리소스 그룹이 설정되지 않는 문제를 해결했습니다.
* 문제 https://github.com/Azure/azure-powershell/issues/6603 해결
    - Import-AzureRmApiManagementApi 및 *-AzureRmApiManagementCertificate cmdlet은 이제 상대 경로를 처리합니다.
* 문제 https://github.com/Azure/azure-powershell/issues/6879 해결
    - CertificateInformation은 Set-AzureRmApiManagement cmdlet이 제대로 작동 하게 하는 설정 가능한 속성입니다. 4\.0.4-preview nuget으로 업그레이드하여 해결됨
* 문제 https://github.com/Azure/azure-powershell/issues/6853 해결
    - 제품에서 이름별 검색에 대해 Odata 필터가 수정됨
* 문제 https://github.com/Azure/azure-powershell/issues/6814 해결
    - API에서 이름별 검색에 대해 Odata 필터가 수정됨
* AzureMonitor 로거에 대한 지원 추가


#### <a name="azurermcompute"></a>AzureRM.Compute
* 오류 출력에 대상이 없는 문제를 해결했습니다.
* 관리 디스크를 사용하는 VM에 대한 스토리지 계정 유형 문제 해결
* 기본 리소스 그룹이 설정되지 않는 문제를 해결했습니다.
* 예를 들어 Azure 중국과 같이, 다른 환경에 대한 AEM 확장 cmdlet 수정

#### <a name="azurermnetwork"></a>AzureRM.Network
* 기본 cmdlet 출력 표시를 테이블 뷰로 변경

#### <a name="azurermpowerbiembedded"></a>AzureRM.PowerBIEmbedded
* 일시 중지된 용량을 확장하려고 할 때 Update-AzureRmPowerBIEmbeddedCapacity 실패 수정


#### <a name="azurermresources"></a>AzureRM.Resources
* MarketPlace에서 관리되는 애플리케이션 생성 시의 문제 해결.

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* 해결된 문제
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a>AzureRM.TrafficManager
* 다중값 라우팅 메서드에 대한 지원이 추가됨
    - 다중값 라우팅에 대한 새 매개 변수 'MaxReturn'
* 서브넷 라우팅 메서드에 대한 지원이 추가됨
    - 엔드포인트의 IP 주소 범위(서브넷)에 대한 지원
* 프로필 내 사용자 지정 헤더에 대한 지원이 추가됨
* 프로필 내 예상 상태 코드 범위에 대한 지원이 추가됨
* 엔드포인트 내 사용자 지정 헤더에 대한 지원이 추가됨

## <a name="680---august-2018"></a>6.8.0 - 2018년 8월
#### <a name="general"></a>일반
* 기본 리소스 그룹이 설정되지 않는 문제를 해결했습니다.

#### <a name="azurermprofile"></a>AzureRM.Profile
* Connect-AzureRmAccount 중에 반환된 토큰에 만료 속성 추가

#### <a name="azurermcompute"></a>AzureRM.Compute
* 오류 출력에 대상이 없는 문제를 해결했습니다.
* 관리 디스크를 사용하는 VM에 대한 스토리지 계정 유형 문제 해결
* 예를 들어 Azure 중국과 같이, 다른 환경에 대한 AEM 확장 cmdlet 수정

#### <a name="azurermiothub"></a>AzureRM.IotHub
* New-AzureRmIotHubExportDevices 및 New-AzureRmIotHubImportDevices에 대한 예제를 수정

#### <a name="azurermnetwork"></a>AzureRM.Network
* 기본 모델 표시를 테이블 뷰로 변경

#### <a name="azurermpowerbiembedded"></a>AzureRM.PowerBIEmbedded
* 일시 중지된 용량을 확장하려고 할 때 Update-AzureRmPowerBIEmbeddedCapacity 실패 수정

#### <a name="azurermresources"></a>AzureRM.Resources
* MarketPlace에서 관리되는 애플리케이션 생성 시의 문제 해결.

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* 문제 해결
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a>AzureRM.TrafficManager
* 다중값 라우팅 메서드에 대한 지원
    - 다중값 라우팅에 대한 새 매개 변수 'MaxReturn'
* 서브넷 라우팅 메서드에 대한 지원
    - 엔드포인트의 IP 주소 범위(서브넷)에 대한 지원
* 프로필 내 사용자 지정 헤더에 대한 지원
* 프로필 내 예상 상태 코드 범위에 대한 지원
* 엔드포인트 내 사용자 지정 헤더에 대한 지원

#### <a name="azurermwebsites"></a>AzureRM.Websites
* 기본 리소스 그룹이 잘못 설정되는 문제를 해결했습니다.

## <a name="670---august-2018"></a>6.7.0 - 2018년 8월
#### <a name="azurermprofile"></a>AzureRM.Profile
* 최신 버전의 Azure ClientRuntime으로 업데이트됨
* 충돌을 방지하려면 기본 컨텍스트 이름으로 사용자 ID를 추가합니다.
    - https://github.com/Azure/azure-powershell/issues/6489
* #6398 컨텍스트를 선택할 때 문제를 발생시킨 Clear-AzureRmContext 문제 해결
* 'Connect-AzureRmAccount'에 대한 '-TenantId' 매개 변수에 전달할 테넌트 도메인을 사용하도록 설정
    - https://github.com/Azure/azure-powershell/issues/3974
    - https://github.com/Azure/azure-powershell/issues/6709

#### <a name="azurestorage"></a>Azure.Storage
* Azure 파일 공유 할당량에 대한 5TB 제한 제거
* Set-AzureStorageShareQuota

#### <a name="azurermanalysisservices"></a>AzureRM.AnalysisServices
* 최신 버전의 Azure ClientRuntime으로 업데이트됨

#### <a name="azureanalysisservices"></a>Azure.AnalysisServices
* 최신 버전의 Azure ClientRuntime으로 업데이트됨

#### <a name="azurermapimanagement"></a>AzureRM.ApiManagement
* 최신 버전의 Azure ClientRuntime으로 업데이트됨

#### <a name="azurermapplicationinsights"></a>AzureRM.ApplicationInsights
* 최신 버전의 Azure ClientRuntime으로 업데이트됨

#### <a name="azurermautomation"></a>AzureRM.Automation
* 최신 버전의 Azure ClientRuntime으로 업데이트됨

#### <a name="azurermbackup"></a>AzureRM.Backup
* 최신 버전의 Azure ClientRuntime으로 업데이트됨

#### <a name="azurermbatch"></a>AzureRM.Backup
* 최신 버전의 Azure ClientRuntime으로 업데이트됨

#### <a name="azurermbilling"></a>AzureRM.Billing
* 최신 버전의 Azure ClientRuntime으로 업데이트됨

#### <a name="azurermcdn"></a>AzureRM.Cdn
* 최신 버전의 Azure ClientRuntime으로 업데이트됨

#### <a name="azurermcognitiveservices"></a>AzureRM.CognitiveServices
* 최신 버전의 Azure ClientRuntime으로 업데이트됨

#### <a name="azurermcompute"></a>AzureRM.Compute
* 최신 버전의 Azure ClientRuntime으로 업데이트됨
* New-AzureRmVmssConfig에 EvictionPolicy 매개 변수를 추가
* 지정된 위치가 없는 경우에 New-AzureRmVm의 DiskFileParameterSet 내의 기본 위치를 사용합니다.
* Save-AzureRmVMImage에서 매개 변수 설명 수정
* 특정 singlepass 관련 시나리오에 대해 Get-AzureRmVMDiskEncryptionStatus cmdlet 수정

#### <a name="azurermconsumption"></a>AzureRM.Consumption
* 최신 버전의 Azure ClientRuntime으로 업데이트됨

#### <a name="azurermcontainerinstance"></a>AzureRM.ContainerInstance
* 최신 버전의 Azure ClientRuntime으로 업데이트됨

#### <a name="azurermcontainerregistry"></a>AzureRM.ContainerRegistry
* 최신 버전의 Azure ClientRuntime으로 업데이트됨

#### <a name="azurermdatafactories"></a>AzureRM.DataFactories
* 최신 버전의 Azure ClientRuntime으로 업데이트됨

#### <a name="azurermdatafactoryv2"></a>AzureRM.DataFactoryV2
* 최신 버전의 Azure ClientRuntime으로 업데이트됨

#### <a name="azurermdatalakeanalytics"></a>AzureRM.DataLakeAnalytics
* 최신 버전의 Azure ClientRuntime으로 업데이트됨

#### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* DebugPreference가 powershell 명령줄에서 설정된 경우 디버깅 수정
* Set-AzureRmDataLakeStoreItemAcl에 대한 예제 업데이트
* 최신 버전의 Azure ClientRuntime으로 업데이트됨
* Set-AzureRmDataLakeStoreItemAclEntry에 대한 예제 업데이트

#### <a name="azurermdevtestlabs"></a>AzureRM.DevTestLabs
* 최신 버전의 Azure ClientRuntime으로 업데이트됨

#### <a name="azurermdns"></a>AzureRM.Dns
* 최신 버전의 Azure ClientRuntime으로 업데이트됨

#### <a name="azurermeventgrid"></a>AzureRM.EventGrid
* 최신 버전의 Azure ClientRuntime으로 업데이트됨

#### <a name="azurermeventhub"></a>AzureRM.EventHub
* 최신 버전의 Azure ClientRuntime으로 업데이트됨

#### <a name="azurermhdinsight"></a>AzureRM.HDInsight
* 최신 버전의 Azure ClientRuntime으로 업데이트됨

#### <a name="azurerminsights"></a>AzureRM.Insights
* 최신 버전의 Azure ClientRuntime으로 업데이트됨

#### <a name="azurermiothub"></a>AzureRM.IotHub
* 최신 버전의 Azure ClientRuntime으로 업데이트됨

#### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* 최신 버전의 Azure ClientRuntime으로 업데이트됨

#### <a name="azurermlogicapp"></a>AzureRM.LogicApp
* 최신 버전의 Azure ClientRuntime으로 업데이트됨

#### <a name="azurermmachinelearning"></a>AzureRM.MachineLearning
* 최신 버전의 Azure ClientRuntime으로 업데이트됨

#### <a name="azurermmachinelearningcompute"></a>AzureRM.MachineLearningCompute
* 최신 버전의 Azure ClientRuntime으로 업데이트됨

#### <a name="azurermmarketplaceordering"></a>AzureRM.MarketplaceOrdering
* 최신 버전의 Azure ClientRuntime으로 업데이트됨

#### <a name="azurermmedia"></a>AzureRM.Media
* 최신 버전의 Azure ClientRuntime으로 업데이트됨

#### <a name="azurermnetwork"></a>AzureRM.Network
* Set-AzureRmLocalNetworkGateway에 대한 예제가 추가됨
* Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey, New-AzureRmVirtualNetworkGatewayConnection에 대한 예제 및 설명 추가
* Remove-AzureRmVirtualNetworkGatewayIpConfig 및 Reset-AzureRmVirtualNetworkGateway에 대한 예제 추가
* Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey에 대한 예제 추가
* Set-AzureRmVirtualNetworkGatewayConnectionSharedKey에 대한 예제 추가
* Set-AzureRmVirtualNetworkGatewayConnection에 대한 예제 추가
* 최신 코드 생성기를 사용하여 ApplicationSecurityGroup, RouteTable 및 Usage에 대한 cmdlet을 다시 생성함
* Exitc 하지 않는 서브넷을 얻으려고 할 때의 Get-AzureRmVirtualNetworkSubnetConfig에 대한 오류 메시지를 설명

#### <a name="azurermnotificationhubs"></a>AzureRM.NotificationHubs
* 최신 버전의 Azure ClientRuntime으로 업데이트됨

#### <a name="azurermoperationalinsights"></a>AzureRM.OperationalInsights
* 최신 버전의 Azure ClientRuntime으로 업데이트됨

#### <a name="azurermpolicyinsights"></a>AzureRM.PolicyInsights
* 최신 버전의 Azure ClientRuntime으로 업데이트됨

#### <a name="azurermpowerbiembedded"></a>AzureRM.PowerBIEmbedded
* 최신 버전의 Azure ClientRuntime으로 업데이트됨

#### <a name="azurermrecoveryservices"></a>AzureRM.RecoveryServices
* 최신 버전의 Azure ClientRuntime으로 업데이트됨

#### <a name="azurermrecoveryservicesbackup"></a>AzureRM.RecoveryServices.Backup
* Get-AzureRmRecoveryServicesBackItem cmdlet에 정책 필터 추가 해당 명령은 지정된 정책 ID에 의해 보호되는 백업 항목의 목록을 반환합니다.
* Microsoft.Azure.Management.RecoveryServices.Backup을 버전 3.0.0-preview로 업데이트함
* 최신 버전의 Azure ClientRuntime으로 업데이트됨
* Restore-AzureRmRecoveryServicesBackupItem에 TargetResourceGroupName 매개 변수 추가 관리 디스크가 복원될 리소스 그룹 관리 디스크가 있는 VM의 백업에 적용 가능

#### <a name="azurermrecoveryservicessiterecovery"></a>AzureRM.RecoveryServices.SiteRecovery
* 최신 버전의 Azure ClientRuntime으로 업데이트됨

#### <a name="azurermrediscache"></a>AzureRM.RedisCache
* 최신 버전의 Azure ClientRuntime으로 업데이트됨

#### <a name="azurermrelay"></a>AzureRM.Relay
* 최신 버전의 Azure ClientRuntime으로 업데이트됨

#### <a name="azurermresources"></a>AzureRM.Resources
* 구독 범위에서 템플릿 배포를 지원합니다. 새 cmdlet 추가:
    - New-AzureRmDeployment
    - Get-AzureRmDeployment
    - Test-AzureRmDeployment
    - Remove-AzureRmDeployment
    - Stop-AzureRmDeployment
    - Save-AzureRmDeploymentTemplate
    - Get-AzureRmDeploymentOperation
* Set-AzureRmResource에 컨텍스트를 전달할 때 오류가 발생하는 문제 해결
    - https://github.com/Azure/azure-powershell/issues/5705
* New-AzureRmResourceGroupDeployment의 예제 수정
* 최신 버전의 Azure ClientRuntime으로 업데이트됨

#### <a name="azurermscheduler"></a>AzureRM.Scheduler
* 최신 버전의 Azure ClientRuntime으로 업데이트됨

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* 최신 버전의 Azure ClientRuntime으로 업데이트됨

#### <a name="azurermservicefabric"></a>AzureRM.ServiceFabric
* 최신 버전의 Azure ClientRuntime으로 업데이트됨

#### <a name="azurermsql"></a>AzureRM.Sql
* 최신 버전의 Azure ClientRuntime으로 업데이트됨

#### <a name="azurermstorage"></a>AzureRM.Storage
* 최신 버전의 Azure ClientRuntime으로 업데이트됨

#### <a name="azurermstreamanalytics"></a>AzureRM.StreamAnalytics
* 최신 버전의 Azure ClientRuntime으로 업데이트됨

#### <a name="azurermtags"></a>AzureRM.Tags
* 최신 버전의 Azure ClientRuntime으로 업데이트됨

#### <a name="azurermtrafficmanager"></a>AzureRM.TrafficManager
* 최신 버전의 Azure ClientRuntime으로 업데이트됨

#### <a name="azurermusageaggregates"></a>AzureRM.UsageAggregates
* 최신 버전의 Azure ClientRuntime으로 업데이트됨

#### <a name="azurermwebsites"></a>AzureRM.Websites
* 최신 버전의 Azure ClientRuntime으로 업데이트됨

## <a name="660---july-2018"></a>6.6.0 - 2018년 7월
#### <a name="general"></a>일반
* 전체 매개 변수 형식 및 올바른 입/출력 형식을 포함하도록 모든 도움말 파일을 업데이트했습니다.

#### <a name="azurermprofile"></a>AzureRM.Profile
* Common.Strategy 라이브러리가 리소스에 대한 현재 구성이 대상 리소스와 호환되는지 유효성을 검사할 수 있도록 업데이트했습니다.
* Common.Storage에 ps1xml 형식 추가

#### <a name="azurestorage"></a>Azure.Storage
* DefaultProfile에서 스토리지 컨텍스트를 가져오기 위한 지원 추가
* Ps1XmlAttribute를 cmdlet 출력 형식 속성에 추가

#### <a name="azurermapimanagement"></a>AzureRM.ApiManagement
* 문제 https://github.com/Azure/azure-powershell/issues/6370 해결
    - PsApiManagementApi를 ApiContract로 좌표 이동하도록 Automapper 버그가 수정됨
* 문제 https://github.com/Azure/azure-powershell/issues/6515 해결
    - 인코딩 형식을 사용하여 오버로드하지 않도록 File.Save 버그가 수정됨
* 문제 https://github.com/Azure/azure-powershell/issues/6560 해결
    - apiId에서 패턴 예외를 수정하는 4.0.3 Nuget 버전으로 업그레이드됨

#### <a name="azurermcompute"></a>AzureRM.Compute
* PremiumLRS 스토리지 계정 형식 이름 바꾸기로 인해 New-AzureRmVm에서 DiskFileParameterSet를 사용하여 vm 생성 시 실패하는 문제를 해결합니다.
* Invoke-AzureRmVMRunCommand cmdlet 수정
* Get-AzureRmAvailabilitySet를 업데이트하여 구독에서 모든 가용성 집합 리스트를 사용하도록 합니다.  (ResouceGroupName 매개 변수는 이제 선택적 요소입니다.)
* vm 선별에 가속화된 네트워크를 사용하도록 'New-AzureRmVm'의 SimpleParameterSet를 업데이트합니다.
* New-AzureRmVmss 간단 매개 변수가 사용자 지정 LB가 이미 존재할 때 vms 생성에 실패하도록 설정하여 업데이트합니다.
* New-AzureRmDisk에 대한 예제 업데이트
* 'New-AzureRmVM'에 대한 예제 추가
* Set-AzureRmVMOSDisk에 대한 설명 업데이트
* Set-AzureRmVMBginfoExtension 맞춤법 및 접두사를 수정하도록 예제 1을 업데이트합니다. 

#### <a name="azurermdatafactoryv2"></a>AzureRM.DataFactoryV2
* ADF.Net SDK 버전을 1.1.0으로 업데이트했습니다.
* 데이터 팩터리를 공유하는 자체 호스팅된 통합 런타임을 지원합니다.
     - 새 매개 변수 -SharedIntegrationRuntimeResourceId를 Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet에 추가.
     - 새로운 선택적 매개 변수 -LinkedDataFactoryName을 Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet에 추가.

#### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* DataPlane SDK(Microsoft.Azure.DataLake.Store) 버전을 1.1.9로 업데이트

#### <a name="azurermeventhub"></a>AzureRM.EventHub
* cmdlet 제거에서 InputObject 및 ResourceId에 대한 파이핑이 업데이트됨

#### <a name="azurerminsights"></a>AzureRM.Insights
* 도움말 파일에서 OutputType 서식 지정 수정
* Microsoft.Azure.Management.Monitor SDK 0.19.1-preview를 사용

#### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* Set-AzureRmKeyVaultAccessPolicy 내 파이핑 문제 해결

#### <a name="azurermnetwork"></a>AzureRM.Network
* LoadBalancerInboundNatPoolConfig cmdlet에 대한 예제가 추가되었습니다.

#### <a name="azurermresources"></a>AzureRM.Resources
* 'Get-AzureRmResource'에 대한 태그 이름 및 값을 제공할 때의 문제 해결
    - https://github.com/Azure/azure-powershell/issues/6765
* 'Set-AzureRmResource'를 사용하여 파이핑 시나리오 해결

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* cmdlet 제거에서 InputObject 및 ResourceId에 대한 파이핑이 업데이트됨
* 몇 가지 문제 해결
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a>AzureRM.Sql
* 다음 cmdlet 사용하여 서버 Advanced Threat Protection 지원을 추가합니다.
    - Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy
* 다음 cmdlet을 사용하여 취약성 평가 지원을 추가합니다.
    - Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings
    - Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline
    - Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan
* Remove-AzureRmSqlServerFirewallRule의 예제 수정
* Get-AzureSqlSyncGroupLog에서 미국이 아닌 문화권에서 날짜/시간을 올바르지 않게 다루는 문제 해결

#### <a name="azurermstorage"></a>AzureRM.Storage
* Ps1XmlAttribute를 cmdlet 출력 형식 속성에 추가
* StorageAccount cmdlet 출력을 테이블 뷰로 표시
    - Get-AzureRmStorageAccount
    - New-AzureRmStorageAccount
    - Set-AzureRmStorageAccount

#### <a name="azurermtags"></a>AzureRM.Tags
* 태그 cmdlet 도움말에서 잘못된 문을 제거합니다
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a>6.5.0 - 2018년 7월
#### <a name="azurermprofile"></a>AzureRM.Profile
* 'Get-AzureRmContextAutosaveSetting'에 대한 도움말이 업데이트됨

#### <a name="azurestorage"></a>Azure.Storage
* 쓰기 전용 SaS 토큰을 사용하는 Blob 또는 파일 업로드 지원
* Set-AzureStorageBlobContent
* Set-AzureStorageFileContent

#### <a name="azurermanalysisservices"></a>AzureRM.AnalysisServices
* 필수 속성 ResourceGroupName을 AS에 추가

#### <a name="azurermautomation"></a>AzureRM.Automation
* 도움말을 업데이트하고 'New-AzureRMAutomationSchedule'에 대한 예제 추가

#### <a name="azurermcompute"></a>AzureRM.Compute
* -Tag 매개 변수를 Update/New-AzureRmAvailabilitySet에 추가
* ‘Add-AzureRmVmssExtension’에 대한 예제 추가
* ‘Remove-AzureRmVmssExtension’에 대한 예제 추가
* ‘Set-AzureRmVMAccessExtension’에 대한 도움말 업데이트
* 기본으로 SinglePlacementGroup을 false로 설정하고 단일 배치 그룹에 VMSS를 만들 수 있는 스위치 매개 변수 'SinglePlacementGroup'을 추가하도록 New-AzureRmVmss에 대한 SimpleParameterSet을 업데이트합니다.

#### <a name="azurermeventhub"></a>AzureRM.EventHub
* PSEventHubDRConfigurationAttributes 클래스에 읽기 전용 속성 'PendingReplicationOperationsCount'를 추가하여 복제가 진행되는 동안 보류 중인 복제 작업 수를 제공

#### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* Set-AzureRmKeyVaultAccessPolicy에 대한 오류 메시지 업데이트

#### <a name="azurermlogicapp"></a>AzureRM.LogicApp
* New-AzureRmLogicApp에서 "매개 변수 집합을 확인할 수 없습니다" 오류 해결

#### <a name="azurermnetwork"></a>AzureRM.Network
* Set/Add-AzureRmVirtualNetworkPeering에 대한 여러 테넌트의 가상 네트워크에서 피어링을 사용하도록 설정
* Application Gateway에 대한 아래 cmdlet 업데이트
    - New-AzureRmApplicationGateway : EnableFIPS 플래그 및 영역 지원이 추가됨
    - New-AzureRmApplicationGatewaySku : 새 SKU Standard_v2 및 WAF_v2 추가
    - Set-AzureRmApplicationGatewaySku : 새 SKU Standard_v2 및 WAF_v2 추가
* 최신 생성기를 사용하여 RouteTable cmdlet을 재생성

#### <a name="azurermrelay"></a>AzureRM.Relay
* markdown 파일을 업데이트하여 예제에서 매개 변수 이름 문제에 대해 해결

#### <a name="azurermresources"></a>AzureRM.Resources
* Roledefinition 및 Roleassignment cmdlet을 업데이트
    - 페이징의 일부분으로 수행하는 추가 roledefinition 호출을 제거합니다.
* Get-AzureRmRoleAssignment cmdlet 수정
    - -ExpandPrincipalGroups 명령 매개 변수 기능 수정
* 'Get-AzureRmResource'에서 '-ResourceType' 매개 변수가 대/소문자를 구분하는 문제 해결

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* top 및 skip 매개 변수가 cmdlet 목록을 나열하도록 추가
* 표준을 프리미엄 네임스페이스 마이그레이션 cmdlet에 추가
    - Start-AzureRmServiceBusMigration
    - Get-AzureRmServiceBusMigration
    - Complete-AzureRmServiceBusMigration
    - Stop-AzureRmServiceBusMigration
    - Remove-AzureRmServiceBusMigration
* PSServiceBusDRConfigurationAttributes 클래스에 읽기 전용 속성 'PendingReplicationOperationsCount'를 추가하여 복제가 진행되는 동안 보류 중인 복제 작업 수를 제공

#### <a name="azurermservicefabric"></a>AzureRM.ServiceFabric
* ‘New-AzureRmServiceFabricCluster’에 대한 예제 업데이트

#### <a name="azurermsql"></a>AzureRM.Sql
* Management.Sql에 대한 새 cmdlet을 추가하여 고객이 TDE 인증서를 SQL Server 인스턴스 또는 Managed Instance에 추가할 수 있도록 허용
    - Add-AzureRmSqlServerTransparentDataEncryptionCertificate
    - Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate

#### <a name="azurermwebsites"></a>AzureRM.Websites
* `Set-AzureRmWebApp -AssignIdentity` 및 `Set-AzureRmWebAppSlot -AssignIdentity`가 false로 설정되면 사이트 개체에서 Identity 속성이 제거됩니다. 미리보기 태그도 제거됩니다.
* `Get-AzureRmWebAppMetrics`, `Get-AzureRmAppServicePlanMetrics` 예제가 업데이트됨
* `Set-AzureRmWebApp -PhpVersion`이 유효한 php 버전으로 해제 지원

## <a name="640---july-2018"></a>6.4.0 - 2018년 7월
#### <a name="general"></a>일반
* 대부분의 모듈에 대한 도움말 파일에서 OutputType 서식 지정 수정

#### <a name="azurermprofile"></a>AzureRM.Profile
* 기본 출력 형식에 추가된 Ps1Xml 특성

#### <a name="azurermcompute"></a>AzureRM.Compute
* VMSS에 대한 IP 태그 기능
    - 'New-AzureRmVmssIpTagConfig' cmdlet 추가
    - New-AzureRmVmssIpConfig에 IpTag 매개 변수가 추가됨
* VMSS에 대한 자동 OS 롤백 기능
    - New-AzureRmVmssConfig 및 Update-AzureRmVmss에 DisableAutoRollback 매개 변수가 추가됨
* Vmss에 대한 OS 업그레이드 기록 기능
    - Get-AzureRmVmss에 OSUpgradeHistory 스위치 매개 변수 추가

#### <a name="azurermdatalakeanalytics"></a>AzureRM.DataLakeAnalytics
* 다음 명령을 통해 카탈로그 액세스 제어 목록에 대한 지원을 추가합니다.
    - Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry
    - Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry
    - Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry

#### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl에 대한 취소 지원 및 진행률 추적 추가
* Export-AzureRmDataLakeStoreChildItemProperties에 대한 취소 지원 추가
* 재귀 작업을 수행하는 cmdlet에 대한 디버그 메시지 플러시 수정
* DataLake cmdlet의 테스트 위치 수정

#### <a name="azurermeventhub"></a>AzureRM.EventHub
* 목록 작업 cmdlet Get-AzureRmEventHub 및 Get-AzureRmEventHubConsumerGroup에 선택적 MaxCount 매개 변수 추가
* 새 EventHub 만드는 동안 하나 이상의 매개 변수가 필요한 New-AzureRmEventHub cmdlet 문제를 해결. 기본 매개 변수 집합을 제공.
* 선택적 매개 변수 -KeyValue를 New-AzureRmEventHubKey cmdlet에 추가 하여 사용자가 KeyValue를 제공할 수 있습니다.

#### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* Get-AzureRmKeyVault -Tag 실행 시 모든 리소스가 리턴되는 문제 해결

#### <a name="azurermnetwork"></a>AzureRM.Network
* 영역 중복 VirtualNetworkGateways에 대한 새 Sku를 노출합니다.
* 기능에 대한 새로운 명령이 추가됨: ARM을 통한 ExpressRoute 파트너 API
    - Get- AzureRmExpressRouteCrossConnection 추가
    - Set-AzureRmExpressRouteCrossConnection 추가
    - Add-AzureRmExpressRouteCrossConnectionPeering 추가
    - Get-AzureRmExpressRouteCrossConnectionPeering 추가
    - Remove-AzureRmExpressRouteCrossConnectionPeering 추가
    - Get-AzureRMExpressRouteCrossConnectionArpTable 추가
    - Get-AzureRMExpressRouteCrossConnectionRouteTable 추가
    - Get-AzureRMExpressRouteCrossConnectionRouteTableSummary 추가

#### <a name="azurermrecoveryservicesbackup"></a>AzureRM.RecoveryServices.Backup
* Get-AzureRmRecoveryServicesBackupStatus cmdlet 추가 이 cmdlet은 VM ID를 가져와서 VM이 구독에서 일부 자격 증명 모음으로 보호되는지 확인합니다. 이러한 자격 증명 모음이 존재하는 경우 cmdlet은 자격 증명 모음 세부 정보를 출력 합니다.

#### <a name="azurermresources"></a>AzureRM.Resources
* Get-AzureRmPolicyAssignment cmdlet을 다음과 같이 업데이트함.
    - 관리 그룹 수준에서 -Scope 값 리스팅에 대한 지원 추가
    - 관리 그룹 수준에서 -Scope 값을 사용하여 개별 할당값을 검색하는 것에 대한 지원 추가
    - 제어 매개 변수에 -Effective 및 -All 스위치 추가
* Get/New/Remove/Set-AzureRmPolicyDefinition cmdlet 업데이트
    - 지정된 관리 그룹에 작업을 적용할 -ManagementGroupName 매개 변수 추가
    - 지정된 구독에 작업을 적용할 -SubscriptionId 매개 변수 추가
* Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlet 업데이트
    - 지정된 관리 그룹에 작업을 적용할 -ManagementGroupName 매개 변수 추가
    - 지정된 구독에 작업을 적용할 -SubscriptionId 매개 변수 추가
* 'New-AzureRmResourceGroupDeployment'에서 'TemplateParameterObject'를 사용하는 경우 매개 변수에 KeyVault 비밀 참조 지원 추가
* 'New-AzureRmADAppCredential'에 대해 '-EndDate' 매개 변수가 무시되는 문제를 해결
    - https://github.com/Azure/azure-powershell/issues/6505
* 'Add-AzureRmADGroupMember'가 요청에 잘못된 URL을 사용하는 문제 해결
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* 선택적 매개 변수 -KeyValue를 New-AzureRmServiceBusKey cmdlet에 추가 하여 사용자가 KeyValue를 제공할 수 있습니다.

#### <a name="azurermsql"></a>AzureRM.Sql
* New-AzureRmSqlDatabaseRestorePoint 도움말에서 SQLDW에 대한 사용자 정의 복원 지점 명시
* 몇 가지 cmdlet에서-ComputeGeneration 매개 변수의 설명서 업데이트

## <a name="630---june-2018"></a>6.3.0 - 2018년 6월
#### <a name="azurermprofile"></a>AzureRM.Profile
* Enable-AzureRmContextAutoSave에 대한 오류 메시지 업데이트됨
* 이전 컨텍스트 없이 'Connect-AzureRmAccount' 실행 시 각 구독에 대한 컨텍스트 생성

#### <a name="azurestorage"></a>Azure.Storage
* 도움말 파일 내 -Permissions 매개 변수에 대한 추가 정보가 추가됨

#### <a name="azurermcompute"></a>AzureRM.Compute
* 'Get-AzureRmVmDiskEncryptionStatus'가 데이터 디스크가 없는 VM에 대해 관찰된 문제를 해결 
* Compute 클라이언트 라이브러리 버전을 업데이트하여 다음 cmdlet 수정
    - Grant-AzureRmDiskAccess
    - Grant-AzureRmSnapshotAccess
    - Save-AzureRmVMImage
* 다음 cmdlet이 '작업 ID' 및 '작업 상태'를 올바르게 표시하도록 수정:
    - Start-AzureRmVM
    - Stop-AzureRmVM
    - Restart-AzureRmVM
    - Set-AzureRmVM
    - Remove-AzuerRmVM
    - Set-AzureRmVmss
    - Start-AzureRmVmssRollingOSUpgrade
    - Stop-AzureRmVmssRollingUpgrade
    - Start-AzureRmVmss
    - Restart-AzureRmVmss
    - Stop-AzureRmVmss
    - Remove-AzureRmVmss
    - ConvertTo-AzureRmVMManagedDisk
    - Revoke-AzureRmSnapshotAccess
    - Remove-AzureRmSnapshot
    - Revoke-AzureRmDiskAccess
    - Remove-AzureRmDisk
    - Remove-AzureRmContainerService
    - Remove-AzureRmAvailabilitySet

#### <a name="azurermeventgrid"></a>AzureRM.EventGrid
* Update-AzureRmEventGridSubscription cmdlet의 SubjectBeginsWith/SubjectEndsWith에 대한 ValidateNotNullOrEmpty 유효성 검사 조건을 제거하여 필요에 따라 이러한 매개 변수를 빈 문자열로 변경할 수 있습니다.

#### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* Get-AzureRmKeyVault -Tag 실행 시 태그가 리턴되지 않는 문제 해결

#### <a name="azurermpolicyinsights"></a>AzureRM.PolicyInsights
* Policy Insights cmdlet의 공개 릴리스
    - API 버전 2018-04-04 사용
    - PolicyDefinitionReferenceId를 Get-AzureRmPolicyStateSummary의 결과 집합에 추가

#### <a name="azurermrecoveryservicesbackup"></a>AzureRM.RecoveryServices.Backup
* -Vault 매개 변수를 RecoveryServices.Backup cmdlet에 추가. 전달되는 경우 이는 Set-AzureRmRecoveryServicesContext cmdlet을 재정의함.

#### <a name="azurermsql"></a>AzureRM.Sql
* Get-AzureRmSqlDatabaseExpanded에 대한 도움말 파일의 예가 업데이트됨

#### <a name="azurermtrafficmanager"></a>AzureRM.TrafficManager
* Add-AzureRmTrafficManagerEndpointConfig에대한 도움말 파일이 업데이트됨

#### <a name="azurermwebsites"></a>AzureRM.Websites
* -AssignIdentity를 사용할 때 AppSetting을 덮어쓰지 않도록 'Set-AzureRmWebApp'이 업데이트됨
* 'New-AzureRmWebAppSlot'이 AppServicePlan을 옵션 매개변수로 사용하도록 업데이트됨

## <a name="621---june-2018"></a>6.2.1 - 2018년 6월
### <a name="azurermoperationalinsights"></a>AzureRM.OperationalInsights
* PSWorkspace 모델이 Network 형식을 매개 변수로 사용하도록 업데이트됨

## <a name="620---june-2018"></a>6.2.0 - 2018년 6월
#### <a name="azurermprofile"></a>AzureRM.Profile
* Newtonsoft.Json의 버전 10.0.3이 모듈 가져오기에 로드되지 않는 문제 해결

#### <a name="azurermcompute"></a>AzureRM.Compute
* VMSS VM 업데이트 기능
    - 'Update-AzureRmVmssVM' 및 'New-AzureRmVMDataDisk' cmdlets 추가
    - 데이터 디스크를 Vmss VM에 추가할 수 있도록 지원하기 위해 VirtualMachineScaleSetVM 매개변수를 'Add-AzureRmVMDataDisk' cmdlet에 추가하였습니다.

#### <a name="azurermdatafactoryv2"></a>AzureRM.DataFactoryV2
* ADF .Net SDK 버전이 다음 변경 내용이 포함된 0.8.0-preview로 업데이트되었습니다.
    - 팩터리 리포지토리 작업 구성 추가
    - QuickBooks LinkedService가 ConsumerKey 및 consumerSecret 속성을 노출하도록 업데이트됨
    - 여러 모델 유형을 SecretBase에서 개체로 업데이트함
    - Blob 이벤트 트리거 추가

### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* 예제 출력으로 설명서 업데이트

### <a name="azurermnetwork"></a>AzureRM.Network
* Network Watcher cmdlet에서 트래픽 분석 매개 변수를 사용가능하도록 설정

#### <a name="azurermresources"></a>AzureRM.Resources
* 'Get AzureRmResource'에서 반환된 'PSResource' 개체의 'Properties' 속성의 문제 해결

#### <a name="azurermscheduler"></a>AzureRM.Scheduler
* ServiceBusQueueJob 업데이트가 새 인증 값을 설정하지 않는 문제 해결

### <a name="azurermsql"></a>AzureRM.Sql
* 옵션 LicenseType 매개 변수를 사용하여 다음 cmdlet을 업데이트
    - New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase
    - New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool
    - New-AzureRmSqlDatabaseCopy
    - New-AzureRmSqlDatabaseSecondary
    - Restore-AzureRmSqlDatabase

#### <a name="azurermwebsites"></a>AzureRM.Websites
* 'New-AzureRMWebApp'이 전략 라이브러리의 공통 알고리즘을 사용하도록 업데이트 되었습니다.

## <a name="610---may-2018"></a>6.1.0 - 2018년 5월
#### <a name="azurermprofile"></a>AzureRM.Profile
* 'Clear-AzureRmContext'를 실행하면 이전 기본 컨텍스트의 이름으로 빈 컨텍스트가 유지되어 사용자가 이전 이름으로 새 컨텍스트를 만들지 못하게 되는 문제를 수정했습니다.

#### <a name="azurermanalysisservices"></a>AzureRM.AnalysisServices
* AS에서 게이트웨이가 작업을 연결하거나 연결 해제할 수 있습니다.

#### <a name="azurermapimanagement"></a>AzureRM.ApiManagement
* ApiVersions, ApiReleases 및 ApiRevisions에 대한 지원이 추가됨
* ServiceFabric 백 엔드에 대한 지원 추가됨
* Application Insights 로거에 대한 지원 추가됨
* '기본' SKU를 API Management 서비스의 유효한 SKU로 인식하는 지원 추가됨
* 프라이빗 CA가 발급한 인증서를 루트 또는 CA로 설치하는 지원 추가됨
* KeyVault 및 다중 프록시 호스트 이름을 통한 사용자 정의 SSL 인증서를 수락하는 지원 추가됨
* MSI ID에 대한 지원 추가됨
* URL을 통해 정책을 수용하기 위한 지원이 추가되었습니다. 참고: 다음 cmdlet은 이후 릴리스에서 사용되지 않을 예정입니다.
   - Import-AzureRmApiManagementHostnameCertificate
   - New-AzureRmApiManagementHostnameConfiguration
   - Set-AzureRmApiManagementHostnames
   - Update-AzureRmApiManagementDeployment

#### <a name="azurermbatch"></a>AzureRM.Backup
* 새 cmdlet Get AzureBatchPoolNodeCounts 릴리스
* 새 cmdlet Start-AzureBatchComputeNodeServiceLogUpload 릴리스

#### <a name="azurermconsumption"></a>AzureRM.Consumption
* Expand, ResourceGroup, InstanceName, InstanceId, Tags, Top on Cmdlet Get-AzureRmConsumptionUsageDetail 등 새 매개 변수 추가

#### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* Export-AzureRmDataLakeStoreChildItemProperties에 대한 예제 수정
* Set-AzureRmDataLakeStoreItemAclEntry에서 재귀 사례에 대한 null 매개 변수 예외 수정 
* Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry에 대한 도움말 파일 수정 

#### <a name="azurermnetwork"></a>AzureRM.Network
* 18.0.0-preview에서 19.0.0-preview로 네트워크 SDK 버전 업그레이드
* 프로토콜 구성을 만들기 위해 추가된 cmdlet
    - New-AzureRmNetworkWatcherProtocolConfiguration
* 기존 Express 경로 회로에 새 회로 연결을 추가하기 위해 추가된 cmdlet
    - Add-AzureRmExpressRouteCircuitConnectionConfig
* 기존 Express 경로 회로에서 회로 연결을 제거하기 위해 추가된 cmdlet
    - Remove-AzureRmExpressRouteCircuitConnectionConfig
* 회로 연결을 검색하기 위해 추가된 cmdlet
    - Get-AzureRmExpressRouteCircuitConnectionConfig

#### <a name="azurermservicefabric"></a>AzureRM.ServiceFabric
* 생성된 인증서로 고정 서버 인증 사용(문제 # 5998)

#### <a name="azurermsql"></a>AzureRM.Sql
* AuditActions 또는 AuditActionGroups를 제거할 수 있도록 업데이트된 감사 cmdlet
* 'Azure 복구 서비스 자격 증명 모음을 사용하여 장기 보존 정책을 구성하면 정책이 더 이상 지원되지 않습니다. 새로운 유연 보유 정책으로 요청을 제출하십시오.'라는 메시지와 함께 명령이 실패하는 새로운 유연 보유 정책을 설정할 때 Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy의 문제 수정
* Azure SQL Database/ElasticPool Creation/Update 관련 cmdlet을 모두 업데이트하여 규모 및 계층 관련 속성에 대한 SKU 속성을 지원하는 새 데이터베이스 API를 사용합니다.
* 업데이트된 cmdlet는 다음과 같습니다. 
    - New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase
    - New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool
    - New-AzureRmSqlDatabaseCopy
    - New-AzureRmSqlDatabaseSecondary
    - Restore-AzureRmSqlDatabase

#### <a name="azurermtrafficmanager"></a>AzureRM.TrafficManager
* -Name 매개 변수를 사용할 때 -ResourceGroupName 매개 변수가 필요하도록 'Get-AzureRmTrafficManagerProfile'에 대한 매개 변수를 업데이트합니다.
