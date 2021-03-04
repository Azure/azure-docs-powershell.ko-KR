---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/powershell/module/az.policyinsights/get-azpolicystatesummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyStateSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyStateSummary.md
ms.openlocfilehash: 09fce075ae0f6d8c55f5ef18d070a72daafa2cac
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989086"
---
# Get-AzPolicyStateSummary

## SYNOPSIS
리소스에 대한 최신 정책 준수 상태 요약을 얻습니다.

## 구문

### SubscriptionScope(기본값)
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] [-Top <Int32>] [-From <DateTime>] [-To <DateTime>]
 [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ManagementGroupScope
```
Get-AzPolicyStateSummary -ManagementGroupName <String> [-Top <Int32>] [-From <DateTime>] [-To <DateTime>]
 [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceGroupScope
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -ResourceGroupName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### PolicySetDefinitionScope
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -PolicySetDefinitionName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### PolicyDefinitionScope
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -PolicyDefinitionName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### SubscriptionLevelPolicyAssignmentScope
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -PolicyAssignmentName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ResourceGroupLevelPolicyAssignmentScope
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -ResourceGroupName <String> -PolicyAssignmentName <String>
 [-Top <Int32>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceScope
```
Get-AzPolicyStateSummary -ResourceId <String> [-Top <Int32>] [-From <DateTime>] [-To <DateTime>]
 [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
정책 할당 및 정책 정의로 세분화된 다양한 범위의 최신 정책 준수 상태 번호에 대한 요약 보기를 제공합니다. 비준수 정책 상태만 포함합니다.

## 예제

### 예제 1: 현재 구독 범위에서 최신 비준수 정책 상태 요약을 얻습니다.
```powershell
PS C:\> Get-AzPolicyStateSummary
```

현재 세션 컨텍스트에서 구독 내의 모든 리소스에 대해 마지막 날에 생성된 최신 정책 준수 상태의 요약 보기를 를 GETS합니다.

### 예제 2: 지정된 구독 범위에서 최신 비준수 정책 상태 요약을 얻습니다.
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

지정된 구독 내의 모든 리소스에 대해 마지막 날에 생성된 최신 정책 준수 상태의 요약 보기를 얻습니다.

### 예제 3: 관리 그룹 범위에서 최신 비준수 정책 상태 요약을 얻습니다.
```powershell
PS C:\> Get-AzPolicyStateSummary -ManagementGroupName "myManagementGroup"
```

지정된 관리 그룹 내의 모든 리소스에 대해 마지막 날에 생성된 최신 정책 준수 상태의 요약 보기를 얻습니다.

### 예제 4: 현재 구독의 리소스 그룹 범위에서 최신 비준수 정책 상태 요약을 얻습니다.
```powershell
PS C:\> Get-AzPolicyStateSummary -ResourceGroupName "myResourceGroup"
```

지정된 리소스 그룹 내의 모든 리소스(현재 세션 컨텍스트의 구독)에 대한 마지막 날에 생성된 최신 정책 준수 상태의 요약 보기를 얻습니다.

### 예제 5: 지정된 구독의 리소스 그룹 범위에서 최신 비준수 정책 상태 요약을 얻습니다.
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

지정된 리소스 그룹 내의 모든 리소스(지정된 구독에서)에 대해 마지막 날에 생성된 최신 정책 준수 상태의 요약 보기를 얻습니다.

### 예제 6: 리소스에 대한 최신 비준수 정책 상태 요약을 다운로드합니다.
```powershell
PS C:\> Get-AzPolicyStateSummary -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

지정된 리소스에 대한 마지막 날에 생성된 최신 정책 준수 상태의 요약 보기를 를 제공합니다.

### 예제 7: 현재 구독에서 정책 집합 정의에 대한 최신 비준수 정책 상태 요약을 다운로드합니다.
```powershell
PS C:\> Get-AzPolicyStateSummary -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

지정된 정책 집합 정의(현재 세션 컨텍스트의 구독에 있는 구독에 있는) 영향이 있는 모든 리소스(현재 세션 컨텍스트의 테넌트 내)에 대해 마지막 날에 생성된 최신 정책 준수 상태의 요약 보기를 를 제공합니다.

### 예제 8: 지정된 구독에서 정책 집합 정의에 대한 최신 비준수 정책 상태 요약을 다운로드합니다.
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

지정된 정책 집합 정의(지정된 구독에 있는)의 영향이 있는 모든 리소스(현재 세션 컨텍스트의 테넌트 내)에 대해 마지막 날에 생성된 최신 정책 준수 상태의 요약 보기를 얻습니다.

### 예제 9: 현재 구독의 정책 정의에 대한 최신 비준수 정책 상태 요약을 다운로드합니다.
```powershell
PS C:\> Get-AzPolicyStateSummary -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

지정된 정책 정의(현재 세션 컨텍스트의 구독에 있는)에 의해 영향을 받을 모든 리소스(현재 세션 컨텍스트의 테넌트 내)에 대해 마지막 날에 생성된 최신 정책 준수 상태의 요약 보기를 를 제공합니다.

### 예제 10: 지정된 구독에서 정책 정의에 대한 최신 비준수 정책 상태 요약을 다운로드합니다.
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

지정된 정책 정의(지정된 구독에 있는)의 영향이 있는 모든 리소스(현재 세션 컨텍스트의 테넌트 내)에 대해 마지막 날에 생성된 최신 정책 준수 상태의 요약 보기를 제공합니다.

### 예제 11: 현재 구독에서 정책 할당에 대한 최신 비준수 정책 상태 요약을 다운로드합니다.
```powershell
PS C:\> Get-AzPolicyStateSummary -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

지정된 정책 할당(현재 세션 컨텍스트의 구독에 있는 구독에 있는)의 영향이 있는 모든 리소스(현재 세션 컨텍스트의 테넌트 내)에 대해 마지막 날에 생성된 최신 정책 준수 상태의 요약 보기를 얻습니다.

### 예제 12: 지정된 구독에서 정책 할당에 대한 최신 비준수 정책 상태 요약을 다운로드합니다.
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

지정된 정책 할당(지정된 구독에 있는)의 영향이 있는 모든 리소스(현재 세션 컨텍스트의 테넌트 내)에 대해 마지막 날에 생성된 최신 정책 준수 상태의 요약 보기를 얻습니다.

### 예제 13: 현재 구독의 지정된 리소스 그룹의 정책 할당에 대한 최신 비준수 정책 상태 요약을 다운로드합니다.
```powershell
PS C:\> Get-AzPolicyStateSummary -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

지정된 정책 할당(현재 세션 컨텍스트의 구독의 리소스 그룹에 있는)의 영향이 있는 모든 리소스(현재 세션 컨텍스트의 테넌트 내)에 대해 마지막 날에 생성된 최신 정책 준수 상태의 요약 보기를 를 제공합니다.

### 예제 14: 최상위 쿼리 옵션을 사용하여 현재 구독 범위에서 최신 비준수 정책 상태 요약을 얻습니다.
```powershell
PS C:\> Get-AzPolicyStateSummary -Top 5
```

현재 세션 컨텍스트에서 구독 내의 모든 리소스에 대해 마지막 날에 생성된 최신 정책 준수 상태의 요약 보기를 를 GETS합니다. 명령은 규정을 준수하지 않는 리소스 수를 내선 순서로 계산하여 결과에 정책 할당 요약을 순서대로 명령하고, 이러한 정책 할당 요약의 상위 5개만 사용하게 됩니다.

### 예제 15: 시작 및 쿼리 옵션으로 현재 구독 범위에서 최신 비준수 정책 상태 요약을 얻습니다.
```powershell
PS C:\> Get-AzPolicyStateSummary -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

현재 세션 컨텍스트에서 구독 내의 모든 리소스에 대해 지정된 날짜 범위 내에서 생성된 최신 정책 준수 상태의 요약 보기를 를 GETS합니다.

### 예제 16: 필터 쿼리 옵션을 사용하여 현재 구독 범위에서 최신 비준수 정책 상태 요약을 얻습니다.
```powershell
PS C:\> Get-AzPolicyStateSummary -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and ResourceLocation ne 'eastus'"
```

현재 세션 컨텍스트에서 구독 내의 모든 리소스에 대해 마지막 날에 생성된 최신 정책 준수 상태의 요약 보기를 를 GETS합니다.
명령은 정책 정의 작업(거부 또는 감사 작업 포함) 및 리소스 위치(eastus 위치 제외)에 따라 필터링하여 반환되는 결과를 제한합니다.

## 매개 변수

### -DefaultProfile
Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.

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

### -Filter
OData 표기어를 사용하여 식 필터링

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -From
쿼리할 간격의 시작 시간을 지정하는 ISO 8601 서식 타임스탬프입니다.
지정하지 않으면 기본값은 'To' 매개 변수 값에서 1일을 1일로 입니다.

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ManagementGroupName
관리 그룹 이름입니다.

```yaml
Type: System.String
Parameter Sets: ManagementGroupScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PolicyAssignmentName
정책 할당 이름입니다.

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelPolicyAssignmentScope, ResourceGroupLevelPolicyAssignmentScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PolicyDefinitionName
정책 정의 이름입니다.

```yaml
Type: System.String
Parameter Sets: PolicyDefinitionScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PolicySetDefinitionName
정책 집합 정의 이름입니다.

```yaml
Type: System.String
Parameter Sets: PolicySetDefinitionScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
리소스 그룹 이름입니다.

```yaml
Type: System.String
Parameter Sets: ResourceGroupScope, ResourceGroupLevelPolicyAssignmentScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
리소스 ID입니다.

```yaml
Type: System.String
Parameter Sets: ResourceScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SubscriptionId
구독 ID입니다.

```yaml
Type: System.String
Parameter Sets: SubscriptionScope, ResourceGroupScope, PolicySetDefinitionScope, PolicyDefinitionScope, SubscriptionLevelPolicyAssignmentScope, ResourceGroupLevelPolicyAssignmentScope
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -To
쿼리할 간격의 종료 시간을 지정하는 ISO 8601 서식 타임스탬프입니다.
지정하지 않으면 기본적으로 요청 시간으로 설정됩니다.

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Top
반환할 최대 레코드 수입니다.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## 입력

### System.String

## 출력

### Microsoft.Azure.Commands.PolicyInsights.Models.PolicyStateSummary

## 참고 사항

## 관련 링크

[Get-AzPolicyState](./Get-AzPolicyState.md)
