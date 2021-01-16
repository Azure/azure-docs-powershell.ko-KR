---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/get-aztimeseriesinsightsaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsAccessPolicy.md
ms.openlocfilehash: c7d8f46f42b1b42e4831540f5c68706c61ff78cf
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98360879"
---
# <span data-ttu-id="e3889-101">Get-AzTimeSeriesInsightsAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e3889-101">Get-AzTimeSeriesInsightsAccessPolicy</span></span>

## <span data-ttu-id="e3889-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3889-102">SYNOPSIS</span></span>
<span data-ttu-id="e3889-103">지정된 환경에서 지정된 이름의 액세스 정책을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e3889-103">Gets the access policy with the specified name in the specified environment.</span></span>

## <span data-ttu-id="e3889-104">구문</span><span class="sxs-lookup"><span data-stu-id="e3889-104">SYNTAX</span></span>

### <span data-ttu-id="e3889-105">목록(기본값)</span><span class="sxs-lookup"><span data-stu-id="e3889-105">List (Default)</span></span>
```
Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e3889-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="e3889-106">Get</span></span>
```
Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e3889-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e3889-107">GetViaIdentity</span></span>
```
Get-AzTimeSeriesInsightsAccessPolicy -InputObject <ITimeSeriesInsightsIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="e3889-108">설명</span><span class="sxs-lookup"><span data-stu-id="e3889-108">DESCRIPTION</span></span>
<span data-ttu-id="e3889-109">지정된 환경에서 지정된 이름의 액세스 정책을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e3889-109">Gets the access policy with the specified name in the specified environment.</span></span>

## <span data-ttu-id="e3889-110">예제</span><span class="sxs-lookup"><span data-stu-id="e3889-110">EXAMPLES</span></span>

### <span data-ttu-id="e3889-111">예제 1: 지정된 환경의 모든 액세스 정책 나열</span><span class="sxs-lookup"><span data-stu-id="e3889-111">Example 1: List all access policies under a specified environment</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -ResourceGroupName testgroup

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
policy002 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="e3889-112">이 명령은 지정된 환경의 모든 액세스 정책을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="e3889-112">This command lists all access policies under a specified environment.</span></span>

### <span data-ttu-id="e3889-113">예제 2: 이름에 따라 지정된 액세스 정책 얻기</span><span class="sxs-lookup"><span data-stu-id="e3889-113">Example 2: Get a specified access policy by name</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -ResourceGroupName testgroup -Name policy001

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="e3889-114">이 명령은 지정된 액세스 정책을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e3889-114">This command gets a specified access policy.</span></span>

### <span data-ttu-id="e3889-115">예제 3: 개체에 따라 지정된 액세스 정책 얻기</span><span class="sxs-lookup"><span data-stu-id="e3889-115">Example 3: Get a specified access policy by object</span></span>
```powershell
PS C:\>$ap = Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsi-envv8u56x -ResourceGroupName tsi-test-i01k5l -Name tsi-apilgj5y 
PS C:\>Get-AzTimeSeriesInsightsAccessPolicy -InputObject $ap

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="e3889-116">이 명령은 지정된 액세스 정책을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e3889-116">This command gets a specified access policy.</span></span>

## <span data-ttu-id="e3889-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e3889-117">PARAMETERS</span></span>

### <span data-ttu-id="e3889-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3889-118">-DefaultProfile</span></span>
<span data-ttu-id="e3889-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e3889-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3889-120">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="e3889-120">-EnvironmentName</span></span>
<span data-ttu-id="e3889-121">지정된 리소스 그룹과 연결된 Time Series Insights 환경의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e3889-121">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3889-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e3889-122">-InputObject</span></span>
<span data-ttu-id="e3889-123">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="e3889-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e3889-124">-Name</span><span class="sxs-lookup"><span data-stu-id="e3889-124">-Name</span></span>
<span data-ttu-id="e3889-125">지정된 환경과 연결된 Time Series Insights 액세스 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e3889-125">The name of the Time Series Insights access policy associated with the specified environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: AccessPolicyName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3889-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3889-126">-ResourceGroupName</span></span>
<span data-ttu-id="e3889-127">Azure 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e3889-127">Name of an Azure Resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3889-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e3889-128">-SubscriptionId</span></span>
<span data-ttu-id="e3889-129">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="e3889-129">Azure Subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3889-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3889-130">CommonParameters</span></span>
<span data-ttu-id="e3889-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e3889-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3889-132">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e3889-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3889-133">입력</span><span class="sxs-lookup"><span data-stu-id="e3889-133">INPUTS</span></span>

### <span data-ttu-id="e3889-134">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="e3889-134">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="e3889-135">출력</span><span class="sxs-lookup"><span data-stu-id="e3889-135">OUTPUTS</span></span>

### <span data-ttu-id="e3889-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IAccessPolicyResource</span><span class="sxs-lookup"><span data-stu-id="e3889-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IAccessPolicyResource</span></span>

## <span data-ttu-id="e3889-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e3889-137">NOTES</span></span>

<span data-ttu-id="e3889-138">별칭</span><span class="sxs-lookup"><span data-stu-id="e3889-138">ALIASES</span></span>

<span data-ttu-id="e3889-139">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="e3889-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e3889-140">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="e3889-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e3889-141">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e3889-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e3889-142">INPUTOBJECT: <ITimeSeriesInsightsIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="e3889-142">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e3889-143">`[AccessPolicyName <String>]`: 액세스 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e3889-143">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="e3889-144">`[EnvironmentName <String>]`: 환경의 이름</span><span class="sxs-lookup"><span data-stu-id="e3889-144">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="e3889-145">`[EventSourceName <String>]`: 지정된 환경과 연결된 Time Series Insights 이벤트 원본의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e3889-145">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="e3889-146">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="e3889-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e3889-147">`[ReferenceDataSetName <String>]`: 참조 데이터 집합의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e3889-147">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="e3889-148">`[ResourceGroupName <String>]`: Azure 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e3889-148">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="e3889-149">`[SubscriptionId <String>]`: Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="e3889-149">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="e3889-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e3889-150">RELATED LINKS</span></span>

