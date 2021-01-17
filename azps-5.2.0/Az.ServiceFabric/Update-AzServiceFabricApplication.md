---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/update-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricApplication.md
ms.openlocfilehash: e53ed405c9a03e7a9ec7a7c3694a44d513a1a1ea
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98343322"
---
# Update-AzServiceFabricApplication

## SYNOPSIS
Service Fabric 애플리케이션을 업데이트합니다. 이렇게 하면 애플리케이션 매개 변수를 업데이트하고/또는 애플리케이션 업그레이드를 트리거하는 애플리케이션 유형 버전을 업그레이드할 수 있습니다. 배포된 ARM 지원됩니다.

## 구문

### ByResourceGroup(기본값)
```
Update-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [[-ApplicationTypeVersion] <String>] [-ApplicationParameter <Hashtable>] [-MinimumNodeCount <Int64>]
 [-MaximumNodeCount <Int64>] [-ForceRestart] [-UpgradeReplicaSetCheckTimeoutSec <Int32>]
 [-FailureAction <FailureAction>] [-HealthCheckRetryTimeoutSec <Int32>] [-HealthCheckWaitDurationSec <Int32>]
 [-HealthCheckStableDurationSec <Int32>] [-UpgradeDomainTimeoutSec <Int32>] [-UpgradeTimeoutSec <Int32>]
 [-ConsiderWarningAsError] [-DefaultServiceTypeMaxPercentUnhealthyPartitionsPerService <Int32>]
 [-DefaultServiceTypeMaxPercentUnhealthyReplicasPerPartition <Int32>]
 [-DefaultServiceTypeUnhealthyServicesMaxPercent <Int32>] [-UnhealthyDeployedApplicationsMaxPercent <Int32>]
 [-ServiceTypeHealthPolicyMap <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByResourceId
```
Update-AzServiceFabricApplication [[-ApplicationTypeVersion] <String>] [-ApplicationParameter <Hashtable>]
 [-MinimumNodeCount <Int64>] [-MaximumNodeCount <Int64>] [-ForceRestart]
 [-UpgradeReplicaSetCheckTimeoutSec <Int32>] [-FailureAction <FailureAction>]
 [-HealthCheckRetryTimeoutSec <Int32>] [-HealthCheckWaitDurationSec <Int32>]
 [-HealthCheckStableDurationSec <Int32>] [-UpgradeDomainTimeoutSec <Int32>] [-UpgradeTimeoutSec <Int32>]
 [-ConsiderWarningAsError] [-DefaultServiceTypeMaxPercentUnhealthyPartitionsPerService <Int32>]
 [-DefaultServiceTypeMaxPercentUnhealthyReplicasPerPartition <Int32>]
 [-DefaultServiceTypeUnhealthyServicesMaxPercent <Int32>] [-UnhealthyDeployedApplicationsMaxPercent <Int32>]
 [-ServiceTypeHealthPolicyMap <Hashtable>] [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByInputObject
```
Update-AzServiceFabricApplication -InputObject <PSApplication> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명
이 cmdlet을 사용하여 애플리케이션 매개 변수를 업데이트하고 애플리케이션 유형 버전을 업그레이드할 수 있습니다. 매개 변수를 업데이트하면 새 형식 버전이 사용되는 ARM 모델만 변경됩니다. 명령은 애플리케이션 업그레이드를 트리거합니다. 지정된 형식 버전은 **New-AzServiceFabricApplicationTypeVersion을** 사용하여 클러스터에 이미 만들어야 합니다.

## 예제

### 예제 1
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $version = "v2"
PS C:\> $packageUrl = "https://sftestapp.blob.core.windows.net/sftestapp/testAppType_v2.sfpkg"
PS C:\> New-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName -Version $version -PackageUrl $packageUrl -Verbose
PS C:\> Update-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationTypeVersion $version -Name $appName -ApplicationParameter @{key0="value0";key1=$null;key2="value2"}
```

이 예제에서는 **New-AzServiceFabricApplicationTypeVersion으로** 만든 형식 버전을 "v2"로 업데이트하는 애플리케이션 업그레이드를 시작합니다. 사용되는 애플리케이션 매개 변수는 애플리케이션 매니페스트에 정의해야 합니다.

### 예제 2
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Update-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName -MinimumNodes 1 -MaximumNodes 4 -Verbose
```

이 예제에서는 애플리케이션에 대한 최소 및 최대 노드 수 제한을 업데이트합니다.

### 예제 3
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $version = "v2"
PS C:\> $packageUrl = "https://sftestapp.blob.core.windows.net/sftestapp/testAppType_v2.sfpkg"
PS C:\> New-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName -Version $version -PackageUrl $packageUrl -Verbose
PS C:\> Update-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationTypeVersion $version -Name $appName -ApplicationParameter @{key0="value0";key1=$null;key2="value2"} -HealthCheckStableDurationSec 0 -HealthCheckWaitDurationSec 0 -HealthCheckRetryTimeoutSec 0 -UpgradeDomainTimeoutSec 5000 -UpgradeTimeoutSec 7000 -FailureAction Rollback -UpgradeReplicaSetCheckTimeoutSec 300 -ForceRestart
```

이 예제에서는 유형 버전을 "v2"로 업데이트하는 애플리케이션 업그레이드를 시작하고 현재 업그레이드에서 적용될 일부 업그레이드 정책 매개 변수도 설정합니다.

### 예제 4
```powershell
PS C:\> Update-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName -ApplicationParameter @{key0="value0";key1=$null;key2="value2"}
```

이 예제에서는 애플리케이션 매개 변수를 업데이트하지만 이러한 변경 내용은 다음 버전이 애플리케이션으로 업그레이드될 때까지만 적용됩니다.

## PARAMETERS

### -ApplicationParameter
애플리케이션 매개 변수를 키/값 쌍으로 지정합니다.
이러한 매개 변수는 애플리케이션 매니페스트에 있어야 합니다.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ApplicationTypeVersion
애플리케이션 유형 버전 지정

```yaml
Type: System.String
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ClusterName
클러스터의 이름을 지정합니다.

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ConsiderWarningAsError
상태 평가 중에 경고 상태 이벤트를 오류 이벤트로 취급할지 여부를 나타냅니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultServiceTypeMaxPercentUnhealthyPartitionsPerService
모니터링된 업그레이드에 사용할 기본 서비스 유형에 대한 상태 정책에서 허용하는 서비스당 미지정 파티션의 최대 백분율을 지정합니다.

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultServiceTypeMaxPercentUnhealthyReplicasPerPartition
모니터링되는 업그레이드에 사용할 기본 서비스 유형에 대한 상태 정책에서 허용하는 서비스당 미지정 복제본의 최대 백분율을 지정합니다.

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultServiceTypeUnhealthyServicesMaxPercent
모니터링된 업그레이드에 사용할 기본 서비스 유형에 대한 상태 정책에서 허용하는 비보안 서비스의 최대 백분율을 지정합니다.

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FailureAction
모니터링되는 업그레이드가 실패하는 경우 취할 작업을 지정합니다.
이 매개 변수에 허용되는 값은 Rollback 또는 Manual입니다.

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.FailureAction
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:
Accepted values: Rollback, Manual

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ForceRestart
업그레이드가 구성 전용 변경인 경우에도 서비스 호스트가 다시 시작된다고 나타냅니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HealthCheckRetryTimeoutSec
이전 상태 검사가 실패하면 Service Fabric이 상태 검사를 다시 검색하는 기간(초)을 지정합니다.

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HealthCheckStableDurationSec
Service Fabric이 다음 업그레이드 도메인으로 이동하거나 업그레이드를 완료하기 전에 애플리케이션이 안정적인지 확인하기 위해 대기하는 기간(초)을 지정합니다.
이 대기 기간은 상태 검사가 수행된 직후에 확인되지 않도록 상태 변경을 방지합니다.

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HealthCheckWaitDurationSec
Service Fabric이 업그레이드 도메인에서 업그레이드를 완료한 후 초기 상태 검사를 수행하기 전에 대기하는 기간(초)을 지정합니다.

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
애플리케이션 리소스입니다.

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -MaximumNodeCount
애플리케이션을 두는 노드의 최대 수를 지정합니다.

```yaml
Type: System.Int64
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MinimumNodeCount
Service Fabric이 이 애플리케이션에 대한 용량을 예약하는 노드의 최소 수를 지정합니다.

```yaml
Type: System.Int64
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
애플리케이션의 이름 지정

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases: ApplicationName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
리소스 그룹의 이름을 지정합니다.

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
애플리케이션의 Arm ResourceId입니다.

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServiceTypeHealthPolicyMap
다양한 서비스 유형에 사용할 상태 정책 맵을 @"ServiceTypeName" @ {"ServiceTypeName" : "MaxPercentUnhealthyPartitionsPerService,MaxPercentUnhealthyReplicasPerPartition,MaxPercentUnhealthyServices"}}으로 지정합니다.
예: @{ "ServiceTypeName01" = "5,10,5"; "ServiceTypeName02" = "5,5,5" }

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UnhealthyDeployedApplicationsMaxPercent
클러스터의 애플리케이션 상태 오류가 발생하기 전에 클러스터의 노드에 배포된 애플리케이션 인스턴스의 최대 백분율을 지정합니다.

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UpgradeDomainTimeoutSec
Service Fabric이 단일 업그레이드 도메인을 업그레이드하는 데 걸리는 최대 시간(초)을 지정합니다.
이 기간 후에 업그레이드가 실패합니다.

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UpgradeReplicaSetCheckTimeoutSec
Service Fabric이 업그레이드를 진행하기 전에 서비스 패브릭이 안전한 상태로 재구성할 때까지 대기하는 최대 시간을 지정합니다(안전 상태가 아닌 경우).

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UpgradeTimeoutSec
Service Fabric이 전체 업그레이드에 걸리는 최대 시간(초)을 지정합니다.
이 기간 후에 업그레이드가 실패합니다.

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
cmdlet이 실행되는 경우의 결과 표시
cmdlet이 실행되지 않습니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## 입력

### System.String

### Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication

## 출력

### Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication

## 참고 사항

## 관련 링크
