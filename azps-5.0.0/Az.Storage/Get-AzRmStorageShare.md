---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageShare.md
ms.openlocfilehash: 90edd254eb77b03f4f4d26761020d71025960426
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226479"
---
# Get-AzRmStorageShare

## SYNOPSIS
저장소 파일 공유를 가져오거나 나열 합니다.

## 구문과

### AccountNameSingle (기본값)
```
Get-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> [-Name <String>]
 [-GetShareUsage] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### 계정
```
Get-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> [-IncludeDeleted]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### AccountObjectSingle
```
Get-AzRmStorageShare -StorageAccount <PSStorageAccount> -Name <String> [-GetShareUsage]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### AccountObject
```
Get-AzRmStorageShare -StorageAccount <PSStorageAccount> [-IncludeDeleted]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ShareResourceId
```
Get-AzRmStorageShare [-ResourceId] <String> [-Name <String>] [-GetShareUsage]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**Get-AzRmStorageShare** Cmdlet은 저장소 파일 공유를 가져오거나 나열 합니다.

## 예제의

### 예제 1: 저장소 계정 이름과 공유 이름을 사용 하 여 저장소 파일 공유 가져오기
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -Name "myshare"

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare  5120
```

이 명령은 저장소 계정 이름과 공유 이름이 있는 저장소 파일 공유를 가져옵니다.

### 예제 2: 저장소 계정의 모든 저장소 파일 공유 나열
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount"

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier           Deleted Version ShareUsageBytes
----     -------- --------------- ----------           ------- ------- ---------------
share1   5120                     TransactionOptimized
share2   5120                     TransactionOptimized
```

이 명령은 저장소 계정 이름이 있는 저장소 계정의 모든 저장소 파일 공유를 나열 합니다.

### 예제 3: 저장소 계정 개체 및 컨테이너 이름을 사용 하 여 저장소 blob 컨테이너를 가져옵니다.
```
Get-AzStorageAccount -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" | Get-AzRmStorageShare -Name "myshare"

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare  5120
```

이 명령은 저장소 계정 개체와 컨테이너 이름이 있는 저장소 blob 컨테이너를 가져옵니다.

### 예제 4: 공유 사용량으로 저장소 파일 공유 가져오기 (바이트)
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -Name "myshare" -GetShareUsage

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare  5120                                                2097152
```

이 명령은 저장소 계정 이름과 공유 이름이 있는 저장소 파일 공유를 가져오고 공유 사용량 (바이트)을 포함 합니다.

### 예제 5: 저장소 계정의 모든 저장소 파일 공유 나열 삭제 된 공유 포함
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -IncludeDeleted 

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier           Deleted Version          ShareUsageBytes
----     -------- --------------- ----------           ------- -------          ---------------
test     100                      TransactionOptimized                                         
share1   100                      TransactionOptimized True    01D61FD1FC5498B6
```

이 명령은 저장소 계정 이름이 있는 저장소 계정의 삭제 된 공유를 포함 하는 모든 저장소 파일 공유를 나열 합니다.

## 변수

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

### -GetShareUsage
공유 사용량을 바이트로 가져오려면이 매개 변수를 지정 합니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AccountNameSingle, AccountObjectSingle, ShareResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IncludeDeleted
삭제 된 공유 포함 목록 공유는 기본적으로 삭제 된 공유를 포함 하지 않습니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AccountName, AccountObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -이름
공유 이름

```yaml
Type: System.String
Parameter Sets: AccountNameSingle, ShareResourceId
Aliases: N, ShareName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AccountObjectSingle
Aliases: N, ShareName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
리소스 그룹 이름입니다.

```yaml
Type: System.String
Parameter Sets: AccountNameSingle, AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
파일 공유 리소스 Id를 입력 합니다.

```yaml
Type: System.String
Parameter Sets: ShareResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccount
저장소 계정 개체

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObjectSingle, AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -StorageAccountName
저장소 계정 이름입니다.

```yaml
Type: System.String
Parameter Sets: AccountNameSingle, AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### System. 문자열

### Microsoft. Azure.. i m a. 모델. PSStorageAccount

## 출력

### Microsoft. i. m a i 공유.

## 상속자

## 관련 링크
