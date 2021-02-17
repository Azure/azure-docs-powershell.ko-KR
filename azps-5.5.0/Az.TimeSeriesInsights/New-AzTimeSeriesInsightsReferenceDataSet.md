---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/new-aztimeseriesinsightsreferencedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsReferenceDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsReferenceDataSet.md
ms.openlocfilehash: 39bbdf61a5068ea32f1febf66249213264235dfc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190548"
---
# <span data-ttu-id="b6b16-101">New-AzTimeSeriesInsightsReferenceDataSet</span><span class="sxs-lookup"><span data-stu-id="b6b16-101">New-AzTimeSeriesInsightsReferenceDataSet</span></span>

## <span data-ttu-id="b6b16-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6b16-102">SYNOPSIS</span></span>
<span data-ttu-id="b6b16-103">지정된 환경에서 참조 데이터 집합을 만들거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="b6b16-103">Create or update a reference data set in the specified environment.</span></span>

## <span data-ttu-id="b6b16-104">구문</span><span class="sxs-lookup"><span data-stu-id="b6b16-104">SYNTAX</span></span>

```
New-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 -KeyProperty <IReferenceDataSetKeyProperty[]> -Location <String> [-SubscriptionId <String>]
 [-DataStringComparisonBehavior <DataStringComparisonBehavior>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b6b16-105">설명</span><span class="sxs-lookup"><span data-stu-id="b6b16-105">DESCRIPTION</span></span>
<span data-ttu-id="b6b16-106">지정된 환경에서 참조 데이터 집합을 만들거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="b6b16-106">Create or update a reference data set in the specified environment.</span></span>

## <span data-ttu-id="b6b16-107">예제</span><span class="sxs-lookup"><span data-stu-id="b6b16-107">EXAMPLES</span></span>

### <span data-ttu-id="b6b16-108">예제 1: 지정된 환경에 대한 참조 데이터 집합 만들기</span><span class="sxs-lookup"><span data-stu-id="b6b16-108">Example 1: Create a reference data set for a specified environment</span></span>  
```powershell
PS C:\> $mykeyproperties = @{ "name" = "device01"; "type" = "Double"}
PS C:\> New-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -Name dstest001 -ResourceGroupName testgroup -Location eastus -DataStringComparisonBehavior Ordinal -KeyProperty $mykeyproperties

Location Name      Type
-------- ----      ----
eastus   dstest001 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="b6b16-109">이 명령은 특정 환경에 대한 참조 데이터 집합을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b6b16-109">This command creates a reference data set for a specific environment.</span></span>

## <span data-ttu-id="b6b16-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b6b16-110">PARAMETERS</span></span>

### <span data-ttu-id="b6b16-111">-DataStringComparisonBehavior</span><span class="sxs-lookup"><span data-stu-id="b6b16-111">-DataStringComparisonBehavior</span></span>
<span data-ttu-id="b6b16-112">이 속성을 사용하여 참조 데이터 집합 키 비교 동작을 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b6b16-112">The reference data set key comparison behavior can be set using this property.</span></span>
<span data-ttu-id="b6b16-113">기본적으로 값은 'Ordinal'입니다. 즉, 참조 데이터를 이벤트와 조인하거나 새 참조 데이터를 추가하는 동안 대소문자 구분 키 비교가 수행됩니다.</span><span class="sxs-lookup"><span data-stu-id="b6b16-113">By default, the value is 'Ordinal' - which means case sensitive key comparison will be performed while joining reference data with events or while adding new reference data.</span></span>
<span data-ttu-id="b6b16-114">'OrdinalIgnoreCase'를 설정하면 대소문자 비대화 비교가 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="b6b16-114">When 'OrdinalIgnoreCase' is set, case insensitive comparison will be used.</span></span>

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

