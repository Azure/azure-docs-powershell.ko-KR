---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 39AADD19-2EDD-4C1F-BC9E-22186DD9A085
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmoperatingsystem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOperatingSystem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOperatingSystem.md
ms.openlocfilehash: 75eb0ef60443cdbf2dfe3fa53202d3c8141d4888
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990444"
---
# Set-AzVMOperatingSystem

## SYNOPSIS
가상 머신에 대한 운영 체제 속성을 설정합니다.

## 구문

### Windows(기본값)
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-PatchMode <String>] [-EnableHotpatching]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### WindowsWinRmHttps
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri> [-PatchMode <String>]
 [-EnableHotpatching] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### WindowsDisableVMAgent
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisableVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-PatchMode <String>] [-EnableHotpatching]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### WindowsDisableVMAgentWinRmHttps
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisableVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri> [-PatchMode <String>]
 [-EnableHotpatching] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Linux
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Linux] [-ComputerName] <String> [-Credential] <PSCredential>
 [[-CustomData] <String>] [-PatchMode <String>] [-DisablePasswordAuthentication]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
**Set-AzVMOperatingSystem** cmdlet은 가상 머신에 대한 운영 체제 속성을 설정합니다.
로그온 자격 증명, 컴퓨터 이름 및 운영 체제 유형을 지정할 수 있습니다.

## 예제

### 예제 1: 새 가상 머신에 대한 운영 체제 속성 설정
```
$SecurePassword = ConvertTo-SecureString "Password" -AsPlainText -Force
$Credential = New-Object System.Management.Automation.PSCredential ("FullerP", $SecurePassword); 
$AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" 
$VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
$ComputerName = "ContosoVM122"
$WinRMCertUrl = "http://keyVaultName.vault.azure.net/secrets/secretName/secretVersion"
$TimeZone = "Pacific Standard Time"
$CustomData = "echo 'Hello World'"
$VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -CustomData $CustomData -WinRMHttp -WinRMHttps -WinRMCertificateUrl $WinRMCertUrl -ProvisionVMAgent -EnableAutoUpdate -TimeZone $TimeZone -PatchMode "AutomaticByPlatform"
```

첫 번째 명령은 암호를 보안 문자열로 변환한 다음, 암호 $SecurePassword 저장합니다.
자세한 내용은 `Get-Help ConvertTo-SecureString` 를 입력합니다.
두 번째 명령은 사용자 FullerP 및 암호에 저장된 암호에 대한 자격 증명을 $SecurePassword 자격 증명을 $Credential 변수에 저장합니다.
자세한 내용은 `Get-Help New-Object` 를 입력합니다.
세 번째 명령은 ResourceGroup11이라는 리소스 그룹에서 AvailabilitySet03이라는 가용성 집합을 얻은 다음 해당 개체를 $AvailabilitySet 저장합니다.
네 번째 명령은 가상 머신 개체를 만든 다음, 가상 머신 개체를 $VirtualMachine 변수에 저장합니다.
명령은 가상 머신에 이름과 크기를 할당합니다.
가상 머신은 가상 머신에 저장된 가용성 집합에 $AvailabilitySet.
다음 네 개의 명령은 다음 명령에서 사용할 변수에 값을 할당합니다.
**Set-AzVMOperatingSystem** 명령에서 직접 이러한 문자열을 지정할 수 있기 때문에 이 방법은 가독성에만 사용됩니다.
그러나 스크립트에서 이와 같은 방법을 사용할 수 있습니다.
최종 명령은 가상 머신에 저장된 가상 머신에 대한 운영 체제 속성을 $VirtualMachine.
명령은 명령에 저장된 자격 증명을 $Credential.
명령은 일부 매개 변수에 대해 이전 명령에 할당된 변수를 사용합니다.

