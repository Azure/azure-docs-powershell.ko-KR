---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 66B25541-0FA5-46CF-90D8-FE9527BE11C6
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTag.md
ms.openlocfilehash: 22a43739ec63f8287ce51c4c4f4a125b4e5b1c65
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98354825"
---
# Remove-AzTag

## SYNOPSIS
미리 정의한 Azure 태그 또는 값을 삭제합니다. | 리소스 또는 구독에서 태그의 전체 집합을 삭제합니다.

## 구문

### RemovePredefinedTagParameterSet

```powershell
Remove-AzTag [-Name] <String> [[-Value] <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RemoveByResourceIdParameterSet

```powershell
Remove-AzTag
   -ResourceId <String>
   [-PassThru]
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

## 설명

**RemovePredefinedTagSet:** **Remove-AzTag** cmdlet은 구독에서 미리 정의한 Azure 태그 및 값을 삭제합니다.
미리 정의한 태그에서 특정 값을 삭제하려면 Value 매개 *변수를* 사용합니다.
기본적으로 **Remove-AzTag는** 지정된 태그 및 모든 해당 값을 삭제합니다. 현재 리소스 또는 리소스 그룹에 적용되는 태그 또는 값을 삭제할 수 없습니다.
**Remove-AzTag를** 사용하기 전에 Set-AzResourceGroup cmdlet의 *Tag* 매개 변수를 사용하여 리소스 또는 리소스 그룹에서 태그 또는 값을 삭제합니다.
**Remove-AzTag의** 일부인 Azure Tags 모듈은 미리 정의한 Azure 태그를 관리하는 데 도움이 될 수 있습니다.
Azure 태그는 부서 또는 비용 센터와 같은 Azure 리소스 및 리소스 그룹을 분류하거나 리소스 및 그룹에 대한 메모 또는 메모를 추적하는 데 사용할 수 있는 이름-값 쌍입니다.
한 단계에서 태그를 정의하고 적용할 수 있지만 미리 정의된 태그를 사용하면 구독의 태그에 대한 표준, 일관되고 예측 가능한 이름 및 값을 설정할 수 있습니다.

**RemoveByResourceIdParameterSet:** **ResourceId가** 있는 **Remove-AzTag** cmdlet은 리소스 또는 구독에 대한 태그의 전체 집합을 삭제합니다.

## 예제

### 예제 1: 미리 정의한 태그 삭제
```powershell
PS C:\>Remove-AzTag -Name "Department"
```

이 명령은 Department라는 미리 정의된 태그와 모든 해당 값을 삭제합니다.
태그가 리소스 또는 리소스 그룹에 적용된 경우 명령이 실패합니다.

### 예제 2: 미리 정의한 태그에서 값 삭제
```powershell
PS C:\>Remove-AzTag -Name "Department" -Value "HumanResources" -PassThru
Name:   Department
Count:  14
Values: 

        Name        Count
        =========   =====

        Finance        2
        IT            12
```

이 명령은 미리 정의한 Department 태그에서 HumanResources 값을 삭제합니다.
태그는 삭제하지 않습니다.
값이 리소스 또는 리소스 그룹에 적용된 경우 명령이 실패합니다.

### 예제 3: 구독에서 태그의 전체 집합을 삭제합니다.

```powershell
PS C:\>Remove-AzTag -ResourceId /subscriptions/{subId}
```

이 명령은 {subId}를 사용하여 구독에서 태그의 전체 집합을 삭제합니다. "-PassThru"를 전달하지 않는 경우 삭제된 개체를 반환하지 않습니다.

### 예제 4: 리소스에서 태그의 전체 집합을 삭제합니다.

```powershell
PS C:\>Remove-AzTag -ResourceId /subscriptions/{subId}/resourcegroups/{rg}/providers/Microsoft.Sql/servers/Server1 -PassThru

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             Dept     Finance
             Status   Normal
```

이 명령은 {resourceId}를 사용하여 리소스의 태그 집합 전체를 삭제합니다. "-PassThru"를 전달할 때 삭제된 oject를 반환합니다.

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
제거할 미리 정의된 태그의 이름을 지정합니다.
기본적으로 **Remove-AzTag는** 지정된 태그 및 모든 해당 값을 제거합니다.
선택한 값을 삭제하지만 태그를 삭제하지 않는 경우 Value 매개 *변수를* 사용합니다.

```yaml
Type: System.String
Parameter Sets: RemovePredefinedTagParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Value
미리 정의한 태그에서 지정된 값을 삭제하지만 태그는 삭제하지 않습니다.

```yaml
Type: System.String[]
Parameter Sets: RemovePredefinedTagParameterSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
태그가 지정된 엔터티의 리소스 식별자입니다. 리소스, 리소스 그룹 또는 구독에 태그가 지정될 수 있습니다.

```yaml
Type: System.String
Parameter Sets: RemoveByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
삭제된 태그를 나타내는 개체 또는 삭제된 값이 있는 결과 태그를 반환합니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
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

### System.String[]

### System.Management.Automation.SwitchParameter

## 출력

### Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag | Microsoft.Azure.Commands.Tags.Model.PSTagResource

## 참고 사항

## 관련 링크

[Get-AzTag](./Get-AzTag.md)

[New-AzTag](./New-AzTag.md)

[Update-AzTag](./Update-AzTag.md)