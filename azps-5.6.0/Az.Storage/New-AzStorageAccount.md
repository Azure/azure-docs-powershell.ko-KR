---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A3DA1205-B8FB-4B4C-9C40-AD303D038EDF
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
ms.openlocfilehash: 0a5ccfaec396f4dc79c877da38112a5bfa575e09
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993202"
---
# New-AzStorageAccount

## SYNOPSIS
Storage 계정을 만듭니다.

## 구문

### AzureActiveDirectoryDomainServicesForFile(기본값)
```
New-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Location] <String>
 [-Kind <String>] [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>]
 [-Tag <Hashtable>] [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-EnableHierarchicalNamespace <Boolean>] [-EnableAzureActiveDirectoryDomainServicesForFile <Boolean>]
 [-EnableLargeFileShare] [-PublishMicrosoftEndpoint <Boolean>] [-PublishInternetEndpoint <Boolean>] [-AsJob]
 [-EncryptionKeyTypeForTable <String>] [-EncryptionKeyTypeForQueue <String>] [-RequireInfrastructureEncryption]
 [-AllowBlobPublicAccess <Boolean>] [-MinimumTlsVersion <String>] [-AllowSharedKeyAccess <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-RoutingChoice <String>] [<CommonParameters>]
```

### ActiveDirectoryDomainServicesForFile
```
New-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Location] <String>
 [-Kind <String>] [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>]
 [-Tag <Hashtable>] [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-EnableHierarchicalNamespace <Boolean>] [-EnableLargeFileShare] [-PublishMicrosoftEndpoint <Boolean>]
 [-PublishInternetEndpoint <Boolean>] [-EnableActiveDirectoryDomainServicesForFile <Boolean>]
 [-ActiveDirectoryDomainName <String>] [-ActiveDirectoryNetBiosDomainName <String>]
 [-ActiveDirectoryForestName <String>] [-ActiveDirectoryDomainGuid <String>]
 [-ActiveDirectoryDomainSid <String>] [-ActiveDirectoryAzureStorageSid <String>] [-AsJob]
 [-EncryptionKeyTypeForTable <String>] [-EncryptionKeyTypeForQueue <String>] [-RequireInfrastructureEncryption]
 [-AllowBlobPublicAccess <Boolean>] [-MinimumTlsVersion <String>] [-AllowSharedKeyAccess <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-RoutingChoice <String>] [<CommonParameters>]
```

## 설명
**New-AzStorageAccount** cmdlet은 Azure Storage 계정을 만듭니다.

## 예제

### 예제 1: Storage 계정 만들기
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS
```

이 명령은 리소스 그룹 이름 MyResourceGroup에 대한 Storage 계정을 만듭니다.

### 예제 2: BlobStorage Kind 및 hot AccessTier를 사용하여 Blob Storage 계정 만들기
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind BlobStorage -AccessTier Hot
```

이 명령은 BlobStorage Kind 및 hot AccessTier를 사용하여 Blob Storage 계정을 만듭니다.

### 예제 3: Kind StorageV2를 사용하여 Storage 계정을 만들고 Azure KeyVault에 대한 ID 생성 및 할당
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind StorageV2 -AssignIdentity
```

이 명령은 Kind StorageV2를 사용하여 Storage 계정을 만듭니다.  또한 Azure KeyVault를 통해 계정 키를 관리하는 데 사용할 수 있는 ID를 생성하고 할당합니다.

### 예제 4: JSON에서 NetworkRuleSet을 사용하여 Storage 계정 만들기
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -Type Standard_LRS -NetworkRuleSet (@{bypass="Logging,Metrics";
    ipRules=(@{IPAddressOrRange="20.11.0.0/16";Action="allow"},
            @{IPAddressOrRange="10.0.0.0/7";Action="allow"});
    virtualNetworkRules=(@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},
                        @{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2";Action="allow"});
    defaultAction="Deny"})
```

이 명령은 JSON에서 NetworkRuleSet 속성이 있는 Storage 계정을 만듭니다.

### 예제 5: 계층적 네임스페이스를 사용하도록 설정한 저장소 계정 만들기
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "US West" -SkuName "Standard_GRS" -Kind StorageV2  -EnableHierarchicalNamespace $true
```

이 명령은 계층적 네임스페이스를 사용하도록 설정한 Storage 계정을 만듭니다.

### 예제 6: Azure Files AAD DS 인증을 사용하여 Storage 계정을 만들고 대용량 파일 공유를 사용하도록 설정합니다.
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EnableAzureActiveDirectoryDomainServicesForFile $true -EnableLargeFileShare
```

