---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/powershell/module/az.digitaltwins/new-azdigitaltwinsendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsEndpoint.md
ms.openlocfilehash: 3c59099a2e4440e2c92836ab02b8396b5fc3b207
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984942"
---
# <span data-ttu-id="b4226-101">New-AzDigitalTwinsEndpoint</span><span class="sxs-lookup"><span data-stu-id="b4226-101">New-AzDigitalTwinsEndpoint</span></span>

## <span data-ttu-id="b4226-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4226-102">SYNOPSIS</span></span>
<span data-ttu-id="b4226-103">DigitalTwinsInstance 엔드포인트를 만들거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="b4226-103">Create or update DigitalTwinsInstance endpoint.</span></span>

## <span data-ttu-id="b4226-104">구문</span><span class="sxs-lookup"><span data-stu-id="b4226-104">SYNTAX</span></span>

### <span data-ttu-id="b4226-105">EventHub(기본값)</span><span class="sxs-lookup"><span data-stu-id="b4226-105">EventHub (Default)</span></span>
```
New-AzDigitalTwinsEndpoint -EndpointName <String> -ResourceGroupName <String> -ResourceName <String>
 -ConnectionStringPrimaryKey <String> -EndpointType <EndpointType> [-SubscriptionId <String>]
 [-ConnectionStringSecondaryKey <String>] [-DeadLetterSecret <String>]
 [-EndpointDescription <IDigitalTwinsEndpointResource>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b4226-106">EventGrid</span><span class="sxs-lookup"><span data-stu-id="b4226-106">EventGrid</span></span>
```
New-AzDigitalTwinsEndpoint -EndpointName <String> -ResourceGroupName <String> -ResourceName <String>
 -AccessKey1 <String> -EndpointType <EndpointType> -TopicEndpoint <String> [-SubscriptionId <String>]
 [-DeadLetterSecret <String>] [-EndpointDescription <IDigitalTwinsEndpointResource>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b4226-107">ServiceBus</span><span class="sxs-lookup"><span data-stu-id="b4226-107">ServiceBus</span></span>
```
New-AzDigitalTwinsEndpoint -EndpointName <String> -ResourceGroupName <String> -ResourceName <String>
 -EndpointType <EndpointType> -PrimaryConnectionString <String> [-SubscriptionId <String>]
 [-DeadLetterSecret <String>] [-EndpointDescription <IDigitalTwinsEndpointResource>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b4226-108">설명</span><span class="sxs-lookup"><span data-stu-id="b4226-108">DESCRIPTION</span></span>
<span data-ttu-id="b4226-109">DigitalTwinsInstance 엔드포인트를 만들거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="b4226-109">Create or update DigitalTwinsInstance endpoint.</span></span>

## <span data-ttu-id="b4226-110">예제</span><span class="sxs-lookup"><span data-stu-id="b4226-110">EXAMPLES</span></span>

### <span data-ttu-id="b4226-111">예제 1: Eventhub용 AzDigitalTwinsEndpoint 만들기</span><span class="sxs-lookup"><span data-stu-id="b4226-111">Example 1: Create an AzDigitalTwinsEndpoint for Eventhub</span></span>
```powershell
PS C:\> New-AzDigitalTwinsEndpoint -EndpointName youriEventHubEndPoint  -EndpointType EventHub -ResourceGroupName youritemp -ResourceName youriDigitalTwins -connectionStringPrimaryKey 'Endpoint=sb://yourieventhubnp.servicebus.windows.net/;SharedAccessKeyName=youriEventhubPolicy;SharedAccessKey=********;EntityPath=yourieventhub'

Name                  Type
----                  ----
youriEventHubEndPoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="b4226-112">connectionStringPrimaryKey를 사용하여 Eventhub용 AzDigitalTwinsEndpoint 만들기</span><span class="sxs-lookup"><span data-stu-id="b4226-112">Create an AzDigitalTwinsEndpoint for Eventhub by connectionStringPrimaryKey</span></span>

### <span data-ttu-id="b4226-113">예제 2: EventGrid에 대한 AzDigitalTwinsEndpoint 만들기</span><span class="sxs-lookup"><span data-stu-id="b4226-113">Example 2: Create an AzDigitalTwinsEndpoint for EventGrid</span></span>
```powershell
PS C:\> New-AzDigitalTwinsEndpoint -EndpointName youriEventGridPoint  -EndpointType EventGrid -ResourceGroupName youritemp -ResourceName youriDigitalTwins -TopicEndpoint 'https://yourieventgrid.eastus-1.eventgrid.azure.net/api/events' -AccessKey1 'xxxxxxxxx='

Name                  Type
----                  ----
youriEventGridPoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="b4226-114">TopicEndpoint 및 accessKey1에서 Eventhub용 AzDigitalTwinsEndpoint 만들기</span><span class="sxs-lookup"><span data-stu-id="b4226-114">Create an AzDigitalTwinsEndpoint for Eventhub by TopicEndpoint and accessKey1</span></span>

### <span data-ttu-id="b4226-115">예제 3: ServiceBus용 AzDigitalTwinsEndpoint 만들기</span><span class="sxs-lookup"><span data-stu-id="b4226-115">Example 3: Create an AzDigitalTwinsEndpoint for ServiceBus</span></span>
```powershell
PS C:\> New-AzDigitalTwinsEndpoint -EndpointName youriServiceBusPoint  -EndpointType EventGrid -ResourceGroupName youritemp -ResourceName youriDigitalTwins -PrimaryConnectionString "Endpoint=sb://yourieventhubnp.servicebus.windows.net/;SharedAccessKeyName=******;SharedAccessKey=********;EntityPath=yourieventhub"

Name                  Type
----                  ----
youriServiceBusPoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="b4226-116">PrimaryConnectionString에서 ServicBus용 AzDigitalTwinsEndpoint 만들기</span><span class="sxs-lookup"><span data-stu-id="b4226-116">Create an AzDigitalTwinsEndpoint for ServicBus by PrimaryConnectionString</span></span>

## <span data-ttu-id="b4226-117">매개 변수</span><span class="sxs-lookup"><span data-stu-id="b4226-117">PARAMETERS</span></span>

### <span data-ttu-id="b4226-118">-AccessKey1</span><span class="sxs-lookup"><span data-stu-id="b4226-118">-AccessKey1</span></span>
<span data-ttu-id="b4226-119">구독 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="b4226-119">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: EventGrid
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4226-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b4226-120">-AsJob</span></span>
<span data-ttu-id="b4226-121">작업으로 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="b4226-121">Run the command as a job</span></span>

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

### <span data-ttu-id="b4226-122">-ConnectionStringPrimaryKey</span><span class="sxs-lookup"><span data-stu-id="b4226-122">-ConnectionStringPrimaryKey</span></span>
<span data-ttu-id="b4226-123">구독 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="b4226-123">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: EventHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4226-124">-ConnectionStringSecondaryKey</span><span class="sxs-lookup"><span data-stu-id="b4226-124">-ConnectionStringSecondaryKey</span></span>
<span data-ttu-id="b4226-125">구독 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="b4226-125">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: EventHub
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4226-126">-DeadLetterSecret</span><span class="sxs-lookup"><span data-stu-id="b4226-126">-DeadLetterSecret</span></span>
<span data-ttu-id="b4226-127">Dead letter Storage 비밀입니다.</span><span class="sxs-lookup"><span data-stu-id="b4226-127">Dead letter storage secret.</span></span>
<span data-ttu-id="b4226-128">읽기 중에 난독화됩니다.</span><span class="sxs-lookup"><span data-stu-id="b4226-128">Will be obfuscated during read.</span></span>

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

### <span data-ttu-id="b4226-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4226-129">-DefaultProfile</span></span>
<span data-ttu-id="b4226-130">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b4226-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4226-131">-EndpointDescription</span><span class="sxs-lookup"><span data-stu-id="b4226-131">-EndpointDescription</span></span>
<span data-ttu-id="b4226-132">DigitalTwinsInstance 엔드포인트 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="b4226-132">DigitalTwinsInstance endpoint resource.</span></span>
<span data-ttu-id="b4226-133">생성을 위해 ENDPOINTDESCRIPTION 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="b4226-133">To construct, see NOTES section for ENDPOINTDESCRIPTION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b4226-134">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="b4226-134">-EndpointName</span></span>
<span data-ttu-id="b4226-135">엔드포인트 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b4226-135">Name of Endpoint Resource.</span></span>

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

### <span data-ttu-id="b4226-136">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="b4226-136">-EndpointType</span></span>
<span data-ttu-id="b4226-137">Digital Twins 엔드포인트 유형</span><span class="sxs-lookup"><span data-stu-id="b4226-137">The type of Digital Twins endpoint</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Support.EndpointType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4226-138">-NoWait</span><span class="sxs-lookup"><span data-stu-id="b4226-138">-NoWait</span></span>
<span data-ttu-id="b4226-139">명령 비동기 실행</span><span class="sxs-lookup"><span data-stu-id="b4226-139">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b4226-140">-PrimaryConnectionString</span><span class="sxs-lookup"><span data-stu-id="b4226-140">-PrimaryConnectionString</span></span>
<span data-ttu-id="b4226-141">구독 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="b4226-141">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceBus
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4226-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4226-142">-ResourceGroupName</span></span>
<span data-ttu-id="b4226-143">DigitalTwinsInstance를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b4226-143">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="b4226-144">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="b4226-144">-ResourceName</span></span>
<span data-ttu-id="b4226-145">DigitalTwinsInstance의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b4226-145">The name of the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="b4226-146">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b4226-146">-SubscriptionId</span></span>
<span data-ttu-id="b4226-147">구독 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="b4226-147">The subscription identifier.</span></span>

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

### <span data-ttu-id="b4226-148">-TopicEndpoint</span><span class="sxs-lookup"><span data-stu-id="b4226-148">-TopicEndpoint</span></span>
<span data-ttu-id="b4226-149">구독 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="b4226-149">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: EventGrid
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4226-150">-확인</span><span class="sxs-lookup"><span data-stu-id="b4226-150">-Confirm</span></span>
<span data-ttu-id="b4226-151">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b4226-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4226-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4226-152">-WhatIf</span></span>
<span data-ttu-id="b4226-153">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="b4226-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4226-154">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b4226-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4226-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4226-155">CommonParameters</span></span>
<span data-ttu-id="b4226-156">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b4226-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4226-157">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b4226-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4226-158">입력</span><span class="sxs-lookup"><span data-stu-id="b4226-158">INPUTS</span></span>

### <span data-ttu-id="b4226-159">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span><span class="sxs-lookup"><span data-stu-id="b4226-159">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span></span>

## <span data-ttu-id="b4226-160">출력</span><span class="sxs-lookup"><span data-stu-id="b4226-160">OUTPUTS</span></span>

### <span data-ttu-id="b4226-161">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span><span class="sxs-lookup"><span data-stu-id="b4226-161">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span></span>

## <span data-ttu-id="b4226-162">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b4226-162">NOTES</span></span>

<span data-ttu-id="b4226-163">별칭</span><span class="sxs-lookup"><span data-stu-id="b4226-163">ALIASES</span></span>

<span data-ttu-id="b4226-164">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="b4226-164">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b4226-165">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="b4226-165">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b4226-166">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b4226-166">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b4226-167">ENDPOINTDESCRIPTION <IDigitalTwinsEndpointResource> : DigitalTwinsInstance 엔드포인트 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="b4226-167">ENDPOINTDESCRIPTION <IDigitalTwinsEndpointResource>: DigitalTwinsInstance endpoint resource.</span></span>
  - <span data-ttu-id="b4226-168">`EndpointType <EndpointType>`: Digital Twins 엔드포인트 유형</span><span class="sxs-lookup"><span data-stu-id="b4226-168">`EndpointType <EndpointType>`: The type of Digital Twins endpoint</span></span>
  - <span data-ttu-id="b4226-169">`[DeadLetterSecret <String>]`: 데드 레터 저장소 비밀입니다.</span><span class="sxs-lookup"><span data-stu-id="b4226-169">`[DeadLetterSecret <String>]`: Dead letter storage secret.</span></span> <span data-ttu-id="b4226-170">읽기 중에 난독화됩니다.</span><span class="sxs-lookup"><span data-stu-id="b4226-170">Will be obfuscated during read.</span></span>

## <span data-ttu-id="b4226-171">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b4226-171">RELATED LINKS</span></span>

