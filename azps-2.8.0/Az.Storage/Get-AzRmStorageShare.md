---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageShare.md
ms.openlocfilehash: f54196ef5b055a5e1968c682d21f861ee41c77ac
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93874111"
---
# <span data-ttu-id="17d56-101">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="17d56-101">Get-AzRmStorageShare</span></span>

## <span data-ttu-id="17d56-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17d56-102">SYNOPSIS</span></span>
<span data-ttu-id="17d56-103">저장소 파일 공유를 가져오거나 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="17d56-103">Gets or lists Storage file shares.</span></span>

## <span data-ttu-id="17d56-104">구문과</span><span class="sxs-lookup"><span data-stu-id="17d56-104">SYNTAX</span></span>

### <span data-ttu-id="17d56-105">AccountName (기본값)</span><span class="sxs-lookup"><span data-stu-id="17d56-105">AccountName (Default)</span></span>
```
Get-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="17d56-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="17d56-106">AccountObject</span></span>
```
Get-AzRmStorageShare -StorageAccount <PSStorageAccount> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="17d56-107">ShareResourceId</span><span class="sxs-lookup"><span data-stu-id="17d56-107">ShareResourceId</span></span>
```
Get-AzRmStorageShare [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="17d56-108">설명은</span><span class="sxs-lookup"><span data-stu-id="17d56-108">DESCRIPTION</span></span>
<span data-ttu-id="17d56-109">**Get-AzRmStorageShare** Cmdlet은 저장소 파일 공유를 가져오거나 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="17d56-109">The **Get-AzRmStorageShare** cmdlet gets or lists Storage file shares.</span></span>

## <span data-ttu-id="17d56-110">예제의</span><span class="sxs-lookup"><span data-stu-id="17d56-110">EXAMPLES</span></span>

### <span data-ttu-id="17d56-111">예제 1: 저장소 계정 이름과 공유 이름을 사용 하 여 저장소 파일 공유 가져오기</span><span class="sxs-lookup"><span data-stu-id="17d56-111">Example 1: Get a Storage file share with Storage account name and share name</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount" -Name "myshare"

Name     StorageAccountName ResourceGroupName Etag                QuotaGiB LastModifiedTime    
----     ------------------ ----------------- ----                -------- ----------------    
myshare  myStorageAccount   myResourceGroup   "0x8D71F03028DDDC9" 5120     2019-08-12 08:56:48Z
```

<span data-ttu-id="17d56-112">이 명령은 저장소 계정 이름과 공유 이름이 있는 저장소 파일 공유를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="17d56-112">This command gets a Storage file share with Storage account name and share name.</span></span>

### <span data-ttu-id="17d56-113">예제 2: 저장소 계정의 모든 저장소 파일 공유 나열</span><span class="sxs-lookup"><span data-stu-id="17d56-113">Example 2: List all Storage file shares of a Storage account</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount"

Name     StorageAccountName ResourceGroupName Etag                QuotaGiB LastModifiedTime    
----     ------------------ ----------------- ----                -------- ----------------    
share1   myStorageAccount   myResourceGroup   "0x8D71F03028DDDC9" 5120     2019-08-12 08:56:48Z
share2   myStorageAccount   myResourceGroup   "0x8D6FF862774FE57" 5120     2019-07-03 07:14:57Z
```

<span data-ttu-id="17d56-114">이 명령은 저장소 계정 이름이 있는 저장소 계정의 모든 저장소 파일 공유를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="17d56-114">This command lists all Storage file shares of a Storage account with Storage account name.</span></span>

### <span data-ttu-id="17d56-115">예제 3: 저장소 계정 개체 및 컨테이너 이름을 사용 하 여 저장소 blob 컨테이너를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="17d56-115">Example 3: Get a Storage blob container with Storage account object and container name.</span></span>
```
Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount" | Get-AzRmStorageShare -Name "myshare"

Name     StorageAccountName ResourceGroupName Etag                QuotaGiB LastModifiedTime    
----     ------------------ ----------------- ----                -------- ----------------    
myshare  myStorageAccount   myResourceGroup   "0x8D71F03028DDDC9" 5120     2019-08-12 08:56:48Z
```

<span data-ttu-id="17d56-116">이 명령은 저장소 계정 개체와 컨테이너 이름이 있는 저장소 blob 컨테이너를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="17d56-116">This command gets a Storage blob container with Storage account object and container name.</span></span>

## <span data-ttu-id="17d56-117">변수</span><span class="sxs-lookup"><span data-stu-id="17d56-117">PARAMETERS</span></span>

### <span data-ttu-id="17d56-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17d56-118">-DefaultProfile</span></span>
<span data-ttu-id="17d56-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="17d56-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17d56-120">-이름</span><span class="sxs-lookup"><span data-stu-id="17d56-120">-Name</span></span>
<span data-ttu-id="17d56-121">공유 이름</span><span class="sxs-lookup"><span data-stu-id="17d56-121">Share Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, ShareName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="17d56-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17d56-122">-ResourceGroupName</span></span>
<span data-ttu-id="17d56-123">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="17d56-123">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17d56-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="17d56-124">-ResourceId</span></span>
<span data-ttu-id="17d56-125">파일 공유 리소스 Id를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="17d56-125">Input a File Share Resource Id.</span></span>

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

### <span data-ttu-id="17d56-126">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="17d56-126">-StorageAccount</span></span>
<span data-ttu-id="17d56-127">저장소 계정 개체</span><span class="sxs-lookup"><span data-stu-id="17d56-127">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="17d56-128">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="17d56-128">-StorageAccountName</span></span>
<span data-ttu-id="17d56-129">저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="17d56-129">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17d56-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17d56-130">CommonParameters</span></span>
<span data-ttu-id="17d56-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="17d56-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17d56-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17d56-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17d56-133">입력</span><span class="sxs-lookup"><span data-stu-id="17d56-133">INPUTS</span></span>

### <span data-ttu-id="17d56-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="17d56-134">System.String</span></span>

### <span data-ttu-id="17d56-135">Microsoft. Azure.. i m a. 모델. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="17d56-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="17d56-136">출력</span><span class="sxs-lookup"><span data-stu-id="17d56-136">OUTPUTS</span></span>

### <span data-ttu-id="17d56-137">Microsoft. i. m a i 공유.</span><span class="sxs-lookup"><span data-stu-id="17d56-137">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="17d56-138">상속자</span><span class="sxs-lookup"><span data-stu-id="17d56-138">NOTES</span></span>

## <span data-ttu-id="17d56-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="17d56-139">RELATED LINKS</span></span>
