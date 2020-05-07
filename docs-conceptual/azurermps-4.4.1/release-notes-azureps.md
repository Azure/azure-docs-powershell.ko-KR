---
title: Azure PowerShell 변경 로그 | Microsoft Docs
description: Azure PowerShell에 대한 최신 릴리스의 변경 내용입니다.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 07/26/2017
ms.openlocfilehash: 1491f3f23deb767b754a98b3fab616356daa71f3
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/05/2020
ms.locfileid: "67863777"
---
# <a name="release-notes"></a>릴리스 정보

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

Azure PowerShell에 대한 릴리스의 변경 내용 목록입니다.

## <a name="20170925---version-440"></a>2017.09.25 - 버전 4.4.0
* AnalysisServices
  * 읽기/쓰기 인스턴스에서 읽기 전용 인스턴스로 데이터베이스의 동기화를 허용하도록 새 데이터 평면 commandlet이 추가됨
    - Commandlet에 대한 도움말 파일이 포함됨
    - 메모리 내 테스트 및 시나리오 테스트(라이브만)가 추가됨
  * Add-AzureAsAccount commandlet의 버그가 수정됨
* Automation
  * 이전 릴리스에서 수정된 cmdlet에 대한 도움말 문서가 수정되었습니다.
  * DSC 노드 구성의 단계적 출시를 지원하는 4가지 새로운 cmdlet이 추가되었습니다.
    - Start-AzureRmAutomationDscNodeConfigurationDeployment
    - Stop-AzureRmAutomationDscNodeConfigurationDeployment
    - Get-AzureRmAutomationDscNodeConfigurationDeployment
    - Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule
* CognitiveServices
  * Cognitive Services Management SDK 버전 2.0.0과 통합합니다.
  * 이제 Get-AzureRmCognitiveServicesAccount가 페이징을 올바르게 지원할 수 있습니다.
* 컴퓨팅
  * 실행 명령 기능:
    - 새 cmdlet: ‘Invoke-AzureRmVMRunCommand’는 VM에서 실행 명령을 호출합니다.
    - 새 cmdlet: ‘Get-AzureRmVMRunCommandDocument’는 사용 가능한 실행 명령 문서를 표시합니다.
  * ‘StorageAccountType’ 매개 변수를 Set-AzureRmDataDisk에 추가합니다.
  * 가상 머신, VM 확장 집합 및 디스크에 대한 가용성 영역 지원
    - 새 매개 변수: ‘Zone’이 New-AzureRmVM, New-AzureRmVMConfig, New-AzureRmVmssConfig, New-AzureRmDiskConfig에 추가됩니다.
  * VM 확장 집합 롤링 업그레이드 기능:
    - 새 cmdlet: ‘Start-AzureRmVmssRollingOSUpgrade’는 VM 확장 집합의 OS 롤링 업그레이드를 호출합니다.
    - 새 cmdlet: ‘Set-AzureRmVmssRollingUpgradePolicy’는 VM 확장 집합 롤링 업그레이드에 대한 업그레이드 정책을 설정합니다.
    - 새 cmdlet: ‘Stop-AzureRmVmssRollingUpgrade’는 VM 확장 집합의 롤링 업그레이드를 취소합니다.
    - 새 cmdlet: ‘Get-AzureRmVmssRollingUpgrade’는 VM 확장 집합 롤링 업그레이드의 상태를 표시합니다.
  * AssignIdentity 스위치 매개 변수가 시스템 할당 ID에 도입됩니다.
    - 새 매개 변수: ‘AssignIdentity’가 New-AzureRmVMConfig, New-AzureRmVmssConfig 및 Update-AzureRmVM에 추가됩니다.
  * Vmss 디스크 암호화 기능:
    - 새 cmdlet: ‘Set-AzureRmVmssDiskEncryptionExtension’은 VM 확장 집합에서 디스크 암호화를 사용하도록 설정합니다.
    - 새 cmdlet: ‘Disable-AzureRmVmssDiskEncryption’은 VM 확장 집합에서 디스크 암호화를 사용하지 않도록 설정합니다.
    - 새 cmdlet: ‘Get-AzureRmVmssDiskEncryptionStatus’는 VM 확장 집합의 디스크 암호화 상태를 표시합니다.
    - 새 cmdlet: ‘Get-AzureRmVmssVMDiskEncryptionStatus’는 VM 확장 집합에서 VM의 디스크 암호화 상태를 표시합니다.
* ContainerInstance
  * Azure Container Registry에 대한 PowerShell cmdlet 추가
    - New-AzureRmContainerGroup
    - Get-AzureRmContainerGroup
    - Remove-AzureRmContainerGroup
    - Get-AzureRmContainerInstanceLog
* 자세한 정보
  * 새 cmdlet Disable-AzureRmActivityLogAlert
    - 기존 활동 로그 경고를 사용하지 않도록 설정하는 새 cmdlet.
    - 필요에 따라 태그가 이 cmdlet과 함께 설정됩니다.
  * 새 cmdlet Enable-AzureRmActivityLogAlert
    - 기존 활동 로그 경고를 사용하도록 설정하는 새 cmdlet.
    - 필요에 따라 태그가 이 cmdlet과 함께 설정됩니다.
  * 새 cmdlet Get-AzureRmActivityLogAlert
    - 하나 이상의 활동 로그 경고를 검색하는 새 cmdlet.
    - 경고를 이름, 리소스 그룹 또는 구독으로 검색할 수 있습니다.
  * 새 cmdlet New-AzureRmActionGroup
    - 메모리에 ActionGroup 개체를 만드는 새 cmdlet(관련 요청 없음)
  * 새 cmdlet New-AzureRmActivityLogAlertCondition
    - 메모리에 활동 로그 경고 리프 조건 개체를 만드는 새 cmdlet(관련 요청 없음)
  * 새 cmdlet Set-AzureRmActivityLogAlert
    - 활동 로그 경고를 만들거나 업데이트하는 새 cmdlet.
  * 새 cmdlet Remove-AzureRmActivityLogAlert
    - 하나의 활동 로그 경고를 제거하는 새 cmdlet.
  * 새 cmdlet Set-AzureRmActionGroup
    - 기존 작업 그룹을 업데이트하거나 새로 만드는 새 cmdlet.
  * 새 cmdlet Get-AzureRmActionGroup
    - 하나 이상의 작업 그룹을 검색하는 새 cmdlet.
    - 작업 그룹을 이름, 리소스 그룹 또는 구독으로 검색할 수 있습니다.
  * 새 cmdlet Remove-AzureRmActionGroup
    - 하나의 작업 그룹을 제거하는 새 cmdlet.
  * 새 cmdlet New-AzureRmActionGroupReceiver
    - 메모리에 새 작업 그룹 수신기를 만드는 새 cmdlet.
* KeyVault
  * KeyVault 인증서에 대한 일시 삭제를 지원하는 새/업데이트된 cmdlet
    * Get-AzureKeyVaultCertificate
    * Remove-AzureKeyVaultCertificate
    * Undo-AzureKeyVaultCertificateRemoval
