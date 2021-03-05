---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9DDB3672-4C98-4449-9F29-DD9501ED4D3E
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azvmdiskencryptionextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDiskEncryptionExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDiskEncryptionExtension.md
ms.openlocfilehash: 8bdfa0afeb5b558faa91d82df9ccdc64a0b4433c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985292"
---
# Remove-AzVMDiskEncryptionExtension

## SYNOPSIS
가상 머신에서 디스크 암호화 확장을 제거합니다.

## 구문

```
Remove-AzVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Force]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명
**Remove-AzVMDiskEncryptionExtension** cmdlet은 가상 머신에서 디스크 암호화 확장 및 관련 확장 구성을 제거합니다. 확장 이름이 지정되지 않은 경우 이 cmdlet은 Windows 운영 체제를 실행하는 가상 머신의 기본 이름 AzureDiskEncryption 또는 Linux 기반 가상 머신용 AzureDiskEncryptionForLinux를 사용하여 확장을 제거합니다. 

가상 머신의 암호화를 처음 사용하지 않도록 설정하지 않은 경우 이 cmdlet은 실패합니다.  가상 머신에서 암호화를 사용하지 않도록 설정하기 위해 [Disable-AzVMDiskEncryption 을 사용합니다.](./Disable-AzVMDiskEncryption.md) 

## 예제

### 예제 1: 가상 머신에서 디스크 암호화 확장을 제거합니다.
```
PS C:\> Remove-AzVMDiskEncryptionExtension -ResourceGroupName "MyResourceGroup" -VMName "MyTestVM"
```

이 명령은 Windows 운영 체제를 실행하는 가상 머신의 AzureDiskEncryption 또는 MyTestVM이라는 Linux 기반 가상 머신용 AzureDiskEncryptionForLinux를 사용하여 확장을 제거합니다.

### 예제 2: 가상 머신에서 특정 디스크 암호화 확장을 제거합니다.
```
PS C:\> Remove-AzVMDiskEncryptionExtension -ResourceGroupName "MyResourceGroup" -VMName "MyTestVM" -Name "MyDiskEncryptionExtension"
```

이 명령은 MyTestVM이라는 가상 머신에서 MyDiskEncryptionExtension이라는 암호화 확장을 제거합니다.

## 매개 변수

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

### -Name
확장을 나타내는 Azure Resource Manager 리소스의 이름을 지정합니다.
이 Set-AzVMDiskEncryptionExtension cmdlet은 Windows 운영 체제를 실행하는 가상 머신에 대해 AzureDiskEncryption 및 Linux 가상 머신용 AzureDiskEncryptionForLinux로 이 이름을 설정합니다.
**Set-AzVMDiskEncryptionExtension** cmdlet에서 기본 이름을 변경하거나 Resource Manager 템플릿에서 다른 리소스 이름을 사용한 경우만 이 매개 변수를 지정합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
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
가상 머신에 대한 리소스 그룹의 이름을 지정합니다.

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

### -VMName
가상 머신의 이름을 지정합니다.

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

### System.String

## 출력

### Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse

## 참고 사항

## 관련 링크

[Get-AzVMDiskEncryptionStatus](./Get-AzVMDiskEncryptionStatus.md)

[Set-AzVMDiskEncryptionExtension](./Set-AzVMDiskEncryptionExtension.md)


