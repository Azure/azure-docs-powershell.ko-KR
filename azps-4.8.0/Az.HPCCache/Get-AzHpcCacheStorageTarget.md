---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/get-azhpccachestoragetarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCacheStorageTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCacheStorageTarget.md
ms.openlocfilehash: c32b47b7300c7da0a6517ca5e3802af60bd0f571
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056341"
---
# <span data-ttu-id="7249d-101">Get-AzHpcCacheStorageTarget</span><span class="sxs-lookup"><span data-stu-id="7249d-101">Get-AzHpcCacheStorageTarget</span></span>

## <span data-ttu-id="7249d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7249d-102">SYNOPSIS</span></span>
<span data-ttu-id="7249d-103">HPC 캐시 저장소 대상을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7249d-103">Get HPC cache storage target(s).</span></span>

## <span data-ttu-id="7249d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7249d-104">SYNTAX</span></span>

### <span data-ttu-id="7249d-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="7249d-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7249d-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7249d-106">ByResourceIdParameterSet</span></span>
```
Get-AzHpcCacheStorageTarget -CacheId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7249d-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7249d-107">ByObjectParameterSet</span></span>
```
Get-AzHpcCacheStorageTarget -CacheObject <PSHPCCache> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7249d-108">설명은</span><span class="sxs-lookup"><span data-stu-id="7249d-108">DESCRIPTION</span></span>
<span data-ttu-id="7249d-109">**AzHpcCacheStorageTarget** cmdlet은 캐시에 존재 하는 저장소 대상을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7249d-109">The **Get-AzHpcCacheStorageTarget** cmdlet gets storage target(s) that exist on cache.</span></span>

## <span data-ttu-id="7249d-110">예제의</span><span class="sxs-lookup"><span data-stu-id="7249d-110">EXAMPLES</span></span>

### <span data-ttu-id="7249d-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="7249d-111">Example 1</span></span>
```powershell
PS C:\> Get-AzHpcCacheStorageTarget -ResourceGroupName rgTest -CacheName cacheTest
```

### <span data-ttu-id="7249d-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="7249d-112">Example 2</span></span>
```powershell
PS C:\> Get-AzHpcCacheStorageTarget -ResourceGroupName rgTest -CacheName cacheTest -StorageTargetName stTest
```

## <span data-ttu-id="7249d-113">변수</span><span class="sxs-lookup"><span data-stu-id="7249d-113">PARAMETERS</span></span>

### <span data-ttu-id="7249d-114">-CacheId</span><span class="sxs-lookup"><span data-stu-id="7249d-114">-CacheId</span></span>
<span data-ttu-id="7249d-115">캐시의 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="7249d-115">The resource id of the Cache</span></span>

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

### <span data-ttu-id="7249d-116">-CacheName</span><span class="sxs-lookup"><span data-stu-id="7249d-116">-CacheName</span></span>
<span data-ttu-id="7249d-117">캐시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7249d-117">Name of cache.</span></span>

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

### <span data-ttu-id="7249d-118">-CacheObject</span><span class="sxs-lookup"><span data-stu-id="7249d-118">-CacheObject</span></span>
<span data-ttu-id="7249d-119">시작할 캐시 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="7249d-119">The cache object to start.</span></span>

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

### <span data-ttu-id="7249d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7249d-120">-DefaultProfile</span></span>
<span data-ttu-id="7249d-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7249d-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7249d-122">-이름</span><span class="sxs-lookup"><span data-stu-id="7249d-122">-Name</span></span>
<span data-ttu-id="7249d-123">저장 대상의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7249d-123">Name of storage target.</span></span>

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

### <span data-ttu-id="7249d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7249d-124">-ResourceGroupName</span></span>
<span data-ttu-id="7249d-125">리소스 그룹 캐시의 이름이 in입니다.</span><span class="sxs-lookup"><span data-stu-id="7249d-125">Name of resource group cache is in.</span></span>


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

### <span data-ttu-id="7249d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7249d-126">CommonParameters</span></span>
<span data-ttu-id="7249d-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7249d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7249d-128">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7249d-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7249d-129">입력</span><span class="sxs-lookup"><span data-stu-id="7249d-129">INPUTS</span></span>

### <span data-ttu-id="7249d-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7249d-130">System.String</span></span>

## <span data-ttu-id="7249d-131">출력</span><span class="sxs-lookup"><span data-stu-id="7249d-131">OUTPUTS</span></span>

### <span data-ttu-id="7249d-132">PSHpcStorageTarget (Microsoft. PowerShell. \*)</span><span class="sxs-lookup"><span data-stu-id="7249d-132">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHpcStorageTarget</span></span>

## <span data-ttu-id="7249d-133">상속자</span><span class="sxs-lookup"><span data-stu-id="7249d-133">NOTES</span></span>

## <span data-ttu-id="7249d-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7249d-134">RELATED LINKS</span></span>
