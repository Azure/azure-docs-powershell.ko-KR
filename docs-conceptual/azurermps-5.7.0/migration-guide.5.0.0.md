---
title: Microsoft Azure PowerShell 5.0.0의 주요 변경 내용
description: 이 마이그레이션 가이드에는 Azure PowerShell 버전 5 릴리스에 이루어진 호환성이 손상되는 변경의 목록이 포함되어 있습니다.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/01/2018
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 81f52ee8b84f60d59a7f2d53b6675129ac054fd6
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/01/2020
ms.locfileid: "89243738"
---
# <a name="breaking-changes-for-microsoft-azure-powershell-500"></a>Microsoft Azure PowerShell 5.0.0의 주요 변경 내용

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

이 문서는 Microsoft Azure PowerShell cmdlet의 소비자를 위한 주요 변경 내용 알림 및 마이그레이션 가이드 역할을 합니다. 각 섹션에서는 주요 변경에 대한 원동력과 최소 저항의 마이그레이션 경로에 대해 설명합니다. 심층적인 맥락에서는 각 변경 내용과 관련된 끌어오기 요청을 참조하세요.

## <a name="table-of-contents"></a>목차

- [ApiManagement cmdlet의 주요 변경 내용](#breaking-changes-to-apimanagement-cmdlets)
- [Batch cmdlet의 주요 변경 내용](#breaking-changes-to-batch-cmdlets)
- [Compute cmdlet의 호환성이 손상되는 변경](#breaking-changes-to-compute-cmdlets)
- [EventHub cmdlet의 주요 변경 내용](#breaking-changes-to-eventhub-cmdlets)
- [Insights cmdlet의 주요 변경 내용](#breaking-changes-to-insights-cmdlets)
- [Network cmdlet의 주요 변경 내용](#breaking-changes-to-network-cmdlets)
- [Resources cmdlet의 주요 변경 내용](#breaking-changes-to-resources-cmdlets)
- [ServiceBus cmdlet의 주요 변경 내용](#breaking-changes-to-servicebus-cmdlets)

## <a name="breaking-changes-to-apimanagement-cmdlets"></a>ApiManagement cmdlet의 주요 변경 내용

### <a name="new-azurermapimanagementbackendproxy"></a>**New-AzureRmApiManagementBackendProxy**
- 매개 변수 "UserName" 및 "Password"가 PSCredential에 대해 대체됨

```powershell-interactive
# Old
New-AzureRmApiManagementBackendProxy [other required parameters] -UserName "plain-text string" -Password "plain-text string"

# New
New-AzureRmApiManagementBackendProxy [other required parameters] -Credential $PSCredentialVariable
```

### <a name="new-azurermapimanagementuser"></a>**New-AzureRmApiManagementUser**
- 매개 변수 "Password"가 SecureString에 대해 대체됨

```powershell-interactive
# Old
New-AzureRmApiManagementUser [other required parameters] -Password "plain-text string"

# New
New-AzureRmApiManagementUser [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermapimanagementuser"></a>**Set-AzureRmApiManagementUser**
- 매개 변수 "Password"가 SecureString에 대해 대체됨

```powershell-interactive
# Old
Set-AzureRmApiManagementUser [other required parameters] -Password "plain-text string"

# New
Set-AzureRmApiManagementUser [other required parameters] -Password $SecureStringVariable
```

## <a name="breaking-changes-to-batch-cmdlets"></a>Batch cmdlet의 주요 변경 내용

### <a name="new-azurebatchcertificate"></a>**New-AzureBatchCertificate**
- 매개 변수 `Password`가 보안 문자열에 대해 대체됨

```powershell-interactive
# Old
New-AzureBatchCertificate [other required parameters] -Password "plain-text string"

# New
New-AzureBatchCertificate [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurebatchcomputenodeuser"></a>**New-AzureBatchComputeNodeUser**
- 매개 변수 `Password`가 보안 문자열에 대해 대체됨

```powershell-interactive
# Old
New-AzureBatchComputeNodeUser [other required parameters] -Password "plain-text string"

# New
New-AzureBatchComputeNodeUser [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermbatchcomputenodeuser"></a>**Set-AzureRmBatchComputeNodeUser**
- 매개 변수 `Password`가 보안 문자열에 대해 대체됨

```powershell-interactive
# Old
Set-AzureRmBatchComputeNodeUser [other required parameters] -Password "plain-text string"

# New
Set-AzureRmBatchComputeNodeUser [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurebatchtask"></a>**New-AzureBatchTask**
 - `RunElevated` 스위치가 제거되고 `UserIdentity`로 대체되었습니다.

```powershell-interactive
# Old
New-AzureBatchTask -Id $taskId1 -JobId $jobId -CommandLine "cmd /c echo hello" -RunElevated $TRUE

# New
$autoUser = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoUserSpecification -ArgumentList @("Task", "Admin")
$userIdentity = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserIdentity $autoUser
New-AzureBatchTask -Id $taskId1 -JobId $jobId -CommandLine "cmd /c echo hello" -UserIdentity $userIdentity
```

또한 `PSCloudTask`, `PSStartTask`, `PSJobManagerTask`, `PSJobPreparationTask` 및 `PSJobReleaseTask`의 `RunElevated` 속성에 영향을 줍니다.

### <a name="psmultiinstancesettings"></a>**PSMultiInstanceSettings**

- `PSMultiInstanceSettings` 생성자는 더 이상 필수 `numberOfInstances` 매개 변수를 사용하지 않고 대신 필수 `coordinationCommandLine` 매개 변수를 사용합니다.

```powershell-interactive
# Old
$settings = New-Object Microsoft.Azure.Commands.Batch.Models.PSMultiInstanceSettings -ArgumentList @(2)
$settings.CoordinationCommandLine = "cmd /c echo hello"
New-AzureBatchTask [other parameters] -MultiInstanceSettings $settings

# New
$settings = New-Object Microsoft.Azure.Commands.Batch.Models.PSMultiInstanceSettings -ArgumentList @("cmd /c echo hello", 2)
New-AzureBatchTask [other parameters] -MultiInstanceSettings $settings
```

### <a name="get-azurebatchtask"></a>**Get-AzureBatchTask**
 - `PSCloudTask`에서 `RunElevated` 속성이 제거되었습니다. `UserIdentity`를 대체하기 위해 `RunElevated` 속성이 추가되었습니다.

```powershell-interactive
# Old
$task = Get-AzureBatchTask [parameters]
$task.RunElevated

# New
$task = Get-AzureBatchTask [parameters]
$task.UserIdentity.AutoUser.ElevationLevel
```

또한 `PSCloudTask`, `PSStartTask`, `PSJobManagerTask`, `PSJobPreparationTask` 및 `PSJobReleaseTask`의 `RunElevated` 속성에 영향을 줍니다.

### <a name="multiple-types"></a>**여러 형식**

- `PSExitConditions`에서 `SchedulingError` 속성의 이름이 `PreProcessingError`로 변경되었습니다.

```powershell-interactive
# Old
$task = Get-AzureBatchTask [parameters]
$task.ExitConditions.SchedulingError

# New
$task = Get-AzureBatchTask [parameters]
$task.ExitConditions.PreProcessingError
```

### <a name="multiple-types"></a>**여러 형식**

- `PSJobPreparationTaskExecutionInformation`, `PSJobReleaseTaskExecutionInformation`, `PSStartTaskInformation`, `PSSubtaskInformation` 및 `PSTaskExecutionInformation`에서 `SchedulingError` 속성의 이름이 `FailureInformation`으로 변경되었습니다.
  - 작업 실패가 있을 때마다 `FailureInformation`이 반환됩니다. 여기에는 이전의 모든 예약 오류 사례는 물론, 0이 아닌 작업 종료 코드 및 새 출력 파일 기능의 파일 업로드 오류가 포함됩니다.
  - 이것은 이전과 동일하게 구성되므로 이 형식을 사용할 때는 코드 변경 내용이 필요하지 않습니다.

```powershell-interactive
# Old
$task = Get-AzureBatchTask [parameters]
$task.ExecutionInformation.SchedulingError

# New
$task = Get-AzureBatchTask [parameters]
$task.ExecutionInformation.FailureInformation
```

또한 이것은 다음에 영향을 줍니다. Get-AzureBatchPool, Get-AzureBatchSubtask, Get-AzureBatchJobPreparationAndReleaseTaskStatus

### <a name="new-azurebatchpool"></a>**New-AzureBatchPool**
 - `TargetDedicated`가 제거되고 `TargetDedicatedComputeNodes` 및 `TargetLowPriorityComputeNodes`로 대체되었습니다.
 - `TargetDedicatedComputeNodes`에 `TargetDedicated` 별칭이 있습니다.

```powershell-interactive
# Old
New-AzureBatchPool [other parameters] [-TargetDedicated <Int32>]

# New
New-AzureBatchPool [other parameters] [-TargetDedicatedComputeNodes <Int32>] [-TargetLowPriorityComputeNodes <Int32>]
```

또한 이것은 다음에 영향을 줍니다. Start-AzureBatchPoolResize

### <a name="get-azurebatchpool"></a>**Get-AzureBatchPool**
 - `PSCloudPool`에서 `TargetDedicated` 및 `CurrentDedicated` 속성 이름이 `TargetDedicatedComputeNodes` 및 `CurrentDedicatedComputeNodes`로 변경되었습니다.

```powershell-interactive
# Old
$pool = Get-AzureBatchPool [parameters]
$pool.TargetDedicated
$pool.CurrentDedicated

# New
$pool = Get-AzureBatchPool [parameters]
$pool.TargetDedicatedComputeNodes
$pool.CurrentDedicatedComputeNodes
```

### <a name="type-pscloudpool"></a>**PSCloudPool 형식**

- `PSCloudPool`에서 `ResizeError`의 이름이 `ResizeErrors`로 변경되었고 이제 컬렉션입니다.

```powershell-interactive
# Old
$pool = Get-AzureBatchPool [parameters]
$pool.ResizeError

# New
$pool = Get-AzureBatchPool [parameters]
$pool.ResizeErrors[0]
```

### <a name="new-azurebatchjob"></a>**New-AzureBatchJob**
- `PSPoolSpecification`에서 `TargetDedicated` 속성의 이름이 `TargetDedicatedComputeNodes`로 변경되었습니다.

```powershell-interactive
# Old
$poolInfo = New-Object Microsoft.Azure.Commands.Batch.Models.PSPoolInformation
$poolInfo.AutoPoolSpecification = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoPoolSpecification
$poolInfo.AutoPoolSpecification.PoolSpecification = New-Object Microsoft.Azure.Commands.Batch.Models.PSPoolSpecification
$poolInfo.AutoPoolSpecification.PoolSpecification.TargetDedicated = 5
New-AzureBatchJob [other parameters] -PoolInformation $poolInfo

# New
$poolInfo = New-Object Microsoft.Azure.Commands.Batch.Models.PSPoolInformation
$poolInfo.AutoPoolSpecification = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoPoolSpecification
$poolInfo.AutoPoolSpecification.PoolSpecification = New-Object Microsoft.Azure.Commands.Batch.Models.PSPoolSpecification
$poolInfo.AutoPoolSpecification.PoolSpecification.TargetDedicatedComputeNodes = 5
New-AzureBatchJob [other parameters] -PoolInformation $poolInfo
```

### <a name="get-azurebatchnodefile"></a>**Get-AzureBatchNodeFile**
 - `Name`이 제거되고 `Path`로 대체되었습니다.
 - `Path`에 `Name` 별칭이 있습니다.

```powershell-interactive
# Old
Get-AzureBatchNodeFile [other parameters] [[-Name] <String>]

# New
Get-AzureBatchNodeFile [other parameters] [[-Path] <String>]
```

또한 이것은 다음에 영향을 줍니다. Get-AzureBatchNodeFileContent, Remove-AzureBatchNodeFile

### <a name="type-psnodefile"></a>**PSNodeFile** 형식

 - `PSNodeFile`에서 `Name` 속성의 이름이 `Path`로 변경되었습니다.

```powershell-interactive
# Old
$file = Get-AzureBatchNodeFile [parameters]
$file.Name

# New
$file = Get-AzureBatchNodeFile [parameters]
$file.Path
```

### <a name="get-azurebatchsubtask"></a>**Get-AzureBatchSubtask**
- `PSSubtaskInformation`의 `PreviousState` 및 `State` 속성은 더 이상 `TaskState` 형식이 아니며, 대신 `SubtaskState` 형식입니다.
  - 하위 작업이 `Active` 상태가 될 수 없으므로, `TaskState`와 달리, `SubtaskState`에는 `Active` 값이 없습니다.

```powershell-interactive
# Old
$subtask = Get-AzureBatchSubtask [parameters]
if ($subtask.State -eq Microsoft.Azure.Batch.Common.TaskState.Running) { }

# New
$subtask = Get-AzureBatchSubtask [parameters]
if ($subtask.State -eq Microsoft.Azure.Batch.Common.SubtaskState.Running) { }
```

## <a name="breaking-changes-to-compute-cmdlets"></a>Compute cmdlet의 호환성이 손상되는 변경

### <a name="set-azurermvmaccessextension"></a>**Set-AzureRmVMAccessExtension**
- 매개 변수 "UserName" 및 "Password"가 PSCredential에 대해 대체됨

```powershell-interactive
# Old
Set-AzureRmVMAccessExtension [other required parameters] -UserName "plain-text string" -Password "plain-text string"

# New
Set-AzureRmVMAccessExtension [other required parameters] -Credential $PSCredential
```

## <a name="breaking-changes-to-eventhub-cmdlets"></a>EventHub cmdlet의 주요 변경 내용

### <a name="new-azurermeventhubnamespaceauthorizationrule"></a>**New-AzureRmEventHubNamespaceAuthorizationRule**
- 'New-AzureRmEventHubNamespaceAuthorizationRule' cmdlet이 제거되었습니다. 'New-AzureRmEventHubAuthorizationRule' cmdlet을 사용하세요.

### <a name="get-azurermeventhubnamespaceauthorizationrule"></a>**Get-AzureRmEventHubNamespaceAuthorizationRule**
- 'Get-AzureRmEventHubNamespaceAuthorizationRule' cmdlet이 제거되었습니다. 'Get-AzureRmEventHubAuthorizationRule' cmdlet을 사용하세요.

### <a name="set-azurermeventhubnamespaceauthorizationrule"></a>**Set-AzureRmEventHubNamespaceAuthorizationRule**
- 'Set-AzureRmEventHubNamespaceAuthorizationRule' cmdlet이 제거되었습니다. 'Set-AzureRmEventHubAuthorizationRule' cmdlet을 사용하세요.

### <a name="remove-azurermeventhubnamespaceauthorizationrule"></a>**Remove-AzureRmEventHubNamespaceAuthorizationRule**
- 'Remove-AzureRmEventHubNamespaceAuthorizationRule' cmdlet이 제거되었습니다. 'Remove-AzureRmEventHubAuthorizationRule' cmdlet을 사용하세요.

### <a name="new-azurermeventhubnamespacekey"></a>**New-AzureRmEventHubNamespaceKey**
- 'New-AzureRmEventHubNamespaceKey' cmdlet이 제거되었습니다. 'New-AzureRmEventHubKey' cmdlet을 사용하세요.

### <a name="get-azurermeventhubnamespacekey"></a>**Get-AzureRmEventHubNamespaceKey**
- 'Get-AzureRmEventHubNamespaceKey' cmdlet이 제거되었습니다. 'Get-AzureRmEventHubKey' cmdlet을 사용하세요.

### <a name="new-azurermeventhubnamespace"></a>**New-AzureRmEventHubNamespace**
- NamespceAttributes의 'Status' 및 'Enabled' 속성이 제거되었습니다.

```powershell-interactive
# Old
# The $namespace has Status and Enabled property
$namespace = New-AzureRmEventHubNamespace <parameters>
$namespace.Status
$namespace.Enabled

# New
# The call remains the same, but the returned values NameSpace object will not have the Status and Enabled property
$namespace = Get-AzureRmEventHubNamespace <parameters>
```

### <a name="get-azurermeventhubnamespace"></a>**Get-AzureRmEventHubNamespace**
- NamespceAttributes의 'Status' 및 'Enabled' 속성이 제거되었습니다.

```powershell-interactive
# Old
# The $namespace has Status and Enabled property
$namespace = Get-AzureRmEventHubNamespace <parameters>
$namespace.Status
$namespace.Enabled

# New
# The call remains the same, but the returned values NameSpace object will not have the Status and Enabled property
$namespace = Get-AzureRmEventHubNamespace <parameters>
```

### <a name="set-azurermeventhubnamespace"></a>**Set-AzureRmEventHubNamespace**
- NamespceAttributes의 'Status' 및 'Enabled' 속성이 제거되었습니다.

```powershell-interactive
# Old
# The $namespace has Status and Enabled property
$namespace = Set-AzureRmEventHubNamespace <parameters>
$namespace.Status
$namespace.Enabled

# New
# The call remains the same, but the returned values NameSpace object will not have the Status and Enabled property
$namespace = Set-AzureRmEventHubNamespace <parameters>
```

### <a name="new-azurermeventhubconsumergroup"></a>**New-AzureRmEventHubConsumerGroup**
- ConsumerGroupAttributes의 'EventHubPath' 속성이 제거되었습니다.

```powershell-interactive
# Old
# The $consumergroup has EventHubPath property
$consumergroup = New-AzureRmEventHubConsumerGroup <parameters>
$consumergroup.EventHubPath

# New
# The call remains the same, but the returned values ConsumerGroup object will not have the EventHubPath property
$consumergroup = New-AzureRmEventHubConsumerGroup <parameters>
```

### <a name="set-azurermeventhubconsumergroup"></a>**Set-AzureRmEventHubConsumerGroup**
- ConsumerGroupAttributes의 'EventHubPath' 속성이 제거되었습니다.

```powershell-interactive
# Old
# The $consumergroup has EventHubPath property
$consumergroup = Set-AzureRmEventHubConsumerGroup <parameters>
$consumergroup.EventHubPath

# New
# The call remains the same, but the returned values ConsumerGroup object will not have the EventHubPath property
$consumergroup = Set-AzureRmEventHubConsumerGroup <parameters>
```

### <a name="get-azurermeventhubconsumergroup"></a>**Get-AzureRmEventHubConsumerGroup**
- ConsumerGroupAttributes의 'EventHubPath' 속성이 제거되었습니다.

```powershell-interactive
# Old
# The $consumergroup has EventHubPath property
$consumergroup = Get-AzureRmEventHubConsumerGroup <parameters>
$consumergroup.EventHubPath

# New
# The call remains the same, but the returned values ConsumerGroup object will not have the EventHubPath property
$consumergroup = Get-AzureRmEventHubConsumerGroup <parameters>
```

## <a name="breaking-changes-to-insights-cmdlets"></a>Insights cmdlet의 주요 변경 내용

### <a name="add-azurermlogalertrule"></a>**Add-AzureRMLogAlertRule**
- **Add-AzureRMLogAlertRule** cmdlet이 더 이상 사용되지 않습니다.
- 이 cmdlet을 사용하는 10월 1일 이후에는 이 기능이 활동 로그 경고로 전환되므로 더 이상 유효하지 않습니다. 자세한 내용은 https://aka.ms/migratemealerts 을 참조하세요.

### <a name="get-azurermusage"></a>**Get-AzureRMUsage**
- **Get-AzureRMUsage** cmdlet이 더 이상 사용되지 않습니다.

### <a name="get-azurermalerthistory--get-azurermautoscalehistory--get-azurermlogs"></a>**Get-AzureRmAlertHistory** / **Get-AzureRmAutoscaleHistory** / **Get-AzureRmLogs**
- 출력 변경: 이제 상수 값(Admin,Operation)을 반환하므로 EventData 개체(이러한 cmdlet에서 반환됨)의 EventChannels 필드가 더 이상 사용되지 않습니다.

### <a name="get-azurermalertrule"></a>**Get-AzureRmAlertRule**
- 출력 변경: 이 cmdlet의 출력이 평면화되어, 즉 속성 필드가 제거되어 사용자 환경이 개선될 것입니다.

```powershell-interactive
# Old
$rules = Get-AzureRmAlertRule -ResourceGroup $resourceGroup
if ($rules -and $rules.count -ge 1)
{
    Write-Host -Foreground Red "Error updating alert rule"
    Write-Host $rules[0].Id
    Write-Host $rules[0].Properties.IsEnabled
    Write-Host $rules[0].Properties.Condition
}

# New
$rules = Get-AzureRmAlertRule -ResourceGroup $resourceGroup
if ($rules -and $rules.count -ge 1)
{
    Write-Host -Foreground red "Error updating alert rule"
    Write-Host $rules[0].Id

    # Properties will remain for a while
    Write-Host $rules[0].Properties.IsEnabled

    # But the properties will be at the top level too. Later Properties will be removed
    Write-Host $rules[0].IsEnabled
    Write-Host $rules[0].Condition
}
```

### <a name="get-azurermautoscalesetting"></a>**Get-AzureRmAutoscaleSetting**
- 출력 변경: AutoscaleSettingResourceName 필드는 항상 이름 필드와 같으므로 더 이상 사용되지 않습니다.

```powershell-interactive
# Old
$s1 = Get-AzureRmAutoscaleSetting -ResourceGroup $resourceGroup -Name MySetting
if ($s1.AutoscaleSettingResourceName -ne $s1.Name)
{
    Write-Host "There is something wrong with the name"
}

# New
$s1 = Get-AzureRmAutoscaleSetting -ResourceGroup $resourceGroup -Name MySetting

# there won't be a AutoscaleSettingResourceName
Write-Host $s1.Name
```

### <a name="remove-azurermalertrule--remove-azurermlogprofile"></a>**Remove-AzureRmAlertRule** / **Remove-AzureRmLogProfile**
- 출력 변경: 출력 형식은 요청 ID 및 상태 코드가 포함된 단일 개체를 반환하도록 변경됩니다.

```powershell-interactive
# Old
$s1 = Remove-AzureRmAlertRule -ResourceGroup $resourceGroup -name $ruleName
if ($s1 -ne $null)
{
    $r = $s1[0].RequestId
    $s = $s1[0].StatusCode
}

# New
$s1 = Remove-AzureRmAlertRule -ResourceGroup $resourceGroup -name $ruleName
$r = $s1.RequestId
$s = $s1.StatusCode
```

## <a name="breaking-changes-to-network-cmdlets"></a>Network cmdlet의 주요 변경 내용

### <a name="add-azurermapplicationgatewaysslcertificate"></a>**Add-AzureRmApplicationGatewaySslCertificate**
- 매개 변수 "Password"가 SecureString에 대해 대체됨

```powershell-interactive
# Old
Add-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password "plain-text string"

# New
Add-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermapplicationgatewaysslcertificate"></a>**New-AzureRmApplicationGatewaySslCertificate**
- 매개 변수 "Password"가 SecureString에 대해 대체됨

```powershell-interactive
# Old
New-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password "plain-text string"

# New
New-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermapplicationgatewaysslcertificate"></a>**Set-AzureRmApplicationGatewaySslCertificate**
- 매개 변수 "Password"가 SecureString에 대해 대체됨

```powershell-interactive
# Old
Set-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password "plain-text string"

# New
Set-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password $SecureStringVariable
```

## <a name="breaking-changes-to-resources-cmdlets"></a>Resources cmdlet의 주요 변경 내용

### <a name="new-azurermadappcredential"></a>**New-AzureRmADAppCredential**
- 매개 변수 "Password"가 SecureString에 대해 대체됨

```powershell-interactive
# Old
New-AzureRmADAppCredential [other required parameters] -Password "plain-text string"

# New
New-AzureRmADAppCredential [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermadapplication"></a>**New-AzureRmADApplication**
- 매개 변수 "Password"가 SecureString에 대해 대체됨

```powershell-interactive
# Old
New-AzureRmADApplication [other required parameters] -Password "plain-text string"

# New
New-AzureRmADApplication [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermadserviceprincipal"></a>**New-AzureRmADServicePrincipal**
- 매개 변수 "Password"가 SecureString에 대해 대체됨

```powershell-interactive
# Old
New-AzureRmADServicePrincipal [other required parameters] -Password "plain-text string"

# New
New-AzureRmADServicePrincipal [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermadspcredential"></a>**New-AzureRmADSpCredential**
- 매개 변수 "Password"가 SecureString에 대해 대체됨

```powershell-interactive
# Old
New-AzureRmADSpCredential [other required parameters] -Password "plain-text string"

# New
New-AzureRmADSpCredential [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermaduser"></a>**New-AzureRmADUser**
- 매개 변수 "Password"가 SecureString에 대해 대체됨

```powershell-interactive
# Old
New-AzureRmADUser [other required parameters] -Password "plain-text string"

# New
New-AzureRmADUser [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermaduser"></a>**Set-AzureRmADUser**
- 매개 변수 "Password"가 SecureString에 대해 대체됨

```powershell-interactive
# Old
Set-AzureRmADUser [other required parameters] -Password "plain-text string"

# New
Set-AzureRmADUser [other required parameters] -Password $SecureStringVariable
```

## <a name="breaking-changes-to-servicebus-cmdlets"></a>ServiceBus cmdlet의 주요 변경 내용

### <a name="get-azurermservicebustopicauthorizationrule"></a>**Get-AzureRmServiceBusTopicAuthorizationRule**
- 'Get-AzureRmServiceBusTopicAuthorizationRule' cmdlet이 제거되었습니다. 'Get-AzureRmServiceBusAuthorizationRule' cmdlet을 사용하세요.

### <a name="get-azurermservicebustopickey"></a>**Get-AzureRmServiceBusTopicKey**
- 'Get-AzureRmServiceBusTopicKey' cmdlet이 제거되었습니다. 'Get-AzureRmServiceBusKey' cmdlet을 사용하세요.

### <a name="new-azurermservicebustopicauthorizationrule"></a>**New-AzureRmServiceBusTopicAuthorizationRule**
- 'New-AzureRmServiceBusTopicAuthorizationRule' cmdlet이 제거되었습니다. 'New-AzureRmServiceBusAuthorizationRule' cmdlet을 사용하세요.

### <a name="new-azurermservicebustopickey"></a>**New-AzureRmServiceBusTopicKey**
- 'New-AzureRmServiceBusTopicKey' cmdlet이 제거되었습니다. 'New-AzureRmServiceBusKey' cmdlet을 사용하세요.

### <a name="remove-azurermservicebustopicauthorizationrule"></a>**Remove-AzureRmServiceBusTopicAuthorizationRule**
- 'Remove-AzureRmServiceBusTopicAuthorizationRule' cmdlet이 제거되었습니다. 'Remove-AzureRmServiceBusAuthorizationRule' cmdlet을 사용하세요.

### <a name="set-azurermservicebustopicauthorizationrule"></a>**Set-AzureRmServiceBusTopicAuthorizationRule**
- 'Set-AzureRmServiceBusTopicAuthorizationRule' cmdlet이 제거되었습니다. 'Set-AzureRmServiceBusAuthorizationRule' cmdlet을 사용하세요.

### <a name="new-azurermservicebusnamespacekey"></a>**New-AzureRmServiceBusNamespaceKey**
- 'New-AzureRmServiceBusNamespaceKey' cmdlet이 제거되었습니다. 'New-AzureRmServiceBusKey' cmdlet을 사용하세요.

### <a name="get-azurermservicebusqueueauthorizationrule"></a>**Get-AzureRmServiceBusQueueAuthorizationRule**
- 'Get-AzureRmServiceBusQueueAuthorizationRule' cmdlet이 제거되었습니다. 'Get-AzureRmServiceBusAuthorizationRule' cmdlet을 사용하세요.

### <a name="get-azurermservicebusqueuekey"></a>**Get-AzureRmServiceBusQueueKey**
- 'Get-AzureRmServiceBusQueueKey' cmdlet이 제거되었습니다. 'Get-AzureRmServiceBusKey' cmdlet을 사용하세요.

### <a name="new-azurermservicebusqueueauthorizationrule"></a>**New-AzureRmServiceBusQueueAuthorizationRule**
- 'New-AzureRmServiceBusQueueAuthorizationRule' cmdlet이 제거되었습니다. 'New-AzureRmServiceBusAuthorizationRule' cmdlet을 사용하세요.

### <a name="new-azurermservicebusqueuekey"></a>**New-AzureRmServiceBusQueueKey**
- 'New-AzureRmServiceBusQueueKey' cmdlet이 제거되었습니다. 'New-AzureRmServiceBusKey' cmdlet을 사용하세요.

### <a name="remove-azurermservicebusqueueauthorizationrule"></a>**Remove-AzureRmServiceBusQueueAuthorizationRule**
- 'Remove-AzureRmServiceBusQueueAuthorizationRule' cmdlet이 제거되었습니다. 'GRemove-AzureRmServiceBusAuthorizationRule' cmdlet을 사용하세요.

### <a name="set-azurermservicebusqueueauthorizationrule"></a>**Set-AzureRmServiceBusQueueAuthorizationRule**
- 'Set-AzureRmServiceBusQueueAuthorizationRule' cmdlet이 제거되었습니다. 'Set-AzureRmServiceBusAuthorizationRule' cmdlet을 사용하세요.

### <a name="get-azurermservicebusnamespaceauthorizationrule"></a>**Get-AzureRmServiceBusNamespaceAuthorizationRule**
- 'Get-AzureRmServiceBusNamespaceAuthorizationRule' cmdlet이 제거되었습니다. 'Get-AzureRmServiceBusAuthorizationRule' cmdlet을 사용하세요.

### <a name="get-azurermservicebusnamespacekey"></a>**Get-AzureRmServiceBusNamespaceKey**
- 'Get-AzureRmServiceBusNamespaceKey' cmdlet이 제거되었습니다. 'Get-AzureRmServiceBusKey' cmdlet을 사용하세요.

### <a name="new-azurermservicebusnamespaceauthorizationrule"></a>**New-AzureRmServiceBusNamespaceAuthorizationRule**
- 'New-AzureRmServiceBusNamespaceAuthorizationRule' cmdlet이 제거되었습니다. 'New-AzureRmServiceBusAuthorizationRule' cmdlet을 사용하세요.

### <a name="remove-azurermservicebusnamespaceauthorizationrule"></a>**Remove-AzureRmServiceBusNamespaceAuthorizationRule**
- 'Remove-AzureRmServiceBusNamespaceAuthorizationRule' cmdlet이 제거되었습니다. 'Remove-AzureRmServiceBusAuthorizationRule' cmdlet을 사용하세요.

### <a name="set-azurermservicebusnamespaceauthorizationrule"></a>**Set-AzureRmServiceBusNamespaceAuthorizationRule**
- 'Set-AzureRmServiceBusNamespaceAuthorizationRule' cmdlet이 제거되었습니다. 'Set-AzureRmServiceBusAuthorizationRule' cmdlet을 사용하세요.

### <a name="type-namespaceattributes"></a>**NamespaceAttributes 형식**
- 다음 속성이 제거되었습니다.
    - 사용
    - 상태

```powershell-interactive
# Old
# The $namespace has Status and Enabled property
$namespace = Get-AzureRmServiceBusNamespace <parameters>
$namespace.Status
$namespace.Enabled

# New
# The call remains the same, but the returned values NameSpace object will not have the Enabled and Status properties
$namespace = Get-AzureRmServiceBusNamespace <parameters>
```

### <a name="type-queueattribute"></a>**QueueAttribute 형식**
- 다음 속성은 사용되지 않음으로 표시됩니다.
    - EnableBatchedOperations
    - EntityAvailabilityStatus
    - IsAnonymousAccessible
    - SupportOrdering

```powershell-interactive
# Old
# The $queue has EntityAvailabilityStatus, EnableBatchedOperations, IsAnonymousAccessible and SupportOrdering properties
$queue = Get-AzureRmServiceBusQueue <parameters>
$queue.EntityAvailabilityStatus
$queue.EnableBatchedOperations
$queue.IsAnonymousAccessible
$queue.SupportOrdering

# New
# The call remains the same, but the returned values Queue object will not have the EntityAvailabilityStatus, EnableBatchedOperations, IsAnonymousAccessible and SupportOrdering properties
$queue = Get-AzureRmServiceBusQueue <parameters>
```

### <a name="type-topicattribute"></a>**TopicAttribute 형식**
- 다음 속성은 사용되지 않음으로 표시됩니다.
    - 위치
    - IsExpress
    - IsAnonymousAccessible
    - FilteringMessagesBeforePublishing
    - EnableSubscriptionPartitioning
    - EntityAvailabilityStatus

```powershell-interactive
# Old
# The $topic has EntityAvailabilityStatus, EnableSubscriptionPartitioning, IsAnonymousAccessible, IsExpress, Location and FilteringMessagesBeforePublishing properties
$topic = Get-AzureRmServiceBusTopic <parameters>
$topic.EntityAvailabilityStatus
$topic.EnableSubscriptionPartitioning
$topic.IsAnonymousAccessible
$topic.IsExpress
$topic.FilteringMessagesBeforePublishing
$topic.Location

# New
# The call remains the same, but the returned values Topic object will not have the EntityAvailabilityStatus, EnableBatchedOperations, IsAnonymousAccessible and SupportOrdering properties
$topic = Get-AzureRmServiceBusTopic <parameters>
```

### <a name="type-subscriptionattribute"></a>**SubscriptionAttribute 형식**
- 다음 속성은 사용되지 않음으로 표시됩니다.
    - DeadLetteringOnFilterEvaluationExceptions
    - EntityAvailabilityStatus
    - IsReadOnly
    - 위치

```powershell-interactive
# Old
# The $subscription has EntityAvailabilityStatus, EnableSubscriptionPartitioning, IsAnonymousAccessible, IsExpress, Location and FilteringMessagesBeforePublishing properties
$subscription = Get-AzureRmServiceBussubscription <parameters>
$subscription.EntityAvailabilityStatus
$subscription.EnableSubscriptionPartitioning
$subscription.IsAnonymousAccessible
$subscription.IsExpress
$subscription.FilteringMessagesBeforePublishing
$subscription.Location

# New
# The call remains the same, but the returned values Topic object will not have the EntityAvailabilityStatus, EnableBatchedOperations, IsAnonymousAccessible and SupportOrdering properties
$subscription = Get-AzureRmServiceBussubscription <parameters>
```
