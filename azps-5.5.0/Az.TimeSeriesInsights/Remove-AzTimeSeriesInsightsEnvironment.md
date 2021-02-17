---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/remove-aztimeseriesinsightsenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsEnvironment.md
ms.openlocfilehash: 8b56475d2510099b7873fa444a0dc78497aeb729
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190537"
---
# <span data-ttu-id="ff9cc-101">Remove-AzTimeSeriesInsightsEnvironment</span><span class="sxs-lookup"><span data-stu-id="ff9cc-101">Remove-AzTimeSeriesInsightsEnvironment</span></span>

## <span data-ttu-id="ff9cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff9cc-102">SYNOPSIS</span></span>
<span data-ttu-id="ff9cc-103">지정된 구독 및 리소스 그룹에 지정된 이름의 환경을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="ff9cc-103">Deletes the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="ff9cc-104">구문</span><span class="sxs-lookup"><span data-stu-id="ff9cc-104">SYNTAX</span></span>

### <span data-ttu-id="ff9cc-105">삭제(기본값)</span><span class="sxs-lookup"><span data-stu-id="ff9cc-105">Delete (Default)</span></span>
```
Remove-AzTimeSeriesInsightsEnvironment -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ff9cc-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ff9cc-106">DeleteViaIdentity</span></span>
```
Remove-AzTimeSeriesInsightsEnvironment -InputObject <ITimeSeriesInsightsIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ff9cc-107">설명</span><span class="sxs-lookup"><span data-stu-id="ff9cc-107">DESCRIPTION</span></span>
<span data-ttu-id="ff9cc-108">지정된 구독 및 리소스 그룹에 지정된 이름의 환경을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="ff9cc-108">Deletes the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="ff9cc-109">예제</span><span class="sxs-lookup"><span data-stu-id="ff9cc-109">EXAMPLES</span></span>

### <span data-ttu-id="ff9cc-110">예제 1: 이름에 따라 Time Series Insights 환경 제거</span><span class="sxs-lookup"><span data-stu-id="ff9cc-110">Example 1: Remove a time series insights environment by name</span></span>
```powershell
PS C:\> Remove-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsill

```

<span data-ttu-id="ff9cc-111">이 명령은 Time Series Insights 환경을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="ff9cc-111">This command removes a time series insights environment.</span></span>

### <span data-ttu-id="ff9cc-112">예제 2: 개체에 따라 Time Series Insights 환경 제거</span><span class="sxs-lookup"><span data-stu-id="ff9cc-112">Example 2: Remove a time series insights environment by object</span></span>
```powershell
PS C:\> $env = Get-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsill
PS C:\> Remove-AzTimeSeriesInsightsEnvironment -InputObject $env

```

<span data-ttu-id="ff9cc-113">이 명령은 Time Series Insights 환경을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="ff9cc-113">This command removes a time series insights environment.</span></span>

## <span data-ttu-id="ff9cc-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ff9cc-114">PARAMETERS</span></span>

### <span data-ttu-id="ff9cc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff9cc-115">-DefaultProfile</span></span>
<span data-ttu-id="ff9cc-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ff9cc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff9cc-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ff9cc-117">-InputObject</span></span>
<span data-ttu-id="ff9cc-118">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="ff9cc-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ff9cc-119">-Name</span><span class="sxs-lookup"><span data-stu-id="ff9cc-119">-Name</span></span>
<span data-ttu-id="ff9cc-120">지정된 리소스 그룹과 연결된 Time Series Insights 환경의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ff9cc-120">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="ff9cc-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ff9cc-121">-PassThru</span></span>
<span data-ttu-id="ff9cc-122">명령이 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="ff9cc-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="ff9cc-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff9cc-123">-ResourceGroupName</span></span>
<span data-ttu-id="ff9cc-124">Azure 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ff9cc-124">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="ff9cc-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ff9cc-125">-SubscriptionId</span></span>
<span data-ttu-id="ff9cc-126">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="ff9cc-126">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="ff9cc-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ff9cc-127">-Confirm</span></span>
<span data-ttu-id="ff9cc-128">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ff9cc-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff9cc-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff9cc-129">-WhatIf</span></span>
<span data-ttu-id="ff9cc-130">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="ff9cc-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff9cc-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ff9cc-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff9cc-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff9cc-132">CommonParameters</span></span>
<span data-ttu-id="ff9cc-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ff9cc-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff9cc-134">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ff9cc-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff9cc-135">입력</span><span class="sxs-lookup"><span data-stu-id="ff9cc-135">INPUTS</span></span>

### <span data-ttu-id="ff9cc-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="ff9cc-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="ff9cc-137">출력</span><span class="sxs-lookup"><span data-stu-id="ff9cc-137">OUTPUTS</span></span>

### <span data-ttu-id="ff9cc-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ff9cc-138">System.Boolean</span></span>

## <span data-ttu-id="ff9cc-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ff9cc-139">NOTES</span></span>

<span data-ttu-id="ff9cc-140">별칭</span><span class="sxs-lookup"><span data-stu-id="ff9cc-140">ALIASES</span></span>

<span data-ttu-id="ff9cc-141">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="ff9cc-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ff9cc-142">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="ff9cc-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ff9cc-143">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ff9cc-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ff9cc-144">INPUTOBJECT: <ITimeSeriesInsightsIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="ff9cc-144">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ff9cc-145">`[AccessPolicyName <String>]`: 액세스 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ff9cc-145">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="ff9cc-146">`[EnvironmentName <String>]`: 환경의 이름</span><span class="sxs-lookup"><span data-stu-id="ff9cc-146">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="ff9cc-147">`[EventSourceName <String>]`: 지정된 환경과 연결된 Time Series Insights 이벤트 원본의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ff9cc-147">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="ff9cc-148">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="ff9cc-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ff9cc-149">`[ReferenceDataSetName <String>]`: 참조 데이터 집합의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ff9cc-149">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="ff9cc-150">`[ResourceGroupName <String>]`: Azure 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ff9cc-150">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="ff9cc-151">`[SubscriptionId <String>]`: Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="ff9cc-151">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="ff9cc-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ff9cc-152">RELATED LINKS</span></span>

