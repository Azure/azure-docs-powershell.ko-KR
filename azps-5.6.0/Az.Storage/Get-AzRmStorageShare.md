---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageShare.md
ms.openlocfilehash: 44ad4fadb86b84b5eacb82a15bf92b7b1d831b70
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002827"
---
# <span data-ttu-id="5163a-101">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="5163a-101">Get-AzRmStorageShare</span></span>

## <span data-ttu-id="5163a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5163a-102">SYNOPSIS</span></span>
<span data-ttu-id="5163a-103">Storage 파일 공유를 얻거나 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="5163a-103">Gets or lists Storage file shares.</span></span>

## <span data-ttu-id="5163a-104">구문</span><span class="sxs-lookup"><span data-stu-id="5163a-104">SYNTAX</span></span>

### <span data-ttu-id="5163a-105">AccountNameSingle(기본값)</span><span class="sxs-lookup"><span data-stu-id="5163a-105">AccountNameSingle (Default)</span></span>
```
Get-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> [-Name <String>]
 [-GetShareUsage] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5163a-106">AccountName</span><span class="sxs-lookup"><span data-stu-id="5163a-106">AccountName</span></span>
```
Get-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> [-IncludeDeleted]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5163a-107">AccountObjectSingle</span><span class="sxs-lookup"><span data-stu-id="5163a-107">AccountObjectSingle</span></span>
```
Get-AzRmStorageShare -StorageAccount <PSStorageAccount> -Name <String> [-GetShareUsage]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5163a-108">AccountObject</span><span class="sxs-lookup"><span data-stu-id="5163a-108">AccountObject</span></span>
```
Get-AzRmStorageShare -StorageAccount <PSStorageAccount> [-IncludeDeleted]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5163a-109">ShareResourceId</span><span class="sxs-lookup"><span data-stu-id="5163a-109">ShareResourceId</span></span>
```
Get-AzRmStorageShare [-ResourceId] <String> [-Name <String>] [-GetShareUsage]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5163a-110">설명</span><span class="sxs-lookup"><span data-stu-id="5163a-110">DESCRIPTION</span></span>
<span data-ttu-id="5163a-111">**Get-AzRmStorageShare** cmdlet은 Storage 파일 공유를 얻거나 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="5163a-111">The **Get-AzRmStorageShare** cmdlet gets or lists Storage file shares.</span></span>

## <span data-ttu-id="5163a-112">예제</span><span class="sxs-lookup"><span data-stu-id="5163a-112">EXAMPLES</span></span>

### <span data-ttu-id="5163a-113">예제 1: Storage 계정 이름 및 공유 이름으로 Storage 파일 공유하기</span><span class="sxs-lookup"><span data-stu-id="5163a-113">Example 1: Get a Storage file share with Storage account name and share name</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -Name "myshare"

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare  5120
```

<span data-ttu-id="5163a-114">이 명령은 Storage 계정 이름 및 공유 이름으로 Storage 파일 공유를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5163a-114">This command gets a Storage file share with Storage account name and share name.</span></span>

### <span data-ttu-id="5163a-115">예제 2: Storage 계정의 모든 Storage 파일 공유 나열</span><span class="sxs-lookup"><span data-stu-id="5163a-115">Example 2: List all Storage file shares of a Storage account</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount"

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier           Deleted Version ShareUsageBytes
----     -------- --------------- ----------           ------- ------- ---------------
share1   5120                     TransactionOptimized
share2   5120                     TransactionOptimized
```

<span data-ttu-id="5163a-116">이 명령은 Storage 계정 이름으로 Storage 계정의 모든 Storage 파일 공유를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="5163a-116">This command lists all Storage file shares of a Storage account with Storage account name.</span></span>

### <span data-ttu-id="5163a-117">예제 3: Storage 계정 개체 및 컨테이너 이름으로 Storage Blob 컨테이너를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5163a-117">Example 3: Get a Storage blob container with Storage account object and container name.</span></span>
```
Get-AzStorageAccount -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" | Get-AzRmStorageShare -Name "myshare"

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare  5120
```

<span data-ttu-id="5163a-118">이 명령은 Storage 계정 개체 및 컨테이너 이름이 있는 Storage Blob 컨테이너를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5163a-118">This command gets a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="5163a-119">예제 4: 공유 사용량과 저장소 파일 공유를 bytes로 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5163a-119">Example 4: Get a Storage file share with the share usage in bytes</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -Name "myshare" -GetShareUsage

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare  5120                                                2097152
```

