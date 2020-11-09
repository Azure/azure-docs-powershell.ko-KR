---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 07c6e327-05f4-4279-a5fb-d4e860c897d4
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/update-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzTag.md
ms.openlocfilehash: df34b529a64e1c773c95a5234fd995944e8caac8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94308699"
---
# Update-AzTag

## SYNOPSIS

리소스나 구독의 태그 집합을 선택적으로 업데이트 합니다.

## 구문과

```powershell
Update-AzTag
   -ResourceId <String>
   -Operation <TagPatchOpeation>
   -Tag <Hashtable>
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]

```

## 설명은

**ResourceId** 가 있는 **업데이트-AzTag** cmdlet은 리소스 또는 구독에 대 한 태그 집합을 선택적으로 업데이트 합니다.
이 작업을 수행 하면 지정 된 리소스나 구독의 태그를 바꾸거나, 병합 하거나, 삭제할 수 있습니다. 작업이 끝날 때 지정 된 엔터티는 최대 50 태그를 가질 수 있습니다. ' 바꾸기 ' 옵션은 기존 태그의 전체 집합을 새 집합으로 바꿉니다. ' 병합 ' 옵션을 사용 하면 새 이름으로 태그를 추가 하 고 기존 이름을 사용 하 여 태그 값을 업데이트할 수 있습니다. ' 삭제 ' 옵션을 사용 하면 지정 된 이름 또는 이름/값 쌍을 기준으로 태그를 선택적으로 삭제할 수 있습니다.

## 예제의

### 예제 1: "Merge" 작업을 사용 하 여 선택적으로 구독에 태그 집합을 업데이트 합니다.

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

이 명령은 {subId}를 사용 하 여 구독의 태그 집합을 병합 합니다.

### 예제 2: "바꾸기" 작업을 사용 하 여 선택적으로 구독에 태그 집합을 업데이트 합니다.

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

이 명령은 {subId}를 사용 하 여 구독에 대 한 태그 집합을 Repalces.

### 예제 3: "Delete" 작업을 사용 하 여 구독에서 태그 집합을 선택적으로 업데이트 합니다.

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

이 명령은 {subId}를 사용 하 여 구독에서 태그 집합을 삭제 합니다.

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

### -ResourceId
태그가 지정 된 엔터티의 리소스 식별자입니다. 리소스, 리소스 그룹 또는 구독에 태그가 지정 될 수 있습니다.

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

### 태그
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

### -작업
업데이트 작업입니다. 옵션은 병합, 바꾸기 및 삭제입니다.

```yaml
Type: Microsoft.Azure.Commands.Tags.Model.TagPatchOpeation
Parameter Sets: (All)
Aliases:
Accepted values: Merge, Replace, Delete

Required: True
Position: 2
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

### TagPatchOpeation에 대 한.

### System.webserver. 컬렉션 테이블

## 출력

### PSTagResource에 대 한.

## 상속자

## 관련 링크

[Get-AzTag](./Get-AzTag.md)

[새로운 AzTag](./New-AzTag.md)

[제거-AzTag](./Remove-AzTag.md)