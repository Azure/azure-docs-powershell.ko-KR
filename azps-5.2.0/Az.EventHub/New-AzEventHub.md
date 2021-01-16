---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHub.md
ms.openlocfilehash: eec7294a15217be85b4c2248dac6506d54c2e6aa
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98332313"
---
# <span data-ttu-id="31613-101">New-AzEventHub</span><span class="sxs-lookup"><span data-stu-id="31613-101">New-AzEventHub</span></span>

## <span data-ttu-id="31613-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31613-102">SYNOPSIS</span></span>
<span data-ttu-id="31613-103">새 이벤트 허브를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="31613-103">Creates a new Event Hub.</span></span>

## <span data-ttu-id="31613-104">구문</span><span class="sxs-lookup"><span data-stu-id="31613-104">SYNTAX</span></span>

### <span data-ttu-id="31613-105">EventhubPropertiesSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="31613-105">EventhubPropertiesSet (Default)</span></span>
```
New-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-MessageRetentionInDays <Int64>] [-PartitionCount <Int64>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31613-106">EventhubInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="31613-106">EventhubInputObjectSet</span></span>
```
New-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSEventHubAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="31613-107">설명</span><span class="sxs-lookup"><span data-stu-id="31613-107">DESCRIPTION</span></span>
<span data-ttu-id="31613-108">New-AzEventHub cmdlet은 새 Azure 이벤트 허브를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="31613-108">The New-AzEventHub cmdlet creates a new Azure Event Hub.</span></span>
<span data-ttu-id="31613-109">캡처 설명 속성을 사용하여 Eventhub를 만들 경우 아래 단계(예제 2)를 따르세요.</span><span class="sxs-lookup"><span data-stu-id="31613-109">To create Eventhub with Capture description properties, please follow the below steps (Examples 2).</span></span> 

## <span data-ttu-id="31613-110">예제</span><span class="sxs-lookup"><span data-stu-id="31613-110">EXAMPLES</span></span>

### <span data-ttu-id="31613-111">예제 1: - 새 EventHub 만들기</span><span class="sxs-lookup"><span data-stu-id="31613-111">Example 1: - Create new EventHub</span></span>
```powershell
PS C:\> New-AzEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Name MyEventHubName
```

<span data-ttu-id="31613-112">리소스 그룹 \` \` \` \` \` MyResourceGroupName을 통해 3일의 메시지 보존 기간과 2개의 파티션이 있는 MyEventHubName이라는 이벤트 허브를 WestUS 위치에 \` 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="31613-112">Creates an Event Hub named \`MyEventHubName\` with a 3-day message retention period and two partitions, in the \`WestUS\` location, with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="31613-113">예제 2: Eventhub를 'CaptureDescription'으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="31613-113">Example 2: Update Eventhub with 'CaptureDescription'</span></span>
```powershell
PS C:\> New-AzEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Name MyEventHubName -MessageRetentionInDays 3 -PartitionCount 2

PS C:\> $CreatedEventHub = Get-AzEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName

PS C:\> $createdEventHub.CaptureDescription = New-Object -TypeName Microsoft.Azure.Commands.EventHub.Models.PSCaptureDescriptionAttributes

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

<span data-ttu-id="31613-114">리소스 그룹 \` \` \` \` \` MyResourceGroupName을 사용하여 3일의 메시지 보존 기간, 2개 파티션 및 CaptureDescription 속성을 사용하여 MyEventHubName이라는 이벤트 허브를 \` 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="31613-114">Creates an Event Hub named \`MyEventHubName\` with a 3-day message retention period, 2 partitions and CaptureDescription properties in the \`WestUS\` location, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="31613-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="31613-115">PARAMETERS</span></span>

### <span data-ttu-id="31613-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31613-116">-DefaultProfile</span></span>
<span data-ttu-id="31613-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="31613-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31613-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="31613-118">-InputObject</span></span>
<span data-ttu-id="31613-119">EventHub 입력 개체</span><span class="sxs-lookup"><span data-stu-id="31613-119">EventHub Input object</span></span>

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

### <span data-ttu-id="31613-120">-MessageRetentionInDays</span><span class="sxs-lookup"><span data-stu-id="31613-120">-MessageRetentionInDays</span></span>
<span data-ttu-id="31613-121">Eventhub 메시지 보존(일)</span><span class="sxs-lookup"><span data-stu-id="31613-121">Eventhub Message Retention In Days</span></span>

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

### <span data-ttu-id="31613-122">-Name</span><span class="sxs-lookup"><span data-stu-id="31613-122">-Name</span></span>
<span data-ttu-id="31613-123">Eventhub 이름</span><span class="sxs-lookup"><span data-stu-id="31613-123">Eventhub Name</span></span>

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

### <span data-ttu-id="31613-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="31613-124">-Namespace</span></span>
<span data-ttu-id="31613-125">네임스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="31613-125">Namespace Name</span></span>

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

### <span data-ttu-id="31613-126">-PartitionCount</span><span class="sxs-lookup"><span data-stu-id="31613-126">-PartitionCount</span></span>
<span data-ttu-id="31613-127">Eventhub PartitionCount</span><span class="sxs-lookup"><span data-stu-id="31613-127">Eventhub PartitionCount</span></span>

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

### <span data-ttu-id="31613-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31613-128">-ResourceGroupName</span></span>
<span data-ttu-id="31613-129">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="31613-129">Resource Group Name</span></span>

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

### <span data-ttu-id="31613-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="31613-130">-Confirm</span></span>
<span data-ttu-id="31613-131">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="31613-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31613-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31613-132">-WhatIf</span></span>
<span data-ttu-id="31613-133">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="31613-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="31613-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="31613-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31613-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31613-135">CommonParameters</span></span>
<span data-ttu-id="31613-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="31613-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31613-137">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="31613-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31613-138">입력</span><span class="sxs-lookup"><span data-stu-id="31613-138">INPUTS</span></span>

### <span data-ttu-id="31613-139">System.String</span><span class="sxs-lookup"><span data-stu-id="31613-139">System.String</span></span>

### <span data-ttu-id="31613-140">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="31613-140">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

### <span data-ttu-id="31613-141">System.Nullable'1[[System.Int64, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="31613-141">System.Nullable\`1[[System.Int64, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="31613-142">출력</span><span class="sxs-lookup"><span data-stu-id="31613-142">OUTPUTS</span></span>

### <span data-ttu-id="31613-143">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="31613-143">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="31613-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="31613-144">NOTES</span></span>

## <span data-ttu-id="31613-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="31613-145">RELATED LINKS</span></span>