* 네트워크
  * Virtual Network 서브넷에 엔드포인트 서비스 지원 추가됨
    - Add-AzureRmVirtualSubnetConfig 업데이트: 선택적 매개 변수 -ServiceEndpoint 추가됨
    - New-AzureRmVirtualSubnetConfig 업데이트: 선택적 매개 변수 -ServiceEndpoint 추가됨
    - Set-AzureRmVirtualSubnetConfig 업데이트: 선택적 매개 변수 -ServiceEndpoint 추가됨
  * 위치에서 사용할 수 있는 목록 엔드포인트 서비스에 cmdlet 추가됨
    - Get-AzureRmVirtualNetworkAvailableEndpointService
  * 다음 commandlet에 외부 radius 기반 P2S 인증을 구성하는 기능 추가됨
    - New-AzureVirtualNetworkGateway
    - Set-AzureVirtualNetworkGateway
    - Set-AzureRmVirtualNetworkGatewayVpnClientConfig
  * 외부 radius 기반 P2S에 대한 VpnProfiles의 생성을 허용하는 cmdlet 추가됨
    - New-AzureRmVpnClientConfiguration
    - Get-AzureRmVpnClientConfiguration
  * 공용 IP 주소 및 부하 분산 장치에 SKU 매개 변수 지원 추가됨
    - New-AzureRMLoadBalancer 업데이트: 선택적 매개 변수 -Sku 추가됨
    - New-AzureRMPublicIpAddress 업데이트: 선택적 매개 변수 -Sku 추가됨
  * 부하 분산 장치 규칙에 DisableOutboundSNAT 지원 추가됨
    - New-AzureRMLoadBalancerRuleConfig 업데이트: 선택적 매개 변수 DisableOutboundSNAT 추가됨
    - Add-AzureRMLoadBalancerRuleConfig 업데이트: 선택적 매개 변수 DisableOutboundSNAT 추가됨
    - Set-AzureRMLoadBalancerRuleConfig 업데이트: 선택적 매개 변수 DisableOutboundSNAT 추가됨
  * IkeV2 P2S에 대한 지원 추가됨
    - New-AzureRmVirtualNetworkGateway 업데이트: 선택적 매개 변수 -VpnClientProtocol 추가됨, 기본값은 [ “SSTP”, “IkeV2” ]
    - Set-AzureRmVirtualNetworkGateway 업데이트: 선택적 매개 변수 -VpnClientProtocol 추가됨
  * 네트워크 보안 규칙 및 효과적인 네트워크 보안 규칙의 다중값 규칙 지원 추가됨
    - Add-AzureRmNetworkSecurityRuleConfig 업데이트: 문자열 목록을 수락하는 SourcePortRange, DestinationPortRange, SourceAddressPrefix 매개 변수 업데이트
    - New-AzureRmNetworkSecurityRuleConfig 업데이트: 문자열 목록을 수락하는 SourcePortRange, DestinationPortRange, SourceAddressPrefix 매개 변수 업데이트
    - Set-AzureRmNetworkSecurityRuleConfig 업데이트: 문자열 목록을 수락하는 SourcePortRange, DestinationPortRange, SourceAddressPrefix 매개 변수 업데이트
    - Add-AzureRmNetworkSecurityRuleConfig 업데이트: 문자열 목록을 수락하는 SourcePortRange, DestinationPortRange, SourceAddressPrefix 매개 변수 업데이트
    - New-AzureRmNetworkSecurityGroup 업데이트: PSSecurityRule 개체에서 문자열 목록인 SourcePortRange, DestinationPortRange, SourceAddressPrefix 매개 변수를 수락하는 SecurityRules 매개 변수 업데이트
    - Get-AzureRmEffectiveNetworkSecurityGroup 업데이트: 매개 변수 TagMap 추가됨
    - Get-AzureRmEffectiveNetworkSecurityGroup 업데이트: 문자열 목록인 SourcePortRange, DestinationPortRange, SourceAddressPrefix 매개 변수와 반환된 PSEffectiveSecurityRule 개체가 업데이트되었습니다.
  * 가상 네트워크에 대한 DDoS 보호 지원 추가됨
    - New-AzureRmVirtualNetwork 업데이트: 스위치 매개 변수 EnableDDoSProtection 및 EnableVmProtection 추가됨
    - PSVirtualNetwork 개체에서 속성 EnableDDoSProtection 및 EnableVmProtection 추가됨
  * 항상 사용 가능한 내부 부하 분산 장치에 대한 지원 추가됨
    - Add-AzureRmLoadBalancerRuleConfig 업데이트: 프로토콜 매개 변수에 대한 허용되는 값으로 모두 추가됨
    - New-AzureRmLoadBalancerRuleConfig 업데이트: 프로토콜 매개 변수에 대한 허용되는 값으로 모두 추가됨
    - Set-AzureRmLoadBalancerRuleConfig 업데이트: 프로토콜 매개 변수에 대한 허용되는 값으로 모두 추가됨
  * 애플리케이션 보안 그룹에 대한 지원 추가됨
    - New-AzureRmApplicationSecurityGroup 추가됨
    - Get-AzureRmApplicationSecurityGroup 추가됨
    - Remove-AzureRmApplicationSecurityGroup 추가됨
    - New-AzureRmNetworkInterface 업데이트: 선택적 매개 변수 ApplicationSecurityGroup 및 ApplicationSecurityGroupId 추가됨
    - New-AzureRmNetworkInterfaceIpConfig 업데이트: 선택적 매개 변수 ApplicationSecurityGroup 및 ApplicationSecurityGroupId 추가됨
    - Add-AzureRmNetworkInterfaceIpConfig 업데이트: 선택적 매개 변수 ApplicationSecurityGroup 및 ApplicationSecurityGroupId 추가됨
    - Set-AzureRmNetworkInterfaceIpConfig 업데이트: 선택적 매개 변수 ApplicationSecurityGroup 및 ApplicationSecurityGroupId 추가됨
    - New-AzureRmNetworkSecurityRuleConfig 업데이트: 선택적 매개 변수 SourceApplicationSecurityGroup, SourceApplicationSecurityGroupId, DestinationApplicationSecurityGroup 및 DestinationApplicationSecurityGroupId 추가됨
    - Add-AzureRmNetworkSecurityRuleConfig 업데이트: 선택적 매개 변수 SourceApplicationSecurityGroup, SourceApplicationSecurityGroupId, DestinationApplicationSecurityGroup 및 DestinationApplicationSecurityGroupId 추가됨
    - Set-AzureRmNetworkSecurityRuleConfig 업데이트: 선택적 매개 변수 SourceApplicationSecurityGroup, SourceApplicationSecurityGroupId, DestinationApplicationSecurityGroup 및 DestinationApplicationSecurityGroupId 추가됨
  * VpnDeviceConfiguration 스크립트에 대한 새 명령 추가됨
    - Get-AzureRmVirtualNetworkGatewaySupportedVpnDevices
    - Get-AzureRmVirtualNetworkGatewayConnectionVpnDeviceConfigScript
* 프로필
  * AzureRm cmdlet에 대한 시작 작업 지원.
    * 모든 AzureRmCmdlet은 컨텍스트(컨텍스트 cmdlet의 출력)를 허용할 수 있는 -AzureRmContext 매개 변수를 추가합니다.
      - 컨텍스트 지속성을 사용하지 않는 작업에 대한 일반적인 패턴: `Start-Job {param ($context) New-AzureRmVM -AzureRmContext $context [... other parameters]} -ArgumentList (Get-AzureRmContext)`
      - 컨텍스트 지속성을 사용하는 작업에 대한 일반적인 패턴: `Start-Job {New-AzureRmVM [... other parameters]}`
  * 세션 간 로그인 정보 유지, 새 cmdlet:
    - Enable-AzureRmContextAutosave - 세션 간 자격 증명 지속성을 사용합니다.
    - Enable-AzureRmContextAutosave - 세션 간 자격 증명 지속성을 사용하지 않습니다.
  * 컨텍스트 정보 관리, 새 cmdlet
    - Select-AzureRmContext - 활성 이름의 컨텍스트를 선택합니다.
    - Rename-AzureRmContext - 쉽게 참조할 수 있도록 기존 컨텍스트의 이름을 바꿉니다.
    - Remove-AzureRmContext - 기존 컨텍스트를 제거합니다.
    - Remove-AzureRmAccount - 계정과 관련된 자격 증명, 구독 및 테넌트를 모두 제거합니다.
  * 컨텍스트 정보 관리, cmdlet 변경:
    - Scope = (Process | CurrentUser)가 자격 증명을 변경하는 모든 cmdlet에 추가됨
    - Get-AzureRmContext - 저장된 모든 컨텍스트를 나열하는 ListAvailable 매개 변수가 추가됨
