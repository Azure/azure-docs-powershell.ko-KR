---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/powershell/module/az.functions/get-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionAppPlan.md
ms.openlocfilehash: 786f3e406228eb7929993804a8cef84e7cae109e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101969083"
---
# <span data-ttu-id="51938-101">Get-AzFunctionAppPlan</span><span class="sxs-lookup"><span data-stu-id="51938-101">Get-AzFunctionAppPlan</span></span>

## <span data-ttu-id="51938-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51938-102">SYNOPSIS</span></span>
<span data-ttu-id="51938-103">구독에서 함수 앱 요금제 다운로드</span><span class="sxs-lookup"><span data-stu-id="51938-103">Get function apps plans in a subscription.</span></span>

## <span data-ttu-id="51938-104">구문</span><span class="sxs-lookup"><span data-stu-id="51938-104">SYNTAX</span></span>

### <span data-ttu-id="51938-105">GetAll(기본값)</span><span class="sxs-lookup"><span data-stu-id="51938-105">GetAll (Default)</span></span>
```
Get-AzFunctionAppPlan [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="51938-106">ByLocation</span><span class="sxs-lookup"><span data-stu-id="51938-106">ByLocation</span></span>
```
Get-AzFunctionAppPlan -Location <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="51938-107">ByName</span><span class="sxs-lookup"><span data-stu-id="51938-107">ByName</span></span>
```
Get-AzFunctionAppPlan -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="51938-108">ByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51938-108">ByResourceGroupName</span></span>
```
Get-AzFunctionAppPlan [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="51938-109">설명</span><span class="sxs-lookup"><span data-stu-id="51938-109">DESCRIPTION</span></span>
<span data-ttu-id="51938-110">구독에서 함수 앱 요금제 다운로드</span><span class="sxs-lookup"><span data-stu-id="51938-110">Get function apps plans in a subscription.</span></span>

## <span data-ttu-id="51938-111">예제</span><span class="sxs-lookup"><span data-stu-id="51938-111">EXAMPLES</span></span>

### <span data-ttu-id="51938-112">예제 1: 모든 함수 앱 계획을 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="51938-112">Example 1: Get all function app plans.</span></span>
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

<span data-ttu-id="51938-113">이 명령은 모든 함수 앱 계획을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="51938-113">This command gets all function app plans.</span></span>

### <span data-ttu-id="51938-114">예제 2: 리소스 그룹 이름으로 함수 앱 계획을 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="51938-114">Example 2: Get function app plans by resource group name.</span></span>
```powershell
PS C:\> Get-AzFunctionAppPlan -ResourceGroupName "West Europe"

Name                               WorkerType SkuTier        SkuName Location    ResourceGroupName                SubscriptionId
----                               ---------- -------        ------- --------    -----------------                --------------
Func99-West-Europe-Linux-Premium   Linux      ElasticPremium EP1     West Europe Func99-West-Europe-Linux-Premium fe16564a-d943-4bf8-8c28-cf01708c3f8b
Func99-West-Europe-Windows-Premium Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8b
Func99-Windows-Premium1680894595   Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8b
```

<span data-ttu-id="51938-115">이 명령은 리소스 그룹 이름으로 함수 앱 계획을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="51938-115">This command gets function app plans by resource group name.</span></span>

### <span data-ttu-id="51938-116">예제 3: 주어진 구독에 대한 함수 앱 계획을 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="51938-116">Example 3: Get function app plans for the given subscriptions.</span></span>
```powershell
PS C:\> Get-AzFunctionAppPlan -SubscriptionId fe16564a-d943-4bf8-8c28-cf01708c3f8z

Name                               WorkerType SkuTier        SkuName Location    ResourceGroupName                SubscriptionId
----                               ---------- -------        ------- --------    -----------------                --------------
Func99-West-Europe-Windows-Premium Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8z
```

<span data-ttu-id="51938-117">이 명령은 주어진 구독에 대한 함수 앱 계획을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="51938-117">This command gets function app plans for the given subscriptions.</span></span>

### <span data-ttu-id="51938-118">예제 4: 위치로 함수 앱 계획을 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="51938-118">Example 4: Get function app plans by location.</span></span>
```powershell
PS C:\> Get-AzFunctionAppPlan -Location "Central US"

Name                               WorkerType SkuTier        SkuName Location   ResourceGroupName                SubscriptionId
----                               ---------- -------        ------- --------   -----------------                --------------
Func99-West-Europe-Windows-Premium Windows    ElasticPremium EP1     Central US Func99-West-Europe-Win-Premium   3r16564a-d943-4bf8-8c28-cf01708c3f8b
```

<span data-ttu-id="51938-119">이 명령은 위치로 함수 앱 계획을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="51938-119">This command gets function app plans by location.</span></span>

## <span data-ttu-id="51938-120">매개 변수</span><span class="sxs-lookup"><span data-stu-id="51938-120">PARAMETERS</span></span>

### <span data-ttu-id="51938-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51938-121">-DefaultProfile</span></span>
<span data-ttu-id="51938-122">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="51938-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="51938-123">-Location</span><span class="sxs-lookup"><span data-stu-id="51938-123">-Location</span></span>
<span data-ttu-id="51938-124">함수 앱 계획의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="51938-124">The location of the function app plan.</span></span>

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

### <span data-ttu-id="51938-125">-Name</span><span class="sxs-lookup"><span data-stu-id="51938-125">-Name</span></span>
<span data-ttu-id="51938-126">서비스 계획 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="51938-126">The service plan name.</span></span>

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

### <span data-ttu-id="51938-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51938-127">-ResourceGroupName</span></span>
<span data-ttu-id="51938-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="51938-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="51938-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="51938-129">-SubscriptionId</span></span>
<span data-ttu-id="51938-130">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="51938-130">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="51938-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51938-131">CommonParameters</span></span>
<span data-ttu-id="51938-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="51938-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51938-133">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="51938-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51938-134">입력</span><span class="sxs-lookup"><span data-stu-id="51938-134">INPUTS</span></span>

## <span data-ttu-id="51938-135">출력</span><span class="sxs-lookup"><span data-stu-id="51938-135">OUTPUTS</span></span>

### <span data-ttu-id="51938-136">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="51938-136">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span></span>

## <span data-ttu-id="51938-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="51938-137">NOTES</span></span>

<span data-ttu-id="51938-138">별칭</span><span class="sxs-lookup"><span data-stu-id="51938-138">ALIASES</span></span>

## <span data-ttu-id="51938-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="51938-139">RELATED LINKS</span></span>

