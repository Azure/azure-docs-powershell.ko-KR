---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/powershell/module/az.timeseriesinsights/new-aztimeseriesinsightsreferencedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsReferenceDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsReferenceDataSet.md
ms.openlocfilehash: 1c4e0fa2a8e204ee3b0dad160d3cfb54f58b4323
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976048"
---
# <span data-ttu-id="0ace3-101">New-AzTimeSeriesInsightsReferenceDataSet</span><span class="sxs-lookup"><span data-stu-id="0ace3-101">New-AzTimeSeriesInsightsReferenceDataSet</span></span>

## <span data-ttu-id="0ace3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ace3-102">SYNOPSIS</span></span>
<span data-ttu-id="0ace3-103">지정된 환경에서 참조 데이터 집합을 만들거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="0ace3-103">Create or update a reference data set in the specified environment.</span></span>

## <span data-ttu-id="0ace3-104">구문</span><span class="sxs-lookup"><span data-stu-id="0ace3-104">SYNTAX</span></span>

```
New-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 -KeyProperty <IReferenceDataSetKeyProperty[]> -Location <String> [-SubscriptionId <String>]
 [-DataStringComparisonBehavior <DataStringComparisonBehavior>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0ace3-105">설명</span><span class="sxs-lookup"><span data-stu-id="0ace3-105">DESCRIPTION</span></span>
<span data-ttu-id="0ace3-106">지정된 환경에서 참조 데이터 집합을 만들거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="0ace3-106">Create or update a reference data set in the specified environment.</span></span>

## <span data-ttu-id="0ace3-107">예제</span><span class="sxs-lookup"><span data-stu-id="0ace3-107">EXAMPLES</span></span>

### <span data-ttu-id="0ace3-108">예제 1: 지정된 환경에 대한 참조 데이터 집합 만들기</span><span class="sxs-lookup"><span data-stu-id="0ace3-108">Example 1: Create a reference data set for a specified environment</span></span>  
```powershell
PS C:\> $mykeyproperties = @{ "name" = "device01"; "type" = "Double"}
PS C:\> New-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -Name dstest001 -ResourceGroupName testgroup -Location eastus -DataStringComparisonBehavior Ordinal -KeyProperty $mykeyproperties

Location Name      Type
-------- ----      ----
eastus   dstest001 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="0ace3-109">이 명령은 특정 환경에 대한 참조 데이터 집합을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0ace3-109">This command creates a reference data set for a specific environment.</span></span>

## <span data-ttu-id="0ace3-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="0ace3-110">PARAMETERS</span></span>

### <span data-ttu-id="0ace3-111">-DataStringComparisonBehavior</span><span class="sxs-lookup"><span data-stu-id="0ace3-111">-DataStringComparisonBehavior</span></span>
<span data-ttu-id="0ace3-112">이 속성을 사용하여 참조 데이터 집합 키 비교 동작을 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0ace3-112">The reference data set key comparison behavior can be set using this property.</span></span>
<span data-ttu-id="0ace3-113">기본적으로 값은 'Ordinal'으로, 이벤트와 참조 데이터를 조인하거나 새 참조 데이터를 추가하는 동안 대소문자 구분 키 비교가 수행됩니다.</span><span class="sxs-lookup"><span data-stu-id="0ace3-113">By default, the value is 'Ordinal' - which means case sensitive key comparison will be performed while joining reference data with events or while adding new reference data.</span></span>
<span data-ttu-id="0ace3-114">'OrdinalIgnoreCase'가 설정되어 있는 경우 대소문자 무관정 비교가 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="0ace3-114">When 'OrdinalIgnoreCase' is set, case insensitive comparison will be used.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Support.DataStringComparisonBehavior
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ace3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ace3-115">-DefaultProfile</span></span>
<span data-ttu-id="0ace3-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0ace3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0ace3-117">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="0ace3-117">-EnvironmentName</span></span>
<span data-ttu-id="0ace3-118">지정된 리소스 그룹과 연결된 Time Series Insights 환경의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0ace3-118">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ace3-119">-KeyProperty</span><span class="sxs-lookup"><span data-stu-id="0ace3-119">-KeyProperty</span></span>
<span data-ttu-id="0ace3-120">참조 데이터 집합의 키 속성 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="0ace3-120">The list of key properties for the reference data set.</span></span>
<span data-ttu-id="0ace3-121">생성을 위해 KEYPROPERTY 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="0ace3-121">To construct, see NOTES section for KEYPROPERTY properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IReferenceDataSetKeyProperty[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ace3-122">-Location</span><span class="sxs-lookup"><span data-stu-id="0ace3-122">-Location</span></span>
<span data-ttu-id="0ace3-123">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="0ace3-123">The location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ace3-124">-Name</span><span class="sxs-lookup"><span data-stu-id="0ace3-124">-Name</span></span>
<span data-ttu-id="0ace3-125">참조 데이터 집합의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0ace3-125">Name of the reference data set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ReferenceDataSetName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ace3-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ace3-126">-ResourceGroupName</span></span>
<span data-ttu-id="0ace3-127">Azure 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0ace3-127">Name of an Azure Resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ace3-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0ace3-128">-SubscriptionId</span></span>
<span data-ttu-id="0ace3-129">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="0ace3-129">Azure Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ace3-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="0ace3-130">-Tag</span></span>
<span data-ttu-id="0ace3-131">리소스에 대한 추가 속성의 키 값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="0ace3-131">Key-value pairs of additional properties for the resource.</span></span>

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

### <span data-ttu-id="0ace3-132">-확인</span><span class="sxs-lookup"><span data-stu-id="0ace3-132">-Confirm</span></span>
<span data-ttu-id="0ace3-133">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="0ace3-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ace3-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ace3-134">-WhatIf</span></span>
<span data-ttu-id="0ace3-135">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="0ace3-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0ace3-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0ace3-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ace3-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ace3-137">CommonParameters</span></span>
<span data-ttu-id="0ace3-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0ace3-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ace3-139">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0ace3-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ace3-140">입력</span><span class="sxs-lookup"><span data-stu-id="0ace3-140">INPUTS</span></span>

## <span data-ttu-id="0ace3-141">출력</span><span class="sxs-lookup"><span data-stu-id="0ace3-141">OUTPUTS</span></span>

### <span data-ttu-id="0ace3-142">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IReferenceDataSetResource</span><span class="sxs-lookup"><span data-stu-id="0ace3-142">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IReferenceDataSetResource</span></span>

## <span data-ttu-id="0ace3-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0ace3-143">NOTES</span></span>

<span data-ttu-id="0ace3-144">별칭</span><span class="sxs-lookup"><span data-stu-id="0ace3-144">ALIASES</span></span>

<span data-ttu-id="0ace3-145">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="0ace3-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0ace3-146">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="0ace3-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0ace3-147">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0ace3-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0ace3-148">KEYPROPERTY <IReferenceDataSetKeyProperty[]>: 참조 데이터 집합의 키 속성 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="0ace3-148">KEYPROPERTY <IReferenceDataSetKeyProperty[]>: The list of key properties for the reference data set.</span></span>
  - <span data-ttu-id="0ace3-149">`[Name <String>]`: 키 속성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0ace3-149">`[Name <String>]`: The name of the key property.</span></span>
  - <span data-ttu-id="0ace3-150">`[Type <ReferenceDataKeyPropertyType?>]`: 키 속성의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="0ace3-150">`[Type <ReferenceDataKeyPropertyType?>]`: The type of the key property.</span></span>

## <span data-ttu-id="0ace3-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0ace3-151">RELATED LINKS</span></span>

