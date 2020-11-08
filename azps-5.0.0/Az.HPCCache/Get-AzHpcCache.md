---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/get-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCache.md
ms.openlocfilehash: 82b5bdd7e10b8119a058ab3a30f6836ff9255d01
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217818"
---
# <span data-ttu-id="eea95-101">Get-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="eea95-101">Get-AzHpcCache</span></span>

## <span data-ttu-id="eea95-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eea95-102">SYNOPSIS</span></span>
<span data-ttu-id="eea95-103">캐시를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="eea95-103">Gets a cache(s).</span></span>

## <span data-ttu-id="eea95-104">구문과</span><span class="sxs-lookup"><span data-stu-id="eea95-104">SYNTAX</span></span>

```
Get-AzHpcCache [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="eea95-105">설명은</span><span class="sxs-lookup"><span data-stu-id="eea95-105">DESCRIPTION</span></span>
<span data-ttu-id="eea95-106">**AzHpcCache** cmdlet은 단일 캐시, 특정 리소스 그룹의 캐시 또는 캐시의 구독 전체 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="eea95-106">The **Get-AzHpcCache** cmdlet gets a single cache, cache(s) in a specific resource group, or subscription wide list of caches.</span></span>

## <span data-ttu-id="eea95-107">예제의</span><span class="sxs-lookup"><span data-stu-id="eea95-107">EXAMPLES</span></span>

### <span data-ttu-id="eea95-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="eea95-108">Example 1</span></span>
```powershell
PS C:\> Get-AzHPCCache -ResourceGroupName rgtest -CacheName cachetest
```

### <span data-ttu-id="eea95-109">예제 2</span><span class="sxs-lookup"><span data-stu-id="eea95-109">Example 2</span></span>
```powershell
PS C:\> Get-AzHPCCache -ResourceGroupName rgtest
```

### <span data-ttu-id="eea95-110">예제 3</span><span class="sxs-lookup"><span data-stu-id="eea95-110">Example 3</span></span>
```powershell
PS C:\> Get-AzHPCCache
```

## <span data-ttu-id="eea95-111">변수</span><span class="sxs-lookup"><span data-stu-id="eea95-111">PARAMETERS</span></span>

### <span data-ttu-id="eea95-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eea95-112">-DefaultProfile</span></span>
<span data-ttu-id="eea95-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="eea95-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eea95-114">-이름</span><span class="sxs-lookup"><span data-stu-id="eea95-114">-Name</span></span>
<span data-ttu-id="eea95-115">특정 캐시의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="eea95-115">Name of specific cache.</span></span>

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

### <span data-ttu-id="eea95-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eea95-116">-ResourceGroupName</span></span>
<span data-ttu-id="eea95-117">캐시를 나열 하려는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="eea95-117">Name of resource group under which you want to list cache(s).</span></span>

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

### <span data-ttu-id="eea95-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eea95-118">CommonParameters</span></span>
<span data-ttu-id="eea95-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="eea95-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eea95-120">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="eea95-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eea95-121">입력</span><span class="sxs-lookup"><span data-stu-id="eea95-121">INPUTS</span></span>

### <span data-ttu-id="eea95-122">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="eea95-122">System.String</span></span>

## <span data-ttu-id="eea95-123">출력</span><span class="sxs-lookup"><span data-stu-id="eea95-123">OUTPUTS</span></span>

### <span data-ttu-id="eea95-124">Microsoft. PowerShell. a i m/PSHPCCache</span><span class="sxs-lookup"><span data-stu-id="eea95-124">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache</span></span>

## <span data-ttu-id="eea95-125">상속자</span><span class="sxs-lookup"><span data-stu-id="eea95-125">NOTES</span></span>

## <span data-ttu-id="eea95-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="eea95-126">RELATED LINKS</span></span>
