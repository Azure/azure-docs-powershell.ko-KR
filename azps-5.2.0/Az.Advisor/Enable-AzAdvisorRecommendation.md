---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Advisor.dll-Help.xml
Module Name: Az.Advisor
online version: https://docs.microsoft.com/en-us/powershell/module/az.advisor/enable-azadvisorrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Enable-AzAdvisorRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Enable-AzAdvisorRecommendation.md
ms.openlocfilehash: 7126a9c8ee11bcb5b32cc47ae31aaf821b171522
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98342566"
---
# Enable-AzAdvisorRecommendation

## SYNOPSIS
Azure Advisor 권장을 사용할 수 있습니다.

## 구문

### NameParameterSet(기본값)
```
Enable-AzAdvisorRecommendation [-RecommendationName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### IdParameterSet
```
Enable-AzAdvisorRecommendation [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### InputObjectParameterSet
```
Enable-AzAdvisorRecommendation [-InputObject] <PsAzureAdvisorResourceRecommendationBase>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명
이 cmdlet을 사용하면 이전에 표시하지 않습니다. 권장과 연결된 모든 표시 안 을 제거할 수 있습니다.

## 예제

### 예제 1
```powershell
PS C:\> Enable-AzAdvisorRecommendation -ResourceId c3621337-f131-4bf4-92f2-3fb9c8cfa0d8 

ResourceId           : subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz/providers/Microsoft.Advisor/recommendations/c3621337-f131-4bf4-92f2-3fb9c8cfa0d8
Category             : Performance
ExtendedProperties   : {}
Impact               : Medium
ImpactedField        : Microsoft.Cache/Redis
ImpactedValue        : xyz
LastUpdated          : 12/4/2018 12:06:47 AM
Metadata             : {}
RecommendationTypeId : 905a0026-8010-45b2-ab46-a92c3e4a5131
Risk                 : None
ShortDescription     : problem : Improve the performance and reliability of your Redis Cache instance
                       solution : Follow Redis cache Advisor recommendations

SuppressionIds       : {} 
Name                 : c3621337-f131-4bf4-92f2-3fb9c8cfa0d8
Type                 : Microsoft.Advisor/recommendations
```

"recommendation_id"라는 이름으로 지정한 권장에 대한 모든 표시를 제거합니다.

### 예제 2
```powershell
PS C:\> Get-AzAdvisorRecommendation -ResourceId "/subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz" 
| Enable-AzAdvisorRecommendation

ResourceId           : subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz/providers/Microsoft.Advisor/recommendations/{recommendation_id}
Category             : Performance
ExtendedProperties   : {}
Impact               : Medium
ImpactedField        : Microsoft.Cache/Redis
ImpactedValue        : xyz
LastUpdated          : 12/4/2018 12:06:47 AM
Metadata             : {}
RecommendationTypeId : 905a0026-8010-45b2-ab46-a92c3e4a5131
Risk                 : None
ShortDescription     : problem : Improve the performance and reliability of your Redis Cache instance
                       solution : Follow Redis cache Advisor recommendations

SuppressionIds       : {} 
Name                 : {recommendation_id}
Type                 : Microsoft.Advisor/recommendations
```

파이프라인에서 전달된 주어진 권장에 대한 모든 표시를 제거합니다.

## PARAMETERS

### -Confirm
cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
powershell 개체 형식 PsAzureAdvisorResourceRecommendationBase는 Get-AzAdvisorRecommendation 반환합니다.

```yaml
Type: PsAzureAdvisorResourceRecommendationBase
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -RecommendationName
권장의 ResourceName입니다.

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
표시 안 하게 될 권장의 ID입니다.

```yaml
Type: String
Parameter Sets: IdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WhatIf
cmdlet이 실행되는 경우의 결과 표시
cmdlet이 실행되지 않습니다.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.
자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.

## 입력

### System.String

### Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase

## 출력

### Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase

## 참고 사항

## 관련 링크
