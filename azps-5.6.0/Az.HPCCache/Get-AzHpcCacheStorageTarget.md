---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/powershell/module/az.hpccache/get-azhpccachestoragetarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCacheStorageTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCacheStorageTarget.md
ms.openlocfilehash: 6fb1e00f74bcd170d8117e4e37655da6c275a62f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988227"
---
# <span data-ttu-id="828ee-101">Get-AzHpcCacheStorageTarget</span><span class="sxs-lookup"><span data-stu-id="828ee-101">Get-AzHpcCacheStorageTarget</span></span>

## <span data-ttu-id="828ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="828ee-102">SYNOPSIS</span></span>
<span data-ttu-id="828ee-103">HPC 캐시 저장소 대상을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="828ee-103">Get HPC cache storage target(s).</span></span>

## <span data-ttu-id="828ee-104">구문</span><span class="sxs-lookup"><span data-stu-id="828ee-104">SYNTAX</span></span>

### <span data-ttu-id="828ee-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="828ee-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="828ee-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="828ee-106">ByResourceIdParameterSet</span></span>
```
Get-AzHpcCacheStorageTarget -CacheId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="828ee-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="828ee-107">ByObjectParameterSet</span></span>
```
Get-AzHpcCacheStorageTarget -CacheObject <PSHPCCache> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="828ee-108">설명</span><span class="sxs-lookup"><span data-stu-id="828ee-108">DESCRIPTION</span></span>
<span data-ttu-id="828ee-109">**Get-AzHpcCacheStorageTarget** cmdlet은 캐시에 있는 저장소 대상을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="828ee-109">The **Get-AzHpcCacheStorageTarget** cmdlet gets storage target(s) that exist on cache.</span></span>

## <span data-ttu-id="828ee-110">예제</span><span class="sxs-lookup"><span data-stu-id="828ee-110">EXAMPLES</span></span>

### <span data-ttu-id="828ee-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="828ee-111">Example 1</span></span>
```powershell
PS C:\> Get-AzHpcCacheStorageTarget -ResourceGroupName rgTest -CacheName cacheTest
```

### <span data-ttu-id="828ee-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="828ee-112">Example 2</span></span>
```powershell
PS C:\> Get-AzHpcCacheStorageTarget -ResourceGroupName rgTest -CacheName cacheTest -StorageTargetName stTest
```

## <span data-ttu-id="828ee-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="828ee-113">PARAMETERS</span></span>

### <span data-ttu-id="828ee-114">-CacheId</span><span class="sxs-lookup"><span data-stu-id="828ee-114">-CacheId</span></span>
<span data-ttu-id="828ee-115">캐시의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="828ee-115">The resource id of the Cache</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="828ee-116">-CacheName</span><span class="sxs-lookup"><span data-stu-id="828ee-116">-CacheName</span></span>
<span data-ttu-id="828ee-117">캐시의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="828ee-117">Name of cache.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="828ee-118">-CacheObject</span><span class="sxs-lookup"><span data-stu-id="828ee-118">-CacheObject</span></span>
<span data-ttu-id="828ee-119">시작할 캐시 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="828ee-119">The cache object to start.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="828ee-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="828ee-120">-DefaultProfile</span></span>
<span data-ttu-id="828ee-121">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="828ee-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="828ee-122">-Name</span><span class="sxs-lookup"><span data-stu-id="828ee-122">-Name</span></span>
<span data-ttu-id="828ee-123">저장소 대상의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="828ee-123">Name of storage target.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: StorageTargetName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="828ee-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="828ee-124">-ResourceGroupName</span></span>
<span data-ttu-id="828ee-125">리소스 그룹 캐시의 이름이 에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="828ee-125">Name of resource group cache is in.</span></span>


```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="828ee-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="828ee-126">CommonParameters</span></span>
<span data-ttu-id="828ee-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="828ee-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="828ee-128">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="828ee-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="828ee-129">입력</span><span class="sxs-lookup"><span data-stu-id="828ee-129">INPUTS</span></span>

### <span data-ttu-id="828ee-130">System.String</span><span class="sxs-lookup"><span data-stu-id="828ee-130">System.String</span></span>

## <span data-ttu-id="828ee-131">출력</span><span class="sxs-lookup"><span data-stu-id="828ee-131">OUTPUTS</span></span>

### <span data-ttu-id="828ee-132">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHpcStorageTarget</span><span class="sxs-lookup"><span data-stu-id="828ee-132">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHpcStorageTarget</span></span>

## <span data-ttu-id="828ee-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="828ee-133">NOTES</span></span>

## <span data-ttu-id="828ee-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="828ee-134">RELATED LINKS</span></span>