<span data-ttu-id="5163a-120">이 명령은 Storage 계정 이름 및 공유 이름과 함께 Storage 파일 공유를 얻게 며, 공유 사용량을 bytes에 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="5163a-120">This command gets a Storage file share with Storage account name and share name, and include the share usage in bytes.</span></span>

### <span data-ttu-id="5163a-121">예제 5: Storage 계정의 모든 Storage 파일 공유 나열, 삭제된 공유 포함</span><span class="sxs-lookup"><span data-stu-id="5163a-121">Example 5: List all Storage file shares of a Storage account, include the deleted shares</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -IncludeDeleted 

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier           Deleted Version          ShareUsageBytes
----     -------- --------------- ----------           ------- -------          ---------------
test     100                      TransactionOptimized                                         
share1   100                      TransactionOptimized True    01D61FD1FC5498B6
```

<span data-ttu-id="5163a-122">이 명령에는 저장소 계정 이름이 포함된 Storage 계정의 삭제된 공유가 포함된 모든 Storage 파일 공유가 나열됩니다.</span><span class="sxs-lookup"><span data-stu-id="5163a-122">This command lists all Storage file shares include the deleted shares of a Storage account with Storage account name.</span></span>

## <span data-ttu-id="5163a-123">매개 변수</span><span class="sxs-lookup"><span data-stu-id="5163a-123">PARAMETERS</span></span>

### <span data-ttu-id="5163a-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5163a-124">-DefaultProfile</span></span>
<span data-ttu-id="5163a-125">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5163a-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5163a-126">-GetShareUsage</span><span class="sxs-lookup"><span data-stu-id="5163a-126">-GetShareUsage</span></span>
<span data-ttu-id="5163a-127">이 매개 변수를 지정하여 Bytes에서 공유 사용량을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5163a-127">Specify this parameter to get the Share Usage in Bytes.</span></span>

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

### <span data-ttu-id="5163a-128">-IncludeDeleted</span><span class="sxs-lookup"><span data-stu-id="5163a-128">-IncludeDeleted</span></span>
<span data-ttu-id="5163a-129">삭제된 공유 포함, 기본적으로 목록 공유는 삭제된 공유를 포함하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5163a-129">Include deleted shares, by default list shares won't include deleted shares</span></span>

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

### <span data-ttu-id="5163a-130">-Name</span><span class="sxs-lookup"><span data-stu-id="5163a-130">-Name</span></span>
<span data-ttu-id="5163a-131">이름 공유</span><span class="sxs-lookup"><span data-stu-id="5163a-131">Share Name</span></span>

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

### <span data-ttu-id="5163a-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5163a-132">-ResourceGroupName</span></span>
<span data-ttu-id="5163a-133">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5163a-133">Resource Group Name.</span></span>

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

### <span data-ttu-id="5163a-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5163a-134">-ResourceId</span></span>
<span data-ttu-id="5163a-135">파일 공유 리소스 ID를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="5163a-135">Input a File Share Resource Id.</span></span>

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

### <span data-ttu-id="5163a-136">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="5163a-136">-StorageAccount</span></span>
<span data-ttu-id="5163a-137">저장소 계정 개체</span><span class="sxs-lookup"><span data-stu-id="5163a-137">Storage account object</span></span>

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

### <span data-ttu-id="5163a-138">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="5163a-138">-StorageAccountName</span></span>
<span data-ttu-id="5163a-139">저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5163a-139">Storage Account Name.</span></span>

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

### <span data-ttu-id="5163a-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5163a-140">CommonParameters</span></span>
<span data-ttu-id="5163a-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5163a-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5163a-142">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5163a-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5163a-143">입력</span><span class="sxs-lookup"><span data-stu-id="5163a-143">INPUTS</span></span>

### <span data-ttu-id="5163a-144">System.String</span><span class="sxs-lookup"><span data-stu-id="5163a-144">System.String</span></span>

### <span data-ttu-id="5163a-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5163a-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="5163a-146">출력</span><span class="sxs-lookup"><span data-stu-id="5163a-146">OUTPUTS</span></span>

### <span data-ttu-id="5163a-147">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span><span class="sxs-lookup"><span data-stu-id="5163a-147">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="5163a-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5163a-148">NOTES</span></span>

## <span data-ttu-id="5163a-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5163a-149">RELATED LINKS</span></span>
