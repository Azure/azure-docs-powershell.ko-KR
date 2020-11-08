---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/get-azhpccachesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCacheSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCacheSku.md
ms.openlocfilehash: b9b9771cb5e06b4560dc436b738425288c0ad202
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217816"
---
# <span data-ttu-id="ae944-101">Get-AzHpcCacheSku</span><span class="sxs-lookup"><span data-stu-id="ae944-101">Get-AzHpcCacheSku</span></span>

## <span data-ttu-id="ae944-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae944-102">SYNOPSIS</span></span>
<span data-ttu-id="ae944-103">구독에서 사용할 수 있는 모든 Sku를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ae944-103">Gets all SKUs available in subscription.</span></span>

## <span data-ttu-id="ae944-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ae944-104">SYNTAX</span></span>

```
Get-AzHpcCacheSku [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ae944-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ae944-105">DESCRIPTION</span></span>
<span data-ttu-id="ae944-106">**AzHpcCacheSku** cmdlet은 구독에서 사용할 수 있는 sku 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae944-106">The **Get-AzHpcCacheSku** cmdlet returns a list of SKUs available in subscription.</span></span>

## <span data-ttu-id="ae944-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ae944-107">EXAMPLES</span></span>

### <span data-ttu-id="ae944-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="ae944-108">Example 1</span></span>
```powershell
PS C:\> Get-AzHpcCacheSku
```

## <span data-ttu-id="ae944-109">변수</span><span class="sxs-lookup"><span data-stu-id="ae944-109">PARAMETERS</span></span>

### <span data-ttu-id="ae944-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae944-110">-DefaultProfile</span></span>
<span data-ttu-id="ae944-111">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ae944-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae944-112">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae944-112">CommonParameters</span></span>
<span data-ttu-id="ae944-113">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae944-113">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae944-114">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ae944-114">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae944-115">입력</span><span class="sxs-lookup"><span data-stu-id="ae944-115">INPUTS</span></span>

### <span data-ttu-id="ae944-116">않아야</span><span class="sxs-lookup"><span data-stu-id="ae944-116">None</span></span>

## <span data-ttu-id="ae944-117">출력</span><span class="sxs-lookup"><span data-stu-id="ae944-117">OUTPUTS</span></span>

### <span data-ttu-id="ae944-118">Microsoft. a HPCCache. PSSku</span><span class="sxs-lookup"><span data-stu-id="ae944-118">Microsoft.Azure.Commands.HPCCache.PSSku</span></span>

## <span data-ttu-id="ae944-119">상속자</span><span class="sxs-lookup"><span data-stu-id="ae944-119">NOTES</span></span>

## <span data-ttu-id="ae944-120">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ae944-120">RELATED LINKS</span></span>
