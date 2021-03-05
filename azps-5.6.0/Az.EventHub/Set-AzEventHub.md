---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/set-azeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHub.md
ms.openlocfilehash: 70c059598f895ee933abefb0b71aa36d5ce0f6f7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980416"
---
# <span data-ttu-id="3fcce-101">Set-AzEventHub</span><span class="sxs-lookup"><span data-stu-id="3fcce-101">Set-AzEventHub</span></span>

## <span data-ttu-id="3fcce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3fcce-102">SYNOPSIS</span></span>
<span data-ttu-id="3fcce-103">지정된 Event Hub를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="3fcce-103">Updates the specified Event Hub.</span></span>

## <span data-ttu-id="3fcce-104">구문</span><span class="sxs-lookup"><span data-stu-id="3fcce-104">SYNTAX</span></span>

### <span data-ttu-id="3fcce-105">EventhubInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="3fcce-105">EventhubInputObjectSet</span></span>
```
Set-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSEventHubAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3fcce-106">EventhubPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="3fcce-106">EventhubPropertiesSet</span></span>
```
Set-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-messageRetentionInDays <Int64>] [-partitionCount <Int64>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3fcce-107">설명</span><span class="sxs-lookup"><span data-stu-id="3fcce-107">DESCRIPTION</span></span>
<span data-ttu-id="3fcce-108">Set-AzEventHub cmdlet은 지정된 Event Hub의 속성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="3fcce-108">The Set-AzEventHub cmdlet updates the properties of the specified Event Hub.</span></span>

## <span data-ttu-id="3fcce-109">예제</span><span class="sxs-lookup"><span data-stu-id="3fcce-109">EXAMPLES</span></span>

### <span data-ttu-id="3fcce-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="3fcce-110">Example 1</span></span>
<span data-ttu-id="3fcce-111">Capture 설명 속성을 사용하여 Eventhub를 업데이트하기 위해 아래 단계를 따르세요.</span><span class="sxs-lookup"><span data-stu-id="3fcce-111">To update Eventhub with Capture description properties, please follow the below steps.</span></span> 

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

<span data-ttu-id="3fcce-112">\`MyCreatedEventHub 개체로 나타내는 Event Hub MyEventHubName을 업데이트하여 \` \` \` CaptureDescription 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="3fcce-112">Updates the Event Hub \`MyEventHubName\` represented by the \`MyCreatedEventHub\` object, setting the CaptureDescription properties</span></span>

### <span data-ttu-id="3fcce-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="3fcce-113">Example 2</span></span>
```
PS C:\> Set-AzEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName -InputObject MyCreatedEventHub -messageRetentionInDays 4 -partitionCount 2
```

<span data-ttu-id="3fcce-114">\`MyCreatedEventHub 개체로 나타내는 Event Hub MyEventHubName을 업데이트하고 메시지 보존 기간을 \` \` \` 4일로 설정하고 파티션 수를 2로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="3fcce-114">Updates the Event Hub \`MyEventHubName\` represented by the \`MyCreatedEventHub\` object, setting the message retention period to 4 days, and the number of partitions to 2.</span></span>

## <span data-ttu-id="3fcce-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="3fcce-115">PARAMETERS</span></span>

### <span data-ttu-id="3fcce-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fcce-116">-DefaultProfile</span></span>
<span data-ttu-id="3fcce-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3fcce-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3fcce-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3fcce-118">-InputObject</span></span>
<span data-ttu-id="3fcce-119">EventHub 개체</span><span class="sxs-lookup"><span data-stu-id="3fcce-119">EventHub object</span></span>

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

### <span data-ttu-id="3fcce-120">-messageRetentionInDays</span><span class="sxs-lookup"><span data-stu-id="3fcce-120">-messageRetentionInDays</span></span>
<span data-ttu-id="3fcce-121">며칠 동안의 Eventhub 메시지 보존</span><span class="sxs-lookup"><span data-stu-id="3fcce-121">Eventhub Message Retention In Days</span></span>

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

### <span data-ttu-id="3fcce-122">-Name</span><span class="sxs-lookup"><span data-stu-id="3fcce-122">-Name</span></span>
<span data-ttu-id="3fcce-123">네임스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="3fcce-123">Namespace Name</span></span>

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

### <span data-ttu-id="3fcce-124">-네임스페이스</span><span class="sxs-lookup"><span data-stu-id="3fcce-124">-Namespace</span></span>
<span data-ttu-id="3fcce-125">네임스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="3fcce-125">Namespace Name</span></span>

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

### <span data-ttu-id="3fcce-126">-partitionCount</span><span class="sxs-lookup"><span data-stu-id="3fcce-126">-partitionCount</span></span>
<span data-ttu-id="3fcce-127">Eventhub PartitionCount</span><span class="sxs-lookup"><span data-stu-id="3fcce-127">Eventhub PartitionCount</span></span>

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

### <span data-ttu-id="3fcce-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3fcce-128">-ResourceGroupName</span></span>
<span data-ttu-id="3fcce-129">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="3fcce-129">Resource Group Name</span></span>

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

### <span data-ttu-id="3fcce-130">-확인</span><span class="sxs-lookup"><span data-stu-id="3fcce-130">-Confirm</span></span>
<span data-ttu-id="3fcce-131">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="3fcce-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3fcce-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3fcce-132">-WhatIf</span></span>
<span data-ttu-id="3fcce-133">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="3fcce-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3fcce-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3fcce-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3fcce-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fcce-135">CommonParameters</span></span>
<span data-ttu-id="3fcce-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3fcce-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fcce-137">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="3fcce-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fcce-138">입력</span><span class="sxs-lookup"><span data-stu-id="3fcce-138">INPUTS</span></span>

### <span data-ttu-id="3fcce-139">System.String</span><span class="sxs-lookup"><span data-stu-id="3fcce-139">System.String</span></span>

### <span data-ttu-id="3fcce-140">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="3fcce-140">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

### <span data-ttu-id="3fcce-141">System.Nullable'1[[System.Int64, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="3fcce-141">System.Nullable\`1[[System.Int64, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="3fcce-142">출력</span><span class="sxs-lookup"><span data-stu-id="3fcce-142">OUTPUTS</span></span>

### <span data-ttu-id="3fcce-143">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="3fcce-143">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="3fcce-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3fcce-144">NOTES</span></span>

## <span data-ttu-id="3fcce-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3fcce-145">RELATED LINKS</span></span>
