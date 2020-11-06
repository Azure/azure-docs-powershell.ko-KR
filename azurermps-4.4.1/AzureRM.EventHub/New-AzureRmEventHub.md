---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHub.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 656e010a05ce1272355f689be8513ecadd330e7a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537251"
---
# <span data-ttu-id="67040-101">New-AzureRmEventHub</span><span class="sxs-lookup"><span data-stu-id="67040-101">New-AzureRmEventHub</span></span>

## <span data-ttu-id="67040-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67040-102">SYNOPSIS</span></span>
<span data-ttu-id="67040-103">새 이벤트 허브를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="67040-103">Creates a new Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="67040-104">구문과</span><span class="sxs-lookup"><span data-stu-id="67040-104">SYNTAX</span></span>

### <span data-ttu-id="67040-105">EventhubInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="67040-105">EventhubInputObjectSet</span></span>
```
New-AzureRmEventHub [-ResourceGroupName] <String> -Namespace <String> [[-Location] <String>] -Name <String>
 [-InputObject <EventHubAttributes>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="67040-106">EventhubPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="67040-106">EventhubPropertiesSet</span></span>
```
New-AzureRmEventHub [-ResourceGroupName] <String> -Namespace <String> [[-Location] <String>] -Name <String>
 [-MessageRetentionInDays <Int64>] [-PartitionCount <Int64>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="67040-107">설명은</span><span class="sxs-lookup"><span data-stu-id="67040-107">DESCRIPTION</span></span>
<span data-ttu-id="67040-108">New-AzureRmEventHub cmdlet은 새 Azure 이벤트 허브를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="67040-108">The New-AzureRmEventHub cmdlet creates a new Azure Event Hub.</span></span>
<span data-ttu-id="67040-109">캡처 설명 속성을 사용 하 여 Eventhub를 만들려면 다음 단계를 따르세요 (예 2).</span><span class="sxs-lookup"><span data-stu-id="67040-109">To create Eventhub with Capture description properties, please follow the below steps (Examples 2).</span></span> 


## <span data-ttu-id="67040-110">예제의</span><span class="sxs-lookup"><span data-stu-id="67040-110">EXAMPLES</span></span>

### <span data-ttu-id="67040-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="67040-111">Example 1</span></span>
```
PS C:\> New-AzureRmEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location WestUS -EventHubName MyEventHubName -MessageRetentionInDays 3 -PartitionCount 2
```

<span data-ttu-id="67040-112">\` \` 3 일 메시지 보존 기간과 두 개의 파티션과 \` WestUS \` 위치에서 리소스 그룹 MyResourceGroupName을 사용 하 여 MyEventHubName \` 라는 이벤트 허브를 만듭니다 \` .</span><span class="sxs-lookup"><span data-stu-id="67040-112">Creates an Event Hub named \`MyEventHubName\` with a 3-day message retention period and two partitions, in the \`WestUS\` location, with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="67040-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="67040-113">Example 2</span></span>
```
PS C:\> New-AzureRmEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location WestUS -EventHubName MyEventHubName -MessageRetentionInDays 3 -PartitionCount 2

PS C:\> $CreatedEventHub = Get-AzureRmEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName

PS C:\> $createdEventHub.CaptureDescription = New-Object -TypeName Microsoft.Azure.Commands.EventHub.Models.CaptureDescriptionAttributes

PS C:\> $createdEventHub.CaptureDescription.Enabled = $true
PS C:\> $createdEventHub.CaptureDescription.IntervalInSeconds  = 120
PS C:\> $createdEventHub.CaptureDescription.Encoding  = "Avro"
PS C:\> $createdEventHub.CaptureDescription.SizeLimitInBytes = 10485763
PS C:\> $createdEventHub.CaptureDescription.Destination.Name = "EventHubArchive.AzureBlockBlob"
PS C:\> $createdEventHub.CaptureDescription.Destination.BlobContainer = "container"
PS C:\> $createdEventHub.CaptureDescription.Destination.ArchiveNameFormat = "{Namespace}/{EventHub}/{PartitionId}/{Year}/{Month}/{Day}/{Hour}/{Minute}/{Second}"
PS C:\> $createdEventHub.CaptureDescription.Destination.StorageAccountResourceId = "/subscriptions/{SubscriptionId}/resourceGroups/MyResourceGroupName/providers/Microsoft.ClassicStorage/storageAccounts/arjunteststorage"
PS C:\> Set-AzureRmEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName -InputObject MyCreatedEventHub -messageRetentionInDays 4 -partitionCount 2
```

<span data-ttu-id="67040-114">\` \` 3 일 메시지 보존 기간, 2 개 파티션 및 CaptureDescription 속성을 사용 하 여 \` WestUS \` 위치에 리소스 그룹 MyResourceGroupName이 있는 \` MyEventHubName 라는 이벤트 허브를 만듭니다 \` .</span><span class="sxs-lookup"><span data-stu-id="67040-114">Creates an Event Hub named \`MyEventHubName\` with a 3-day message retention period, 2 partitions and CaptureDescription properties in the \`WestUS\` location, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="67040-115">변수</span><span class="sxs-lookup"><span data-stu-id="67040-115">PARAMETERS</span></span>

### <span data-ttu-id="67040-116">-위치</span><span class="sxs-lookup"><span data-stu-id="67040-116">-Location</span></span>
<span data-ttu-id="67040-117">네임 스페이스 지리적 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="67040-117">Namespace geographic location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67040-118">-MessageRetentionInDays</span><span class="sxs-lookup"><span data-stu-id="67040-118">-MessageRetentionInDays</span></span>
<span data-ttu-id="67040-119">이벤트 허브 메시지 보존 시간 (일).</span><span class="sxs-lookup"><span data-stu-id="67040-119">Event Hubs message retention time in days.</span></span>

```yaml
Type: Int64
Parameter Sets: EventhubPropertiesSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67040-120">-파티션 수</span><span class="sxs-lookup"><span data-stu-id="67040-120">-PartitionCount</span></span>
<span data-ttu-id="67040-121">이벤트 허브의 파티션 수입니다.</span><span class="sxs-lookup"><span data-stu-id="67040-121">Number of partitions in the Event Hub.</span></span>

```yaml
Type: Int64
Parameter Sets: EventhubPropertiesSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67040-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67040-122">-ResourceGroupName</span></span>
<span data-ttu-id="67040-123">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="67040-123">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67040-124">-확인</span><span class="sxs-lookup"><span data-stu-id="67040-124">-Confirm</span></span>
<span data-ttu-id="67040-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="67040-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67040-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67040-126">-WhatIf</span></span>
<span data-ttu-id="67040-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="67040-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67040-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="67040-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67040-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="67040-129">-InputObject</span></span>
<span data-ttu-id="67040-130">EventHub 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="67040-130">EventHub Input object.</span></span>

```yaml
Type: EventHubAttributes
Parameter Sets: EventhubInputObjectSet
Aliases: EventHubObj

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67040-131">-이름</span><span class="sxs-lookup"><span data-stu-id="67040-131">-Name</span></span>
<span data-ttu-id="67040-132">Eventhub 이름.</span><span class="sxs-lookup"><span data-stu-id="67040-132">Eventhub Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67040-133">-Namespace</span><span class="sxs-lookup"><span data-stu-id="67040-133">-Namespace</span></span>
<span data-ttu-id="67040-134">네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="67040-134">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="67040-135">입력</span><span class="sxs-lookup"><span data-stu-id="67040-135">INPUTS</span></span>

### <span data-ttu-id="67040-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="67040-136">System.String</span></span>

## <span data-ttu-id="67040-137">출력</span><span class="sxs-lookup"><span data-stu-id="67040-137">OUTPUTS</span></span>

### <span data-ttu-id="67040-138">EventHubAttributes (.).</span><span class="sxs-lookup"><span data-stu-id="67040-138">Microsoft.Azure.Commands.EventHub.Models.EventHubAttributes</span></span>

## <span data-ttu-id="67040-139">상속자</span><span class="sxs-lookup"><span data-stu-id="67040-139">NOTES</span></span>

## <span data-ttu-id="67040-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="67040-140">RELATED LINKS</span></span>

