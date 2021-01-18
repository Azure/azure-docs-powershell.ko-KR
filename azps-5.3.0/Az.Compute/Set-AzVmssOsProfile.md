---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3E7B9EFA-8BC2-46EB-9AD7-43EAB7FF3891
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssosprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssOsProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssOsProfile.md
ms.openlocfilehash: 71bd8ca26755118a4bb9c075ae89bad765922f3d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98493799"
---
# Set-AzVmssOsProfile

## SYNOPSIS
VMSS 운영 체제 프로필 속성을 지정합니다.

## 구문

```
Set-AzVmssOsProfile [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-ComputerNamePrefix] <String>]
 [[-AdminUsername] <String>] [[-AdminPassword] <String>] [[-CustomData] <String>]
 [[-WindowsConfigurationProvisionVMAgent] <Boolean>] [[-WindowsConfigurationEnableAutomaticUpdate] <Boolean>]
 [[-TimeZone] <String>] [[-AdditionalUnattendContent] <AdditionalUnattendContent[]>]
 [[-Listener] <WinRMListener[]>] [[-LinuxConfigurationDisablePasswordAuthentication] <Boolean>]
 [[-PublicKey] <SshPublicKey[]>] [[-Secret] <VaultSecretGroup[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명
**Set-AzVmssOsProfile** cmdlet은 Virtual Machine Scale Set 운영 체제 프로필 속성을 설정합니다.

## 예제

### 예제 1: VMSS에 대한 운영 체제 프로필 속성 설정
```
PS C:\> Set-AzVmssOSProfile -VirtualMachineScaleSet "ContosoVMSS" -ComputerNamePrefix "Test" -AdminUsername $AdminUsername -AdminPassword $AdminPassword
```

이 명령은 ContosoVMSS라는 VMSS에 속하는 가상 머신에 대한 운영 체제 프로필 속성을 설정합니다.
이 명령은 테스트할 VMSS의 모든 가상 머신 인스턴스에 대한 컴퓨터 이름 prefix를 설정하고 관리자 사용자 이름과 암호를 제공합니다.

## PARAMETERS

### -AdditionalUnattendContent
무인 콘텐츠 개체를 지정합니다.
개체를 만드는 데 Add-AzVMAdditionalUnattendContent 수 있습니다.

```yaml
Type: Microsoft.Azure.Management.Compute.Models.AdditionalUnattendContent[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AdminPassword
VMSS의 모든 가상 머신 인스턴스에 사용할 관리자 암호를 지정합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AdminUsername
VMSS의 모든 가상 머신 인스턴스에 사용할 관리자 계정 이름을 지정합니다. <br>
**Windows 전용 제한:** .로 끝날 수 \" 없습니다.\" <br>
**수 없습니다.** \" \"관리자, \" \" 관리자, \" \" 사용자, \" \" user1, \" \" 테스트, \" \" user2, \" \" test1, \" \" user3, \" \" admin1, \" \" 1 , \" 123, \" a , \" \" \" actuser, \" \" \" adm, \" \" admin2, \" aspnet, \" \" \" backup, console , \" \" \" \" david, guest , \" \" \" john, \" \" \" owner, \" \" root, \" \" server, \" \" sql, support , support_388945a0 \" \" , \" \" \" sys, \" \" \" test2, \" \" test3, \" \" user4, \" \" user5. <br>
**최소 길이(Linux):** 1자 <br>
**최대 길이(Linux):** 64자 <br>
**최대 길이(Windows):** 20자  <br>
<li> Linux VM에 대한 루트 액세스는 Azure의 Linux 가상 머신에서 루트 권한 [사용을 참조하세요.](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-use-root-privileges?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json)<br>
<li> 이 필드에서 사용할 수 없는 Linux의 기본 제공 시스템 사용자 목록은 Azure에서 Linux용 사용자 이름 [선택을 참조하세요.](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-usernames?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json)

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

### -ComputerNamePrefix
VMSS의 모든 가상 머신 인스턴스에 대한 컴퓨터 이름의 연결부를 지정합니다.
컴퓨터 이름은 1~15자 되어야 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CustomData
사용자 지정 데이터의 base-64로 인코딩된 문자열을 지정합니다.
가상 머신에 파일로 저장된 이진 배열로 디코딩됩니다.
이진 배열의 최대 길이는 65535 바이트입니다. <br>
VM에 cloud-init를 사용하는 경우 [cloud-init를 사용하여 생성 중에 Linux VM을 사용자 지정하는 방법을 참조합니다.](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json)

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### -LinuxConfigurationDisablePasswordAuthentication
이 cmdlet이 암호 인증을 사용하지 않도록 설정하는지 나타냅니다.

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Listener
WinRM(Windows 원격 관리) 수신기를 지정합니다.
이렇게 하면 원격 Windows PowerShell.
Add-AzVmssWinRMListener cmdlet을 사용하여 수신기 만들 수 있습니다.

```yaml
Type: Microsoft.Azure.Management.Compute.Models.WinRMListener[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PublicKey
SSH(Secure Shell) 공개 키 개체를 지정합니다.
Add-AzVMSshPublicKey cmdlet을 사용하여 개체를 만들 수 있습니다.

```yaml
Type: Microsoft.Azure.Management.Compute.Models.SshPublicKey[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Secret
가상 머신에 두기 위한 인증서 참조를 포함하는 비밀 개체를 지정합니다.
Add-AzVmssSecret cmdlet을 사용하여 비밀 개체를 만들 수 있습니다.

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VaultSecretGroup[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 12
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TimeZone
가상 머신의 표준 시간대를 지정합니다. 예: \" 태평양 표준시 \" <br>
가능한 값은 [TimeZoneInfo.getSystemTimeZones에서](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.getsystemtimezones) [TimeZoneInfo.Id](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) 표준 시간대의 값으로 사용할 수 있습니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualMachineScaleSet
VMSS 개체를 지정합니다.
New-AzVmssConfig cmdlet을 사용하여 개체를 만들 수 있습니다.

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -WindowsConfigurationEnableAutomaticUpdate
VMSS의 가상 머신이 자동 업데이트를 사용하도록 설정되어 있는지 여부를 나타냅니다.

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WindowsConfigurationProvisionVMAgent
VMSS의 가상 머신에 가상 머신 에이전트를 프로비전해야 하는지 여부를 나타냅니다.

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
cmdlet이 실행되는 경우의 결과 표시 cmdlet이 실행되지 않습니다.

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
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## 입력

### Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet

### System.String

### System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

### Microsoft.Azure.Management.Compute.Models.AdditionalUnattendContent[]

### Microsoft.Azure.Management.Compute.Models.WinRMListener[]

### Microsoft.Azure.Management.Compute.Models.SshPublicKey[]

### Microsoft.Azure.Management.Compute.Models.VaultSecretGroup[]

## 출력

### Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet

## 참고 사항

## 관련 링크

[Add-AzVMAdditionalUnattendContent](./Add-AzVMAdditionalUnattendContent.md)

[Add-AzVmssWinRMListener](./Add-AzVmssWinRMListener.md)

[Add-AzVMSshPublicKey](./Add-AzVMSshPublicKey.md)

[Add-AzVmssSecret](./Add-AzVmssSecret.md)

[New-AzVmssConfig](./New-AzVmssConfig.md)


