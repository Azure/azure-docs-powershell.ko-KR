---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/get-AzKeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 70ee1aaf9fb082819c626c43ba5c08ad01f0f1d6
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876708"
---
# Get-AzKeyVaultManagedStorageAccount

## SYNOPSIS
키 보관소 관리 Azure 저장소 계정을 가져옵니다.

## 구문과

### ByVaultName (기본값)
```
Get-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ByAccountName
```
Get-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
계정 이름이 지정 되 고 계정 키가 지정 된 자격 증명 모음에 의해 관리 되는 경우 키 보관소 관리 Azure 저장소 계정을 가져옵니다. 계정 이름을 지정 하지 않으면 해당 키가 지정 된 자격 증명 모음에 의해 관리 되는 모든 계정이 나열 됩니다.

## 예제의

### 예제 1: 모든 키 보관소 관리 저장소 계정 나열
```
PS C:\> Get-AzKeyVaultManagedStorageAccount -VaultName 'myvault'
```

' Myvault ' 자격 증명 모음으로 해당 키를 관리 하는 모든 계정이 나열 됩니다.

### 예제 2: 키 보관소 관리 저장소 계정 가져오기
```
PS C:\> Get-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -Name 'mystorageaccount'
```

' Mystorageaccount ' 키 저장소 계정이 자격 증명 모음 ' myvault '에 의해 관리 되는 경우 해당 키 자격 증명 모음 관리의 세부 정보를 가져옵니다.

## 변수

### -AccountName
키 자격 증명 모음 관리 저장소 계정 이름입니다. Cmdlet은 자격 증명 모음 이름, 현재 선택한 환경 및 manged 저장소 계정 이름에서 관리 되는 저장소 계정 이름의 FQDN을 생성 합니다.

```yaml
Type: String
Parameter Sets: ByAccountName
Aliases: StorageAccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### -VaultName
자격 증명 모음 이름
Cmdlet은 이름 및 현재 선택 된 환경을 기준으로 자격 증명 모음의 FQDN을 생성 합니다.

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

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### System. 문자열

## 출력

### System.webserver. List ' 1 [[Microsoft Azure.]. t e m '을 (를) ' ' [2.5.0.0 Storageaccount. '. KeyVault, Version =, Culture = 중립적인, PublicKeyToken = null]]
Microsoft. KeyVault. * ManagedStorageAccount

## 상속자

## 관련 링크

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

