---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityPricing.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityPricing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityPricing.md
ms.openlocfilehash: f5b23c9221fe8d344e9220590283ab7799a0a3fc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530068"
---
# <span data-ttu-id="2a42d-101">Set-AzureRmSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="2a42d-101">Set-AzureRmSecurityPricing</span></span>

## <span data-ttu-id="2a42d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a42d-102">SYNOPSIS</span></span>
<span data-ttu-id="2a42d-103">범위에 대 한 Azure 보안 센터 계층의 가격 산정을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a42d-103">Sets the pricing of Azure Security Center tier for a scope.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2a42d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2a42d-104">SYNTAX</span></span>

### <span data-ttu-id="2a42d-105">구독 Levelresource (기본값)</span><span class="sxs-lookup"><span data-stu-id="2a42d-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzureRmSecurityPricing -Name <String> -PricingTier <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a42d-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="2a42d-106">ResourceGroupLevelResource</span></span>
```
Set-AzureRmSecurityPricing -ResourceGroupName <String> -Name <String> -PricingTier <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a42d-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="2a42d-107">InputObject</span></span>
```
Set-AzureRmSecurityPricing -InputObject <PSAddPricingInputObject> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a42d-108">설명은</span><span class="sxs-lookup"><span data-stu-id="2a42d-108">DESCRIPTION</span></span>
<span data-ttu-id="2a42d-109">범위에 대 한 Azure 보안 센터 계층의 가격 산정을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a42d-109">Sets the pricing of Azure Security Center tier for a scope.</span></span>

## <span data-ttu-id="2a42d-110">예제의</span><span class="sxs-lookup"><span data-stu-id="2a42d-110">EXAMPLES</span></span>

### <span data-ttu-id="2a42d-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="2a42d-111">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmSecurityPricing -Name "default" -PricingTier "Standard"
Id                                                                                                 Name    PricingTier
--                                                                                                 ----    -----------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/pricings/default default Standard
```

<span data-ttu-id="2a42d-112">구독 Azure 보안 센터 가격 책정 계층을 "표준"으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a42d-112">Sets the subscription Azure Security Center pricing tier to "Standard"</span></span>

### <span data-ttu-id="2a42d-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="2a42d-113">Example 2</span></span>
```powershell
PS C:\> Set-AzureRmSecurityPricing -Name "myService1" -ResourceGroupName "myService1" -PricingTier "Standard"

Id                                                                                                                     
--                                                                                                                     
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/pricings/...
```

<span data-ttu-id="2a42d-114">"MyService1" 자원 그룹 Azure 보안 센터 가격 책정 계층을 "표준"으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a42d-114">Sets the "myService1" resource group Azure Security Center pricing tier to "Standard"</span></span>

## <span data-ttu-id="2a42d-115">변수</span><span class="sxs-lookup"><span data-stu-id="2a42d-115">PARAMETERS</span></span>

### <span data-ttu-id="2a42d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a42d-116">-DefaultProfile</span></span>
<span data-ttu-id="2a42d-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2a42d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a42d-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2a42d-118">-InputObject</span></span>
<span data-ttu-id="2a42d-119">입력 개체</span><span class="sxs-lookup"><span data-stu-id="2a42d-119">Input Object.</span></span>

```yaml
Type: PSAddPricingInputObject
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2a42d-120">-이름</span><span class="sxs-lookup"><span data-stu-id="2a42d-120">-Name</span></span>
<span data-ttu-id="2a42d-121">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2a42d-121">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource, ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a42d-122">-PricingTier</span><span class="sxs-lookup"><span data-stu-id="2a42d-122">-PricingTier</span></span>
<span data-ttu-id="2a42d-123">가격 책정 계층.</span><span class="sxs-lookup"><span data-stu-id="2a42d-123">Pricing Tier.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource, ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a42d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a42d-124">-ResourceGroupName</span></span>
<span data-ttu-id="2a42d-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2a42d-125">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a42d-126">-확인</span><span class="sxs-lookup"><span data-stu-id="2a42d-126">-Confirm</span></span>
<span data-ttu-id="2a42d-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a42d-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a42d-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a42d-128">-WhatIf</span></span>
<span data-ttu-id="2a42d-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2a42d-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2a42d-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2a42d-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a42d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a42d-131">CommonParameters</span></span>
<span data-ttu-id="2a42d-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a42d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a42d-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a42d-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a42d-134">입력</span><span class="sxs-lookup"><span data-stu-id="2a42d-134">INPUTS</span></span>

### <span data-ttu-id="2a42d-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="2a42d-135">System.String</span></span>
<span data-ttu-id="2a42d-136">Pricings. PSAddPricingInputObject에 대 한</span><span class="sxs-lookup"><span data-stu-id="2a42d-136">Microsoft.Azure.Commands.Security.Cmdlets.Pricings.PSAddPricingInputObject</span></span>

## <span data-ttu-id="2a42d-137">출력</span><span class="sxs-lookup"><span data-stu-id="2a42d-137">OUTPUTS</span></span>

### <span data-ttu-id="2a42d-138">Pricings. PSSecurityPricing에 대 한 Microsoft</span><span class="sxs-lookup"><span data-stu-id="2a42d-138">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="2a42d-139">상속자</span><span class="sxs-lookup"><span data-stu-id="2a42d-139">NOTES</span></span>

## <span data-ttu-id="2a42d-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2a42d-140">RELATED LINKS</span></span>
