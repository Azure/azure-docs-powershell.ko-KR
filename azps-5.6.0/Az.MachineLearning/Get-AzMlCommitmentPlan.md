---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/powershell/module/az.machinelearning/get-azmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentPlan.md
ms.openlocfilehash: b3ea89f2470052a0d5858da199ee5285b3d5ea18
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965824"
---
# Get-AzMlCommitmentPlan

## SYNOPSIS
하나 이상의 약정 계획에 대한 요약 정보를 검색합니다.

## 구문

```
Get-AzMlCommitmentPlan [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
약정 계획 정보를 검색합니다.
전달된 매개 변수에 따라 cmdlet은 특정 약정 계획, 현재 구독 내의 지정된 리소스 그룹에 대한 약정 계획 컬렉션 또는 현재 구독 내의 약정 계획 컬렉션을 반환합니다.

## 예제

### 예제 1: 특정 약정 계획 수립
```
Get-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

### 예제 2: 현재 구독의 모든 약정 계획 리소스 사용
```
Get-AzMlCommitmentPlan
```

### 예제 3: 현재 구독 및 주어진 리소스 그룹의 모든 약정 계획 사용
```
Get-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup"
```

## 매개 변수

### -DefaultProfile
azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독

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

### -Name
약정 계획의 이름입니다.

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

### -ResourceGroupName
Azure ML 약정 계획에 대한 리소스 그룹의 이름입니다.

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

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.

## 입력

### 없음

## 출력

### Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan

## 참고 사항
키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 기계, 기계 학습, azureml

## 관련 링크
