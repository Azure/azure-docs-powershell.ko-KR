---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azcomputeresourcesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzComputeResourceSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzComputeResourceSku.md
ms.openlocfilehash: e3c33fb3d61479531303389defb0d7ebdbb3fb64
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93697482"
---
# <span data-ttu-id="15f75-101">Get-AzComputeResourceSku</span><span class="sxs-lookup"><span data-stu-id="15f75-101">Get-AzComputeResourceSku</span></span>

## <span data-ttu-id="15f75-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="15f75-102">SYNOPSIS</span></span>
<span data-ttu-id="15f75-103">모든 계산 자원 Sku 나열</span><span class="sxs-lookup"><span data-stu-id="15f75-103">List all compute resource Skus</span></span>

## <span data-ttu-id="15f75-104">구문과</span><span class="sxs-lookup"><span data-stu-id="15f75-104">SYNTAX</span></span>

```
Get-AzComputeResourceSku [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="15f75-105">설명은</span><span class="sxs-lookup"><span data-stu-id="15f75-105">DESCRIPTION</span></span>
<span data-ttu-id="15f75-106">모든 계산 자원 Sku 나열</span><span class="sxs-lookup"><span data-stu-id="15f75-106">List all compute resource Skus</span></span>

## <span data-ttu-id="15f75-107">예제의</span><span class="sxs-lookup"><span data-stu-id="15f75-107">EXAMPLES</span></span>

### <span data-ttu-id="15f75-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="15f75-108">Example 1</span></span>
```
PS C:\> PS C:\> Get-AzComputeResourceSku | where {$_.Locations.Contains("westus")};
```

<span data-ttu-id="15f75-109">미국 지역에 모든 계산 자원 sku 나열</span><span class="sxs-lookup"><span data-stu-id="15f75-109">List all compute resource skus in West US region</span></span>

## <span data-ttu-id="15f75-110">변수</span><span class="sxs-lookup"><span data-stu-id="15f75-110">PARAMETERS</span></span>

### <span data-ttu-id="15f75-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15f75-111">-DefaultProfile</span></span>
<span data-ttu-id="15f75-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="15f75-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="15f75-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15f75-113">CommonParameters</span></span>
<span data-ttu-id="15f75-114">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="15f75-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15f75-115">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="15f75-115">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15f75-116">입력</span><span class="sxs-lookup"><span data-stu-id="15f75-116">INPUTS</span></span>

### <span data-ttu-id="15f75-117">않아야</span><span class="sxs-lookup"><span data-stu-id="15f75-117">None</span></span>

## <span data-ttu-id="15f75-118">출력</span><span class="sxs-lookup"><span data-stu-id="15f75-118">OUTPUTS</span></span>

### <span data-ttu-id="15f75-119">PSResourceSku의. m a.</span><span class="sxs-lookup"><span data-stu-id="15f75-119">Microsoft.Azure.Commands.Compute.Automation.Models.PSResourceSku</span></span>

## <span data-ttu-id="15f75-120">상속자</span><span class="sxs-lookup"><span data-stu-id="15f75-120">NOTES</span></span>

## <span data-ttu-id="15f75-121">관련 링크</span><span class="sxs-lookup"><span data-stu-id="15f75-121">RELATED LINKS</span></span>
