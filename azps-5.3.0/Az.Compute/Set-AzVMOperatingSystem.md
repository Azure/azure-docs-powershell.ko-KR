---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 39AADD19-2EDD-4C1F-BC9E-22186DD9A085
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmoperatingsystem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOperatingSystem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOperatingSystem.md
ms.openlocfilehash: c22e1a09f20eca32cb21056ae45334f0d55ce14b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495912"
---
# Set-AzVMOperatingSystem

## SYNOPSIS
가상 머신에 대한 운영 체제 속성을 지정합니다.

## 구문

### Windows(기본값)
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-PatchMode <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### WindowsWinRmHttps
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri> [-PatchMode <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### WindowsDisableVMAgent
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisableVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-PatchMode <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### WindowsDisableVMAgentWinRmHttps
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisableVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri> [-PatchMode <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Linux
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Linux] [-ComputerName] <String> [-Credential] <PSCredential>
 [[-CustomData] <String>] [-DisablePasswordAuthentication] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
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
$VirtualMachine = Set-AzVMOperatingSystem -VM $$VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -CustomData $CustomData -WinRMHttp -WinRMHttps -WinRMCertificateUrl $WinRMCertUrl -ProvisionVMAgent -EnableAutoUpdate -TimeZone $TimeZone -PatchMode "AutomaticByPlatform"
```

첫 번째 명령은 암호를 보안 문자열로 변환한 다음 $SecurePassword 변수에 저장합니다.
자세한 내용은 `Get-Help ConvertTo-SecureString` .를 입력합니다.
두 번째 명령은 FullerP 사용자에 대한 자격 증명과 사용자에 저장된 암호를 $SecurePassword 자격 증명을 $Credential 변수에 저장합니다.
자세한 내용은 `Get-Help New-Object` .를 입력합니다.
세 번째 명령은 ResourceGroup11이라는 리소스 그룹에서 AvailabilitySet03이라는 가용성 집합을 얻은 다음 해당 개체를 $AvailabilitySet 변수에 저장합니다.
네 번째 명령은 가상 머신 개체를 만든 다음 가상 머신 $VirtualMachine 저장합니다.
이 명령은 가상 머신에 이름 및 크기를 할당합니다.
가상 머신은 가상 머신에 저장된 가용성 집합에 $AvailabilitySet.
다음 네 개의 명령은 다음 명령에서 사용할 변수에 값을 할당합니다.
**Set-AzVMOperatingSystem** 명령에서 직접 이러한 문자열을 지정할 수 있기 때문에 이 방법은 가독성에만 사용됩니다.
그러나 스크립트에서 이와 같은 방법을 사용할 수 있습니다.
마지막 명령은 가상 머신에 저장된 가상 머신에 대한 운영 체제 속성을 $VirtualMachine.
이 명령은 명령에 저장된 자격 증명을 $Credential.
이 명령은 일부 매개 변수에 대해 이전 명령에 할당된 변수를 사용합니다.

## PARAMETERS

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

### -Credential
가상 머신의 사용자 이름 및 암호를 **PSCredential 개체로 지정합니다.**
자격 증명을 얻습니다. Get-Credential cmdlet을 사용 합니다.
자세한 내용은 `Get-Help Get-Credential` .를 입력합니다.

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
사용자 지정 데이터의 base-64로 인코딩된 문자열을 지정합니다.
가상 머신에 파일로 저장된 이진 배열로 디코딩됩니다.
이진 배열의 최대 길이는 65535 바이트입니다.<br>
**참고: customData 속성에 비밀 또는 암호를 전달하지 않습니다.**<br>
VM을 만든 후 이 속성을 업데이트할 수 없습니다. <br>
customData가 파일로 저장될 VM에 전달됩니다. 자세한 내용은 Azure VM의 사용자 지정 데이터를 [참조하세요.](https://azure.microsoft.com/en-us/blog/custom-data-and-cloud-init-on-windows-azure/) <br>
Linux VM에 cloud-init를 사용하는 경우 [cloud-init를](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init) 사용하여 생성 중에 Linux VM 사용자 지정을 참조

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

### -DisablePasswordAuthentication
이 cmdlet이 암호 인증을 사용하지 않도록 설정하는지 나타냅니다.

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
VM 에이전트 프로비전을 사용하지 않도록 설정

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
이 cmdlet을 통해 자동 업데이트를 사용할 수 있습니다.

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
IaaS 가상 머신에 대한 게스트 내 패치 모드를 지정합니다.<br><br>
가능한 값은<br>
**수동** - 가상 머신에 대한 패치의 애플리케이션을 제어합니다. VM 내에서 패치를 수동으로 적용하여 이 작업을 수행하세요. 이 모드에서는 자동 업데이트가 비활성화됩니다. WindowsConfiguration.enableAutomaticUpdates 속성은 false가 되어야 합니다.<br>
**AutomaticByOS** - 가상 머신은 OS에 의해 자동으로 업데이트됩니다. WindowsConfiguration.enableAutomaticUpdates 속성은 true입니다. <br >
**AutomaticByPlatform** - 가상 머신이 OS에 의해 자동으로 업데이트됩니다. properties provisionVMAgent 및 WindowsConfiguration.enableAutomaticUpdates는 true가 되어야 합니다.

```yaml
Type: System.String
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ProvisionVMAgent
가상 머신에 가상 머신 에이전트를 설치해야 하는 설정을 나타냅니다.

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
가상 머신의 표준 시간대를 지정합니다. 예: \" 태평양 표준시 \" <br>
가능한 값은 [TimeZoneInfo.getSystemTimeZones에서](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.getsystemtimezones) [TimeZoneInfo.Id](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) 표준 시간대의 값으로 사용할 수 있습니다.

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
가상 머신 개체를 얻습니다. Get-AzVM cmdlet을 사용합니다.
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
운영 체제의 유형이 Windows인 경우를 나타냅니다.

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
Key Vault에 저장해야 합니다.

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
이 운영 체제가 HTTP WinRM을 사용 중입니다.

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
이 운영 체제가 HTTPS WinRM을 사용 중입니다.

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
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

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


