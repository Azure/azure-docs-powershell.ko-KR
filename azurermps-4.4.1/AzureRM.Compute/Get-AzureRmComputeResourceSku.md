---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmComputeResourceSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmComputeResourceSku.md
ms.openlocfilehash: fd4a06375a4dfab7f8b8cd4b08a2112310e99b73
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536455"
---
# <span data-ttu-id="1cac1-101">Get-AzureRmComputeResourceSku</span><span class="sxs-lookup"><span data-stu-id="1cac1-101">Get-AzureRmComputeResourceSku</span></span>

## <span data-ttu-id="1cac1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1cac1-102">SYNOPSIS</span></span>
<span data-ttu-id="1cac1-103">모든 계산 자원 Sku 나열</span><span class="sxs-lookup"><span data-stu-id="1cac1-103">List all compute resource Skus</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1cac1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1cac1-104">SYNTAX</span></span>

```
Get-AzureRmComputeResourceSku [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1cac1-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1cac1-105">DESCRIPTION</span></span>
<span data-ttu-id="1cac1-106">모든 계산 자원 Sku 나열</span><span class="sxs-lookup"><span data-stu-id="1cac1-106">List all compute resource Skus</span></span>

## <span data-ttu-id="1cac1-107">예제의</span><span class="sxs-lookup"><span data-stu-id="1cac1-107">EXAMPLES</span></span>

### <span data-ttu-id="1cac1-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="1cac1-108">Example 1</span></span>
```
PS C:\> PS C:\> Get-AzureRmComputeResourceSku | where {$_.Locations.Contains("westus")};
```

<span data-ttu-id="1cac1-109">미국 지역에 모든 계산 자원 sku 나열</span><span class="sxs-lookup"><span data-stu-id="1cac1-109">List all compute resource skus in West US region</span></span>

## <span data-ttu-id="1cac1-110">변수</span><span class="sxs-lookup"><span data-stu-id="1cac1-110">PARAMETERS</span></span>

### <span data-ttu-id="1cac1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cac1-111">-DefaultProfile</span></span>
<span data-ttu-id="1cac1-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1cac1-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cac1-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cac1-113">CommonParameters</span></span>
<span data-ttu-id="1cac1-114">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1cac1-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cac1-115">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1cac1-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cac1-116">입력</span><span class="sxs-lookup"><span data-stu-id="1cac1-116">INPUTS</span></span>

### <span data-ttu-id="1cac1-117">않아야</span><span class="sxs-lookup"><span data-stu-id="1cac1-117">None</span></span>

## <span data-ttu-id="1cac1-118">출력</span><span class="sxs-lookup"><span data-stu-id="1cac1-118">OUTPUTS</span></span>

### <span data-ttu-id="1cac1-119">System. 개체</span><span class="sxs-lookup"><span data-stu-id="1cac1-119">System.Object</span></span>

## <span data-ttu-id="1cac1-120">상속자</span><span class="sxs-lookup"><span data-stu-id="1cac1-120">NOTES</span></span>

## <span data-ttu-id="1cac1-121">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1cac1-121">RELATED LINKS</span></span>

