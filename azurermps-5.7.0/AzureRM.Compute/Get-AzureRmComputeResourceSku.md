---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmComputeResourceSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmComputeResourceSku.md
ms.openlocfilehash: b9e1c42ca3a67a80a939a4e79626253b903764f4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526991"
---
# <span data-ttu-id="5b969-101">Get-AzureRmComputeResourceSku</span><span class="sxs-lookup"><span data-stu-id="5b969-101">Get-AzureRmComputeResourceSku</span></span>

## <span data-ttu-id="5b969-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b969-102">SYNOPSIS</span></span>
<span data-ttu-id="5b969-103">모든 계산 자원 Sku 나열</span><span class="sxs-lookup"><span data-stu-id="5b969-103">List all compute resource Skus</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5b969-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5b969-104">SYNTAX</span></span>

```
Get-AzureRmComputeResourceSku [<CommonParameters>]
```

## <span data-ttu-id="5b969-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5b969-105">DESCRIPTION</span></span>
<span data-ttu-id="5b969-106">모든 계산 자원 Sku 나열</span><span class="sxs-lookup"><span data-stu-id="5b969-106">List all compute resource Skus</span></span>

## <span data-ttu-id="5b969-107">예제의</span><span class="sxs-lookup"><span data-stu-id="5b969-107">EXAMPLES</span></span>

### <span data-ttu-id="5b969-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="5b969-108">Example 1</span></span>
```
PS C:\> PS C:\> Get-AzureRmComputeResourceSku | where {$_.Locations.Contains("westus")};
```

<span data-ttu-id="5b969-109">미국 지역에 모든 계산 자원 sku 나열</span><span class="sxs-lookup"><span data-stu-id="5b969-109">List all compute resource skus in West US region</span></span>

## <span data-ttu-id="5b969-110">변수</span><span class="sxs-lookup"><span data-stu-id="5b969-110">PARAMETERS</span></span>

### <span data-ttu-id="5b969-111">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b969-111">CommonParameters</span></span>
<span data-ttu-id="5b969-112">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b969-112">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b969-113">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b969-113">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b969-114">입력</span><span class="sxs-lookup"><span data-stu-id="5b969-114">INPUTS</span></span>

### <span data-ttu-id="5b969-115">않아야</span><span class="sxs-lookup"><span data-stu-id="5b969-115">None</span></span>


## <span data-ttu-id="5b969-116">출력</span><span class="sxs-lookup"><span data-stu-id="5b969-116">OUTPUTS</span></span>

### <span data-ttu-id="5b969-117">System. 개체</span><span class="sxs-lookup"><span data-stu-id="5b969-117">System.Object</span></span>

## <span data-ttu-id="5b969-118">상속자</span><span class="sxs-lookup"><span data-stu-id="5b969-118">NOTES</span></span>

## <span data-ttu-id="5b969-119">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5b969-119">RELATED LINKS</span></span>

