---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 23DB0AD2-7EB7-4373-BB8D-BB6CB651DD54
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTag.md
ms.openlocfilehash: 176328452c123c3d3cada88940efcdadf88943e0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204426"
---
# New-AzTag

## SYNOPSIS
미리 정의 된 Azure 태그를 만들거나 기존 태그에 값을 추가 합니다. | 리소스나 구독에 대 한 전체 태그 집합을 만들거나 업데이트 합니다.

## 구문과

### CreatePredefinedTagParameterSet

```powershell
New-AzTag [-Name] <String> [[-Value] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### CreateByResourceIdParameterSet

```powershell
New-AzTag
   -ResourceId <String>
   -Tag <Hashtable>
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

## 설명은

**CreatePredefinedTagSet** : **AzTag** cmdlet은 미리 정의 된 선택적 값으로 미리 정의 되어 있는 Azure 태그를 만듭니다.
또한 기존에 미리 정의 된 태그에 다른 값을 추가 하는 데 사용할 수 있습니다.
미리 정의 된 태그를 만들려면 고유한 태그 이름을 입력 합니다.
미리 정의 된 기존 태그에 값을 추가 하려면 기존 태그의 이름과 새 값을 지정 합니다.
이 cmdlet은 새 태그 또는 수정 된 태그가 해당 값과 적용 된 리소스 수를 나타내는 개체를 반환 합니다.
**새로운 AzTag** 의 일부인 azure tags 모듈은 미리 정의 된 Azure 태그를 관리 하는 데 도움이 될 수 있습니다.
Azure 태그는 사용자가 Azure 리소스 및 리소스 그룹 (예: 부서나 비용 센터)을 분류 하거나 리소스 및 그룹에 대 한 메모 또는 설명을 추적 하는 데 사용할 수 있는 이름-값 쌍입니다.
한 단계에서 태그를 정의 하 고 적용할 수 있지만, 미리 정의 된 태그를 사용 하면 구독의 태그에 대 한 표준, 일관성, 예측 가능한 이름 및 값을 설정할 수 있습니다.
리소스 또는 리소스 그룹에 미리 정의 된 태그를 적용 하려면 New-AzTag cmdlet의 *tag* 매개 변수를 사용 합니다.
지정 된 태그 이름이 나 이름 및 값을 사용 하 여 리소스 그룹을 검색 하려면 Get-AzResourceGroup cmdlet의 *tag* 매개 변수를 사용 합니다.
모든 태그에는 이름이 있습니다.
값은 선택 사항입니다.
미리 정의 된 Azure 태그에는 여러 값이 포함 될 수 있지만 리소스 또는 리소스 그룹에 태그를 적용 하는 경우 태그 이름과 해당 값 중 하나만 적용 됩니다.
예를 들어 재무, 인적 자원 등의 각 부서에 대 한 값을 사용 하 여 미리 정의 된 부서 태그를 만들 수 있습니다.
자원에 부서 태그를 적용 하는 경우 재무와 같은 미리 정의 된 값을 하나만 적용 합니다.

**CreateByResourceIdParameterSet** : **ResourceId** 가 있는 **New-AzTag** cmdlet은 리소스나 구독에 대 한 전체 태그 집합을 만들거나 업데이트 합니다.
이 작업을 수행 하면 지정 된 리소스나 구독에 대 한 전체 태그 집합을 추가 하거나 바꿀 수 있습니다. 지정 된 엔터티는 최대 50 태그를 가질 수 있습니다.

## 예제의

### 예제 1: 미리 정의 된 태그 만들기
```powershell
PS C:\>New-AzTag -Name "FY2015"
                                
Name   ValuesTable Count Values 
----   ----------- ----- ------
FY2015             0     {}
```

이 명령은 FY2015 이라는 미리 정의 된 태그를 만듭니다.
이 태그에는 값이 없습니다.
값이 없는 태그를 리소스나 리소스 그룹에 적용 하거나, **New-AzTag** 를 사용 하 여 태그에 값을 추가할 수 있습니다.
리소스 또는 리소스 그룹에 태그를 적용 하는 경우 값을 지정할 수도 있습니다.

### 예제 2: 값을 사용 하 여 미리 정의 된 태그 만들기
```powershell
PS C:\>New-AzTag -Name "Department" -Value "Finance"
Name:   Department
Count:  0
Values: 

        Name        Count
        =========   =====
        Finance     0
```

이 명령은 재무 값이 포함 된 부서별 이라는 미리 정의 된 태그를 만듭니다.

### 예제 3: 미리 정의 된 태그에 값 추가
```powershell
PS C:\>New-AzTag -Name "Department" -Value "Finance"
Name:   Department
Count:  0
Values: 
        Name        Count
        =========   =====
        Finance     0 
PS C:\>New-AzTag -Name "Department" -Value "IT"
Name:   Department
Count:  0
Values: 
        Name        Count
        =========   =====
        Finance     0
        IT          0
```

