---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/new-aztimeseriesinsightseventsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsEventSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsEventSource.md
ms.openlocfilehash: 1c5e14fa71ded51d91792f462d01cb463ff36c61
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226459"
---
# <span data-ttu-id="e5db3-101">New-AzTimeSeriesInsightsEventSource</span><span class="sxs-lookup"><span data-stu-id="e5db3-101">New-AzTimeSeriesInsightsEventSource</span></span>

## <span data-ttu-id="e5db3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5db3-102">SYNOPSIS</span></span>
<span data-ttu-id="e5db3-103">지정 된 환경에서 이벤트 원본을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e5db3-103">Create an event source under the specified environment.</span></span>

## <span data-ttu-id="e5db3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e5db3-104">SYNTAX</span></span>

### <span data-ttu-id="e5db3-105">eventhub (기본값)</span><span class="sxs-lookup"><span data-stu-id="e5db3-105">eventhub (Default)</span></span>
```
New-AzTimeSeriesInsightsEventSource -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 -ConsumerGroupName <String> -EventHubName <String> -EventSourceResourceId <String> -KeyName <String>
 -Kind <Kind> -Location <String> -ServiceBusNameSpace <String> -SharedAccessKey <SecureString>
 [-SubscriptionId <String>] [-Tag <Hashtable>] [-TimeStampPropertyName <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e5db3-106">iothub</span><span class="sxs-lookup"><span data-stu-id="e5db3-106">iothub</span></span>
```
New-AzTimeSeriesInsightsEventSource -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 -ConsumerGroupName <String> -EventSourceResourceId <String> -IoTHubName <String> -KeyName <String>
 -Kind <Kind> -Location <String> -SharedAccessKey <SecureString> [-SubscriptionId <String>] [-Tag <Hashtable>]
 [-TimeStampPropertyName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e5db3-107">설명은</span><span class="sxs-lookup"><span data-stu-id="e5db3-107">DESCRIPTION</span></span>
<span data-ttu-id="e5db3-108">지정 된 환경에서 이벤트 원본을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e5db3-108">Create an event source under the specified environment.</span></span>

## <span data-ttu-id="e5db3-109">예제의</span><span class="sxs-lookup"><span data-stu-id="e5db3-109">EXAMPLES</span></span>

### <span data-ttu-id="e5db3-110">예제 1: 지정 된 환경에서 eventhub 이벤트 원본 만들기</span><span class="sxs-lookup"><span data-stu-id="e5db3-110">Example 1: Create an eventhub event source under the specified environment</span></span>
```powershell
PS C:\> New-AzEventHubNamespace -Name spacename002 -ResourceGroupName testgroup -Location eastus
PS C:\> $ev = New-AzEventHub -ResourceGroupName testgroup -NamespaceName spacename002 -Name hubname001 -MessageRetentionInDays 3 -PartitionCount 2
PS C:\> $ks = Get-AzEventHubKey -ResourceGroupName testgroup -NamespaceName spacename002 -AuthorizationRuleName RootManageSharedAccessKey
PS C:\> $k  = $ks.PrimaryKey | ConvertTo-SecureString -AsPlainText -Force
PS C:\> New-AzTimeSeriesInsightsEventSource -ResourceGroupName testgroup -Name estest001 -EnvironmentName tsitest001 -Kind Microsoft.EventHub -ConsumerGroupName testgroup -Location eastus -KeyName RootManageSharedAccessKey -ServiceBusNameSpace spacename002 -EventHubName hubname001 -EventSourceResourceId $ev.id -SharedAccessKey $k

Kind               Location Name      Type
----               -------- ----      ----
Microsoft.EventHub eastus   estest001 Microsoft.TimeSeriesInsights/Environments/EventSources
```

<span data-ttu-id="e5db3-111">이 명령은 지정 된 환경에서 eventhub 이벤트 원본을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e5db3-111">This command creates an eventhub event source under the specified environment.</span></span>

### <span data-ttu-id="e5db3-112">예제 2: 지정 된 환경에서 iothub 이벤트 원본 만들기</span><span class="sxs-lookup"><span data-stu-id="e5db3-112">Example 2: Create an iothub event source under the specified environment</span></span>
```powershell
PS C:\> $ev = New-AzIotHub -ResourceGroupName testgroup -Location eastus -Name iotname001 -SkuName S1 -Units 100
PS C:\> $ks = Get-AzIotHubKey -ResourceGroupName testgroup -Name iotname001
PS C:\> $k  = $ks[0].PrimaryKey | ConvertTo-SecureString -AsPlainText -Force
PS C:\> New-AzTimeSeriesInsightsEventSource -ResourceGroupName testgroup -Name iots001 -EnvironmentName tsitest001 -Kind Microsoft.IoTHub -ConsumerGroupName testgroup -Location eastus -KeyName RootManageSharedAccessKey -IoTHubName iotname001 -EventSourceResourceId $ev.id -SharedAccessKey $k

Location Name    Type                                                   Kind
-------- ----    ----                                                   ----
eastus   iots001 Microsoft.TimeSeriesInsights/Environments/EventSources Microsoft.IoTHub
```

<span data-ttu-id="e5db3-113">이 명령은 지정 된 환경에서 iothub 이벤트 원본을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e5db3-113">This command creates an iothub event source under the specified environment.</span></span>

## <span data-ttu-id="e5db3-114">변수</span><span class="sxs-lookup"><span data-stu-id="e5db3-114">PARAMETERS</span></span>

### <span data-ttu-id="e5db3-115">-ConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="e5db3-115">-ConsumerGroupName</span></span>
<span data-ttu-id="e5db3-116">이벤트를 읽을 파티션을 보유 하는 이벤트/iot hub 소비자 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e5db3-116">The name of the event/iot hub's consumer group that holds the partitions from which events will be read.</span></span>

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

### <span data-ttu-id="e5db3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5db3-117">-DefaultProfile</span></span>
<span data-ttu-id="e5db3-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e5db3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5db3-119">-환경 이름</span><span class="sxs-lookup"><span data-stu-id="e5db3-119">-EnvironmentName</span></span>
<span data-ttu-id="e5db3-120">지정 된 리소스 그룹과 연결 된 시계열 Insights 환경의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e5db3-120">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="e5db3-121">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="e5db3-121">-EventHubName</span></span>
<span data-ttu-id="e5db3-122">이벤트 허브의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e5db3-122">The name of the event hub.</span></span>

```yaml
Type: System.String
Parameter Sets: eventhub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5db3-123">-EventSourceResourceId</span><span class="sxs-lookup"><span data-stu-id="e5db3-123">-EventSourceResourceId</span></span>
<span data-ttu-id="e5db3-124">Azure 리소스 관리자의 이벤트 원본에 대 한 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="e5db3-124">The resource id of the event source in Azure Resource Manager.</span></span>

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

### <span data-ttu-id="e5db3-125">-IoTHubName</span><span class="sxs-lookup"><span data-stu-id="e5db3-125">-IoTHubName</span></span>
<span data-ttu-id="e5db3-126">Iot hub의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e5db3-126">The name of the iot hub.</span></span>

```yaml
Type: System.String
Parameter Sets: iothub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5db3-127">-KeyName</span><span class="sxs-lookup"><span data-stu-id="e5db3-127">-KeyName</span></span>
<span data-ttu-id="e5db3-128">이벤트/iot hub에 대 한 시계열 Insights 서비스 액세스를 허용 하는 SAS 키의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e5db3-128">The name of the SAS key that grants the Time Series Insights service access to the event/iot hub.</span></span>

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

### <span data-ttu-id="e5db3-129">-종류</span><span class="sxs-lookup"><span data-stu-id="e5db3-129">-Kind</span></span>
<span data-ttu-id="e5db3-130">이벤트 소스의 종류입니다.</span><span class="sxs-lookup"><span data-stu-id="e5db3-130">The kind of the event source.</span></span>

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

### <span data-ttu-id="e5db3-131">-위치</span><span class="sxs-lookup"><span data-stu-id="e5db3-131">-Location</span></span>
<span data-ttu-id="e5db3-132">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="e5db3-132">The location of the resource.</span></span>

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

### <span data-ttu-id="e5db3-133">-이름</span><span class="sxs-lookup"><span data-stu-id="e5db3-133">-Name</span></span>
<span data-ttu-id="e5db3-134">이벤트 원본의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e5db3-134">Name of the event source.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EventSourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5db3-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5db3-135">-ResourceGroupName</span></span>
<span data-ttu-id="e5db3-136">Azure 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e5db3-136">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="e5db3-137">-ServiceBusNameSpace</span><span class="sxs-lookup"><span data-stu-id="e5db3-137">-ServiceBusNameSpace</span></span>
<span data-ttu-id="e5db3-138">이벤트 허브가 포함 된 서비스 버스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e5db3-138">The name of the service bus that contains the event hub.</span></span>

```yaml
Type: System.String
Parameter Sets: eventhub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5db3-139">-SharedAccessKey</span><span class="sxs-lookup"><span data-stu-id="e5db3-139">-SharedAccessKey</span></span>
<span data-ttu-id="e5db3-140">이벤트/iot hub에 대 한 시계열 Insights 서비스 읽기 액세스 권한을 부여 하는 공유 액세스 키의 값입니다.</span><span class="sxs-lookup"><span data-stu-id="e5db3-140">The value of the shared access key that grants the Time Series Insights service read access to the event/iot hub.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5db3-141">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e5db3-141">-SubscriptionId</span></span>
<span data-ttu-id="e5db3-142">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="e5db3-142">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="e5db3-143">태그</span><span class="sxs-lookup"><span data-stu-id="e5db3-143">-Tag</span></span>
<span data-ttu-id="e5db3-144">리소스에 대 한 추가 속성의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="e5db3-144">Key-value pairs of additional properties for the resource.</span></span>

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

### <span data-ttu-id="e5db3-145">-TimeStampPropertyName</span><span class="sxs-lookup"><span data-stu-id="e5db3-145">-TimeStampPropertyName</span></span>
<span data-ttu-id="e5db3-146">이벤트 원본에 대 한 타임 스탬프로 사용 되는 이벤트 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="e5db3-146">The event property that will be used as the event source's timestamp.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5db3-147">-확인</span><span class="sxs-lookup"><span data-stu-id="e5db3-147">-Confirm</span></span>
<span data-ttu-id="e5db3-148">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5db3-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5db3-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5db3-149">-WhatIf</span></span>
<span data-ttu-id="e5db3-150">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e5db3-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5db3-151">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e5db3-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5db3-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5db3-152">CommonParameters</span></span>
<span data-ttu-id="e5db3-153">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5db3-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5db3-154">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e5db3-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5db3-155">입력</span><span class="sxs-lookup"><span data-stu-id="e5db3-155">INPUTS</span></span>

## <span data-ttu-id="e5db3-156">출력</span><span class="sxs-lookup"><span data-stu-id="e5db3-156">OUTPUTS</span></span>

### <span data-ttu-id="e5db3-157">Api20200515. IEventSourceResource에 대 한 정보를 모두 보세요.</span><span class="sxs-lookup"><span data-stu-id="e5db3-157">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEventSourceResource</span></span>

## <span data-ttu-id="e5db3-158">상속자</span><span class="sxs-lookup"><span data-stu-id="e5db3-158">NOTES</span></span>

<span data-ttu-id="e5db3-159">별칭과</span><span class="sxs-lookup"><span data-stu-id="e5db3-159">ALIASES</span></span>

## <span data-ttu-id="e5db3-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e5db3-160">RELATED LINKS</span></span>

