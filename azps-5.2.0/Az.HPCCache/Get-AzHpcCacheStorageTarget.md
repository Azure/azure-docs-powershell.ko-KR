---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/get-azhpccachestoragetarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCacheStorageTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCacheStorageTarget.md
ms.openlocfilehash: c32b47b7300c7da0a6517ca5e3802af60bd0f571
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98328229"
---
# <span data-ttu-id="fd66b-101">Get-AzHpcCacheStorageTarget</span><span class="sxs-lookup"><span data-stu-id="fd66b-101">Get-AzHpcCacheStorageTarget</span></span>

## <span data-ttu-id="fd66b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd66b-102">SYNOPSIS</span></span>
<span data-ttu-id="fd66b-103">HPC 캐시 저장소 대상을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="fd66b-103">Get HPC cache storage target(s).</span></span>

## <span data-ttu-id="fd66b-104">구문</span><span class="sxs-lookup"><span data-stu-id="fd66b-104">SYNTAX</span></span>

### <span data-ttu-id="fd66b-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="fd66b-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fd66b-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd66b-106">ByResourceIdParameterSet</span></span>
```
Get-AzHpcCacheStorageTarget -CacheId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fd66b-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd66b-107">ByObjectParameterSet</span></span>
```
Get-AzHpcCacheStorageTarget -CacheObject <PSHPCCache> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fd66b-108">설명</span><span class="sxs-lookup"><span data-stu-id="fd66b-108">DESCRIPTION</span></span>
<span data-ttu-id="fd66b-109">**Get-AzHpcCacheStorageTarget** cmdlet은 캐시에 있는 저장소 대상을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="fd66b-109">The **Get-AzHpcCacheStorageTarget** cmdlet gets storage target(s) that exist on cache.</span></span>

## <span data-ttu-id="fd66b-110">예제</span><span class="sxs-lookup"><span data-stu-id="fd66b-110">EXAMPLES</span></span>

### <span data-ttu-id="fd66b-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="fd66b-111">Example 1</span></span>
```powershell
PS C:\> Get-AzHpcCacheStorageTarget -ResourceGroupName rgTest -CacheName cacheTest
```

### <span data-ttu-id="fd66b-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="fd66b-112">Example 2</span></span>
```powershell
PS C:\> Get-AzHpcCacheStorageTarget -ResourceGroupName rgTest -CacheName cacheTest -StorageTargetName stTest
```

## <span data-ttu-id="fd66b-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fd66b-113">PARAMETERS</span></span>

### <span data-ttu-id="fd66b-114">-CacheId</span><span class="sxs-lookup"><span data-stu-id="fd66b-114">-CacheId</span></span>
<span data-ttu-id="fd66b-115">캐시의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="fd66b-115">The resource id of the Cache</span></span>

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

### <span data-ttu-id="fd66b-116">-CacheName</span><span class="sxs-lookup"><span data-stu-id="fd66b-116">-CacheName</span></span>
<span data-ttu-id="fd66b-117">캐시의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fd66b-117">Name of cache.</span></span>

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

### <span data-ttu-id="fd66b-118">-CacheObject</span><span class="sxs-lookup"><span data-stu-id="fd66b-118">-CacheObject</span></span>
<span data-ttu-id="fd66b-119">시작할 캐시 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="fd66b-119">The cache object to start.</span></span>

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

### <span data-ttu-id="fd66b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd66b-120">-DefaultProfile</span></span>
<span data-ttu-id="fd66b-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fd66b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd66b-122">-Name</span><span class="sxs-lookup"><span data-stu-id="fd66b-122">-Name</span></span>
<span data-ttu-id="fd66b-123">저장소 대상의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fd66b-123">Name of storage target.</span></span>

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

### <span data-ttu-id="fd66b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd66b-124">-ResourceGroupName</span></span>
<span data-ttu-id="fd66b-125">리소스 그룹 캐시의 이름이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fd66b-125">Name of resource group cache is in.</span></span>


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

### <span data-ttu-id="fd66b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd66b-126">CommonParameters</span></span>
<span data-ttu-id="fd66b-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="fd66b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd66b-128">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="fd66b-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd66b-129">입력</span><span class="sxs-lookup"><span data-stu-id="fd66b-129">INPUTS</span></span>

### <span data-ttu-id="fd66b-130">System.String</span><span class="sxs-lookup"><span data-stu-id="fd66b-130">System.String</span></span>

## <span data-ttu-id="fd66b-131">출력</span><span class="sxs-lookup"><span data-stu-id="fd66b-131">OUTPUTS</span></span>

### <span data-ttu-id="fd66b-132">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHpcStorageTarget</span><span class="sxs-lookup"><span data-stu-id="fd66b-132">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHpcStorageTarget</span></span>

## <span data-ttu-id="fd66b-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="fd66b-133">NOTES</span></span>

## <span data-ttu-id="fd66b-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fd66b-134">RELATED LINKS</span></span>
