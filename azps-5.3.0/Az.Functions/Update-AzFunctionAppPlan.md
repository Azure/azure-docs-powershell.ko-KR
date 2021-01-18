---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/update-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionAppPlan.md
ms.openlocfilehash: e0831e95a5601d3558af7089825684cc48e7838c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492972"
---
# <span data-ttu-id="acd75-101">Update-AzFunctionAppPlan</span><span class="sxs-lookup"><span data-stu-id="acd75-101">Update-AzFunctionAppPlan</span></span>

## <span data-ttu-id="acd75-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="acd75-102">SYNOPSIS</span></span>
<span data-ttu-id="acd75-103">함수 앱 서비스 계획을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="acd75-103">Updates a function app service plan.</span></span>

## <span data-ttu-id="acd75-104">구문</span><span class="sxs-lookup"><span data-stu-id="acd75-104">SYNTAX</span></span>

### <span data-ttu-id="acd75-105">ByName(기본값)</span><span class="sxs-lookup"><span data-stu-id="acd75-105">ByName (Default)</span></span>
```
Update-AzFunctionAppPlan -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-MaximumWorkerCount <Int32>] [-MinimumWorkerCount <Int32>] [-Sku <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="acd75-106">ByObjectInput</span><span class="sxs-lookup"><span data-stu-id="acd75-106">ByObjectInput</span></span>
```
Update-AzFunctionAppPlan -InputObject <IAppServicePlan> [-MaximumWorkerCount <Int32>]
 [-MinimumWorkerCount <Int32>] [-Sku <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="acd75-107">설명</span><span class="sxs-lookup"><span data-stu-id="acd75-107">DESCRIPTION</span></span>
<span data-ttu-id="acd75-108">함수 앱 서비스 계획을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="acd75-108">Updates a function app service plan.</span></span>

## <span data-ttu-id="acd75-109">예제</span><span class="sxs-lookup"><span data-stu-id="acd75-109">EXAMPLES</span></span>

### <span data-ttu-id="acd75-110">예제 1: 최대 작업자 20명으로 App Service 계획을 EP2 sku로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="acd75-110">Example 1: Update an app service plan to EP2 sku with twenty maximum workers.</span></span>
```powershell
PS C:\> Update-AzFunctionAppPlan -ResourceGroupName MyResourceGroupName `
                                 -Name MyPremiumPlan `
                                 -MaximumWorkerCount 20 `
                                 -Sku EP2

```

<span data-ttu-id="acd75-111">이 명령은 최대 20개 작업자를 사용하여 App Service 계획을 EP2 sku로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="acd75-111">This command updates an app service plan to EP2 sku with twenty maximum workers.</span></span>

## <span data-ttu-id="acd75-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="acd75-112">PARAMETERS</span></span>

### <span data-ttu-id="acd75-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="acd75-113">-AsJob</span></span>
<span data-ttu-id="acd75-114">명령을 작업으로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="acd75-114">Run the command as a job.</span></span>

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

### <span data-ttu-id="acd75-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acd75-115">-DefaultProfile</span></span>


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

### <span data-ttu-id="acd75-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="acd75-116">-InputObject</span></span>
<span data-ttu-id="acd75-117">생성을 위해 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="acd75-117">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan
Parameter Sets: ByObjectInput
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="acd75-118">-MaximumWorkerCount</span><span class="sxs-lookup"><span data-stu-id="acd75-118">-MaximumWorkerCount</span></span>
<span data-ttu-id="acd75-119">App Service 계획에 대한 최대 작업자 수입니다.</span><span class="sxs-lookup"><span data-stu-id="acd75-119">The maximum number of workers for the app service plan.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: MaxBurst

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acd75-120">-MinimumWorkerCount</span><span class="sxs-lookup"><span data-stu-id="acd75-120">-MinimumWorkerCount</span></span>
<span data-ttu-id="acd75-121">App Service 계획에 대한 최소 작업자 수입니다.</span><span class="sxs-lookup"><span data-stu-id="acd75-121">The minimum number of workers for the app service plan.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: MinInstances

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acd75-122">-Name</span><span class="sxs-lookup"><span data-stu-id="acd75-122">-Name</span></span>
<span data-ttu-id="acd75-123">App Service 계획의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="acd75-123">Name of the App Service plan.</span></span>

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

### <span data-ttu-id="acd75-124">-NoWait</span><span class="sxs-lookup"><span data-stu-id="acd75-124">-NoWait</span></span>
<span data-ttu-id="acd75-125">명령을 비동기적으로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="acd75-125">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="acd75-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="acd75-126">-ResourceGroupName</span></span>
<span data-ttu-id="acd75-127">리소스가 속한 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="acd75-127">Name of the resource group to which the resource belongs.</span></span>

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

### <span data-ttu-id="acd75-128">-Sku</span><span class="sxs-lookup"><span data-stu-id="acd75-128">-Sku</span></span>
<span data-ttu-id="acd75-129">계획 SKU입니다.</span><span class="sxs-lookup"><span data-stu-id="acd75-129">The plan sku.</span></span>
<span data-ttu-id="acd75-130">유효한 입력은 EP1, EP2, EP3입니다.</span><span class="sxs-lookup"><span data-stu-id="acd75-130">Valid inputs are: EP1, EP2, EP3</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acd75-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="acd75-131">-SubscriptionId</span></span>
<span data-ttu-id="acd75-132">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="acd75-132">The Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acd75-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="acd75-133">-Tag</span></span>
<span data-ttu-id="acd75-134">리소스 태그.</span><span class="sxs-lookup"><span data-stu-id="acd75-134">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acd75-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="acd75-135">-Confirm</span></span>
<span data-ttu-id="acd75-136">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="acd75-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="acd75-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="acd75-137">-WhatIf</span></span>
<span data-ttu-id="acd75-138">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="acd75-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="acd75-139">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="acd75-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="acd75-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acd75-140">CommonParameters</span></span>
<span data-ttu-id="acd75-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="acd75-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acd75-142">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="acd75-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acd75-143">입력</span><span class="sxs-lookup"><span data-stu-id="acd75-143">INPUTS</span></span>

### <span data-ttu-id="acd75-144">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="acd75-144">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span></span>

## <span data-ttu-id="acd75-145">출력</span><span class="sxs-lookup"><span data-stu-id="acd75-145">OUTPUTS</span></span>

### <span data-ttu-id="acd75-146">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="acd75-146">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span></span>

## <span data-ttu-id="acd75-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="acd75-147">NOTES</span></span>

<span data-ttu-id="acd75-148">별칭</span><span class="sxs-lookup"><span data-stu-id="acd75-148">ALIASES</span></span>

<span data-ttu-id="acd75-149">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="acd75-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="acd75-150">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="acd75-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="acd75-151">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="acd75-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="acd75-152">INPUTOBJECT: <IAppServicePlan></span><span class="sxs-lookup"><span data-stu-id="acd75-152">INPUTOBJECT <IAppServicePlan>:</span></span> 
  - <span data-ttu-id="acd75-153">`Location <String>`: 리소스 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="acd75-153">`Location <String>`: Resource Location.</span></span>
  - <span data-ttu-id="acd75-154">`[Kind <String>]`: 리소스의 종류입니다.</span><span class="sxs-lookup"><span data-stu-id="acd75-154">`[Kind <String>]`: Kind of resource.</span></span>
  - <span data-ttu-id="acd75-155">`[Tag <IResourceTags>]`: 리소스 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="acd75-155">`[Tag <IResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="acd75-156">`[(Any) <String>]`: 이 개체에 추가할 수 있는 속성을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="acd75-156">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="acd75-157">`[Capacity <Int32?>]`: 리소스에 할당된 현재 인스턴스 수입니다.</span><span class="sxs-lookup"><span data-stu-id="acd75-157">`[Capacity <Int32?>]`: Current number of instances assigned to the resource.</span></span>
  - <span data-ttu-id="acd75-158">`[FreeOfferExpirationTime <DateTime?>]`: 서버 팜 무료 제안이 만료되는 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="acd75-158">`[FreeOfferExpirationTime <DateTime?>]`: The time when the server farm free offer expires.</span></span>
  - <span data-ttu-id="acd75-159">`[HostingEnvironmentProfileId <String>]`: App Service Environment의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="acd75-159">`[HostingEnvironmentProfileId <String>]`: Resource ID of the App Service Environment.</span></span>
  - <span data-ttu-id="acd75-160">`[HyperV <Boolean?>]`: Hyper-V 컨테이너 앱 서비스 계획인 경우 <code>true</code> 그렇지 <code>false</code> 않은 경우.</span><span class="sxs-lookup"><span data-stu-id="acd75-160">`[HyperV <Boolean?>]`: If Hyper-V container app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="acd75-161">`[IsSpot <Boolean?>]`: 이 <code>true</code> App Service 계획은 스폿 인스턴스를 소유합니다.</span><span class="sxs-lookup"><span data-stu-id="acd75-161">`[IsSpot <Boolean?>]`: If <code>true</code>, this App Service Plan owns spot instances.</span></span>
  - <span data-ttu-id="acd75-162">`[IsXenon <Boolean?>]`: 사용되지 않습니다. Hyper-V 컨테이너 앱 서비스 계획인 경우 <code>true</code> 그렇지 <code>false</code> 않은 경우.</span><span class="sxs-lookup"><span data-stu-id="acd75-162">`[IsXenon <Boolean?>]`: Obsolete: If Hyper-V container app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="acd75-163">`[MaximumElasticWorkerCount <Int32?>]`: 이 ElasticScaleEnabled App Service 계획에 허용되는 최대 총 작업자 수</span><span class="sxs-lookup"><span data-stu-id="acd75-163">`[MaximumElasticWorkerCount <Int32?>]`: Maximum number of total workers allowed for this ElasticScaleEnabled App Service Plan</span></span>
  - <span data-ttu-id="acd75-164">`[PerSiteScaling <Boolean?>]`: 이 App Service 계획에 <code>true</code> 할당된 앱은 독립적으로 확장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="acd75-164">`[PerSiteScaling <Boolean?>]`: If <code>true</code>, apps assigned to this App Service plan can be scaled independently.</span></span>         <span data-ttu-id="acd75-165">이 App Service 계획에 할당된 앱은 계획의 모든 <code>false</code> 인스턴스로 확장됩니다.</span><span class="sxs-lookup"><span data-stu-id="acd75-165">If <code>false</code>, apps assigned to this App Service plan will scale to all instances of the plan.</span></span>
  - <span data-ttu-id="acd75-166">`[Reserved <Boolean?>]`: Linux 앱 서비스 계획인 경우 <code>true</code> 그렇지 <code>false</code> 않은 경우.</span><span class="sxs-lookup"><span data-stu-id="acd75-166">`[Reserved <Boolean?>]`: If Linux app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="acd75-167">`[SkuCapability <ICapability[]>]`: SKU의 기능(예: Traffic Manager를 사용하도록 설정되어 있나요?</span><span class="sxs-lookup"><span data-stu-id="acd75-167">`[SkuCapability <ICapability[]>]`: Capabilities of the SKU, e.g., is traffic manager enabled?</span></span>
    - <span data-ttu-id="acd75-168">`[Name <String>]`: SKU 기능의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="acd75-168">`[Name <String>]`: Name of the SKU capability.</span></span>
    - <span data-ttu-id="acd75-169">`[Reason <String>]`: SKU 기능의 이유입니다.</span><span class="sxs-lookup"><span data-stu-id="acd75-169">`[Reason <String>]`: Reason of the SKU capability.</span></span>
    - <span data-ttu-id="acd75-170">`[Value <String>]`: SKU 기능의 값입니다.</span><span class="sxs-lookup"><span data-stu-id="acd75-170">`[Value <String>]`: Value of the SKU capability.</span></span>
  - <span data-ttu-id="acd75-171">`[SkuCapacityDefault <Int32?>]`: 이 App Service 계획 SKU에 대한 기본 작업자 수입니다.</span><span class="sxs-lookup"><span data-stu-id="acd75-171">`[SkuCapacityDefault <Int32?>]`: Default number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="acd75-172">`[SkuCapacityMaximum <Int32?>]`: 이 App Service 계획 SKU에 대한 최대 작업자 수입니다.</span><span class="sxs-lookup"><span data-stu-id="acd75-172">`[SkuCapacityMaximum <Int32?>]`: Maximum number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="acd75-173">`[SkuCapacityMinimum <Int32?>]`: 이 App Service 계획 SKU에 대한 최소 작업자 수입니다.</span><span class="sxs-lookup"><span data-stu-id="acd75-173">`[SkuCapacityMinimum <Int32?>]`: Minimum number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="acd75-174">`[SkuCapacityScaleType <String>]`: App Service 계획에 사용 가능한 크기 조정 구성입니다.</span><span class="sxs-lookup"><span data-stu-id="acd75-174">`[SkuCapacityScaleType <String>]`: Available scale configurations for an App Service plan.</span></span>
  - <span data-ttu-id="acd75-175">`[SkuFamily <String>]`: 리소스 SKU의 패밀리 코드입니다.</span><span class="sxs-lookup"><span data-stu-id="acd75-175">`[SkuFamily <String>]`: Family code of the resource SKU.</span></span>
  - <span data-ttu-id="acd75-176">`[SkuLocation <String[]>]`: SKU의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="acd75-176">`[SkuLocation <String[]>]`: Locations of the SKU.</span></span>
  - <span data-ttu-id="acd75-177">`[SkuName <String>]`: 리소스 SKU의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="acd75-177">`[SkuName <String>]`: Name of the resource SKU.</span></span>
  - <span data-ttu-id="acd75-178">`[SkuSize <String>]`: 리소스 SKU의 크기 지정자입니다.</span><span class="sxs-lookup"><span data-stu-id="acd75-178">`[SkuSize <String>]`: Size specifier of the resource SKU.</span></span>
  - <span data-ttu-id="acd75-179">`[SkuTier <String>]`: 리소스 SKU의 서비스 계층입니다.</span><span class="sxs-lookup"><span data-stu-id="acd75-179">`[SkuTier <String>]`: Service tier of the resource SKU.</span></span>
  - <span data-ttu-id="acd75-180">`[SpotExpirationTime <DateTime?>]`: 서버 팜이 만료되는 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="acd75-180">`[SpotExpirationTime <DateTime?>]`: The time when the server farm expires.</span></span> <span data-ttu-id="acd75-181">스폿 서버 팜인 경우만 유효합니다.</span><span class="sxs-lookup"><span data-stu-id="acd75-181">Valid only if it is a spot server farm.</span></span>
  - <span data-ttu-id="acd75-182">`[TargetWorkerCount <Int32?>]`: 작업자 수를 조정합니다.</span><span class="sxs-lookup"><span data-stu-id="acd75-182">`[TargetWorkerCount <Int32?>]`: Scaling worker count.</span></span>
  - <span data-ttu-id="acd75-183">`[TargetWorkerSizeId <Int32?>]`: 작업자 크기 ID 크기 조정</span><span class="sxs-lookup"><span data-stu-id="acd75-183">`[TargetWorkerSizeId <Int32?>]`: Scaling worker size ID.</span></span>
  - <span data-ttu-id="acd75-184">`[WorkerTierName <String>]`: App Service 계획에 할당된 대상 작업 계층입니다.</span><span class="sxs-lookup"><span data-stu-id="acd75-184">`[WorkerTierName <String>]`: Target worker tier assigned to the App Service plan.</span></span>

## <span data-ttu-id="acd75-185">관련 링크</span><span class="sxs-lookup"><span data-stu-id="acd75-185">RELATED LINKS</span></span>