이러한 명령을 사용 하면 두 값이 있는 부서별 이라는 미리 정의 된 태그를 만듭니다.
태그 이름이 있으면 새 항목을 만드는 대신 **AzTag** 에서 기존 태그에 값을 추가 합니다.

### 예제 4: 미리 정의 된 태그 사용
```powershell
PS C:\>New-AzTag -Name "CostCenter" -Value "0001"
Name:   CostCenter
Count:  0
Values: 
        Name        Count
        =========   =====
        0001        0 
PS C:\>Set-AzResourceGroup -Name "EngineerBlog" -Tag @{Name="CostCenter";Value="0001"}
Name:      EngineerBlog
Location:  East US
Resources: 
            
  Name             Type                     Location
    ===============  =======================  ========
    EngineerBlog     Microsoft.Web/sites      West US
    EngSvr01         Microsoft.Sql/servers    West US
    EngDB02          Microsoft.Sql/databases  West US
Tags: 
    Name         Value
    ==========   =====
    CostCenter   0001 
PS C:\>Get-AzTag -Name "CostCenter"
Name:   CostCenter
Count:  1
Values: 
        Name        Count
        =========   =====
        0001        1 
PS C:\>Get-AzResourceGroup -Tag @{Name="CostCenter"}
Name:      EngineerBlog
Location:  East US
Resources: 
     Name             Type                     Location
    ===============  =======================  ========
    EngineerBlog     Microsoft.Web/sites      West US

    EngSvr01         Microsoft.Sql/servers    West US
    EngDB02          Microsoft.Sql/databases  West US
Tags: 
    Name         Value
    ==========   =====
    CostCenter   0001
```

이 예제의 명령은 미리 정의 된 태그를 만들고 사용 합니다.

### 예제 5: 구독에 대 한 전체 태그 집합을 만들거나 업데이트 합니다.

```powershell
PS C:\>$Tags = @{"tagKey1"="tagValue1"; "tagKey2"="tagValue2"}
PS C:\>New-AzTag -ResourceId /subscriptions/{subId} -Tag $Tags

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             tagKey1  tagValue1
             tagKey2  tagValue2
```

이 명령은 {subId}를 사용 하 여 구독에 대 한 전체 태그 집합을 만들거나 업데이트 합니다.

### 예제 6: 리소스의 전체 태그 집합을 만들거나 업데이트 합니다.

```powershell
PS C:\>$Tags = @{"Dept"="Finance"; "Status"="Normal"}
PS C:\>New-AzTag -ResourceId /subscriptions/{subId}/resourcegroups/{rg}/providers/Microsoft.Sql/servers/Server1 -Tag $Tags

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             Dept     Finance
             Status   Normal
```

이 명령은 {resourceId}를 사용 하 여 자원의 전체 태그 집합을 만들거나 업데이트 합니다.

## 변수

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

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

### -이름
미리 정의 된 태그 이름을 지정 합니다.
미리 정의 된 새 태그를 만들려면 고유한 이름을 입력 합니다.
기존 태그에 값을 추가 하려면 기존 태그의 이름을 입력 합니다.
미리 정의 된 기존 태그에 지정 된 이름이 있는 경우 새 태그를 만드는 대신 해당 이름의 태그에 지정 된 값이 있는 경우 **AzTag** 를 추가 합니다.

```yaml
Type: System.String
Parameter Sets: CreatePredefinedTagParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -값
미리 정의 된 태그 값을 지정 합니다.
미리 정의 된 태그에 여러 값이 있을 수 있지만 각 명령에 하나의 값만 입력할 수 있습니다.
태그에 값이 없는 이름이 있을 수 있으므로이 매개 변수는 선택 사항입니다.

```yaml
Type: System.String
Parameter Sets: CreatePredefinedTagParameterSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
태그가 지정 되는 엔터티의 리소스 식별자입니다. 리소스, 리소스 그룹 또는 구독에 태그가 지정 될 수 있습니다.

```yaml
Type: System.String
Parameter Sets: CreateByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### 태그
리소스에 포함할 태그입니다.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateByResourceIdParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -확인
Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.
Cmdlet이 실행 되지 않습니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.

## 입력

### System. 문자열

### System.webserver. 컬렉션 테이블

## 출력

### PSTag |을 (를) 보세요. PSTagResource에 대 한.

## 상속자

## 관련 링크

[Get-AzTag](./Get-AzTag.md)

[제거-AzTag](./Remove-AzTag.md)

[업데이트-AzTag](./Update-AzTag.md)
