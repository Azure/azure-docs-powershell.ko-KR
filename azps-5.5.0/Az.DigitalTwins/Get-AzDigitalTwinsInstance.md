---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.digitaltwins/get-azdigitaltwinsinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Get-AzDigitalTwinsInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Get-AzDigitalTwinsInstance.md
ms.openlocfilehash: 17e036128dcc6c43044a83d2bbc254cc994ae508
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204165"
---
# <span data-ttu-id="efd94-101">Get-AzDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="efd94-101">Get-AzDigitalTwinsInstance</span></span>

## <span data-ttu-id="efd94-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="efd94-102">SYNOPSIS</span></span>
<span data-ttu-id="efd94-103">DigitalTwinsInstances 리소스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="efd94-103">Get DigitalTwinsInstances resource.</span></span>

## <span data-ttu-id="efd94-104">구문</span><span class="sxs-lookup"><span data-stu-id="efd94-104">SYNTAX</span></span>

### <span data-ttu-id="efd94-105">목록(기본값)</span><span class="sxs-lookup"><span data-stu-id="efd94-105">List (Default)</span></span>
```
Get-AzDigitalTwinsInstance [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="efd94-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="efd94-106">Get</span></span>
```
Get-AzDigitalTwinsInstance -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="efd94-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="efd94-107">GetViaIdentity</span></span>
```
Get-AzDigitalTwinsInstance -InputObject <IDigitalTwinsIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="efd94-108">List1</span><span class="sxs-lookup"><span data-stu-id="efd94-108">List1</span></span>
```
Get-AzDigitalTwinsInstance -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="efd94-109">설명</span><span class="sxs-lookup"><span data-stu-id="efd94-109">DESCRIPTION</span></span>
<span data-ttu-id="efd94-110">DigitalTwinsInstances 리소스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="efd94-110">Get DigitalTwinsInstances resource.</span></span>

## <span data-ttu-id="efd94-111">예제</span><span class="sxs-lookup"><span data-stu-id="efd94-111">EXAMPLES</span></span>

### <span data-ttu-id="efd94-112">예제 1: 목록(기본값)</span><span class="sxs-lookup"><span data-stu-id="efd94-112">Example 1: List (Default)</span></span>
```powershell
PS C:\> Get-AzDigitalTwinsInstance

Location Name                    Type
-------- ----                    ----
eastus   youriDigitalTwinsTest   Microsoft.DigitalTwins/digitalTwinsInstances
eastus   youriDigitalTwin        Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="efd94-113">기본적으로 모든 DigitalTwinsInstance를 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="efd94-113">Get all the DigitalTwinsInstance by default</span></span>

### <span data-ttu-id="efd94-114">예제 2: Get</span><span class="sxs-lookup"><span data-stu-id="efd94-114">Example 2: Get</span></span>
```powershell
PS C:\> Get-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwin

Location Name             Type
-------- ----             ----
eastus   youriDigitalTwin Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="efd94-115">ResourceName에서 지정된 AzDigitalTwinsInstance를 얻게 합니다.</span><span class="sxs-lookup"><span data-stu-id="efd94-115">Get the specified AzDigitalTwinsInstance by ResourceName</span></span>

### <span data-ttu-id="efd94-116">예제 3: GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="efd94-116">Example 3: GetViaIdentity</span></span>
```powershell
PS C:\> $NewAzDigital = New-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwin -Location eastus
Get-AzDigitalTwinsInstance -inputObject $NewAzDigital

Location Name             Type
-------- ----             ----
eastus   youriDigitalTwin Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="efd94-117">지정된 AzDigitalTwinsInstance by Object를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="efd94-117">Get the specified AzDigitalTwinsInstance by Object</span></span>

### <span data-ttu-id="efd94-118">예제 4: List1</span><span class="sxs-lookup"><span data-stu-id="efd94-118">Example 4: List1</span></span>
```powershell
PS C:\> Get-AzDigitalTwinsInstance -ResourceGroupName youritemp

Location Name                    Type
-------- ----                    ----
eastus   youriDigitalTwinsTest   Microsoft.DigitalTwins/digitalTwinsInstances
eastus   youriDigitalTwin        Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="efd94-119">ResourceGroupName에 의해 모든 DigitalTwinsInstance를 얻게</span><span class="sxs-lookup"><span data-stu-id="efd94-119">Get all the DigitalTwinsInstance by ResourceGroupName</span></span>

## <span data-ttu-id="efd94-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="efd94-120">PARAMETERS</span></span>

### <span data-ttu-id="efd94-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efd94-121">-DefaultProfile</span></span>
<span data-ttu-id="efd94-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="efd94-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="efd94-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="efd94-123">-InputObject</span></span>
<span data-ttu-id="efd94-124">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="efd94-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="efd94-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="efd94-125">-ResourceGroupName</span></span>
<span data-ttu-id="efd94-126">DigitalTwinsInstance를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="efd94-126">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="efd94-127">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="efd94-127">-ResourceName</span></span>
<span data-ttu-id="efd94-128">DigitalTwinsInstance의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="efd94-128">The name of the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="efd94-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="efd94-129">-SubscriptionId</span></span>
<span data-ttu-id="efd94-130">구독 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="efd94-130">The subscription identifier.</span></span>

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

### <span data-ttu-id="efd94-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efd94-131">CommonParameters</span></span>
<span data-ttu-id="efd94-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="efd94-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efd94-133">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="efd94-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efd94-134">입력</span><span class="sxs-lookup"><span data-stu-id="efd94-134">INPUTS</span></span>

### <span data-ttu-id="efd94-135">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="efd94-135">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span></span>

## <span data-ttu-id="efd94-136">출력</span><span class="sxs-lookup"><span data-stu-id="efd94-136">OUTPUTS</span></span>

### <span data-ttu-id="efd94-137">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span><span class="sxs-lookup"><span data-stu-id="efd94-137">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span></span>

## <span data-ttu-id="efd94-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="efd94-138">NOTES</span></span>

<span data-ttu-id="efd94-139">별칭</span><span class="sxs-lookup"><span data-stu-id="efd94-139">ALIASES</span></span>

<span data-ttu-id="efd94-140">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="efd94-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="efd94-141">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="efd94-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="efd94-142">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="efd94-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="efd94-143">INPUTOBJECT: <IDigitalTwinsIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="efd94-143">INPUTOBJECT <IDigitalTwinsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="efd94-144">`[EndpointName <String>]`: 엔드포인트 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="efd94-144">`[EndpointName <String>]`: Name of Endpoint Resource.</span></span>
  - <span data-ttu-id="efd94-145">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="efd94-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="efd94-146">`[Location <String>]`: DigitalTwinsInstance의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="efd94-146">`[Location <String>]`: Location of DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="efd94-147">`[ResourceGroupName <String>]`: DigitalTwinsInstance를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="efd94-147">`[ResourceGroupName <String>]`: The name of the resource group that contains the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="efd94-148">`[ResourceName <String>]`: DigitalTwinsInstance의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="efd94-148">`[ResourceName <String>]`: The name of the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="efd94-149">`[SubscriptionId <String>]`: 구독 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="efd94-149">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="efd94-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="efd94-150">RELATED LINKS</span></span>

