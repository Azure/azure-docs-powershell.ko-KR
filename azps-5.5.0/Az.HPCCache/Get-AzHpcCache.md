---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/get-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCache.md
ms.openlocfilehash: 82b5bdd7e10b8119a058ab3a30f6836ff9255d01
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185833"
---
# <span data-ttu-id="19e53-101">Get-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="19e53-101">Get-AzHpcCache</span></span>

## <span data-ttu-id="19e53-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19e53-102">SYNOPSIS</span></span>
<span data-ttu-id="19e53-103">캐시를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="19e53-103">Gets a cache(s).</span></span>

## <span data-ttu-id="19e53-104">구문</span><span class="sxs-lookup"><span data-stu-id="19e53-104">SYNTAX</span></span>

```
Get-AzHpcCache [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="19e53-105">설명</span><span class="sxs-lookup"><span data-stu-id="19e53-105">DESCRIPTION</span></span>
<span data-ttu-id="19e53-106">**Get-AzHpcCache** cmdlet은 특정 리소스 그룹의 단일 캐시, 캐시 또는 구독 전체 캐시 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="19e53-106">The **Get-AzHpcCache** cmdlet gets a single cache, cache(s) in a specific resource group, or subscription wide list of caches.</span></span>

## <span data-ttu-id="19e53-107">예제</span><span class="sxs-lookup"><span data-stu-id="19e53-107">EXAMPLES</span></span>

### <span data-ttu-id="19e53-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="19e53-108">Example 1</span></span>
```powershell
PS C:\> Get-AzHPCCache -ResourceGroupName rgtest -CacheName cachetest
```

### <span data-ttu-id="19e53-109">예제 2</span><span class="sxs-lookup"><span data-stu-id="19e53-109">Example 2</span></span>
```powershell
PS C:\> Get-AzHPCCache -ResourceGroupName rgtest
```

### <span data-ttu-id="19e53-110">예제 3</span><span class="sxs-lookup"><span data-stu-id="19e53-110">Example 3</span></span>
```powershell
PS C:\> Get-AzHPCCache
```

## <span data-ttu-id="19e53-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="19e53-111">PARAMETERS</span></span>

### <span data-ttu-id="19e53-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19e53-112">-DefaultProfile</span></span>
<span data-ttu-id="19e53-113">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="19e53-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="19e53-114">-Name</span><span class="sxs-lookup"><span data-stu-id="19e53-114">-Name</span></span>
<span data-ttu-id="19e53-115">특정 캐시의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="19e53-115">Name of specific cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CacheName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19e53-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19e53-116">-ResourceGroupName</span></span>
<span data-ttu-id="19e53-117">캐시를 나열하려는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="19e53-117">Name of resource group under which you want to list cache(s).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19e53-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19e53-118">CommonParameters</span></span>
<span data-ttu-id="19e53-119">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="19e53-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19e53-120">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="19e53-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19e53-121">입력</span><span class="sxs-lookup"><span data-stu-id="19e53-121">INPUTS</span></span>

### <span data-ttu-id="19e53-122">System.String</span><span class="sxs-lookup"><span data-stu-id="19e53-122">System.String</span></span>

## <span data-ttu-id="19e53-123">출력</span><span class="sxs-lookup"><span data-stu-id="19e53-123">OUTPUTS</span></span>

### <span data-ttu-id="19e53-124">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache</span><span class="sxs-lookup"><span data-stu-id="19e53-124">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache</span></span>

## <span data-ttu-id="19e53-125">참고 사항</span><span class="sxs-lookup"><span data-stu-id="19e53-125">NOTES</span></span>

## <span data-ttu-id="19e53-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="19e53-126">RELATED LINKS</span></span>
