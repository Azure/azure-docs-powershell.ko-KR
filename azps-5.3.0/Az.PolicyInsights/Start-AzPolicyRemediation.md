---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/start-azpolicyremediation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyRemediation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyRemediation.md
ms.openlocfilehash: e4a0e3ad4ffac7e610f5807c7687cdc1bf548770
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98378547"
---
# Start-AzPolicyRemediation

## SYNOPSIS
정책 할당에 대한 정책 수정을 만들고 시작합니다.

## 구문

### ByName(기본값)
```
Start-AzPolicyRemediation -Name <String> [-Scope <String>] [-ManagementGroupName <String>]
 [-ResourceGroupName <String>] -PolicyAssignmentId <String> [-PolicyDefinitionReferenceId <String>]
 [-LocationFilter <String[]>] [-ResourceDiscoveryMode <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByResourceId
```
Start-AzPolicyRemediation -ResourceId <String> -PolicyAssignmentId <String>
 [-PolicyDefinitionReferenceId <String>] [-LocationFilter <String[]>] [-ResourceDiscoveryMode <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명
**Start-AzPolicyRemediation** cmdlet은 특정 정책 할당에 대한 정책 수정을 만듭니다. 수정 범위의 모든 비준수 리소스가 수정됩니다. 수정은 'deployIfNotExists' 효과가 적용된 정책에만 지원됩니다.

## 예제

### 예제 1: 구독 범위에서 수정 시작
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Select-AzSubscription -Subscription "My Subscription"
PS C:\> Start-AzPolicyRemediation -PolicyAssignmentId $policyAssignmentId -Name "remediation1"
```

이 명령은 주어진 정책 할당에 대한 구독 '내 구독'에 새 정책 수정을 만듭니다.

### 예제 2: 선택적 필터를 사용하여 관리 그룹 범위에서 수정 시작
```
PS C:\> $policyAssignmentId = "/providers/Microsoft.Management/managementGroups/mg1/providers/Microsoft.Authorization/policyAssignments/pa1"
PS C:\> Start-AzPolicyRemediation -ManagementGroupName "mg1" -PolicyAssignmentId $policyAssignmentId -Name "remediation1" -LocationFilter "westus","eastus"
```

이 명령은 주어진 정책 할당에 대한 관리 그룹 'mg1'에 새 정책 수정을 만듭니다. 'westus' 또는 'eastus' 위치에 있는 리소스만 수정됩니다.

### 예제 3: 정책 집합 정의 할당에 대한 리소스 그룹 범위에서 수정 시작
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/resourceGroups/myRG/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Start-AzPolicyRemediation -ResourceGroupName "myRG" -PolicyAssignmentId $policyAssignmentId -PolicyDefinitionReferenceId "0349234412441" -Name "remediation1"
```

이 명령은 주어진 정책 할당에 대한 리소스 그룹 'myRG'에 새 정책 수정을 만듭니다. 정책 할당은 이니셔티브라고도 하는 정책 집합 정의를 할당합니다. 정책 정의 참조 ID는 이니셔티브 내에서 수정해야 하는 정책을 나타냅니다.

### 예제 4: 수정을 시작하고 백그라운드에서 완료될 때까지 기다림
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Select-AzSubscription -Subscription f0710c27-9663-4c05-19f8-1b4be01e86a5
PS C:\> $job = Start-AzPolicyRemediation -PolicyAssignmentId $policyAssignmentId -Name "remediation1" -AsJob
PS C:\> $job | Wait-Job
PS C:\> $remediation = $job | Receive-Job
```

이 명령은 주어진 정책 할당에 대한 구독 '내 구독'에서 새 정책 수정을 시작합니다. 최종 수정 상태를 반환하기 전에 수정이 완료될 때까지 기다릴 수 있습니다.

### 예제 5: 수정하기 전에 비준수 리소스를 검색하는 수정 시작
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Select-AzSubscription -Subscription "My Subscription"
PS C:\> Start-AzPolicyRemediation -PolicyAssignmentId $policyAssignmentId -Name "remediation1" -ResourceDiscoveryMode ReEvaluateCompliance
```

이 명령은 주어진 정책 할당에 대한 구독 '내 구독'에 새 정책 수정을 만듭니다. 구독의 리소스 규정 준수 상태는 정책 할당에 대해 다시 평가됩니다. 비준수 리소스는 수정됩니다.

## PARAMETERS

### -AsJob
백그라운드에서 cmdlet을 실행합니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
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

### -LocationFilter
수정에 포함해야 하는 리소스 위치입니다.
이러한 위치에 없는 리소스는 수정되지 않습니다.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ManagementGroupName
관리 그룹 ID입니다.

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
리소스 이름입니다.

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PolicyAssignmentId
정책 할당 ID입니다.
예:
'/subscriptions/{subscriptionId}/providers/Microsoft.Authorization/policyAssignments/{assignmentName}'.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PolicyDefinitionReferenceId
수정되는 개별 정의의 정책 정의 참조 ID를 얻습니다.
정책 할당이 정책 집합 정의를 할당할 때 필요합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceDiscoveryMode
수정 작업에서 수정해야 하는 리소스를 검색하는 방법을 설명 합니다.
관리 그룹 범위를 수정하는 경우 ReEvaluateCompliance가 지원되지 않습니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: ExistingNonCompliant, ReEvaluateCompliance

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
리소스 그룹 이름입니다.

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
리소스 ID입니다.

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Scope
리소스의 범위입니다.
예:
'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### System.String[]

## 출력

### Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation

## 참고 사항

## 관련 링크
