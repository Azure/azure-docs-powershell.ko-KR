---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultmanagedstoragesasdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultManagedStorageSasDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultManagedStorageSasDefinition.md
ms.openlocfilehash: ff73d5db0b16d7176b9c49aa6e70bc13fc9f3fba
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185484"
---
# Set-AzKeyVaultManagedStorageSasDefinition

## SYNOPSIS
주어진 Key Vault 관리 Azure Storage 계정에 대한 Key Vault를 사용하여 SAS(공유 액세스 서명) 정의를 설정합니다.

## 구문

### 기본값(기본값)
```
Set-AzKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-TemplateUri] <String> [-SasType] <String> [-Disable] [-Tag <Hashtable>] -ValidityPeriod <TimeSpan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByInputObject
```
Set-AzKeyVaultManagedStorageSasDefinition [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [-Name] <String> [-TemplateUri] <String> [-SasType] <String> [-Disable] [-Tag <Hashtable>]
 -ValidityPeriod <TimeSpan> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## 설명
주어진 Key Vault 관리 Azure Storage 계정으로 SAS(공유 액세스 서명) 정의를 설정합니다. 또한 이 SAS 정의에 따라 SAS 토큰을 사용하는 데 사용할 수 있는 비밀을 설정합니다.
SAS 토큰은 이러한 매개 변수 및 Key Vault 관리 Azure Storage 계정의 활성 키를 사용하여 생성됩니다.

## 예제

### 예제 1: 계정 유형 SAS 정의를 설정하고 이를 기반으로 현재 SAS 토큰을 얻습니다.
```powershell
PS C:\> $sa = Get-AzStorageAccount -Name mysa -ResourceGroupName myrg
PS C:\> $kv = Get-AzKeyVault -VaultName mykv
PS C:\> Add-AzKeyVaultManagedStorageAccount -VaultName $kv.VaultName -AccountName $sa.StorageAccountName -AccountResourceId $sa.Id -ActiveKeyName key1 -RegenerationPeriod ([System.Timespan]::FromDays(180))
PS C:\> $sctx = New-AzStorageContext -StorageAccountName $sa.StorageAccountName -Protocol Https -StorageAccountKey Key1
PS C:\> $start = [System.DateTime]::Now.AddDays(-1)
PS C:\> $end = [System.DateTime]::Now.AddMonths(1)
PS C:\> $at = New-AzStorageAccountSasToken -Service blob,file,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup" -Protocol HttpsOnly -StartTime $start -ExpiryTime $end -Context $sctx
PS C:\> $sas = Set-AzKeyVaultManagedStorageSasDefinition -AccountName $sa.StorageAccountName -VaultName $kv.VaultName -Name accountsas -TemplateUri $at -SasType 'account' -ValidityPeriod ([System.Timespan]::FromDays(30))
PS C:\> Get-AzKeyVaultSecret -VaultName $kv.VaultName -Name $sas.Sid.Substring($sas.Sid.LastIndexOf('/')+1)
```

자격 증명 모음 'mykv'의 KeyVault 관리 저장소 계정 'mysa'에서 계정 SAS 정의 'accountsas'를 설정합니다. 특히 위의 시퀀스는 다음을 실행합니다.
  - (기존) 저장소 계정을 얻습니다.
  - (기존) 키 자격 증명 모음을 얻습니다.
  - KeyVault 관리 저장소 계정을 자격 증명 모음에 추가하고 Key1을 활성 키로 설정하고 다시 재생성 기간은 180일입니다.
  - Key1을 통해 지정된 저장소 계정에 대한 저장소 컨텍스트를 설정
  - 서비스, 컨테이너 및 개체에 대한 서비스 Blob, 파일, 테이블 및 큐에 대한 계정 SAS 토큰을 만들고 https를 통해, 지정된 시작 및 종료 날짜를 사용하여 모든 권한을 사용하여 서비스, 컨테이너 및 개체에 대한 계정 SAS 토큰을 만듭니다.
  - 자격 증명 모음에서 KeyVault 관리 저장소 SAS 정의를 설정하고 템플릿 URI를 위에서 만든 SAS 토큰으로 설정하고 SAS 형식 '계정'으로 설정하고 30일 동안 유효합니다.
  - SAS 정의에 해당하는 KeyVault 비밀에서 실제 액세스 토큰을 검색합니다.

## PARAMETERS

### -AccountName
Key Vault 관리 저장소 계정 이름입니다. Cmdlet은 자격 증명 모음 이름, 현재 선택한 환경 및 관리되는 저장소 계정 이름에서 관리되는 저장소 계정 이름의 FQDN을 생성합니다.

```yaml
Type: System.String
Parameter Sets: Default
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독

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

### -Disable
sas 토큰 생성에 sas 정의 사용을 비활성화합니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
ManagedStorageAccount 개체입니다.

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
저장소 sas 정의 이름입니다. Cmdlet은 자격 증명 모음 이름, 현재 선택한 환경, 저장소 계정 이름 및 sas 정의 이름에서 저장소 sas 정의의 FQDN을 생성합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SasDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SasType
저장소 SAS 유형입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tag
해시 테이블 형식의 키-값 쌍입니다. 예: @{key0="value0";key1=$null;key2="value2"}

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TemplateUri
저장소 SAS 정의 템플릿 URI입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ValidityPeriod
생성되는 시간부터 sas 토큰의 만료 시간을 설정하는 데 사용되는 유효 기간입니다.

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VaultName
자격 증명 모음 이름입니다.
Cmdlet은 이름 및 현재 선택한 환경을 기반으로 자격 증명 모음의 FQDN을 생성합니다.

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
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
cmdlet이 실행되지 않습니다.

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

### Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem

## 출력

### Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinition

## 참고 사항

## 관련 링크

[Azureâ€'RM.â€'€Keyâ€€Vault](/powershell/module/az.keyvault/)
