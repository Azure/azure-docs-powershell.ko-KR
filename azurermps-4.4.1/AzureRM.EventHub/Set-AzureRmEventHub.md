---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHub.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 2ff36708ba9b8303c8b8763146c81ee4e4d8b209
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532275"
---
# <span data-ttu-id="9e453-101">Set-AzureRmEventHub</span><span class="sxs-lookup"><span data-stu-id="9e453-101">Set-AzureRmEventHub</span></span>

## <span data-ttu-id="9e453-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e453-102">SYNOPSIS</span></span>
<span data-ttu-id="9e453-103">지정 된 이벤트 허브를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e453-103">Updates the specified Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9e453-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9e453-104">SYNTAX</span></span>

### <span data-ttu-id="9e453-105">EventhubInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="9e453-105">EventhubInputObjectSet</span></span>
```
Set-AzureRmEventHub [-ResourceGroupName] <String> -Namespace <String> -Name <String>
 [-InputObject <EventHubAttributes>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="9e453-106">EventhubPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="9e453-106">EventhubPropertiesSet</span></span>
```
Set-AzureRmEventHub [-ResourceGroupName] <String> -Namespace <String> -Name <String>
 [-messageRetentionInDays <Int64>] [-partitionCount <Int64>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="9e453-107">설명은</span><span class="sxs-lookup"><span data-stu-id="9e453-107">DESCRIPTION</span></span>
<span data-ttu-id="9e453-108">Set-AzureRmEventHub cmdlet은 지정 된 이벤트 허브의 속성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e453-108">The Set-AzureRmEventHub cmdlet updates the properties of the specified Event Hub.</span></span>

## <span data-ttu-id="9e453-109">예제의</span><span class="sxs-lookup"><span data-stu-id="9e453-109">EXAMPLES</span></span>

### <span data-ttu-id="9e453-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="9e453-110">Example 1</span></span>
<span data-ttu-id="9e453-111">캡처 설명 속성을 사용 하 여 Eventhub를 업데이트 하려면 아래 단계를 수행 하세요.</span><span class="sxs-lookup"><span data-stu-id="9e453-111">To update Eventhub with Capture description properties, please follow the below steps.</span></span> 

```
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

<span data-ttu-id="9e453-112">\` \` MyCreatedEventHub 개체가 나타내는 이벤트 허브 MyEventHubName를 업데이트 \` 하 고 \` , 메시지 보존 기간을 4 일로 설정 하 고, 파티션 수를 2로, CaptureDescription 속성을</span><span class="sxs-lookup"><span data-stu-id="9e453-112">Updates the Event Hub \`MyEventHubName\` represented by the \`MyCreatedEventHub\` object, setting the message retention period to 4 days, the number of partitions to 2 and CaptureDescription properties</span></span>

### <span data-ttu-id="9e453-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="9e453-113">Example 2</span></span>

```
PS C:\> Set-AzureRmEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName -InputObject MyCreatedEventHub -messageRetentionInDays 4 -partitionCount 2
```

<span data-ttu-id="9e453-114">MyCreatedEventHub 개체로 표시 되는 이벤트 허브 \` MyEventHubName \` 를 업데이트 하 고 \` \` , 메시지 보존 기간을 4 일로, 파티션 수를 2로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e453-114">Updates the Event Hub \`MyEventHubName\` represented by the \`MyCreatedEventHub\` object, setting the message retention period to 4 days, and the number of partitions to 2.</span></span>

## <span data-ttu-id="9e453-115">변수</span><span class="sxs-lookup"><span data-stu-id="9e453-115">PARAMETERS</span></span>

### <span data-ttu-id="9e453-116">-messageRetentionInDays</span><span class="sxs-lookup"><span data-stu-id="9e453-116">-messageRetentionInDays</span></span>
<span data-ttu-id="9e453-117">이벤트 허브 메시지 보존 기간 (일)입니다.</span><span class="sxs-lookup"><span data-stu-id="9e453-117">Event Hub message retention period, in days.</span></span>

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

### <span data-ttu-id="9e453-118">-파티션 수</span><span class="sxs-lookup"><span data-stu-id="9e453-118">-partitionCount</span></span>
<span data-ttu-id="9e453-119">이 이벤트 허브의 파티션 수입니다.</span><span class="sxs-lookup"><span data-stu-id="9e453-119">Number of partitions on this Event Hub.</span></span>

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

### <span data-ttu-id="9e453-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e453-120">-ResourceGroupName</span></span>
<span data-ttu-id="9e453-121">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9e453-121">Resource group name.</span></span>

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

### <span data-ttu-id="9e453-122">-확인</span><span class="sxs-lookup"><span data-stu-id="9e453-122">-Confirm</span></span>
<span data-ttu-id="9e453-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e453-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e453-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e453-124">-WhatIf</span></span>
<span data-ttu-id="9e453-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9e453-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e453-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9e453-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e453-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9e453-127">-InputObject</span></span>
<span data-ttu-id="9e453-128">EventHub 개체</span><span class="sxs-lookup"><span data-stu-id="9e453-128">EventHub object.</span></span>

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

### <span data-ttu-id="9e453-129">-이름</span><span class="sxs-lookup"><span data-stu-id="9e453-129">-Name</span></span>
<span data-ttu-id="9e453-130">네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9e453-130">Namespace Name.</span></span>

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

### <span data-ttu-id="9e453-131">-Namespace</span><span class="sxs-lookup"><span data-stu-id="9e453-131">-Namespace</span></span>
<span data-ttu-id="9e453-132">네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9e453-132">Namespace Name.</span></span>

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

## <span data-ttu-id="9e453-133">입력</span><span class="sxs-lookup"><span data-stu-id="9e453-133">INPUTS</span></span>

### <span data-ttu-id="9e453-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9e453-134">System.String</span></span>

## <span data-ttu-id="9e453-135">출력</span><span class="sxs-lookup"><span data-stu-id="9e453-135">OUTPUTS</span></span>

### <span data-ttu-id="9e453-136">EventHubAttributes (.).</span><span class="sxs-lookup"><span data-stu-id="9e453-136">Microsoft.Azure.Commands.EventHub.Models.EventHubAttributes</span></span>

## <span data-ttu-id="9e453-137">상속자</span><span class="sxs-lookup"><span data-stu-id="9e453-137">NOTES</span></span>

## <span data-ttu-id="9e453-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9e453-138">RELATED LINKS</span></span>

