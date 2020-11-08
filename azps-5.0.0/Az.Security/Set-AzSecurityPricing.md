---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityPricing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityPricing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityPricing.md
ms.openlocfilehash: e9dfe0e7ed4612ca99a2decf3aa91b521a7e9664
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217997"
---
# <span data-ttu-id="69f1b-101">Set-AzSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="69f1b-101">Set-AzSecurityPricing</span></span>

## <span data-ttu-id="69f1b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69f1b-102">SYNOPSIS</span></span>
<span data-ttu-id="69f1b-103">범위에 대 한 Azure 보안 센터 계층의 가격 산정을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="69f1b-103">Sets the pricing of Azure Security Center tier for a scope.</span></span>

## <span data-ttu-id="69f1b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="69f1b-104">SYNTAX</span></span>

### <span data-ttu-id="69f1b-105">구독 Levelresource (기본값)</span><span class="sxs-lookup"><span data-stu-id="69f1b-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzSecurityPricing -Name <String> -PricingTier <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69f1b-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="69f1b-106">InputObject</span></span>
```
Set-AzSecurityPricing -InputObject <PSSecurityPricing> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69f1b-107">설명은</span><span class="sxs-lookup"><span data-stu-id="69f1b-107">DESCRIPTION</span></span>
<span data-ttu-id="69f1b-108">범위에 대 한 Azure 보안 센터 계층의 가격 산정을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="69f1b-108">Sets the pricing of Azure Security Center tier for a scope.</span></span>

## <span data-ttu-id="69f1b-109">예제의</span><span class="sxs-lookup"><span data-stu-id="69f1b-109">EXAMPLES</span></span>

### <span data-ttu-id="69f1b-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="69f1b-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityPricing -Name "virtualmachines" -PricingTier "Standard"
```

<span data-ttu-id="69f1b-111">구독 Azure 보안 센터 가격 책정 계층을 "표준"으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="69f1b-111">Sets the subscription Azure Security Center pricing tier to "Standard"</span></span>


## <span data-ttu-id="69f1b-112">변수</span><span class="sxs-lookup"><span data-stu-id="69f1b-112">PARAMETERS</span></span>

### <span data-ttu-id="69f1b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69f1b-113">-DefaultProfile</span></span>
<span data-ttu-id="69f1b-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="69f1b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69f1b-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="69f1b-115">-InputObject</span></span>
<span data-ttu-id="69f1b-116">입력 개체</span><span class="sxs-lookup"><span data-stu-id="69f1b-116">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="69f1b-117">-이름</span><span class="sxs-lookup"><span data-stu-id="69f1b-117">-Name</span></span>
<span data-ttu-id="69f1b-118">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="69f1b-118">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69f1b-119">-PricingTier</span><span class="sxs-lookup"><span data-stu-id="69f1b-119">-PricingTier</span></span>
<span data-ttu-id="69f1b-120">가격 책정 계층.</span><span class="sxs-lookup"><span data-stu-id="69f1b-120">Pricing Tier.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69f1b-121">-확인</span><span class="sxs-lookup"><span data-stu-id="69f1b-121">-Confirm</span></span>
<span data-ttu-id="69f1b-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="69f1b-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69f1b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69f1b-123">-WhatIf</span></span>
<span data-ttu-id="69f1b-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="69f1b-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="69f1b-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="69f1b-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69f1b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69f1b-126">CommonParameters</span></span>
<span data-ttu-id="69f1b-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="69f1b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69f1b-128">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="69f1b-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69f1b-129">입력</span><span class="sxs-lookup"><span data-stu-id="69f1b-129">INPUTS</span></span>

### <span data-ttu-id="69f1b-130">Pricings. PSSecurityPricing에 대 한 Microsoft</span><span class="sxs-lookup"><span data-stu-id="69f1b-130">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="69f1b-131">출력</span><span class="sxs-lookup"><span data-stu-id="69f1b-131">OUTPUTS</span></span>

### <span data-ttu-id="69f1b-132">Pricings. PSSecurityPricing에 대 한 Microsoft</span><span class="sxs-lookup"><span data-stu-id="69f1b-132">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="69f1b-133">상속자</span><span class="sxs-lookup"><span data-stu-id="69f1b-133">NOTES</span></span>

## <span data-ttu-id="69f1b-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="69f1b-134">RELATED LINKS</span></span>
