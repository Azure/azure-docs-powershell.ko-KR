---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.digitaltwins/update-azdigitaltwinsinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Update-AzDigitalTwinsInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Update-AzDigitalTwinsInstance.md
ms.openlocfilehash: 4de7ab82f60c651e23565569ccf2cda7f4d949b5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491985"
---
# <span data-ttu-id="d7f0f-101">Update-AzDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="d7f0f-101">Update-AzDigitalTwinsInstance</span></span>

## <span data-ttu-id="d7f0f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7f0f-102">SYNOPSIS</span></span>
<span data-ttu-id="d7f0f-103">DigitalTwinsInstance의 메타데이터를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="d7f0f-103">Update metadata of DigitalTwinsInstance.</span></span>

## <span data-ttu-id="d7f0f-104">구문</span><span class="sxs-lookup"><span data-stu-id="d7f0f-104">SYNTAX</span></span>

### <span data-ttu-id="d7f0f-105">UpdateExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="d7f0f-105">UpdateExpanded (Default)</span></span>
```
Update-AzDigitalTwinsInstance -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d7f0f-106">업데이트</span><span class="sxs-lookup"><span data-stu-id="d7f0f-106">Update</span></span>
```
Update-AzDigitalTwinsInstance -ResourceGroupName <String> -ResourceName <String>
 -DigitalTwinsPatchDescription <IDigitalTwinsPatchDescription> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d7f0f-107">UpdateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d7f0f-107">UpdateViaIdentity</span></span>
```
Update-AzDigitalTwinsInstance -InputObject <IDigitalTwinsIdentity>
 -DigitalTwinsPatchDescription <IDigitalTwinsPatchDescription> [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d7f0f-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="d7f0f-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzDigitalTwinsInstance -InputObject <IDigitalTwinsIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d7f0f-109">설명</span><span class="sxs-lookup"><span data-stu-id="d7f0f-109">DESCRIPTION</span></span>
<span data-ttu-id="d7f0f-110">DigitalTwinsInstance의 메타데이터를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="d7f0f-110">Update metadata of DigitalTwinsInstance.</span></span>

## <span data-ttu-id="d7f0f-111">예제</span><span class="sxs-lookup"><span data-stu-id="d7f0f-111">EXAMPLES</span></span>

### <span data-ttu-id="d7f0f-112">예제 1: UpdateExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="d7f0f-112">Example 1: UpdateExpanded (Default)</span></span>
```powershell
PS C:\> Update-AzDigitalTwinsInstance -ResourcegroupName youritemp -ResourceName youriDigitalTwinsTest -Tag @{“dtt”="001"}

Location Name                  Type
-------- ----                  ----
eastus   youriDigitalTwinsTest Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="d7f0f-113">ResourceGroupName에 의해 지정된 DigitalTwinsInstance 업데이트</span><span class="sxs-lookup"><span data-stu-id="d7f0f-113">Update the specified DigitalTwinsInstance by ResourceGroupName</span></span>

### <span data-ttu-id="d7f0f-114">예제 2: 다른 AzDigitalTwinsInstance에 의해 AzDigitalTwinsInstance 업데이트</span><span class="sxs-lookup"><span data-stu-id="d7f0f-114">Example 2: Update the AzDigitalTwinsInstance by another AzDigitalTwinsInstance</span></span>
```powershell
PS C:\> $updateDigitalTwinInstance1 = Update-AzDigitalTwinsInstance -ResourcegroupName youritemp -ResourceName youriDigitalTwin1 -Tag @{"dtt"="002"}
Update-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest -DigitalTwinsPatchDescription $updateDigitalTwinInstance1

Location Name                  Type
-------- ----                  ----
eastus   youriDigitalTwinsTest Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="d7f0f-115">다른 AzDigitalTwinsInstance에 의해 AzDigitalTwinsInstance 업데이트</span><span class="sxs-lookup"><span data-stu-id="d7f0f-115">Update the AzDigitalTwinsInstance by another AzDigitalTwinsInstance</span></span>

## <span data-ttu-id="d7f0f-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d7f0f-116">PARAMETERS</span></span>

### <span data-ttu-id="d7f0f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7f0f-117">-DefaultProfile</span></span>
<span data-ttu-id="d7f0f-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d7f0f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7f0f-119">-DigitalTwinsPatchDescription</span><span class="sxs-lookup"><span data-stu-id="d7f0f-119">-DigitalTwinsPatchDescription</span></span>
<span data-ttu-id="d7f0f-120">DigitalTwins 서비스에 대한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="d7f0f-120">The description of the DigitalTwins service.</span></span>
<span data-ttu-id="d7f0f-121">생성을 위해 DIGITALTWINSPATCHDESCRIPTION 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="d7f0f-121">To construct, see NOTES section for DIGITALTWINSPATCHDESCRIPTION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsPatchDescription
Parameter Sets: Update, UpdateViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d7f0f-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d7f0f-122">-InputObject</span></span>
<span data-ttu-id="d7f0f-123">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="d7f0f-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity
Parameter Sets: UpdateViaIdentity, UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d7f0f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7f0f-124">-ResourceGroupName</span></span>
<span data-ttu-id="d7f0f-125">DigitalTwinsInstance를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d7f0f-125">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

```yaml
Type: System.String
Parameter Sets: Update, UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7f0f-126">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="d7f0f-126">-ResourceName</span></span>
<span data-ttu-id="d7f0f-127">DigitalTwinsInstance의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d7f0f-127">The name of the DigitalTwinsInstance.</span></span>

