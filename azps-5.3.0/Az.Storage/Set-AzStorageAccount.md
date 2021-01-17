---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 4D7EEDD7-89D4-4B1E-A9A1-B301E759CE72
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageAccount.md
ms.openlocfilehash: 0b5e34fe3d7fe4c680ac20da53a32e1e5bad36fa
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491259"
---
# Set-AzStorageAccount

## SYNOPSIS
Storage 계정을 수정합니다.

## 구문

### StorageEncryption(기본값)
```
Set-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-SkuName <String>]
 [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>] [-Tag <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-StorageEncryption] [-AssignIdentity]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-UpgradeToStorageV2]
 [-EnableAzureActiveDirectoryDomainServicesForFile <Boolean>] [-EnableLargeFileShare]
 [-AllowBlobPublicAccess <Boolean>] [-MinimumTlsVersion <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### KeyvaultEncryption
```
Set-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-SkuName <String>]
 [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>] [-Tag <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-KeyvaultEncryption] -KeyName <String> [-KeyVersion <String>]
 -KeyVaultUri <String> [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>] [-UpgradeToStorageV2]
 [-EnableAzureActiveDirectoryDomainServicesForFile <Boolean>] [-EnableLargeFileShare]
 [-AllowBlobPublicAccess <Boolean>] [-MinimumTlsVersion <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ActiveDirectoryDomainServicesForFile
```
Set-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-SkuName <String>]
 [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>] [-Tag <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-UpgradeToStorageV2] [-EnableLargeFileShare] -EnableActiveDirectoryDomainServicesForFile <Boolean>
 [-ActiveDirectoryDomainName <String>] [-ActiveDirectoryNetBiosDomainName <String>]
 [-ActiveDirectoryForestName <String>] [-ActiveDirectoryDomainGuid <String>]
 [-ActiveDirectoryDomainSid <String>] [-ActiveDirectoryAzureStorageSid <String>]
 [-AllowBlobPublicAccess <Boolean>] [-MinimumTlsVersion <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명
**Set-AzStorageAccount** cmdlet은 Azure Storage 계정을 수정합니다.
이 cmdlet을 사용하여 계정 유형을 수정하거나, 고객 도메인을 업데이트하거나, Storage 계정에 태그를 설정할 수 있습니다.

## 예제

### 예제 1: Storage 계정 유형 설정
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Type "Standard_RAGRS"
```

이 명령은 Storage 계정 유형을 저장소 계정 유형으로 Standard_RAGRS.

### 예제 2: Storage 계정에 대한 사용자 지정 도메인 설정
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -CustomDomainName "www.contoso.com" -UseSubDomain $True
```

이 명령은 Storage 계정에 대한 사용자 지정 도메인을 설정합니다.

### 예제 3: 액세스 계층 값 설정
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -AccessTier Cool
```

이 명령은 액세스 계층 값을 쿨로 설정합니다.

### 예제 4: 사용자 지정 도메인 및 태그 설정
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -CustomDomainName "www.domainname.com" -UseSubDomain $true -Tag @{tag0="value0";tag1="value1";tag2="value2"}
```

이 명령은 Storage 계정에 대한 사용자 지정 도메인 및 태그를 설정합니다.

### 예제 5: 암호화 KeySource를 Keyvault로 설정
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -AssignIdentity
PS C:\>$account = Get-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount"

PS C:\>$keyVault = New-AzKeyVault -VaultName "MyKeyVault" -ResourceGroupName "MyResourceGroup" -Location "EastUS2"
PS C:\>$key = Add-AzKeyVaultKey -VaultName "MyKeyVault" -Name "MyKey" -Destination 'Software'
PS C:\>Set-AzKeyVaultAccessPolicy -VaultName "MyKeyVault" -ObjectId $account.Identity.PrincipalId -PermissionsToKeys wrapkey,unwrapkey,get

PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -KeyvaultEncryption -KeyName $key.Name -KeyVersion $key.Version -KeyVaultUri $keyVault.VaultUri
```

이 명령은 새로 만든 Keyvault로 암호화 KeySource를 설정합니다.

### 예제 6: 암호화 KeySource를 "Microsoft.Storage"로 설정
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -StorageEncryption
```

이 명령은 암호화 KeySource를 "Microsoft.Storage"로 설정

### 예제 7: JSON을 통해 Storage 계정의 NetworkRuleSet 속성 설정
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -NetworkRuleSet (@{bypass="Logging,Metrics";
    ipRules=(@{IPAddressOrRange="20.11.0.0/16";Action="allow"},
            @{IPAddressOrRange="10.0.0.0/7";Action="allow"});
    virtualNetworkRules=(@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},
                        @{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2";Action="allow"});
    defaultAction="allow"})
```

이 명령은 JSON을 사용하여 Storage 계정의 NetworkRuleSet 속성을 설정

### 예제 8: Storage 계정에서 NetworkRuleSet 속성을 액세스하고 다른 Storage 계정으로 설정
```
PS C:\> $networkRuleSet = (Get-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount").NetworkRuleSet 
PS C:\> Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount2" -NetworkRuleSet $networkRuleSet
```

이 첫 번째 명령은 Storage 계정에서 NetworkRuleSet 속성을, 두 번째 명령은 다른 Storage 계정으로 설정 

### 예제 9: 종류가 "Storage" 또는 "BlobStorage"인 Storage 계정을 "StorageV2" 종류의 Storage 계정으로 업그레이드
```
PS C:\> Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -UpgradeToStorageV2
```

이 명령은 종류가 "Storage" 또는 "BlobStorage"인 Storage 계정을 "StorageV2" 종류의 Storage 계정으로 업그레이드합니다.

### 예제 10: Azure Files AAD DS 인증을 사용하도록 설정하여 Storage 계정을 업데이트합니다.
```
PS C:\> $account = Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -EnableAzureActiveDirectoryDomainServicesForFile $true PS

PS C:\> $account.AzureFilesIdentityBasedAuth.DirectoryServiceOptions
AADDS
```

이 명령은 Azure Files AAD DS 인증을 사용하도록 설정하여 Storage 계정을 업데이트합니다.

### 예제 11: Files Active Directory Domain Service 인증을 사용하도록 설정하여 Storage 계정을 업데이트한 다음 파일 ID 기반 인증 설정을 표시
```
PS C:\> $account = Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -EnableActiveDirectoryDomainServicesForFile $true `
        -ActiveDirectoryDomainName "mydomain.com" `
        -ActiveDirectoryNetBiosDomainName "mydomain.com" `
        -ActiveDirectoryForestName "mydomain.com" `
        -ActiveDirectoryDomainGuid "12345678-1234-1234-1234-123456789012" `
        -ActiveDirectoryDomainSid "S-1-5-21-1234567890-1234567890-1234567890" `
        -ActiveDirectoryAzureStorageSid "S-1-5-21-1234567890-1234567890-1234567890-1234"
        
PS C:\> $account.AzureFilesIdentityBasedAuth.DirectoryServiceOptions
AD

PS C:\> $account.AzureFilesIdentityBasedAuth.ActiveDirectoryProperties

DomainName        : mydomain.com
NetBiosDomainName : mydomain.com
ForestName        : mydomain.com
DomainGuid        : 12345678-1234-1234-1234-123456789012
DomainSid         : S-1-5-21-1234567890-1234567890-1234567890
AzureStorageSid   : S-1-5-21-1234567890-1234567890-1234567890-1234
```

이 명령은 Azure Files Active Directory 도메인 서비스 인증을 사용하도록 설정하여 Storage 계정을 업데이트한 다음 파일 ID 기반 인증 설정을 보여줍니다.

### 예제 12: MinimumTlsVersion 및 AllowBlobPublicAccess 설정
```
PS C:\> $account = Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -MinimumTlsVersion TLS1_1 -AllowBlobPublicAccess $false

PS C:\> $account.MinimumTlsVersion
TLS1_1

PS C:\> $account.AllowBlobPublicAccess
False
```

이 명령은 MinimumTlsVersion 및 AllowBlobPublicAccess를 설정한 다음 계정의 2개 속성을 보여 주며, 

## PARAMETERS

### -AccessTier
이 cmdlet이 수정하는 Storage 계정의 액세스 계층을 지정합니다.
이 매개 변수에 허용되는 값은 핫 및 쿨입니다.
액세스 계층을 변경하면 추가 요금이 부과될 수 있습니다. 자세한 내용은 Azure Blob Storage: 핫 및 쿨 [스토리지 계층을 참조하세요.](http://go.microsoft.com/fwlink/?LinkId=786482)
Storage 계정에 Kind as StorageV2 또는 BlobStorage가 있는 경우 *AccessTier* 매개 변수를 지정할 수 있습니다. Storage 계정에 Kind as Storage가 있는 경우 *AccessTier* 매개 변수를 지정하지 않습니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Hot, Cool

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ActiveDirectoryAzureStorageSid
Azure Storage에 대한 SID(보안 식별자)를 지정합니다. -EnableActiveDirectoryDomainServicesForFile이 true로 설정된 경우 이 매개 변수를 설정해야 합니다.

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ActiveDirectoryDomainGuid
도메인 GUID를 지정합니다. -EnableActiveDirectoryDomainServicesForFile이 true로 설정된 경우 이 매개 변수를 설정해야 합니다.

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ActiveDirectoryDomainName
AD DNS 서버가 권한이 있는 주 도메인을 지정합니다. -EnableActiveDirectoryDomainServicesForFile이 true로 설정된 경우 이 매개 변수를 설정해야 합니다.

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ActiveDirectoryDomainSid
SID(보안 식별자)를 지정합니다. -EnableActiveDirectoryDomainServicesForFile이 true로 설정된 경우 이 매개 변수를 설정해야 합니다.

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ActiveDirectoryForestName
얻을 Active Directory 포리스트를 지정합니다. -EnableActiveDirectoryDomainServicesForFile이 true로 설정된 경우 이 매개 변수를 설정해야 합니다.

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ActiveDirectoryNetBiosDomainName
NetBIOS 도메인 이름을 지정합니다. -EnableActiveDirectoryDomainServicesForFile이 true로 설정된 경우 이 매개 변수를 설정해야 합니다.

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AllowBlobPublicAccess
저장소 계정의 모든 Blob 또는 컨테이너에 대한 공용 액세스를 허용하거나 허용하지 않습니다.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AsJob
백그라운드에서 cmdlet 실행

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

### -AssignIdentity
Azure KeyVault와 같은 키 관리 서비스에서 사용할 새 Storage 계정 ID를 생성하고 이 Storage 계정에 할당합니다.

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

### -CustomDomainName
사용자 지정 도메인의 이름을 지정합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

### -EnableActiveDirectoryDomainServicesForFile
저장소 계정에 대해 Azure Files Active Directory Domain Service 인증을 사용하도록 설정할 수 있습니다.

```yaml
Type: System.Boolean
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableAzureActiveDirectoryDomainServicesForFile
저장소 계정에 대해 Azure Files Active Directory Domain Service 인증을 사용하도록 설정할 수 있습니다.

```yaml
Type: System.Boolean
Parameter Sets: StorageEncryption, KeyvaultEncryption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableHttpsTrafficOnly
Storage 계정이 HTTPS 트래픽만 사용할 수 있는지 여부를 나타냅니다.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableLargeFileShare
저장소 계정이 용량이 5 TiB 이상인 대용량 파일 공유를 지원할 수 있는지 여부를 나타냅니다. 계정이 활성화되면 기능을 사용하지 않도록 설정할 수 없습니다. 현재 LRS 및 ZRS 복제 유형에서만 지원됩니다. 따라서 계정은 지역 중복 계정으로 변환할 수 없습니다. 자세한 내용은 https://go.microsoft.com/fwlink/?linkid=2086047

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

### -Force
변경을 저장소 계정에 강제로 기록합니다.

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

### -KeyName
-KeyvaultEncryption을 사용하여 Key Vault에서 암호화를 사용하도록 설정하는 경우 이 옵션을 사용하여 Keyname 속성을 지정합니다.

```yaml
Type: System.String
Parameter Sets: KeyvaultEncryption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyvaultEncryption
Storage 서비스 암호화를 사용할 때 암호화 키에 Microsoft KeyVault를 사용할지 여부를 나타냅니다. KeyName, KeyVersion 및 KeyVaultUri가 모두 설정된 경우 KeySource는 이 매개 변수가 설정되어 있는지 여부에 따라 Microsoft.Keyvault로 설정됩니다. 

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: KeyvaultEncryption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyVaultUri
-KeyvaultEncryption 매개 변수를 지정하여 Key Vault 암호화를 사용하는 경우 이 옵션을 사용하여 Key Vault에 대한 URI를 지정합니다.

```yaml
Type: System.String
Parameter Sets: KeyvaultEncryption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyVersion
-KeyvaultEncryption 매개 변수를 지정하여 Key Vault 암호화를 사용하는 경우 이 옵션을 사용하여 키 버전에 대한 URI를 지정합니다.

```yaml
Type: System.String
Parameter Sets: KeyvaultEncryption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MinimumTlsVersion
저장소에 대한 요청에 허용되는 최소 TLS 버전입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: TLS1_0, TLS1_1, TLS1_2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
수정할 Storage 계정의 이름을 지정합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NetworkRuleSet
NetworkRuleSet은 방화벽 및 가상 네트워크에 대한 구성 규칙 집합을 정의하고, 규칙을 무시할 수 있는 서비스 및 정의된 규칙과 일치하지 않는 요청을 처리하는 방법과 같은 네트워크 속성에 대한 값을 설정하는 데 사용됩니다.

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Storage 계정을 수정할 리소스 그룹의 이름을 지정합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SkuName
Storage 계정의 SKU 이름을 지정합니다.
이 매개 변수에 허용되는 값은
- Standard_LRS - 로컬 중복 저장소입니다.
- Standard_ZRS - 영역 중복 저장소입니다.
- Standard_GRS - 지역 중복 저장소입니다.
- Standard_RAGRS - 읽기 액세스 지역 중복 저장소
- Premium_LRS - 프리미엄 로컬 중복 저장소.
- Standard_GZRS - 지역 중복 영역 중복 저장소입니다.
- Standard_RAGZRS - 읽기 액세스 지역 중복 영역 중복 저장소.
다른 계정 유형으로 Standard_ZRS Premium_LRS 변경할 수 없습니다.
다른 계정 유형을 다른 계정 유형으로 변경하거나 Standard_ZRS 변경할 Premium_LRS.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountType, AccountType, Type
Accepted values: Standard_LRS, Standard_ZRS, Standard_GRS, Standard_RAGRS, Premium_LRS, Standard_GZRS, Standard_RAGZRS

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageEncryption
Microsoft 관리 키를 사용하기 위해 Storage 계정 암호화를 설정할지 여부를 나타냅니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: StorageEncryption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tag
서버의 태그로 설정된 해시 테이블 형식의 키-값 쌍입니다. 예: @{key0="value0";key1=$null;key2="value2"}

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -UpgradeToStorageV2
Storage 계정 종류를 Storage 또는 BlobStorage에서 StorageV2로 업그레이드합니다.

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

### -UseSubDomain
간접 CName 유효성 검사를 사용할지 여부를 나타냅니다.

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
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
Default value: False
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.

## 입력

### System.String

### System.Collections.Hashtable

## 출력

### Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount

## 참고 사항

## 관련 링크

[Get-AzStorageAccount](./Get-AzStorageAccount.md)

[New-AzStorageAccount](./New-AzStorageAccount.md)

[Remove-AzStorageAccount](./Remove-AzStorageAccount.md)
