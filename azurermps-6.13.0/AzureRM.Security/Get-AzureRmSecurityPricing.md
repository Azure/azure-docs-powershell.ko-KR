---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityPricing.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityPricing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityPricing.md
ms.openlocfilehash: 27d27cf3df8c41eaa507d9223c73f2b36637a04c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526040"
---
# <span data-ttu-id="69ca7-101">Get-AzureRmSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="69ca7-101">Get-AzureRmSecurityPricing</span></span>

## <span data-ttu-id="69ca7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69ca7-102">SYNOPSIS</span></span>
<span data-ttu-id="69ca7-103">범위에 대 한 Azure 보안 센터에 대 한 가격 책정 계층 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="69ca7-103">Gets the pricing tier data for Azure Security Center for a scope.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="69ca7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="69ca7-104">SYNTAX</span></span>

### <span data-ttu-id="69ca7-105">구독 범위 (기본값)</span><span class="sxs-lookup"><span data-stu-id="69ca7-105">SubscriptionScope (Default)</span></span>
```
Get-AzureRmSecurityPricing [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="69ca7-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="69ca7-106">ResourceGroupLevelResource</span></span>
```
Get-AzureRmSecurityPricing -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="69ca7-107">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="69ca7-107">ResourceGroupScope</span></span>
```
Get-AzureRmSecurityPricing -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="69ca7-108">구독 Levelresource</span><span class="sxs-lookup"><span data-stu-id="69ca7-108">SubscriptionLevelResource</span></span>
```
Get-AzureRmSecurityPricing -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="69ca7-109">리소스</span><span class="sxs-lookup"><span data-stu-id="69ca7-109">ResourceId</span></span>
```
Get-AzureRmSecurityPricing -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="69ca7-110">설명은</span><span class="sxs-lookup"><span data-stu-id="69ca7-110">DESCRIPTION</span></span>
<span data-ttu-id="69ca7-111">Azure 보안 센터 가격 책정 계층은 범위 별로 결정 되며이 cmdlet을 사용 하 여 구성 된 가격 책정 계층을 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="69ca7-111">Azure Security Center pricing tier is decided per scope, with this cmdlet you can get the configured pricing tiers.</span></span>
<span data-ttu-id="69ca7-112">구독 가격 책정 계층에는 모든 리소스 그룹이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="69ca7-112">Subscription pricing tier include all the resource groups under it.</span></span>
<span data-ttu-id="69ca7-113">자원 그룹 가격 책정 계층이 구독 가격 책정 계층을 재정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="69ca7-113">Resource Group pricing tier will override the subscription pricing tier.</span></span>

## <span data-ttu-id="69ca7-114">예제의</span><span class="sxs-lookup"><span data-stu-id="69ca7-114">EXAMPLES</span></span>

### <span data-ttu-id="69ca7-115">예제 1</span><span class="sxs-lookup"><span data-stu-id="69ca7-115">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmSecurityPricing
Id                                                                                                                             Name       PricingTier
--                                                                                                                             ----       -----------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/pricings/default                              default    Standard
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/pricings/myService1 myService1 Standard
```

<span data-ttu-id="69ca7-116">구독에 대해 구성 된 모든 가격 책정 계층과 그 아래의 리소스 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="69ca7-116">Gets all the configured pricing tiers for the subscription and the resource groups under it.</span></span>

### <span data-ttu-id="69ca7-117">예제 2</span><span class="sxs-lookup"><span data-stu-id="69ca7-117">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmSecurityPricing -ResourceGroupName "myService1"
Id                                                                                                                             Name       PricingTier
--                                                                                                                             ----       -----------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/pricings/myService1 myService1 Standard
```

<span data-ttu-id="69ca7-118">"MyService1" 리소스 gorup에 대해 구성 된 가격 책정 계층을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="69ca7-118">Gets the configured pricing tier for the "myService1" resource gorup.</span></span>

## <span data-ttu-id="69ca7-119">변수</span><span class="sxs-lookup"><span data-stu-id="69ca7-119">PARAMETERS</span></span>

### <span data-ttu-id="69ca7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69ca7-120">-DefaultProfile</span></span>
<span data-ttu-id="69ca7-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="69ca7-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69ca7-122">-이름</span><span class="sxs-lookup"><span data-stu-id="69ca7-122">-Name</span></span>
<span data-ttu-id="69ca7-123">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="69ca7-123">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource, SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69ca7-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69ca7-124">-ResourceGroupName</span></span>
<span data-ttu-id="69ca7-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="69ca7-125">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource, ResourceGroupScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69ca7-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="69ca7-126">-ResourceId</span></span>
<span data-ttu-id="69ca7-127">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="69ca7-127">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69ca7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69ca7-128">CommonParameters</span></span>
<span data-ttu-id="69ca7-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="69ca7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69ca7-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69ca7-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69ca7-131">입력</span><span class="sxs-lookup"><span data-stu-id="69ca7-131">INPUTS</span></span>

### <span data-ttu-id="69ca7-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="69ca7-132">System.String</span></span>

## <span data-ttu-id="69ca7-133">출력</span><span class="sxs-lookup"><span data-stu-id="69ca7-133">OUTPUTS</span></span>

### <span data-ttu-id="69ca7-134">Pricings. PSSecurityPricing에 대 한 Microsoft</span><span class="sxs-lookup"><span data-stu-id="69ca7-134">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="69ca7-135">상속자</span><span class="sxs-lookup"><span data-stu-id="69ca7-135">NOTES</span></span>

## <span data-ttu-id="69ca7-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="69ca7-136">RELATED LINKS</span></span>
