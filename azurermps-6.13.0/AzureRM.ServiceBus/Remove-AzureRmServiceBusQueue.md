---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/remove-azurermservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusQueue.md
ms.openlocfilehash: ba59f19183cf49802240d7631b99b3e69a9bc6f5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530904"
---
# <span data-ttu-id="d5868-101">Remove-AzureRmServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="d5868-101">Remove-AzureRmServiceBusQueue</span></span>

## <span data-ttu-id="d5868-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5868-102">SYNOPSIS</span></span>
<span data-ttu-id="d5868-103">지정 된 Service Bus 네임 스페이스에서 큐를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5868-103">Removes the queue from the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d5868-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d5868-104">SYNTAX</span></span>

### <span data-ttu-id="d5868-105">Queue속성 집합 (기본값)</span><span class="sxs-lookup"><span data-stu-id="d5868-105">QueuePropertiesSet (Default)</span></span>
```
Remove-AzureRmServiceBusQueue [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5868-106">QueueInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d5868-106">QueueInputObjectSet</span></span>
```
Remove-AzureRmServiceBusQueue [-InputObject] <PSQueueAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5868-107">QueueResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="d5868-107">QueueResourceIdSet</span></span>
```
Remove-AzureRmServiceBusQueue [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d5868-108">설명은</span><span class="sxs-lookup"><span data-stu-id="d5868-108">DESCRIPTION</span></span>
<span data-ttu-id="d5868-109">**AzureRmServiceBusQueue** cmdlet은 지정 된 Service Bus 네임 스페이스에서 큐를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5868-109">The **Remove-AzureRmServiceBusQueue** cmdlet removes the queue from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="d5868-110">예제의</span><span class="sxs-lookup"><span data-stu-id="d5868-110">EXAMPLES</span></span>

### <span data-ttu-id="d5868-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="d5868-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1
```

<span data-ttu-id="d5868-112">네임 스페이스에서 서비스 버스 대기열을 제거 합니다 `SB-Queue_exampl1` `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="d5868-112">Removes the Service Bus queue `SB-Queue_exampl1` from the namespace `SB-Example1`.</span></span>

### <span data-ttu-id="d5868-113">예제 2.1-InputObject-Using 변수:</span><span class="sxs-lookup"><span data-stu-id="d5868-113">Example 2.1 - InputObject - Using variable:</span></span>
```
PS C:\> $inputobject = Get-AzureRmServiceBusQueue <params>
PS C:\> Remove-AzureRmServiceBusQueue -InputObject $inputobject
```

<span data-ttu-id="d5868-114">-InputObject 매개 변수에 대 한 $inputobject에 제공 된 서비스 버스 대기열을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5868-114">Removes the Service Bus queue provided in the $inputobject for -InputObject parameter</span></span>

### <span data-ttu-id="d5868-115">예제 2.1-InputObject-Using 파이핑:</span><span class="sxs-lookup"><span data-stu-id="d5868-115">Example 2.1 - InputObject - Using Piping:</span></span>
```
PS C:\>  Get-AzureRmServiceBusQueue <params> | Remove-AzureRmServiceBusQueue
```

### <span data-ttu-id="d5868-116">예제 3.1-ResourceId-변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5868-116">Example 3.1 - ResourceId - Using variable:</span></span>
```
PS c:\> $resourceid = Get-AzureRmServiceBusQueue <params>
PS C:\> Remove-AzureRmServiceBusQueue -ResourceId $resourceid.Id
```

<span data-ttu-id="d5868-117">-ResourceId 매개 변수에 대 한 $resourceid/문자열의 ARM id에 제공 된 서비스 버스 대기열을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5868-117">Removes the Service Bus queue provided in the ARM id in $resourceid/string for -ResourceId parameter</span></span>

### <span data-ttu-id="d5868-118">예제 3.2-ResourceId-문자열 형식으로 기호:</span><span class="sxs-lookup"><span data-stu-id="d5868-118">Example 3.2 - ResourceId - passign as string:</span></span>
```
PS C:\> Remove-AzureRmServiceBusQueue -ResourceId "/subscriptions/xxxx-xxxxx-xxxxx-xxxxxx-xxxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.ServiceBus/namespaces/NamespaceName/queues/QueueName"
```

## <span data-ttu-id="d5868-119">변수</span><span class="sxs-lookup"><span data-stu-id="d5868-119">PARAMETERS</span></span>

### <span data-ttu-id="d5868-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d5868-120">-AsJob</span></span>
<span data-ttu-id="d5868-121">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="d5868-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d5868-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5868-122">-DefaultProfile</span></span>
<span data-ttu-id="d5868-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d5868-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5868-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d5868-124">-InputObject</span></span>
<span data-ttu-id="d5868-125">Service Bus 큐 개체</span><span class="sxs-lookup"><span data-stu-id="d5868-125">Service Bus Queue Object</span></span>

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

### <span data-ttu-id="d5868-126">-이름</span><span class="sxs-lookup"><span data-stu-id="d5868-126">-Name</span></span>
<span data-ttu-id="d5868-127">큐 이름</span><span class="sxs-lookup"><span data-stu-id="d5868-127">Queue Name</span></span>

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

### <span data-ttu-id="d5868-128">-Namespace</span><span class="sxs-lookup"><span data-stu-id="d5868-128">-Namespace</span></span>
<span data-ttu-id="d5868-129">네임 스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="d5868-129">Namespace Name</span></span>

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

### <span data-ttu-id="d5868-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d5868-130">-PassThru</span></span>
<span data-ttu-id="d5868-131">명령이 성공적으로 실행 되 면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5868-131">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="d5868-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5868-132">-ResourceGroupName</span></span>
<span data-ttu-id="d5868-133">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d5868-133">The name of the resource group</span></span>

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

### <span data-ttu-id="d5868-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d5868-134">-ResourceId</span></span>
<span data-ttu-id="d5868-135">Service Bus 큐 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="d5868-135">Service Bus Queue Resource Id</span></span>

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

### <span data-ttu-id="d5868-136">-확인</span><span class="sxs-lookup"><span data-stu-id="d5868-136">-Confirm</span></span>
<span data-ttu-id="d5868-137">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5868-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5868-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5868-138">-WhatIf</span></span>
<span data-ttu-id="d5868-139">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d5868-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d5868-140">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d5868-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5868-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5868-141">CommonParameters</span></span>
<span data-ttu-id="d5868-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5868-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5868-143">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5868-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5868-144">입력</span><span class="sxs-lookup"><span data-stu-id="d5868-144">INPUTS</span></span>

### <span data-ttu-id="d5868-145">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d5868-145">System.String</span></span>

### <span data-ttu-id="d5868-146">ServiceBus. a m/.</span><span class="sxs-lookup"><span data-stu-id="d5868-146">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>
<span data-ttu-id="d5868-147">매개 변수: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d5868-147">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="d5868-148">출력</span><span class="sxs-lookup"><span data-stu-id="d5868-148">OUTPUTS</span></span>

### <span data-ttu-id="d5868-149">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="d5868-149">System.Boolean</span></span>

## <span data-ttu-id="d5868-150">상속자</span><span class="sxs-lookup"><span data-stu-id="d5868-150">NOTES</span></span>

## <span data-ttu-id="d5868-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d5868-151">RELATED LINKS</span></span>
