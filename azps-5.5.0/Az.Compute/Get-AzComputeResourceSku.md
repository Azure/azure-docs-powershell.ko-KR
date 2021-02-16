---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azcomputeresourcesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzComputeResourceSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzComputeResourceSku.md
ms.openlocfilehash: 970cbb3e03a4934f648df2f6f8c06275a30740de
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195057"
---
# <span data-ttu-id="766f3-101">Get-AzComputeResourceSku</span><span class="sxs-lookup"><span data-stu-id="766f3-101">Get-AzComputeResourceSku</span></span>

## <span data-ttu-id="766f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="766f3-102">SYNOPSIS</span></span>
<span data-ttu-id="766f3-103">모든 계산 리소스 SKU 나열</span><span class="sxs-lookup"><span data-stu-id="766f3-103">List all compute resource Skus</span></span>

## <span data-ttu-id="766f3-104">구문</span><span class="sxs-lookup"><span data-stu-id="766f3-104">SYNTAX</span></span>

```
Get-AzComputeResourceSku [[-Location] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="766f3-105">설명</span><span class="sxs-lookup"><span data-stu-id="766f3-105">DESCRIPTION</span></span>
<span data-ttu-id="766f3-106">모든 계산 리소스 SKU 나열</span><span class="sxs-lookup"><span data-stu-id="766f3-106">List all compute resource Skus</span></span>

## <span data-ttu-id="766f3-107">예제</span><span class="sxs-lookup"><span data-stu-id="766f3-107">EXAMPLES</span></span>

### <span data-ttu-id="766f3-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="766f3-108">Example 1</span></span>
```
PS C:\> Get-AzComputeResourceSku "westus";
```

<span data-ttu-id="766f3-109">미국 서부 지역의 모든 계산 리소스 SKU 나열</span><span class="sxs-lookup"><span data-stu-id="766f3-109">List all compute resource skus in West US region</span></span>

## <span data-ttu-id="766f3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="766f3-110">PARAMETERS</span></span>

### <span data-ttu-id="766f3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="766f3-111">-DefaultProfile</span></span>
<span data-ttu-id="766f3-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="766f3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="766f3-113">-Location</span><span class="sxs-lookup"><span data-stu-id="766f3-113">-Location</span></span>
<span data-ttu-id="766f3-114">나열할 사용 가능한 SKU의 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="766f3-114">Specifies a location of the available skus to list.</span></span>

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

### <span data-ttu-id="766f3-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="766f3-115">CommonParameters</span></span>
<span data-ttu-id="766f3-116">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="766f3-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="766f3-117">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="766f3-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="766f3-118">입력</span><span class="sxs-lookup"><span data-stu-id="766f3-118">INPUTS</span></span>

### <span data-ttu-id="766f3-119">System.String</span><span class="sxs-lookup"><span data-stu-id="766f3-119">System.String</span></span>

## <span data-ttu-id="766f3-120">출력</span><span class="sxs-lookup"><span data-stu-id="766f3-120">OUTPUTS</span></span>

### <span data-ttu-id="766f3-121">Microsoft.Azure.Commands.Compute.Automation.Models.PSResourceSku</span><span class="sxs-lookup"><span data-stu-id="766f3-121">Microsoft.Azure.Commands.Compute.Automation.Models.PSResourceSku</span></span>

## <span data-ttu-id="766f3-122">참고 사항</span><span class="sxs-lookup"><span data-stu-id="766f3-122">NOTES</span></span>

## <span data-ttu-id="766f3-123">관련 링크</span><span class="sxs-lookup"><span data-stu-id="766f3-123">RELATED LINKS</span></span>