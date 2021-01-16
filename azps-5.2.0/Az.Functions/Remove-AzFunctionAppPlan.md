---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/remove-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Remove-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Remove-AzFunctionAppPlan.md
ms.openlocfilehash: 6668952ba07327482da7ed3c274eb003ac61c73c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98326773"
---
# <span data-ttu-id="30423-101">Remove-AzFunctionAppPlan</span><span class="sxs-lookup"><span data-stu-id="30423-101">Remove-AzFunctionAppPlan</span></span>

## <span data-ttu-id="30423-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30423-102">SYNOPSIS</span></span>
<span data-ttu-id="30423-103">함수 앱 계획을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="30423-103">Deletes a function app plan.</span></span>

## <span data-ttu-id="30423-104">구문</span><span class="sxs-lookup"><span data-stu-id="30423-104">SYNTAX</span></span>

### <span data-ttu-id="30423-105">ByName(기본값)</span><span class="sxs-lookup"><span data-stu-id="30423-105">ByName (Default)</span></span>
```
Remove-AzFunctionAppPlan -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Force]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="30423-106">ByObjectInput</span><span class="sxs-lookup"><span data-stu-id="30423-106">ByObjectInput</span></span>
```
Remove-AzFunctionAppPlan -InputObject <IAppServicePlan> [-Force] [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="30423-107">설명</span><span class="sxs-lookup"><span data-stu-id="30423-107">DESCRIPTION</span></span>
<span data-ttu-id="30423-108">함수 앱 계획을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="30423-108">Deletes a function app plan.</span></span>

## <span data-ttu-id="30423-109">예제</span><span class="sxs-lookup"><span data-stu-id="30423-109">EXAMPLES</span></span>

### <span data-ttu-id="30423-110">예제 1: 이름에 따라 함수 앱 계획을 다운로드하고 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="30423-110">Example 1: Get a function app plan by name and delete it.</span></span>
```powershell
PS C:\> Get-AzFunctionAppPlan -Name MyAppName -ResourceGroupName MyResourceGroupName | Remove-AzFunctionAppPlan -Force
```

<span data-ttu-id="30423-111">이 명령은 함수 앱 계획을 이름으로 다운로드하고 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="30423-111">This command gets a function app plan by name and deletes it.</span></span>

### <span data-ttu-id="30423-112">예제 2: 이름으로 함수 앱 계획을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="30423-112">Example 2: Delete a function app plan by name.</span></span>
```powershell
PS C:\> Remove-AzFunctionAppPlan -Name MyAppName -ResourceGroupName MyResourceGroupName -Force
```

<span data-ttu-id="30423-113">이 명령은 함수 앱 계획을 이름으로 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="30423-113">This command deletes a function app plan by name.</span></span>

## <span data-ttu-id="30423-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="30423-114">PARAMETERS</span></span>

### <span data-ttu-id="30423-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30423-115">-DefaultProfile</span></span>
<span data-ttu-id="30423-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="30423-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30423-117">-Force</span><span class="sxs-lookup"><span data-stu-id="30423-117">-Force</span></span>
<span data-ttu-id="30423-118">확인을 요청하지 않고 cmdlet이 함수 앱 계획을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="30423-118">Forces the cmdlet to remove the function app plan without prompting for confirmation.</span></span>

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

### <span data-ttu-id="30423-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="30423-119">-InputObject</span></span>
<span data-ttu-id="30423-120">생성을 위해 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="30423-120">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="30423-121">-Name</span><span class="sxs-lookup"><span data-stu-id="30423-121">-Name</span></span>
<span data-ttu-id="30423-122">함수 앱의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="30423-122">The name of function app.</span></span>

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

### <span data-ttu-id="30423-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="30423-123">-PassThru</span></span>
<span data-ttu-id="30423-124">명령이 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="30423-124">Returns true when the command succeeds.</span></span>

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

### <span data-ttu-id="30423-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30423-125">-ResourceGroupName</span></span>


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

### <span data-ttu-id="30423-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="30423-126">-SubscriptionId</span></span>
<span data-ttu-id="30423-127">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="30423-127">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="30423-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="30423-128">-Confirm</span></span>
<span data-ttu-id="30423-129">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="30423-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30423-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30423-130">-WhatIf</span></span>
<span data-ttu-id="30423-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="30423-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30423-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="30423-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30423-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30423-133">CommonParameters</span></span>
<span data-ttu-id="30423-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="30423-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30423-135">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="30423-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30423-136">입력</span><span class="sxs-lookup"><span data-stu-id="30423-136">INPUTS</span></span>

### <span data-ttu-id="30423-137">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="30423-137">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span></span>

## <span data-ttu-id="30423-138">출력</span><span class="sxs-lookup"><span data-stu-id="30423-138">OUTPUTS</span></span>

### <span data-ttu-id="30423-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="30423-139">System.Boolean</span></span>

## <span data-ttu-id="30423-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="30423-140">NOTES</span></span>

<span data-ttu-id="30423-141">별칭</span><span class="sxs-lookup"><span data-stu-id="30423-141">ALIASES</span></span>

<span data-ttu-id="30423-142">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="30423-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="30423-143">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="30423-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="30423-144">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="30423-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="30423-145">INPUTOBJECT: <IAppServicePlan></span><span class="sxs-lookup"><span data-stu-id="30423-145">INPUTOBJECT <IAppServicePlan>:</span></span> 
  - <span data-ttu-id="30423-146">`Location <String>`: 리소스 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="30423-146">`Location <String>`: Resource Location.</span></span>
  - <span data-ttu-id="30423-147">`[Kind <String>]`: 리소스의 종류입니다.</span><span class="sxs-lookup"><span data-stu-id="30423-147">`[Kind <String>]`: Kind of resource.</span></span>
  - <span data-ttu-id="30423-148">`[Tag <IResourceTags>]`: 리소스 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="30423-148">`[Tag <IResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="30423-149">`[(Any) <String>]`: 이 개체에 추가할 수 있는 속성을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="30423-149">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="30423-150">`[Capacity <Int32?>]`: 리소스에 할당된 현재 인스턴스 수입니다.</span><span class="sxs-lookup"><span data-stu-id="30423-150">`[Capacity <Int32?>]`: Current number of instances assigned to the resource.</span></span>
  - <span data-ttu-id="30423-151">`[FreeOfferExpirationTime <DateTime?>]`: 서버 팜 무료 제안이 만료되는 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="30423-151">`[FreeOfferExpirationTime <DateTime?>]`: The time when the server farm free offer expires.</span></span>
  - <span data-ttu-id="30423-152">`[HostingEnvironmentProfileId <String>]`: App Service Environment의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="30423-152">`[HostingEnvironmentProfileId <String>]`: Resource ID of the App Service Environment.</span></span>
  - <span data-ttu-id="30423-153">`[HyperV <Boolean?>]`: Hyper-V 컨테이너 앱 서비스 계획인 경우 <code>true</code> 그렇지 <code>false</code> 않은 경우.</span><span class="sxs-lookup"><span data-stu-id="30423-153">`[HyperV <Boolean?>]`: If Hyper-V container app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="30423-154">`[IsSpot <Boolean?>]`: 이 <code>true</code> App Service 계획은 스폿 인스턴스를 소유합니다.</span><span class="sxs-lookup"><span data-stu-id="30423-154">`[IsSpot <Boolean?>]`: If <code>true</code>, this App Service Plan owns spot instances.</span></span>
  - <span data-ttu-id="30423-155">`[IsXenon <Boolean?>]`: 사용되지 않습니다. Hyper-V 컨테이너 앱 서비스 계획인 경우 <code>true</code> 그렇지 <code>false</code> 않은 경우.</span><span class="sxs-lookup"><span data-stu-id="30423-155">`[IsXenon <Boolean?>]`: Obsolete: If Hyper-V container app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="30423-156">`[MaximumElasticWorkerCount <Int32?>]`: 이 ElasticScaleEnabled App Service 계획에 허용되는 최대 총 작업자 수</span><span class="sxs-lookup"><span data-stu-id="30423-156">`[MaximumElasticWorkerCount <Int32?>]`: Maximum number of total workers allowed for this ElasticScaleEnabled App Service Plan</span></span>
  - <span data-ttu-id="30423-157">`[PerSiteScaling <Boolean?>]`: 이 App Service 계획에 <code>true</code> 할당된 앱은 독립적으로 확장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="30423-157">`[PerSiteScaling <Boolean?>]`: If <code>true</code>, apps assigned to this App Service plan can be scaled independently.</span></span>         <span data-ttu-id="30423-158">이 App Service 계획에 할당된 앱은 계획의 모든 <code>false</code> 인스턴스로 확장됩니다.</span><span class="sxs-lookup"><span data-stu-id="30423-158">If <code>false</code>, apps assigned to this App Service plan will scale to all instances of the plan.</span></span>
  - <span data-ttu-id="30423-159">`[Reserved <Boolean?>]`: Linux 앱 서비스 계획인 경우 <code>true</code> 그렇지 <code>false</code> 않은 경우.</span><span class="sxs-lookup"><span data-stu-id="30423-159">`[Reserved <Boolean?>]`: If Linux app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="30423-160">`[SkuCapability <ICapability[]>]`: SKU의 기능(예: Traffic Manager를 사용하도록 설정되어 있나요?</span><span class="sxs-lookup"><span data-stu-id="30423-160">`[SkuCapability <ICapability[]>]`: Capabilities of the SKU, e.g., is traffic manager enabled?</span></span>
    - <span data-ttu-id="30423-161">`[Name <String>]`: SKU 기능의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="30423-161">`[Name <String>]`: Name of the SKU capability.</span></span>
    - <span data-ttu-id="30423-162">`[Reason <String>]`: SKU 기능의 이유입니다.</span><span class="sxs-lookup"><span data-stu-id="30423-162">`[Reason <String>]`: Reason of the SKU capability.</span></span>
    - <span data-ttu-id="30423-163">`[Value <String>]`: SKU 기능의 값입니다.</span><span class="sxs-lookup"><span data-stu-id="30423-163">`[Value <String>]`: Value of the SKU capability.</span></span>
  - <span data-ttu-id="30423-164">`[SkuCapacityDefault <Int32?>]`: 이 App Service 계획 SKU에 대한 기본 작업자 수입니다.</span><span class="sxs-lookup"><span data-stu-id="30423-164">`[SkuCapacityDefault <Int32?>]`: Default number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="30423-165">`[SkuCapacityMaximum <Int32?>]`: 이 App Service 계획 SKU에 대한 최대 작업자 수입니다.</span><span class="sxs-lookup"><span data-stu-id="30423-165">`[SkuCapacityMaximum <Int32?>]`: Maximum number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="30423-166">`[SkuCapacityMinimum <Int32?>]`: 이 App Service 계획 SKU에 대한 최소 작업자 수입니다.</span><span class="sxs-lookup"><span data-stu-id="30423-166">`[SkuCapacityMinimum <Int32?>]`: Minimum number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="30423-167">`[SkuCapacityScaleType <String>]`: App Service 계획에 사용 가능한 크기 조정 구성입니다.</span><span class="sxs-lookup"><span data-stu-id="30423-167">`[SkuCapacityScaleType <String>]`: Available scale configurations for an App Service plan.</span></span>
  - <span data-ttu-id="30423-168">`[SkuFamily <String>]`: 리소스 SKU의 패밀리 코드입니다.</span><span class="sxs-lookup"><span data-stu-id="30423-168">`[SkuFamily <String>]`: Family code of the resource SKU.</span></span>
  - <span data-ttu-id="30423-169">`[SkuLocation <String[]>]`: SKU의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="30423-169">`[SkuLocation <String[]>]`: Locations of the SKU.</span></span>
  - <span data-ttu-id="30423-170">`[SkuName <String>]`: 리소스 SKU의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="30423-170">`[SkuName <String>]`: Name of the resource SKU.</span></span>
  - <span data-ttu-id="30423-171">`[SkuSize <String>]`: 리소스 SKU의 크기 지정자입니다.</span><span class="sxs-lookup"><span data-stu-id="30423-171">`[SkuSize <String>]`: Size specifier of the resource SKU.</span></span>
  - <span data-ttu-id="30423-172">`[SkuTier <String>]`: 리소스 SKU의 서비스 계층입니다.</span><span class="sxs-lookup"><span data-stu-id="30423-172">`[SkuTier <String>]`: Service tier of the resource SKU.</span></span>
  - <span data-ttu-id="30423-173">`[SpotExpirationTime <DateTime?>]`: 서버 팜이 만료되는 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="30423-173">`[SpotExpirationTime <DateTime?>]`: The time when the server farm expires.</span></span> <span data-ttu-id="30423-174">스폿 서버 팜인 경우만 유효합니다.</span><span class="sxs-lookup"><span data-stu-id="30423-174">Valid only if it is a spot server farm.</span></span>
  - <span data-ttu-id="30423-175">`[TargetWorkerCount <Int32?>]`: 작업자 수를 조정합니다.</span><span class="sxs-lookup"><span data-stu-id="30423-175">`[TargetWorkerCount <Int32?>]`: Scaling worker count.</span></span>
  - <span data-ttu-id="30423-176">`[TargetWorkerSizeId <Int32?>]`: 작업자 크기 ID 크기 조정</span><span class="sxs-lookup"><span data-stu-id="30423-176">`[TargetWorkerSizeId <Int32?>]`: Scaling worker size ID.</span></span>
  - <span data-ttu-id="30423-177">`[WorkerTierName <String>]`: App Service 계획에 할당된 대상 작업 계층입니다.</span><span class="sxs-lookup"><span data-stu-id="30423-177">`[WorkerTierName <String>]`: Target worker tier assigned to the App Service plan.</span></span>

## <span data-ttu-id="30423-178">관련 링크</span><span class="sxs-lookup"><span data-stu-id="30423-178">RELATED LINKS</span></span>

