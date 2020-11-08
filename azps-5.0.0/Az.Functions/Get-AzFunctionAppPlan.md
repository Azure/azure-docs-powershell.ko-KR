---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/get-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionAppPlan.md
ms.openlocfilehash: d08d050253842e13967d001889e1b7d1b331ce17
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215429"
---
# <span data-ttu-id="91c9c-101">Get-AzFunctionAppPlan</span><span class="sxs-lookup"><span data-stu-id="91c9c-101">Get-AzFunctionAppPlan</span></span>

## <span data-ttu-id="91c9c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91c9c-102">SYNOPSIS</span></span>
<span data-ttu-id="91c9c-103">구독에서 함수 앱 계획을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="91c9c-103">Get function apps plans in a subscription.</span></span>

## <span data-ttu-id="91c9c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="91c9c-104">SYNTAX</span></span>

### <span data-ttu-id="91c9c-105">GetAll (기본값)</span><span class="sxs-lookup"><span data-stu-id="91c9c-105">GetAll (Default)</span></span>
```
Get-AzFunctionAppPlan [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="91c9c-106">ByLocation</span><span class="sxs-lookup"><span data-stu-id="91c9c-106">ByLocation</span></span>
```
Get-AzFunctionAppPlan -Location <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="91c9c-107">ByName</span><span class="sxs-lookup"><span data-stu-id="91c9c-107">ByName</span></span>
```
Get-AzFunctionAppPlan -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="91c9c-108">ByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91c9c-108">ByResourceGroupName</span></span>
```
Get-AzFunctionAppPlan [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="91c9c-109">설명은</span><span class="sxs-lookup"><span data-stu-id="91c9c-109">DESCRIPTION</span></span>
<span data-ttu-id="91c9c-110">구독에서 함수 앱 계획을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="91c9c-110">Get function apps plans in a subscription.</span></span>

## <span data-ttu-id="91c9c-111">예제의</span><span class="sxs-lookup"><span data-stu-id="91c9c-111">EXAMPLES</span></span>

### <span data-ttu-id="91c9c-112">예제 1: 모든 함수 앱 계획을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="91c9c-112">Example 1: Get all function app plans.</span></span>
```powershell
PS C:\> Get-AzFunctionAppPlan

Name                               WorkerType SkuTier        SkuName Location    ResourceGroupName                SubscriptionId
----                               ---------- -------        ------- --------    -----------------                --------------
Func99-West-Europe-Linux-Premium   Linux      ElasticPremium EP1     West Europe Func99-West-Europe-Linux-Premium fe16564a-d943-4bf8-8c28-cf01708c3f8b
Func99-West-Europe-Windows-Premium Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8b
Func99-Windows-Premium1680894595   Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8b
Func99-Windows-Premium428118799    Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8b
Func99-Windows-Premium677505437    Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8b
Func99-Windows-Premium711892854    Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8b
Func99-Windows-Premium819994758    Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8b
```

<span data-ttu-id="91c9c-113">이 명령은 모든 함수 앱 계획을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="91c9c-113">This command gets all function app plans.</span></span>

### <span data-ttu-id="91c9c-114">예제 2: 리소스 그룹 이름을 기준으로 함수 앱 계획을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="91c9c-114">Example 2: Get function app plans by resource group name.</span></span>
```powershell
PS C:\> Get-AzFunctionAppPlan -ResourceGroupName "West Europe"

Name                               WorkerType SkuTier        SkuName Location    ResourceGroupName                SubscriptionId
----                               ---------- -------        ------- --------    -----------------                --------------
Func99-West-Europe-Linux-Premium   Linux      ElasticPremium EP1     West Europe Func99-West-Europe-Linux-Premium fe16564a-d943-4bf8-8c28-cf01708c3f8b
Func99-West-Europe-Windows-Premium Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8b
Func99-Windows-Premium1680894595   Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8b
```

<span data-ttu-id="91c9c-115">이 명령은 리소스 그룹 이름을 기준으로 함수 앱 계획을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="91c9c-115">This command gets function app plans by resource group name.</span></span>

### <span data-ttu-id="91c9c-116">예제 3: 지정 된 구독에 대 한 함수 앱 계획을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="91c9c-116">Example 3: Get function app plans for the given subscriptions.</span></span>
```powershell
PS C:\> Get-AzFunctionAppPlan -SubscriptionId fe16564a-d943-4bf8-8c28-cf01708c3f8z

Name                               WorkerType SkuTier        SkuName Location    ResourceGroupName                SubscriptionId
----                               ---------- -------        ------- --------    -----------------                --------------
Func99-West-Europe-Windows-Premium Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8z
```

<span data-ttu-id="91c9c-117">이 명령은 지정 된 구독에 대 한 함수 앱 계획을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="91c9c-117">This command gets function app plans for the given subscriptions.</span></span>

### <span data-ttu-id="91c9c-118">예제 4: 위치에 따라 함수 앱 계획을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="91c9c-118">Example 4: Get function app plans by location.</span></span>
```powershell
PS C:\> Get-AzFunctionAppPlan -Location "Central US"

Name                               WorkerType SkuTier        SkuName Location   ResourceGroupName                SubscriptionId
----                               ---------- -------        ------- --------   -----------------                --------------
Func99-West-Europe-Windows-Premium Windows    ElasticPremium EP1     Central US Func99-West-Europe-Win-Premium   3r16564a-d943-4bf8-8c28-cf01708c3f8b
```

<span data-ttu-id="91c9c-119">이 명령은 위치에 따라 함수 앱 계획을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="91c9c-119">This command gets function app plans by location.</span></span>

## <span data-ttu-id="91c9c-120">변수</span><span class="sxs-lookup"><span data-stu-id="91c9c-120">PARAMETERS</span></span>

### <span data-ttu-id="91c9c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91c9c-121">-DefaultProfile</span></span>
<span data-ttu-id="91c9c-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="91c9c-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91c9c-123">-위치</span><span class="sxs-lookup"><span data-stu-id="91c9c-123">-Location</span></span>
<span data-ttu-id="91c9c-124">함수 앱 계획의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="91c9c-124">The location of the function app plan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91c9c-125">-이름</span><span class="sxs-lookup"><span data-stu-id="91c9c-125">-Name</span></span>
<span data-ttu-id="91c9c-126">서비스 계획 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="91c9c-126">The service plan name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91c9c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91c9c-127">-ResourceGroupName</span></span>
<span data-ttu-id="91c9c-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="91c9c-128">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName, ByResourceGroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91c9c-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="91c9c-129">-SubscriptionId</span></span>
<span data-ttu-id="91c9c-130">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="91c9c-130">The Azure subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91c9c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91c9c-131">CommonParameters</span></span>
<span data-ttu-id="91c9c-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="91c9c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91c9c-133">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="91c9c-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91c9c-134">입력</span><span class="sxs-lookup"><span data-stu-id="91c9c-134">INPUTS</span></span>

## <span data-ttu-id="91c9c-135">출력</span><span class="sxs-lookup"><span data-stu-id="91c9c-135">OUTPUTS</span></span>

### <span data-ttu-id="91c9c-136">Api20190801. i p. PowerShell. IAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="91c9c-136">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span></span>

## <span data-ttu-id="91c9c-137">상속자</span><span class="sxs-lookup"><span data-stu-id="91c9c-137">NOTES</span></span>

<span data-ttu-id="91c9c-138">별칭과</span><span class="sxs-lookup"><span data-stu-id="91c9c-138">ALIASES</span></span>

## <span data-ttu-id="91c9c-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="91c9c-139">RELATED LINKS</span></span>

