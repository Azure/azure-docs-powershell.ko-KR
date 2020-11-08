---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/new-aztimeseriesinsightsenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsEnvironment.md
ms.openlocfilehash: b4f27c31ebc3eb54727d6df1139409529c20eed9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213445"
---
# <span data-ttu-id="fcbac-101">New-AzTimeSeriesInsightsEnvironment</span><span class="sxs-lookup"><span data-stu-id="fcbac-101">New-AzTimeSeriesInsightsEnvironment</span></span>

## <span data-ttu-id="fcbac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fcbac-102">SYNOPSIS</span></span>
<span data-ttu-id="fcbac-103">지정 된 구독 및 리소스 그룹에서 환경을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fcbac-103">Create an environment in the specified subscription and resource group.</span></span>

## <span data-ttu-id="fcbac-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fcbac-104">SYNTAX</span></span>

### <span data-ttu-id="fcbac-105">Gen1 (기본값)</span><span class="sxs-lookup"><span data-stu-id="fcbac-105">Gen1 (Default)</span></span>
```
New-AzTimeSeriesInsightsEnvironment -Name <String> -ResourceGroupName <String> -Capacity <Int32>
 -DataRetentionTime <TimeSpan> -Kind <Kind> -Location <String> -Sku <SkuName> [-SubscriptionId <String>]
 [-PartitionKeyProperty <ITimeSeriesIdProperty[]>] [-StorageLimitExceededBehavior <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="fcbac-106">Gen2</span><span class="sxs-lookup"><span data-stu-id="fcbac-106">Gen2</span></span>
```
New-AzTimeSeriesInsightsEnvironment -Name <String> -ResourceGroupName <String> -Kind <Kind> -Location <String>
 -Sku <SkuName> -StorageAccountKey <SecureString> -StorageAccountName <String>
 -TimeSeriesIdProperty <ITimeSeriesIdProperty[]> [-SubscriptionId <String>] [-Tag <Hashtable>]
 [-WarmStoreDataRetentionTime <TimeSpan>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="fcbac-107">설명은</span><span class="sxs-lookup"><span data-stu-id="fcbac-107">DESCRIPTION</span></span>
<span data-ttu-id="fcbac-108">지정 된 구독 및 리소스 그룹에서 환경을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fcbac-108">Create an environment in the specified subscription and resource group.</span></span>

## <span data-ttu-id="fcbac-109">예제의</span><span class="sxs-lookup"><span data-stu-id="fcbac-109">EXAMPLES</span></span>

### <span data-ttu-id="fcbac-110">예제 1: Gen1 시계열 insights 환경 만들기</span><span class="sxs-lookup"><span data-stu-id="fcbac-110">Example 1: Create a Gen1 time series insights environment</span></span>
```powershell
PS C:\> $TimeSpan = New-TimeSpan -Days 1 -Hours 1 -Minutes 25
PS C:\> New-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsitest001 -Kind Gen1 -Location eastus -Sku S1 -DataRetentionTime $TimeSpan -Capacity 2

Kind     Location Name       SkuCapacity SkuName Type
----     -------- ----       ----------- ------- ----
Gen1 eastus   tsitest001 2           S1      Microsoft.TimeSeriesInsights/Environments
```

<span data-ttu-id="fcbac-111">이 명령은 Gen1 시계열 insights 환경을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fcbac-111">This command creates a Gen1 time series insights environment.</span></span>

### <span data-ttu-id="fcbac-112">예제 2: Gen2 시계열 insights 환경 만들기</span><span class="sxs-lookup"><span data-stu-id="fcbac-112">Example 2: Create a Gen2 time series insights environment</span></span>
```powershell
PS C:\> $ks = Get-AzStorageAccountKey -ResourceGroupName "testgroup" -Name "staccount001"
PS C:\> $k  = $ks[0].Value | ConvertTo-SecureString -AsPlainText -Force
PS C:\> New-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsitest002 -Kind Gen2 -Location eastus -Sku L1 -StorageAccountName staccount001 -StorageAccountKey $k -TimeSeriesIdProperty @{name='cdc';type='string'}

Kind     Location Name       SkuCapacity SkuName Type
----     -------- ----       ----------- ------- ----
Gen2 eastus   tsitest002 1           L1      Microsoft.TimeSeriesInsights/Environments
```

<span data-ttu-id="fcbac-113">이 명령은 Gen2 시계열 insights 환경을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fcbac-113">This command creates a Gen2 time series insights environment.</span></span>

## <span data-ttu-id="fcbac-114">변수</span><span class="sxs-lookup"><span data-stu-id="fcbac-114">PARAMETERS</span></span>

### <span data-ttu-id="fcbac-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fcbac-115">-AsJob</span></span>
<span data-ttu-id="fcbac-116">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="fcbac-116">Run the command as a job</span></span>

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

### <span data-ttu-id="fcbac-117">용량</span><span class="sxs-lookup"><span data-stu-id="fcbac-117">-Capacity</span></span>
<span data-ttu-id="fcbac-118">Sku의 용량.</span><span class="sxs-lookup"><span data-stu-id="fcbac-118">The capacity of the sku.</span></span>
<span data-ttu-id="fcbac-119">Gen1 환경의 경우이 값을 만든 후 환경에서 확장을 지원 하도록 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fcbac-119">For Gen1 environments, this value can be changed to support scale out of environments after they have been created.</span></span>

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

### <span data-ttu-id="fcbac-120">-Data보존 기능 Ontime</span><span class="sxs-lookup"><span data-stu-id="fcbac-120">-DataRetentionTime</span></span>
<span data-ttu-id="fcbac-121">데이터 보존 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="fcbac-121">The data retention time.</span></span>

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

### <span data-ttu-id="fcbac-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcbac-122">-DefaultProfile</span></span>
<span data-ttu-id="fcbac-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fcbac-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fcbac-124">-종류</span><span class="sxs-lookup"><span data-stu-id="fcbac-124">-Kind</span></span>
<span data-ttu-id="fcbac-125">환경의 종류입니다.</span><span class="sxs-lookup"><span data-stu-id="fcbac-125">The kind of the environment.</span></span>

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

### <span data-ttu-id="fcbac-126">-위치</span><span class="sxs-lookup"><span data-stu-id="fcbac-126">-Location</span></span>
<span data-ttu-id="fcbac-127">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="fcbac-127">The location of the resource.</span></span>

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

### <span data-ttu-id="fcbac-128">-이름</span><span class="sxs-lookup"><span data-stu-id="fcbac-128">-Name</span></span>
<span data-ttu-id="fcbac-129">환경의 이름</span><span class="sxs-lookup"><span data-stu-id="fcbac-129">Name of the environment</span></span>

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

### <span data-ttu-id="fcbac-130">-NoWait</span><span class="sxs-lookup"><span data-stu-id="fcbac-130">-NoWait</span></span>
<span data-ttu-id="fcbac-131">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="fcbac-131">Run the command asynchronously</span></span>

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

### <span data-ttu-id="fcbac-132">-파티션 속성</span><span class="sxs-lookup"><span data-stu-id="fcbac-132">-PartitionKeyProperty</span></span>
<span data-ttu-id="fcbac-133">환경에서 데이터를 분할 하는 데 사용 되는 이벤트 속성 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="fcbac-133">The list of event properties which will be used to partition data in the environment.</span></span>
<span data-ttu-id="fcbac-134">생성을 하려면 파티션 섹션의 속성 속성 및 해시 테이블 만들기에 대 한 참고 사항을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="fcbac-134">To construct, see NOTES section for PARTITIONKEYPROPERTY properties and create a hash table.</span></span>

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

### <span data-ttu-id="fcbac-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fcbac-135">-ResourceGroupName</span></span>
<span data-ttu-id="fcbac-136">Azure 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fcbac-136">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="fcbac-137">-Sku</span><span class="sxs-lookup"><span data-stu-id="fcbac-137">-Sku</span></span>
<span data-ttu-id="fcbac-138">이 SKU의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fcbac-138">The name of this SKU.</span></span>

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

### <span data-ttu-id="fcbac-139">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="fcbac-139">-StorageAccountKey</span></span>
<span data-ttu-id="fcbac-140">저장소 계정에 대 한 시계열 Insights 서비스 쓰기 액세스 권한을 부여 하는 관리 키의 값입니다.</span><span class="sxs-lookup"><span data-stu-id="fcbac-140">The value of the management key that grants the Time Series Insights service write access to the storage account.</span></span>

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

### <span data-ttu-id="fcbac-141">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="fcbac-141">-StorageAccountName</span></span>
<span data-ttu-id="fcbac-142">환경의 장기 데이터를 보관할 저장소 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fcbac-142">The name of the storage account that will hold the environment's long term data.</span></span>

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

### <span data-ttu-id="fcbac-143">-StorageLimitExceededBehavior</span><span class="sxs-lookup"><span data-stu-id="fcbac-143">-StorageLimitExceededBehavior</span></span>
<span data-ttu-id="fcbac-144">환경의 용량을 초과한 경우 시계열 Insights 서비스에서 수행 해야 하는 동작입니다.</span><span class="sxs-lookup"><span data-stu-id="fcbac-144">The behavior the Time Series Insights service should take when the environment's capacity has been exceeded</span></span>

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

### <span data-ttu-id="fcbac-145">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fcbac-145">-SubscriptionId</span></span>
<span data-ttu-id="fcbac-146">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="fcbac-146">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="fcbac-147">태그</span><span class="sxs-lookup"><span data-stu-id="fcbac-147">-Tag</span></span>
<span data-ttu-id="fcbac-148">리소스에 대 한 추가 속성의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="fcbac-148">Key-value pairs of additional properties for the resource.</span></span>

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

### <span data-ttu-id="fcbac-149">-Timesa Esidproperty</span><span class="sxs-lookup"><span data-stu-id="fcbac-149">-TimeSeriesIdProperty</span></span>
<span data-ttu-id="fcbac-150">환경의 시계열 id를 정의 하는 데 사용 되는 이벤트 속성 목록입니다. 생성 하려면 TIMESERIESIDPROPERTY 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fcbac-150">The list of event properties which will be used to define the environment's time series id. To construct, see NOTES section for TIMESERIESIDPROPERTY properties and create a hash table.</span></span>

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

### <span data-ttu-id="fcbac-151">-WarmStoreDataRetentionTime</span><span class="sxs-lookup"><span data-stu-id="fcbac-151">-WarmStoreDataRetentionTime</span></span>
<span data-ttu-id="fcbac-152">ISO8601 시간 (일)을 지정 합니다. 웜 저장소의 쿼리에 해당 환경의 이벤트를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fcbac-152">ISO8601 timespan specifying the number of days the environment's events will be available for query from the warm store.</span></span>

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

### <span data-ttu-id="fcbac-153">-확인</span><span class="sxs-lookup"><span data-stu-id="fcbac-153">-Confirm</span></span>
<span data-ttu-id="fcbac-154">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcbac-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fcbac-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fcbac-155">-WhatIf</span></span>
<span data-ttu-id="fcbac-156">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="fcbac-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fcbac-157">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fcbac-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fcbac-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcbac-158">CommonParameters</span></span>
<span data-ttu-id="fcbac-159">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcbac-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcbac-160">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="fcbac-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcbac-161">입력</span><span class="sxs-lookup"><span data-stu-id="fcbac-161">INPUTS</span></span>

## <span data-ttu-id="fcbac-162">출력</span><span class="sxs-lookup"><span data-stu-id="fcbac-162">OUTPUTS</span></span>

### <span data-ttu-id="fcbac-163">Api20200515. a PowerShell. a i i. a i m.</span><span class="sxs-lookup"><span data-stu-id="fcbac-163">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEnvironmentResource</span></span>

## <span data-ttu-id="fcbac-164">상속자</span><span class="sxs-lookup"><span data-stu-id="fcbac-164">NOTES</span></span>

<span data-ttu-id="fcbac-165">별칭과</span><span class="sxs-lookup"><span data-stu-id="fcbac-165">ALIASES</span></span>

<span data-ttu-id="fcbac-166">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="fcbac-166">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="fcbac-167">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcbac-167">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="fcbac-168">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="fcbac-168">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="fcbac-169">Partition KEYPROPERTY <Itimes메이 Esidproperty [] >: 환경에서 데이터를 분할 하는 데 사용 되는 이벤트 속성 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="fcbac-169">PARTITIONKEYPROPERTY <ITimeSeriesIdProperty[]>: The list of event properties which will be used to partition data in the environment.</span></span>
  - <span data-ttu-id="fcbac-170">`[Name <String>]`: 속성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fcbac-170">`[Name <String>]`: The name of the property.</span></span>
  - <span data-ttu-id="fcbac-171">`[Type <PropertyType?>]`: 속성의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="fcbac-171">`[Type <PropertyType?>]`: The type of the property.</span></span>

<span data-ttu-id="fcbac-172">TIMES<Esidesidproperty [] >: 환경의 시계열 id를 정의 하는 데 사용 되는 이벤트 속성 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="fcbac-172">TIMESERIESIDPROPERTY <ITimeSeriesIdProperty[]>: The list of event properties which will be used to define the environment's time series id.</span></span>
  - <span data-ttu-id="fcbac-173">`[Name <String>]`: 속성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fcbac-173">`[Name <String>]`: The name of the property.</span></span>
  - <span data-ttu-id="fcbac-174">`[Type <PropertyType?>]`: 속성의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="fcbac-174">`[Type <PropertyType?>]`: The type of the property.</span></span>

## <span data-ttu-id="fcbac-175">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fcbac-175">RELATED LINKS</span></span>

