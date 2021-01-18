---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/get-azfunctionappavailablelocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionAppAvailableLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionAppAvailableLocation.md
ms.openlocfilehash: 3ab2ab4778b7fdb12334db416c953a7c373c63b5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492983"
---
# <span data-ttu-id="dfa97-101">Get-AzFunctionAppAvailableLocation</span><span class="sxs-lookup"><span data-stu-id="dfa97-101">Get-AzFunctionAppAvailableLocation</span></span>

## <span data-ttu-id="dfa97-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dfa97-102">SYNOPSIS</span></span>
<span data-ttu-id="dfa97-103">주어진 os 및 계획 유형에 대한 함수 앱을 사용할 수 있는 위치를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="dfa97-103">Gets the location where a function app for the given os and plan type is available.</span></span>

## <span data-ttu-id="dfa97-104">구문</span><span class="sxs-lookup"><span data-stu-id="dfa97-104">SYNTAX</span></span>

```
Get-AzFunctionAppAvailableLocation [[-SubscriptionId] <String[]>] [[-PlanType] <String>] [[-OSType] <String>]
 [[-DefaultProfile] <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="dfa97-105">설명</span><span class="sxs-lookup"><span data-stu-id="dfa97-105">DESCRIPTION</span></span>
<span data-ttu-id="dfa97-106">주어진 os 및 계획 유형에 대한 함수 앱을 사용할 수 있는 위치를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="dfa97-106">Gets the location where a function app for the given os and plan type is available.</span></span>

## <span data-ttu-id="dfa97-107">예제</span><span class="sxs-lookup"><span data-stu-id="dfa97-107">EXAMPLES</span></span>

### <span data-ttu-id="dfa97-108">예제 1: Windows에서 프리미엄을 사용할 수 있는 위치를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="dfa97-108">Example 1: Get the locations where Premium is available for Windows.</span></span> <span data-ttu-id="dfa97-109">매개 변수를 지정하지 않으면 PlanType이 'Premium'으로 설정되어 OSType이 'Windows'로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="dfa97-109">If no parameters are specified, PlanType is set to 'Premium' and OSType is set to 'Windows'.</span></span>
```powershell
PS C:\> Get-AzFunctionAppAvailableLocation

Name
----
Central US
North Europe
West Europe
Southeast Asia
East Asia
West US
East US
Japan West
Japan East
East US 2
North Central US
South Central US
Brazil South
Australia East
Australia Southeast
East Asia (Stage)
West India
South India
Canada Central
West US 2
UK West
UK South
East US 2 EUAP
Central US EUAP
Korea Central
France Central
Australia Central 2
Australia Central
Germany West Central
Norway East
```

<span data-ttu-id="dfa97-110">이 명령은 Windows에서 프리미엄을 사용할 수 있는 위치를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="dfa97-110">This command gets the locations where Premium is available for Windows.</span></span>

### <span data-ttu-id="dfa97-111">예제 2: Linux에서 프리미엄을 사용할 수 있는 위치를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="dfa97-111">Example 2: Get the locations where Premium is available for Linux.</span></span>
```powershell
PS C:\> Get-AzFunctionAppAvailableLocation -PlanType Premium -OSType Linux

Name
----
Central US
North Europe
West Europe
Southeast Asia
East Asia
West US
East US
Japan West
Japan East
East US 2
North Central US
South Central US
Brazil South
Australia East
Australia Southeast
West India
Canada Central
West Central US
West US 2
UK West
UK South
Central US EUAP
Korea Central
France Central
Norway East
```

<span data-ttu-id="dfa97-112">이 명령은 Linux에서 프리미엄을 사용할 수 있는 위치를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="dfa97-112">This command gets the locations where Premium is available for Linux.</span></span>

### <span data-ttu-id="dfa97-113">예제 3: Windows에서 소비를 사용할 수 있는 위치를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="dfa97-113">Example 3: Get the locations where Consumption is available for Windows.</span></span>
```powershell
PS C:\> Get-AzFunctionAppAvailableLocation -PlanType Consumption -OSType Windows

Name
----
Central US
North Europe
West Europe
Southeast Asia
East Asia
West US
East US
Japan West
Japan East
East US 2
North Central US
South Central US
Brazil South
Australia East
Australia Southeast
East Asia (Stage)
Central India
West India
South India
Canada Central
Canada East
West Central US
West US 2
UK West
UK South
East US 2 EUAP
Central US EUAP
Korea Central
France Central
Australia Central 2
Australia Central
South Africa North
Switzerland North
Germany West Central
```

<span data-ttu-id="dfa97-114">이 명령은 Windows에서 소비를 사용할 수 있는 위치를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="dfa97-114">This command gets the locations where Consumption is available for Windows.</span></span>

## <span data-ttu-id="dfa97-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dfa97-115">PARAMETERS</span></span>

### <span data-ttu-id="dfa97-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfa97-116">-DefaultProfile</span></span>
<span data-ttu-id="dfa97-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="dfa97-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfa97-118">-OSType</span><span class="sxs-lookup"><span data-stu-id="dfa97-118">-OSType</span></span>
<span data-ttu-id="dfa97-119">서비스 계획의 OS 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="dfa97-119">The OS type for the service plan.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfa97-120">-PlanType</span><span class="sxs-lookup"><span data-stu-id="dfa97-120">-PlanType</span></span>
<span data-ttu-id="dfa97-121">계획 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="dfa97-121">The plan type.</span></span>
<span data-ttu-id="dfa97-122">유효한 입력: 소비 또는 프리미엄</span><span class="sxs-lookup"><span data-stu-id="dfa97-122">Valid inputs: Consumption or Premium</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfa97-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="dfa97-123">-SubscriptionId</span></span>
<span data-ttu-id="dfa97-124">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="dfa97-124">The Azure subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfa97-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfa97-125">CommonParameters</span></span>
<span data-ttu-id="dfa97-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="dfa97-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfa97-127">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="dfa97-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfa97-128">입력</span><span class="sxs-lookup"><span data-stu-id="dfa97-128">INPUTS</span></span>

## <span data-ttu-id="dfa97-129">출력</span><span class="sxs-lookup"><span data-stu-id="dfa97-129">OUTPUTS</span></span>

### <span data-ttu-id="dfa97-130">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IGeoRegion</span><span class="sxs-lookup"><span data-stu-id="dfa97-130">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IGeoRegion</span></span>

## <span data-ttu-id="dfa97-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="dfa97-131">NOTES</span></span>

<span data-ttu-id="dfa97-132">별칭</span><span class="sxs-lookup"><span data-stu-id="dfa97-132">ALIASES</span></span>

## <span data-ttu-id="dfa97-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dfa97-133">RELATED LINKS</span></span>

