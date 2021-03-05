---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/powershell/module/az.CostManagement/new-AzCostManagementQueryFilterObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryFilterObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryFilterObject.md
ms.openlocfilehash: 84b54353b1f36dbfbb3cef068987c50a4b60923e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010651"
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

### 예제 1: 비용 관리 내보내기에 대한 쿼리의 필터 개체 만들기
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

이 명령은 비용 관리 내보내기에 대한 쿼리의 필터 개체를 만듭니다.

## 매개 변수

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

### -차원
차원에 대한 비교 식이 있습니다.
생성을 위해 차원 속성에 대한 메모 섹션을 참조하고 해시 테이블을 만드십시오.

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
생성을 위해 NOT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.

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
구문을 작성하기 위해 OR 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.

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
생성을 위해 TAG 속성에 대한 메모 섹션을 참조하고 해시 테이블을 만드십시오.

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
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## 입력

## 출력

### Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.QueryFilter

## 참고 사항

별칭

복잡한 매개 변수 속성

아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다. 해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.


및 <IQueryFilter[]>: 논리 "AND" 식입니다. 항목이 2개 이상 있어야 합니다.
  - `[And <IQueryFilter[]>]`: 논리 "AND" 식입니다. 항목이 2개 이상 있어야 합니다.
  - `[Dimensions <IQueryComparisonExpression>]`: 차원에 대한 비교 식이 있습니다.
    - `Name <String>`: 비교하여 사용할 열의 이름입니다.
    - `Value <String[]>`: 비교에 사용할 값의 배열
  - `[Not <IQueryFilter>]`: 논리 "NOT" 식입니다.
  - `[Or <IQueryFilter[]>]`: 논리 "OR" 식입니다. 항목이 2개 이상 있어야 합니다.
  - `[Tag <IQueryComparisonExpression>]`: 태그에 대한 비교 식이 있습니다.

차원 <IQueryComparisonExpression> : 차원에 대한 비교 식이 있습니다.
  - `Name <String>`: 비교하여 사용할 열의 이름입니다.
  - `Value <String[]>`: 비교에 사용할 값의 배열

NOT <IQueryFilter> : 논리 "NOT" 식입니다.
  - `[And <IQueryFilter[]>]`: 논리 "AND" 식입니다. 항목이 2개 이상 있어야 합니다.
  - `[Dimensions <IQueryComparisonExpression>]`: 차원에 대한 비교 식이 있습니다.
    - `Name <String>`: 비교하여 사용할 열의 이름입니다.
    - `Value <String[]>`: 비교에 사용할 값의 배열
  - `[Not <IQueryFilter>]`: 논리 "NOT" 식입니다.
  - `[Or <IQueryFilter[]>]`: 논리 "OR" 식입니다. 항목이 2개 이상 있어야 합니다.
  - `[Tag <IQueryComparisonExpression>]`: 태그에 대한 비교 식이 있습니다.

또는 <IQueryFilter[]>: 논리 "OR" 식입니다. 항목이 2개 이상 있어야 합니다.
  - `[And <IQueryFilter[]>]`: 논리 "AND" 식입니다. 항목이 2개 이상 있어야 합니다.
  - `[Dimensions <IQueryComparisonExpression>]`: 차원에 대한 비교 식이 있습니다.
    - `Name <String>`: 비교하여 사용할 열의 이름입니다.
    - `Value <String[]>`: 비교에 사용할 값의 배열
  - `[Not <IQueryFilter>]`: 논리 "NOT" 식입니다.
  - `[Or <IQueryFilter[]>]`: 논리 "OR" 식입니다. 항목이 2개 이상 있어야 합니다.
  - `[Tag <IQueryComparisonExpression>]`: 태그에 대한 비교 식이 있습니다.

태그 <IQueryComparisonExpression> : 태그에 대한 비교 식이 있습니다.
  - `Name <String>`: 비교하여 사용할 열의 이름입니다.
  - `Value <String[]>`: 비교에 사용할 값의 배열

## 관련 링크