* 리소스
  * PolicySetDefinition cmdlet 추가
    - 정책 집합 정의를 만드는 New-AzureRmPolicySetDefinition cmdlet
    - 모든 정책 집합 정의를 나열하거나 특정 정책 집합 정의를 가져오는 Get-AzureRmPolicySetDefinition cmdlet
    - 정책 집합 정의를 삭제하는 Remove-AzureRmPolicySetDefinition cmdlet
    - 기존 정책 집합 정의를 업데이트하는 Set-AzureRmPolicySetDefinition cmdlet
  * -PolicySetDefinition, -Sku 및 -NotScope 매개 변수를 New-AzureRmPolicyAssignment 및 Set-AzureRmPolicyAssignment cmdlet에 추가
  * New-AzureRmPolicyDefinition 및 Set-AzureRmPolicyDefinition cmdlet에 정책 URL을 전달하기 위한 지원 추가
  * -Mode 매개 변수 New-AzureRmPolicyDefinition cmdlet에 추가
  * PSRoleAssignment 개체를 사용하여 roleassignment 제거를 위한 지원 추가
    - 사용자는 이제 Remove-AzureRMRoleAssignment commandlet과 함께 PSRoleassignmnet inputobject를 사용하여 roleassignment를 제거할 수 있습니다.
  * ManagedApplication cmdlet 추가
    - 관리되는 애플리케이션을 만드는 New-AzureRmManagedApplication cmdlet
    - 구독에서 모든 관리되는 애플리케이션을 나열하거나 관리되는 특정 애플리케이션을 가져오는 Get-AzureRmManagedApplication cmdlet
    - 관리되는 애플리케이션을 삭제하는 Remove-AzureRmManagedApplication cmdlet
    - 기존의 관리되는 애플리케이션을 업데이트하는 Set-AzureRmManagedApplication cmdlet
  * ManagedApplicationDefinition cmdlet 추가
    - zip 파일 URI를 사용하거나 mainTemplate 및 createUiDefinition json 파일을 사용하여 관리되는 애플리케이션 정의를 만드는 New-AzureRmManagedApplicationDefinition cmdlet
    - 리소스 그룹에서 모든 관리되는 애플리케이션 정의를 나열하거나 관리되는 특정 애플리케이션 정의를 가져오는 Get-AzureRmManagedApplicationDefinition cmdlet
    - 관리되는 애플리케이션 정의를 삭제하는 Remove-AzureRmManagedApplicationDefinition cmdlet
    - 기존의 관리되는 애플리케이션 정의를 업데이트하는 Set-AzureRmManagedApplicationDefinition cmdlet
* Sql
  * Virtual Network 규칙에 대한 지원 추가
    - Azure SQL Server에서 가상 네트워크 규칙의 목록 또는 특정 규칙 이름에 의해 가상 네트워크 규칙을 가져오는 Get-AzureRmSqlServerVirtualNetworkRule cmdlet 추가.
    - 규칙이 가리키는 가상 네트워크를 변경하는 Set-AzureRmSqlServerVirtualNetworkRule cmdlet 추가.
    - Azure SQL Server에 대한 가상 네트워크 규칙을 제거하는 Remove-AzureRmSqlServerVirtualNetworkRule cmdlet 추가.
    - Azure SQL Server에 대한 새 가상 네트워크 규칙을 만드는 New-AzureRmSqlServerVirtualNetworkRule cmdlet 추가.
* Websites
  * App Service 요금제에 대한 PremiumV2 계층 추가
* Azure.Storage
  * Azure Storage 클라이언트 라이브러리 8.4.0 및 Azure Storage DataMovement 라이브러리 0.6.1로 업그레이드
  * Blob API 복사 및 업로드에 PremiumPageBlobTier 지원 추가
    - Set-AzureStorageBlobContent
    - Start-AzureStorageBlobCopy
  * AzureStorageContainer, AzureStorageBlob, AzureStorageQueue, AzureStorageTable의 콘솔 출력 형식 구체화
    - Get-AzureStorageContainer
    - Get-AzureStorageBlob
    - Get-AzureStorageQueue
    - Get-AzureStorageTable

## <a name="20170810---version-431"></a>2017.08.10 - 버전 4.3.1
  * 어셈블리 서명 문제를 수정하기 위한 업데이트

## <a name="20170807---version-430"></a>2017.08.07 - 버전 4.3.0
* AnalysisServices
  * Set-AzureRmAnalysisServciesServer에서 버그 수정됨
    - 관리자가 제공되지 않으면 관리자가 제거됩니다.
  * New-AzureRmAnalysisServicesServer 및 Set-AzureRmAnalysisServicesServer에서 BackupBlobContainerUri가 추가됨
    - Azure Analysis Services Server 백업/복원을 위해 백업 Blob 컨테이너 설정/비활성화 사용
  * New-AzureRmAnalysisServicesServer 및 Set-AzureRmAnalysisServicesServer에서 Sku 조회가 업데이트됨
    - 하드 코딩된 Sku가 동적 조회로 변경되었습니다.
  * 서비스 주체로 로그인을 지원하는 Add-AzureAnalysisServicesAccount
* Automation
  * AutomationDSC* cmdlet이 100개가 넘는 레코드를 풀하도록 변경되었음
  * 일부 Automation cmdlet(예: Get-AzureRmAutomationVariable, Get-AzureRmAutomationJob)을 호출한 후 자세한 정보 표시 스트림 작동이 중지되는 문제가 해결되었습니다.
  * NodeConfiguration 빌드 버전 관리에 대한 지원이 StartAzureAutomationDscCompilationJob 및 ImportAzureAutomationDscNodeConfiguration에서 추가되었습니다.
  * 기존 문제에 대한 버그 수정 - 별칭 문제 해결은 #3775이며 runOn 별칭 및 HybridWorkers에 대한 지원
* 컴퓨팅
  * Set-AzureRmVMAEMExtension: 새로운 프리미엄 디스크 크기에 대한 지원 추가
  * Set-AzureRmVMAEMExtension: M 시리즈에 대한 지원 추가
  * ForceUpdateTag 매개 변수를 Add-AzureRmVmssExtension에 추가
  * 기본 매개 변수를 New-AzureRmVmssIpConfig에 추가
  * EnableAcceleratedNetworking 매개 변수를 Add-AzureRmVmssNetworkInterfaceConfig에 추가
  * Set-AzureRmVmss에 인스턴스 ID 추가
  * Get-AzureRmVM -Status 출력에 MaintenanceRedeployStatus 공개
  * Get-AzureRmComputeResourceSku의 테이블 형식에 제한 및 기능 공개
* DataLakeStore
  * 문제 수정: https://github.com/Azure/azure-powershell/issues/4323
* EventHub
  * ResourceGroup 속성이 NamespaceAttributes에 추가됨
    - 'ResourceGroup'은 네임스페이스가 있는 리소스 그룹 이름을 가져옵니다.
  * cmdlet이 AuthorizationRule 작업을 위한 네임스페이스 및 EventHub에 대한 Parametersets로 업데이트됨
    - New-AzureRmEventHubAuthorizationRule - 기존 NameSpace 또는 EventHub에 새 AuthorizationRule을 추가합니다.
    - Get-AzureRmEventHubAuthorizationRule - 기존 NameSpace 또는 EventHub에 대한 AuthorizationRule / AuthorizationRule 목록을 가져옵니다.
    - Set-AzureRmEventHubAuthorizationRule - EventHub NameSpace의 기존 AuthorizationRule 속성을 업데이트합니다.
    - Remove-AzureRmEventHubAuthorizationRule - 기존 NameSpace 또는 EventHub의 기존 AuthorizationRule을 삭제합니다.
    - New-AzureRmEventHubKey - 기존 NameSpace 또는 EventHub의 AuthorizationRule에 대한 새로운 주/보조 키를 생성합니다.
    - Get-AzureRmEventHubKey - 기존 NameSpace 또는 EventHub의 AuthorizationRule에 대한 주/보조 키를 가져옵니다.
* 네트워크
    * IPv6 지원 및 새로운 선택 사항 매개 변수 -PeerAddressType이 추가됨
      * New-AzureRmExpressRouteCircuitPeeringConfig:
      * Set-AzureRmExpressRouteCircuitPeeringConfig: IPv6 지원이 추가되었습니다. 새로운 선택적 매개 변수 추가됨
      * Remove-AzureRmExpressRouteCircuitPeeringConfig: IPv6 지원이 추가되었습니다. 새로운 선택적 매개 변수 추가됨
    * 매개 변수 -ProbeEnabled가 사용되지 않는 것으로 표시됨
      - Add-AzureRmApplicationGatewayBackendHttpSettings
      - New-AzureRmApplicationGatewayBackendHttpSettings
      - Set-AzureRmApplicationGatewayBackendHttpSettings
