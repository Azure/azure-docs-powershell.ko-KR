---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityPricing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityPricing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityPricing.md
ms.openlocfilehash: aa93fee1aa1cf9242d87239625e1c25612498e09
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699242"
---
# <span data-ttu-id="1ad3d-101">Get-AzSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="1ad3d-101">Get-AzSecurityPricing</span></span>

## <span data-ttu-id="1ad3d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ad3d-102">SYNOPSIS</span></span>
<span data-ttu-id="1ad3d-103">범위에 대 한 Azure 보안 센터에 대 한 가격 책정 계층 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1ad3d-103">Gets the pricing tier data for Azure Security Center for a scope.</span></span>

## <span data-ttu-id="1ad3d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1ad3d-104">SYNTAX</span></span>

### <span data-ttu-id="1ad3d-105">구독 범위 (기본값)</span><span class="sxs-lookup"><span data-stu-id="1ad3d-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityPricing [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1ad3d-106">구독 Levelresource</span><span class="sxs-lookup"><span data-stu-id="1ad3d-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityPricing -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1ad3d-107">리소스</span><span class="sxs-lookup"><span data-stu-id="1ad3d-107">ResourceId</span></span>
```
Get-AzSecurityPricing -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1ad3d-108">설명은</span><span class="sxs-lookup"><span data-stu-id="1ad3d-108">DESCRIPTION</span></span>
<span data-ttu-id="1ad3d-109">Azure 보안 센터 가격 책정 계층은 범위 별로 결정 되며이 cmdlet을 사용 하 여 구성 된 가격 책정 계층을 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1ad3d-109">Azure Security Center pricing tier is decided per scope, with this cmdlet you can get the configured pricing tiers.</span></span>
<span data-ttu-id="1ad3d-110">구독 가격 책정 계층에는 모든 리소스 그룹이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1ad3d-110">Subscription pricing tier include all the resource groups under it.</span></span>
<span data-ttu-id="1ad3d-111">자원 그룹 가격 책정 계층이 구독 가격 책정 계층을 재정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ad3d-111">Resource Group pricing tier will override the subscription pricing tier.</span></span>

## <span data-ttu-id="1ad3d-112">예제의</span><span class="sxs-lookup"><span data-stu-id="1ad3d-112">EXAMPLES</span></span>

### <span data-ttu-id="1ad3d-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="1ad3d-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityPricing
Id                                                                                                                             Name       PricingTier
--                                                                                                                             ----       -----------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/pricings/default                              default    Standard
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/pricings/myService1 myService1 Standard
```

<span data-ttu-id="1ad3d-114">구독에 대해 구성 된 모든 가격 책정 계층과 그 아래의 리소스 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1ad3d-114">Gets all the configured pricing tiers for the subscription and the resource groups under it.</span></span>

### <span data-ttu-id="1ad3d-115">예제 2</span><span class="sxs-lookup"><span data-stu-id="1ad3d-115">Example 2</span></span>
```powershell
PS C:\> Get-AzSecurityPricing -ResourceGroupName "myService1"
Id                                                                                                                             Name       PricingTier
--                                                                                                                             ----       -----------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/pricings/myService1 myService1 Standard
```

<span data-ttu-id="1ad3d-116">"MyService1" 리소스 gorup에 대해 구성 된 가격 책정 계층을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1ad3d-116">Gets the configured pricing tier for the "myService1" resource gorup.</span></span>

## <span data-ttu-id="1ad3d-117">변수</span><span class="sxs-lookup"><span data-stu-id="1ad3d-117">PARAMETERS</span></span>

### <span data-ttu-id="1ad3d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ad3d-118">-DefaultProfile</span></span>
<span data-ttu-id="1ad3d-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1ad3d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1ad3d-120">-이름</span><span class="sxs-lookup"><span data-stu-id="1ad3d-120">-Name</span></span>
<span data-ttu-id="1ad3d-121">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1ad3d-121">Resource name.</span></span>

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

### <span data-ttu-id="1ad3d-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1ad3d-122">-ResourceId</span></span>
<span data-ttu-id="1ad3d-123">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="1ad3d-123">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ad3d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ad3d-124">CommonParameters</span></span>
<span data-ttu-id="1ad3d-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ad3d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ad3d-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ad3d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ad3d-127">입력</span><span class="sxs-lookup"><span data-stu-id="1ad3d-127">INPUTS</span></span>

### <span data-ttu-id="1ad3d-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="1ad3d-128">System.String</span></span>

## <span data-ttu-id="1ad3d-129">출력</span><span class="sxs-lookup"><span data-stu-id="1ad3d-129">OUTPUTS</span></span>

### <span data-ttu-id="1ad3d-130">Pricings. PSSecurityPricing에 대 한 Microsoft</span><span class="sxs-lookup"><span data-stu-id="1ad3d-130">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="1ad3d-131">상속자</span><span class="sxs-lookup"><span data-stu-id="1ad3d-131">NOTES</span></span>

## <span data-ttu-id="1ad3d-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1ad3d-132">RELATED LINKS</span></span>
