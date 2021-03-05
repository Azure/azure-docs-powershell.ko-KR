---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/powershell/module/az.cdn/new-azcdndeliverypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryPolicy.md
ms.openlocfilehash: 01cadd267a98cab239b7a83357d308d8dd2d32bd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001840"
---
# <span data-ttu-id="080c8-101">New-AzCdnDeliveryPolicy</span><span class="sxs-lookup"><span data-stu-id="080c8-101">New-AzCdnDeliveryPolicy</span></span>

## <span data-ttu-id="080c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="080c8-102">SYNOPSIS</span></span>
<span data-ttu-id="080c8-103">배달 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="080c8-103">Creates a delivery policy.</span></span>

## <span data-ttu-id="080c8-104">구문</span><span class="sxs-lookup"><span data-stu-id="080c8-104">SYNTAX</span></span>

```
New-AzCdnDeliveryPolicy [-Description <String>] -Rule <PSDeliveryRule[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="080c8-105">설명</span><span class="sxs-lookup"><span data-stu-id="080c8-105">DESCRIPTION</span></span>
<span data-ttu-id="080c8-106">**New-AzCdnDeliveryPolicy** cmdlet은 CDN 엔드포인트 만들기에 대한 배달 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="080c8-106">The **New-AzCdnDeliveryPolicy** cmdlet creates a delivery policy for CDN endpoint creation.</span></span>

## <span data-ttu-id="080c8-107">예제</span><span class="sxs-lookup"><span data-stu-id="080c8-107">EXAMPLES</span></span>

### <span data-ttu-id="080c8-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="080c8-108">Example 1</span></span>
```powershell
PS C:\> New-AzCdnDeliveryPolicy -Description "Sample Policy" -Rule $rule

Description   Rules
-----------   -----
Sample Policy {rule1}
```

<span data-ttu-id="080c8-109">샘플 배달 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="080c8-109">Create a sample delivery policy</span></span>

## <span data-ttu-id="080c8-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="080c8-110">PARAMETERS</span></span>

### <span data-ttu-id="080c8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="080c8-111">-DefaultProfile</span></span>
<span data-ttu-id="080c8-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="080c8-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="080c8-113">-Description</span><span class="sxs-lookup"><span data-stu-id="080c8-113">-Description</span></span>
<span data-ttu-id="080c8-114">정책에 대한 설명</span><span class="sxs-lookup"><span data-stu-id="080c8-114">Description of the policy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="080c8-115">-Rule</span><span class="sxs-lookup"><span data-stu-id="080c8-115">-Rule</span></span>
<span data-ttu-id="080c8-116">deliveryRules의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="080c8-116">A list of deliveryRules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="080c8-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="080c8-117">CommonParameters</span></span>
<span data-ttu-id="080c8-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="080c8-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="080c8-119">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="080c8-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="080c8-120">입력</span><span class="sxs-lookup"><span data-stu-id="080c8-120">INPUTS</span></span>

### <span data-ttu-id="080c8-121">없음</span><span class="sxs-lookup"><span data-stu-id="080c8-121">None</span></span>

## <span data-ttu-id="080c8-122">출력</span><span class="sxs-lookup"><span data-stu-id="080c8-122">OUTPUTS</span></span>

### <span data-ttu-id="080c8-123">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryPolicy</span><span class="sxs-lookup"><span data-stu-id="080c8-123">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryPolicy</span></span>

## <span data-ttu-id="080c8-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="080c8-124">NOTES</span></span>

## <span data-ttu-id="080c8-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="080c8-125">RELATED LINKS</span></span>
