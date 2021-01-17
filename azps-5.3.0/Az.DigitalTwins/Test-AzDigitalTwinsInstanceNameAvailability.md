---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.digitaltwins/test-azdigitaltwinsinstancenameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Test-AzDigitalTwinsInstanceNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Test-AzDigitalTwinsInstanceNameAvailability.md
ms.openlocfilehash: af911fc4eb4cccbd3f22e0d54a8aad2933b5db46
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489868"
---
# <span data-ttu-id="60ab5-101">Test-AzDigitalTwinsInstanceNameAvailability</span><span class="sxs-lookup"><span data-stu-id="60ab5-101">Test-AzDigitalTwinsInstanceNameAvailability</span></span>

## <span data-ttu-id="60ab5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60ab5-102">SYNOPSIS</span></span>
<span data-ttu-id="60ab5-103">DigitalTwinsInstance 이름을 사용할 수 있는지 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="60ab5-103">Check if a DigitalTwinsInstance name is available.</span></span>

## <span data-ttu-id="60ab5-104">구문</span><span class="sxs-lookup"><span data-stu-id="60ab5-104">SYNTAX</span></span>

### <span data-ttu-id="60ab5-105">CheckExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="60ab5-105">CheckExpanded (Default)</span></span>
```
Test-AzDigitalTwinsInstanceNameAvailability -Location <String> -Name <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="60ab5-106">확인</span><span class="sxs-lookup"><span data-stu-id="60ab5-106">Check</span></span>
```
Test-AzDigitalTwinsInstanceNameAvailability -Location <String>
 -DigitalTwinsInstanceCheckName <ICheckNameRequest> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="60ab5-107">CheckViaIdentity</span><span class="sxs-lookup"><span data-stu-id="60ab5-107">CheckViaIdentity</span></span>
```
Test-AzDigitalTwinsInstanceNameAvailability -InputObject <IDigitalTwinsIdentity>
 -DigitalTwinsInstanceCheckName <ICheckNameRequest> [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="60ab5-108">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="60ab5-108">CheckViaIdentityExpanded</span></span>
```
Test-AzDigitalTwinsInstanceNameAvailability -InputObject <IDigitalTwinsIdentity> -Name <String>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="60ab5-109">설명</span><span class="sxs-lookup"><span data-stu-id="60ab5-109">DESCRIPTION</span></span>
<span data-ttu-id="60ab5-110">DigitalTwinsInstance 이름을 사용할 수 있는지 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="60ab5-110">Check if a DigitalTwinsInstance name is available.</span></span>

## <span data-ttu-id="60ab5-111">예제</span><span class="sxs-lookup"><span data-stu-id="60ab5-111">EXAMPLES</span></span>

### <span data-ttu-id="60ab5-112">예제 1: 위치 및 이름으로 이름을 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="60ab5-112">Example 1: Check the name by location and name.</span></span>
```powershell
PS C:\> Test-AzDigitalTwinsInstanceNameAvailability -Location eastus -name youriTestName

Message                       NameAvailable Reason
-------                       ------------- ------
'youriTestName' is available. True
```

<span data-ttu-id="60ab5-113">위치 및 이름에 따라 이름의 가용성을 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="60ab5-113">Check the availability of the name by location and name.</span></span>

### <span data-ttu-id="60ab5-114">예제 2: DigitalTwinsObject 및 CheckNameObject로 이름을 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="60ab5-114">Example 2: Check the name by DigitalTwinsObject and CheckNameObject.</span></span>
```powershell
PS C:\> $getAzDT =Get-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest 
$checkName = New-AzDigitalTwinsCheckNameRequestObject -name youriTestName
Test-AzDigitalTwinsInstanceNameAvailability -InputObject $getAzDT -DigitalTwinsInstanceCheckName $checkName

Message                     NameAvailable Reason
-------                     ------------- ------
'youriTestName' is available. True
```

<span data-ttu-id="60ab5-115">DigitalTwinsInstance를 만들고 이름의 가용성을 테스트하는 Requset 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="60ab5-115">Get A DigitalTwinsInstance and create a Requset Object to Test the availability of the name.</span></span>

## <span data-ttu-id="60ab5-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="60ab5-116">PARAMETERS</span></span>

