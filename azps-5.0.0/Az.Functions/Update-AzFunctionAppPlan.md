---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/update-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionAppPlan.md
ms.openlocfilehash: e0831e95a5601d3558af7089825684cc48e7838c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215404"
---
# <span data-ttu-id="d394b-101">Update-AzFunctionAppPlan</span><span class="sxs-lookup"><span data-stu-id="d394b-101">Update-AzFunctionAppPlan</span></span>

## <span data-ttu-id="d394b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d394b-102">SYNOPSIS</span></span>
<span data-ttu-id="d394b-103">함수 앱 서비스 계획을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="d394b-103">Updates a function app service plan.</span></span>

## <span data-ttu-id="d394b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d394b-104">SYNTAX</span></span>

### <span data-ttu-id="d394b-105">ByName (기본값)</span><span class="sxs-lookup"><span data-stu-id="d394b-105">ByName (Default)</span></span>
```
Update-AzFunctionAppPlan -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-MaximumWorkerCount <Int32>] [-MinimumWorkerCount <Int32>] [-Sku <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d394b-106">ByObjectInput</span><span class="sxs-lookup"><span data-stu-id="d394b-106">ByObjectInput</span></span>
```
Update-AzFunctionAppPlan -InputObject <IAppServicePlan> [-MaximumWorkerCount <Int32>]
 [-MinimumWorkerCount <Int32>] [-Sku <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d394b-107">설명은</span><span class="sxs-lookup"><span data-stu-id="d394b-107">DESCRIPTION</span></span>
<span data-ttu-id="d394b-108">함수 앱 서비스 계획을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="d394b-108">Updates a function app service plan.</span></span>

## <span data-ttu-id="d394b-109">예제의</span><span class="sxs-lookup"><span data-stu-id="d394b-109">EXAMPLES</span></span>

### <span data-ttu-id="d394b-110">예제 1: 앱 서비스 계획을 업데이트 하 여 최대 25 명의 작업자와 sku를 EP2.</span><span class="sxs-lookup"><span data-stu-id="d394b-110">Example 1: Update an app service plan to EP2 sku with twenty maximum workers.</span></span>
```powershell
PS C:\> Update-AzFunctionAppPlan -ResourceGroupName MyResourceGroupName `
                                 -Name MyPremiumPlan `
                                 -MaximumWorkerCount 20 `
                                 -Sku EP2

```

<span data-ttu-id="d394b-111">이 명령은 앱 서비스 계획을 최대 25 개 작업자와 EP2 sku로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="d394b-111">This command updates an app service plan to EP2 sku with twenty maximum workers.</span></span>

## <span data-ttu-id="d394b-112">변수</span><span class="sxs-lookup"><span data-stu-id="d394b-112">PARAMETERS</span></span>

### <span data-ttu-id="d394b-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d394b-113">-AsJob</span></span>
<span data-ttu-id="d394b-114">명령을 작업으로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="d394b-114">Run the command as a job.</span></span>

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

### <span data-ttu-id="d394b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d394b-115">-DefaultProfile</span></span>


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

### <span data-ttu-id="d394b-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d394b-116">-InputObject</span></span>
<span data-ttu-id="d394b-117">생성 하려면 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d394b-117">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d394b-118">-Maximum개 수</span><span class="sxs-lookup"><span data-stu-id="d394b-118">-MaximumWorkerCount</span></span>
<span data-ttu-id="d394b-119">App service 계획의 최대 작업자 수입니다.</span><span class="sxs-lookup"><span data-stu-id="d394b-119">The maximum number of workers for the app service plan.</span></span>

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

### <span data-ttu-id="d394b-120">-가 수</span><span class="sxs-lookup"><span data-stu-id="d394b-120">-MinimumWorkerCount</span></span>
<span data-ttu-id="d394b-121">App service 계획의 최소 작업자 수입니다.</span><span class="sxs-lookup"><span data-stu-id="d394b-121">The minimum number of workers for the app service plan.</span></span>

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

### <span data-ttu-id="d394b-122">-이름</span><span class="sxs-lookup"><span data-stu-id="d394b-122">-Name</span></span>
<span data-ttu-id="d394b-123">App Service 계획의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d394b-123">Name of the App Service plan.</span></span>

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

### <span data-ttu-id="d394b-124">-NoWait</span><span class="sxs-lookup"><span data-stu-id="d394b-124">-NoWait</span></span>
<span data-ttu-id="d394b-125">비동기적으로 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="d394b-125">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="d394b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d394b-126">-ResourceGroupName</span></span>
<span data-ttu-id="d394b-127">자원이 속한 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d394b-127">Name of the resource group to which the resource belongs.</span></span>

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

### <span data-ttu-id="d394b-128">-Sku</span><span class="sxs-lookup"><span data-stu-id="d394b-128">-Sku</span></span>
<span data-ttu-id="d394b-129">계획 sku입니다.</span><span class="sxs-lookup"><span data-stu-id="d394b-129">The plan sku.</span></span>
<span data-ttu-id="d394b-130">유효한 입력: EP1, EP2, EP3</span><span class="sxs-lookup"><span data-stu-id="d394b-130">Valid inputs are: EP1, EP2, EP3</span></span>

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

### <span data-ttu-id="d394b-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d394b-131">-SubscriptionId</span></span>
<span data-ttu-id="d394b-132">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="d394b-132">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="d394b-133">태그</span><span class="sxs-lookup"><span data-stu-id="d394b-133">-Tag</span></span>
<span data-ttu-id="d394b-134">리소스 태그.</span><span class="sxs-lookup"><span data-stu-id="d394b-134">Resource tags.</span></span>

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

### <span data-ttu-id="d394b-135">-확인</span><span class="sxs-lookup"><span data-stu-id="d394b-135">-Confirm</span></span>
<span data-ttu-id="d394b-136">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d394b-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d394b-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d394b-137">-WhatIf</span></span>
<span data-ttu-id="d394b-138">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d394b-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d394b-139">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d394b-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d394b-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d394b-140">CommonParameters</span></span>
<span data-ttu-id="d394b-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d394b-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d394b-142">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d394b-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d394b-143">입력</span><span class="sxs-lookup"><span data-stu-id="d394b-143">INPUTS</span></span>

### <span data-ttu-id="d394b-144">Api20190801. i p. PowerShell. IAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="d394b-144">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span></span>

## <span data-ttu-id="d394b-145">출력</span><span class="sxs-lookup"><span data-stu-id="d394b-145">OUTPUTS</span></span>

### <span data-ttu-id="d394b-146">Api20190801. i p. PowerShell. IAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="d394b-146">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span></span>

## <span data-ttu-id="d394b-147">상속자</span><span class="sxs-lookup"><span data-stu-id="d394b-147">NOTES</span></span>

<span data-ttu-id="d394b-148">별칭과</span><span class="sxs-lookup"><span data-stu-id="d394b-148">ALIASES</span></span>

<span data-ttu-id="d394b-149">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="d394b-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d394b-150">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="d394b-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d394b-151">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="d394b-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d394b-152">INPUTOBJECT <IAppServicePlan> :</span><span class="sxs-lookup"><span data-stu-id="d394b-152">INPUTOBJECT <IAppServicePlan>:</span></span> 
  - <span data-ttu-id="d394b-153">`Location <String>`: 리소스 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="d394b-153">`Location <String>`: Resource Location.</span></span>
  - <span data-ttu-id="d394b-154">`[Kind <String>]`: 리소스 종류입니다.</span><span class="sxs-lookup"><span data-stu-id="d394b-154">`[Kind <String>]`: Kind of resource.</span></span>
  - <span data-ttu-id="d394b-155">`[Tag <IResourceTags>]`: 리소스 태그.</span><span class="sxs-lookup"><span data-stu-id="d394b-155">`[Tag <IResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="d394b-156">`[(Any) <String>]`:이 개체에 모든 속성이 추가 될 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="d394b-156">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="d394b-157">`[Capacity <Int32?>]`: 리소스에 할당 된 현재 인스턴스 수입니다.</span><span class="sxs-lookup"><span data-stu-id="d394b-157">`[Capacity <Int32?>]`: Current number of instances assigned to the resource.</span></span>
  - <span data-ttu-id="d394b-158">`[FreeOfferExpirationTime <DateTime?>]`: 서버 팜 무료 제공이 만료 되는 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="d394b-158">`[FreeOfferExpirationTime <DateTime?>]`: The time when the server farm free offer expires.</span></span>
  - <span data-ttu-id="d394b-159">`[HostingEnvironmentProfileId <String>]`: 앱 서비스 환경의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="d394b-159">`[HostingEnvironmentProfileId <String>]`: Resource ID of the App Service Environment.</span></span>
  - <span data-ttu-id="d394b-160">`[HyperV <Boolean?>]`: Hyper-v 컨테이너 app service 계획 <code>true</code> 인 경우에는 <code>false</code> 그렇지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d394b-160">`[HyperV <Boolean?>]`: If Hyper-V container app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="d394b-161">`[IsSpot <Boolean?>]`: <code>true</code> 이 앱 서비스 계획에서 스폿 인스턴스를 소유 하는 경우</span><span class="sxs-lookup"><span data-stu-id="d394b-161">`[IsSpot <Boolean?>]`: If <code>true</code>, this App Service Plan owns spot instances.</span></span>
  - <span data-ttu-id="d394b-162">`[IsXenon <Boolean?>]`: 사용 하지 않음: Hyper-v 컨테이너 app service 계획 <code>true</code> 인 경우 <code>false</code></span><span class="sxs-lookup"><span data-stu-id="d394b-162">`[IsXenon <Boolean?>]`: Obsolete: If Hyper-V container app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="d394b-163">`[MaximumElasticWorkerCount <Int32?>]`:이 ElasticScaleEnabled App Service 계획에 허용 되는 최대 총 작업자 수</span><span class="sxs-lookup"><span data-stu-id="d394b-163">`[MaximumElasticWorkerCount <Int32?>]`: Maximum number of total workers allowed for this ElasticScaleEnabled App Service Plan</span></span>
  - <span data-ttu-id="d394b-164">`[PerSiteScaling <Boolean?>]`: <code>true</code> 이 앱 서비스 계획에 할당 된 앱을 독립적으로 확장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d394b-164">`[PerSiteScaling <Boolean?>]`: If <code>true</code>, apps assigned to this App Service plan can be scaled independently.</span></span>         <span data-ttu-id="d394b-165"><code>false</code>이 앱 서비스 계획에 할당 된 앱이 계획의 모든 인스턴스에 맞게 조정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d394b-165">If <code>false</code>, apps assigned to this App Service plan will scale to all instances of the plan.</span></span>
  - <span data-ttu-id="d394b-166">`[Reserved <Boolean?>]`: Linux app service 계획 <code>true</code> 인 경우에는 <code>false</code> 그렇지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d394b-166">`[Reserved <Boolean?>]`: If Linux app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="d394b-167">`[SkuCapability <ICapability[]>]`: SKU의 기능 (예:)은 traffic manager를 사용할 수 있나요?</span><span class="sxs-lookup"><span data-stu-id="d394b-167">`[SkuCapability <ICapability[]>]`: Capabilities of the SKU, e.g., is traffic manager enabled?</span></span>
    - <span data-ttu-id="d394b-168">`[Name <String>]`: SKU 기능의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d394b-168">`[Name <String>]`: Name of the SKU capability.</span></span>
    - <span data-ttu-id="d394b-169">`[Reason <String>]`: SKU 기능에 대 한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="d394b-169">`[Reason <String>]`: Reason of the SKU capability.</span></span>
    - <span data-ttu-id="d394b-170">`[Value <String>]`: SKU 기능의 값입니다.</span><span class="sxs-lookup"><span data-stu-id="d394b-170">`[Value <String>]`: Value of the SKU capability.</span></span>
  - <span data-ttu-id="d394b-171">`[SkuCapacityDefault <Int32?>]`:이 App Service 계획 SKU에 대 한 기본 작업자 수입니다.</span><span class="sxs-lookup"><span data-stu-id="d394b-171">`[SkuCapacityDefault <Int32?>]`: Default number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="d394b-172">`[SkuCapacityMaximum <Int32?>]`:이 App Service 계획 SKU에 대 한 최대 작업자 수입니다.</span><span class="sxs-lookup"><span data-stu-id="d394b-172">`[SkuCapacityMaximum <Int32?>]`: Maximum number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="d394b-173">`[SkuCapacityMinimum <Int32?>]`:이 App Service 계획 SKU의 최소 작업자 수입니다.</span><span class="sxs-lookup"><span data-stu-id="d394b-173">`[SkuCapacityMinimum <Int32?>]`: Minimum number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="d394b-174">`[SkuCapacityScaleType <String>]`: 앱 서비스 계획에 사용할 수 있는 배율 구성입니다.</span><span class="sxs-lookup"><span data-stu-id="d394b-174">`[SkuCapacityScaleType <String>]`: Available scale configurations for an App Service plan.</span></span>
  - <span data-ttu-id="d394b-175">`[SkuFamily <String>]`: 리소스 SKU의 패밀리 코드입니다.</span><span class="sxs-lookup"><span data-stu-id="d394b-175">`[SkuFamily <String>]`: Family code of the resource SKU.</span></span>
  - <span data-ttu-id="d394b-176">`[SkuLocation <String[]>]`: SKU의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="d394b-176">`[SkuLocation <String[]>]`: Locations of the SKU.</span></span>
  - <span data-ttu-id="d394b-177">`[SkuName <String>]`: 리소스 SKU의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d394b-177">`[SkuName <String>]`: Name of the resource SKU.</span></span>
  - <span data-ttu-id="d394b-178">`[SkuSize <String>]`: 리소스 SKU의 크기 지정자입니다.</span><span class="sxs-lookup"><span data-stu-id="d394b-178">`[SkuSize <String>]`: Size specifier of the resource SKU.</span></span>
  - <span data-ttu-id="d394b-179">`[SkuTier <String>]`: 리소스 SKU의 서비스 계층입니다.</span><span class="sxs-lookup"><span data-stu-id="d394b-179">`[SkuTier <String>]`: Service tier of the resource SKU.</span></span>
  - <span data-ttu-id="d394b-180">`[SpotExpirationTime <DateTime?>]`: 서버 팜이 만료 되는 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="d394b-180">`[SpotExpirationTime <DateTime?>]`: The time when the server farm expires.</span></span> <span data-ttu-id="d394b-181">스폿 서버 팜과만 유효 합니다.</span><span class="sxs-lookup"><span data-stu-id="d394b-181">Valid only if it is a spot server farm.</span></span>
  - <span data-ttu-id="d394b-182">`[TargetWorkerCount <Int32?>]`: 작업자 수의 크기를 조정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d394b-182">`[TargetWorkerCount <Int32?>]`: Scaling worker count.</span></span>
  - <span data-ttu-id="d394b-183">`[TargetWorkerSizeId <Int32?>]`: 작업자 크기 ID를 조정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d394b-183">`[TargetWorkerSizeId <Int32?>]`: Scaling worker size ID.</span></span>
  - <span data-ttu-id="d394b-184">`[WorkerTierName <String>]`: 앱 서비스 계획에 할당 된 대상 작업자 계층입니다.</span><span class="sxs-lookup"><span data-stu-id="d394b-184">`[WorkerTierName <String>]`: Target worker tier assigned to the App Service plan.</span></span>

## <span data-ttu-id="d394b-185">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d394b-185">RELATED LINKS</span></span>

