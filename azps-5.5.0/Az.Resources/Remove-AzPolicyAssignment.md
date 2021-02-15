---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 36399302-3EA5-45A3-A042-536CC7EC2E6D
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyAssignment.md
ms.openlocfilehash: 00ec24c13a5c51db7da63cd1d94c01f251a7e289
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201849"
---
# Remove-AzPolicyAssignment

## SYNOPSIS
정책 할당을 제거합니다.

## 구문

### NameParameterSet(기본값)
```
Remove-AzPolicyAssignment -Name <String> [-Scope <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### IdParameterSet
```
Remove-AzPolicyAssignment -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### InputObjectParameterSet
```
Remove-AzPolicyAssignment -InputObject <PsPolicyAssignment> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명
**Remove-AzPolicyAssignment** cmdlet은 지정된 정책 할당을 제거합니다.

## 예제

### 예제 1: 이름 및 범위에 따라 정책 할당 제거
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> Remove-AzPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId -Confirm
```

첫 번째 명령은 Get-AzResourceGroup cmdlet을 사용하여 ResourceGroup11이라는 리소스 그룹을 얻습니다.
이 명령은 해당 개체를 $ResourceGroup 저장합니다.
두 번째 명령은 리소스 그룹 수준에서 할당된 PolicyAssignment07이라는 정책 할당을 제거합니다.
리소스 **그룹의 ResourceId** 속성은 $ResourceGroup 식별합니다.

### 예제 2: ID로 정책 할당 제거
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11' 
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId
PS C:\> Remove-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -Confirm
```

첫 번째 명령은 ResourceGroup11이라는 리소스 그룹을 구한 다음 해당 개체를 $ResourceGroup 변수에 저장합니다.
두 번째 명령은 리소스 그룹 수준에서 정책 할당을 구한 다음, 리소스 $PolicyAssignment 저장합니다.
리소스 **그룹의 ResourceId** 속성은 $ResourceGroup 식별합니다.
마지막 명령은 리소스의 **ResourceId** 속성이 식별하는 $PolicyAssignment 제거합니다.

## PARAMETERS

### -ApiVersion
사용할 리소스 공급자 API의 버전을 지정합니다.
버전을 지정하지 않으면 이 cmdlet은 사용 가능한 최신 버전을 사용하게 됩니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독

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

### -Id
이 cmdlet에서 제거하는 정책 할당에 대한 자격이 있는 리소스 ID를 지정합니다.

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -InputObject
다른 cmdlet에서 출력된 정책을 제거할 정책 할당 개체입니다.

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.Policy.PsPolicyAssignment
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Name
이 cmdlet이 제거하는 정책 할당의 이름을 지정합니다.

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Pre
이 cmdlet은 사용할 버전을 자동으로 결정할 때 릴리스 전 API 버전을 고려합니다.

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

### -Scope
정책이 적용되는 범위를 지정합니다.

```yaml
Type: System.String
Parameter Sets: NameParameterSet
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

## 출력

### System.Boolean

## 참고 사항

## 관련 링크

[Get-AzPolicyAssignment](./Get-AzPolicyAssignment.md)

[New-AzPolicyAssignment](./New-AzPolicyAssignment.md)

[Set-AzPolicyAssignment](./Set-AzPolicyAssignment.md)


