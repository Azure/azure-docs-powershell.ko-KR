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
# <span data-ttu-id="77af1-101">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="77af1-101">Get-AzRmStorageShare</span></span>

## <span data-ttu-id="77af1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="77af1-102">SYNOPSIS</span></span>
<span data-ttu-id="77af1-103">저장소 파일 공유를 가져오거나 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="77af1-103">Gets or lists Storage file shares.</span></span>

## <span data-ttu-id="77af1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="77af1-104">SYNTAX</span></span>

### <span data-ttu-id="77af1-105">AccountNameSingle (기본값)</span><span class="sxs-lookup"><span data-stu-id="77af1-105">AccountNameSingle (Default)</span></span>
```
Get-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> [-Name <String>]
 [-GetShareUsage] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="77af1-106">계정</span><span class="sxs-lookup"><span data-stu-id="77af1-106">AccountName</span></span>
```
Get-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> [-IncludeDeleted]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="77af1-107">AccountObjectSingle</span><span class="sxs-lookup"><span data-stu-id="77af1-107">AccountObjectSingle</span></span>
```
Get-AzRmStorageShare -StorageAccount <PSStorageAccount> -Name <String> [-GetShareUsage]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="77af1-108">AccountObject</span><span class="sxs-lookup"><span data-stu-id="77af1-108">AccountObject</span></span>
```
Get-AzRmStorageShare -StorageAccount <PSStorageAccount> [-IncludeDeleted]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="77af1-109">ShareResourceId</span><span class="sxs-lookup"><span data-stu-id="77af1-109">ShareResourceId</span></span>
```
Get-AzRmStorageShare [-ResourceId] <String> [-Name <String>] [-GetShareUsage]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="77af1-110">설명은</span><span class="sxs-lookup"><span data-stu-id="77af1-110">DESCRIPTION</span></span>
<span data-ttu-id="77af1-111">**Get-AzRmStorageShare** Cmdlet은 저장소 파일 공유를 가져오거나 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="77af1-111">The **Get-AzRmStorageShare** cmdlet gets or lists Storage file shares.</span></span>

## <span data-ttu-id="77af1-112">예제의</span><span class="sxs-lookup"><span data-stu-id="77af1-112">EXAMPLES</span></span>

### <span data-ttu-id="77af1-113">예제 1: 저장소 계정 이름과 공유 이름을 사용 하 여 저장소 파일 공유 가져오기</span><span class="sxs-lookup"><span data-stu-id="77af1-113">Example 1: Get a Storage file share with Storage account name and share name</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -Name "myshare"

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare  5120
```

<span data-ttu-id="77af1-114">이 명령은 저장소 계정 이름과 공유 이름이 있는 저장소 파일 공유를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="77af1-114">This command gets a Storage file share with Storage account name and share name.</span></span>

### <span data-ttu-id="77af1-115">예제 2: 저장소 계정의 모든 저장소 파일 공유 나열</span><span class="sxs-lookup"><span data-stu-id="77af1-115">Example 2: List all Storage file shares of a Storage account</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount"

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier           Deleted Version ShareUsageBytes
----     -------- --------------- ----------           ------- ------- ---------------
share1   5120                     TransactionOptimized
share2   5120                     TransactionOptimized
```

<span data-ttu-id="77af1-116">이 명령은 저장소 계정 이름이 있는 저장소 계정의 모든 저장소 파일 공유를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="77af1-116">This command lists all Storage file shares of a Storage account with Storage account name.</span></span>

### <span data-ttu-id="77af1-117">예제 3: 저장소 계정 개체 및 컨테이너 이름을 사용 하 여 저장소 blob 컨테이너를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="77af1-117">Example 3: Get a Storage blob container with Storage account object and container name.</span></span>
```
Get-AzStorageAccount -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" | Get-AzRmStorageShare -Name "myshare"

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare  5120
```

<span data-ttu-id="77af1-118">이 명령은 저장소 계정 개체와 컨테이너 이름이 있는 저장소 blob 컨테이너를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="77af1-118">This command gets a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="77af1-119">예제 4: 공유 사용량으로 저장소 파일 공유 가져오기 (바이트)</span><span class="sxs-lookup"><span data-stu-id="77af1-119">Example 4: Get a Storage file share with the share usage in bytes</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -Name "myshare" -GetShareUsage

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare  5120                                                2097152
```