이 명령은 Azure Files AAD DS 인증을 사용하여 Storage 계정을 만들고 대용량 파일 공유를 사용하도록 설정합니다.

### 예제 7: Files Active Directory 도메인 서비스 인증을 사용하도록 설정하여 Storage 계정을 만드십시오.
```
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EnableActiveDirectoryDomainServicesForFile $true `
        -ActiveDirectoryDomainName "mydomain.com" `
        -ActiveDirectoryNetBiosDomainName "mydomain.com" `
        -ActiveDirectoryForestName "mydomain.com" `
        -ActiveDirectoryDomainGuid "12345678-1234-1234-1234-123456789012" `
        -ActiveDirectoryDomainSid "S-1-5-21-1234567890-1234567890-1234567890" `
        -ActiveDirectoryAzureStorageSid "S-1-5-21-1234567890-1234567890-1234567890-1234"
```

이 명령은 사용 가능한 Files Active Directory 도메인 서비스 인증이 있는 Storage 계정을 만듭니다.

### 예제 8: 큐 및 Table Service를 사용하여 Storage 계정을 만들고 계정 범위 암호화 키를 사용하며 인프라 암호화가 필요합니다.
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EncryptionKeyTypeForTable Account -EncryptionKeyTypeForQueue Account -RequireInfrastructureEncryption

PS C:\>$account = get-AzStorageAccount -ResourceGroupName $rgname -StorageAccountName $accountName

PS C:\>$account.Encryption.Services.Queue

Enabled LastEnabledTime     KeyType
------- ---------------     -------
   True 1/9/2020 6:09:11 AM Account

PS C:\>$account.Encryption.Services.Table

Enabled LastEnabledTime     KeyType
------- ---------------     -------
   True 1/9/2020 6:09:11 AM Account

PS C:\> $account.Encryption.RequireInfrastructureEncryption
True
```

이 명령은 큐 및 Table Service에서 계정 범위 암호화 키 및 인프라 암호화 요구를 사용하여 Storage 계정을 만듭니다. 따라서 큐와 테이블은 Blob 및 File service와 동일한 암호화 키를 사용하며, 서비스는 미사용 데이터에 대해 플랫폼 관리 키로 보조 암호화 계층을 적용합니다.
그런 다음 Storage 계정 속성을 얻게 하여 큐 및 테이블 서비스의 암호화 키 타이프 및 RequireInfrastructureEncryption 값을 를 본다.

### 예제 9: Account MinimumTlsVersion 및 AllowBlobPublicAccesss를 만들고 SharedKey Access를 사용하지 않도록 설정
```
PS C:\> $account = New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2 -MinimumTlsVersion TLS1_1 -AllowBlobPublicAccess $false -AllowSharedKeyAccess $false

PS C:\> $account.MinimumTlsVersion
TLS1_1

PS C:\> $account.AllowBlobPublicAccess
False

PS C:\> $a.AllowSharedKeyAccess
False
```

명령은 MinimumTlsVersion, AllowBlobPublicAccess를 사용하여 계정을 만들고 계정에 대한 SharedKey 액세스를 사용하지 않도록 설정한 다음, 생성된 계정의 3개 속성을 보여 주며 

### 예제 10: RoutingPreference 설정을 사용하여 Storage 계정 만들기
```powershell
PS C:\>$account = New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -PublishMicrosoftEndpoint $true -PublishInternetEndpoint $true -RoutingChoice MicrosoftRouting

PS C:\>$account.RoutingPreference

RoutingChoice    PublishMicrosoftEndpoints PublishInternetEndpoints
-------------    ------------------------- ------------------------
MicrosoftRouting                     True                     True

PS C:\>$account.PrimaryEndpoints

