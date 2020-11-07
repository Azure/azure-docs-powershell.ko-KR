---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: C4E7ACDF-22FB-4D49-93B3-69E787B7E0CD
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/restore-AzKeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Restore-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Restore-AzKeyVaultKey.md
ms.openlocfilehash: 5d090bae05e3d931fbf41b656ea66409d1297e8f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876704"
---
# Restore-AzKeyVaultKey

## SYNOPSIS
백업 키의 키 보관소에 키를 만듭니다.

## 구문과

```
Restore-AzKeyVaultKey [-VaultName] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명은
**Restore-AzKeyVaultKey** cmdlet은 지정 된 키 보관소에 키를 만듭니다.
이 키는 입력 파일의 백업 키 복제본 이며 원래 키와 같은 이름을 갖습니다.
키 보관소에 같은 이름의 키가 이미 있는 경우, 원본 키를 덮어쓰지 않고이 cmdlet이 실패 합니다.
백업에 여러 버전의 키가 포함 되어 있으면 모든 버전이 복원 됩니다.

키를 복원 하는 키 보관소는 해당 키를 백업한 키 보관소와 다를 수 있습니다.
그러나 키 자격 증명 모음이 동일한 구독을 사용 해야 하며 같은 지리 (예: 북미)의 Azure 지역에 있어야 합니다.
https://azure.microsoft.com/support/trust-center/)Azure 지역을 지역에 매핑하는 Microsoft Azure 보안 센터를 참조 하세요.

## 예제의

### 예제 1: 백업 된 키 복원
```
PS C:\>Restore-AzKeyVaultKey -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"
```

이 명령은 모든 버전을 포함 한 키를 Backup. a y y (백업 파일 이름)에서 MyKeyVault 라는 키 자격 증명 모음으로 복원 합니다.

## 변수

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputFile
복원할 키의 백업을 포함 하는 입력 파일을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VaultName
키를 복원할 키 보관소의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.
Cmdlet이 실행 되지 않습니다.

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

### 않아야
이 cmdlet은 입력을 허용 하지 않습니다.

## 출력

### Microsoft. KeyVault. Keyvault

## 상속자

## 관련 링크

[추가-AzKeyVaultKey](./Add-AzKeyVaultKey.md)

[백업-AzKeyVaultKey](./Backup-AzKeyVaultKey.md)

[Get-AzKeyVaultKey](./Get-AzKeyVaultKey.md)

[제거-AzKeyVaultKey](./Remove-AzKeyVaultKey.md)

