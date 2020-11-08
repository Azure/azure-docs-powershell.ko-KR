---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 4D7EEDD7-89D4-4B1E-A9A1-B301E759CE72
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageAccount.md
ms.openlocfilehash: 0b5e34fe3d7fe4c680ac20da53a32e1e5bad36fa
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204716"
---
# Set-AzStorageAccount

## SYNOPSIS
저장소 계정을 수정 합니다.

## 구문과

### StorageEncryption (기본값)
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

## 설명은
**AzStorageAccount** Cmdlet은 Azure 저장소 계정을 수정 합니다.
이 cmdlet을 사용 하 여 계정 유형을 수정 하거나, 고객 도메인을 업데이트 하거나, 저장소 계정에서 태그를 설정할 수 있습니다.

## 예제의

### 예제 1: 저장소 계정 유형 설정
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Type "Standard_RAGRS"
```

이 명령은 저장소 계정 유형을 Standard_RAGRS 설정 합니다.

### 예제 2: 저장소 계정의 사용자 지정 도메인 설정
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -CustomDomainName "www.contoso.com" -UseSubDomain $True
```

이 명령은 저장소 계정에 대 한 사용자 지정 도메인을 설정 합니다.

### 예제 3: 액세스 계층 값 설정
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -AccessTier Cool
```

명령에서 액세스 계층 값이 멋진 것으로 설정 됩니다.

### 예제 4: 사용자 지정 도메인 및 태그 설정
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -CustomDomainName "www.domainname.com" -UseSubDomain $true -Tag @{tag0="value0";tag1="value1";tag2="value2"}
```

이 명령은 저장소 계정의 사용자 지정 도메인 및 태그를 설정 합니다.

### 예제 5: 암호화 KeySource를 Keysource로 설정
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -AssignIdentity
PS C:\>$account = Get-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount"

PS C:\>$keyVault = New-AzKeyVault -VaultName "MyKeyVault" -ResourceGroupName "MyResourceGroup" -Location "EastUS2"
PS C:\>$key = Add-AzKeyVaultKey -VaultName "MyKeyVault" -Name "MyKey" -Destination 'Software'
PS C:\>Set-AzKeyVaultAccessPolicy -VaultName "MyKeyVault" -ObjectId $account.Identity.PrincipalId -PermissionsToKeys wrapkey,unwrapkey,get

PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -KeyvaultEncryption -KeyName $key.Name -KeyVersion $key.Version -KeyVaultUri $keyVault.VaultUri
```

이 명령은 새로 만든 Keysource를 사용 하 여 암호화 KeySource를 설정 합니다.

### 예제 6: 암호화 KeySource를 "Microsoft. 저장소"로 설정
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -StorageEncryption
```

이 명령은 암호화 KeySource를 "Microsoft. 저장소"로 설정 합니다.

