---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/get-azfunctionapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionApp.md
ms.openlocfilehash: 6a3a421f1da374db1cc08635891bdeec4375855a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212772"
---
# <span data-ttu-id="76c7c-101">Get-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="76c7c-101">Get-AzFunctionApp</span></span>

## <span data-ttu-id="76c7c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76c7c-102">SYNOPSIS</span></span>
<span data-ttu-id="76c7c-103">구독에서 함수 앱을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="76c7c-103">Gets function apps in a subscription.</span></span>

## <span data-ttu-id="76c7c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="76c7c-104">SYNTAX</span></span>

### <span data-ttu-id="76c7c-105">GetAll (기본값)</span><span class="sxs-lookup"><span data-stu-id="76c7c-105">GetAll (Default)</span></span>
```
Get-AzFunctionApp [-SubscriptionId <String[]>] [-IncludeSlot] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="76c7c-106">ByLocation</span><span class="sxs-lookup"><span data-stu-id="76c7c-106">ByLocation</span></span>
```
Get-AzFunctionApp -Location <String> [-SubscriptionId <String[]>] [-IncludeSlot] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="76c7c-107">ByName</span><span class="sxs-lookup"><span data-stu-id="76c7c-107">ByName</span></span>
```
Get-AzFunctionApp -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>] [-IncludeSlot]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="76c7c-108">ByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76c7c-108">ByResourceGroupName</span></span>
```
Get-AzFunctionApp [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-IncludeSlot]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="76c7c-109">설명은</span><span class="sxs-lookup"><span data-stu-id="76c7c-109">DESCRIPTION</span></span>
<span data-ttu-id="76c7c-110">구독에서 함수 앱을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="76c7c-110">Gets function apps in a subscription.</span></span>

## <span data-ttu-id="76c7c-111">예제의</span><span class="sxs-lookup"><span data-stu-id="76c7c-111">EXAMPLES</span></span>

### <span data-ttu-id="76c7c-112">예제 1: 모든 함수 앱 가져오기</span><span class="sxs-lookup"><span data-stu-id="76c7c-112">Example 1: Get all function apps.</span></span>
```powershell
PS C:\> Get-AzFunctionApp

Name                     Status  OSType  Runtime Location    AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------    -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US  CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
Functions1-Windows-Java  Running Windows Java    West Europe Premium1-WE    Functions-West-Europe1    fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



### <span data-ttu-id="76c7c-113">예제 2: 이름별로 함수 앱을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="76c7c-113">Example 2: Get function apps by name.</span></span>
```powershell
PS C:\> Get-AzFunctionApp -ResourceGroupName Functions-West-Europe-Win -Name Functions1-Windows-DoNet

Name                     Status  OSType  Runtime Location   AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------   -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



### <span data-ttu-id="76c7c-114">예제 3: 리소스 그룹 이름을 기준으로 함수 앱을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="76c7c-114">Example 3: Get function apps by resource group name.</span></span>
```powershell
PS C:\> Get-AzFunctionApp -ResourceGroupName Functions-West-Europe-Win

Name                     Status  OSType  Runtime Location   AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------   -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



### <span data-ttu-id="76c7c-115">예제 4: 지정 된 구독에 대 한 함수 앱 가져오기</span><span class="sxs-lookup"><span data-stu-id="76c7c-115">Example 4: Get function apps for the given subscriptions.</span></span>
```powershell
PS C:\> Get-AzFunctionApp -SubscriptionId fe16564a-d943-4bf8-8c28-cf01708c3f8b

Name                     Status  OSType  Runtime Location   AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------   -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



### <span data-ttu-id="76c7c-116">예제 5: 위치를 기준으로 함수 앱을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="76c7c-116">Example 5: Get function apps by location.</span></span>
```powershell
PS C:\> Get-AzFunctionApp -Location "Central US"

Name                     Status  OSType  Runtime Location   AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------   -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



## <span data-ttu-id="76c7c-117">변수</span><span class="sxs-lookup"><span data-stu-id="76c7c-117">PARAMETERS</span></span>

### <span data-ttu-id="76c7c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76c7c-118">-DefaultProfile</span></span>
<span data-ttu-id="76c7c-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="76c7c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76c7c-120">-IncludeSlot</span><span class="sxs-lookup"><span data-stu-id="76c7c-120">-IncludeSlot</span></span>
<span data-ttu-id="76c7c-121">배포 슬롯을 결과에 포함시킬지 여부를 지정 하는 데 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="76c7c-121">Use to specify whether to include deployment slots in results.</span></span>

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

### <span data-ttu-id="76c7c-122">-위치</span><span class="sxs-lookup"><span data-stu-id="76c7c-122">-Location</span></span>
<span data-ttu-id="76c7c-123">함수 앱의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="76c7c-123">The location of the function app.</span></span>

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

### <span data-ttu-id="76c7c-124">-이름</span><span class="sxs-lookup"><span data-stu-id="76c7c-124">-Name</span></span>
<span data-ttu-id="76c7c-125">함수 앱의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="76c7c-125">The name of the function app.</span></span>

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

### <span data-ttu-id="76c7c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76c7c-126">-ResourceGroupName</span></span>
<span data-ttu-id="76c7c-127">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="76c7c-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="76c7c-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="76c7c-128">-SubscriptionId</span></span>
<span data-ttu-id="76c7c-129">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="76c7c-129">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="76c7c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76c7c-130">CommonParameters</span></span>
<span data-ttu-id="76c7c-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="76c7c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76c7c-132">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="76c7c-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76c7c-133">입력</span><span class="sxs-lookup"><span data-stu-id="76c7c-133">INPUTS</span></span>

## <span data-ttu-id="76c7c-134">출력</span><span class="sxs-lookup"><span data-stu-id="76c7c-134">OUTPUTS</span></span>

### <span data-ttu-id="76c7c-135">Api20190801. ISite의. PowerShell for.</span><span class="sxs-lookup"><span data-stu-id="76c7c-135">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span></span>

## <span data-ttu-id="76c7c-136">상속자</span><span class="sxs-lookup"><span data-stu-id="76c7c-136">NOTES</span></span>

<span data-ttu-id="76c7c-137">별칭과</span><span class="sxs-lookup"><span data-stu-id="76c7c-137">ALIASES</span></span>

## <span data-ttu-id="76c7c-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="76c7c-138">RELATED LINKS</span></span>