```yaml
Type: System.String
Parameter Sets: Update, UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7f0f-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d7f0f-128">-SubscriptionId</span></span>
<span data-ttu-id="d7f0f-129">구독 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="d7f0f-129">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Update, UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7f0f-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="d7f0f-130">-Tag</span></span>
<span data-ttu-id="d7f0f-131">인스턴스 태그</span><span class="sxs-lookup"><span data-stu-id="d7f0f-131">Instance tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7f0f-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d7f0f-132">-Confirm</span></span>
<span data-ttu-id="d7f0f-133">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d7f0f-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7f0f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7f0f-134">-WhatIf</span></span>
<span data-ttu-id="d7f0f-135">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="d7f0f-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7f0f-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d7f0f-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7f0f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7f0f-137">CommonParameters</span></span>
<span data-ttu-id="d7f0f-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d7f0f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7f0f-139">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d7f0f-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7f0f-140">입력</span><span class="sxs-lookup"><span data-stu-id="d7f0f-140">INPUTS</span></span>

### <span data-ttu-id="d7f0f-141">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsPatchDescription</span><span class="sxs-lookup"><span data-stu-id="d7f0f-141">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsPatchDescription</span></span>

### <span data-ttu-id="d7f0f-142">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="d7f0f-142">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span></span>

## <span data-ttu-id="d7f0f-143">출력</span><span class="sxs-lookup"><span data-stu-id="d7f0f-143">OUTPUTS</span></span>

### <span data-ttu-id="d7f0f-144">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span><span class="sxs-lookup"><span data-stu-id="d7f0f-144">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span></span>

## <span data-ttu-id="d7f0f-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d7f0f-145">NOTES</span></span>

<span data-ttu-id="d7f0f-146">별칭</span><span class="sxs-lookup"><span data-stu-id="d7f0f-146">ALIASES</span></span>

<span data-ttu-id="d7f0f-147">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="d7f0f-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d7f0f-148">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="d7f0f-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d7f0f-149">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d7f0f-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d7f0f-150">DIGITALTWINSPATCHDESCRIPTION: <IDigitalTwinsPatchDescription> DigitalTwins 서비스에 대한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="d7f0f-150">DIGITALTWINSPATCHDESCRIPTION <IDigitalTwinsPatchDescription>: The description of the DigitalTwins service.</span></span>
  - <span data-ttu-id="d7f0f-151">`[Tag <IDigitalTwinsPatchDescriptionTags>]`: 인스턴스 태그</span><span class="sxs-lookup"><span data-stu-id="d7f0f-151">`[Tag <IDigitalTwinsPatchDescriptionTags>]`: Instance tags</span></span>
    - <span data-ttu-id="d7f0f-152">`[(Any) <String>]`: 이 개체에 추가할 수 있는 속성을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="d7f0f-152">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>

<span data-ttu-id="d7f0f-153">INPUTOBJECT: <IDigitalTwinsIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="d7f0f-153">INPUTOBJECT <IDigitalTwinsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d7f0f-154">`[EndpointName <String>]`: 엔드포인트 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d7f0f-154">`[EndpointName <String>]`: Name of Endpoint Resource.</span></span>
  - <span data-ttu-id="d7f0f-155">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="d7f0f-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d7f0f-156">`[Location <String>]`: DigitalTwinsInstance의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="d7f0f-156">`[Location <String>]`: Location of DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="d7f0f-157">`[ResourceGroupName <String>]`: DigitalTwinsInstance를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d7f0f-157">`[ResourceGroupName <String>]`: The name of the resource group that contains the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="d7f0f-158">`[ResourceName <String>]`: DigitalTwinsInstance의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d7f0f-158">`[ResourceName <String>]`: The name of the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="d7f0f-159">`[SubscriptionId <String>]`: 구독 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="d7f0f-159">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="d7f0f-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d7f0f-160">RELATED LINKS</span></span>

