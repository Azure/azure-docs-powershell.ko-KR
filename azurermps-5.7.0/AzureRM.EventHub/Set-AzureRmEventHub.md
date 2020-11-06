---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/set-azurermeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHub.md
ms.openlocfilehash: 4de16b04151daa1c3e64dc6ea93b171c38fdb96a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530530"
---
# <span data-ttu-id="03ba9-101">Set-AzureRmEventHub</span><span class="sxs-lookup"><span data-stu-id="03ba9-101">Set-AzureRmEventHub</span></span>

## <span data-ttu-id="03ba9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03ba9-102">SYNOPSIS</span></span>
<span data-ttu-id="03ba9-103">지정 된 이벤트 허브를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="03ba9-103">Updates the specified Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="03ba9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="03ba9-104">SYNTAX</span></span>

### <span data-ttu-id="03ba9-105">EventhubInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="03ba9-105">EventhubInputObjectSet</span></span>
```
Set-AzureRmEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSEventHubAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="03ba9-106">EventhubPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="03ba9-106">EventhubPropertiesSet</span></span>
```
Set-AzureRmEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-messageRetentionInDays <Int64>] [-partitionCount <Int64>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03ba9-107">설명은</span><span class="sxs-lookup"><span data-stu-id="03ba9-107">DESCRIPTION</span></span>
<span data-ttu-id="03ba9-108">Set-AzureRmEventHub cmdlet은 지정 된 이벤트 허브의 속성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="03ba9-108">The Set-AzureRmEventHub cmdlet updates the properties of the specified Event Hub.</span></span>

## <span data-ttu-id="03ba9-109">예제의</span><span class="sxs-lookup"><span data-stu-id="03ba9-109">EXAMPLES</span></span>

### <span data-ttu-id="03ba9-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="03ba9-110">Example 1</span></span>
<span data-ttu-id="03ba9-111">캡처 설명 속성을 사용 하 여 Eventhub를 업데이트 하려면 아래 단계를 수행 하세요.</span><span class="sxs-lookup"><span data-stu-id="03ba9-111">To update Eventhub with Capture description properties, please follow the below steps.</span></span> 



```
PS C:\> $CreatedEventHub = Get-AzureRmEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName
PS C:\> $createdEventHub.CaptureDescription = New-Object -TypeName Microsoft.Azure.Commands.EventHub.Models.PSCaptureDescriptionAttributes
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

<span data-ttu-id="03ba9-112">\` \` MyCreatedEventHub 개체가 나타내는 이벤트 허브 MyEventHubName를 업데이트 \` 하 고 \` , 메시지 보존 기간을 4 일로 설정 하 고, 파티션 수를 2로, CaptureDescription 속성을</span><span class="sxs-lookup"><span data-stu-id="03ba9-112">Updates the Event Hub \`MyEventHubName\` represented by the \`MyCreatedEventHub\` object, setting the message retention period to 4 days, the number of partitions to 2 and CaptureDescription properties</span></span>

### <span data-ttu-id="03ba9-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="03ba9-113">Example 2</span></span>
```
PS C:\> Set-AzureRmEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName -InputObject MyCreatedEventHub -messageRetentionInDays 4 -partitionCount 2
```

<span data-ttu-id="03ba9-114">MyCreatedEventHub 개체로 표시 되는 이벤트 허브 \` MyEventHubName \` 를 업데이트 하 고 \` \` , 메시지 보존 기간을 4 일로, 파티션 수를 2로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="03ba9-114">Updates the Event Hub \`MyEventHubName\` represented by the \`MyCreatedEventHub\` object, setting the message retention period to 4 days, and the number of partitions to 2.</span></span>

## <span data-ttu-id="03ba9-115">변수</span><span class="sxs-lookup"><span data-stu-id="03ba9-115">PARAMETERS</span></span>

### <span data-ttu-id="03ba9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03ba9-116">-DefaultProfile</span></span>
<span data-ttu-id="03ba9-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="03ba9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03ba9-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="03ba9-118">-InputObject</span></span>
<span data-ttu-id="03ba9-119">EventHub 개체</span><span class="sxs-lookup"><span data-stu-id="03ba9-119">EventHub object</span></span>

```yaml
Type: PSEventHubAttributes
Parameter Sets: EventhubInputObjectSet
Aliases: EventHubObj

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03ba9-120">-messageRetentionInDays</span><span class="sxs-lookup"><span data-stu-id="03ba9-120">-messageRetentionInDays</span></span>
<span data-ttu-id="03ba9-121">Eventhub 메시지 보존 기간 (일)</span><span class="sxs-lookup"><span data-stu-id="03ba9-121">Eventhub Message Retention In Days</span></span>

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

### <span data-ttu-id="03ba9-122">-이름</span><span class="sxs-lookup"><span data-stu-id="03ba9-122">-Name</span></span>
<span data-ttu-id="03ba9-123">네임 스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="03ba9-123">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03ba9-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="03ba9-124">-Namespace</span></span>
<span data-ttu-id="03ba9-125">네임 스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="03ba9-125">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03ba9-126">-파티션 수</span><span class="sxs-lookup"><span data-stu-id="03ba9-126">-partitionCount</span></span>
<span data-ttu-id="03ba9-127">Eventhub/Count</span><span class="sxs-lookup"><span data-stu-id="03ba9-127">Eventhub PartitionCount</span></span>

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

### <span data-ttu-id="03ba9-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03ba9-128">-ResourceGroupName</span></span>
<span data-ttu-id="03ba9-129">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="03ba9-129">Resource Group Name</span></span>

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

### <span data-ttu-id="03ba9-130">-확인</span><span class="sxs-lookup"><span data-stu-id="03ba9-130">-Confirm</span></span>
<span data-ttu-id="03ba9-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="03ba9-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03ba9-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03ba9-132">-WhatIf</span></span>
<span data-ttu-id="03ba9-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="03ba9-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03ba9-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="03ba9-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03ba9-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03ba9-135">CommonParameters</span></span>
<span data-ttu-id="03ba9-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="03ba9-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="03ba9-137">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03ba9-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03ba9-138">입력</span><span class="sxs-lookup"><span data-stu-id="03ba9-138">INPUTS</span></span>

### <span data-ttu-id="03ba9-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="03ba9-139">System.String</span></span>
<span data-ttu-id="03ba9-140">PSEventHubAttributes System. Null 허용 ' 1 [[System.webserver, mscorlib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="03ba9-140">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes System.Nullable\`1[[System.Int64, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>


## <span data-ttu-id="03ba9-141">출력</span><span class="sxs-lookup"><span data-stu-id="03ba9-141">OUTPUTS</span></span>

### <span data-ttu-id="03ba9-142">PSEventHubAttributes (.).</span><span class="sxs-lookup"><span data-stu-id="03ba9-142">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>


## <span data-ttu-id="03ba9-143">상속자</span><span class="sxs-lookup"><span data-stu-id="03ba9-143">NOTES</span></span>

## <span data-ttu-id="03ba9-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="03ba9-144">RELATED LINKS</span></span>
