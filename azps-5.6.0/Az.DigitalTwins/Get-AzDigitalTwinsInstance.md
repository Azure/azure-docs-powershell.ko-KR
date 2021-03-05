---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/powershell/module/az.digitaltwins/get-azdigitaltwinsinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Get-AzDigitalTwinsInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Get-AzDigitalTwinsInstance.md
ms.openlocfilehash: 38f9aef513e13b2676569d434977752f3d193062
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985007"
---
# <span data-ttu-id="37ae7-101">Get-AzDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="37ae7-101">Get-AzDigitalTwinsInstance</span></span>

## <span data-ttu-id="37ae7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37ae7-102">SYNOPSIS</span></span>
<span data-ttu-id="37ae7-103">DigitalTwinsInstances 리소스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="37ae7-103">Get DigitalTwinsInstances resource.</span></span>

## <span data-ttu-id="37ae7-104">구문</span><span class="sxs-lookup"><span data-stu-id="37ae7-104">SYNTAX</span></span>

### <span data-ttu-id="37ae7-105">목록(기본값)</span><span class="sxs-lookup"><span data-stu-id="37ae7-105">List (Default)</span></span>
```
Get-AzDigitalTwinsInstance [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="37ae7-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="37ae7-106">Get</span></span>
```
Get-AzDigitalTwinsInstance -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="37ae7-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="37ae7-107">GetViaIdentity</span></span>
```
Get-AzDigitalTwinsInstance -InputObject <IDigitalTwinsIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="37ae7-108">List1</span><span class="sxs-lookup"><span data-stu-id="37ae7-108">List1</span></span>
```
Get-AzDigitalTwinsInstance -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="37ae7-109">설명</span><span class="sxs-lookup"><span data-stu-id="37ae7-109">DESCRIPTION</span></span>
<span data-ttu-id="37ae7-110">DigitalTwinsInstances 리소스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="37ae7-110">Get DigitalTwinsInstances resource.</span></span>

## <span data-ttu-id="37ae7-111">예제</span><span class="sxs-lookup"><span data-stu-id="37ae7-111">EXAMPLES</span></span>

### <span data-ttu-id="37ae7-112">예제 1: 목록(기본값)</span><span class="sxs-lookup"><span data-stu-id="37ae7-112">Example 1: List (Default)</span></span>
```powershell
PS C:\> Get-AzDigitalTwinsInstance

Location Name                    Type
-------- ----                    ----
eastus   youriDigitalTwinsTest   Microsoft.DigitalTwins/digitalTwinsInstances
eastus   youriDigitalTwin        Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="37ae7-113">기본적으로 모든 DigitalTwinsInstance를 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="37ae7-113">Get all the DigitalTwinsInstance by default</span></span>

### <span data-ttu-id="37ae7-114">예제 2: Get</span><span class="sxs-lookup"><span data-stu-id="37ae7-114">Example 2: Get</span></span>
```powershell
PS C:\> Get-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwin

Location Name             Type
-------- ----             ----
eastus   youriDigitalTwin Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="37ae7-115">ResourceName에서 지정된 AzDigitalTwinsInstance를 얻다</span><span class="sxs-lookup"><span data-stu-id="37ae7-115">Get the specified AzDigitalTwinsInstance by ResourceName</span></span>

### <span data-ttu-id="37ae7-116">예제 3: GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="37ae7-116">Example 3: GetViaIdentity</span></span>
```powershell
PS C:\> $NewAzDigital = New-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwin -Location eastus
Get-AzDigitalTwinsInstance -inputObject $NewAzDigital

Location Name             Type
-------- ----             ----
eastus   youriDigitalTwin Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="37ae7-117">지정된 AzDigitalTwinsInstance by Object</span><span class="sxs-lookup"><span data-stu-id="37ae7-117">Get the specified AzDigitalTwinsInstance by Object</span></span>

### <span data-ttu-id="37ae7-118">예제 4: List1</span><span class="sxs-lookup"><span data-stu-id="37ae7-118">Example 4: List1</span></span>
```powershell
PS C:\> Get-AzDigitalTwinsInstance -ResourceGroupName youritemp

Location Name                    Type
-------- ----                    ----
eastus   youriDigitalTwinsTest   Microsoft.DigitalTwins/digitalTwinsInstances
eastus   youriDigitalTwin        Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="37ae7-119">ResourceGroupName의 모든 DigitalTwinsInstance 사용</span><span class="sxs-lookup"><span data-stu-id="37ae7-119">Get all the DigitalTwinsInstance by ResourceGroupName</span></span>

## <span data-ttu-id="37ae7-120">매개 변수</span><span class="sxs-lookup"><span data-stu-id="37ae7-120">PARAMETERS</span></span>

### <span data-ttu-id="37ae7-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37ae7-121">-DefaultProfile</span></span>
<span data-ttu-id="37ae7-122">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="37ae7-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37ae7-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="37ae7-123">-InputObject</span></span>
<span data-ttu-id="37ae7-124">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="37ae7-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="37ae7-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37ae7-125">-ResourceGroupName</span></span>
<span data-ttu-id="37ae7-126">DigitalTwinsInstance를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="37ae7-126">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37ae7-127">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="37ae7-127">-ResourceName</span></span>
<span data-ttu-id="37ae7-128">DigitalTwinsInstance의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="37ae7-128">The name of the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="37ae7-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="37ae7-129">-SubscriptionId</span></span>
<span data-ttu-id="37ae7-130">구독 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="37ae7-130">The subscription identifier.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37ae7-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37ae7-131">CommonParameters</span></span>
<span data-ttu-id="37ae7-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="37ae7-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37ae7-133">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="37ae7-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37ae7-134">입력</span><span class="sxs-lookup"><span data-stu-id="37ae7-134">INPUTS</span></span>

### <span data-ttu-id="37ae7-135">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="37ae7-135">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span></span>

## <span data-ttu-id="37ae7-136">출력</span><span class="sxs-lookup"><span data-stu-id="37ae7-136">OUTPUTS</span></span>

### <span data-ttu-id="37ae7-137">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span><span class="sxs-lookup"><span data-stu-id="37ae7-137">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span></span>

## <span data-ttu-id="37ae7-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="37ae7-138">NOTES</span></span>

<span data-ttu-id="37ae7-139">별칭</span><span class="sxs-lookup"><span data-stu-id="37ae7-139">ALIASES</span></span>

<span data-ttu-id="37ae7-140">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="37ae7-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="37ae7-141">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="37ae7-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="37ae7-142">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="37ae7-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="37ae7-143">INPUTOBJECT <IDigitalTwinsIdentity> : ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="37ae7-143">INPUTOBJECT <IDigitalTwinsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="37ae7-144">`[EndpointName <String>]`: 엔드포인트 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="37ae7-144">`[EndpointName <String>]`: Name of Endpoint Resource.</span></span>
  - <span data-ttu-id="37ae7-145">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="37ae7-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="37ae7-146">`[Location <String>]`: DigitalTwinsInstance의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="37ae7-146">`[Location <String>]`: Location of DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="37ae7-147">`[ResourceGroupName <String>]`: DigitalTwinsInstance를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="37ae7-147">`[ResourceGroupName <String>]`: The name of the resource group that contains the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="37ae7-148">`[ResourceName <String>]`: DigitalTwinsInstance의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="37ae7-148">`[ResourceName <String>]`: The name of the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="37ae7-149">`[SubscriptionId <String>]`: 구독 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="37ae7-149">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="37ae7-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="37ae7-150">RELATED LINKS</span></span>