### <span data-ttu-id="b6b16-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6b16-115">-DefaultProfile</span></span>
<span data-ttu-id="b6b16-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b6b16-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6b16-117">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="b6b16-117">-EnvironmentName</span></span>
<span data-ttu-id="b6b16-118">지정된 리소스 그룹과 연결된 Time Series Insights 환경의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b6b16-118">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="b6b16-119">-KeyProperty</span><span class="sxs-lookup"><span data-stu-id="b6b16-119">-KeyProperty</span></span>
<span data-ttu-id="b6b16-120">참조 데이터 집합에 대한 키 속성 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="b6b16-120">The list of key properties for the reference data set.</span></span>
<span data-ttu-id="b6b16-121">생성을 위해 KEYPROPERTY 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="b6b16-121">To construct, see NOTES section for KEYPROPERTY properties and create a hash table.</span></span>

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

### <span data-ttu-id="b6b16-122">-Location</span><span class="sxs-lookup"><span data-stu-id="b6b16-122">-Location</span></span>
<span data-ttu-id="b6b16-123">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="b6b16-123">The location of the resource.</span></span>

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

### <span data-ttu-id="b6b16-124">-Name</span><span class="sxs-lookup"><span data-stu-id="b6b16-124">-Name</span></span>
<span data-ttu-id="b6b16-125">참조 데이터 집합의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b6b16-125">Name of the reference data set.</span></span>

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

### <span data-ttu-id="b6b16-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6b16-126">-ResourceGroupName</span></span>
<span data-ttu-id="b6b16-127">Azure 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b6b16-127">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="b6b16-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b6b16-128">-SubscriptionId</span></span>
<span data-ttu-id="b6b16-129">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="b6b16-129">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="b6b16-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="b6b16-130">-Tag</span></span>
<span data-ttu-id="b6b16-131">리소스에 대한 추가 속성의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="b6b16-131">Key-value pairs of additional properties for the resource.</span></span>

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

### <span data-ttu-id="b6b16-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b6b16-132">-Confirm</span></span>
<span data-ttu-id="b6b16-133">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b6b16-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6b16-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6b16-134">-WhatIf</span></span>
<span data-ttu-id="b6b16-135">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="b6b16-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6b16-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b6b16-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6b16-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6b16-137">CommonParameters</span></span>
<span data-ttu-id="b6b16-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b6b16-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6b16-139">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b6b16-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6b16-140">입력</span><span class="sxs-lookup"><span data-stu-id="b6b16-140">INPUTS</span></span>

## <span data-ttu-id="b6b16-141">출력</span><span class="sxs-lookup"><span data-stu-id="b6b16-141">OUTPUTS</span></span>

### <span data-ttu-id="b6b16-142">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IReferenceDataSetResource</span><span class="sxs-lookup"><span data-stu-id="b6b16-142">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IReferenceDataSetResource</span></span>

## <span data-ttu-id="b6b16-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b6b16-143">NOTES</span></span>

<span data-ttu-id="b6b16-144">별칭</span><span class="sxs-lookup"><span data-stu-id="b6b16-144">ALIASES</span></span>

<span data-ttu-id="b6b16-145">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="b6b16-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b6b16-146">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="b6b16-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b6b16-147">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b6b16-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b6b16-148">KEYPROPERTY <IReferenceDataSetKeyProperty[]>: 참조 데이터 집합에 대한 키 속성 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="b6b16-148">KEYPROPERTY <IReferenceDataSetKeyProperty[]>: The list of key properties for the reference data set.</span></span>
  - <span data-ttu-id="b6b16-149">`[Name <String>]`: 키 속성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b6b16-149">`[Name <String>]`: The name of the key property.</span></span>
  - <span data-ttu-id="b6b16-150">`[Type <ReferenceDataKeyPropertyType?>]`: 키 속성의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="b6b16-150">`[Type <ReferenceDataKeyPropertyType?>]`: The type of the key property.</span></span>

## <span data-ttu-id="b6b16-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b6b16-151">RELATED LINKS</span></span>

