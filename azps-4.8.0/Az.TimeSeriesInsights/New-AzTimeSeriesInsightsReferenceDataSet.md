---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/new-aztimeseriesinsightsreferencedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsReferenceDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsReferenceDataSet.md
ms.openlocfilehash: 39bbdf61a5068ea32f1febf66249213264235dfc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213151"
---
# <span data-ttu-id="10d13-101">New-AzTimeSeriesInsightsReferenceDataSet</span><span class="sxs-lookup"><span data-stu-id="10d13-101">New-AzTimeSeriesInsightsReferenceDataSet</span></span>

## <span data-ttu-id="10d13-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10d13-102">SYNOPSIS</span></span>
<span data-ttu-id="10d13-103">지정 된 환경에서 참조 데이터 집합을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="10d13-103">Create or update a reference data set in the specified environment.</span></span>

## <span data-ttu-id="10d13-104">구문과</span><span class="sxs-lookup"><span data-stu-id="10d13-104">SYNTAX</span></span>

```
New-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 -KeyProperty <IReferenceDataSetKeyProperty[]> -Location <String> [-SubscriptionId <String>]
 [-DataStringComparisonBehavior <DataStringComparisonBehavior>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="10d13-105">설명은</span><span class="sxs-lookup"><span data-stu-id="10d13-105">DESCRIPTION</span></span>
<span data-ttu-id="10d13-106">지정 된 환경에서 참조 데이터 집합을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="10d13-106">Create or update a reference data set in the specified environment.</span></span>

## <span data-ttu-id="10d13-107">예제의</span><span class="sxs-lookup"><span data-stu-id="10d13-107">EXAMPLES</span></span>

### <span data-ttu-id="10d13-108">예제 1: 지정 된 환경에 대 한 참조 데이터 집합 만들기</span><span class="sxs-lookup"><span data-stu-id="10d13-108">Example 1: Create a reference data set for a specified environment</span></span>  
```powershell
PS C:\> $mykeyproperties = @{ "name" = "device01"; "type" = "Double"}
PS C:\> New-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -Name dstest001 -ResourceGroupName testgroup -Location eastus -DataStringComparisonBehavior Ordinal -KeyProperty $mykeyproperties

Location Name      Type
-------- ----      ----
eastus   dstest001 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="10d13-109">이 명령은 특정 환경에 대 한 참조 데이터 집합을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="10d13-109">This command creates a reference data set for a specific environment.</span></span>

## <span data-ttu-id="10d13-110">변수</span><span class="sxs-lookup"><span data-stu-id="10d13-110">PARAMETERS</span></span>

### <span data-ttu-id="10d13-111">-DataStringComparisonBehavior</span><span class="sxs-lookup"><span data-stu-id="10d13-111">-DataStringComparisonBehavior</span></span>
<span data-ttu-id="10d13-112">이 속성을 사용 하 여 참조 데이터 설정 키 비교 동작을 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="10d13-112">The reference data set key comparison behavior can be set using this property.</span></span>
<span data-ttu-id="10d13-113">기본적으로 값은 ' 서 수 '입니다. 참조 데이터를 이벤트와 조인 하거나 새 참조 데이터를 추가 하는 동안 대/소문자 구분 키 비교가 수행 됨을 의미 합니다.</span><span class="sxs-lookup"><span data-stu-id="10d13-113">By default, the value is 'Ordinal' - which means case sensitive key comparison will be performed while joining reference data with events or while adding new reference data.</span></span>
<span data-ttu-id="10d13-114">' OrdinalIgnoreCase '가 설정 되 면 대/소문자를 구분 하지 않는 비교를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="10d13-114">When 'OrdinalIgnoreCase' is set, case insensitive comparison will be used.</span></span>

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

