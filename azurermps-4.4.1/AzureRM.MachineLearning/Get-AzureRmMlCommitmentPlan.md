---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentPlan.md
ms.openlocfilehash: 9f9789d288773b16b2003e23b00674c12ca08738
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532244"
---
# Get-AzureRmMlCommitmentPlan

## SYNOPSIS
하나 이상의 약정 계획에 대 한 요약 정보를 검색 합니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
Get-AzureRmMlCommitmentPlan [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
약정 계획 정보를 검색 합니다.
Paramenters에 따라 cmdlet은 특정 약정 계획, 현재 구독 내의 지정 된 리소스 그룹에 대 한 약정 계획 모음 또는 현재 구독 내의 약정 계획 컬렉션을 반환 합니다.

## 예제의

### --------------------------예제 1: 특정 약정 계획 가져오기--------------------------
@ {paragraph = PS C: \\ \> }





```
Get-AzureRmMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

### --------------------------예제 2: 현재 구독에서 모든 약정 계획 리소스 가져오기--------------------------
@ {paragraph = PS C: \\ \> }





```
Get-AzureRmMlCommitmentPlan
```

### --------------------------예제 3: 현재 구독 및 지정 된 리소스 그룹에서 모든 약정 계획 가져오기--------------------------
@ {paragraph = PS C: \\ \> }





```
Get-AzureRmMlCommitmentPlan -ResourceGroupName "MyResourceGroup"
```

## 변수

### -이름
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
Azure ML 약정 계획에 대 한 리소스 그룹의 이름입니다.

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

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

## 출력

### MachineLearning. CommitmentPlans. \ CommitmentPlan
MachineLearning [] CommitmentPlans. CommitmentPlan []

## 상속자
키워드: azure, azurerm, arm, resource, 관리, manager, machine, 기계 학습, azureml

## 관련 링크