<span data-ttu-id="77af1-120">이 명령은 저장소 계정 이름과 공유 이름이 있는 저장소 파일 공유를 가져오고 공유 사용량 (바이트)을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="77af1-120">This command gets a Storage file share with Storage account name and share name, and include the share usage in bytes.</span></span>

### <span data-ttu-id="77af1-121">예제 5: 저장소 계정의 모든 저장소 파일 공유 나열 삭제 된 공유 포함</span><span class="sxs-lookup"><span data-stu-id="77af1-121">Example 5: List all Storage file shares of a Storage account, include the deleted shares</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -IncludeDeleted 

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier           Deleted Version          ShareUsageBytes
----     -------- --------------- ----------           ------- -------          ---------------
test     100                      TransactionOptimized                                         
share1   100                      TransactionOptimized True    01D61FD1FC5498B6
```

<span data-ttu-id="77af1-122">이 명령은 저장소 계정 이름이 있는 저장소 계정의 삭제 된 공유를 포함 하는 모든 저장소 파일 공유를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="77af1-122">This command lists all Storage file shares include the deleted shares of a Storage account with Storage account name.</span></span>

## <span data-ttu-id="77af1-123">변수</span><span class="sxs-lookup"><span data-stu-id="77af1-123">PARAMETERS</span></span>

### <span data-ttu-id="77af1-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77af1-124">-DefaultProfile</span></span>
<span data-ttu-id="77af1-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="77af1-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77af1-126">-GetShareUsage</span><span class="sxs-lookup"><span data-stu-id="77af1-126">-GetShareUsage</span></span>
<span data-ttu-id="77af1-127">공유 사용량을 바이트로 가져오려면이 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="77af1-127">Specify this parameter to get the Share Usage in Bytes.</span></span>

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

### <span data-ttu-id="77af1-128">-IncludeDeleted</span><span class="sxs-lookup"><span data-stu-id="77af1-128">-IncludeDeleted</span></span>
<span data-ttu-id="77af1-129">삭제 된 공유 포함 목록 공유는 기본적으로 삭제 된 공유를 포함 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="77af1-129">Include deleted shares, by default list shares won't include deleted shares</span></span>

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

### <span data-ttu-id="77af1-130">-이름</span><span class="sxs-lookup"><span data-stu-id="77af1-130">-Name</span></span>
<span data-ttu-id="77af1-131">공유 이름</span><span class="sxs-lookup"><span data-stu-id="77af1-131">Share Name</span></span>

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

### <span data-ttu-id="77af1-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77af1-132">-ResourceGroupName</span></span>
<span data-ttu-id="77af1-133">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="77af1-133">Resource Group Name.</span></span>

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

### <span data-ttu-id="77af1-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="77af1-134">-ResourceId</span></span>
<span data-ttu-id="77af1-135">파일 공유 리소스 Id를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="77af1-135">Input a File Share Resource Id.</span></span>

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

### <span data-ttu-id="77af1-136">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="77af1-136">-StorageAccount</span></span>
<span data-ttu-id="77af1-137">저장소 계정 개체</span><span class="sxs-lookup"><span data-stu-id="77af1-137">Storage account object</span></span>

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

### <span data-ttu-id="77af1-138">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="77af1-138">-StorageAccountName</span></span>
<span data-ttu-id="77af1-139">저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="77af1-139">Storage Account Name.</span></span>

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

### <span data-ttu-id="77af1-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77af1-140">CommonParameters</span></span>
<span data-ttu-id="77af1-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="77af1-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77af1-142">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77af1-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77af1-143">입력</span><span class="sxs-lookup"><span data-stu-id="77af1-143">INPUTS</span></span>

### <span data-ttu-id="77af1-144">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="77af1-144">System.String</span></span>

### <span data-ttu-id="77af1-145">Microsoft. Azure.. i m a. 모델. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="77af1-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="77af1-146">출력</span><span class="sxs-lookup"><span data-stu-id="77af1-146">OUTPUTS</span></span>

### <span data-ttu-id="77af1-147">Microsoft. i. m a i 공유.</span><span class="sxs-lookup"><span data-stu-id="77af1-147">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="77af1-148">상속자</span><span class="sxs-lookup"><span data-stu-id="77af1-148">NOTES</span></span>

## <span data-ttu-id="77af1-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="77af1-149">RELATED LINKS</span></span>