### <span data-ttu-id="10d13-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10d13-115">-DefaultProfile</span></span>
<span data-ttu-id="10d13-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="10d13-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="10d13-117">-환경 이름</span><span class="sxs-lookup"><span data-stu-id="10d13-117">-EnvironmentName</span></span>
<span data-ttu-id="10d13-118">지정 된 리소스 그룹과 연결 된 시계열 Insights 환경의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="10d13-118">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="10d13-119">-KeyProperty</span><span class="sxs-lookup"><span data-stu-id="10d13-119">-KeyProperty</span></span>
<span data-ttu-id="10d13-120">참조 데이터 집합에 대 한 키 속성의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="10d13-120">The list of key properties for the reference data set.</span></span>
<span data-ttu-id="10d13-121">생성 하려면 KEYPROPERTY 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="10d13-121">To construct, see NOTES section for KEYPROPERTY properties and create a hash table.</span></span>

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

### <span data-ttu-id="10d13-122">-위치</span><span class="sxs-lookup"><span data-stu-id="10d13-122">-Location</span></span>
<span data-ttu-id="10d13-123">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="10d13-123">The location of the resource.</span></span>

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

### <span data-ttu-id="10d13-124">-이름</span><span class="sxs-lookup"><span data-stu-id="10d13-124">-Name</span></span>
<span data-ttu-id="10d13-125">참조 데이터 집합의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="10d13-125">Name of the reference data set.</span></span>

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

### <span data-ttu-id="10d13-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10d13-126">-ResourceGroupName</span></span>
<span data-ttu-id="10d13-127">Azure 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="10d13-127">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="10d13-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="10d13-128">-SubscriptionId</span></span>
<span data-ttu-id="10d13-129">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="10d13-129">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="10d13-130">태그</span><span class="sxs-lookup"><span data-stu-id="10d13-130">-Tag</span></span>
<span data-ttu-id="10d13-131">리소스에 대 한 추가 속성의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="10d13-131">Key-value pairs of additional properties for the resource.</span></span>

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

### <span data-ttu-id="10d13-132">-확인</span><span class="sxs-lookup"><span data-stu-id="10d13-132">-Confirm</span></span>
<span data-ttu-id="10d13-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="10d13-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10d13-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10d13-134">-WhatIf</span></span>
<span data-ttu-id="10d13-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="10d13-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10d13-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="10d13-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10d13-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10d13-137">CommonParameters</span></span>
<span data-ttu-id="10d13-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="10d13-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10d13-139">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="10d13-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10d13-140">입력</span><span class="sxs-lookup"><span data-stu-id="10d13-140">INPUTS</span></span>

## <span data-ttu-id="10d13-141">출력</span><span class="sxs-lookup"><span data-stu-id="10d13-141">OUTPUTS</span></span>

### <span data-ttu-id="10d13-142">Api20200515. IReferenceDataSetResource를 호출 하는 경우.</span><span class="sxs-lookup"><span data-stu-id="10d13-142">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IReferenceDataSetResource</span></span>

## <span data-ttu-id="10d13-143">상속자</span><span class="sxs-lookup"><span data-stu-id="10d13-143">NOTES</span></span>

<span data-ttu-id="10d13-144">별칭과</span><span class="sxs-lookup"><span data-stu-id="10d13-144">ALIASES</span></span>

<span data-ttu-id="10d13-145">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="10d13-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="10d13-146">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="10d13-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="10d13-147">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="10d13-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="10d13-148">KEYPROPERTY <IReferenceDataSetKeyProperty [] >: 참조 데이터 집합에 대 한 키 속성의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="10d13-148">KEYPROPERTY <IReferenceDataSetKeyProperty[]>: The list of key properties for the reference data set.</span></span>
  - <span data-ttu-id="10d13-149">`[Name <String>]`: 키 속성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="10d13-149">`[Name <String>]`: The name of the key property.</span></span>
  - <span data-ttu-id="10d13-150">`[Type <ReferenceDataKeyPropertyType?>]`: 키 속성의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="10d13-150">`[Type <ReferenceDataKeyPropertyType?>]`: The type of the key property.</span></span>

## <span data-ttu-id="10d13-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="10d13-151">RELATED LINKS</span></span>

