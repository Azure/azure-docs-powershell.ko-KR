---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityPricing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityPricing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityPricing.md
ms.openlocfilehash: a52ae3b59cc7cbf99bf7f4751a36f271bc9610de
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93871649"
---
# <span data-ttu-id="d62f5-101">Set-AzSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="d62f5-101">Set-AzSecurityPricing</span></span>

## <span data-ttu-id="d62f5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d62f5-102">SYNOPSIS</span></span>
<span data-ttu-id="d62f5-103">범위에 대 한 Azure 보안 센터 계층의 가격 산정을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d62f5-103">Sets the pricing of Azure Security Center tier for a scope.</span></span>

## <span data-ttu-id="d62f5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d62f5-104">SYNTAX</span></span>

### <span data-ttu-id="d62f5-105">구독 Levelresource (기본값)</span><span class="sxs-lookup"><span data-stu-id="d62f5-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzSecurityPricing -Name <String> -PricingTier <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d62f5-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="d62f5-106">InputObject</span></span>
```
Set-AzSecurityPricing -InputObject <PSSecurityPricing> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d62f5-107">설명은</span><span class="sxs-lookup"><span data-stu-id="d62f5-107">DESCRIPTION</span></span>
<span data-ttu-id="d62f5-108">범위에 대 한 Azure 보안 센터 계층의 가격 산정을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d62f5-108">Sets the pricing of Azure Security Center tier for a scope.</span></span>

## <span data-ttu-id="d62f5-109">예제의</span><span class="sxs-lookup"><span data-stu-id="d62f5-109">EXAMPLES</span></span>

### <span data-ttu-id="d62f5-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="d62f5-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityPricing -Name "default" -PricingTier "Standard"
Id                                                                                                 Name    PricingTier
--                                                                                                 ----    -----------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/pricings/default default Standard
```

<span data-ttu-id="d62f5-111">구독 Azure 보안 센터 가격 책정 계층을 "표준"으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d62f5-111">Sets the subscription Azure Security Center pricing tier to "Standard"</span></span>

### <span data-ttu-id="d62f5-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="d62f5-112">Example 2</span></span>
```powershell
PS C:\> Set-AzSecurityPricing -Name "myService1" -ResourceGroupName "myService1" -PricingTier "Standard"

Id                                                                                                                     
--                                                                                                                     
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/pricings/...
```

<span data-ttu-id="d62f5-113">"MyService1" 자원 그룹 Azure 보안 센터 가격 책정 계층을 "표준"으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d62f5-113">Sets the "myService1" resource group Azure Security Center pricing tier to "Standard"</span></span>

## <span data-ttu-id="d62f5-114">변수</span><span class="sxs-lookup"><span data-stu-id="d62f5-114">PARAMETERS</span></span>

### <span data-ttu-id="d62f5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d62f5-115">-DefaultProfile</span></span>
<span data-ttu-id="d62f5-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d62f5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d62f5-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d62f5-117">-InputObject</span></span>
<span data-ttu-id="d62f5-118">입력 개체</span><span class="sxs-lookup"><span data-stu-id="d62f5-118">Input Object.</span></span>

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

### <span data-ttu-id="d62f5-119">-이름</span><span class="sxs-lookup"><span data-stu-id="d62f5-119">-Name</span></span>
<span data-ttu-id="d62f5-120">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d62f5-120">Resource name.</span></span>

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

### <span data-ttu-id="d62f5-121">-PricingTier</span><span class="sxs-lookup"><span data-stu-id="d62f5-121">-PricingTier</span></span>
<span data-ttu-id="d62f5-122">가격 책정 계층.</span><span class="sxs-lookup"><span data-stu-id="d62f5-122">Pricing Tier.</span></span>

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

### <span data-ttu-id="d62f5-123">-확인</span><span class="sxs-lookup"><span data-stu-id="d62f5-123">-Confirm</span></span>
<span data-ttu-id="d62f5-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d62f5-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d62f5-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d62f5-125">-WhatIf</span></span>
<span data-ttu-id="d62f5-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d62f5-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d62f5-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d62f5-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d62f5-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d62f5-128">CommonParameters</span></span>
<span data-ttu-id="d62f5-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d62f5-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d62f5-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d62f5-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d62f5-131">입력</span><span class="sxs-lookup"><span data-stu-id="d62f5-131">INPUTS</span></span>

### <span data-ttu-id="d62f5-132">Pricings. PSSecurityPricing에 대 한 Microsoft</span><span class="sxs-lookup"><span data-stu-id="d62f5-132">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="d62f5-133">출력</span><span class="sxs-lookup"><span data-stu-id="d62f5-133">OUTPUTS</span></span>

### <span data-ttu-id="d62f5-134">Pricings. PSSecurityPricing에 대 한 Microsoft</span><span class="sxs-lookup"><span data-stu-id="d62f5-134">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="d62f5-135">상속자</span><span class="sxs-lookup"><span data-stu-id="d62f5-135">NOTES</span></span>

## <span data-ttu-id="d62f5-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d62f5-136">RELATED LINKS</span></span>
