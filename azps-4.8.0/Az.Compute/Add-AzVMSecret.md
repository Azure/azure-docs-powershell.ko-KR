---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 5008F83F-AF3E-47CF-99A3-55129E654128
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSecret.md
ms.openlocfilehash: 059aedf6ca3b5c229092f9ce536d23a8fc602830
ms.sourcegitcommit: 7aaa37edc9681b643946505bcbc3cc6435f1d7ca
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/10/2020
ms.locfileid: "94395342"
---
# Add-AzVMSecret

## SYNOPSIS
가상 컴퓨터에 비밀을 추가 합니다.

## 구문과

```
Add-AzVMSecret [-VM] <PSVirtualMachine> [[-SourceVaultId] <String>] [[-CertificateStore] <String>]
 [[-CertificateUrl] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**추가-AzVMSecret** cmdlet은 가상 컴퓨터에 비밀을 추가 합니다.
이 값을 사용 하 여 가상 컴퓨터에 인증서를 추가할 수 있습니다.
비밀은 키 보관소에 저장 되어 있어야 합니다.
키 자격 증명 모음에 대 한 자세한 내용은 [Azure 키 보관소 란?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/)을 참조 하세요.
Cmdlet에 대 한 자세한 내용은 [Azure 키 자격 증명 모음 cmdlet](/powershell/module/az.keyvault) 또는 [AzKeyVaultSecret](/powershell/module/az.keyvault/set-azkeyvaultsecret) cmdlet을 참조 하세요.

## 예제의

### 예제 1: 가상 컴퓨터에 비밀 추가
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
PS C:\> $Credential = Get-Credential
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine  -Windows -ComputerName "Contoso26" -Credential $Credential
PS C:\> $SourceVaultId = "/subscriptions/46f8cea4-2de6-4179-8ab1-365da4211af4/resourceGroups/vault/providers/Microsoft.KeyVault/vaults/keyvault"
PS C:\> $CertificateStore01 = "My"
PS C:\> $CertificateUrl01 = "https://contosovault.vault.azure.net/secrets/514ceb769c984379a7e0230bdd703272"
PS C:\> $VirtualMachine = Add-AzVMSecret -VM $VirtualMachine -SourceVaultId $SourceVaultId -CertificateStore $CertificateStore01 -CertificateUrl $CertificateUrl01
```

첫 번째 명령은 가상 컴퓨터 개체를 만든 다음 $VirtualMachine 변수에 저장 합니다.
명령에서 가상 컴퓨터에 이름과 크기를 할당 합니다.
두 번째 명령은 Get-Credential cmdlet을 사용 하 여 credential 개체를 만든 다음 그 결과를 $Credential 변수에 저장 합니다.
명령이 사용자 이름 및 암호를 묻는 메시지를 표시 합니다.
자세한 내용은을 입력 `Get-Help Get-Credential` 하세요.
세 번째 명령은 **AzVMOperatingSystem** cmdlet을 사용 하 여 $VirtualMachine에 저장 된 가상 컴퓨터를 구성 합니다.
네 번째 명령은 나중에 사용할 수 있도록 $SourceVaultId 변수에 원본 자격 증명 모음 ID를 할당 합니다.
명령에서는 $SubscriptionId 변수에 적절 한 값이 있다고 가정 합니다.
다섯 번째 명령은 나중에 사용할 수 있도록 $CertificateStore 01 변수에 값을 할당 합니다.
여섯 번째 명령은 인증서 저장소에 대 한 URL을 할당 합니다.
일곱째 명령은 $VirtualMachine에 저장 된 가상 컴퓨터에 비밀을 추가 합니다.
SourceVaultId 매개 변수는 키 보관소를 지정 합니다.
명령은 인증서 저장소의 이름과 인증서의 URL을 지정 합니다.
**추가-AzVMSecret** 를 반복적으로 실행 하 여 다른 인증서에 대 한 비밀을 추가할 수 있습니다.

## 변수

### -CertificateStore
Windows 운영 체제를 실행 하는 가상 컴퓨터의 인증서 저장소 이름을 지정 합니다.
이 cmdlet은이 매개 변수에서 지정 하는 저장소에 인증서를 추가 합니다.
Windows 운영 체제를 실행 하는 가상 컴퓨터에 대해서만이 매개 변수를 지정할 수 있습니다.

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
인증서를 포함 하는 키 보관소 비밀을 가리키는 URL을 지정 합니다.
인증서는 u t f-8: {"data": " \<Base64-encoded-file\> ", "dataType": "" \<file-format\> , "암호": "", "password" "" ", \<pfx-file-password\> 현재 데이터 형식은 .pfx 파일만 허용 하는 JSON (JavaScript 개체 표기법) 개체의 Base64 인코딩입니다.

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
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

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
가상 컴퓨터에 추가할 수 있는 인증서를 포함 하는 키 보관소의 리소스 ID를 지정 합니다.
이 값은 또한 여러 인증서를 추가 하는 키 역할을 합니다.
즉, 동일한 키 보관소에서 여러 개의 인증서를 추가 하는 경우 *SourceVaultId* 에 동일한 값을 사용할 수 있습니다.

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
이 cmdlet이 수정 하는 가상 컴퓨터 개체를 지정 합니다.
가상 컴퓨터 개체를 가져오려면 [AzVM](./Get-AzVM.md) cmdlet을 사용 합니다.
[새 AzVMConfig](./New-AzVMConfig.md) cmdlet을 사용 하 여 가상 컴퓨터 개체를 만들 수 있습니다.

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
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.

## 입력

### PSVirtualMachine를 계산 합니다.

### System. 문자열

## 출력

### PSVirtualMachine를 계산 합니다.

## 상속자

## 관련 링크

[Get-AzVM](./Get-AzVM.md)

[새로운 AzVMConfig](./New-AzVMConfig.md)

[Set-AzVMOperatingSystem](./Set-AzVMOperatingSystem.md)