### 예제 2: 핫 패치를 사용하도록 설정된 새 가상 머신에 대한 운영 체제 속성 설정
```
$SecurePassword = ConvertTo-SecureString "Password" -AsPlainText -Force
$Credential = New-Object System.Management.Automation.PSCredential ("FullerP", $SecurePassword); 
$AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" 
$VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
$ComputerName = "ContosoVM122"
$WinRMCertUrl = "http://keyVaultName.vault.azure.net/secrets/secretName/secretVersion"
$TimeZone = "Pacific Standard Time"
$CustomData = "echo 'Hello World'"
$VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -CustomData $CustomData -WinRMHttp -WinRMHttps -WinRMCertificateUrl $WinRMCertUrl -ProvisionVMAgent -EnableAutoUpdate -TimeZone $TimeZone -PatchMode "AutomaticByPlatform" -EnableHotPatching
```

첫 번째 명령은 암호를 보안 문자열로 변환한 다음, 암호 $SecurePassword 저장합니다.
자세한 내용은 `Get-Help ConvertTo-SecureString` 를 입력합니다.
두 번째 명령은 사용자 FullerP 및 암호에 저장된 암호에 대한 자격 증명을 $SecurePassword 자격 증명을 $Credential 변수에 저장합니다.
자세한 내용은 `Get-Help New-Object` 를 입력합니다.
세 번째 명령은 ResourceGroup11이라는 리소스 그룹에서 AvailabilitySet03이라는 가용성 집합을 얻은 다음 해당 개체를 $AvailabilitySet 저장합니다.
네 번째 명령은 가상 머신 개체를 만든 다음, 가상 머신 개체를 $VirtualMachine 변수에 저장합니다.
명령은 가상 머신에 이름과 크기를 할당합니다.
가상 머신은 가상 머신에 저장된 가용성 집합에 $AvailabilitySet.
다음 네 개의 명령은 다음 명령에서 사용할 변수에 값을 할당합니다.
**Set-AzVMOperatingSystem** 명령에서 직접 이러한 문자열을 지정할 수 있기 때문에 이 방법은 가독성에만 사용됩니다.
그러나 스크립트에서 이와 같은 방법을 사용할 수 있습니다.
최종 명령은 가상 머신에 저장된 가상 머신에 대한 운영 체제 속성을 $VirtualMachine.
명령은 명령에 저장된 자격 증명을 $Credential.
명령은 일부 매개 변수에 대해 이전 명령에 할당된 변수를 사용합니다.
이 명령은 가상 머신에서 Hotpatching을 사용할 수 있습니다.

### 예제 3: 새 Linux 가상 머신에 대한 운영 체제 속성 설정
```
$SecurePassword = ConvertTo-SecureString "Password" -AsPlainText -Force
$Credential = New-Object System.Management.Automation.PSCredential ("FullerP", $SecurePassword); 
$AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" 
$VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
$ComputerName = "ContosoVM122"
$CustomData = "echo 'Hello World'"
$VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Linux -ComputerName $ComputerName -Credential $Credential -CustomData $CustomData -PatchMode "AutomaticByPlatform"
```

첫 번째 명령은 암호를 보안 문자열로 변환한 다음, 암호 $SecurePassword 저장합니다.
자세한 내용은 `Get-Help ConvertTo-SecureString` 를 입력합니다.
두 번째 명령은 사용자 FullerP 및 암호에 저장된 암호에 대한 자격 증명을 $SecurePassword 자격 증명을 $Credential 변수에 저장합니다.
자세한 내용은 `Get-Help New-Object` 를 입력합니다.
세 번째 명령은 ResourceGroup11이라는 리소스 그룹에서 AvailabilitySet03이라는 가용성 집합을 얻은 다음 해당 개체를 $AvailabilitySet 저장합니다.
네 번째 명령은 가상 머신 개체를 만든 다음, 가상 머신 개체를 $VirtualMachine 변수에 저장합니다.
명령은 가상 머신에 이름과 크기를 할당합니다.
가상 머신은 가상 머신에 저장된 가용성 집합에 $AvailabilitySet.
다음 두 명령은 다음 명령에서 사용할 변수에 값을 할당합니다.
최종 명령은 가상 머신에 저장된 가상 머신에 대한 운영 체제 속성을 $VirtualMachine.
명령은 명령에 저장된 자격 증명을 $Credential.
명령은 일부 매개 변수에 대해 이전 명령에 할당된 변수를 사용합니다.
명령은 가상 머신의 패치 모드 값을 "AutomaticByPlatform"으로 설정합니다.

