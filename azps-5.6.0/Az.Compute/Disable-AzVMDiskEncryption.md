---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 979E956B-4C74-426E-A617-E50C4EBC8A20
online version: https://docs.microsoft.com/powershell/module/az.compute/disable-azvmdiskencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Disable-AzVMDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Disable-AzVMDiskEncryption.md
ms.openlocfilehash: bd96a26eda14770dcc7a5592e12e64e15eac02f6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101969435"
---
# Disable-AzVMDiskEncryption

## SYNOPSIS
IaaS 가상 머신에서 암호화를 사용하지 않도록 설정합니다.

## 구문

```
Disable-AzVMDiskEncryption [-ResourceGroupName] <String> [-VMName] <String> [[-VolumeType] <String>]
 [[-Name] <String>] [[-TypeHandlerVersion] <String>] [-Force] [-DisableAutoUpgradeMinorVersion]
 [-ExtensionType <String>] [-ExtensionPublisherName <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명
**Disable-AzVMDiskEncryption** cmdlet은 IaaS(가상 머신)로 인프라에서 암호화를 사용하지 않도록 설정합니다.
이 cmdlet은 Linux 가상 머신이 아닌 Windows 가상 머신에서만 지원됩니다.
이 cmdlet은 암호화를 사용하지 않도록 설정하기 위해 가상 머신에 확장을 설치합니다.
이름 *매개* 변수를 지정하지 않으면 기본 이름 "Windows VM용 AzureDiskEncryption"이 있는 확장이 만들어집니다.
주의: 이 cmdlet은 가상 머신을 다시 부트합니다.

## 예제

### 예제 1: Windows 가상 머신의 모든 볼륨에 대한 암호화 사용 안 하세요.
```
PS C:\> Disable-AzVMDiskEncryption -ResourceGroupName "Group001" -VMName "VM002"
```

이 명령은 Group001이라는 리소스 그룹에 속하는 VM002라는 가상 머신에 대한 모든 형식의 볼륨에 대한 암호화를 사용하지 않도록 설정합니다.
*VolumeType* 매개 변수가 지정되지 않은 경우 cmdlet은 값을 모두로 설정합니다.

### 예제 2: Windows 가상 머신의 데이터 볼륨에 대한 암호화 사용 안 하세요.
```
PS C:\> $ResourceGroup = "Group002"
PS C:\> $VMName = "VM004"
PS C:\> $VolumeType = "Data"
PS C:\> Disable-AzVMDiskEncryption -ResourceGroupName $ResourceGroup -VMName $VMName -VolumeType $VolumeType
```

이 명령은 Group002라는 리소스 그룹에 속하는 VM004라는 가상 머신에 대한 형식 데이터 볼륨에 대한 암호화를 사용하지 않도록 설정합니다.

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

### -DisableAutoUpgradeMinorVersion
이 cmdlet은 확장의 부 버전 자동 업그레이드를 사용하지 않도록 설정하고 있습니다.

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

### -ExtensionPublisherName
확장 게시자 이름입니다. 이 매개 변수를 지정하여 "Microsoft.Azure.Security"의 기본값을 오버라이드합니다.

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

### -ExtensionType
확장 형식입니다. 이 매개 변수를 지정하여 Windows VM에 대한 "AzureDiskEncryption" 및 Linux VM에 대한 "AzureDiskEncryptionForLinux"의 기본값을 오버라이드합니다.

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
확장을 나타내는 Azure Resource Manager(ARM) 리소스의 이름을 지정합니다.
이 매개 변수를 지정하지 않으면 이 cmdlet은 "Windows VM용 AzureDiskEncryption"으로 기본값을 지정합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
가상 머신의 리소스 그룹 이름을 지정합니다.

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
암호화 확장의 버전을 지정합니다.
이 매개 변수에 대한 값을 지정하지 않으면 확장의 최신 버전이 사용됩니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMName
이 cmdlet에서 암호화를 사용하지 않도록 설정하는 가상 머신의 이름을 지정합니다.

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

### -VolumeType
암호화 작업을 수행할 가상 머신 볼륨 유형을 지정합니다.
Windows 가상 머신의 경우 유효한 값은 다음을 나타냅니다. 
- 모두
- OS
- 데이터입니다.
이 매개 변수에 대한 값을 지정하지 않으면 기본값은 모두입니다.
암호화를 사용하지 않도록 설정하는 것은 현재 Linux에 지원되지 않습니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: OS, Data, All

Required: False
Position: 2
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

### System.Management.Automation.SwitchParameter

## 출력

### Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse

## 참고 사항

## 관련 링크

[Get-AzVMDiskEncryptionStatus](./Get-AzVMDiskEncryptionStatus.md)

[Remove-AzVMDiskEncryptionExtension](./Remove-AzVMDiskEncryptionExtension.md)

[Set-AzVMDiskEncryptionExtension](./Set-AzVMDiskEncryptionExtension.md)


