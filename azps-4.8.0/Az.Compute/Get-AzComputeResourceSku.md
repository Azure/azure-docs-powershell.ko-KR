---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azcomputeresourcesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzComputeResourceSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzComputeResourceSku.md
ms.openlocfilehash: 970cbb3e03a4934f648df2f6f8c06275a30740de
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048154"
---
# <span data-ttu-id="bcdf9-101">Get-AzComputeResourceSku</span><span class="sxs-lookup"><span data-stu-id="bcdf9-101">Get-AzComputeResourceSku</span></span>

## <span data-ttu-id="bcdf9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bcdf9-102">SYNOPSIS</span></span>
<span data-ttu-id="bcdf9-103">모든 계산 자원 Sku 나열</span><span class="sxs-lookup"><span data-stu-id="bcdf9-103">List all compute resource Skus</span></span>

## <span data-ttu-id="bcdf9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bcdf9-104">SYNTAX</span></span>

```
Get-AzComputeResourceSku [[-Location] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bcdf9-105">설명은</span><span class="sxs-lookup"><span data-stu-id="bcdf9-105">DESCRIPTION</span></span>
<span data-ttu-id="bcdf9-106">모든 계산 자원 Sku 나열</span><span class="sxs-lookup"><span data-stu-id="bcdf9-106">List all compute resource Skus</span></span>

## <span data-ttu-id="bcdf9-107">예제의</span><span class="sxs-lookup"><span data-stu-id="bcdf9-107">EXAMPLES</span></span>

### <span data-ttu-id="bcdf9-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="bcdf9-108">Example 1</span></span>
```
PS C:\> Get-AzComputeResourceSku "westus";
```

<span data-ttu-id="bcdf9-109">미국 지역에 모든 계산 자원 sku 나열</span><span class="sxs-lookup"><span data-stu-id="bcdf9-109">List all compute resource skus in West US region</span></span>

## <span data-ttu-id="bcdf9-110">변수</span><span class="sxs-lookup"><span data-stu-id="bcdf9-110">PARAMETERS</span></span>

### <span data-ttu-id="bcdf9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcdf9-111">-DefaultProfile</span></span>
<span data-ttu-id="bcdf9-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bcdf9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bcdf9-113">-위치</span><span class="sxs-lookup"><span data-stu-id="bcdf9-113">-Location</span></span>
<span data-ttu-id="bcdf9-114">사용할 수 있는 sku 목록의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bcdf9-114">Specifies a location of the available skus to list.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bcdf9-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcdf9-115">CommonParameters</span></span>
<span data-ttu-id="bcdf9-116">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bcdf9-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcdf9-117">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="bcdf9-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcdf9-118">입력</span><span class="sxs-lookup"><span data-stu-id="bcdf9-118">INPUTS</span></span>

### <span data-ttu-id="bcdf9-119">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="bcdf9-119">System.String</span></span>

## <span data-ttu-id="bcdf9-120">출력</span><span class="sxs-lookup"><span data-stu-id="bcdf9-120">OUTPUTS</span></span>

### <span data-ttu-id="bcdf9-121">PSResourceSku의. m a.</span><span class="sxs-lookup"><span data-stu-id="bcdf9-121">Microsoft.Azure.Commands.Compute.Automation.Models.PSResourceSku</span></span>

## <span data-ttu-id="bcdf9-122">상속자</span><span class="sxs-lookup"><span data-stu-id="bcdf9-122">NOTES</span></span>

## <span data-ttu-id="bcdf9-123">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bcdf9-123">RELATED LINKS</span></span>
