---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D93666EC-C252-4E3B-B311-50B6EEA6D4BF
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmaccessextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMAccessExtension.md
ms.openlocfilehash: 3b5d877186ec82cad5246b122908eb0ca19ab47c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001696"
---
# Set-AzVMAccessExtension

## SYNOPSIS
VMAccess 확장을 가상 머신에 추가합니다.

## 구문

```
Set-AzVMAccessExtension [-Credential <PSCredential>] [-ResourceGroupName] <String> [-VMName] <String>
 [-Name <String>] [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion]
 [-ForceRerun <String>] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## 설명
**Set-AzVMAccessExtension** cmdlet은 VMAccess(Virtual Machine Access) Virtual Machine VMAccess 확장을 가상 머신에 추가합니다. VMAccess 확장을 사용하여 임시 암호를 설정할 수 있으며 컴퓨터에 로그인한 후 즉시 변경해야 합니다. Windows 도메인 컨트롤러에서는 지원되지 않습니다.

## 예제

### 예제 1: VMAccess 확장 추가
```powershell
PS C:\> Set-AzVMAccessExtension -ResourceGroupName "ResourceGroup11" -Location "Central US" -VMName "VirtualMachine07" -Name "ContosoTest" -TypeHandlerVersion "2.4" -UserName "PFuller" -Password "Password"
```

이 명령은 ResourceGroup11에서 VirtualMachine07이라는 가상 머신에 대한 VMAccess 확장을 추가합니다.
명령은 VMAccess에 대한 이름 및 형식 처리기 버전을 지정합니다.

### 예제 2

VMAccess 확장을 가상 머신에 추가합니다. (자동 재생)

```powershell <!-- Aladdin Generated Example --> 
Set-AzVMAccessExtension -Credential <PSCredential> -Location 'Central US' -Name 'ContosoTest' -ResourceGroupName 'ResourceGroup11' -TypeHandlerVersion '2.4' -VMName 'VirtualMachine07'
```

## 매개 변수

### -자격 증명
가상 머신에 대한 사용자 이름 및 암호를 **PSCredential 개체로 지정합니다.**
VM의 현재 로컬 관리자 계정과 다른 이름을 입력하면 VMAccess 확장에서 해당 이름이 있는 로컬 관리자 계정을 추가하고 지정된 암호를 해당 계정에 할당합니다. VM의 로컬 관리자 계정이 있는 경우 암호를 다시 설정하고 계정을 사용하지 않도록 설정하면 VMAccess 확장을 사용할 수 있습니다.
자격 증명을 얻은 경우 Get-Credential cmdlet을 사용 합니다.
자세한 내용은 `Get-Help Get-Credential` 를 입력합니다.

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.

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

### -DisableAutoUpgradeMinorVersion
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

### -ForceRerun
이 cmdlet은 확장을 삭제하고 다시 설치하지 않고 가상 머신에서 동일한 확장 구성을 다시 억지합니다.
값은 현재 값과 다른 문자열일 수 있습니다.
forceUpdateTag가 변경되지 않은 경우 처리기에서 공용 또는 보호된 설정에 대한 업데이트가 계속 적용됩니다.

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

### -Location
가상 머신의 위치를 지정합니다.

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

### -Name
이 cmdlet이 추가하는 확장의 이름을 지정합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NoWait
작업을 시작하고 작업이 완료되기 전에 즉시 반환합니다. 작업이 성공적으로 완료된지 확인하기 위해 다른 메커니즘을 사용 합니다.

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

### -ResourceGroupName
가상 머신의 리소스 그룹의 이름을 지정합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TypeHandlerVersion
이 가상 머신에 사용할 확장 버전을 지정합니다.
버전을 얻게 Get-AzVMExtensionImage *Type* 매개 변수에 대한 Microsoft.Compute 매개 변수 및 VMAccessAgent 값을 사용하여 Get-AzVMExtensionImage cmdlet을 *실행합니다.* 버전 1이 사용되지 않습니다. typeHandlerVersion은 2.0 이상이 되어야 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMName
가상 머신의 이름을 지정합니다.
이 cmdlet은 이 매개 변수가 지정하는 가상 머신에 대한 VMAccess를 추가합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -확인
cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.

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
cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.
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
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## 입력

### System.Management.Automation.PSCredential

### System.String

### System.Management.Automation.SwitchParameter

## 출력

### Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse

## 참고 사항

## 관련 링크

[Get-AzVMAccessExtension](./Get-AzVMAccessExtension.md)

[Remove-AzVMAccessExtension](./Remove-AzVMAccessExtension.md)

[Set-AzVMExtension](./Set-AzVMExtension.md)

[Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md)


