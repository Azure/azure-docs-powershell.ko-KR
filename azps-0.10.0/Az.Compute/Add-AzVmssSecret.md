---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 656BE930-E778-40B0-8A75-BFE52DE386CE
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmsssecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVmssSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVmssSecret.md
ms.openlocfilehash: 2f4f11c66e01160fe757f16fb74cddc952cbd228
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93877119"
---
# Add-AzVmssSecret

## SYNOPSIS
VMSS에 비밀을 추가 합니다.

## 구문과

```
Add-AzVmssSecret [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-SourceVaultId] <String>]
 [[-VaultCertificate] <VaultCertificate[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## 설명은
**AzVmssSecret** Cmdlet은 가상 컴퓨터 크기 조정 집합 (vmss)에 비밀을 추가 합니다.
비밀은 Azure Key Vault에 저장 되어 있어야 합니다.
키 볼트에 대 한 자세한 내용은 [Azure 키 보관소 란?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/) 을 참조 하세요. (https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).
Cmdlet에 대 한 자세한 내용은 [Azure 키 자격 증명 모음 cmdlet](https://msdn.microsoft.com/library/azure/dn868052.aspx) ( https://msdn.microsoft.com/library/azure/dn868052.aspx) Microsoft 개발자 네트워크 라이브러리 또는 [AzureKeyVaultSecret](/powershell/module/azurerm.keyvault/set-azurekeyvaultsecret) cmdlet)을 참조 하세요.

## 예제의

### 예제 1: VMSS에 비밀 추가
```
PS C:\> $Vault = Get-AzKeyVault -VaultName "ContosoVault"
PS C:\> $CertConfig = New-AzVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "Certificates"
PS C:\> $VMSS = New-AzVmssConfig
PS C:\> Add-AzVmssSecret -VirtualMachineScaleSet $VMSS -SourceVaultId $Vault.ResourceId -VaultCertificate $CertConfig
```

이 예제에서는 VMSS에 비밀을 추가 합니다.
첫 번째 명령은 Get-AzKeyVault cmdlet을 사용 하 여 ContosoVault 이라는 자격 증명 모음에서 자격 증명 모음 비밀을 가져오고 그 결과를 $Vault 이라는 변수에 저장 합니다.
두 번째 명령은 **AzVmssVaultCertificateConfig** cmdlet을 사용 하 여 인증서 저장소에서 지정 된 인증서 URL을 사용 하 여 키 보관소 인증서 구성을 만든 다음 해당 결과를 $CertConfig 라는 변수에 저장 합니다.
세 번째 명령은 **AzVmssConfig** cmdlet을 사용 하 여 vmss 구성 개체를 만들고 결과를 $VMSS 이라는 변수에 저장 합니다.
네 번째 명령은 $Vault 및 $CertConfig 변수에 저장 된 키 리소스 ID 및 자격 증명 모음 인증서를 사용 하 여 VMSS에 비밀을 추가 합니다.

## 변수

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

### -SourceVaultId
가상 컴퓨터에 추가할 수 있는 인증서를 포함 하는 키 보관소의 리소스 ID를 지정 합니다.
이 값은 또한 여러 인증서를 추가 하는 키 역할을 합니다.
즉, 동일한 키 보관소에서 여러 개의 인증서를 추가 하는 경우 *SourceVaultId* 매개 변수에 대해 동일한 값을 사용할 수 있습니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VaultCertificate
인증서 URL 및 인증서 이름을 포함 하는 자격 증명 모음 **인증서** 개체를 지정 합니다.
[새 AzVmssVaultCertificateConfig](./New-AzVmssVaultCertificateConfig.md) cmdlet을 사용 하 여이 개체를 만들 수 있습니다.

```yaml
Type: VaultCertificate[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualMachineScaleSet
VMSS 개체를 지정 합니다.
[새 AzVmssConfig](./New-AzVmssConfig.md) cmdlet을 사용 하 여이 개체를 만들 수 있습니다.

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -확인
Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet이 실행 되는 경우의 동작을 보여 줍니다. Cmdlet이 실행 되지 않습니다.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### VirtualMachineScaleSet
' VirtualMachineScaleSet ' 매개 변수는 파이프라인에서 ' VirtualMachineScaleSet ' 형식의 값을 허용 합니다.

## 출력

### 않아야
이 cmdlet은 출력을 생성 하지 않습니다.

## 상속자

## 관련 링크

[새로운 AzVmssVaultCertificateConfig](./New-AzVmssVaultCertificateConfig.md)

[새로운 AzVmssConfig](./New-AzVmssConfig.md)
