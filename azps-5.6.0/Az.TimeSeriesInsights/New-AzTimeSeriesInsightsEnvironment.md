---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/powershell/module/az.timeseriesinsights/new-aztimeseriesinsightsenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsEnvironment.md
ms.openlocfilehash: 51cbe7cd6d4e08543feadb5ddd096330763b7236
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955051"
---
# <span data-ttu-id="eb269-101">New-AzTimeSeriesInsightsEnvironment</span><span class="sxs-lookup"><span data-stu-id="eb269-101">New-AzTimeSeriesInsightsEnvironment</span></span>

## <span data-ttu-id="eb269-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eb269-102">SYNOPSIS</span></span>
<span data-ttu-id="eb269-103">지정된 구독 및 리소스 그룹에 환경을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="eb269-103">Create an environment in the specified subscription and resource group.</span></span>

## <span data-ttu-id="eb269-104">구문</span><span class="sxs-lookup"><span data-stu-id="eb269-104">SYNTAX</span></span>

### <span data-ttu-id="eb269-105">Gen1(기본값)</span><span class="sxs-lookup"><span data-stu-id="eb269-105">Gen1 (Default)</span></span>
```
New-AzTimeSeriesInsightsEnvironment -Name <String> -ResourceGroupName <String> -Capacity <Int32>
 -DataRetentionTime <TimeSpan> -Kind <Kind> -Location <String> -Sku <SkuName> [-SubscriptionId <String>]
 [-PartitionKeyProperty <ITimeSeriesIdProperty[]>] [-StorageLimitExceededBehavior <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="eb269-106">Gen2</span><span class="sxs-lookup"><span data-stu-id="eb269-106">Gen2</span></span>
```
New-AzTimeSeriesInsightsEnvironment -Name <String> -ResourceGroupName <String> -Kind <Kind> -Location <String>
 -Sku <SkuName> -StorageAccountKey <SecureString> -StorageAccountName <String>
 -TimeSeriesIdProperty <ITimeSeriesIdProperty[]> [-SubscriptionId <String>] [-Tag <Hashtable>]
 [-WarmStoreDataRetentionTime <TimeSpan>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="eb269-107">설명</span><span class="sxs-lookup"><span data-stu-id="eb269-107">DESCRIPTION</span></span>
<span data-ttu-id="eb269-108">지정된 구독 및 리소스 그룹에 환경을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="eb269-108">Create an environment in the specified subscription and resource group.</span></span>

## <span data-ttu-id="eb269-109">예제</span><span class="sxs-lookup"><span data-stu-id="eb269-109">EXAMPLES</span></span>

### <span data-ttu-id="eb269-110">예제 1: Gen1 타임 시리즈 인사이트 환경 만들기</span><span class="sxs-lookup"><span data-stu-id="eb269-110">Example 1: Create a Gen1 time series insights environment</span></span>
```powershell
PS C:\> $TimeSpan = New-TimeSpan -Days 1 -Hours 1 -Minutes 25
PS C:\> New-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsitest001 -Kind Gen1 -Location eastus -Sku S1 -DataRetentionTime $TimeSpan -Capacity 2

Kind     Location Name       SkuCapacity SkuName Type
----     -------- ----       ----------- ------- ----
Gen1 eastus   tsitest001 2           S1      Microsoft.TimeSeriesInsights/Environments
```

<span data-ttu-id="eb269-111">이 명령은 Gen1 타임 시리즈 인사이트 환경을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="eb269-111">This command creates a Gen1 time series insights environment.</span></span>

### <span data-ttu-id="eb269-112">예제 2: Gen2 타임 시리즈 인사이트 환경 만들기</span><span class="sxs-lookup"><span data-stu-id="eb269-112">Example 2: Create a Gen2 time series insights environment</span></span>
```powershell
PS C:\> $ks = Get-AzStorageAccountKey -ResourceGroupName "testgroup" -Name "staccount001"
PS C:\> $k  = $ks[0].Value | ConvertTo-SecureString -AsPlainText -Force
PS C:\> New-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsitest002 -Kind Gen2 -Location eastus -Sku L1 -StorageAccountName staccount001 -StorageAccountKey $k -TimeSeriesIdProperty @{name='cdc';type='string'}

Kind     Location Name       SkuCapacity SkuName Type
----     -------- ----       ----------- ------- ----
Gen2 eastus   tsitest002 1           L1      Microsoft.TimeSeriesInsights/Environments
```

<span data-ttu-id="eb269-113">이 명령은 Gen2 타임 시리즈 인사이트 환경을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="eb269-113">This command creates a Gen2 time series insights environment.</span></span>

## <span data-ttu-id="eb269-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="eb269-114">PARAMETERS</span></span>

### <span data-ttu-id="eb269-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eb269-115">-AsJob</span></span>
<span data-ttu-id="eb269-116">작업으로 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="eb269-116">Run the command as a job</span></span>

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

### <span data-ttu-id="eb269-117">-Capacity</span><span class="sxs-lookup"><span data-stu-id="eb269-117">-Capacity</span></span>
<span data-ttu-id="eb269-118">sku의 용량입니다.</span><span class="sxs-lookup"><span data-stu-id="eb269-118">The capacity of the sku.</span></span>
<span data-ttu-id="eb269-119">Gen1 환경의 경우 이 값을 변경하여 만든 후 환경 확장을 지원할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eb269-119">For Gen1 environments, this value can be changed to support scale out of environments after they have been created.</span></span>

```yaml
Type: System.Int32
Parameter Sets: Gen1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb269-120">-DataRetentionTime</span><span class="sxs-lookup"><span data-stu-id="eb269-120">-DataRetentionTime</span></span>
<span data-ttu-id="eb269-121">데이터 보존 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="eb269-121">The data retention time.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: Gen1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb269-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb269-122">-DefaultProfile</span></span>
<span data-ttu-id="eb269-123">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="eb269-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eb269-124">-Kind</span><span class="sxs-lookup"><span data-stu-id="eb269-124">-Kind</span></span>
<span data-ttu-id="eb269-125">환경의 종류입니다.</span><span class="sxs-lookup"><span data-stu-id="eb269-125">The kind of the environment.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Support.Kind
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb269-126">-Location</span><span class="sxs-lookup"><span data-stu-id="eb269-126">-Location</span></span>
<span data-ttu-id="eb269-127">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="eb269-127">The location of the resource.</span></span>

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

### <span data-ttu-id="eb269-128">-Name</span><span class="sxs-lookup"><span data-stu-id="eb269-128">-Name</span></span>
<span data-ttu-id="eb269-129">환경 이름</span><span class="sxs-lookup"><span data-stu-id="eb269-129">Name of the environment</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb269-130">-NoWait</span><span class="sxs-lookup"><span data-stu-id="eb269-130">-NoWait</span></span>
<span data-ttu-id="eb269-131">명령 비동기 실행</span><span class="sxs-lookup"><span data-stu-id="eb269-131">Run the command asynchronously</span></span>

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

### <span data-ttu-id="eb269-132">-PartitionKeyProperty</span><span class="sxs-lookup"><span data-stu-id="eb269-132">-PartitionKeyProperty</span></span>
<span data-ttu-id="eb269-133">환경에서 데이터를 분할하는 데 사용할 이벤트 속성 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="eb269-133">The list of event properties which will be used to partition data in the environment.</span></span>
<span data-ttu-id="eb269-134">생성을 위해 PARTITIONKEYPROPERTY 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="eb269-134">To construct, see NOTES section for PARTITIONKEYPROPERTY properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.ITimeSeriesIdProperty[]
Parameter Sets: Gen1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb269-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb269-135">-ResourceGroupName</span></span>
<span data-ttu-id="eb269-136">Azure 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="eb269-136">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="eb269-137">-Sku</span><span class="sxs-lookup"><span data-stu-id="eb269-137">-Sku</span></span>
<span data-ttu-id="eb269-138">이 SKU의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="eb269-138">The name of this SKU.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Support.SkuName
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb269-139">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="eb269-139">-StorageAccountKey</span></span>
<span data-ttu-id="eb269-140">Time Series Insights 서비스 쓰기 액세스 권한을 저장소 계정에 부여하는 관리 키의 값입니다.</span><span class="sxs-lookup"><span data-stu-id="eb269-140">The value of the management key that grants the Time Series Insights service write access to the storage account.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: Gen2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb269-141">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="eb269-141">-StorageAccountName</span></span>
<span data-ttu-id="eb269-142">환경의 장기 데이터를 보유할 저장소 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="eb269-142">The name of the storage account that will hold the environment's long term data.</span></span>

```yaml
Type: System.String
Parameter Sets: Gen2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb269-143">-StorageLimitExceededBehavior</span><span class="sxs-lookup"><span data-stu-id="eb269-143">-StorageLimitExceededBehavior</span></span>
<span data-ttu-id="eb269-144">Time Series Insights 서비스가 환경의 용량을 초과할 때 취해야 하는 동작</span><span class="sxs-lookup"><span data-stu-id="eb269-144">The behavior the Time Series Insights service should take when the environment's capacity has been exceeded</span></span>

```yaml
Type: System.String
Parameter Sets: Gen1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb269-145">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="eb269-145">-SubscriptionId</span></span>
<span data-ttu-id="eb269-146">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="eb269-146">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="eb269-147">-Tag</span><span class="sxs-lookup"><span data-stu-id="eb269-147">-Tag</span></span>
<span data-ttu-id="eb269-148">리소스에 대한 추가 속성의 키 값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="eb269-148">Key-value pairs of additional properties for the resource.</span></span>

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

### <span data-ttu-id="eb269-149">-TimeSeriesIdProperty</span><span class="sxs-lookup"><span data-stu-id="eb269-149">-TimeSeriesIdProperty</span></span>
<span data-ttu-id="eb269-150">환경의 타임 시리즈 ID를 정의하는 데 사용할 이벤트 속성 목록입니다. 생성을 위해 TIMESERIESIDPROPERTY 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="eb269-150">The list of event properties which will be used to define the environment's time series id. To construct, see NOTES section for TIMESERIESIDPROPERTY properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.ITimeSeriesIdProperty[]
Parameter Sets: Gen2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb269-151">-WarmStoreDataRetentionTime</span><span class="sxs-lookup"><span data-stu-id="eb269-151">-WarmStoreDataRetentionTime</span></span>
<span data-ttu-id="eb269-152">환경의 이벤트가 웜 저장소에서 쿼리에 사용할 수 있는 일 수를 지정하는 ISO8601 timespan입니다.</span><span class="sxs-lookup"><span data-stu-id="eb269-152">ISO8601 timespan specifying the number of days the environment's events will be available for query from the warm store.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: Gen2
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb269-153">-확인</span><span class="sxs-lookup"><span data-stu-id="eb269-153">-Confirm</span></span>
<span data-ttu-id="eb269-154">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="eb269-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb269-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb269-155">-WhatIf</span></span>
<span data-ttu-id="eb269-156">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="eb269-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb269-157">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="eb269-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb269-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb269-158">CommonParameters</span></span>
<span data-ttu-id="eb269-159">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="eb269-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb269-160">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="eb269-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb269-161">입력</span><span class="sxs-lookup"><span data-stu-id="eb269-161">INPUTS</span></span>

## <span data-ttu-id="eb269-162">출력</span><span class="sxs-lookup"><span data-stu-id="eb269-162">OUTPUTS</span></span>

### <span data-ttu-id="eb269-163">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEnvironmentResource</span><span class="sxs-lookup"><span data-stu-id="eb269-163">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEnvironmentResource</span></span>

## <span data-ttu-id="eb269-164">참고 사항</span><span class="sxs-lookup"><span data-stu-id="eb269-164">NOTES</span></span>

<span data-ttu-id="eb269-165">별칭</span><span class="sxs-lookup"><span data-stu-id="eb269-165">ALIASES</span></span>

<span data-ttu-id="eb269-166">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="eb269-166">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="eb269-167">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="eb269-167">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="eb269-168">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="eb269-168">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="eb269-169">PARTITIONKEYPROPERTY <ITimeSeriesIdProperty[]>: 환경에서 데이터를 분할하는 데 사용할 이벤트 속성 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="eb269-169">PARTITIONKEYPROPERTY <ITimeSeriesIdProperty[]>: The list of event properties which will be used to partition data in the environment.</span></span>
  - <span data-ttu-id="eb269-170">`[Name <String>]`: 속성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="eb269-170">`[Name <String>]`: The name of the property.</span></span>
  - <span data-ttu-id="eb269-171">`[Type <PropertyType?>]`: 속성의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="eb269-171">`[Type <PropertyType?>]`: The type of the property.</span></span>

<span data-ttu-id="eb269-172">TIMESERIESIDPROPERTY <ITimeSeriesIdProperty[]>: 환경의 타임 시리즈 ID를 정의하는 데 사용할 이벤트 속성 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="eb269-172">TIMESERIESIDPROPERTY <ITimeSeriesIdProperty[]>: The list of event properties which will be used to define the environment's time series id.</span></span>
  - <span data-ttu-id="eb269-173">`[Name <String>]`: 속성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="eb269-173">`[Name <String>]`: The name of the property.</span></span>
  - <span data-ttu-id="eb269-174">`[Type <PropertyType?>]`: 속성의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="eb269-174">`[Type <PropertyType?>]`: The type of the property.</span></span>

## <span data-ttu-id="eb269-175">관련 링크</span><span class="sxs-lookup"><span data-stu-id="eb269-175">RELATED LINKS</span></span>

