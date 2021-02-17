---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/get-azhpccachesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCacheSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCacheSku.md
ms.openlocfilehash: b9b9771cb5e06b4560dc436b738425288c0ad202
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188337"
---
# <span data-ttu-id="83442-101">Get-AzHpcCacheSku</span><span class="sxs-lookup"><span data-stu-id="83442-101">Get-AzHpcCacheSku</span></span>

## <span data-ttu-id="83442-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83442-102">SYNOPSIS</span></span>
<span data-ttu-id="83442-103">구독에서 사용할 수 있는 모든 SKUS를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="83442-103">Gets all SKUs available in subscription.</span></span>

## <span data-ttu-id="83442-104">구문</span><span class="sxs-lookup"><span data-stu-id="83442-104">SYNTAX</span></span>

```
Get-AzHpcCacheSku [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="83442-105">설명</span><span class="sxs-lookup"><span data-stu-id="83442-105">DESCRIPTION</span></span>
<span data-ttu-id="83442-106">**Get-AzHpcCacheSku** cmdlet은 구독에서 사용할 수 있는 SKU 목록을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="83442-106">The **Get-AzHpcCacheSku** cmdlet returns a list of SKUs available in subscription.</span></span>

## <span data-ttu-id="83442-107">예제</span><span class="sxs-lookup"><span data-stu-id="83442-107">EXAMPLES</span></span>

### <span data-ttu-id="83442-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="83442-108">Example 1</span></span>
```powershell
PS C:\> Get-AzHpcCacheSku
```

## <span data-ttu-id="83442-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="83442-109">PARAMETERS</span></span>

### <span data-ttu-id="83442-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83442-110">-DefaultProfile</span></span>
<span data-ttu-id="83442-111">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="83442-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="83442-112">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83442-112">CommonParameters</span></span>
<span data-ttu-id="83442-113">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="83442-113">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83442-114">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="83442-114">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83442-115">입력</span><span class="sxs-lookup"><span data-stu-id="83442-115">INPUTS</span></span>

### <span data-ttu-id="83442-116">없음</span><span class="sxs-lookup"><span data-stu-id="83442-116">None</span></span>

## <span data-ttu-id="83442-117">출력</span><span class="sxs-lookup"><span data-stu-id="83442-117">OUTPUTS</span></span>

### <span data-ttu-id="83442-118">Microsoft.Azure.Commands.HPCCache.PSSku</span><span class="sxs-lookup"><span data-stu-id="83442-118">Microsoft.Azure.Commands.HPCCache.PSSku</span></span>

## <span data-ttu-id="83442-119">참고 사항</span><span class="sxs-lookup"><span data-stu-id="83442-119">NOTES</span></span>

## <span data-ttu-id="83442-120">관련 링크</span><span class="sxs-lookup"><span data-stu-id="83442-120">RELATED LINKS</span></span>
