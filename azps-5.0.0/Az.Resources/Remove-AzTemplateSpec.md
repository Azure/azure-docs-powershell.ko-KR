---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTemplateSpec.md
ms.openlocfilehash: 718de3ac2da38b8ed7950e8f8a59b0d8fc2f4db7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226542"
---
# Remove-AzTemplateSpec

## SYNOPSIS
서식 파일 사양을 제거 합니다.

## 구문과

### RemoveByNameParameterSet (기본값)
```
Remove-AzTemplateSpec [-Force] [-ResourceGroupName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RemoveByIdParameterSet
```
Remove-AzTemplateSpec [-Force] [[-Version] <String>] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명은
지정 된 서식 파일 사양을 제거 합니다. 버전 **버전** 매개 변수를 제공 하면 지정 된 버전만 제거 됩니다. 특정 버전을 제공 하지 않으면 서식 파일 사양 및 해당 버전이 모두 제거 됩니다. **-Force** 플래그가 표시 되는 경우 제거에 대 한 확인 메시지가 표시 되지 않습니다.

## 예제의

### 예제 1: 이름으로 특정 버전 제거
```powershell
PS C:\> Remove-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec' -Version 'v1.0'
```

리소스 그룹 ' myRG ' 내에서 이름이 ' MyTemplateSpec ' 인 템플릿 사양의 ' v 1.0 ' 버전을 제거 합니다.

### 예제 2: 리소스 id를 기준으로 특정 버전 제거
```powershell
PS C:\> Remove-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -Version 'v1.0'
```

구독 하위 id의 리소스 그룹 ' myRG ' 내에서 이름이 ' MyTemplateSpec ' 인 템플릿 사양의 ' v 1.0 ' 버전을 제거 \{ \} 합니다.

### 예제 3: 이름으로 템플릿 사양 및 모든 버전 제거
```powershell
PS C:\> Remove-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec'
```

리소스 그룹 ' myRG ' 내에서 이름이 ' MyTemplateSpec '이 고 해당 하는 모든 버전이 있는 템플릿 사양을 제거 합니다.

### 예제 3: 리소스 id를 기준으로 템플릿 사양 및 모든 버전 제거
```powershell
PS C:\> Remove-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -ResourceGroupName 'myRG'
```

구독 하위 id의 리소스 그룹 ' myRG ' 내에 있는 ' MyTemplateSpec ' 및 해당 버전의 모든 버전이 포함 된 템플릿 사양을 제거 합니다 \{ \} .

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

### -Force
확인 메시지를 표시 하지 않습니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -이름
템플릿 사양의 이름입니다.

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
템플릿 사양의 리소스 그룹의 이름입니다.

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
템플릿 사양의 정규화 된 리소스 Id입니다. 예:/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}

```yaml
Type: System.String
Parameter Sets: RemoveByIdParameterSet
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -버전
삭제할 템플릿 사양의 버전입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet이 실행 되는 경우의 동작을 보여 줍니다. Cmdlet이 실행 되지 않습니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.

## 입력

### System. 문자열

## 출력

### 시스템 부울

## 상속자

## 관련 링크
