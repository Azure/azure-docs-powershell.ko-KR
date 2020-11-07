---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azrmstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainer.md
ms.openlocfilehash: f15d9905abbc7a61dc77d4e8b28c5942126d7b14
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698692"
---
# <span data-ttu-id="029cb-101">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="029cb-101">Get-AzRmStorageContainer</span></span>

## <span data-ttu-id="029cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="029cb-102">SYNOPSIS</span></span>
<span data-ttu-id="029cb-103">저장소 blob 컨테이너를 가져오거나 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="029cb-103">Gets or lists Storage blob containers</span></span>

## <span data-ttu-id="029cb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="029cb-104">SYNTAX</span></span>

### <span data-ttu-id="029cb-105">AccountName (기본값)</span><span class="sxs-lookup"><span data-stu-id="029cb-105">AccountName (Default)</span></span>
```
Get-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="029cb-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="029cb-106">AccountObject</span></span>
```
Get-AzRmStorageContainer -StorageAccount <PSStorageAccount> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="029cb-107">설명은</span><span class="sxs-lookup"><span data-stu-id="029cb-107">DESCRIPTION</span></span>
<span data-ttu-id="029cb-108">**Get-AzRmStorageContainer** Cmdlet은 저장소 blob 컨테이너를 가져오거나 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="029cb-108">The **Get-AzRmStorageContainer** cmdlet gets or lists  Storage blob containers</span></span>

## <span data-ttu-id="029cb-109">예제의</span><span class="sxs-lookup"><span data-stu-id="029cb-109">EXAMPLES</span></span>

### <span data-ttu-id="029cb-110">예제 1: 저장소 계정 이름과 컨테이너 이름을 사용 하 여 저장소 blob 컨테이너 가져오기</span><span class="sxs-lookup"><span data-stu-id="029cb-110">Example 1: Get a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Get-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
```

<span data-ttu-id="029cb-111">이 명령은 저장소 계정 이름과 컨테이너 이름이 있는 저장소 blob 컨테이너를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="029cb-111">This command gets a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="029cb-112">예제 2: 저장소 계정의 모든 저장소 blob 컨테이너 나열</span><span class="sxs-lookup"><span data-stu-id="029cb-112">Example 2: List  all Storage blob containers of a Storage account</span></span>
```
PS C:\>Get-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
```

<span data-ttu-id="029cb-113">이 명령은 저장소 계정 이름이 있는 저장소 계정의 모든 저장소 blob 컨테이너를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="029cb-113">This command lists all Storage blob containers of a Storage account with Storage account name.</span></span>

### <span data-ttu-id="029cb-114">예제 3: 저장소 계정 개체 및 컨테이너 이름을 사용 하 여 저장소 blob 컨테이너를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="029cb-114">Example 3: Get a Storage blob container with Storage account object and container name.</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Get-AzRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer"
```

<span data-ttu-id="029cb-115">이 명령은 저장소 계정 개체와 컨테이너 이름이 있는 저장소 blob 컨테이너를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="029cb-115">This command gets a Storage blob container with Storage account object and container name.</span></span>

## <span data-ttu-id="029cb-116">변수</span><span class="sxs-lookup"><span data-stu-id="029cb-116">PARAMETERS</span></span>

### <span data-ttu-id="029cb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="029cb-117">-DefaultProfile</span></span>
<span data-ttu-id="029cb-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="029cb-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="029cb-119">-이름</span><span class="sxs-lookup"><span data-stu-id="029cb-119">-Name</span></span>
<span data-ttu-id="029cb-120">컨테이너 이름</span><span class="sxs-lookup"><span data-stu-id="029cb-120">Container Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, ContainerName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="029cb-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="029cb-121">-ResourceGroupName</span></span>
<span data-ttu-id="029cb-122">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="029cb-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="029cb-123">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="029cb-123">-StorageAccount</span></span>
<span data-ttu-id="029cb-124">저장소 계정 개체</span><span class="sxs-lookup"><span data-stu-id="029cb-124">Storage account object</span></span>

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

### <span data-ttu-id="029cb-125">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="029cb-125">-StorageAccountName</span></span>
<span data-ttu-id="029cb-126">저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="029cb-126">Storage Account Name.</span></span>

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

### <span data-ttu-id="029cb-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="029cb-127">CommonParameters</span></span>
<span data-ttu-id="029cb-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="029cb-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="029cb-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="029cb-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="029cb-130">입력</span><span class="sxs-lookup"><span data-stu-id="029cb-130">INPUTS</span></span>

### <span data-ttu-id="029cb-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="029cb-131">System.String</span></span>

### <span data-ttu-id="029cb-132">Microsoft. Azure.. i m a. 모델. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="029cb-132">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="029cb-133">출력</span><span class="sxs-lookup"><span data-stu-id="029cb-133">OUTPUTS</span></span>

### <span data-ttu-id="029cb-134">Microsoft. m a. 모델. PSContainer</span><span class="sxs-lookup"><span data-stu-id="029cb-134">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="029cb-135">상속자</span><span class="sxs-lookup"><span data-stu-id="029cb-135">NOTES</span></span>

## <span data-ttu-id="029cb-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="029cb-136">RELATED LINKS</span></span>