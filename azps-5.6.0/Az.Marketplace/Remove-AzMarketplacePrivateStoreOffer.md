---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Marketplace.dll-Help.xml
Module Name: Az.Marketplace
online version: https://docs.microsoft.com/powershell/module/az.marketplace/remove-azmarketplaceprivatestoreoffer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Remove-AzMarketplacePrivateStoreOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Remove-AzMarketplacePrivateStoreOffer.md
ms.openlocfilehash: 829f6b4e95e1d45d68f12ed6dbd8ad7c7987eba3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003760"
---
# <span data-ttu-id="e16a1-101">Remove-AzMarketplacePrivateStoreOffer</span><span class="sxs-lookup"><span data-stu-id="e16a1-101">Remove-AzMarketplacePrivateStoreOffer</span></span>

## <span data-ttu-id="e16a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e16a1-102">SYNOPSIS</span></span>
<span data-ttu-id="e16a1-103">개인 저장소에서 제안을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e16a1-103">Remove an offer from private store.</span></span>

## <span data-ttu-id="e16a1-104">구문</span><span class="sxs-lookup"><span data-stu-id="e16a1-104">SYNTAX</span></span>

```
Remove-AzMarketplacePrivateStoreOffer -PrivateStoreId <String> -OfferId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e16a1-105">설명</span><span class="sxs-lookup"><span data-stu-id="e16a1-105">DESCRIPTION</span></span>
<span data-ttu-id="e16a1-106">테넌트 범위에서 만든 개인 저장소에서 제안을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e16a1-106">Remove an offer from private store that was created in tenant scope.</span></span>

## <span data-ttu-id="e16a1-107">예제</span><span class="sxs-lookup"><span data-stu-id="e16a1-107">EXAMPLES</span></span>

### <span data-ttu-id="e16a1-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="e16a1-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzMarketplacePrivateStoreOffer -privateStoreId 7gh67884-1r56-44fb-a93d-030d4ae08b2d -offerId  publisherid.offerid
```

<span data-ttu-id="e16a1-109">테넌트 범위에서 만든 개인 저장소에서 제안을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e16a1-109">Remove an offer from private store that was created in tenant scope.</span></span>

## <span data-ttu-id="e16a1-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="e16a1-110">PARAMETERS</span></span>

### <span data-ttu-id="e16a1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e16a1-111">-DefaultProfile</span></span>
<span data-ttu-id="e16a1-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e16a1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e16a1-113">-OfferId</span><span class="sxs-lookup"><span data-stu-id="e16a1-113">-OfferId</span></span>
<span data-ttu-id="e16a1-114">필수 Azure Marketplace privateStore 제품</span><span class="sxs-lookup"><span data-stu-id="e16a1-114">Required Azure Marketplace privateStore offer</span></span>

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

### <span data-ttu-id="e16a1-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e16a1-115">-PassThru</span></span>
<span data-ttu-id="e16a1-116">{{ Fill PassThru 설명 }}</span><span class="sxs-lookup"><span data-stu-id="e16a1-116">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="e16a1-117">-PrivateStoreId</span><span class="sxs-lookup"><span data-stu-id="e16a1-117">-PrivateStoreId</span></span>
<span data-ttu-id="e16a1-118">필수 Azure Marketplace privateStore</span><span class="sxs-lookup"><span data-stu-id="e16a1-118">Required Azure Marketplace privateStore</span></span>

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

### <span data-ttu-id="e16a1-119">-확인</span><span class="sxs-lookup"><span data-stu-id="e16a1-119">-Confirm</span></span>
<span data-ttu-id="e16a1-120">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e16a1-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e16a1-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e16a1-121">-WhatIf</span></span>
<span data-ttu-id="e16a1-122">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="e16a1-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e16a1-123">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e16a1-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e16a1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e16a1-124">CommonParameters</span></span>
<span data-ttu-id="e16a1-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e16a1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e16a1-126">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e16a1-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e16a1-127">입력</span><span class="sxs-lookup"><span data-stu-id="e16a1-127">INPUTS</span></span>

### <span data-ttu-id="e16a1-128">없음</span><span class="sxs-lookup"><span data-stu-id="e16a1-128">None</span></span>

## <span data-ttu-id="e16a1-129">출력</span><span class="sxs-lookup"><span data-stu-id="e16a1-129">OUTPUTS</span></span>

### <span data-ttu-id="e16a1-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e16a1-130">System.Boolean</span></span>

## <span data-ttu-id="e16a1-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e16a1-131">NOTES</span></span>

## <span data-ttu-id="e16a1-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e16a1-132">RELATED LINKS</span></span>
