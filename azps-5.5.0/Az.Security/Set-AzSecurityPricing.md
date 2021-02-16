---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityPricing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityPricing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityPricing.md
ms.openlocfilehash: 96f5a9d4791dc2668e4ec82abc140f17cbce7c44
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183569"
---
# <span data-ttu-id="7e42b-101">Set-AzSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="7e42b-101">Set-AzSecurityPricing</span></span>

## <span data-ttu-id="7e42b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e42b-102">SYNOPSIS</span></span>

<span data-ttu-id="7e42b-103">Azure Security Center에서 구독에 대한 Azure Defender 계획을 활성화하거나 비활성화합니다.</span><span class="sxs-lookup"><span data-stu-id="7e42b-103">Enables or disables Azure Defender plans for a subscription in Azure Security Center.</span></span>

## <span data-ttu-id="7e42b-104">구문</span><span class="sxs-lookup"><span data-stu-id="7e42b-104">SYNTAX</span></span>

### <span data-ttu-id="7e42b-105">SubscriptionLevelResource(기본값)</span><span class="sxs-lookup"><span data-stu-id="7e42b-105">SubscriptionLevelResource (Default)</span></span>

```powershell
Set-AzSecurityPricing -Name <String> -PricingTier <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e42b-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="7e42b-106">InputObject</span></span>

```powershell
Set-AzSecurityPricing -InputObject <PSSecurityPricing> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e42b-107">설명</span><span class="sxs-lookup"><span data-stu-id="7e42b-107">DESCRIPTION</span></span>

<span data-ttu-id="7e42b-108">구독에 대한 Azure Defender 계획을 활성화하거나 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="7e42b-108">Enable or disable any of the Azure Defender plans for a subscription.</span></span>

<span data-ttu-id="7e42b-109">Azure Defender 및 사용 가능한 계획에 대한 자세한 내용은 [Azure Defender 소개를 참조하세요.](https://docs.microsoft.com/azure/security-center/azure-defender)</span><span class="sxs-lookup"><span data-stu-id="7e42b-109">For details about Azure Defender and the available plans, see [Introduction to Azure Defender](https://docs.microsoft.com/azure/security-center/azure-defender).</span></span>

## <span data-ttu-id="7e42b-110">예제</span><span class="sxs-lookup"><span data-stu-id="7e42b-110">EXAMPLES</span></span>

### <span data-ttu-id="7e42b-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="7e42b-111">Example 1</span></span>

```powershell
PS C:\> Set-AzSecurityPricing -Name "virtualmachines" -PricingTier "Standard"
```

<span data-ttu-id="7e42b-112">구독에 **대한 서버에 대해 Azure Defender를** 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7e42b-112">Enables **Azure Defender for servers** for the subscription.</span></span>

<span data-ttu-id="7e42b-113">"표준"은 Azure Portal의 Azure Security Center의 가격 책정 및 설정 영역에 표시된 Azure Defender 계획의 "On" 상태를 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="7e42b-113">"Standard" refers to the "On" state for an Azure Defender plan as shown in Azure Security Center's pricing and settings area of the Azure portal.</span></span>


## <span data-ttu-id="7e42b-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7e42b-114">PARAMETERS</span></span>

### <span data-ttu-id="7e42b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e42b-115">-DefaultProfile</span></span>

<span data-ttu-id="7e42b-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7e42b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e42b-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7e42b-117">-InputObject</span></span>

<span data-ttu-id="7e42b-118">입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="7e42b-118">Input Object.</span></span>

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

### <span data-ttu-id="7e42b-119">-Name</span><span class="sxs-lookup"><span data-stu-id="7e42b-119">-Name</span></span>

<span data-ttu-id="7e42b-120">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7e42b-120">Resource name.</span></span>

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

### <span data-ttu-id="7e42b-121">-PricingTier</span><span class="sxs-lookup"><span data-stu-id="7e42b-121">-PricingTier</span></span>

<span data-ttu-id="7e42b-122">가격 책정 계층.</span><span class="sxs-lookup"><span data-stu-id="7e42b-122">Pricing Tier.</span></span>

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

### <span data-ttu-id="7e42b-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7e42b-123">-Confirm</span></span>

<span data-ttu-id="7e42b-124">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7e42b-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e42b-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e42b-125">-WhatIf</span></span>

<span data-ttu-id="7e42b-126">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="7e42b-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7e42b-127">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7e42b-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e42b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e42b-128">CommonParameters</span></span>

<span data-ttu-id="7e42b-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7e42b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e42b-130">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7e42b-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e42b-131">입력</span><span class="sxs-lookup"><span data-stu-id="7e42b-131">INPUTS</span></span>

### <span data-ttu-id="7e42b-132">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="7e42b-132">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="7e42b-133">출력</span><span class="sxs-lookup"><span data-stu-id="7e42b-133">OUTPUTS</span></span>

### <span data-ttu-id="7e42b-134">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="7e42b-134">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="7e42b-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7e42b-135">NOTES</span></span>

## <span data-ttu-id="7e42b-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7e42b-136">RELATED LINKS</span></span>