* 프로필
    * 기본적으로 데이터 컬렉션은 사용하도록 설정되었습니다. 사용자 환경을 개선하기 위해 Microsoft에서 사용량 현황 데이터를 수집합니다. 데이터는 익명이며 명령줄 인수 값을 포함하지 않습니다.
      - Disable-AzureRmDataCollection cmdlet을 사용하여 기능 해제
      - Enable-AzureRmDataCollection cmdlet을 사용하여 이 기능 설정
* 리소스
    * ARM에 요청을 보내기 전에 다음 roledefinition 및 roleassignment commandlet에 대한 범위의 유효성 검사를 위한 지원 추가
      - Get-AzureRMRoleAssignment
      - New-AzureRMRoleAssignment
      - Remove-AzureRMRoleAssignment
      - Get-AzureRMRoleDefinition
      - New-AzureRMRoleDefinition
      - Remove-AzureRMRoleDefinition
      - Set-AzureRMRoleDefinition
* ServiceBus
  * NameSpace, 큐 및 토픽의 AuthorizationRules에 대한 새로운 commandlet이 아래에 추가되었습니다. 매개 변수 집합에 따라 권한 부여 규칙 작업이 수행됩니다.
    - New-AzureRmServiceBusAuthorizationRule - 기존 ServiceBus NameSpace/큐/토픽에 새 AuthorizationRule을 추가합니다.
    - Get-AzureRmServiceBusAuthorizationRule - 기존 ServiceBus NameSpace/큐/토픽에 대한 AuthorizationRule / AuthorizationRule 목록을 가져옵니다.
    - Set-AzureRmServiceBusAuthorizationRule - ServiceBus NameSpace/큐/토픽의 기존 AuthorizationRule 속성을 업데이트합니다.
    - New-AzureRmServiceBusKey - 기존 ServiceBus NameSpace/큐/토픽의 AuthorizationRule에 대한 새로운 주/보조 키를 생성합니다.
    - Get-AzureRmServiceBusKey - 기존 ServiceBus NameSpace/큐/토픽의 AuthorizationRule에 대한 주/보조 키를 가져옵니다.
    - Remove-AzureRmServiceBusNamespaceAuthorizationRule - ServiceBus NameSpace/큐/토픽의 기존 AuthorizationRule을 삭제합니다.
  * 리소스 그룹 속성이 NamespceAttributes에 추가됨

* Sql
    * 암호화 보호기 유형이 AzureKeyVault로 설정되어 있는 경우 경고를 표시하고 확인을 요구하도록 Set-AzureRmSqlServerTransparentDataEncryptionProtector 업데이트 중
    * 감사 설정을 위해 업데이트된 새 cmdlet 추가 중
      - Azure SQL 데이터베이스의 감사 설정을 가져오는 Get-AzureRmSqlDatabaseAuditing cmdlet
      - Azure SQL 서버의 감사 설정을 가져오는 Get-AzureRmSqlServerAuditing cmdlet
      - Azure SQL 데이터베이스의 감사 설정을 변경하는 Set-AzureRmSqlDatabaseAuditing cmdlet
      - Azure SQL 서버의 감사 설정을 변경하는 Set-AzureRmSqlServerAuditing cmdlet
    * 기존 감사 정책 cmdlet을 사용 중단하는 중
      - Get-AzureRmSqlDatabaseAuditingPolicy
      - Get-AzureRmSqlServerAuditingPolicy
      - Set-AzureRmSqlDatabaseAuditingPolicy
      - Set-AzureRmSqlServerAuditingPolicy
      - Use-AzureRmSqlServerAuditingPolicy
      - Remove-AzureRmSqlDatabaseAuditing
      - Remove-AzureRmSqlServerAuditing
    * Update-AzureRmSqlSyncGroup을 위한 스키마 파일 구문 분석은 대/소문자를 구분하지 않습니다.
* 스토리지
    * 리소스 모드 스토리지 계정 cmdlet에 NeworkRule 지원 추가
      - New-AzureRmStorageAccount
      - Set-AzureRmStorageAccount
      - Get-AzureRmStorageAccountNetworkRuleSet
      - Update-AzureRmStorageAccountNetworkRuleSet
      - Add-AzureRmStorageAccountNetworkRule
      - Remove-AzureRmStorageAccountNetworkRule

