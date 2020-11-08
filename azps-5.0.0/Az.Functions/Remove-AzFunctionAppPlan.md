---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/remove-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Remove-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Remove-AzFunctionAppPlan.md
ms.openlocfilehash: 6668952ba07327482da7ed3c274eb003ac61c73c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215417"
---
# <span data-ttu-id="35d97-101">Remove-AzFunctionAppPlan</span><span class="sxs-lookup"><span data-stu-id="35d97-101">Remove-AzFunctionAppPlan</span></span>

## <span data-ttu-id="35d97-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35d97-102">SYNOPSIS</span></span>
<span data-ttu-id="35d97-103">함수 앱 계획을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="35d97-103">Deletes a function app plan.</span></span>

## <span data-ttu-id="35d97-104">구문과</span><span class="sxs-lookup"><span data-stu-id="35d97-104">SYNTAX</span></span>

### <span data-ttu-id="35d97-105">ByName (기본값)</span><span class="sxs-lookup"><span data-stu-id="35d97-105">ByName (Default)</span></span>
```
Remove-AzFunctionAppPlan -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Force]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="35d97-106">ByObjectInput</span><span class="sxs-lookup"><span data-stu-id="35d97-106">ByObjectInput</span></span>
```
Remove-AzFunctionAppPlan -InputObject <IAppServicePlan> [-Force] [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="35d97-107">설명은</span><span class="sxs-lookup"><span data-stu-id="35d97-107">DESCRIPTION</span></span>
<span data-ttu-id="35d97-108">함수 앱 계획을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="35d97-108">Deletes a function app plan.</span></span>

## <span data-ttu-id="35d97-109">예제의</span><span class="sxs-lookup"><span data-stu-id="35d97-109">EXAMPLES</span></span>

### <span data-ttu-id="35d97-110">예제 1: 이름으로 함수 앱 계획을 가져와 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="35d97-110">Example 1: Get a function app plan by name and delete it.</span></span>
```powershell
PS C:\> Get-AzFunctionAppPlan -Name MyAppName -ResourceGroupName MyResourceGroupName | Remove-AzFunctionAppPlan -Force
```

<span data-ttu-id="35d97-111">이 명령은 함수 앱 계획을 이름별로 가져와 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="35d97-111">This command gets a function app plan by name and deletes it.</span></span>

### <span data-ttu-id="35d97-112">예제 2: 이름을 기준으로 함수 앱 계획을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="35d97-112">Example 2: Delete a function app plan by name.</span></span>
```powershell
PS C:\> Remove-AzFunctionAppPlan -Name MyAppName -ResourceGroupName MyResourceGroupName -Force
```

<span data-ttu-id="35d97-113">이 명령은 함수 앱 계획을 이름으로 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="35d97-113">This command deletes a function app plan by name.</span></span>

## <span data-ttu-id="35d97-114">변수</span><span class="sxs-lookup"><span data-stu-id="35d97-114">PARAMETERS</span></span>

### <span data-ttu-id="35d97-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35d97-115">-DefaultProfile</span></span>
<span data-ttu-id="35d97-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="35d97-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35d97-117">-Force</span><span class="sxs-lookup"><span data-stu-id="35d97-117">-Force</span></span>
<span data-ttu-id="35d97-118">확인 메시지 없이 cmdlet에서 함수 앱 계획을 제거 하도록 강제 합니다.</span><span class="sxs-lookup"><span data-stu-id="35d97-118">Forces the cmdlet to remove the function app plan without prompting for confirmation.</span></span>

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

### <span data-ttu-id="35d97-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="35d97-119">-InputObject</span></span>
<span data-ttu-id="35d97-120">생성 하려면 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="35d97-120">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="35d97-121">-이름</span><span class="sxs-lookup"><span data-stu-id="35d97-121">-Name</span></span>
<span data-ttu-id="35d97-122">함수 앱의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="35d97-122">The name of function app.</span></span>

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

### <span data-ttu-id="35d97-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="35d97-123">-PassThru</span></span>
<span data-ttu-id="35d97-124">명령이 성공 하면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="35d97-124">Returns true when the command succeeds.</span></span>

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

### <span data-ttu-id="35d97-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35d97-125">-ResourceGroupName</span></span>


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

### <span data-ttu-id="35d97-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="35d97-126">-SubscriptionId</span></span>
<span data-ttu-id="35d97-127">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="35d97-127">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="35d97-128">-확인</span><span class="sxs-lookup"><span data-stu-id="35d97-128">-Confirm</span></span>
<span data-ttu-id="35d97-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="35d97-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35d97-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35d97-130">-WhatIf</span></span>
<span data-ttu-id="35d97-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="35d97-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35d97-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="35d97-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35d97-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35d97-133">CommonParameters</span></span>
<span data-ttu-id="35d97-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="35d97-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35d97-135">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="35d97-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35d97-136">입력</span><span class="sxs-lookup"><span data-stu-id="35d97-136">INPUTS</span></span>

### <span data-ttu-id="35d97-137">Api20190801. i p. PowerShell. IAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="35d97-137">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span></span>

## <span data-ttu-id="35d97-138">출력</span><span class="sxs-lookup"><span data-stu-id="35d97-138">OUTPUTS</span></span>

### <span data-ttu-id="35d97-139">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="35d97-139">System.Boolean</span></span>

## <span data-ttu-id="35d97-140">상속자</span><span class="sxs-lookup"><span data-stu-id="35d97-140">NOTES</span></span>

<span data-ttu-id="35d97-141">별칭과</span><span class="sxs-lookup"><span data-stu-id="35d97-141">ALIASES</span></span>

<span data-ttu-id="35d97-142">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="35d97-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="35d97-143">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="35d97-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="35d97-144">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="35d97-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="35d97-145">INPUTOBJECT <IAppServicePlan> :</span><span class="sxs-lookup"><span data-stu-id="35d97-145">INPUTOBJECT <IAppServicePlan>:</span></span> 
  - <span data-ttu-id="35d97-146">`Location <String>`: 리소스 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="35d97-146">`Location <String>`: Resource Location.</span></span>
  - <span data-ttu-id="35d97-147">`[Kind <String>]`: 리소스 종류입니다.</span><span class="sxs-lookup"><span data-stu-id="35d97-147">`[Kind <String>]`: Kind of resource.</span></span>
  - <span data-ttu-id="35d97-148">`[Tag <IResourceTags>]`: 리소스 태그.</span><span class="sxs-lookup"><span data-stu-id="35d97-148">`[Tag <IResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="35d97-149">`[(Any) <String>]`:이 개체에 모든 속성이 추가 될 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="35d97-149">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="35d97-150">`[Capacity <Int32?>]`: 리소스에 할당 된 현재 인스턴스 수입니다.</span><span class="sxs-lookup"><span data-stu-id="35d97-150">`[Capacity <Int32?>]`: Current number of instances assigned to the resource.</span></span>
  - <span data-ttu-id="35d97-151">`[FreeOfferExpirationTime <DateTime?>]`: 서버 팜 무료 제공이 만료 되는 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="35d97-151">`[FreeOfferExpirationTime <DateTime?>]`: The time when the server farm free offer expires.</span></span>
  - <span data-ttu-id="35d97-152">`[HostingEnvironmentProfileId <String>]`: 앱 서비스 환경의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="35d97-152">`[HostingEnvironmentProfileId <String>]`: Resource ID of the App Service Environment.</span></span>
  - <span data-ttu-id="35d97-153">`[HyperV <Boolean?>]`: Hyper-v 컨테이너 app service 계획 <code>true</code> 인 경우에는 <code>false</code> 그렇지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="35d97-153">`[HyperV <Boolean?>]`: If Hyper-V container app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="35d97-154">`[IsSpot <Boolean?>]`: <code>true</code> 이 앱 서비스 계획에서 스폿 인스턴스를 소유 하는 경우</span><span class="sxs-lookup"><span data-stu-id="35d97-154">`[IsSpot <Boolean?>]`: If <code>true</code>, this App Service Plan owns spot instances.</span></span>
  - <span data-ttu-id="35d97-155">`[IsXenon <Boolean?>]`: 사용 하지 않음: Hyper-v 컨테이너 app service 계획 <code>true</code> 인 경우 <code>false</code></span><span class="sxs-lookup"><span data-stu-id="35d97-155">`[IsXenon <Boolean?>]`: Obsolete: If Hyper-V container app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="35d97-156">`[MaximumElasticWorkerCount <Int32?>]`:이 ElasticScaleEnabled App Service 계획에 허용 되는 최대 총 작업자 수</span><span class="sxs-lookup"><span data-stu-id="35d97-156">`[MaximumElasticWorkerCount <Int32?>]`: Maximum number of total workers allowed for this ElasticScaleEnabled App Service Plan</span></span>
  - <span data-ttu-id="35d97-157">`[PerSiteScaling <Boolean?>]`: <code>true</code> 이 앱 서비스 계획에 할당 된 앱을 독립적으로 확장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="35d97-157">`[PerSiteScaling <Boolean?>]`: If <code>true</code>, apps assigned to this App Service plan can be scaled independently.</span></span>         <span data-ttu-id="35d97-158"><code>false</code>이 앱 서비스 계획에 할당 된 앱이 계획의 모든 인스턴스에 맞게 조정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="35d97-158">If <code>false</code>, apps assigned to this App Service plan will scale to all instances of the plan.</span></span>
  - <span data-ttu-id="35d97-159">`[Reserved <Boolean?>]`: Linux app service 계획 <code>true</code> 인 경우에는 <code>false</code> 그렇지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="35d97-159">`[Reserved <Boolean?>]`: If Linux app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="35d97-160">`[SkuCapability <ICapability[]>]`: SKU의 기능 (예:)은 traffic manager를 사용할 수 있나요?</span><span class="sxs-lookup"><span data-stu-id="35d97-160">`[SkuCapability <ICapability[]>]`: Capabilities of the SKU, e.g., is traffic manager enabled?</span></span>
    - <span data-ttu-id="35d97-161">`[Name <String>]`: SKU 기능의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="35d97-161">`[Name <String>]`: Name of the SKU capability.</span></span>
    - <span data-ttu-id="35d97-162">`[Reason <String>]`: SKU 기능에 대 한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="35d97-162">`[Reason <String>]`: Reason of the SKU capability.</span></span>
    - <span data-ttu-id="35d97-163">`[Value <String>]`: SKU 기능의 값입니다.</span><span class="sxs-lookup"><span data-stu-id="35d97-163">`[Value <String>]`: Value of the SKU capability.</span></span>
  - <span data-ttu-id="35d97-164">`[SkuCapacityDefault <Int32?>]`:이 App Service 계획 SKU에 대 한 기본 작업자 수입니다.</span><span class="sxs-lookup"><span data-stu-id="35d97-164">`[SkuCapacityDefault <Int32?>]`: Default number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="35d97-165">`[SkuCapacityMaximum <Int32?>]`:이 App Service 계획 SKU에 대 한 최대 작업자 수입니다.</span><span class="sxs-lookup"><span data-stu-id="35d97-165">`[SkuCapacityMaximum <Int32?>]`: Maximum number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="35d97-166">`[SkuCapacityMinimum <Int32?>]`:이 App Service 계획 SKU의 최소 작업자 수입니다.</span><span class="sxs-lookup"><span data-stu-id="35d97-166">`[SkuCapacityMinimum <Int32?>]`: Minimum number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="35d97-167">`[SkuCapacityScaleType <String>]`: 앱 서비스 계획에 사용할 수 있는 배율 구성입니다.</span><span class="sxs-lookup"><span data-stu-id="35d97-167">`[SkuCapacityScaleType <String>]`: Available scale configurations for an App Service plan.</span></span>
  - <span data-ttu-id="35d97-168">`[SkuFamily <String>]`: 리소스 SKU의 패밀리 코드입니다.</span><span class="sxs-lookup"><span data-stu-id="35d97-168">`[SkuFamily <String>]`: Family code of the resource SKU.</span></span>
  - <span data-ttu-id="35d97-169">`[SkuLocation <String[]>]`: SKU의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="35d97-169">`[SkuLocation <String[]>]`: Locations of the SKU.</span></span>
  - <span data-ttu-id="35d97-170">`[SkuName <String>]`: 리소스 SKU의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="35d97-170">`[SkuName <String>]`: Name of the resource SKU.</span></span>
  - <span data-ttu-id="35d97-171">`[SkuSize <String>]`: 리소스 SKU의 크기 지정자입니다.</span><span class="sxs-lookup"><span data-stu-id="35d97-171">`[SkuSize <String>]`: Size specifier of the resource SKU.</span></span>
  - <span data-ttu-id="35d97-172">`[SkuTier <String>]`: 리소스 SKU의 서비스 계층입니다.</span><span class="sxs-lookup"><span data-stu-id="35d97-172">`[SkuTier <String>]`: Service tier of the resource SKU.</span></span>
  - <span data-ttu-id="35d97-173">`[SpotExpirationTime <DateTime?>]`: 서버 팜이 만료 되는 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="35d97-173">`[SpotExpirationTime <DateTime?>]`: The time when the server farm expires.</span></span> <span data-ttu-id="35d97-174">스폿 서버 팜과만 유효 합니다.</span><span class="sxs-lookup"><span data-stu-id="35d97-174">Valid only if it is a spot server farm.</span></span>
  - <span data-ttu-id="35d97-175">`[TargetWorkerCount <Int32?>]`: 작업자 수의 크기를 조정 합니다.</span><span class="sxs-lookup"><span data-stu-id="35d97-175">`[TargetWorkerCount <Int32?>]`: Scaling worker count.</span></span>
  - <span data-ttu-id="35d97-176">`[TargetWorkerSizeId <Int32?>]`: 작업자 크기 ID를 조정 합니다.</span><span class="sxs-lookup"><span data-stu-id="35d97-176">`[TargetWorkerSizeId <Int32?>]`: Scaling worker size ID.</span></span>
  - <span data-ttu-id="35d97-177">`[WorkerTierName <String>]`: 앱 서비스 계획에 할당 된 대상 작업자 계층입니다.</span><span class="sxs-lookup"><span data-stu-id="35d97-177">`[WorkerTierName <String>]`: Target worker tier assigned to the App Service plan.</span></span>

## <span data-ttu-id="35d97-178">관련 링크</span><span class="sxs-lookup"><span data-stu-id="35d97-178">RELATED LINKS</span></span>

