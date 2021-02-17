---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 07c6e327-05f4-4279-a5fb-d4e860c897d4
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/update-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzTag.md
ms.openlocfilehash: 3423331e36fd9fbd636a1ae877275badd5912324
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178681"
---
# Update-AzTag

## SYNOPSIS

리소스 또는 구독에서 태그 집합을 선택적으로 업데이트합니다.

## 구문

```powershell
Update-AzTag
   -ResourceId <String>
   -Operation <TagPatchOperation>
   -Tag <Hashtable>
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]

```

## 설명

**ResourceId가** 있는 **Update-AzTag** cmdlet은 리소스 또는 구독에 대한 태그 집합을 선택적으로 업데이트합니다.
이 작업을 통해 지정된 리소스 또는 구독에서 태그를 바꾸거나, 함께, 선택적으로 삭제할 수 있습니다. 지정된 엔터티는 작업 끝에 최대 50개 태그를 사용할 수 있습니다. 'replace' 옵션은 기존 태그의 전체 집합을 새 집합으로 대체합니다. '병합' 옵션을 사용하면 새 이름의 태그를 추가하고 기존 이름으로 태그 값을 업데이트할 수 있습니다. '삭제' 옵션을 사용하면 지정한 이름 또는 이름/값 쌍에 따라 태그를 선택적으로 삭제할 수 있습니다.

## 예제

### 예제 1: "병합" 작업을 사용하여 구독의 태그 집합을 선택적으로 업데이트합니다.

```powershell
PS C:\>$mergedTags = @{"key1"="value1"; "key3"="value3";}
PS C:\>Update-AzTag -ResourceId /subscriptions/{subId} -Tag $mergedTags -Operation Merge

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             key1     value1
             key2     value2
             key3     value3
```

이 명령은 구독의 태그 집합을 {subId}와 병합합니다.

### 예제 2: "바꾸기" 작업을 사용하여 구독의 태그 집합을 선택적으로 업데이트합니다.

```powershell
PS C:\>$replacedTags = @{"key1"="value1"; "key3"="value3";}
PS C:\>Update-AzTag -ResourceId /subscriptions/{subId} -Tag $replacedTags -Operation Replace

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             key1     value1
             key3     value3
```

이 명령은 {subId}을(를) 사용하여 구독에 태그 집합을 다시 제공합니다.

### 예제 3: "삭제" 작업을 사용하여 구독에서 태그 집합을 선택적으로 업데이트합니다.

```powershell
PS C:\>$deletedTags = @{"key1"="value1"}
PS C:\>Update-AzTag -ResourceId /subscriptions/{subId} -Tag $deletedTags -Operation Delete

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             key3     value3
```

이 명령은 {subId}를 사용하여 구독의 태그 집합을 삭제합니다.

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

### -ResourceId
태그가 지정된 엔터티의 리소스 식별자입니다. 리소스, 리소스 그룹 또는 구독에 태그가 지정될 수 있습니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Merge, Replace, Delete

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tag
업데이트에 사용할 태그 집합입니다.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Operation
업데이트 작업입니다. 옵션은 병합, 바꾸기 및 삭제입니다.

```yaml
Type: Microsoft.Azure.Commands.Tags.Model.TagPatchOperation
Parameter Sets: (All)
Aliases:
Accepted values: Merge, Replace, Delete

Required: True
Position: 2
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

### Microsoft.Azure.Commands.Tags.Model.TagPatchOperation

### System.Collections.Hashtable

## 출력

### Microsoft.Azure.Commands.Tags.Model.PSTagResource

## 참고 사항

## 관련 링크

[Get-AzTag](./Get-AzTag.md)

[New-AzTag](./New-AzTag.md)

[Remove-AzTag](./Remove-AzTag.md)