### <span data-ttu-id="60ab5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60ab5-117">-DefaultProfile</span></span>
<span data-ttu-id="60ab5-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="60ab5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60ab5-119">-DigitalTwinsInstanceCheckName</span><span class="sxs-lookup"><span data-stu-id="60ab5-119">-DigitalTwinsInstanceCheckName</span></span>
<span data-ttu-id="60ab5-120">데이터베이스에서 반환된 결과 이름 가용성 확인 요청입니다.</span><span class="sxs-lookup"><span data-stu-id="60ab5-120">The result returned from a database check name availability request.</span></span>
<span data-ttu-id="60ab5-121">생성을 위해 DIGITALTWINSINSTANCECHECKNAME 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="60ab5-121">To construct, see NOTES section for DIGITALTWINSINSTANCECHECKNAME properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.ICheckNameRequest
Parameter Sets: Check, CheckViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="60ab5-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="60ab5-122">-InputObject</span></span>
<span data-ttu-id="60ab5-123">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="60ab5-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity
Parameter Sets: CheckViaIdentity, CheckViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="60ab5-124">-Location</span><span class="sxs-lookup"><span data-stu-id="60ab5-124">-Location</span></span>
<span data-ttu-id="60ab5-125">DigitalTwinsInstance의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="60ab5-125">Location of DigitalTwinsInstance.</span></span>

```yaml
Type: System.String
Parameter Sets: Check, CheckExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60ab5-126">-Name</span><span class="sxs-lookup"><span data-stu-id="60ab5-126">-Name</span></span>
<span data-ttu-id="60ab5-127">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="60ab5-127">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: CheckExpanded, CheckViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60ab5-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="60ab5-128">-SubscriptionId</span></span>
<span data-ttu-id="60ab5-129">구독 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="60ab5-129">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Check, CheckExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60ab5-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="60ab5-130">-Confirm</span></span>
<span data-ttu-id="60ab5-131">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="60ab5-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60ab5-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60ab5-132">-WhatIf</span></span>
<span data-ttu-id="60ab5-133">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="60ab5-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60ab5-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="60ab5-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60ab5-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60ab5-135">CommonParameters</span></span>
<span data-ttu-id="60ab5-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="60ab5-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60ab5-137">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="60ab5-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60ab5-138">입력</span><span class="sxs-lookup"><span data-stu-id="60ab5-138">INPUTS</span></span>

### <span data-ttu-id="60ab5-139">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.ICheckNameRequest</span><span class="sxs-lookup"><span data-stu-id="60ab5-139">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.ICheckNameRequest</span></span>

### <span data-ttu-id="60ab5-140">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="60ab5-140">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span></span>

## <span data-ttu-id="60ab5-141">출력</span><span class="sxs-lookup"><span data-stu-id="60ab5-141">OUTPUTS</span></span>

### <span data-ttu-id="60ab5-142">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.ICheckNameResult</span><span class="sxs-lookup"><span data-stu-id="60ab5-142">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.ICheckNameResult</span></span>

## <span data-ttu-id="60ab5-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="60ab5-143">NOTES</span></span>

<span data-ttu-id="60ab5-144">별칭</span><span class="sxs-lookup"><span data-stu-id="60ab5-144">ALIASES</span></span>

<span data-ttu-id="60ab5-145">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="60ab5-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="60ab5-146">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="60ab5-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="60ab5-147">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="60ab5-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="60ab5-148">DIGITALTWINSINSTANCECHECKNAME: 데이터베이스 이름 확인 가용성 요청에서 <ICheckNameRequest> 반환된 결과입니다.</span><span class="sxs-lookup"><span data-stu-id="60ab5-148">DIGITALTWINSINSTANCECHECKNAME <ICheckNameRequest>: The result returned from a database check name availability request.</span></span>
  - <span data-ttu-id="60ab5-149">`Name <String>`: 리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="60ab5-149">`Name <String>`: Resource name.</span></span>

<span data-ttu-id="60ab5-150">INPUTOBJECT: <IDigitalTwinsIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="60ab5-150">INPUTOBJECT <IDigitalTwinsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="60ab5-151">`[EndpointName <String>]`: 엔드포인트 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="60ab5-151">`[EndpointName <String>]`: Name of Endpoint Resource.</span></span>
  - <span data-ttu-id="60ab5-152">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="60ab5-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="60ab5-153">`[Location <String>]`: DigitalTwinsInstance의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="60ab5-153">`[Location <String>]`: Location of DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="60ab5-154">`[ResourceGroupName <String>]`: DigitalTwinsInstance를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="60ab5-154">`[ResourceGroupName <String>]`: The name of the resource group that contains the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="60ab5-155">`[ResourceName <String>]`: DigitalTwinsInstance의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="60ab5-155">`[ResourceName <String>]`: The name of the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="60ab5-156">`[SubscriptionId <String>]`: 구독 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="60ab5-156">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="60ab5-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="60ab5-157">RELATED LINKS</span></span>

