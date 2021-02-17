---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.digitaltwins/get-azdigitaltwinsendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Get-AzDigitalTwinsEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Get-AzDigitalTwinsEndpoint.md
ms.openlocfilehash: 6299fcc8828031b61aabc912fcd30c1ed8cbb0e2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188513"
---
# <span data-ttu-id="b1c9e-101">Get-AzDigitalTwinsEndpoint</span><span class="sxs-lookup"><span data-stu-id="b1c9e-101">Get-AzDigitalTwinsEndpoint</span></span>

## <span data-ttu-id="b1c9e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1c9e-102">SYNOPSIS</span></span>
<span data-ttu-id="b1c9e-103">DigitalTwinsInstances 엔드포인트를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b1c9e-103">Get DigitalTwinsInstances Endpoint.</span></span>

## <span data-ttu-id="b1c9e-104">구문</span><span class="sxs-lookup"><span data-stu-id="b1c9e-104">SYNTAX</span></span>

### <span data-ttu-id="b1c9e-105">목록(기본값)</span><span class="sxs-lookup"><span data-stu-id="b1c9e-105">List (Default)</span></span>
```
Get-AzDigitalTwinsEndpoint -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b1c9e-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="b1c9e-106">Get</span></span>
```
Get-AzDigitalTwinsEndpoint -EndpointName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b1c9e-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b1c9e-107">GetViaIdentity</span></span>
```
Get-AzDigitalTwinsEndpoint -InputObject <IDigitalTwinsIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="b1c9e-108">설명</span><span class="sxs-lookup"><span data-stu-id="b1c9e-108">DESCRIPTION</span></span>
<span data-ttu-id="b1c9e-109">DigitalTwinsInstances 엔드포인트를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b1c9e-109">Get DigitalTwinsInstances Endpoint.</span></span>

## <span data-ttu-id="b1c9e-110">예제</span><span class="sxs-lookup"><span data-stu-id="b1c9e-110">EXAMPLES</span></span>

### <span data-ttu-id="b1c9e-111">예제 1: ResourceGroup에서 AzDigitalTwinsEndpoint 나열</span><span class="sxs-lookup"><span data-stu-id="b1c9e-111">Example 1: List AzDigitalTwinsEndpoint in ResourceGroup</span></span>
```powershell
PS C:\> Get-AzDigitalTwinsEndpoint -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest

Name                     Type
----                     ----
youriDigitalTwinEndpoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="b1c9e-112">ResourceGroupName의 모든 AzDigitalTwinsEndpoints 나열</span><span class="sxs-lookup"><span data-stu-id="b1c9e-112">List all AzDigitalTwinsEndpoints by ResourceGroupName</span></span>

### <span data-ttu-id="b1c9e-113">예제 2: EndpointName으로 AzDigitalTwinsEndpoint Get</span><span class="sxs-lookup"><span data-stu-id="b1c9e-113">Example 2: Get AzDigitalTwinsEndpoint by EndpointName</span></span>
```powershell
PS C:\> Get-AzDigitalTwinsEndpoint -EndpointName youriDigitalTwinEndpoint -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest

Name                     Type
----                     ----
youriDigitalTwinEndpoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="b1c9e-114">ResourceGroup에서 EndpointName으로 AzDigitalTwinsEndpoint를 Get</span><span class="sxs-lookup"><span data-stu-id="b1c9e-114">Get AzDigitalTwinsEndpoint by EndpointName in ResourceGroup</span></span>

### <span data-ttu-id="b1c9e-115">예제 3: 'AzDigitalTwinsEndpoint' 개체로 AzDigitalTwinsEndpoint Get</span><span class="sxs-lookup"><span data-stu-id="b1c9e-115">Example 3: Get AzDigitalTwinsEndpoint by 'AzDigitalTwinsEndpoint' Object</span></span>
```powershell
PS C:\> $GetAzDigitalTwinsEndpoint = Get-AzDigitalTwinsEndpoint -EndpointName youriDigitalTwinEndpoint -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest
Get-AzDigitalTwinsEndpoint -InputObject $GetAzDigitalTwinsEndpoint

Name                     Type
----                     ----
youriDigitalTwinEndpoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="b1c9e-116">'AzDigitalTwinsEndpoint' 개체로 AzDigitalTwinsEndpoint를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b1c9e-116">Get AzDigitalTwinsEndpoint by 'AzDigitalTwinsEndpoint' Object</span></span>

## <span data-ttu-id="b1c9e-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b1c9e-117">PARAMETERS</span></span>

### <span data-ttu-id="b1c9e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1c9e-118">-DefaultProfile</span></span>
<span data-ttu-id="b1c9e-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b1c9e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1c9e-120">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="b1c9e-120">-EndpointName</span></span>
<span data-ttu-id="b1c9e-121">엔드포인트 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b1c9e-121">Name of Endpoint Resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1c9e-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b1c9e-122">-InputObject</span></span>
<span data-ttu-id="b1c9e-123">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="b1c9e-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b1c9e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1c9e-124">-ResourceGroupName</span></span>
<span data-ttu-id="b1c9e-125">DigitalTwinsInstance를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b1c9e-125">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1c9e-126">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="b1c9e-126">-ResourceName</span></span>
<span data-ttu-id="b1c9e-127">DigitalTwinsInstance의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b1c9e-127">The name of the DigitalTwinsInstance.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1c9e-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b1c9e-128">-SubscriptionId</span></span>
<span data-ttu-id="b1c9e-129">구독 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="b1c9e-129">The subscription identifier.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1c9e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1c9e-130">CommonParameters</span></span>
<span data-ttu-id="b1c9e-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b1c9e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1c9e-132">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b1c9e-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1c9e-133">입력</span><span class="sxs-lookup"><span data-stu-id="b1c9e-133">INPUTS</span></span>

### <span data-ttu-id="b1c9e-134">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="b1c9e-134">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span></span>

## <span data-ttu-id="b1c9e-135">출력</span><span class="sxs-lookup"><span data-stu-id="b1c9e-135">OUTPUTS</span></span>

### <span data-ttu-id="b1c9e-136">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span><span class="sxs-lookup"><span data-stu-id="b1c9e-136">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span></span>

## <span data-ttu-id="b1c9e-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b1c9e-137">NOTES</span></span>

<span data-ttu-id="b1c9e-138">별칭</span><span class="sxs-lookup"><span data-stu-id="b1c9e-138">ALIASES</span></span>

<span data-ttu-id="b1c9e-139">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="b1c9e-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b1c9e-140">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="b1c9e-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b1c9e-141">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b1c9e-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b1c9e-142">INPUTOBJECT: <IDigitalTwinsIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="b1c9e-142">INPUTOBJECT <IDigitalTwinsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b1c9e-143">`[EndpointName <String>]`: 엔드포인트 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b1c9e-143">`[EndpointName <String>]`: Name of Endpoint Resource.</span></span>
  - <span data-ttu-id="b1c9e-144">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="b1c9e-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b1c9e-145">`[Location <String>]`: DigitalTwinsInstance의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="b1c9e-145">`[Location <String>]`: Location of DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="b1c9e-146">`[ResourceGroupName <String>]`: DigitalTwinsInstance를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b1c9e-146">`[ResourceGroupName <String>]`: The name of the resource group that contains the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="b1c9e-147">`[ResourceName <String>]`: DigitalTwinsInstance의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b1c9e-147">`[ResourceName <String>]`: The name of the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="b1c9e-148">`[SubscriptionId <String>]`: 구독 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="b1c9e-148">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="b1c9e-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b1c9e-149">RELATED LINKS</span></span>

