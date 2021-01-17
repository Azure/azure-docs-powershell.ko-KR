---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Marketplace.dll-Help.xml
Module Name: Az.Marketplace
online version: https://docs.microsoft.com/en-us/powershell/module/az.marketplace/remove-azmarketplaceprivatestoreoffer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Remove-AzMarketplacePrivateStoreOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Remove-AzMarketplacePrivateStoreOffer.md
ms.openlocfilehash: 93c7a1e580d85201465c460740e3d6e327db22aa
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98329877"
---
# <span data-ttu-id="4a75a-101">Remove-AzMarketplacePrivateStoreOffer</span><span class="sxs-lookup"><span data-stu-id="4a75a-101">Remove-AzMarketplacePrivateStoreOffer</span></span>

## <span data-ttu-id="4a75a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a75a-102">SYNOPSIS</span></span>
<span data-ttu-id="4a75a-103">개인 저장소에서 제안을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="4a75a-103">Remove an offer from private store.</span></span>

## <span data-ttu-id="4a75a-104">구문</span><span class="sxs-lookup"><span data-stu-id="4a75a-104">SYNTAX</span></span>

```
Remove-AzMarketplacePrivateStoreOffer -PrivateStoreId <String> -OfferId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a75a-105">설명</span><span class="sxs-lookup"><span data-stu-id="4a75a-105">DESCRIPTION</span></span>
<span data-ttu-id="4a75a-106">테넌트 범위에서 만든 개인 저장소에서 제안을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="4a75a-106">Remove an offer from private store that was created in tenant scope.</span></span>

## <span data-ttu-id="4a75a-107">예제</span><span class="sxs-lookup"><span data-stu-id="4a75a-107">EXAMPLES</span></span>

### <span data-ttu-id="4a75a-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="4a75a-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzMarketplacePrivateStoreOffer -privateStoreId 7gh67884-1r56-44fb-a93d-030d4ae08b2d -offerId  publisherid.offerid
```

<span data-ttu-id="4a75a-109">테넌트 범위에서 만든 개인 저장소에서 제안을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="4a75a-109">Remove an offer from private store that was created in tenant scope.</span></span>

## <span data-ttu-id="4a75a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4a75a-110">PARAMETERS</span></span>

### <span data-ttu-id="4a75a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a75a-111">-DefaultProfile</span></span>
<span data-ttu-id="4a75a-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4a75a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a75a-113">-OfferId</span><span class="sxs-lookup"><span data-stu-id="4a75a-113">-OfferId</span></span>
<span data-ttu-id="4a75a-114">필수 Azure Marketplace privateStore 제품</span><span class="sxs-lookup"><span data-stu-id="4a75a-114">Required Azure Marketplace privateStore offer</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a75a-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4a75a-115">-PassThru</span></span>
<span data-ttu-id="4a75a-116">{{ PassThru 설명 채우기 }}</span><span class="sxs-lookup"><span data-stu-id="4a75a-116">{{ Fill PassThru Description }}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a75a-117">-PrivateStoreId</span><span class="sxs-lookup"><span data-stu-id="4a75a-117">-PrivateStoreId</span></span>
<span data-ttu-id="4a75a-118">필수 Azure Marketplace privateStore</span><span class="sxs-lookup"><span data-stu-id="4a75a-118">Required Azure Marketplace privateStore</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a75a-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4a75a-119">-Confirm</span></span>
<span data-ttu-id="4a75a-120">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4a75a-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a75a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a75a-121">-WhatIf</span></span>
<span data-ttu-id="4a75a-122">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="4a75a-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4a75a-123">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4a75a-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a75a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a75a-124">CommonParameters</span></span>
<span data-ttu-id="4a75a-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4a75a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a75a-126">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4a75a-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a75a-127">입력</span><span class="sxs-lookup"><span data-stu-id="4a75a-127">INPUTS</span></span>

### <span data-ttu-id="4a75a-128">없음</span><span class="sxs-lookup"><span data-stu-id="4a75a-128">None</span></span>

## <span data-ttu-id="4a75a-129">출력</span><span class="sxs-lookup"><span data-stu-id="4a75a-129">OUTPUTS</span></span>

### <span data-ttu-id="4a75a-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4a75a-130">System.Boolean</span></span>

## <span data-ttu-id="4a75a-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4a75a-131">NOTES</span></span>

## <span data-ttu-id="4a75a-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4a75a-132">RELATED LINKS</span></span>
