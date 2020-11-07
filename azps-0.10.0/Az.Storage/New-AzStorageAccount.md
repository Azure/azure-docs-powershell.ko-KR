---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A3DA1205-B8FB-4B4C-9C40-AD303D038EDF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/New-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/New-AzStorageAccount.md
ms.openlocfilehash: 3ded950659546b6ec2a25271bc09718c937d401b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876278"
---
# New-AzStorageAccount

## SYNOPSIS
저장소 계정을 만듭니다.

## 구문과

```
New-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String>
 [-Location] <String> [-Kind <String>] [-AccessTier <String>] [-CustomDomainName <String>]
 [-UseSubDomain <Boolean>] [-Tag <Hashtable>] [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzStorageAccount** Cmdlet은 Azure 저장소 계정을 만듭니다.

## 예제의

### 예제 1: 저장소 계정 만들기
```
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS
```

이 명령은 리소스 그룹 이름 MyResourceGroup에 대 한 저장소 계정을 만듭니다.

### 예제 2: BlobStorage Kind 및 hot AccessTier를 사용 하 여 Blob 저장소 계정 만들기
```
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind BlobStorage -AccessTier Hot
```

이 명령은 BlobStorage Kind 및 hot AccessTier를 사용 하는 Blob 저장소 계정을 만듭니다.

### 예제 3: Kind StorageV2를 사용 하 여 저장소 계정을 만들고 Azure KeyVault에 대 한 Id를 생성 하 고 할당 합니다.
```
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind StorageV2 -AssignIdentity
```

이 명령은 Kind StorageV2를 사용 하 여 저장소 계정을 만듭니다.  또한 Azure KeyVault를 통해 계정 키를 관리 하는 데 사용할 수 있는 id를 생성 하 고 할당 합니다.

### 예제 4: JSON에서 NetworkRuleSet 집합을 사용 하 여 저장소 계정 만들기
```
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -Type Standard_LRS -NetworkRuleSet (@{bypass="Logging,Metrics";
    ipRules=(@{IPAddressOrRange="20.11.0.0/16";Action="allow"},
            @{IPAddressOrRange="10.0.0.0/7";Action="allow"});
    virtualNetworkRules=(@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},
                        @{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2";Action="allow"});
    defaultAction="Deny"})
```

이 명령은 JSON의 NetworkRuleSet 집합 속성이 있는 저장소 계정을 만듭니다.

## 변수

### -AccessTier
이 cmdlet이 만드는 저장소 계정의 액세스 계층을 지정 합니다.
이 매개 변수에 허용 되는 값은 Hot 및 멋지게입니다.
*Kind* 매개 변수에 대 한 blobstorage의 값을 지정 하는 경우 *AccessTier* 매개 변수에 대 한 값을 지정 해야 합니다. 이 *Kind* 매개 변수에 대 한 저장소 값을 지정 하는 경우 *AccessTier* 매개 변수를 지정 하지 마세요.

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
저장소 계정의 사용자 지정 도메인의 이름을 지정 합니다.
기본 값은 저장소입니다.

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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

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
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -종류
이 cmdlet이 만드는 저장소 계정의 종류를 지정 합니다.
이 매개 변수에 허용 되는 값은 다음과 같습니다.
- 용량. Blob, 테이블, 대기열, 파일, 디스크의 저장소를 지 원하는 범용 저장소 계정입니다.
- StorageV2. 데이터 계층화와 같은 고급 기능을 사용 하 여 Blob, 테이블, 대기열, 파일, 디스크를 지 원하는 범용 GPv2 (범용 버전 2) 저장소 계정입니다.
- BlobStorage. Blob 저장소만 지 원하는 blob 저장소 계정입니다.
기본 값은 저장소입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Storage, StorageV2, BlobStorage

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -위치
만들 저장소 계정의 위치를 지정 합니다.

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

### -이름
만들 저장소 계정의 이름을 지정 합니다.

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
저장소 계정을 추가할 리소스 그룹의 이름을 지정 합니다.

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
이 cmdlet이 만드는 저장소 계정의 SKU 이름을 지정 합니다.
이 매개 변수에 허용 되는 값은 다음과 같습니다.
- Standard_LRS. 로컬 중복 저장소.
- Standard_ZRS. 영역 중복 저장소.
- Standard_GRS. 지리적 중복 저장소.
- Standard_RAGRS. 액세스 지리적 중복 저장소 읽기
- Premium_LRS. 프리미엄 로컬 중복 저장소.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountType, AccountType, Type
Accepted values: Standard_LRS, Standard_ZRS, Standard_GRS, Standard_RAGRS, Premium_LRS

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### System. 문자열

### 시스템 부울

## 출력

### Microsoft. Azure.. i m a. 모델. PSStorageAccount

## 상속자

## 관련 링크

[Get-AzStorageAccount](./Get-AzStorageAccount.md)

[제거-AzStorageAccount](./Remove-AzStorageAccount.md)

[Set-AzStorageAccount](./Set-AzStorageAccount.md)
