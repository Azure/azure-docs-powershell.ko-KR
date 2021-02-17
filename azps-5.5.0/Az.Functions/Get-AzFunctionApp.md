---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/get-azfunctionapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionApp.md
ms.openlocfilehash: a81bb1515e25f9000438fbd463117e4fd69b9690
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209445"
---
# <span data-ttu-id="4a073-101">Get-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="4a073-101">Get-AzFunctionApp</span></span>

## <span data-ttu-id="4a073-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a073-102">SYNOPSIS</span></span>
<span data-ttu-id="4a073-103">구독에서 함수 앱을 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="4a073-103">Gets function apps in a subscription.</span></span>

## <span data-ttu-id="4a073-104">구문</span><span class="sxs-lookup"><span data-stu-id="4a073-104">SYNTAX</span></span>

### <span data-ttu-id="4a073-105">GetAll(기본값)</span><span class="sxs-lookup"><span data-stu-id="4a073-105">GetAll (Default)</span></span>
```
Get-AzFunctionApp [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="4a073-106">ByLocation</span><span class="sxs-lookup"><span data-stu-id="4a073-106">ByLocation</span></span>
```
Get-AzFunctionApp -Location <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="4a073-107">ByName</span><span class="sxs-lookup"><span data-stu-id="4a073-107">ByName</span></span>
```
Get-AzFunctionApp -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="4a073-108">ByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a073-108">ByResourceGroupName</span></span>
```
Get-AzFunctionApp -ResourceGroupName <String> [-SubscriptionId <String[]>] [-IncludeSlot]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="4a073-109">설명</span><span class="sxs-lookup"><span data-stu-id="4a073-109">DESCRIPTION</span></span>
<span data-ttu-id="4a073-110">구독에서 함수 앱을 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="4a073-110">Gets function apps in a subscription.</span></span>

## <span data-ttu-id="4a073-111">예제</span><span class="sxs-lookup"><span data-stu-id="4a073-111">EXAMPLES</span></span>

### <span data-ttu-id="4a073-112">예제 1: 모든 함수 앱을 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="4a073-112">Example 1: Get all function apps.</span></span>
```powershell
PS C:\> Get-AzFunctionApp

Name                     Status  OSType  Runtime Location    AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------    -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US  CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
Functions1-Windows-Java  Running Windows Java    West Europe Premium1-WE    Functions-West-Europe1    fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



### <span data-ttu-id="4a073-113">예제 2: 이름으로 함수 앱을 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="4a073-113">Example 2: Get function apps by name.</span></span>
```powershell
PS C:\> Get-AzFunctionApp -ResourceGroupName Functions-West-Europe-Win -Name Functions1-Windows-DoNet

Name                     Status  OSType  Runtime Location   AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------   -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



### <span data-ttu-id="4a073-114">예제 3: 리소스 그룹 이름으로 함수 앱을 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="4a073-114">Example 3: Get function apps by resource group name.</span></span>
```powershell
PS C:\> Get-AzFunctionApp -ResourceGroupName Functions-West-Europe-Win

Name                     Status  OSType  Runtime Location   AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------   -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



### <span data-ttu-id="4a073-115">예제 4: 주어진 구독에 대한 함수 앱을 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="4a073-115">Example 4: Get function apps for the given subscriptions.</span></span>
```powershell
PS C:\> Get-AzFunctionApp -SubscriptionId fe16564a-d943-4bf8-8c28-cf01708c3f8b

Name                     Status  OSType  Runtime Location   AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------   -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



### <span data-ttu-id="4a073-116">예제 5: 위치로 함수 앱 다운로드</span><span class="sxs-lookup"><span data-stu-id="4a073-116">Example 5: Get function apps by location.</span></span>
```powershell
PS C:\> Get-AzFunctionApp -Location "Central US"

Name                     Status  OSType  Runtime Location   AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------   -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



## <span data-ttu-id="4a073-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4a073-117">PARAMETERS</span></span>

### <span data-ttu-id="4a073-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a073-118">-DefaultProfile</span></span>
<span data-ttu-id="4a073-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4a073-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a073-120">-IncludeSlot</span><span class="sxs-lookup"><span data-stu-id="4a073-120">-IncludeSlot</span></span>
<span data-ttu-id="4a073-121">결과에 배포 슬롯을 포함할지 여부를 지정하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4a073-121">Use to specify whether to include deployment slots in results.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByResourceGroupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a073-122">-Location</span><span class="sxs-lookup"><span data-stu-id="4a073-122">-Location</span></span>
<span data-ttu-id="4a073-123">함수 앱의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="4a073-123">The location of the function app.</span></span>

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

### <span data-ttu-id="4a073-124">-Name</span><span class="sxs-lookup"><span data-stu-id="4a073-124">-Name</span></span>
<span data-ttu-id="4a073-125">함수 앱의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4a073-125">The name of the function app.</span></span>

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

### <span data-ttu-id="4a073-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a073-126">-ResourceGroupName</span></span>
<span data-ttu-id="4a073-127">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4a073-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="4a073-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4a073-128">-SubscriptionId</span></span>
<span data-ttu-id="4a073-129">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="4a073-129">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="4a073-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a073-130">CommonParameters</span></span>
<span data-ttu-id="4a073-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4a073-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a073-132">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4a073-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a073-133">입력</span><span class="sxs-lookup"><span data-stu-id="4a073-133">INPUTS</span></span>

## <span data-ttu-id="4a073-134">출력</span><span class="sxs-lookup"><span data-stu-id="4a073-134">OUTPUTS</span></span>

### <span data-ttu-id="4a073-135">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span><span class="sxs-lookup"><span data-stu-id="4a073-135">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span></span>

## <span data-ttu-id="4a073-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4a073-136">NOTES</span></span>

<span data-ttu-id="4a073-137">별칭</span><span class="sxs-lookup"><span data-stu-id="4a073-137">ALIASES</span></span>

## <span data-ttu-id="4a073-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4a073-138">RELATED LINKS</span></span>