Blob               : https://mystorageaccount.blob.core.windows.net/
Queue              : https://mystorageaccount.queue.core.windows.net/
Table              : https://mystorageaccount.table.core.windows.net/
File               : https://mystorageaccount.file.core.windows.net/
Web                : https://mystorageaccount.z2.web.core.windows.net/
Dfs                : https://mystorageaccount.dfs.core.windows.net/
MicrosoftEndpoints : {"Blob":"https://mystorageaccount-microsoftrouting.blob.core.windows.net/","Queue":"https://mystorageaccount-microsoftrouting.queue.core.windows.net/","Table":"https://mystorageaccount-microsoftrouting.table.core.windows.net/","File":"ht
                     tps://mystorageaccount-microsoftrouting.file.core.windows.net/","Web":"https://mystorageaccount-microsoftrouting.z2.web.core.windows.net/","Dfs":"https://mystorageaccount-microsoftrouting.dfs.core.windows.net/"}
InternetEndpoints  : {"Blob":"https://mystorageaccount-internetrouting.blob.core.windows.net/","File":"https://mystorageaccount-internetrouting.file.core.windows.net/","Web":"https://mystorageaccount-internetrouting.z2.web.core.windows.net/","Dfs":"https://w
                     eirp3-internetrouting.dfs.core.windows.net/"}
```

이 명령은 RoutingPreference 설정이 있는 Storage 계정을 만듭니다. PublishMicrosoftEndpoint 및 PublishInternetEndpoint는 true로, RoutingChoice를 MicrosoftRouting으로 만듭니다.

## 매개 변수

### -AccessTier
이 cmdlet이 만드는 Storage 계정의 액세스 계층을 지정합니다.
이 매개 변수에 대해 허용되는 값은 핫 및 쿨입니다.
Kind 매개 변수에 BlobStorage  값을 지정하는 경우 *AccessTier* 매개 변수에 대한 값을 지정해야 합니다. 이 Kind 매개 변수에 대한 Storage 값을 *지정하는* 경우 *AccessTier 매개 변수를 지정하지* 않습니다.

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
Azure Storage에 대한 SID(보안 식별자)를 지정합니다. -EnableActiveDirectoryDomainServicesForFile이 true로 설정될 때 이 매개 변수를 설정해야 합니다.

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
도메인 GUID를 지정합니다. -EnableActiveDirectoryDomainServicesForFile이 true로 설정될 때 이 매개 변수를 설정해야 합니다.

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
AD DNS 서버가 권한이 있는 기본 도메인을 지정합니다. -EnableActiveDirectoryDomainServicesForFile이 true로 설정될 때 이 매개 변수를 설정해야 합니다.

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
SID(보안 식별자)를 지정합니다. -EnableActiveDirectoryDomainServicesForFile이 true로 설정될 때 이 매개 변수를 설정해야 합니다.

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
얻을 Active Directory 포리스트를 지정합니다. -EnableActiveDirectoryDomainServicesForFile이 true로 설정될 때 이 매개 변수를 설정해야 합니다.

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
NetBIOS 도메인 이름을 지정합니다. -EnableActiveDirectoryDomainServicesForFile이 true로 설정될 때 이 매개 변수를 설정해야 합니다.

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

### -AllowBlobPublicAccesss
저장소 계정의 모든 Blob 또는 컨테이너에 대한 공용 액세스를 허용합니다. 이 속성에 대한 기본 해석은 true입니다.

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

### -AllowSharedKeyAccesss
저장소 계정이 공유 키를 통해 계정 액세스 키로 권한을 부여하는 요청을 허용하는지 여부를 나타냅니다. false인 경우 공유 액세스 서명을 포함한 모든 요청은 Azure AD(Azure Active Directory)를 사용하여 권한을 부여해야 합니다. 기본값은 true와 동일한 null입니다.

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
Azure KeyVault와 같은 주요 관리 서비스와 함께 사용하기 위해 이 Storage 계정에 대한 새 Storage 계정 ID를 생성하고 할당합니다.

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
Storage 계정의 사용자 지정 도메인 이름을 지정합니다.
기본값은 Storage입니다.

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
Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.

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
저장소 계정에 대해 Azure Files Active Directory 도메인 서비스 인증을 사용하도록 설정합니다.

```yaml
Type: System.Boolean
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableAzureActiveDirectoryDomainServicesForFile
저장소 계정에 대해 Azure Files Azure Active Directory 도메인 서비스 인증을 사용하도록 설정합니다.

```yaml
Type: System.Boolean
Parameter Sets: AzureActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableHierarchicalNamespace
저장소 계정이 계층적 네임스페이스를 사용할 수 있는지 여부를 나타냅니다.

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

### -enableLargeFileShare
저장소 계정이 TiB 용량이 5개 이상인 대용량 파일 공유를 지원할 수 있는지 여부를 나타냅니다. 계정을 사용하도록 설정하면 기능을 사용하지 않도록 설정할 수 없습니다. 현재 LRS 및 ZRS 복제 유형에만 지원됩니다. 따라서 지역 중복 계정으로 계정 변환은 불가능합니다. 자세히 알아보기 https://go.microsoft.com/fwlink/?linkid=2086047

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

### -EncryptionKeyTypeForQueue
큐에 대한 암호화 키 타이프를 설정합니다. 기본값은 Service입니다.
-Account: 큐는 계정 범위 암호화 키로 암호화됩니다. -Service: 큐는 항상 키로 Service-Managed 됩니다. 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Service, Account

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EncryptionKeyTypeForTable
표에 대한 암호화 키 타이프를 설정합니다. 기본값은 Service입니다.
- 계정: 테이블은 계정 범위 암호화 키로 암호화됩니다. 
- 서비스: 테이블은 항상 키로 Service-Managed 됩니다. 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Service, Account

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Kind
이 cmdlet에서 만드는 저장소 계정의 종류를 지정합니다.
이 매개 변수에 대해 허용되는 값은 다음입니다.
- 저장소. Blob, 테이블, 큐, 파일 및 디스크의 저장소를 지원하는 일반적 저장소 계정입니다.
- StorageV2. 데이터 계층화와 같은 고급 기능을 사용하여 Blob, 테이블, 큐, 파일 및 디스크를 지원하는 일반 용도 버전 2(GPv2) Storage 계정입니다.
- BlobStorage. Blob의 저장소만 지원하는 Blob Storage 계정입니다.
- BlockBlobStorage. 블록 Blob의 저장소만 지원하는 블록 Blob Storage 계정입니다.
- FileStorage. 파일 저장소만 지원하는 파일 저장소 계정입니다.
기본값은 StorageV2입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Storage, StorageV2, BlobStorage, BlockBlobStorage, FileStorage

Required: False
Position: Named
Default value: StorageV2
Accept pipeline input: False
Accept wildcard characters: False
```

### -Location
만들 저장소 계정의 위치를 지정합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -MinimumTlsVersion
저장소에 대한 요청에 허용되는 최소 TLS 버전입니다. 기본 해석은 이 속성에 대한 TLS 1.0입니다.

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
만들 저장소 계정의 이름을 지정합니다.

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
NetworkRuleSet은 방화벽 및 가상 네트워크에 대한 구성 규칙 집합을 정의하고 규칙을 무시할 수 있는 서비스 및 정의된 규칙과 일치하지 않는 요청을 처리하는 방법과 같은 네트워크 속성에 대한 값을 설정하는 데 사용됩니다.

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

### -PublishInternetEndpoint
인터넷 라우팅 저장소 엔드포인트를 게시할지 여부를 나타냅니다.

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

### -PublishMicrosoftEndpoint
Microsoft 라우팅 저장소 엔드포인트를 게시할지 여부를 나타냅니다.

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

### -RequireInfrastructureEncryption
서비스는 미사용 데이터에 대한 플랫폼 관리 키가 있는 보조 암호화 계층을 적용합니다.

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

### -ResourceGroupName
Storage 계정을 추가할 리소스 그룹의 이름을 지정합니다.

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

### -RoutingChoice
라우팅 선택은 사용자가 선택한 네트워크 라우팅의 종류를 정의합니다. 가능한 값에는 'MicrosoftRouting', 'InternetRouting'이 포함됩니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: MicrosoftRouting, InternetRouting

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SkuName
이 cmdlet이 만드는 Storage 계정의 SKU 이름을 지정합니다.
이 매개 변수에 대해 허용되는 값은 다음입니다.
- Standard_LRS. 로컬 중복 저장소입니다.
- Standard_ZRS. 영역 중복 저장소.
- Standard_GRS. 지역 중복 저장소.
- Standard_RAGRS. 액세스 지역 중복 저장소를 읽습니다.
- Premium_LRS. 프리미엄 로컬 중복 저장소.
- Premium_ZRS. 프리미엄 영역 중복 저장소.
- Standard_GZRS - 지역 중복 영역-중복 저장소.
- Standard_RAGZRS - 액세스 지역 중복 영역 중복 저장소를 읽습니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountType, AccountType, Type
Accepted values: Standard_LRS, Standard_ZRS, Standard_GRS, Standard_RAGRS, Premium_LRS, Premium_ZRS, Standard_GZRS, Standard_RAGZRS

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tag
서버의 태그로 설정된 해시 테이블의 형태로 키 값 쌍입니다. 예: @{key0="value0";key1=$null;key2="value2"}

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

### -UseSubDomain
간접 CName 유효성 검사를 사용하도록 설정할지 여부를 나타냅니다.

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

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.

## 입력

### System.String

## 출력

### Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount

## 참고 사항

## 관련 링크

[Get-AzStorageAccount](./Get-AzStorageAccount.md)

[Remove-AzStorageAccount](./Remove-AzStorageAccount.md)

[Set-AzStorageAccount](./Set-AzStorageAccount.md)
