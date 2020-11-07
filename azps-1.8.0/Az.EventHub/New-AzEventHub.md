---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHub.md
ms.openlocfilehash: ac61b1f0bec6ea6b76fcc2b0ea4cf1438359197b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93700845"
---
# <span data-ttu-id="2c739-101">New-AzEventHub</span><span class="sxs-lookup"><span data-stu-id="2c739-101">New-AzEventHub</span></span>

## <span data-ttu-id="2c739-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c739-102">SYNOPSIS</span></span>
<span data-ttu-id="2c739-103">새 이벤트 허브를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2c739-103">Creates a new Event Hub.</span></span>

## <span data-ttu-id="2c739-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2c739-104">SYNTAX</span></span>

### <span data-ttu-id="2c739-105">EventhubPropertiesSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="2c739-105">EventhubPropertiesSet (Default)</span></span>
```
New-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-MessageRetentionInDays <Int64>] [-PartitionCount <Int64>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c739-106">EventhubInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="2c739-106">EventhubInputObjectSet</span></span>
```
New-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSEventHubAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2c739-107">설명은</span><span class="sxs-lookup"><span data-stu-id="2c739-107">DESCRIPTION</span></span>
<span data-ttu-id="2c739-108">New-AzEventHub cmdlet은 새 Azure 이벤트 허브를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2c739-108">The New-AzEventHub cmdlet creates a new Azure Event Hub.</span></span>
<span data-ttu-id="2c739-109">캡처 설명 속성을 사용 하 여 Eventhub를 만들려면 다음 단계를 따르세요 (예 2).</span><span class="sxs-lookup"><span data-stu-id="2c739-109">To create Eventhub with Capture description properties, please follow the below steps (Examples 2).</span></span> 

## <span data-ttu-id="2c739-110">예제의</span><span class="sxs-lookup"><span data-stu-id="2c739-110">EXAMPLES</span></span>

### <span data-ttu-id="2c739-111">예제 1-새 EventHub 만들기</span><span class="sxs-lookup"><span data-stu-id="2c739-111">Example 1  - Create new EventHub</span></span>
```
PS C:\> New-AzEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Name MyEventHubName
```

<span data-ttu-id="2c739-112">\` \` 3 일 메시지 보존 기간과 두 개의 파티션과 \` WestUS \` 위치에서 리소스 그룹 MyResourceGroupName을 사용 하 여 MyEventHubName \` 라는 이벤트 허브를 만듭니다 \` .</span><span class="sxs-lookup"><span data-stu-id="2c739-112">Creates an Event Hub named \`MyEventHubName\` with a 3-day message retention period and two partitions, in the \`WestUS\` location, with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="2c739-113">예제 2 ' CaptureDescription '으로 업데이트 Eventhub</span><span class="sxs-lookup"><span data-stu-id="2c739-113">Example 2 Update Eventhub with 'CaptureDescription'</span></span>
```
PS C:\> New-AzEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Name MyEventHubName -MessageRetentionInDays 3 -PartitionCount 2

PS C:\> $CreatedEventHub = Get-AzEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName

PS C:\> $createdEventHub.CaptureDescription = New-Object -TypeName Microsoft.Azure.Commands.EventHub.Models.CaptureDescriptionAttributes

