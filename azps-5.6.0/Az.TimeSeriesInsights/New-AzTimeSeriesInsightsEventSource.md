---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/powershell/module/az.timeseriesinsights/new-aztimeseriesinsightseventsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsEventSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsEventSource.md
ms.openlocfilehash: fa2573a774df86ee96563e90b617db43aed0b1c3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995843"
---
# <span data-ttu-id="ab60d-101">New-AzTimeSeriesInsightsEventSource</span><span class="sxs-lookup"><span data-stu-id="ab60d-101">New-AzTimeSeriesInsightsEventSource</span></span>

## <span data-ttu-id="ab60d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab60d-102">SYNOPSIS</span></span>
<span data-ttu-id="ab60d-103">지정된 환경 아래에서 이벤트 원본을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="ab60d-103">Create an event source under the specified environment.</span></span>

## <span data-ttu-id="ab60d-104">구문</span><span class="sxs-lookup"><span data-stu-id="ab60d-104">SYNTAX</span></span>

### <span data-ttu-id="ab60d-105">eventhub(기본값)</span><span class="sxs-lookup"><span data-stu-id="ab60d-105">eventhub (Default)</span></span>
```
New-AzTimeSeriesInsightsEventSource -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 -ConsumerGroupName <String> -EventHubName <String> -EventSourceResourceId <String> -KeyName <String>
 -Kind <Kind> -Location <String> -ServiceBusNameSpace <String> -SharedAccessKey <SecureString>
 [-SubscriptionId <String>] [-Tag <Hashtable>] [-TimeStampPropertyName <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ab60d-106">iothub</span><span class="sxs-lookup"><span data-stu-id="ab60d-106">iothub</span></span>
```
New-AzTimeSeriesInsightsEventSource -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 -ConsumerGroupName <String> -EventSourceResourceId <String> -IoTHubName <String> -KeyName <String>
 -Kind <Kind> -Location <String> -SharedAccessKey <SecureString> [-SubscriptionId <String>] [-Tag <Hashtable>]
 [-TimeStampPropertyName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ab60d-107">설명</span><span class="sxs-lookup"><span data-stu-id="ab60d-107">DESCRIPTION</span></span>
<span data-ttu-id="ab60d-108">지정된 환경 아래에서 이벤트 원본을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="ab60d-108">Create an event source under the specified environment.</span></span>

## <span data-ttu-id="ab60d-109">예제</span><span class="sxs-lookup"><span data-stu-id="ab60d-109">EXAMPLES</span></span>

### <span data-ttu-id="ab60d-110">예제 1: 지정된 환경 아래에서 eventhub 이벤트 원본 만들기</span><span class="sxs-lookup"><span data-stu-id="ab60d-110">Example 1: Create an eventhub event source under the specified environment</span></span>
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

<span data-ttu-id="ab60d-111">이 명령은 지정된 환경 아래에 eventhub 이벤트 원본을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ab60d-111">This command creates an eventhub event source under the specified environment.</span></span>

### <span data-ttu-id="ab60d-112">예제 2: 지정된 환경 아래에서 iothub 이벤트 원본 만들기</span><span class="sxs-lookup"><span data-stu-id="ab60d-112">Example 2: Create an iothub event source under the specified environment</span></span>
```powershell
PS C:\> $ev = New-AzIotHub -ResourceGroupName testgroup -Location eastus -Name iotname001 -SkuName S1 -Units 100
PS C:\> $ks = Get-AzIotHubKey -ResourceGroupName testgroup -Name iotname001
PS C:\> $k  = $ks[0].PrimaryKey | ConvertTo-SecureString -AsPlainText -Force
PS C:\> New-AzTimeSeriesInsightsEventSource -ResourceGroupName testgroup -Name iots001 -EnvironmentName tsitest001 -Kind Microsoft.IoTHub -ConsumerGroupName testgroup -Location eastus -KeyName RootManageSharedAccessKey -IoTHubName iotname001 -EventSourceResourceId $ev.id -SharedAccessKey $k

Location Name    Type                                                   Kind
-------- ----    ----                                                   ----
eastus   iots001 Microsoft.TimeSeriesInsights/Environments/EventSources Microsoft.IoTHub
```

<span data-ttu-id="ab60d-113">이 명령은 지정된 환경 아래에 iothub 이벤트 원본을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ab60d-113">This command creates an iothub event source under the specified environment.</span></span>

## <span data-ttu-id="ab60d-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="ab60d-114">PARAMETERS</span></span>

### <span data-ttu-id="ab60d-115">-ConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="ab60d-115">-ConsumerGroupName</span></span>
<span data-ttu-id="ab60d-116">이벤트가 읽을 파티션을 보유하는 event/iot Hub의 소비자 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ab60d-116">The name of the event/iot hub's consumer group that holds the partitions from which events will be read.</span></span>

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

### <span data-ttu-id="ab60d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab60d-117">-DefaultProfile</span></span>
<span data-ttu-id="ab60d-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ab60d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab60d-119">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="ab60d-119">-EnvironmentName</span></span>
<span data-ttu-id="ab60d-120">지정된 리소스 그룹과 연결된 Time Series Insights 환경의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ab60d-120">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="ab60d-121">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="ab60d-121">-EventHubName</span></span>
<span data-ttu-id="ab60d-122">이벤트 허브의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ab60d-122">The name of the event hub.</span></span>

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

### <span data-ttu-id="ab60d-123">-EventSourceResourceId</span><span class="sxs-lookup"><span data-stu-id="ab60d-123">-EventSourceResourceId</span></span>
<span data-ttu-id="ab60d-124">Azure Resource Manager의 이벤트 원본의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="ab60d-124">The resource id of the event source in Azure Resource Manager.</span></span>

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

### <span data-ttu-id="ab60d-125">-IoTHubName</span><span class="sxs-lookup"><span data-stu-id="ab60d-125">-IoTHubName</span></span>
<span data-ttu-id="ab60d-126">iot Hub의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ab60d-126">The name of the iot hub.</span></span>

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

### <span data-ttu-id="ab60d-127">-KeyName</span><span class="sxs-lookup"><span data-stu-id="ab60d-127">-KeyName</span></span>
<span data-ttu-id="ab60d-128">Event/iot Hub에 대한 Time Series Insights 서비스 액세스 권한을 부여하는 SAS 키의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ab60d-128">The name of the SAS key that grants the Time Series Insights service access to the event/iot hub.</span></span>

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

### <span data-ttu-id="ab60d-129">-Kind</span><span class="sxs-lookup"><span data-stu-id="ab60d-129">-Kind</span></span>
<span data-ttu-id="ab60d-130">이벤트 원본의 종류입니다.</span><span class="sxs-lookup"><span data-stu-id="ab60d-130">The kind of the event source.</span></span>

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

### <span data-ttu-id="ab60d-131">-Location</span><span class="sxs-lookup"><span data-stu-id="ab60d-131">-Location</span></span>
<span data-ttu-id="ab60d-132">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="ab60d-132">The location of the resource.</span></span>

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

### <span data-ttu-id="ab60d-133">-Name</span><span class="sxs-lookup"><span data-stu-id="ab60d-133">-Name</span></span>
<span data-ttu-id="ab60d-134">이벤트 원본의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ab60d-134">Name of the event source.</span></span>

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

### <span data-ttu-id="ab60d-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab60d-135">-ResourceGroupName</span></span>
<span data-ttu-id="ab60d-136">Azure 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ab60d-136">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="ab60d-137">-ServiceBusNameSpace</span><span class="sxs-lookup"><span data-stu-id="ab60d-137">-ServiceBusNameSpace</span></span>
<span data-ttu-id="ab60d-138">이벤트 허브를 포함하는 서비스 버스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ab60d-138">The name of the service bus that contains the event hub.</span></span>

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

### <span data-ttu-id="ab60d-139">-SharedAccessKey</span><span class="sxs-lookup"><span data-stu-id="ab60d-139">-SharedAccessKey</span></span>
<span data-ttu-id="ab60d-140">Time Series Insights 서비스가 이벤트/iot 허브에 대한 액세스 권한을 부여하는 공유 액세스 키의 값입니다.</span><span class="sxs-lookup"><span data-stu-id="ab60d-140">The value of the shared access key that grants the Time Series Insights service read access to the event/iot hub.</span></span>

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

### <span data-ttu-id="ab60d-141">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ab60d-141">-SubscriptionId</span></span>
<span data-ttu-id="ab60d-142">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="ab60d-142">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="ab60d-143">-Tag</span><span class="sxs-lookup"><span data-stu-id="ab60d-143">-Tag</span></span>
<span data-ttu-id="ab60d-144">리소스에 대한 추가 속성의 키 값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="ab60d-144">Key-value pairs of additional properties for the resource.</span></span>

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

### <span data-ttu-id="ab60d-145">-TimeStampPropertyName</span><span class="sxs-lookup"><span data-stu-id="ab60d-145">-TimeStampPropertyName</span></span>
<span data-ttu-id="ab60d-146">이벤트 원본의 타임스탬프로 사용되는 이벤트 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="ab60d-146">The event property that will be used as the event source's timestamp.</span></span>

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

### <span data-ttu-id="ab60d-147">-확인</span><span class="sxs-lookup"><span data-stu-id="ab60d-147">-Confirm</span></span>
<span data-ttu-id="ab60d-148">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ab60d-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab60d-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab60d-149">-WhatIf</span></span>
<span data-ttu-id="ab60d-150">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="ab60d-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab60d-151">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ab60d-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab60d-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab60d-152">CommonParameters</span></span>
<span data-ttu-id="ab60d-153">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ab60d-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab60d-154">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ab60d-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab60d-155">입력</span><span class="sxs-lookup"><span data-stu-id="ab60d-155">INPUTS</span></span>

## <span data-ttu-id="ab60d-156">출력</span><span class="sxs-lookup"><span data-stu-id="ab60d-156">OUTPUTS</span></span>

### <span data-ttu-id="ab60d-157">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEventSourceResource</span><span class="sxs-lookup"><span data-stu-id="ab60d-157">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEventSourceResource</span></span>

## <span data-ttu-id="ab60d-158">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ab60d-158">NOTES</span></span>

<span data-ttu-id="ab60d-159">별칭</span><span class="sxs-lookup"><span data-stu-id="ab60d-159">ALIASES</span></span>

## <span data-ttu-id="ab60d-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ab60d-160">RELATED LINKS</span></span>

