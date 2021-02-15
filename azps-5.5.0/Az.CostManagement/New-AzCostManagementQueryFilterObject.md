---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.CostManagement/new-AzCostManagementQueryFilterObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryFilterObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryFilterObject.md
ms.openlocfilehash: d2adba5ac5c75745c43e0d1ef62fb39d9b867c5e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196676"
---
# New-AzCostManagementQueryFilterObject

## SYNOPSIS
QueryFilter에 대한 메모리 내 개체 만들기

## 구문

```
New-AzCostManagementQueryFilterObject [-And <IQueryFilter[]>] [-Dimensions <IQueryComparisonExpression>]
 [-Not <IQueryFilter>] [-Or <IQueryFilter[]>] [-Tag <IQueryComparisonExpression>] [<CommonParameters>]
```

## 설명
QueryFilter에 대한 메모리 내 개체 만들기

## 예제

### 예제 1: 비용 관리 내보내기 쿼리의 필터 개체 만들기
```powershell
PS C:\> $orDimension = New-AzCostManagementQueryComparisonExpressionObject -Name 'ResourceLocation' -Value @('East US', 'West Europe')
PS C:\> $orTag = New-AzCostManagementQueryComparisonExpressionObject -Name 'Environment' -Value @('UAT', 'Prod')
PS C:\> New-AzCostManagementQueryFilterObject -or @((New-AzCostManagementQueryFilterObject -Dimension $orDimension), (New-AzCostManagementQueryFilterObject -Tag $orTag))

And       :
Dimension : Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryComparisonExpression
Not       : Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryFilter
Or        : {Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryFilter, Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryFilter}
Tag       : Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryComparisonExpression
```

이 명령은 비용 관리 내보내기 쿼리의 필터 개체를 만듭니다.

## PARAMETERS

### -And
논리 "AND" 식입니다.
항목이 2개 이상 있어야 합니다.
생성을 위해 AND 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryFilter[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Dimensions
차원에 대한 비교 식이 있습니다.
생성을 위해 차원 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryComparisonExpression
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Not
논리 "NOT" 식입니다.
구성을 위해 NOT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryFilter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Or
논리 "OR" 식입니다.
항목이 2개 이상 있어야 합니다.
구성을 위해 OR 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryFilter[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tag
태그에 대한 비교 식이 있습니다.
생성을 위해 TAG 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryComparisonExpression
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## 입력

## 출력

### Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.QueryFilter

## 참고 사항

별칭

복합 매개 변수 속성

아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다. 해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.


AND <IQueryFilter[]>: 논리 "AND" 식입니다. 항목이 2개 이상 있어야 합니다.
  - `[And <IQueryFilter[]>]`: 논리 "AND" 식입니다. 항목이 2개 이상 있어야 합니다.
  - `[Dimensions <IQueryComparisonExpression>]`: 차원에 대한 비교 식이 있습니다.
    - `Name <String>`: 비교에 사용할 열의 이름입니다.
    - `Value <String[]>`: 비교에 사용할 값의 배열
  - `[Not <IQueryFilter>]`: 논리 "NOT" 식입니다.
  - `[Or <IQueryFilter[]>]`: 논리적 "OR" 식입니다. 항목이 2개 이상 있어야 합니다.
  - `[Tag <IQueryComparisonExpression>]`: 태그에 대한 비교 식이 있습니다.

차원: <IQueryComparisonExpression> 차원에 대한 비교 식이 있습니다.
  - `Name <String>`: 비교에 사용할 열의 이름입니다.
  - `Value <String[]>`: 비교에 사용할 값의 배열

NOT: <IQueryFilter> 논리 "NOT" 식입니다.
  - `[And <IQueryFilter[]>]`: 논리 "AND" 식입니다. 항목이 2개 이상 있어야 합니다.
  - `[Dimensions <IQueryComparisonExpression>]`: 차원에 대한 비교 식이 있습니다.
    - `Name <String>`: 비교에 사용할 열의 이름입니다.
    - `Value <String[]>`: 비교에 사용할 값의 배열
  - `[Not <IQueryFilter>]`: 논리 "NOT" 식입니다.
  - `[Or <IQueryFilter[]>]`: 논리적 "OR" 식입니다. 항목이 2개 이상 있어야 합니다.
  - `[Tag <IQueryComparisonExpression>]`: 태그에 대한 비교 식이 있습니다.

OR <IQueryFilter[]>: 논리 "OR" 식입니다. 항목이 2개 이상 있어야 합니다.
  - `[And <IQueryFilter[]>]`: 논리 "AND" 식입니다. 항목이 2개 이상 있어야 합니다.
  - `[Dimensions <IQueryComparisonExpression>]`: 차원에 대한 비교 식이 있습니다.
    - `Name <String>`: 비교에 사용할 열의 이름입니다.
    - `Value <String[]>`: 비교에 사용할 값의 배열
  - `[Not <IQueryFilter>]`: 논리 "NOT" 식입니다.
  - `[Or <IQueryFilter[]>]`: 논리적 "OR" 식입니다. 항목이 2개 이상 있어야 합니다.
  - `[Tag <IQueryComparisonExpression>]`: 태그에 대한 비교 식이 있습니다.

TAG: <IQueryComparisonExpression> 태그에 대한 비교 식이 있습니다.
  - `Name <String>`: 비교에 사용할 열의 이름입니다.
  - `Value <String[]>`: 비교에 사용할 값의 배열

## 관련 링크

