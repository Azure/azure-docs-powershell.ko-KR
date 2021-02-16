---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 5008F83F-AF3E-47CF-99A3-55129E654128
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSecret.md
ms.openlocfilehash: 059aedf6ca3b5c229092f9ce536d23a8fc602830
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199361"
---
# Add-AzVMSecret

## SYNOPSIS
가상 머신에 비밀을 추가합니다.

## 구문

```
Add-AzVMSecret [-VM] <PSVirtualMachine> [[-SourceVaultId] <String>] [[-CertificateStore] <String>]
 [[-CertificateUrl] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
**Add-AzVMSecret** cmdlet은 가상 머신에 비밀을 추가합니다.
이 값을 사용하면 가상 머신에 인증서를 추가할 수 있습니다.
비밀은 Key Vault에 저장되어야 합니다.
Key Vault에 대한 자세한 내용은 [Azure Key Vault란?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/)
cmdlet에 대한 자세한 내용은 [Azure Key Vault Cmdlet 또는](/powershell/module/az.keyvault) [Set-AzKeyVaultSecret](/powershell/module/az.keyvault/set-azkeyvaultsecret) cmdlet을 참조하세요.

## 예제

### 예제 1: 가상 머신에 비밀 추가
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
PS C:\> $Credential = Get-Credential
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine  -Windows -ComputerName "Contoso26" -Credential $Credential
PS C:\> $SourceVaultId = "/subscriptions/46f8cea4-2de6-4179-8ab1-365da4211af4/resourceGroups/vault/providers/Microsoft.KeyVault/vaults/keyvault"
PS C:\> $CertificateStore01 = "My"
PS C:\> $CertificateUrl01 = "https://contosovault.vault.azure.net/secrets/514ceb769c984379a7e0230bdd703272"
PS C:\> $VirtualMachine = Add-AzVMSecret -VM $VirtualMachine -SourceVaultId $SourceVaultId -CertificateStore $CertificateStore01 -CertificateUrl $CertificateUrl01
```

첫 번째 명령은 가상 머신 개체를 만든 다음 가상 머신 $VirtualMachine 저장합니다.
이 명령은 가상 머신에 이름 및 크기를 할당합니다.
두 번째 명령은 Get-Credential cmdlet을 사용하여 자격 증명 개체를 만든 다음, $Credential 변수에 저장합니다.
이 명령은 사용자 이름 및 암호를 묻는 메시지를 제공합니다.
자세한 내용은 `Get-Help Get-Credential` .를 입력합니다.
세 번째 명령은 **Set-AzVMOperatingSystem** cmdlet을 사용하여 $VirtualMachine.
네 번째 명령은 나중에 사용할 수 $SourceVaultId 원본 자격 증명 모음 ID를 할당합니다.
이 명령은 $SubscriptionId 변수에 적절한 값이 있는 것으로 가정합니다.
다섯 번째 명령은 나중에 사용하기 위해 $CertificateStore 01 변수에 값을 할당합니다.
여섯 번째 명령은 인증서 저장소에 대한 URL을 할당합니다.
7번째 명령은 가상 머신에 저장된 가상 머신에 비밀을 $VirtualMachine.
SourceVaultId 매개 변수는 Key Vault를 지정합니다.
이 명령은 인증서 저장소의 이름과 인증서의 URL을 지정합니다.
**Add-AzVMSecret을** 반복적으로 실행하여 다른 인증서에 대한 비밀을 추가할 수 있습니다.

## PARAMETERS

### -CertificateStore
Windows 운영 체제를 실행하고 있는 가상 머신에서 인증서 저장소의 이름을 지정합니다.
이 cmdlet은 이 매개 변수가 지정하는 인증서를 저장소에 추가합니다.
Windows 운영 체제를 실행하는 가상 머신에만 이 매개 변수를 지정할 수 있습니다.

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

### -CertificateUrl
인증서를 포함하는 Key Vault 비밀을 지정하는 URL을 지정합니다.
인증서는 다음 JSON(JavaScript Object Notation) 개체의 Base64 인코딩으로, UTF-8: { "data": " \<Base64-encoded-file\> ", "dataType": " \<file-format\> ", "password": " \<pfx-file-password\> " } 현재 dataType은 .pfx 파일만 허용합니다.

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

### -SourceVaultId
가상 머신에 추가할 수 있는 인증서를 포함하는 Key Vault의 리소스 ID를 지정합니다.
또한 이 값은 여러 인증서를 추가하기 위한 키 역할을 합니다.
즉, 동일한 Key Vault에서 여러 인증서를 추가할 때 *SourceVaultId에* 동일한 값을 사용할 수 있습니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Id

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VM
이 cmdlet이 수정하는 가상 머신 개체를 지정합니다.
가상 머신 개체를 얻습니다. [Get-AzVM](./Get-AzVM.md) cmdlet을 사용합니다.
[New-AzVMConfig](./New-AzVMConfig.md) cmdlet을 사용하여 가상 머신 개체를 만들 수 있습니다.

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

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## 입력

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine

### System.String

## 출력

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine

## 참고 사항

## 관련 링크

[Get-AzVM](./Get-AzVM.md)

[New-AzVMConfig](./New-AzVMConfig.md)

[Set-AzVMOperatingSystem](./Set-AzVMOperatingSystem.md)
