---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 63BBDF98-75FC-4A44-9FD0-95AD21ED93A6
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/export-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Export-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Export-AzResourceGroup.md
ms.openlocfilehash: 74605a57ab3f2c0898bf3eeb80950f86d4f65d94
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490623"
---
# Export-AzResourceGroup

## SYNOPSIS
리소스 그룹을 템플릿으로 캡처하고 파일에 저장합니다.

## 구문

```
Export-AzResourceGroup -ResourceGroupName <String> [-Path <String>] [-IncludeParameterDefaultValue]
 [-IncludeComments] [-SkipResourceNameParameterization] [-SkipAllParameterization] [-Resource <String[]>]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## 설명
**Export-AzResourceGroup** cmdlet은 지정된 리소스 그룹을 템플릿으로 캡처하고 JSON 파일에 저장합니다. 리소스 그룹에 일부 리소스를 이미 만든 다음 템플릿 지원 배포를 사용하는 이점을 활용하려는 시나리오에서 유용할 수 있습니다.
이 cmdlet을 사용하면 리소스 그룹의 기존 리소스에 대한 템플릿을 생성하여 쉽게 시작할 수 있습니다.
이 cmdlet이 템플릿의 일부를 생성하지 못하는 경우도 있습니다.
경고 메시지는 실패한 리소스를 알 수 있습니다.
템플릿은 성공한 부분에 대해 계속 생성됩니다.

## 예제

### 예제 1: 리소스 그룹 내보내기
```
PS C:\>Export-AzResourceGroup -ResourceGroupName "TestGroup"
```

이 명령은 TestGroup이라는 리소스 그룹을 템플릿으로 캡처하고 현재 디렉터리의 JSON 파일에 저장합니다.

### 예제 2: 리소스 그룹에서 단일 리소스 내보내기
```
PS C:\>Export-AzResourceGroup -ResourceGroupName "TestGroup" -Resource "/subscriptions/5f43547b-1d2d-4a3e-ace4-88d4b600d568/resourceGroups/TestGroup/providers/Microsoft.Compute/virtualMachines/TestVirtualMachine"
```

이 명령은 "TestGroup" 리소스 그룹에서 "TestVirtualMachine"이라는 Virtual Machine 리소스를 템플릿으로 캡처하고 현재 디렉터리의 JSON 파일에 저장합니다.

### 예제 3: 리소스 그룹에서 선택된 리소스 내보내기
```
PS C:\>Export-AzResourceGroup -ResourceGroupName "TestGroup" -SkipAllParameterization -Resource @(
  "/subscriptions/5f43547b-1d2d-4a3e-ace4-88d4b600d568/resourceGroups/TestGroup/providers/Microsoft.Compute/virtualMachines/TestVm",
  "/subscriptions/5f43547b-1d2d-4a3e-ace4-88d4b600d568/resourceGroups/TestGroup/providers/Microsoft.Network/networkInterfaces/TestNic"
)
```

이 명령은 "TestGroup" 리소스 그룹의 두 리소스를 템플릿으로 캡처하고 현재 디렉터리의 JSON 파일에 저장합니다. 생성된 템플릿에는 생성된 매개 변수가 포함되지 않습니다.

## PARAMETERS

### -ApiVersion
사용할 리소스 공급자 API의 버전을 지정합니다.
지정하지 않으면 최신 API 버전이 사용됩니다.

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

### -Force
사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.

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

### -IncludeComments
이 작업은 주석이 있는 템플릿을 내보낼 수 있습니다.

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

### -IncludeParameterDefaultValue
이 작업은 기본값으로 템플릿 매개 변수를 내보낼 수 있습니다.

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

### -Path
템플릿 파일의 출력 경로를 지정합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Pre
사용할 API 버전을 자동으로 결정할 때 이 cmdlet이 릴리스 전 API 버전을 사용 중입니다.

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

### -Resource
결과를 필터링할 resourceId 목록입니다.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
내보낼 리소스 그룹의 이름을 지정합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SkipAllParameterization
모든 매개 변수화를 건너뜁.

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

### -SkipResourceNameParameterization
리소스 이름 매개 변수화 건너뛰기

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

### System.Management.Automation.PSObject

## 참고 사항

## 관련 링크

[Get-AzResourceGroup](./Get-AzResourceGroup.md)


