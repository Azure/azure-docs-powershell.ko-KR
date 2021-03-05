---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/powershell/module/az.timeseriesinsights/remove-aztimeseriesinsightsenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsEnvironment.md
ms.openlocfilehash: 89fa39a5e6e1bb2ded61c41dd553b6d7d0473d4f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963376"
---
# <span data-ttu-id="4b32d-101">Remove-AzTimeSeriesInsightsEnvironment</span><span class="sxs-lookup"><span data-stu-id="4b32d-101">Remove-AzTimeSeriesInsightsEnvironment</span></span>

## <span data-ttu-id="4b32d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b32d-102">SYNOPSIS</span></span>
<span data-ttu-id="4b32d-103">지정된 구독 및 리소스 그룹에 지정된 이름으로 환경을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="4b32d-103">Deletes the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="4b32d-104">구문</span><span class="sxs-lookup"><span data-stu-id="4b32d-104">SYNTAX</span></span>

### <span data-ttu-id="4b32d-105">삭제(기본값)</span><span class="sxs-lookup"><span data-stu-id="4b32d-105">Delete (Default)</span></span>
```
Remove-AzTimeSeriesInsightsEnvironment -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4b32d-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="4b32d-106">DeleteViaIdentity</span></span>
```
Remove-AzTimeSeriesInsightsEnvironment -InputObject <ITimeSeriesInsightsIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4b32d-107">설명</span><span class="sxs-lookup"><span data-stu-id="4b32d-107">DESCRIPTION</span></span>
<span data-ttu-id="4b32d-108">지정된 구독 및 리소스 그룹에 지정된 이름으로 환경을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="4b32d-108">Deletes the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="4b32d-109">예제</span><span class="sxs-lookup"><span data-stu-id="4b32d-109">EXAMPLES</span></span>

### <span data-ttu-id="4b32d-110">예제 1: 이름에 따라 타임 시리즈 인사이트 환경 제거</span><span class="sxs-lookup"><span data-stu-id="4b32d-110">Example 1: Remove a time series insights environment by name</span></span>
```powershell
PS C:\> Remove-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsill

```

<span data-ttu-id="4b32d-111">이 명령은 타임 시리즈 인사이트 환경을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="4b32d-111">This command removes a time series insights environment.</span></span>

### <span data-ttu-id="4b32d-112">예제 2: 개체에 따라 타임 시리즈 인사이트 환경 제거</span><span class="sxs-lookup"><span data-stu-id="4b32d-112">Example 2: Remove a time series insights environment by object</span></span>
```powershell
PS C:\> $env = Get-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsill
PS C:\> Remove-AzTimeSeriesInsightsEnvironment -InputObject $env

```

<span data-ttu-id="4b32d-113">이 명령은 타임 시리즈 인사이트 환경을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="4b32d-113">This command removes a time series insights environment.</span></span>

## <span data-ttu-id="4b32d-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="4b32d-114">PARAMETERS</span></span>

### <span data-ttu-id="4b32d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b32d-115">-DefaultProfile</span></span>
<span data-ttu-id="4b32d-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4b32d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b32d-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4b32d-117">-InputObject</span></span>
<span data-ttu-id="4b32d-118">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="4b32d-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4b32d-119">-Name</span><span class="sxs-lookup"><span data-stu-id="4b32d-119">-Name</span></span>
<span data-ttu-id="4b32d-120">지정된 리소스 그룹과 연결된 Time Series Insights 환경의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4b32d-120">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b32d-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4b32d-121">-PassThru</span></span>
<span data-ttu-id="4b32d-122">명령이 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="4b32d-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="4b32d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b32d-123">-ResourceGroupName</span></span>
<span data-ttu-id="4b32d-124">Azure 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4b32d-124">Name of an Azure Resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b32d-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4b32d-125">-SubscriptionId</span></span>
<span data-ttu-id="4b32d-126">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="4b32d-126">Azure Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b32d-127">-확인</span><span class="sxs-lookup"><span data-stu-id="4b32d-127">-Confirm</span></span>
<span data-ttu-id="4b32d-128">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4b32d-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b32d-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b32d-129">-WhatIf</span></span>
<span data-ttu-id="4b32d-130">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="4b32d-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b32d-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4b32d-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b32d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b32d-132">CommonParameters</span></span>
<span data-ttu-id="4b32d-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4b32d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b32d-134">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4b32d-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b32d-135">입력</span><span class="sxs-lookup"><span data-stu-id="4b32d-135">INPUTS</span></span>

### <span data-ttu-id="4b32d-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="4b32d-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="4b32d-137">출력</span><span class="sxs-lookup"><span data-stu-id="4b32d-137">OUTPUTS</span></span>

### <span data-ttu-id="4b32d-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4b32d-138">System.Boolean</span></span>

## <span data-ttu-id="4b32d-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4b32d-139">NOTES</span></span>

<span data-ttu-id="4b32d-140">별칭</span><span class="sxs-lookup"><span data-stu-id="4b32d-140">ALIASES</span></span>

<span data-ttu-id="4b32d-141">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="4b32d-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4b32d-142">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="4b32d-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4b32d-143">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4b32d-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4b32d-144">INPUTOBJECT <ITimeSeriesInsightsIdentity> : ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="4b32d-144">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4b32d-145">`[AccessPolicyName <String>]`: 액세스 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4b32d-145">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="4b32d-146">`[EnvironmentName <String>]`: 환경 이름</span><span class="sxs-lookup"><span data-stu-id="4b32d-146">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="4b32d-147">`[EventSourceName <String>]`: 지정된 환경과 연결된 Time Series Insights 이벤트 원본의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4b32d-147">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="4b32d-148">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="4b32d-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4b32d-149">`[ReferenceDataSetName <String>]`: 참조 데이터 집합의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4b32d-149">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="4b32d-150">`[ResourceGroupName <String>]`: Azure 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4b32d-150">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="4b32d-151">`[SubscriptionId <String>]`: Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="4b32d-151">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="4b32d-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4b32d-152">RELATED LINKS</span></span>

