---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azrmstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: 2a1dee58ba741e5bd1c1122b704c5d62666338f2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98376279"
---
# <span data-ttu-id="4f381-101">Get-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="4f381-101">Get-AzRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="4f381-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f381-102">SYNOPSIS</span></span>
<span data-ttu-id="4f381-103">Storage Blob 컨테이너의 ImmutabilityPolicy를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4f381-103">Gets ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="4f381-104">구문</span><span class="sxs-lookup"><span data-stu-id="4f381-104">SYNTAX</span></span>

### <span data-ttu-id="4f381-105">AccountName(기본값)</span><span class="sxs-lookup"><span data-stu-id="4f381-105">AccountName (Default)</span></span>
```
Get-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4f381-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="4f381-106">AccountObject</span></span>
```
Get-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4f381-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="4f381-107">ContainerObject</span></span>
```
Get-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4f381-108">설명</span><span class="sxs-lookup"><span data-stu-id="4f381-108">DESCRIPTION</span></span>
<span data-ttu-id="4f381-109">**Get-AzRmStorageContainerImmutabilityPolicy** cmdlet은 Storage Blob 컨테이너의 ImmutabilityPolicy를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4f381-109">The **Get-AzRmStorageContainerImmutabilityPolicy** cmdlet gets ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="4f381-110">예제</span><span class="sxs-lookup"><span data-stu-id="4f381-110">EXAMPLES</span></span>

### <span data-ttu-id="4f381-111">예제 1: Storage 계정 이름 및 컨테이너 이름이 있는 Storage Blob 컨테이너의 ImmutabilityPolicy를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4f381-111">Example 1: Get ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
```

<span data-ttu-id="4f381-112">이 명령은 Storage 계정 이름 및 컨테이너 이름을 사용하여 Storage Blob 컨테이너의 ImmutabilityPolicy를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4f381-112">This command gets ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="4f381-113">예제 2: Storage 계정 개체 및 컨테이너 이름을 통해 Storage Blob 컨테이너의 ImmutabilityPolicy를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4f381-113">Example 2: Get ImmutabilityPolicy of a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
```

<span data-ttu-id="4f381-114">이 명령은 Storage 계정 개체 및 컨테이너 이름을 사용하여 Storage Blob 컨테이너의 ImmutabilityPolicy를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4f381-114">This command gets ImmutabilityPolicy of a Storage blob containers with Storage account object and container name.</span></span>

### <span data-ttu-id="4f381-115">예제 3: Storage 컨테이너 개체를 통해 Storage Blob 컨테이너의 ImmutabilityPolicy를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4f381-115">Example 3: Get ImmutabilityPolicy of a Storage blob container with Storage container object</span></span>
```
PS C:\>$containerObject = Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -Container $containerObject
```

<span data-ttu-id="4f381-116">이 명령은 Storage 컨테이너 개체를 사용하여 Storage Blob 컨테이너의 ImmutabilityPolicy를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4f381-116">This command gets ImmutabilityPolicy of a Storage blob container with Storage container object.</span></span>

## <span data-ttu-id="4f381-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4f381-117">PARAMETERS</span></span>

### <span data-ttu-id="4f381-118">-Container</span><span class="sxs-lookup"><span data-stu-id="4f381-118">-Container</span></span>
<span data-ttu-id="4f381-119">저장소 컨테이너 개체</span><span class="sxs-lookup"><span data-stu-id="4f381-119">Storage container object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSContainer
Parameter Sets: ContainerObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4f381-120">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="4f381-120">-ContainerName</span></span>
<span data-ttu-id="4f381-121">컨테이너 이름</span><span class="sxs-lookup"><span data-stu-id="4f381-121">Container Name</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases: N

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4f381-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f381-122">-DefaultProfile</span></span>
<span data-ttu-id="4f381-123">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4f381-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4f381-124">-Etag</span><span class="sxs-lookup"><span data-stu-id="4f381-124">-Etag</span></span>
<span data-ttu-id="4f381-125">몰입성 정책 etag입니다.</span><span class="sxs-lookup"><span data-stu-id="4f381-125">Immutability policy etag.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IfMatch

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f381-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f381-126">-ResourceGroupName</span></span>
<span data-ttu-id="4f381-127">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4f381-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="4f381-128">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="4f381-128">-StorageAccount</span></span>
<span data-ttu-id="4f381-129">Storage 계정 개체</span><span class="sxs-lookup"><span data-stu-id="4f381-129">Storage account object</span></span>

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

### <span data-ttu-id="4f381-130">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="4f381-130">-StorageAccountName</span></span>
<span data-ttu-id="4f381-131">저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4f381-131">Storage Account Name.</span></span>

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

### <span data-ttu-id="4f381-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f381-132">CommonParameters</span></span>
<span data-ttu-id="4f381-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4f381-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f381-134">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="4f381-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f381-135">입력</span><span class="sxs-lookup"><span data-stu-id="4f381-135">INPUTS</span></span>

### <span data-ttu-id="4f381-136">System.String</span><span class="sxs-lookup"><span data-stu-id="4f381-136">System.String</span></span>

### <span data-ttu-id="4f381-137">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4f381-137">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="4f381-138">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="4f381-138">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="4f381-139">출력</span><span class="sxs-lookup"><span data-stu-id="4f381-139">OUTPUTS</span></span>

### <span data-ttu-id="4f381-140">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="4f381-140">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="4f381-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4f381-141">NOTES</span></span>

## <span data-ttu-id="4f381-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4f381-142">RELATED LINKS</span></span>
