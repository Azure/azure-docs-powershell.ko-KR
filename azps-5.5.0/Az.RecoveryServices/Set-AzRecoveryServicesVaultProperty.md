---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesvaultproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultProperty.md
ms.openlocfilehash: e6bd0284d9ce5b5cb6973fce6aae5e16a4c06883
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191289"
---
# Set-AzRecoveryServicesVaultProperty

## SYNOPSIS
자격 증명 모음의 속성을 업데이트합니다.

## 구문

### AzureRSVaultSoftDelteParameterSet(기본값)
```
Set-AzRecoveryServicesVaultProperty -SoftDeleteFeatureState <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AzureRSVaultCMKParameterSet
```
Set-AzRecoveryServicesVaultProperty -EncryptionKeyId <string> -KeyVaultSubscriptionId <string> [-InfrastructureEncryption] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명
**Set-AzRecoveryServicesVaultProperty** cmdlet은 Recovery Services 자격 증명 모음의 속성을 업데이트합니다. 이 cmdlet은 두 개의 다른 매개 변수 집합이 있는 자격 증명 모음에 대해 소프트 삭제를 사용/사용하지 않도록 설정하거나 CMK 암호화를 설정하는 데 사용할 수 있습니다. 
자격 증명 모음에 등록된 컨테이너가 없는 경우 자격 증명 모음의 **SoftDeleteFeatureState** 속성을 사용하지 않도록 설정할 수 있습니다. InfrastructurEncryption은 사용자가 CMK 자격 증명 모음을 처음 업데이트할 때만 설정할 수 있습니다.

## 예제

### 예제 1: 자격 증명 모음의 SoftDeleteFeatureState 업데이트
```
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName" -Name "vaultName"
PS C:\> $props = Set-AzRecoveryServicesVaultProperty -VaultId $vault.Id -SoftDeleteFeatureState Enable
```

첫 번째 명령은 자격 증명 모음 개체를 인용한 다음, 자격 증명 모음 $vault 저장합니다.
두 번째 명령은 자격 증명 모음의 SoftDeleteFeatureState 속성을 "Enabled" 상태로 업데이트합니다.

### 예제 2: 자격 증명 모음의 CMK 암호화 업데이트

```
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName" -Name "vaultName"
PS C:\> $keyVault = Get-AzKeyVault -VaultName "keyVaultName" -ResourceGroupName "RGName" 
PS C:\> $key = Get-AzKeyVaultKey -VaultName "keyVaultName" -Name "keyName" 
PS C:\> Set-AzRecoveryServicesVaultProperty -EncryptionKeyId $key.ID -KeyVaultSubscriptionId "f870818k-5h28-4t48-8961-37458592348r" -InfrastructureEncryption -VaultId $vault.ID
```

첫 번째 cmdlet은 암호화 속성을 업데이트하는 RSVault를 얻습니다. 두 번째 cmdlet은 Azure Key Vault를 얻습니다. 세 번째 cmdlet은 키 자격 증명 모음에서 키를 얻습니다.
네 번째 cmdlet은 RSVault 내에서 고객 관리 암호화 키를 업데이트합니다. -InfrastructureEncryption param을 사용하여 처음으로 업데이트할 때 인프라 암호화를 사용하도록 설정할 수 있습니다. 

## PARAMETERS

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

### -SoftDeleteFeatureState
Recovery Services 자격 증명 모음의 SoftDeleteFeatureState입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enable, Disable

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EncryptionKeyId
CMK에 사용할 암호화 키의 KeyId입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: KeyID

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyVaultSubscriptionId
Key Vault의 구독 ID입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: SubscriptionID

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InfrastructureEncryption
이 자격 증명 모음에서 인프라 암호화를 사용합니다. 암호화를 구성할 때 인프라 암호화를 사용하도록 설정해야 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VaultId
ARM 자격 증명 모음의 ID입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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
cmdlet이 실행되는 경우의 결과 표시

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

### System.String

### Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.VaultSoftDeleteFeatureState

## 출력

### Microsoft.Azure.Management.RecoveryServices.Backup.Models.BackupResourceVaultConfigResource

## 참고 사항

## 관련 링크

[Get-AzRecoveryServicesVault](./Get-AzRecoveryServicesVault.md)

[Get-AzRecoveryServicesVaultProperty](./Get-AzRecoveryServicesVaultProperty.md)
