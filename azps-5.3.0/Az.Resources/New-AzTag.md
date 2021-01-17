---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 23DB0AD2-7EB7-4373-BB8D-BB6CB651DD54
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTag.md
ms.openlocfilehash: 937ac50ac34f8b04912a0d500dedb5b490806b1a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490352"
---
# New-AzTag

## SYNOPSIS
미리 정의된 Azure 태그를 만들거나 기존 태그에 값을 추가 | 리소스 또는 구독에서 전체 태그 집합을 생성하거나 업데이트합니다.

## 구문

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

## 설명

**CreatePredefinedTagSet:** **New-AzTag** cmdlet은 선택적으로 미리 정의된 값으로 미리 정의된 Azure 태그를 만듭니다.
기존 미리 정의된 태그에 값을 추가하는 데 사용할 수도 있습니다.
미리 정의된 태그를 만들 경우 고유한 태그 이름을 입력합니다.
기존 미리 정의된 태그에 값을 추가하기 위해 기존 태그의 이름과 새 값을 지정합니다.
이 cmdlet은 해당 값 및 적용된 리소스 수를 사용하여 새 태그 또는 수정된 태그를 나타내는 개체를 반환합니다.
**New-AzTag가** 일부인 Azure Tags 모듈은 미리 정의한 Azure 태그를 관리하는 데 도움이 될 수 있습니다.
Azure 태그는 부서 또는 비용 센터와 같은 Azure 리소스 및 리소스 그룹을 분류하거나 리소스 및 그룹에 대한 메모 또는 메모를 추적하는 데 사용할 수 있는 이름-값 쌍입니다.
한 단계에서 태그를 정의하고 적용할 수 있지만 미리 정의된 태그를 사용하면 구독의 태그에 대한 표준, 일관되고 예측 가능한 이름 및 값을 설정할 수 있습니다.
리소스 또는 리소스 그룹에 미리 정의된 태그를 적용하기 위해 New-AzTag cmdlet의 Tag 매개 변수를 사용합니다. 
지정된 태그 이름 또는 이름 및 값을 사용하여 리소스  그룹을 검색하기 위해 Get-AzResourceGroup cmdlet의 Tag 매개 변수를 사용합니다.
모든 태그에는 이름이 있습니다.
값은 선택 사항입니다.
미리 정의한 Azure 태그에는 여러 값이 있을 수 있지만, 리소스 또는 리소스 그룹에 태그를 적용할 때 태그 이름과 해당 값 중 하나만 적용합니다.
예를 들어 재무, 인사 관리 및 IT와 같은 각 부서에 대한 값을 사용하여 미리 정의한 부서 태그를 만들 수 있습니다.
리소스에 부서 태그를 적용하는 경우 재무와 같은 미리 정의한 값 하나만 적용합니다.

**CreateByResourceIdParameterSet:** **ResourceId가** 있는 **New-AzTag** cmdlet은 리소스 또는 구독에 태그의 전체 집합을 만들거나 업데이트합니다.
이 작업을 통해 지정된 리소스 또는 구독에 태그의 전체 집합을 추가하거나 대체할 수 있습니다. 지정된 엔터티에는 최대 50개 태그가 있습니다.

## 예제

### 예제 1: 미리 정의된 태그 만들기
```powershell
PS C:\>New-AzTag -Name "FY2015"
                                
Name   ValuesTable Count Values 
----   ----------- ----- ------
FY2015             0     {}
```

이 명령은 FY2015라는 미리 정의된 태그를 만듭니다.
이 태그에는 값이 없습니다.
리소스 또는 리소스 그룹에 값이 없는 태그를 적용하거나 **New-AzTag를** 사용하여 태그에 값을 추가할 수 있습니다.
리소스 또는 리소스 그룹에 태그를 적용할 때 값을 지정할 수도 있습니다.

### 예제 2: 값이 있는 미리 정의된 태그 만들기
```powershell
PS C:\>New-AzTag -Name "Department" -Value "Finance"
Name:   Department
Count:  0
Values: 

        Name        Count
        =========   =====
        Finance     0
```

이 명령은 Finance 값을 사용하여 Department라는 미리 정의된 태그를 만듭니다.

### 예제 3: 미리 정의한 태그에 값 추가
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

이러한 명령은 두 개의 값을 사용하여 Department라는 미리 정의된 태그를 생성합니다.
태그 이름이 있는 경우 **New-AzTag는** 새 태그를 만드는 대신 기존 태그에 값을 추가합니다.

### 예제 4: 미리 정의한 태그 사용
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

이 예제의 명령은 미리 정의한 태그를 만들고 사용하게 됩니다.

### 예제 5: 구독에서 전체 태그 집합을 생성하거나 업데이트합니다.

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

이 명령은 {subId}를 사용하여 구독에 대한 태그의 전체 집합을 만들거나 업데이트합니다.

### 예제 6: 리소스에 대한 전체 태그 집합을 생성하거나 업데이트합니다.

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

이 명령은 {resourceId}를 사용하여 리소스에 태그의 전체 집합을 만들거나 업데이트합니다.

## PARAMETERS

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

### -Name
미리 정의한 태그 이름을 지정합니다.
미리 정의한 새 태그를 만들 때 고유한 이름을 입력합니다.
기존 태그에 값을 추가하기 위해 기존 태그의 이름을 입력합니다.
기존 미리 정의된 태그에 지정된 이름이 있는 경우 **New-AzTag는** 새 태그를 만드는 대신 해당 이름의 태그에 지정된 값(있는 경우)을 추가합니다.

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

### -Value
미리 정의한 태그 값을 지정합니다.
미리 정의된 태그는 여러 값을 사용할 수 있지만 각 명령에 하나의 값만 입력할 수 있습니다.
태그는 값 없이 이름을 사용할 수 있기 때문에 이 매개 변수는 선택 사항입니다.

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
태그가 지정되는 엔터티의 리소스 식별자입니다. 리소스, 리소스 그룹 또는 구독에 태그가 지정될 수 있습니다.

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

### -Tag
리소스에 넣을 태그입니다.

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

### -Confirm
cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.

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
cmdlet이 실행되는 경우의 결과 표시
cmdlet이 실행되지 않습니다.

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
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## 입력

### System.String

### System.Collections.Hashtable

## 출력

### Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag | Microsoft.Azure.Commands.Tags.Model.PSTagResource

## 참고 사항

## 관련 링크

[Get-AzTag](./Get-AzTag.md)

[Remove-AzTag](./Remove-AzTag.md)

[Update-AzTag](./Update-AzTag.md)