---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azrmstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainer.md
ms.openlocfilehash: aa2a03355431f027a9efd374f5af45199cc77452
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93874098"
---
# <span data-ttu-id="c9188-101">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="c9188-101">Get-AzRmStorageContainer</span></span>

## <span data-ttu-id="c9188-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9188-102">SYNOPSIS</span></span>
<span data-ttu-id="c9188-103">저장소 blob 컨테이너를 가져오거나 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9188-103">Gets or lists Storage blob containers</span></span>

## <span data-ttu-id="c9188-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c9188-104">SYNTAX</span></span>

### <span data-ttu-id="c9188-105">AccountName (기본값)</span><span class="sxs-lookup"><span data-stu-id="c9188-105">AccountName (Default)</span></span>
```
Get-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c9188-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="c9188-106">AccountObject</span></span>
```
Get-AzRmStorageContainer -StorageAccount <PSStorageAccount> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c9188-107">설명은</span><span class="sxs-lookup"><span data-stu-id="c9188-107">DESCRIPTION</span></span>
<span data-ttu-id="c9188-108">**Get-AzRmStorageContainer** Cmdlet은 저장소 blob 컨테이너를 가져오거나 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9188-108">The **Get-AzRmStorageContainer** cmdlet gets or lists  Storage blob containers</span></span>

## <span data-ttu-id="c9188-109">예제의</span><span class="sxs-lookup"><span data-stu-id="c9188-109">EXAMPLES</span></span>

### <span data-ttu-id="c9188-110">예제 1: 저장소 계정 이름과 컨테이너 이름을 사용 하 여 저장소 blob 컨테이너 가져오기</span><span class="sxs-lookup"><span data-stu-id="c9188-110">Example 1: Get a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Get-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
```

<span data-ttu-id="c9188-111">이 명령은 저장소 계정 이름과 컨테이너 이름이 있는 저장소 blob 컨테이너를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c9188-111">This command gets a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="c9188-112">예제 2: 저장소 계정의 모든 저장소 blob 컨테이너 나열</span><span class="sxs-lookup"><span data-stu-id="c9188-112">Example 2: List  all Storage blob containers of a Storage account</span></span>
```
PS C:\>Get-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
```

<span data-ttu-id="c9188-113">이 명령은 저장소 계정 이름이 있는 저장소 계정의 모든 저장소 blob 컨테이너를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9188-113">This command lists all Storage blob containers of a Storage account with Storage account name.</span></span>

### <span data-ttu-id="c9188-114">예제 3: 저장소 계정 개체 및 컨테이너 이름을 사용 하 여 저장소 blob 컨테이너를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c9188-114">Example 3: Get a Storage blob container with Storage account object and container name.</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Get-AzRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer"
```

<span data-ttu-id="c9188-115">이 명령은 저장소 계정 개체와 컨테이너 이름이 있는 저장소 blob 컨테이너를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c9188-115">This command gets a Storage blob container with Storage account object and container name.</span></span>

## <span data-ttu-id="c9188-116">변수</span><span class="sxs-lookup"><span data-stu-id="c9188-116">PARAMETERS</span></span>

### <span data-ttu-id="c9188-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c9188-117">-AsJob</span></span>
<span data-ttu-id="c9188-118">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="c9188-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c9188-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9188-119">-DefaultProfile</span></span>
<span data-ttu-id="c9188-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c9188-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c9188-121">-이름</span><span class="sxs-lookup"><span data-stu-id="c9188-121">-Name</span></span>
<span data-ttu-id="c9188-122">컨테이너 이름</span><span class="sxs-lookup"><span data-stu-id="c9188-122">Container Name</span></span>

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

### <span data-ttu-id="c9188-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9188-123">-ResourceGroupName</span></span>
<span data-ttu-id="c9188-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c9188-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="c9188-125">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="c9188-125">-StorageAccount</span></span>
<span data-ttu-id="c9188-126">저장소 계정 개체</span><span class="sxs-lookup"><span data-stu-id="c9188-126">Storage account object</span></span>

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

### <span data-ttu-id="c9188-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="c9188-127">-StorageAccountName</span></span>
<span data-ttu-id="c9188-128">저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c9188-128">Storage Account Name.</span></span>

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

### <span data-ttu-id="c9188-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9188-129">CommonParameters</span></span>
<span data-ttu-id="c9188-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9188-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9188-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9188-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9188-132">입력</span><span class="sxs-lookup"><span data-stu-id="c9188-132">INPUTS</span></span>

### <span data-ttu-id="c9188-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c9188-133">System.String</span></span>

### <span data-ttu-id="c9188-134">Microsoft. Azure.. i m a. 모델. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c9188-134">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="c9188-135">출력</span><span class="sxs-lookup"><span data-stu-id="c9188-135">OUTPUTS</span></span>

### <span data-ttu-id="c9188-136">Microsoft. m a. 모델. PSContainer</span><span class="sxs-lookup"><span data-stu-id="c9188-136">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="c9188-137">상속자</span><span class="sxs-lookup"><span data-stu-id="c9188-137">NOTES</span></span>

## <span data-ttu-id="c9188-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c9188-138">RELATED LINKS</span></span>
