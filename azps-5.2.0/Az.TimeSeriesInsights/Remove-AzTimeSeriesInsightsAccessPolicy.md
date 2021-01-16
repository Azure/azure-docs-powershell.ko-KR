---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/remove-aztimeseriesinsightsaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsAccessPolicy.md
ms.openlocfilehash: 2a6c58729d08c5bd060434c7a21720f87a3f7de3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98349077"
---
# <span data-ttu-id="9aaf1-101">Remove-AzTimeSeriesInsightsAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="9aaf1-101">Remove-AzTimeSeriesInsightsAccessPolicy</span></span>

## <span data-ttu-id="9aaf1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9aaf1-102">SYNOPSIS</span></span>
<span data-ttu-id="9aaf1-103">지정된 구독, 리소스 그룹 및 환경에서 지정된 이름으로 액세스 정책을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="9aaf1-103">Deletes the access policy with the specified name in the specified subscription, resource group, and environment</span></span>

## <span data-ttu-id="9aaf1-104">구문</span><span class="sxs-lookup"><span data-stu-id="9aaf1-104">SYNTAX</span></span>

### <span data-ttu-id="9aaf1-105">삭제(기본값)</span><span class="sxs-lookup"><span data-stu-id="9aaf1-105">Delete (Default)</span></span>
```
Remove-AzTimeSeriesInsightsAccessPolicy -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="9aaf1-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9aaf1-106">DeleteViaIdentity</span></span>
```
Remove-AzTimeSeriesInsightsAccessPolicy -InputObject <ITimeSeriesInsightsIdentity>
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9aaf1-107">설명</span><span class="sxs-lookup"><span data-stu-id="9aaf1-107">DESCRIPTION</span></span>
<span data-ttu-id="9aaf1-108">지정된 구독, 리소스 그룹 및 환경에서 지정된 이름으로 액세스 정책을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="9aaf1-108">Deletes the access policy with the specified name in the specified subscription, resource group, and environment</span></span>

## <span data-ttu-id="9aaf1-109">예제</span><span class="sxs-lookup"><span data-stu-id="9aaf1-109">EXAMPLES</span></span>

### <span data-ttu-id="9aaf1-110">예제 1: 이름에 따라 지정된 액세스 정책 제거</span><span class="sxs-lookup"><span data-stu-id="9aaf1-110">Example 1: Remove a specified access policy by name</span></span>
```powershell
PS C:\> Remove-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -Name policy001 -ResourceGroupName testgroup

```

<span data-ttu-id="9aaf1-111">이 명령은 지정된 액세스 정책을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="9aaf1-111">This command removes a specified access policy.</span></span>

### <span data-ttu-id="9aaf1-112">예제 2: 개체에 의해 지정된 액세스 정책 제거</span><span class="sxs-lookup"><span data-stu-id="9aaf1-112">Example 2: Remove a specified access policy by object</span></span>
```powershell
PS C:\> $policy = Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -Name policy001 -ResourceGroupName testgroup
PS C:\> Remove-AzTimeSeriesInsightsAccessPolicy -InputObject $policy

```

<span data-ttu-id="9aaf1-113">이 명령은 지정된 액세스 정책을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="9aaf1-113">This command removes a specified access policy.</span></span>

## <span data-ttu-id="9aaf1-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9aaf1-114">PARAMETERS</span></span>

### <span data-ttu-id="9aaf1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9aaf1-115">-DefaultProfile</span></span>
<span data-ttu-id="9aaf1-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9aaf1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9aaf1-117">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="9aaf1-117">-EnvironmentName</span></span>
<span data-ttu-id="9aaf1-118">지정된 리소스 그룹과 연결된 Time Series Insights 환경의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9aaf1-118">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="9aaf1-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9aaf1-119">-InputObject</span></span>
<span data-ttu-id="9aaf1-120">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="9aaf1-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="9aaf1-121">-Name</span><span class="sxs-lookup"><span data-stu-id="9aaf1-121">-Name</span></span>
<span data-ttu-id="9aaf1-122">지정된 환경과 연결된 Time Series Insights 액세스 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9aaf1-122">The name of the Time Series Insights access policy associated with the specified environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: AccessPolicyName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9aaf1-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9aaf1-123">-PassThru</span></span>
<span data-ttu-id="9aaf1-124">명령이 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="9aaf1-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="9aaf1-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9aaf1-125">-ResourceGroupName</span></span>
<span data-ttu-id="9aaf1-126">Azure 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9aaf1-126">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="9aaf1-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9aaf1-127">-SubscriptionId</span></span>
<span data-ttu-id="9aaf1-128">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="9aaf1-128">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="9aaf1-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9aaf1-129">-Confirm</span></span>
<span data-ttu-id="9aaf1-130">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="9aaf1-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9aaf1-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9aaf1-131">-WhatIf</span></span>
<span data-ttu-id="9aaf1-132">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="9aaf1-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9aaf1-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9aaf1-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9aaf1-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9aaf1-134">CommonParameters</span></span>
<span data-ttu-id="9aaf1-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9aaf1-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9aaf1-136">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9aaf1-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9aaf1-137">입력</span><span class="sxs-lookup"><span data-stu-id="9aaf1-137">INPUTS</span></span>

### <span data-ttu-id="9aaf1-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="9aaf1-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="9aaf1-139">출력</span><span class="sxs-lookup"><span data-stu-id="9aaf1-139">OUTPUTS</span></span>

### <span data-ttu-id="9aaf1-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9aaf1-140">System.Boolean</span></span>

## <span data-ttu-id="9aaf1-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9aaf1-141">NOTES</span></span>

<span data-ttu-id="9aaf1-142">별칭</span><span class="sxs-lookup"><span data-stu-id="9aaf1-142">ALIASES</span></span>

<span data-ttu-id="9aaf1-143">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="9aaf1-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9aaf1-144">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="9aaf1-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9aaf1-145">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9aaf1-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9aaf1-146">INPUTOBJECT: <ITimeSeriesInsightsIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="9aaf1-146">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9aaf1-147">`[AccessPolicyName <String>]`: 액세스 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9aaf1-147">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="9aaf1-148">`[EnvironmentName <String>]`: 환경의 이름</span><span class="sxs-lookup"><span data-stu-id="9aaf1-148">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="9aaf1-149">`[EventSourceName <String>]`: 지정된 환경과 연결된 Time Series Insights 이벤트 원본의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9aaf1-149">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="9aaf1-150">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="9aaf1-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9aaf1-151">`[ReferenceDataSetName <String>]`: 참조 데이터 집합의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9aaf1-151">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="9aaf1-152">`[ResourceGroupName <String>]`: Azure 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9aaf1-152">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="9aaf1-153">`[SubscriptionId <String>]`: Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="9aaf1-153">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="9aaf1-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9aaf1-154">RELATED LINKS</span></span>

