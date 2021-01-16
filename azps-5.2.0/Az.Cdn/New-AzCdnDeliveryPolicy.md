---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdndeliverypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryPolicy.md
ms.openlocfilehash: a00e8d11868ae487357f1105d2bc2ae3934a9db9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98368474"
---
# <span data-ttu-id="95939-101">New-AzCdnDeliveryPolicy</span><span class="sxs-lookup"><span data-stu-id="95939-101">New-AzCdnDeliveryPolicy</span></span>

## <span data-ttu-id="95939-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95939-102">SYNOPSIS</span></span>
<span data-ttu-id="95939-103">배달 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="95939-103">Creates a delivery policy.</span></span>

## <span data-ttu-id="95939-104">구문</span><span class="sxs-lookup"><span data-stu-id="95939-104">SYNTAX</span></span>

```
New-AzCdnDeliveryPolicy [-Description <String>] -Rule <PSDeliveryRule[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="95939-105">설명</span><span class="sxs-lookup"><span data-stu-id="95939-105">DESCRIPTION</span></span>
<span data-ttu-id="95939-106">**New-AzCdnDeliveryPolicy** cmdlet은 CDN 엔드포인트를 만들기 위한 배달 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="95939-106">The **New-AzCdnDeliveryPolicy** cmdlet creates a delivery policy for CDN endpoint creation.</span></span>

## <span data-ttu-id="95939-107">예제</span><span class="sxs-lookup"><span data-stu-id="95939-107">EXAMPLES</span></span>

### <span data-ttu-id="95939-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="95939-108">Example 1</span></span>
```powershell
PS C:\> New-AzCdnDeliveryPolicy -Description "Sample Policy" -Rule $rule

Description   Rules
-----------   -----
Sample Policy {rule1}
```

<span data-ttu-id="95939-109">샘플 배달 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="95939-109">Create a sample delivery policy</span></span>

## <span data-ttu-id="95939-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="95939-110">PARAMETERS</span></span>

### <span data-ttu-id="95939-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95939-111">-DefaultProfile</span></span>
<span data-ttu-id="95939-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="95939-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="95939-113">-Description</span><span class="sxs-lookup"><span data-stu-id="95939-113">-Description</span></span>
<span data-ttu-id="95939-114">정책 설명</span><span class="sxs-lookup"><span data-stu-id="95939-114">Description of the policy</span></span>

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

### <span data-ttu-id="95939-115">-Rule</span><span class="sxs-lookup"><span data-stu-id="95939-115">-Rule</span></span>
<span data-ttu-id="95939-116">deliveryRules 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="95939-116">A list of deliveryRules.</span></span>

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

### <span data-ttu-id="95939-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95939-117">CommonParameters</span></span>
<span data-ttu-id="95939-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="95939-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95939-119">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="95939-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95939-120">입력</span><span class="sxs-lookup"><span data-stu-id="95939-120">INPUTS</span></span>

### <span data-ttu-id="95939-121">없음</span><span class="sxs-lookup"><span data-stu-id="95939-121">None</span></span>

## <span data-ttu-id="95939-122">출력</span><span class="sxs-lookup"><span data-stu-id="95939-122">OUTPUTS</span></span>

### <span data-ttu-id="95939-123">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryPolicy</span><span class="sxs-lookup"><span data-stu-id="95939-123">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryPolicy</span></span>

## <span data-ttu-id="95939-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="95939-124">NOTES</span></span>

## <span data-ttu-id="95939-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="95939-125">RELATED LINKS</span></span>