## <a name="20170717---version-421"></a>2017.07.17 - 버전 4.2.1
* 컴퓨팅
  - VM 디스크/VM 디스크 스냅샷 만들기 및 업데이트 cmdlet 관련 문제 수정(링크)[<https://github.com/azure/azure-powershell/issues/4309>]
    - New-AzureRmDisk
    - New-AzureRmSnapshot
    - Update-AzureRmDisk
    - Update-AzureRmSnapshot
* 프로필
  - RDFE에서 비대화형 사용자 인증 관련 문제 수정(링크)[<https://github.com/Azure/azure-powershell/issues/4299>]

* ServiceManagement
  - 비대화형 사용자 인증 관련 문제 수정(링크)[<https://github.com/Azure/azure-powershell/issues/4299>]

## <a name="2017711---version-420"></a>2017.7.11 - 버전 4.2.0
* AnalysisServices
    * 새 데이터 평면 API 추가
        - AS 서버 로그 Export-AzureAnalysisServicesInstanceLog를 인출하는 API를 도입했습니다.
* Automation
    * New-AzureRmAutomationSchedule의 주별 및 월별 일정에 표준 시간대 값을 제대로 설정합니다.
        - 이 문제에 대한 자세한 내용: https://github.com/Azure/azure-powershell/issues/3043 참조
* AzureBatch
    - 새 Get-AzureBatchJobPreparationAndReleaseTaskStatus cmdlet이 추가되었습니다.
    - Get-AzureBatchNodeFileContent 매개 변수에 바이트 범위 시작 및 종료가 추가되었습니다.
* CognitiveServices
    * Cognitive Services Management SDK 버전 1.0.0과 통합합니다.
    * 계정 이름 길이 확인 버그를 수정합니다.
* 컴퓨팅
    * 이미지 디스크에 대한 Storage 계정 형식 지원:
        - Set-AzureRmImageOsDisk 및 Add-AzureRmImageDataDisk에 'StorageAccountType' 매개 변수가 추가되었습니다.
    * VMSS IP 구성에서 PrivateIP 및 PublicIP 기능:
        - New-AzureRmVmssIpConfig에 'PrivateIPAddressVersion', 'PublicIPAddressConfigurationName', 'PublicIPAddressConfigurationIdleTimeoutInMinutes', 'DnsSetting' 이름이 추가되었습니다.
        - New-AzureRmVmssIpConfig에 IPv4 또는 IPv6을 지정하는 'PrivateIPAddressVersion' 매개 변수가 추가되었습니다.
    * 성능 유지 관리 기능:
        - Restart-AzureRmVM에 'PerformMaintenance' 스위치 매개 변수가 추가되었습니다.
        - Get-AzureRmVM 상태는 지정된 VM의 성능 유지 관리 정보를 보여줍니다.
    * Virtual Machine ID 기능:
        - New-AzureRmVMConfig 및 UpdateAzureRmVM에 'IdentityType' 매개 변수가 추가되었습니다.
        - Get-AzureRmVM은 지정된 VM의 ID 정보를 보여줍니다.
    * VMSS ID 기능:
        - New-AzureRmVmssConfig에 'IdentityType' 매개 변수가 추가되었습니다.
        - Get-AzureRmVmss는 지정된 VMSS의 ID 정보를 보여줍니다.
    * VMSS 부트 진단 기능:
        - VMSS 개체의 부트 진단을 설정하는 새 cmdlet: Set-AzureRmVmssBootDiagnostics
        - New-AzureRmVmssConfig에 'BootDiagnostic' 매개 변수가 추가되었습니다.
    * VMSS LicenseType 기능:
        - New-AzureRmVmssConfig에 'LicenseType' 매개 변수가 추가되었습니다.
    * RecoveryPolicyMode 지원:
        - New-AzureRmVmssConfig에 'RecoveryPolicyMode' 매개 변수가 추가되었습니다.
    * Compute 리소스 SKU 기능:
        - 새 cmdlet인 'Get-AzureRmComputeResourceSku'는 모든 컴퓨팅 리소스 SKU를 나열합니다.
* DataFactories
    * New-AzureRmDataFactoryGatewayKey를 사용하지 않습니다.
    * New-AzureRmDataFactoryGatewayAuthKey 및 Get-AzureRmDataFactoryGatewayAuthKey를 추가하여 게이트웨이 인증 주요 기능을 도입합니다.
* DataLakeAnalytics
    * 다음 명령을 통해 Compute 정책 CRUD에 대한 지원을 추가합니다.
        - New-AzureRMDataLakeAnalyticsComputePolicy
        - Get-AzureRMDataLakeAnalyticsComputePolicy
        - Remove-AzureRMDataLakeAnalyticsComputePolicy
        - Update-AzureRMDataLakeAnalyticsComputePolicy
    * 되풀이 작업 및 작업 파이프라인의 도움말에 작업 관계 메타데이터에 대한 지원을 추가합니다. 다음 명령은 업데이트하거나 추가했습니다.
        - Submit-AzureRMDataLakeAnalyticsJob
        - Get-AzureRMDataLakeAnalyticsJob
        - Get-AzureRMDataLakeAnalyticsJobRecurrence
        - Get-AzureRMDataLakeAnalyticsJobPipeline
    * 작업과 카탈로그 API에 토큰 대상을 업데이트하여 Azure 리소스 그룹 대신 올바른 Data Lake 특정 대상을 사용합니다.
* DataLakeStore
    * Set-AzureRMDataLakeStoreAccount cmdlet에서 사용자관리 KeyVault 키 회전에 대한 지원을 추가했습니다.
    * 사용자 관리 KeyVault가 추가되거나 키를 회전할 경우 `enableKeyVault` 호출을 자동으로 트리거하도록 수명 품질 업데이트를 추가했습니다.
    * 작업과 카탈로그 API에 토큰 대상을 업데이트하여 Azure 리소스 그룹 대신 올바른 Data Lake 특정 대상을 사용합니다.
    * 다음 cmdlet을 사용하여 만든/추가한 파일의 크기를 제한하는 버그를 수정했습니다.
        - New-AzureRmDataLakeStoreItem
        - Add-AzureRmDataLakeStoreItemContent
* Dns
    * Get-AzureRmDnsZone에 대한 파이프 시나리오에서 버그를 수정합니다.
        - 자세한 내용은 https://github.com/Azure/azure-powershell/issues/4203 를 참조하세요.
* HDInsight
    * OMS(Operations Management Suite)를 활성화/비활성화하는 지원이 추가되었습니다.
    * 새로운 cmdlet
        - Enable-AzureRmHDInsightOperationsManagementSuite
        - Disable-AzureRmHDInsightOperationsManagementSuite
        - Get-AzureRmHDInsightOperationsManagementSuite
    * Add-AzureRmHDInsightConfigValues에 Spark 사용자 지정 구성을 설정하는 새 매개 변수를 추가합니다.
        - Spark 1.6의 SparkDefaults 및 SparkThriftConf 매개 변수
        - Spark 2.0의 Spark2Defaults 및 Spark2ThriftConf 매개 변수
* 자세한 정보
    * 문제 #4215(변경 요청)는 Get-AzureRmLog cmdlet의 시간 창에서 15일 제한을 제거합니다. 또한 단위 테스트 이름을 사소하게 변경합니다.
    * 문제 #3957는 Get-AzureRmLog를 수정했습니다.
        - 문제 #1: 백 엔드는 각 200개의 레코드 페이지에서 레코드를 반환하며, 연속 토큰에서 다음 페이지로 연결됩니다. 200개 이상의 레코드가 있더라도 cmdlet에서는 반환되는 200개의 레코드만이 표시되었습니다. 200보다 값이 작지 않으면 MaxEvents에 설정한 값에 관계없이 발생했습니다.
        - 문제 #2: 예를 들어 설명서에 포함된 이 cmdlet에 대한 잘못된 데이터는 기본 timewindow가 1시간이었습니다.
        - 수정 사항 #1: 이제 cmdlet은 MaxEvents 또는 집합의 끝에 도달할 때까지 백 엔드에서 반환한 연속 토큰을 수행합니다.<br>MaxEvents의 기본값은 1000이며 최대 100000입니다. 1보다 작은 MaxEvents 값은 무시되고 대신 기본값이 사용됩니다. 이러한 값과 동작은 변경되지 않았으며 이제 올바르게 문서화됩니다.<br>cmdlet의 이름이 이벤트가 아닌 로그를 가리키기 때문에 MaxEvents의 별칭인 MaxRecords가 추가되었습니다.
        - 수정 #2: 설명서는 새 별칭, 올바른 시간 창, 올바른 기본, 최소 및 최대 값에 대한 정확하고 자세한 정보를 포함합니다.
* KeyVault
    * -UserPrincipalName을 Set-AzureRMKeyVaultAccessPolicy 및 Remove-AzureRMKeyVaultAccessPolicy cmdlet에 지정한 경우 디렉터리 쿼리에서 전자 메일 주소를 제거합니다.
      - 이제 cmdlet 모두에 전자 메일 주소를 적절히 쿼리하는 경우 -UserPrincipalName 매개 변수 대신 사용할 수 있는 -EmailAddress 매개 변수를 만들었습니다.  디렉터리에 있는 둘 이상의 전자 메일 주소가 일치하는 경우 cmdlet이 실패합니다.
* 네트워크
    * New-AzureRmIpsecPolicy: SALifeTimeSeconds 및 SADataSizeKilobytes는 더 이상 필수 매개 변수가 아닙니다.
        - SALifeTimeSeconds의 기본값은 27000초입니다.
        - SADataSizeKilobytes의 기본값은 102400000KB입니다.
    * SSL 정책을 사용하고 Application Gateway에서 모든 SSL 옵션 API를 나열하여 사용자 지정 암호 제품군 구성에 대한 지원을 추가했습니다.
        - 선택적 매개 변수인 -PolicyType, -PolicyName, -MinProtocolVersion, -Ciphersuite를 추가했습니다.
            - Add-AzureRmApplicationGatewaySslPolicy
            - New-AzureRmApplicationGatewaySslPolicy
            - Set-AzureRmApplicationGatewaySslPolicy
        - Get-AzureRmApplicationGatewayAvailableSslOptions(별칭: List-AzureRmApplicationGatewayAvailableSslOptions)를 추가했습니다.
        - Get-AzureRmApplicationGatewaySslPredefinedPolicy(별칭: List-AzureRmApplicationGatewaySslPredefinedPolicy)를 추가했습니다.
    * Application Gateway에서 리디렉션 지원을 추가했습니다.
        - Add-AzureRmApplicationGatewayRedirectConfiguration을 추가했습니다.
        - Get-AzureRmApplicationGatewayRedirectConfiguration을 추가했습니다.
        - New-AzureRmApplicationGatewayRedirectConfiguration을 추가했습니다.
        - Remove-AzureRmApplicationGatewayRedirectConfiguration을 추가했습니다.
        - Set-AzureRmApplicationGatewayRedirectConfiguration을 추가했습니다.
        - 선택적 매개 변수인 -RedirectConfiguration을 추가했습니다.
            - Add-AzureRmApplicationGatewayRequestRoutingRule
            - New-AzureRmApplicationGatewayRequestRoutingRule
            - Set-AzureRmApplicationGatewayRequestRoutingRule
        - 선택적 매개 변수인 -DefaultRedirectConfiguration을 추가했습니다.
            - Add-AzureRmApplicationGatewayUrlPathMapConfig
            - New-AzureRmApplicationGatewayUrlPathMapConfig
            - Set-AzureRmApplicationGatewayUrlPathMapConfig
        - 선택적 매개 변수인 -RedirectConfiguration을 추가했습니다.
            - Add-AzureRmApplicationGatewayPathRuleConfig
            - New-AzureRmApplicationGatewayPathRuleConfig
            - Set-AzureRmApplicationGatewayPathRuleConfig
        - 선택적 매개 변수인 RedirectConfigurations를 추가했습니다.
            - New-AzureRmApplicationGateway
            - Set-AzureRmApplicationGateway
    * Application Gateway에서 Azure 웹 사이트에 대한 지원을 추가했습니다.
        - New-AzureRmApplicationGatewayProbeHealthResponseMatch를 추가했습니다.
        - 선택적 매개 변수인 PickHostNameFromBackendHttpSettings, -MinServers, -Match를 추가했습니다.
            - Add-AzureRmApplicationGatewayProbeConfig
            - New-AzureRmApplicationGatewayProbeConfig
            - Set-AzureRmApplicationGatewayProbeConfig
        - 선택적 매개 변수인 PickHostNameFromBackendAddress, -AffinityCookieName, -ProbeEnabled, -Path를 추가했습니다.
            - Add-AzureRmApplicationGatewayBackendHttpSettings
            - New-AzureRmApplicationGatewayBackendHttpSettings
            - Set-AzureRmApplicationGatewayBackendHttpSettings
    * Get-AzureRmPublicIPaddress를 업데이트하여 VM 확장 집합을 통해 만든 publicipaddress 리소스를 검색합니다.
    * 현재 가상 네트워크 사용량을 가져오는 cmdlet을 추가했습니다.
        - Get-AzureRmVirtualNetworkUsageList
* 프로필
    * Import-AzureRmContext 또는 Save-AzureRmContext를 사용하는 경우에 발생하는 오류를 수정했습니다.
        - 이 문제에 대한 자세한 내용: https://github.com/Azure/azure-powershell/issues/3954 참조
* RecoveryServices.SiteRecovery
    * Azure Site Recovery 작업에 대한 새 모듈을 도입합니다.
        - 모든 cmdlet은 AzureRmRecoveryServicesAsr*로 시작합니다.
* Sql
    * AzureRM.Sql에 데이터 동기화 PowerShell Cmdlet을 추가합니다.
    * 서버를 만들 때 시간 초과를 방지하는 새 REST API 버전을 사용하도록 AzureRmSqlServer cmdlet을 업데이트했습니다.
    * 이전 서버 버전(2.0)이 더 이상 존재하지 않기 때문에 사용되지 않는 서버가 cmdlet을 업그레이드합니다.
    * 새 선택적 스위치 매개 변수인 "AssignIdentity"를 New-AzureRmSqlServer 및 Set-AzureRmSqlServer cmdlet에 추가하여 SQL Server 리소스에 대한 리소스 ID를 프로비전하도록 지원합니다.
    * 매개 변수 ResourceGroupName은 이제 Get-AzureRmSqlServer에 선택 사항입니다.
        - 이 문제에 대한 자세한 내용: https://github.com/Azure/azure-powershell/issues/635 참조
* ServiceManagement ExpressRoute의 경우:
    * 다음과 같은 새 옵션을 추가하는 New-AzureBgpPeering cmdlet을 업데이트했습니다.
        - PeerAddressType: 해당 주소 제품군 형식의 BGP 피어링 만들기 위해 "IPv4" 또는 "IPv6" 값을 지정할 수 있습니다.
    * 다음과 같은 새 옵션을 추가하는 Set-AzureBgpPeering cmdlet을 업데이트했습니다.
        - PeerAddressType: 해당 주소 제품군 형식의 BGP 피어링 업데이트하기 위해 "IPv4" 또는 "IPv6" 값을 지정할 수 있습니다.
    * 다음과 같은 새 옵션을 추가하는 Remove-AzureBgpPeering cmdlet을 업데이트했습니다.
        - PeerAddressType: 해당 주소 제품군 형식의 BGP 피어링 또는 모든 항목을 제거하기 위해 "IPv4", "IPv6" 및 모든 값을 지정할 수 있습니다.

## <a name="20170607---version-410"></a>2017.06.07 - 버전 4.1.0
* AnalysisServices
    * B1, B2, S0라는 새 SKU가 추가되었습니다.
    * 스케일 업/다운 지원이 추가되었습니다.
* CognitiveServices
    * Cognitive Services 리소스를 만들 때 라이선스 규약을 자세히 표시하도록 업데이트합니다.
* 컴퓨팅
    * 여러 개의 Managed Disks가 있는 가상 머신에서 Test-AzureRmVMAEMExtension을 수정합니다.
    * Set-AzureRmVMAEMExtension을 업데이트했습니다. Premium Managed Disks에 대한 캐시 정보를 추가합니다.
    * Add-AzureRmVhd: VHD의 크기 제한이 4TB로 확장되었습니다.
    * Stop-AzureRmVM: STayProvisioned 매개 변수에 대한 설명서를 분류합니다.
    * New-AzureRmDiskUpdateConfig
      * CreateOption, StorageAccountId, ImageReference, SourceUri, SourceResourceId 매개 변수는 사용되지 않습니다.
    * Set-AzureRmDiskUpdateImageReference: 사용되지 않는 cmdlet
    * New-AzureRmSnapshotUpdateConfig
      * CreateOption, StorageAccountId, ImageReference, SourceUri, SourceResourceId 매개 변수는 사용되지 않습니다.
    * Set-AzureRmSnapshotUpdateImageReference: 사용되지 않는 cmdlet
* DataLakeStore
    * Enable-AzureRmDataLakeStoreKeyVault(Enable-AdlStoreKeyVault)
      * Data Lake Store에 KeyVault 관리되는 암호화를 사용합니다.
* DevTestLabs
    * cmdlet을 업데이트하여 현재 및 업데이트된 DevTest Labs API 버전에서 작업합니다.
* IotHub
    * IoTHub cmdlet에 라우팅 지원을 추가합니다.
* KeyVault
  * KeyVault 관리되는 Storage 계정 키를 지원하는 새 cmdlet
    * Get-AzureKeyVaultManagedStorageAccount
    * Add-AzureKeyVaultManagedStorageAccount
    * Remove-AzureKeyVaultManagedStorageAccount
    * Update-AzureKeyVaultManagedStorageAccount
    * Update-AzureKeyVaultManagedStorageAccountKey
    * Get-AzureKeyVaultManagedStorageSasDefinition
    * Set-AzureKeyVaultManagedStorageSasDefinition
    * Remove-AzureKeyVaultManagedStorageSasDefinition
* 네트워크
    * Get-AzureRmNetworkUsage: 네트워크 사용량 및 용량 정보를 표시하는 새 cmdlet
    * VirtualNetworkGateways에 새 GatewaySku 옵션을 추가했습니다.
        * VpnGw1, VpnGw2, VpnGw3은 VPN Gateway에 추가된 새 SKU입니다.
    * Set-AzureRmNetworkWatcherConfigFlowLog
      * 도움말 예제를 수정했습니다.
* NotificationHubs
    * 새 API의 NotificationHubs cmdlet에 대한 투명한 업데이트
* 프로필
    * Resolve-AzureRmError
      * 서버 요청/응답 데이터를 비롯한 cmdlet에서 throw한 오류 및 예외 세부 정보를 표시하는 새 cmdlet
    * Send-Feedback
      * 로그인하지 않고 송신 피드백을 사용하도록 설정했습니다.
    * Get-AzureRmSubscription
      * CSP 구독을 검색할 때 발생하는 버그를 수정합니다.
* 리소스
    * roleassignments의 수가 1000보다 큰 경우 Get-AzureRMRoleAssignment가 잘못된 요청을 발생시키는 문제를 수정했습니다.
        * 이제 사용자는 반환되는 roleassignments가 1000보다 큰 경우에도 Get-AzureRMRoleAssignment를 사용할 수 있습니다.
* Sql
    * Restore-AzureRmSqlDatabase: 설명서 예제를 업데이트합니다.
* 스토리지
    * AssignIdentity 설정 지원을 리소스 모드 스토리지 계정 cmdlet에 추가합니다.
        * New-AzureRmStorageAccount
        * Set-AzureRmStorageAccount
    * 고객 키 지원을 리소스 모드 스토리지 계정 cmdlet에 추가합니다.
        * Set-AzureRmStorageAccount
        * New-AzureRmStorageAccountEncryptionKeySource
* TrafficManager

    * 새로운 모니터링 설정 'MonitorIntervalInSeconds', 'MonitorTimeoutInSeconds', 'MonitorToleratedNumberOfFailures'
    * 새로운 모니터링 프로토콜 'TCP'
* ServiceManagement
    * Add-AzureVhd: VHD의 크기 제한이 4TB로 확장되었습니다.
    * New-AzureBGPPeering: LegacyMode를 지원합니다.
* Azure.Storage
    * 와일드 카드 문자를 허용하고 StorageContext 형식을 업데이트하는 매개 변수에 대한 도움말을 업데이트합니다.

## <a name="20170523---version-402"></a>2017.05.23 - 버전 4.0.2
* 프로필
    * Add-AzureRmAccount
      * AzureRM.profile의 2.x 버전을 사용하여 이전 버전과 호환성을 위해 `-EnvironmentName` 매개 변수 별칭을 추가했습니다.

## <a name="20170512---version-401"></a>2017.05.12 - 버전 4.0.1
 * 오프라인 시나리오에서 New-AzureStorageContext 관련 문제 수정: https://github.com/Azure/azure-powershell/issues/3939

## <a name="20170510---version-400"></a>2017.05.10 - 버전 4.0.0


* 이 릴리스에는 주요 변경 내용인 포함됩니다. 변경 세부 정보 및 기존 스크립트에 미치는 영향에 대해서는 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.
* ApiManagement
  - New-AzureRmApiManagementGroup에서 기존 그룹을 구성하기 위한 지원이 추가되었습니다.
* 결제
  - 새 Cmdlet Get-AzureRmBillingPeriod
    + 구독의 Azure 청구 기간을 검색하기 위한 cmdlet입니다.
  - Cmdlet Get-AzureRmBillingInvoice 업데이트
  - 새 속성 BillingPeriodNames
  - 목록 보기에서 출력
* 컴퓨팅
  - 프리미엄 Managed Disks를 지원하도록 Set-AzureRmVMAEMExtension 및 Test-AzureRmVMAEMExtension cmdlet이 업데이트되었습니다.
  - IaaS VM에 대한 암호화 설정 Backup 및 실패 시 복원
  - ChefServiceInterval 옵션 이름이 ChefDaemonInterval로 바뀌었습니다. 그렇지만 이전 이름도 계속 사용할 수 있습니다.
  - PS VM 개체에서 중복된 DataDiskNames 및 NetworkInterfaceIDs 속성을 제거합니다.
  - DataDiskNames 및 NetworkInterfaceIDs 매개 변수를 Remove-AzureRmVMDataDisk 및 Remove-AzureRmVMNetworkInterface에서 각각 옵션으로 지정되었습니다.
  - Get cmdlet이 목록 개체를 반환하는 경우 Get cmdlet의 파이핑 문제가 해결되었습니다.
  - RDFE cmdlet과 충돌하는 Cmdlet 이름이 바뀌었습니다. 이 문제에 대한 자세한 내용은 https://github.com/Azure/azure-powershell/issues/2917 을 참조하세요.
    + `New-AzureVMSqlServerAutoBackupConfig`는 `New-AzureRmVMSqlServerAutoBackupConfig`로 이름이 변경되었습니다.
    + `New-AzureVMSqlServerAutoPatchingConfig`는 `New-AzureRmVMSqlServerAutoPatchingConfig`로 이름이 변경되었습니다.
    + `New-AzureVMSqlServerKeyVaultCredentialConfig`는 `New-AzureRmVMSqlServerKeyVaultCredentialConfig`로 이름이 변경되었습니다.
* Consumption
  - 새 Cmdlet Get-AzureRmConsumptionUsageDetail
    + 구독의 사용량 세부 정보를 검색하기 위한 cmdlet입니다.
* ContainerRegistry
  - Azure Container Registry에 대한 PowerShell cmdlet이 추가되었습니다.
    + New-AzureRmContainerRegistry
    + Get-AzureRmContainerRegistry
    + Update-AzureRmContainerRegistry
    + Remove-AzureRmContainerRegistry
    + Get-AzureRmContainerRegistryCredential
    + Update-AzureRmContainerRegistryCredential
    + Test-AzureRmContainerRegistryNameAvailability
* DataLakeAnalytics
  - 카탈로그 패키지 가져오기 및 나열에 대한 지원 추가
  - 좀 더 높은 수준의 상위 항목에서 다음 카탈로그 항목을 나열하기 위한 지원 추가
    + 테이블
    + TVF
    + 보기
    + 통계
* DataLakeStore
  - `Import-AzureRMDataLakeStoreItem` 및 `Export-AzureRMDataLakeStoreItem`의 경우 성능 향상을 위해 추적 로깅이 기본적으로 사용되지 않도록 설정되어 있습니다. 추적 로깅이 필요한 경우 `-DiagnosticLogLevel` 및 `-DiagnosticLogPath` 매개 변수를 사용하세요.
  - ADLS에 많은 수의 작은 파일을 업로드하는 경우 때때로 PowerShell이 충돌하도록 하는 버그를 수정했습니다.
* EventHub
  - 버그 수정:
    + Set-AzureRmEventHubNamespace cmdlet 오류에 대한 수정 - 'Tier'가 'SkuName'이어야 하는 경우 null로 지정할 수 없습니다.
    + Set-AzureRmEventHub - EventHub를 업데이트하는 동안 '개체 참조가 개체의 인스턴스로 설정되지 않았습니다.' 오류 수정
* 자세한 정보
  - Add-AzureRm*AlertRule
    + 단일 개체 newResource, statusCode, requestId를 반환합니다.
  - Get-AzureRmAlertRule
    + 이제 출력은 단일 개체로 간주되지 않고 열거됩니다. 해당 형식은 변경되지 않았으므로 여전히 목록입니다.
  - Remove-AzureRmAlertRule
    + statusCode는 요청에 의해 반환된 상태 코드(항상 정상임)를 따릅니다.
  - Add-AzureRmAutoscaleSetting
    + 이제 statusCode, requestId 및 새로 생성/업데이트된 리소스를 포함하는 단일 개체(이전처럼 목록이 아님)를 반환합니다.
    + 상태 코드는 요청에 의해 반환된 상태(항상 정상임)를 따릅니다.
  - New-AzureRmAutoscaleRule
    + 매개 변수 ScaleActionType이 확장되었으며 이제 값 ChangeCount, PercentChangeCount, ExactCount를 수신합니다.
  - Remove-AzureRmAutoscaleSetting
    + 출력의 statusCode는 요청에 의해 반환된 statusCode를 따릅니다. 이 코드가 이전에는 항상 정상이었습니다.
  - Get-AzureRMLogProfile
    + 이제 출력이 열거됩니다. 이전에는 단일 개체로 간주되었습니다. 출력의 형식은 이전처럼 목록으로 유지됩니다.
  - Remove-AzureRmLogProfile
    + PassThru 매개 변수가 구현되었습니다.
  - Metrics API
    + 이 SDK는 이제 MDM에서 메트릭을 검색합니다.
  - Get-AzureRmMetricDefinition
    + 출력은 여전히 목록이지만 목록 구조가 변경되었습니다.
  - Get-AzureRmMetric
    + 호출이 변경되었습니다. 새 구문: Get-AzureRmMetric ResourceId [MetricNames [TimeGrain] [AggregationType] [StartTime] [EndTime]] [DetailedOutput]
    + 출력은 목록이며 해당 요소의 구조가 변경되었습니다.
* KeyVault
  - KeyVault 비밀에 대한 백업/복원 지원 추가
    + 비밀을 백업 및 복원할 수 있으며 키에 대해 현재 지원되는 기능과 일치합니다.

  - 키 및 비밀에 대한 Backup cmdlet은 이제 해당 개체를 입력 매개 변수로 수락합니다.
    + 호출자는 검색 및 백업 작업을 연쇄적으로 진행할 수 있음: Get-AzureKeyVaultKey -VaultName myVault -Name myKey | Backup-AzureKeyVaultKey

  - 이제 Backup cmdlet은 기존 파일을 덮어쓰기 위한 -Force 스위치를 지원합니다.
    + 기존 파일을 덮어쓰려고 해도 더 이상 오류가 throw되지 않으며 대신, 사용자에게 진행 방법을 선택하라는 메시지가 표시됩니다.
* LogicApp
  - 교환 컨트롤 번호 재해 복구 cmdlet에 대한 새 매개 변수:
    + 옵션 - 관련 컨트롤 번호를 지정하기 위한 AgreementType 매개 변수("X12" 또는 "Edifact")
* MachineLearning
  - 새 버전의 Azure Machine Learning .Net SDK를 사용하고 새로운 cmdlet을 추가합니다.
    + Add-AzureRmMlWebServiceRegionalProperty
  - 도움말 텍스트의 일부 표현이 수정되었습니다.
* 네트워크
  - Test-AzureRmNetworkWatcherConnectivity cmdlet이 추가되었습니다.
    + 지정된 원본 VM 및 대상에 대한 연결 정보를 반환합니다.
    + 원본 및 대상 간에 연결을 설정할 수 없는 경우 이 cmdlet은 문제에 대한 세부 정보를 반환합니다.
* 프로필
  - `Send-Feedback' cmdlet 추가: 사용자는 Azure PowerShell 팀에 피드백을 전송하는 일련의 메시지를 시작할 수 있습니다.
  - 다음 별칭은 Azure 모듈의 기존 cmdlet 이름과 충돌하므로 제거되었습니다.
    + `Enable-AzureDataCollection`(`Enable-AzureRmDataCollection`에서 지원)
    + `Disable-AzureDataCollection`(`Disable-AzureRmDataCollection`에서 지원)
* 릴레이
  - 사용자가 모든 Azure Relay 리소스를 만들고 관리할 수 있도록 하는 Azure Relay에 대한 cmdlet을 추가합니다.
    + `New-AzureRmRelayNamespace`
    + `Get-AzureRmRelayNamespace`
    + `Set-AzureRmRelayNamespace`
    + `Remove-AzureRmRelayNamespace`
    + `New-AzureRmWcfRelay`
    + `Get-AzureRmWcfRelay`
    + `Set-AzureRmWcfRelay`
    + `Remove-AzureRmWcfRelay`
    + `New-AzureRmRelayHybridConnection`
    + `Get-AzureRmRelayHybridConnection`
    + `Set-AzureRmRelayHybridConnection`
    + `Remove-AzureRmRelayHybridConnection`
    + `Test-AzureRmRelayName`
    + `Get-AzureRmRelayOperation`
    + `New-AzureRmRelayKey`
    + `Get-AzureRmRelayKey`
    + `New-AzureRmRelayAuthorizationRule`
    + `Get-AzureRmRelayAuthorizationRule`
    + `Set-AzureRmRelayAuthorizationRule`
    + `Remove-AzureRmRelayAuthorizationRule`
* 리소스
  - New-AzureRmResourceGroupDeployment에 대한 리소스 그룹 간 배포를 지원합니다.
    + 이제 사용자는 중첩 배포를 사용하여 다른 리소스 그룹에 배포할 수 있습니다.
* ServiceBus

  - 버그 수정: ServiceBus 큐 개체 속성 값이 null로 설정되었으며 해당 개체는 큐 업데이트를 위해 Set-AzureRmServiceBusQueue cmdlet에서 입력 매개 변수로 사용됩니다.
    - 영향 받는 속성은 LockDuration, EntityAvailabilityStatus, DuplicateDetectionHistoryTimeWindow, MaxDeliveryCount 및 MessageCount입니다.
* ServiceFabric

  - Service Fabric에 대한 cmdlet이 추가되었습니다.
    + Add-AzureRmServiceFabricApplicationCertificate       애플리케이션 인증서로 사용할 인증서 추가
    + Add-AzureRmServiceFabricClientCertificate       클라이언트 인증을 위해 일반 이름 또는 지문을 클러스터 설정에 추가
    + Add-AzureRmServiceFabricClusterCertificate       기존 인증서를 롤오버하기 위해 클러스터에 보조 클러스터 인증서 추가
    + Add-AzureRmServiceFabricNodes       클러스터에 특정 노드 형식의 노드/VM 추가
    + Add-AzureRmServiceFabricNodeType       기존 클러스터에 노드 형식/VM 추가
    + Get-AzureRmServiceFabricCluster       클러스터 리소스의 세부 정보 가져오기
    + New-AzureRmServiceFabricCluster 새 ServiceFabric 클러스터를 만들기 이 명령은 다양한 시나리오에 적용되는 여러 오버로드를 제공합니다.
    + Remove-AzureRmServiceFabricClientCertificate       클러스터에 액세스하는 데 사용되는 클라이언트 인증서 제거
    + Remove-AzureRmServiceFabricClusterCertificate       클러스터 보안에 사용되지 않도록 클라이언트 인증서 제거
    + Remove-AzureRmServiceFabricNodes       클러스터에서 특정 노드 형식의 노드 제거
    + Remove-AzureRmServiceFabricNodeType       클러스터에서 노드 형식 제거
    + Remove-AzureRmServiceFabricSettings       클러스터에서 하나 이상의 ServiceFabric 설정 제거
    + Set-AzureRmServiceFabricSettings       클러스터의 하나 이상 ServiceFabric 설정 추가 또는 업데이트
    + Set-AzureRmServiceFabricUpgradeType       클러스터의 ServiceFabric 업그레이드 집합 변경
    + Update-AzureRmServiceFabricDurability       클러스터의 지속성 계층 변경
    + Update-AzureRmServiceFabricReliability       클러스터의 안정성 계층 변경
* Sql
  - New-AzureRmSqlDatabase에 -SampleName 매개 변수 추가
  - 장애 조치 그룹 cmdlet에 대한 업데이트
  - 'Tag' 매개 변수 제거
  - Remove-AzureRmSqlDatabaseFailoverGroup cmdlet에서 'PartnerResourceGroupName' 및 'PartnerServerName' 매개 변수 제거
  - New- 및 Set- cmdlet에 'GracePeriodWithDataLossHours' 매개 변수가 추가되고 결과적으로 'GracePeriodWithDataLossHour' 대신 사용됨
  - 설명서가 보완되고 업데이트되었습니다.
  - 반환된 개체의 서식 변경, 필드가 항상 채워지지는 않던 일부 버그 수정
  - 장애 조치(Failover) 그룹 개체에 'DatabaseNames' 및 'PartnerLocation' 속성 추가
  - Switch- cmdlet에서 작업이 완료되기를 기다리지 않고 즉시 반환되도록 하는 버그 수정
  - 높은 유예 기간 값이 사용되는 정수 오버플로 버그 수정
  - 더 낮은 값이 제공될 경우 유예 기간을 최소값인 1시간으로 조정
  - Set-AzureRmSqlDatabaseThreatDetectionPolicy cmdlet 및 Set-AzureRmSqlServerThreatDetectionPolicy cmdlet의 "ExcludedDetectionType" 매개 변수에 대해 허용되는 값 중에서 "Usage_Anomaly" 제거
* 스토리지
  - SRP SDK를 6.3.0으로 업그레이드
  - New/Set-AzureRmStorageAccount: EnableHttpsTrafficOnly를 지원하기 위한 새 매개 변수 추가
  - New/Set/Get-AzureRmStorageAccount: 반환된 스토리지 계정에 새 특성인 EnableHttpsTrafficOnly가 포함되어 있음
* Azure.Storage
  - Azure Storage 클라이언트 라이브러리 8.1.1 및 Azure Storage DataMovement 라이브러리 0.5.1로 업그레이드
  - Blob 증분 복사 기능을 지원하기 위한 새 cmdlet 추가
