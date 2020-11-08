---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Marketplace.dll-Help.xml
Module Name: Az.Marketplace
online version: https://docs.microsoft.com/en-us/powershell/module/az.marketplace/remove-azmarketplaceprivatestoreoffer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Remove-AzMarketplacePrivateStoreOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Remove-AzMarketplacePrivateStoreOffer.md
ms.openlocfilehash: 93c7a1e580d85201465c460740e3d6e327db22aa
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218636"
---
# <span data-ttu-id="1aac3-101">Remove-AzMarketplacePrivateStoreOffer</span><span class="sxs-lookup"><span data-stu-id="1aac3-101">Remove-AzMarketplacePrivateStoreOffer</span></span>

## <span data-ttu-id="1aac3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1aac3-102">SYNOPSIS</span></span>
<span data-ttu-id="1aac3-103">개인 저장소에서 제안을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1aac3-103">Remove an offer from private store.</span></span>

## <span data-ttu-id="1aac3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1aac3-104">SYNTAX</span></span>

```
Remove-AzMarketplacePrivateStoreOffer -PrivateStoreId <String> -OfferId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1aac3-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1aac3-105">DESCRIPTION</span></span>
<span data-ttu-id="1aac3-106">테 넌 트 범위에서 만들어진 개인 저장소에서 제안을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1aac3-106">Remove an offer from private store that was created in tenant scope.</span></span>

## <span data-ttu-id="1aac3-107">예제의</span><span class="sxs-lookup"><span data-stu-id="1aac3-107">EXAMPLES</span></span>

### <span data-ttu-id="1aac3-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="1aac3-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzMarketplacePrivateStoreOffer -privateStoreId 7gh67884-1r56-44fb-a93d-030d4ae08b2d -offerId  publisherid.offerid
```

<span data-ttu-id="1aac3-109">테 넌 트 범위에서 만들어진 개인 저장소에서 제안을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1aac3-109">Remove an offer from private store that was created in tenant scope.</span></span>

## <span data-ttu-id="1aac3-110">변수</span><span class="sxs-lookup"><span data-stu-id="1aac3-110">PARAMETERS</span></span>

### <span data-ttu-id="1aac3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1aac3-111">-DefaultProfile</span></span>
<span data-ttu-id="1aac3-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1aac3-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1aac3-113">-OfferId</span><span class="sxs-lookup"><span data-stu-id="1aac3-113">-OfferId</span></span>
<span data-ttu-id="1aac3-114">필수 Azure 마켓플레이스 privateStore 제공</span><span class="sxs-lookup"><span data-stu-id="1aac3-114">Required Azure Marketplace privateStore offer</span></span>

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

### <span data-ttu-id="1aac3-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1aac3-115">-PassThru</span></span>
<span data-ttu-id="1aac3-116">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="1aac3-116">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="1aac3-117">-PrivateStoreId</span><span class="sxs-lookup"><span data-stu-id="1aac3-117">-PrivateStoreId</span></span>
<span data-ttu-id="1aac3-118">필수 Azure 마켓플레이스 privateStore</span><span class="sxs-lookup"><span data-stu-id="1aac3-118">Required Azure Marketplace privateStore</span></span>

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

### <span data-ttu-id="1aac3-119">-확인</span><span class="sxs-lookup"><span data-stu-id="1aac3-119">-Confirm</span></span>
<span data-ttu-id="1aac3-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1aac3-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1aac3-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1aac3-121">-WhatIf</span></span>
<span data-ttu-id="1aac3-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1aac3-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1aac3-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1aac3-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1aac3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1aac3-124">CommonParameters</span></span>
<span data-ttu-id="1aac3-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1aac3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1aac3-126">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="1aac3-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1aac3-127">입력</span><span class="sxs-lookup"><span data-stu-id="1aac3-127">INPUTS</span></span>

### <span data-ttu-id="1aac3-128">않아야</span><span class="sxs-lookup"><span data-stu-id="1aac3-128">None</span></span>

## <span data-ttu-id="1aac3-129">출력</span><span class="sxs-lookup"><span data-stu-id="1aac3-129">OUTPUTS</span></span>

### <span data-ttu-id="1aac3-130">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="1aac3-130">System.Boolean</span></span>

## <span data-ttu-id="1aac3-131">상속자</span><span class="sxs-lookup"><span data-stu-id="1aac3-131">NOTES</span></span>

## <span data-ttu-id="1aac3-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1aac3-132">RELATED LINKS</span></span>