### 예제 7: JSON을 사용 하 여 저장소 계정의 NetworkRuleSet 규칙 집합 속성 설정
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -NetworkRuleSet (@{bypass="Logging,Metrics";
    ipRules=(@{IPAddressOrRange="20.11.0.0/16";Action="allow"},
            @{IPAddressOrRange="10.0.0.0/7";Action="allow"});
    virtualNetworkRules=(@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},
                        @{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2";Action="allow"});
    defaultAction="allow"})
```

이 명령은 JSON으로 저장소 계정의 네트워크 규칙 집합 속성을 설정 합니다.

### 예제 8: 저장소 계정에서 NetworkRuleSet 속성 가져오기 및 다른 저장소 계정으로 설정
```
PS C:\> $networkRuleSet = (Get-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount").NetworkRuleSet 
PS C:\> Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount2" -NetworkRuleSet $networkRuleSet
```

첫 번째 명령은 저장소 계정에서 NetworkRuleSet 집합 속성을 가져오며, 두 번째 명령은 다른 저장소 계정으로 설정 합니다. 

### 예제 9: 유형 "저장소" 또는 "BlobStorage"를 "StorageV2" kind 저장소 계정으로 사용 하 여 저장소 계정 업그레이드
```
PS C:\> Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -UpgradeToStorageV2
```

"저장소" 또는 "BlobStorage" 종류가 "StorageV2" kind 저장소 계정으로 저장 된 저장소 계정을 명령으로 업그레이드 합니다.

### 예제 10: Azure Files AAD DS 인증을 사용 하도록 설정 하 여 저장소 계정을 업데이트 합니다.
```
PS C:\> $account = Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -EnableAzureActiveDirectoryDomainServicesForFile $true PS

PS C:\> $account.AzureFilesIdentityBasedAuth.DirectoryServiceOptions
AADDS
```

명령에서 Azure Files AAD DS 인증을 사용 하 여 저장소 계정을 업데이트 합니다.

### 예제 11: 파일 Active Directory 도메인 서비스 인증을 사용 하도록 설정 하 여 저장소 계정을 업데이트 한 다음 파일 Id 기반 인증 설정을 표시 합니다.
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

명령이 Azure Files Active Directory 도메인 서비스 인증을 사용 하도록 설정 하 여 저장소 계정을 업데이트 한 다음 파일 Id 기반 인증 설정을 표시 합니다.

### 예제 12: 이상 버전 및 AllowBlobPublicAccess 설정
```
PS C:\> $account = Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -MinimumTlsVersion TLS1_1 -AllowBlobPublicAccess $false

PS C:\> $account.MinimumTlsVersion
TLS1_1

PS C:\> $account.AllowBlobPublicAccess
False
```

이 명령은 고가을 설정 합니다. \ 및 AllowBlobPublicAccess를 설정한 다음 계정의 2 가지 속성을 표시 합니다. 

## 변수

### -AccessTier
이 cmdlet이 수정 하는 저장소 계정의 액세스 계층을 지정 합니다.
이 매개 변수에 허용 되는 값은 Hot 및 멋지게입니다.
액세스 계층을 변경 하면 추가 요금이 발생할 수 있습니다. 자세한 내용은 [Azure Blob Storage: 핫 및 유용한 저장소 계층](http://go.microsoft.com/fwlink/?LinkId=786482)을 참조 하세요.
저장소 계정의 종류가 StorageV2 또는 BlobStorage 인 경우 *AccessTier* 매개 변수를 지정할 수 있습니다. 저장소 계정에 저장소 유형이 있는 경우 *AccessTier* 매개 변수를 지정 하지 마세요.

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
Azure Storage에 대 한 SID (보안 식별자)를 지정 합니다. -EnableActiveDirectoryDomainServicesForFile가 true로 설정 된 경우이 매개 변수를 설정 해야 합니다.

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
도메인 GUID를 지정 합니다. -EnableActiveDirectoryDomainServicesForFile가 true로 설정 된 경우이 매개 변수를 설정 해야 합니다.

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
광고 DNS 서버에 대해 권한이 있는 기본 도메인을 지정 합니다. -EnableActiveDirectoryDomainServicesForFile가 true로 설정 된 경우이 매개 변수를 설정 해야 합니다.

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
SID (보안 식별자)를 지정 합니다. -EnableActiveDirectoryDomainServicesForFile가 true로 설정 된 경우이 매개 변수를 설정 해야 합니다.

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
가져올 Active Directory 포리스트를 지정 합니다. -EnableActiveDirectoryDomainServicesForFile가 true로 설정 된 경우이 매개 변수를 설정 해야 합니다.

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
NetBIOS 도메인 이름을 지정 합니다. -EnableActiveDirectoryDomainServicesForFile가 true로 설정 된 경우이 매개 변수를 설정 해야 합니다.

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
저장소 계정의 모든 blob 또는 컨테이너에 대 한 공용 액세스를 허용 하거나 허용 하지 않습니다.

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

### -Id 할당
Azure KeyVault 같은 키 관리 서비스에 사용 하기 위해이 저장소 계정에 대 한 새 저장소 계정 Id를 생성 하 고 할당 합니다.

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
사용자 지정 도메인의 이름을 지정 합니다.

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

### -EnableActiveDirectoryDomainServicesForFile
Azure Files 저장소 계정에 대 한 Active Directory 도메인 서비스 인증을 사용 하도록 설정 합니다.

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
Azure Files 저장소 계정에 대 한 Active Directory 도메인 서비스 인증을 사용 하도록 설정 합니다.

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
저장소 계정이 HTTPS 트래픽만 사용할 수 있는지 여부를 나타냅니다.

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
저장소 계정이 5 개 이상의 TiB 용량으로 큰 파일 공유를 지원할 수 있는지 여부를 나타냅니다. 계정을 사용 하도록 설정한 후에는 해당 기능을 사용 하지 않도록 설정할 수 없습니다. 현재 LRS 및 ZRS 복제 유형에만 지원 되므로 지역 중복 계정으로 계정 변환을 수행할 수 없습니다. 자세한 정보 https://go.microsoft.com/fwlink/?linkid=2086047

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
변경 내용이 저장소 계정에 기록 되도록 합니다.

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
-KeyvaultEncryption를 사용 하 여 키 자격 증명 모음으로 암호화를 사용 하는 경우이 옵션을 사용 하 여 Keyname 속성을 지정 합니다.

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
저장소 서비스 암호화를 사용 하는 경우 암호화 키에 Microsoft KeyVault를 사용할지 여부를 나타냅니다. KeyName, KeyVersion, KeyVaultUri이 모두 설정 된 경우 Keyversion는이 매개 변수 설정 여부에 관계 없이 Microsoft. Keyversion에 설정 됩니다. 

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
-KeyvaultEncryption 매개 변수를 지정 하 여 키 보관소 암호화를 사용 하는 경우이 옵션을 사용 하 여 키 보관소에 대 한 URI를 지정 합니다.

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
-KeyvaultEncryption 매개 변수를 지정 하 여 키 보관소 암호화를 사용 하는 경우이 옵션을 사용 하 여 키 버전에 대 한 URI를 지정 합니다.

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

### -없음 Tls 버전
저장소 요청에 허용 되는 최소 TLS 버전입니다.

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

### -이름
수정할 저장소 계정의 이름을 지정 합니다.

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

### -NetworkRuleSet 집합
NetworkRuleSet는 방화벽과 가상 네트워크에 대 한 구성 규칙 집합을 정의 하 고 규칙을 우회 하도록 허용 된 서비스 같은 네트워크 속성에 대 한 값을 설정 하 고 정의 된 규칙과 일치 하지 않는 요청을 처리 하는 데 사용 됩니다.

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
저장소 계정을 수정할 리소스 그룹의 이름을 지정 합니다.

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

### -서 비 Uname
저장소 계정의 SKU 이름을 지정 합니다.
이 매개 변수에 허용 되는 값은 다음과 같습니다.
- Standard_LRS 로컬 중복 저장소.
- Standard_ZRS 영역 중복 저장소.
- Standard_GRS 지역 중복 저장소.
- Standard_RAGRS-액세스 지리적 중복 저장소를 읽습니다.
- Premium_LRS-Premium 로컬 중복 저장소.
- Standard_GZRS 지역 중복 영역 중복 저장소.
- Standard_RAGZRS-액세스 지리적 중복 영역 중복 저장소를 읽습니다.
Standard_ZRS 및 Premium_LRS 형식을 다른 계정 형식으로 변경할 수 없습니다.
다른 계정 유형은 Standard_ZRS 하거나 Premium_LRS 변경할 수 없습니다.

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
Microsoft 관리 키를 사용 하도록 저장소 계정 암호화를 설정할지 여부를 나타냅니다.

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

### 태그
서버에서 태그로 설정 된 해시 테이블 형태의 키-값 쌍입니다. 예: @ {key0 = "value0"; key1 = $null; key2 = "value2"}

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
저장소 또는 BlobStorage에서 저장소 계정 종류를 StorageV2로 업그레이드 합니다.

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

### -(도메인)
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

### -확인
Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.

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
Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.
Cmdlet이 실행 되지 않습니다.

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
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### System. 문자열

### System.webserver. 컬렉션 테이블

## 출력

### Microsoft. Azure.. i m a. 모델. PSStorageAccount

## 상속자

## 관련 링크

[Get-AzStorageAccount](./Get-AzStorageAccount.md)

[새로운 AzStorageAccount](./New-AzStorageAccount.md)

[제거-AzStorageAccount](./Remove-AzStorageAccount.md)
