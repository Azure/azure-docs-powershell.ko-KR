---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 726E01DD-D73C-4D4B-8FC0-52767927367C
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTag.md
ms.openlocfilehash: 058f4a61f1e7ff2fe7f416ea0e4ada098c9efe51
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98365275"
---
# Get-AzTag

## SYNOPSIS
미리 정의된 Azure 태그를 얻습니다. | 리소스 또는 구독에 대한 태그의 전체 집합을 얻습니다.

## 구문

### GetPredefinedTagParameterSet
```
Get-AzTag [[-Name] <String>] [-Detailed] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByResourceIdParameterSet
```
Get-AzTag -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명

**GetPredefinedTagSet:** **Get-AzTag** cmdlet은 구독에서 미리 정의된 Azure 태그를 얻습니다.
이 cmdlet은 태그에 대한 기본 정보 또는 태그 및 해당 값에 대한 자세한 정보를 반환합니다.
모든 출력 개체에는 태그 및 값이 적용된 리소스 및 리소스 그룹의 수를 나타내는 Count 속성이 포함됩니다.
**Get-AzTag가** 일부인 Azure Tags 모듈은 미리 정의한 Azure 태그를 관리하는 데 도움이 될 수 있습니다.
Azure 태그는 부서 또는 비용 센터와 같은 Azure 리소스 및 리소스 그룹을 분류하거나 리소스 및 그룹에 대한 메모 또는 메모를 추적하는 데 사용할 수 있는 이름-값 쌍입니다.
한 단계에서 태그를 정의하고 적용할 수 있지만 미리 정의된 태그를 사용하면 구독의 태그에 대한 표준, 일관되고 예측 가능한 이름 및 값을 설정할 수 있습니다.
미리 정의한 태그를 만들 경우 New-AzTag cmdlet을 사용 합니다.
리소스 그룹에 미리 정의된 태그를 적용하기  위해 New-AzTag cmdlet의 Tag 매개 변수를 사용합니다.
특정 태그 이름 또는 이름 및 값에 대한  리소스 그룹을 검색하기 위해 Get-AzResourceGroup cmdlet의 Tag 매개 변수를 사용합니다.

**GetByResourceIdParameterSet:** **ResourceId가** 있는 **Get-AzTag** cmdlet은 리소스 또는 구독에 대한 태그의 전체 집합을 얻습니다.

## 예제

### 예제 1: 미리 정의한 모든 태그를 얻습니다.
```powershell
PS C:\>Get-AzTag

Name      Count
========  =====

Department    5
FY2015        2
CostCenter   20
```

이 명령은 구독에서 미리 정의한 모든 태그를 얻습니다.
Count 속성은 구독의 리소스 및 리소스 그룹에 태그가 적용된 횟수를 보여줍니다.

### 예제 2: 이름에 의해 태그를 얻게
```powershell
PS C:\>Get-AzTag -Name "Department"

Name:   Department
Count:  5
Values: 

        Name        Count
        ==========  =====

        Finance       2
        IT            3
```

이 명령은 Department 태그 및 해당 값에 대한 자세한 정보를 얻습니다.
Count 속성은 구독의 리소스 및 리소스 그룹에 태그 및 각 값이 적용된 횟수를 보여줍니다.

### 예제 3: 모든 태그의 값 얻기
```powershell
PS C:\>Get-AzTag -Detailed

Name:   Department
Count:  5
Values: 

        Name        Count
        ==========  =====

        Finance       2
        IT            3


Name:   FY2015
Count:  2


Name:   CostCenter
Count:  20
Values: 

        Name        Count
        ==========  =====

        0001          5
        0002         10
        0003          5
```

이 명령은 *Detailed* 매개 변수를 사용하여 구독의 모든 미리 정의된 태그에 대한 자세한 정보를 얻습니다.
Detailed *매개 변수를* 사용하는 것은 모든 태그에 *이름* 매개 변수를 사용하는 경우와 동일합니다.

### 예제 4: 구독에서 태그의 전체 집합을 얻습니다.

```powershell
PS C:\>Get-AzTag -ResourceId /subscriptions/{subId}

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             tagKey1  tagValue1
             tagKey2  tagValue2
```

이 명령은 {subId}를 사용하여 구독에 대한 태그의 전체 집합을 얻습니다.

### 예제 5: 리소스에 대한 전체 태그 집합을 얻습니다.

```powershell
PS C:\>Get-AzTag -ResourceId /subscriptions/{subId}/resourcegroups/{rg}/providers/Microsoft.Sql/servers/Server1

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             Dept     Finance
             Status   Normal
```

이 명령은 {resourceId}를 사용하여 리소스에 대한 태그의 전체 집합을 얻습니다.

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

### -Detailed
이 작업이 출력에 태그 값에 대한 정보를 추가하는지 나타냅니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetPredefinedTagParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
미리 정의한 태그의 이름입니다.
기본적으로 **Get-AzTag는** 구독의 모든 미리 정의된 태그에 대한 기본 정보를 얻습니다.
Name 매개 *변수를 지정하는* 경우 *Detailed* 매개 변수는 영향을 주지 않습니다.

```yaml
Type: System.String
Parameter Sets: GetPredefinedTagParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
태그가 지정된 엔터티의 리소스 식별자입니다. 리소스, 리소스 그룹 또는 구독에 태그가 지정될 수 있습니다.

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## 입력

### System.String

### System.Management.Automation.SwitchParameter

## 출력

### Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag | Microsoft.Azure.Commands.Tags.Model.PSTagResource

## 참고 사항

## 관련 링크

[New-AzTag](./New-AzTag.md)

[Remove-AzTag](./Remove-AzTag.md)

[Update-AzTag](./Update-AzTag.md)
