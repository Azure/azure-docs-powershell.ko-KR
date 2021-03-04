---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/remove-azservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusQueue.md
ms.openlocfilehash: 5e7ecd25006f86005f34c46ba4fa44df0057c3f0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959387"
---
# <span data-ttu-id="aae7e-101">Remove-AzServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="aae7e-101">Remove-AzServiceBusQueue</span></span>

## <span data-ttu-id="aae7e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aae7e-102">SYNOPSIS</span></span>
<span data-ttu-id="aae7e-103">지정된 Service Bus 네임스페이스에서 큐를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="aae7e-103">Removes the queue from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="aae7e-104">구문</span><span class="sxs-lookup"><span data-stu-id="aae7e-104">SYNTAX</span></span>

### <span data-ttu-id="aae7e-105">QueuePropertiesSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="aae7e-105">QueuePropertiesSet (Default)</span></span>
```
Remove-AzServiceBusQueue [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aae7e-106">QueueInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="aae7e-106">QueueInputObjectSet</span></span>
```
Remove-AzServiceBusQueue [-InputObject] <PSQueueAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aae7e-107">QueueResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="aae7e-107">QueueResourceIdSet</span></span>
```
Remove-AzServiceBusQueue [-ResourceId] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aae7e-108">설명</span><span class="sxs-lookup"><span data-stu-id="aae7e-108">DESCRIPTION</span></span>
<span data-ttu-id="aae7e-109">**Remove-AzServiceBusQueue** cmdlet은 지정된 Service Bus 네임스페이스에서 큐를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="aae7e-109">The **Remove-AzServiceBusQueue** cmdlet removes the queue from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="aae7e-110">예제</span><span class="sxs-lookup"><span data-stu-id="aae7e-110">EXAMPLES</span></span>

### <span data-ttu-id="aae7e-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="aae7e-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1
```

<span data-ttu-id="aae7e-112">네임스페이스에서 Service Bus `SB-Queue_exampl1` 큐를 `SB-Example1` 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="aae7e-112">Removes the Service Bus queue `SB-Queue_exampl1` from the namespace `SB-Example1`.</span></span>

### <span data-ttu-id="aae7e-113">예제 2: InputObject - 변수 사용:</span><span class="sxs-lookup"><span data-stu-id="aae7e-113">Example 2: InputObject - Using variable:</span></span>
```powershell
PS C:\> $inputobject = Get-AzServiceBusQueue <params>
PS C:\> Remove-AzServiceBusQueue -InputObject $inputobject
```

<span data-ttu-id="aae7e-114">-InputObject 매개 변수에 대한 $inputobject Service Bus 큐를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="aae7e-114">Removes the Service Bus queue provided in the $inputobject for -InputObject parameter</span></span>

### <span data-ttu-id="aae7e-115">예제 3: InputObject - 배관 사용:</span><span class="sxs-lookup"><span data-stu-id="aae7e-115">Example 3: InputObject - Using Piping:</span></span>
```powershell
PS C:\>  Get-AzServiceBusQueue <params> | Remove-AzServiceBusQueue
```

### <span data-ttu-id="aae7e-116">예제 4: ResourceId - 변수 사용:</span><span class="sxs-lookup"><span data-stu-id="aae7e-116">Example 4: ResourceId - Using variable:</span></span>
```powershell
PS c:\> $resourceid = Get-AzServiceBusQueue <params>
PS C:\> Remove-AzServiceBusQueue -ResourceId $resourceid.Id
```

<span data-ttu-id="aae7e-117">-ResourceId 매개 변수에 대한 ARM/string에서 $resourceid Service Bus 큐를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="aae7e-117">Removes the Service Bus queue provided in the ARM id in $resourceid/string for -ResourceId parameter</span></span>

### <span data-ttu-id="aae7e-118">예제 5: ResourceId - 문자열로 전달:</span><span class="sxs-lookup"><span data-stu-id="aae7e-118">Example 5: ResourceId - passing as string:</span></span>
```powershell
PS C:\> Remove-AzServiceBusQueue -ResourceId "/subscriptions/xxxx-xxxxx-xxxxx-xxxxxx-xxxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.ServiceBus/namespaces/NamespaceName/queues/QueueName"
```

## <span data-ttu-id="aae7e-119">매개 변수</span><span class="sxs-lookup"><span data-stu-id="aae7e-119">PARAMETERS</span></span>

### <span data-ttu-id="aae7e-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aae7e-120">-AsJob</span></span>
<span data-ttu-id="aae7e-121">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="aae7e-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="aae7e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aae7e-122">-DefaultProfile</span></span>
<span data-ttu-id="aae7e-123">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="aae7e-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aae7e-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aae7e-124">-InputObject</span></span>
<span data-ttu-id="aae7e-125">Service Bus 큐 개체</span><span class="sxs-lookup"><span data-stu-id="aae7e-125">Service Bus Queue Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes
Parameter Sets: QueueInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aae7e-126">-Name</span><span class="sxs-lookup"><span data-stu-id="aae7e-126">-Name</span></span>
<span data-ttu-id="aae7e-127">큐 이름</span><span class="sxs-lookup"><span data-stu-id="aae7e-127">Queue Name</span></span>

```yaml
Type: System.String
Parameter Sets: QueuePropertiesSet
Aliases: QueueName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aae7e-128">-네임스페이스</span><span class="sxs-lookup"><span data-stu-id="aae7e-128">-Namespace</span></span>
<span data-ttu-id="aae7e-129">네임스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="aae7e-129">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: QueuePropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aae7e-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="aae7e-130">-PassThru</span></span>
<span data-ttu-id="aae7e-131">명령이 성공하면 이를 지정하면 true가 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="aae7e-131">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="aae7e-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aae7e-132">-ResourceGroupName</span></span>
<span data-ttu-id="aae7e-133">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="aae7e-133">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: QueuePropertiesSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aae7e-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aae7e-134">-ResourceId</span></span>
<span data-ttu-id="aae7e-135">Service Bus 큐 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="aae7e-135">Service Bus Queue Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: QueueResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aae7e-136">-확인</span><span class="sxs-lookup"><span data-stu-id="aae7e-136">-Confirm</span></span>
<span data-ttu-id="aae7e-137">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="aae7e-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aae7e-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aae7e-138">-WhatIf</span></span>
<span data-ttu-id="aae7e-139">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="aae7e-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aae7e-140">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="aae7e-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aae7e-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aae7e-141">CommonParameters</span></span>
<span data-ttu-id="aae7e-142">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="aae7e-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aae7e-143">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="aae7e-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aae7e-144">입력</span><span class="sxs-lookup"><span data-stu-id="aae7e-144">INPUTS</span></span>

### <span data-ttu-id="aae7e-145">System.String</span><span class="sxs-lookup"><span data-stu-id="aae7e-145">System.String</span></span>

### <span data-ttu-id="aae7e-146">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="aae7e-146">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="aae7e-147">출력</span><span class="sxs-lookup"><span data-stu-id="aae7e-147">OUTPUTS</span></span>

### <span data-ttu-id="aae7e-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="aae7e-148">System.Boolean</span></span>

## <span data-ttu-id="aae7e-149">참고 사항</span><span class="sxs-lookup"><span data-stu-id="aae7e-149">NOTES</span></span>

## <span data-ttu-id="aae7e-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="aae7e-150">RELATED LINKS</span></span>