PS C:\> $createdEventHub.CaptureDescription.Enabled = $true
PS C:\> $createdEventHub.CaptureDescription.IntervalInSeconds  = 120
PS C:\> $createdEventHub.CaptureDescription.Encoding  = "Avro"
PS C:\> $createdEventHub.CaptureDescription.SizeLimitInBytes = 10485763
PS C:\> $createdEventHub.CaptureDescription.Destination.Name = "EventHubArchive.AzureBlockBlob"
PS C:\> $createdEventHub.CaptureDescription.Destination.BlobContainer = "container"
PS C:\> $createdEventHub.CaptureDescription.Destination.ArchiveNameFormat = "{Namespace}/{EventHub}/{PartitionId}/{Year}/{Month}/{Day}/{Hour}/{Minute}/{Second}"
PS C:\> $createdEventHub.CaptureDescription.Destination.StorageAccountResourceId = "/subscriptions/{SubscriptionId}/resourceGroups/MyResourceGroupName/providers/Microsoft.ClassicStorage/storageAccounts/arjunteststorage"
PS C:\> Set-AzEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName -InputObject MyCreatedEventHub -messageRetentionInDays 4 -partitionCount 2
```

<span data-ttu-id="2c739-114">\` \` 3 일 메시지 보존 기간, 2 개 파티션 및 CaptureDescription 속성을 사용 하 여 \` WestUS \` 위치에 리소스 그룹 MyResourceGroupName이 있는 \` MyEventHubName 라는 이벤트 허브를 만듭니다 \` .</span><span class="sxs-lookup"><span data-stu-id="2c739-114">Creates an Event Hub named \`MyEventHubName\` with a 3-day message retention period, 2 partitions and CaptureDescription properties in the \`WestUS\` location, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="2c739-115">변수</span><span class="sxs-lookup"><span data-stu-id="2c739-115">PARAMETERS</span></span>

### <span data-ttu-id="2c739-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c739-116">-DefaultProfile</span></span>
<span data-ttu-id="2c739-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2c739-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c739-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2c739-118">-InputObject</span></span>
<span data-ttu-id="2c739-119">EventHub 입력 개체</span><span class="sxs-lookup"><span data-stu-id="2c739-119">EventHub Input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes
Parameter Sets: EventhubInputObjectSet
Aliases: EventHubObj

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c739-120">-MessageRetentionInDays</span><span class="sxs-lookup"><span data-stu-id="2c739-120">-MessageRetentionInDays</span></span>
<span data-ttu-id="2c739-121">Eventhub 메시지 보존 기간 (일)</span><span class="sxs-lookup"><span data-stu-id="2c739-121">Eventhub Message Retention In Days</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: EventhubPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c739-122">-이름</span><span class="sxs-lookup"><span data-stu-id="2c739-122">-Name</span></span>
<span data-ttu-id="2c739-123">Eventhub 이름</span><span class="sxs-lookup"><span data-stu-id="2c739-123">Eventhub Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c739-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="2c739-124">-Namespace</span></span>
<span data-ttu-id="2c739-125">네임 스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="2c739-125">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c739-126">-파티션 수</span><span class="sxs-lookup"><span data-stu-id="2c739-126">-PartitionCount</span></span>
<span data-ttu-id="2c739-127">Eventhub/Count</span><span class="sxs-lookup"><span data-stu-id="2c739-127">Eventhub PartitionCount</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: EventhubPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c739-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c739-128">-ResourceGroupName</span></span>
<span data-ttu-id="2c739-129">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="2c739-129">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c739-130">-확인</span><span class="sxs-lookup"><span data-stu-id="2c739-130">-Confirm</span></span>
<span data-ttu-id="2c739-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c739-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c739-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c739-132">-WhatIf</span></span>
<span data-ttu-id="2c739-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2c739-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c739-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2c739-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c739-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c739-135">CommonParameters</span></span>
<span data-ttu-id="2c739-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c739-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c739-137">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c739-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c739-138">입력</span><span class="sxs-lookup"><span data-stu-id="2c739-138">INPUTS</span></span>

### <span data-ttu-id="2c739-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="2c739-139">System.String</span></span>

### <span data-ttu-id="2c739-140">PSEventHubAttributes (.).</span><span class="sxs-lookup"><span data-stu-id="2c739-140">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

### <span data-ttu-id="2c739-141">시스템 Null 허용 ' 1 [[System.webserver, System.webserver, CoreLib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="2c739-141">System.Nullable\`1[[System.Int64, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="2c739-142">출력</span><span class="sxs-lookup"><span data-stu-id="2c739-142">OUTPUTS</span></span>

### <span data-ttu-id="2c739-143">PSEventHubAttributes (.).</span><span class="sxs-lookup"><span data-stu-id="2c739-143">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="2c739-144">상속자</span><span class="sxs-lookup"><span data-stu-id="2c739-144">NOTES</span></span>

## <span data-ttu-id="2c739-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2c739-145">RELATED LINKS</span></span>