## 매개 변수

### -ComputerName
컴퓨터의 이름을 지정합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -자격 증명
가상 머신에 대한 사용자 이름 및 암호를 **PSCredential 개체로 지정합니다.**
자격 증명을 얻은 경우 Get-Credential cmdlet을 사용 합니다.
자세한 내용은 `Get-Help Get-Credential` 를 입력합니다.

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CustomData
가상 머신에 전달할 문자열을 지정합니다. 자세한 내용은 [Azure VM의 사용자 지정 데이터를 참조하세요.](https://docs.microsoft.com/en-us/azure/virtual-machines/custom-data)
**참고: 사용자 지정 데이터에 중요한 정보를 저장하는 것은 권장되지 않습니다.**


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

### -DisablePasswordAuthentication
이 cmdlet이 암호 인증을 사용하지 않도록 설정하고 있습니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Linux
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DisableVMAgent
프로비전 VM 에이전트를 사용하지 않도록 설정합니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableAutoUpdate
이 cmdlet에서 자동 업데이트를 사용할 수 있습니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EnableHotpatching
고객이 다시 부팅하지 않고도 Azure VM을 패치할 수 있습니다. enableHotpatching의 경우 'provisionVMAgent'를 true로 설정하고 'patchMode'를 'AutomaticByPlatform'으로 설정해야 합니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Linux
운영 체제 유형이 Linux인 경우를 나타냅니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Linux
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PatchMode
IaaS 가상 머신에 게스트 내 패치 모드를 지정합니다.<br><br>
가능한 값은:<br>
**수동** - 가상 머신에 패치 적용을 제어합니다. 이 작업을 수행하려면 VM 내부에 수동으로 패치를 적용합니다. 이 모드에서는 자동 업데이트를 사용할 수 없습니다. 속성 WindowsConfiguration.enableAutomaticUpdates는 false가 되어야 합니다.<br>
**자동ByOS** - 가상 머신은 OS에 의해 자동으로 업데이트됩니다. 속성 WindowsConfiguration.enableAutomaticUpdates는 true가 되어야 합니다. <br >
**AutomaticByPlatform** - 가상 머신이 OS에 의해 자동으로 업데이트됩니다. 속성 프로비전VMAgent 및 WindowsConfiguration.enableAutomaticUpdates는 true가 되어야 합니다.

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

### -ProvisionVMAgent
설정에서 가상 머신 에이전트를 가상 머신에 설치해야 합니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TimeZone
가상 머신의 표준 시간대를 지정합니다. 예: \" 태평양 표준시 \" 입니다. <br>
가능한 값은 [](https://docs.microsoft.com/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) [TimeZoneInfo.GetSystemTimeZones에서](https://docs.microsoft.com/dotnet/api/system.timezoneinfo.getsystemtimezones)TimeZoneInfo.Id 표준 시간대에서 값으로 사용할 수 있습니다.

```yaml
Type: System.String
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VM
운영 체제 속성을 설정할 로컬 가상 머신 개체를 지정합니다.
가상 머신 개체를 얻은 경우 Get-AzVM cmdlet을 사용합니다.
New-AzVMConfig cmdlet을 사용하여 가상 머신 개체를 만듭니다.

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Windows
운영 체제 유형이 Windows인 경우를 나타냅니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WinRMCertificateUrl
WinRM 인증서의 URI를 지정합니다.
이 파일은 Key Vault에 저장해야 합니다.

```yaml
Type: System.Uri
Parameter Sets: WindowsWinRmHttps, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: True
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WinRMHttp
이 운영 체제에서 HTTP WinRM을 사용하는지 나타냅니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WinRMHttps
이 운영 체제에서 HTTPS WinRM을 사용하는지 나타냅니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WindowsWinRmHttps, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: True
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## 입력

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine

### System.Management.Automation.SwitchParameter

### System.String

### System.Management.Automation.PSCredential

### System.Uri

## 출력

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine

## 참고 사항

## 관련 링크

[Get-AzVM](./Get-AzVM.md)

[New-AzVMConfig](./New-AzVMConfig.md)


