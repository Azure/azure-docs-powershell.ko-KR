---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 39AADD19-2EDD-4C1F-BC9E-22186DD9A085
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmoperatingsystem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMOperatingSystem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMOperatingSystem.md
ms.openlocfilehash: 874045a510c8ab87143e25994fd5f15d5be7e741
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876865"
---
# Set-AzVMOperatingSystem

## SYNOPSIS
가상 컴퓨터에 대 한 운영 체제 속성을 설정 합니다.

## 구문과

### Windows (기본값)
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### WindowsWinRmHttps
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Linux
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Linux] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisablePasswordAuthentication]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzVMOperatingSystem** cmdlet은 가상 컴퓨터의 운영 체제 속성을 설정 합니다.
로그온 자격 증명, 컴퓨터 이름 및 운영 체제 유형을 지정할 수 있습니다.

## 예제의

### 예제 1: 새 가상 컴퓨터의 운영 체제 속성 설정
```
PS C:\> $SecurePassword = ConvertTo-SecureString "Password" -AsPlainText -Force
PS C:\> $Credential = New-Object System.Management.Automation.PSCredential ("FullerP", $SecurePassword); 
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" 
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
PS C:\> $ComputerName = "ContosoVM122"
PS C:\> $WinRMCertUrl = "http://keyVaultName.vault.azure.net/secrets/secretName/secretVersion"
PS C:\> $TimeZone = "Pacific Standard Time"
PS C:\> $CustomData = "echo 'Hello World'"
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $$VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -CustomData $CustomData -WinRMHttp -WinRMHttps -WinRMCertificateUrl $WinRMCertUrl -ProvisionVMAgent -EnableAutoUpdate -TimeZone $TimeZone
```

첫 번째 명령은 암호를 안전한 문자열로 변환한 다음 $SecurePassword 변수에 저장 합니다.
자세한 내용은을 입력 `Get-Help ConvertTo-SecureString` 하세요.

두 번째 명령은 사용자의 자격 증명을 만들고 $SecurePassword에 저장 된 암호를 만든 다음 $Credential 변수에 자격 증명을 저장 합니다.
자세한 내용은을 입력 `Get-Help New-Object` 하세요.

세 번째 명령은 ResourceGroup11 이라는 리소스 그룹에서 AvailablitySet03 이라는 가용성 집합을 가져온 다음 해당 개체를 $AvailabilitySet 변수에 저장 합니다.

네 번째 명령은 가상 컴퓨터 개체를 만든 다음 $VirtualMachine 변수에 저장 합니다.
명령에서 가상 컴퓨터에 이름과 크기를 할당 합니다.
가상 머신이 $AvailabilitySet에 저장 된 가용성 집합에 속합니다.

다음 네 개의 명령은 다음 명령에 사용할 변수에 값을 할당 합니다.
이러한 문자열은 **Set-AzVMOperatingSystem** 명령에서 직접 지정할 수 있으므로이 접근 방식은 가독성을 위해 사용 됩니다.
그러나이 방법을 스크립트에 사용할 수 있습니다.

마지막 명령은 $VirtualMachine에 저장 된 가상 컴퓨터의 운영 체제 속성을 설정 합니다.
이 명령은 $Credential에 저장 된 자격 증명을 사용 합니다.
명령에서는 일부 매개 변수에 대해 이전 명령에서 할당 된 변수를 사용 합니다.

## 변수

### -ComputerName
컴퓨터의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Credential
가상 컴퓨터에 대 한 사용자 이름 및 암호를 **PSCredential** 개체로 지정 합니다.
자격 증명을 얻으려면 Get-Credential cmdlet을 사용 합니다.
자세한 내용은을 입력 `Get-Help Get-Credential` 하세요.

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CustomData
사용자 지정 데이터의 base-64 인코딩된 문자열을 지정 합니다.
이는 가상 컴퓨터에 파일로 저장 된 이진 배열로 디코딩됩니다.
이진 배열의 최대 길이는 65535 바이트입니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisablePasswordAuthentication
이 cmdlet이 암호 인증을 사용 하지 않도록 지정 합니다.

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EnableAutoUpdate 업데이트
이 cmdlet이 자동 업데이트를 사용할 수 있음을 나타냅니다.

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Linux
운영 체제 유형이 Linux 임을 나타냅니다.

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ProvisionVMAgent
설정에 따라 가상 컴퓨터에 가상 컴퓨터 에이전트가 설치 되어 있어야 함을 나타냅니다.

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -표준 시간대
가상 컴퓨터에 대 한 표준 시간대를 지정 합니다.

```yaml
Type: String
Parameter Sets: Windows, WindowsWinRmHttps
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VM
운영 체제 속성을 설정할 로컬 가상 컴퓨터 개체를 지정 합니다.
가상 컴퓨터 개체를 가져오려면 Get-AzVM cmdlet을 사용 합니다.
New-AzVMConfig cmdlet을 사용 하 여 가상 컴퓨터 개체를 만듭니다.

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Windows
운영 체제 유형이 Windows 임을 나타냅니다.

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WinRMCertificateUrl
WinRM 인증서의 URI를 지정 합니다.
이를 키 보관소에 저장 해야 합니다.

```yaml
Type: Uri
Parameter Sets: WindowsWinRmHttps
Aliases: 

Required: True
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WinRMHttp
이 운영 체제에서 HTTP WinRM을 사용 함을 나타냅니다.

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WinRMHttps
이 운영 체제에서 HTTPS WinRM을 사용 함을 나타냅니다.

```yaml
Type: SwitchParameter
Parameter Sets: WindowsWinRmHttps
Aliases: 

Required: True
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### PSVirtualMachine
' VM ' 매개 변수는 파이프라인에서 ' PSVirtualMachine ' 형식의 값을 허용 합니다.

## 출력

### PSVirtualMachine를 계산 합니다.

## 상속자

## 관련 링크

[Get-AzVM](./Get-AzVM.md)

[새로운 AzVMConfig](./New-AzVMConfig.md)


