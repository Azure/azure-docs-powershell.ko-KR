---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azrmstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainer.md
ms.openlocfilehash: da0ccdc791318f0a315bea8d2464d8d0852aec8b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98325100"
---
# <span data-ttu-id="54995-101">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="54995-101">Get-AzRmStorageContainer</span></span>

## <span data-ttu-id="54995-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54995-102">SYNOPSIS</span></span>
<span data-ttu-id="54995-103">Storage Blob 컨테이너를 얻거나 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="54995-103">Gets or lists Storage blob containers</span></span>

## <span data-ttu-id="54995-104">구문</span><span class="sxs-lookup"><span data-stu-id="54995-104">SYNTAX</span></span>

### <span data-ttu-id="54995-105">AccountName(기본값)</span><span class="sxs-lookup"><span data-stu-id="54995-105">AccountName (Default)</span></span>
```
Get-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="54995-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="54995-106">AccountObject</span></span>
```
Get-AzRmStorageContainer -StorageAccount <PSStorageAccount> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="54995-107">설명</span><span class="sxs-lookup"><span data-stu-id="54995-107">DESCRIPTION</span></span>
<span data-ttu-id="54995-108">**Get-AzRmStorageContainer** cmdlet은 Storage Blob 컨테이너를 얻거나 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="54995-108">The **Get-AzRmStorageContainer** cmdlet gets or lists  Storage blob containers</span></span>

## <span data-ttu-id="54995-109">예제</span><span class="sxs-lookup"><span data-stu-id="54995-109">EXAMPLES</span></span>

### <span data-ttu-id="54995-110">예제 1: Storage 계정 이름 및 컨테이너 이름을 통해 Storage Blob 컨테이너를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="54995-110">Example 1: Get a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Get-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
```

<span data-ttu-id="54995-111">이 명령은 Storage 계정 이름 및 컨테이너 이름이 있는 Storage Blob 컨테이너를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="54995-111">This command gets a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="54995-112">예제 2: Storage 계정의 모든 Storage Blob 컨테이너 나열</span><span class="sxs-lookup"><span data-stu-id="54995-112">Example 2: List  all Storage blob containers of a Storage account</span></span>
```
PS C:\>Get-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
```

<span data-ttu-id="54995-113">이 명령은 Storage 계정 이름을 사용하여 Storage 계정의 모든 Storage Blob 컨테이너를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="54995-113">This command lists all Storage blob containers of a Storage account with Storage account name.</span></span>

### <span data-ttu-id="54995-114">예제 3: Storage 계정 개체 및 컨테이너 이름이 있는 Storage Blob 컨테이너를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="54995-114">Example 3: Get a Storage blob container with Storage account object and container name.</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Get-AzRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer"
```

<span data-ttu-id="54995-115">이 명령은 Storage 계정 개체 및 컨테이너 이름이 있는 Storage Blob 컨테이너를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="54995-115">This command gets a Storage blob container with Storage account object and container name.</span></span>

## <span data-ttu-id="54995-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="54995-116">PARAMETERS</span></span>

### <span data-ttu-id="54995-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="54995-117">-AsJob</span></span>
<span data-ttu-id="54995-118">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="54995-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="54995-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54995-119">-DefaultProfile</span></span>
<span data-ttu-id="54995-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="54995-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="54995-121">-Name</span><span class="sxs-lookup"><span data-stu-id="54995-121">-Name</span></span>
<span data-ttu-id="54995-122">컨테이너 이름</span><span class="sxs-lookup"><span data-stu-id="54995-122">Container Name</span></span>

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

### <span data-ttu-id="54995-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54995-123">-ResourceGroupName</span></span>
<span data-ttu-id="54995-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="54995-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="54995-125">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="54995-125">-StorageAccount</span></span>
<span data-ttu-id="54995-126">Storage 계정 개체</span><span class="sxs-lookup"><span data-stu-id="54995-126">Storage account object</span></span>

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

### <span data-ttu-id="54995-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="54995-127">-StorageAccountName</span></span>
<span data-ttu-id="54995-128">저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="54995-128">Storage Account Name.</span></span>

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

### <span data-ttu-id="54995-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54995-129">CommonParameters</span></span>
<span data-ttu-id="54995-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="54995-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54995-131">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="54995-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54995-132">입력</span><span class="sxs-lookup"><span data-stu-id="54995-132">INPUTS</span></span>

### <span data-ttu-id="54995-133">System.String</span><span class="sxs-lookup"><span data-stu-id="54995-133">System.String</span></span>

### <span data-ttu-id="54995-134">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="54995-134">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="54995-135">출력</span><span class="sxs-lookup"><span data-stu-id="54995-135">OUTPUTS</span></span>

### <span data-ttu-id="54995-136">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="54995-136">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="54995-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="54995-137">NOTES</span></span>

## <span data-ttu-id="54995-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="54995-138">RELATED LINKS</span></span>
