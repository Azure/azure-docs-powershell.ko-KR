---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHub.md
ms.openlocfilehash: 15704f90530c332eddfeaf4a9e13fe2d7767bfa4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188433"
---
# <span data-ttu-id="2f719-101">Set-AzEventHub</span><span class="sxs-lookup"><span data-stu-id="2f719-101">Set-AzEventHub</span></span>

## <span data-ttu-id="2f719-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2f719-102">SYNOPSIS</span></span>
<span data-ttu-id="2f719-103">지정된 이벤트 허브를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="2f719-103">Updates the specified Event Hub.</span></span>

## <span data-ttu-id="2f719-104">구문</span><span class="sxs-lookup"><span data-stu-id="2f719-104">SYNTAX</span></span>

### <span data-ttu-id="2f719-105">EventhubInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="2f719-105">EventhubInputObjectSet</span></span>
```
Set-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSEventHubAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2f719-106">EventhubPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="2f719-106">EventhubPropertiesSet</span></span>
```
Set-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-messageRetentionInDays <Int64>] [-partitionCount <Int64>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f719-107">설명</span><span class="sxs-lookup"><span data-stu-id="2f719-107">DESCRIPTION</span></span>
<span data-ttu-id="2f719-108">이 Set-AzEventHub cmdlet은 지정된 이벤트 허브의 속성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="2f719-108">The Set-AzEventHub cmdlet updates the properties of the specified Event Hub.</span></span>

## <span data-ttu-id="2f719-109">예제</span><span class="sxs-lookup"><span data-stu-id="2f719-109">EXAMPLES</span></span>

### <span data-ttu-id="2f719-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="2f719-110">Example 1</span></span>
<span data-ttu-id="2f719-111">캡처 설명 속성으로 Eventhub를 업데이트하기 위해 아래 단계를 수행하세요.</span><span class="sxs-lookup"><span data-stu-id="2f719-111">To update Eventhub with Capture description properties, please follow the below steps.</span></span> 

```
PS C:\> $createdEventHub = Get-AzEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyCreatedEventHub
PS C:\> $ceatedEventHub.CaptureDescription = New-Object -TypeName Microsoft.Azure.Commands.EventHub.Models.PSCaptureDescriptionAttributes
PS C:\> $createdEventHub.CaptureDescription.Enabled = $true
PS C:\> $createdEventHub.CaptureDescription.IntervalInSeconds  = 120
PS C:\> $createdEventHub.CaptureDescription.Encoding  = "Avro"
PS C:\> $createdEventHub.CaptureDescription.SizeLimitInBytes = 10485763
PS C:\> $createdEventHub.CaptureDescription.Destination.Name = "EventHubArchive.AzureBlockBlob"
PS C:\> $createdEventHub.CaptureDescription.Destination.BlobContainer = "container"
PS C:\> $createdEventHub.CaptureDescription.Destination.ArchiveNameFormat = "{Namespace}/{EventHub}/{PartitionId}/{Year}/{Month}/{Day}/{Hour}/{Minute}/{Second}"
PS C:\> $createdEventHub.CaptureDescription.Destination.StorageAccountResourceId = "/subscriptions/{SubscriptionId}/resourceGroups/MyResourceGroupName/providers/Microsoft.ClassicStorage/storageAccounts/arjunteststorage"
PS C:\> Set-AzEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName -InputObject $createdEventHub 
```

<span data-ttu-id="2f719-112">MyCreatedEventHub 개체로 표현되는 Event Hub \` MyEventHubName을 업데이트하여 \` \` \` CaptureDescription 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="2f719-112">Updates the Event Hub \`MyEventHubName\` represented by the \`MyCreatedEventHub\` object, setting the CaptureDescription properties</span></span>

### <span data-ttu-id="2f719-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="2f719-113">Example 2</span></span>
```
PS C:\> Set-AzEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName -InputObject MyCreatedEventHub -messageRetentionInDays 4 -partitionCount 2
```

<span data-ttu-id="2f719-114">MyCreatedEventHub 개체로 표현되는 Event Hub MyEventHubName을 업데이트하여 메시지 보존 기간을 4일로 설정하고 파티션 수를 \` \` \` \` 2로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="2f719-114">Updates the Event Hub \`MyEventHubName\` represented by the \`MyCreatedEventHub\` object, setting the message retention period to 4 days, and the number of partitions to 2.</span></span>

## <span data-ttu-id="2f719-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2f719-115">PARAMETERS</span></span>

### <span data-ttu-id="2f719-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f719-116">-DefaultProfile</span></span>
<span data-ttu-id="2f719-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2f719-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f719-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2f719-118">-InputObject</span></span>
<span data-ttu-id="2f719-119">EventHub 개체</span><span class="sxs-lookup"><span data-stu-id="2f719-119">EventHub object</span></span>

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

### <span data-ttu-id="2f719-120">-messageRetentionInDays</span><span class="sxs-lookup"><span data-stu-id="2f719-120">-messageRetentionInDays</span></span>
<span data-ttu-id="2f719-121">Eventhub 메시지 보존(일)</span><span class="sxs-lookup"><span data-stu-id="2f719-121">Eventhub Message Retention In Days</span></span>

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

### <span data-ttu-id="2f719-122">-Name</span><span class="sxs-lookup"><span data-stu-id="2f719-122">-Name</span></span>
<span data-ttu-id="2f719-123">네임스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="2f719-123">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f719-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="2f719-124">-Namespace</span></span>
<span data-ttu-id="2f719-125">네임스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="2f719-125">Namespace Name</span></span>

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

### <span data-ttu-id="2f719-126">-partitionCount</span><span class="sxs-lookup"><span data-stu-id="2f719-126">-partitionCount</span></span>
<span data-ttu-id="2f719-127">Eventhub PartitionCount</span><span class="sxs-lookup"><span data-stu-id="2f719-127">Eventhub PartitionCount</span></span>

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

### <span data-ttu-id="2f719-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f719-128">-ResourceGroupName</span></span>
<span data-ttu-id="2f719-129">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="2f719-129">Resource Group Name</span></span>

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

### <span data-ttu-id="2f719-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2f719-130">-Confirm</span></span>
<span data-ttu-id="2f719-131">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="2f719-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f719-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f719-132">-WhatIf</span></span>
<span data-ttu-id="2f719-133">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="2f719-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f719-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2f719-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f719-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f719-135">CommonParameters</span></span>
<span data-ttu-id="2f719-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2f719-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f719-137">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="2f719-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f719-138">입력</span><span class="sxs-lookup"><span data-stu-id="2f719-138">INPUTS</span></span>

### <span data-ttu-id="2f719-139">System.String</span><span class="sxs-lookup"><span data-stu-id="2f719-139">System.String</span></span>

### <span data-ttu-id="2f719-140">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="2f719-140">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

### <span data-ttu-id="2f719-141">System.Nullable'1[[System.Int64, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="2f719-141">System.Nullable\`1[[System.Int64, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="2f719-142">출력</span><span class="sxs-lookup"><span data-stu-id="2f719-142">OUTPUTS</span></span>

### <span data-ttu-id="2f719-143">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="2f719-143">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="2f719-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2f719-144">NOTES</span></span>

## <span data-ttu-id="2f719-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2f719-145">RELATED LINKS</span></span>
