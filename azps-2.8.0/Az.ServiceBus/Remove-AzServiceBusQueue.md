---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusQueue.md
ms.openlocfilehash: 23aff5b896664321033183ad35909300f9a5c3b7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93871586"
---
# <span data-ttu-id="67647-101">Remove-AzServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="67647-101">Remove-AzServiceBusQueue</span></span>

## <span data-ttu-id="67647-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67647-102">SYNOPSIS</span></span>
<span data-ttu-id="67647-103">지정 된 Service Bus 네임 스페이스에서 큐를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="67647-103">Removes the queue from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="67647-104">구문과</span><span class="sxs-lookup"><span data-stu-id="67647-104">SYNTAX</span></span>

### <span data-ttu-id="67647-105">Queue속성 집합 (기본값)</span><span class="sxs-lookup"><span data-stu-id="67647-105">QueuePropertiesSet (Default)</span></span>
```
Remove-AzServiceBusQueue [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67647-106">QueueInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="67647-106">QueueInputObjectSet</span></span>
```
Remove-AzServiceBusQueue [-InputObject] <PSQueueAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67647-107">QueueResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="67647-107">QueueResourceIdSet</span></span>
```
Remove-AzServiceBusQueue [-ResourceId] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67647-108">설명은</span><span class="sxs-lookup"><span data-stu-id="67647-108">DESCRIPTION</span></span>
<span data-ttu-id="67647-109">**AzServiceBusQueue** cmdlet은 지정 된 Service Bus 네임 스페이스에서 큐를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="67647-109">The **Remove-AzServiceBusQueue** cmdlet removes the queue from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="67647-110">예제의</span><span class="sxs-lookup"><span data-stu-id="67647-110">EXAMPLES</span></span>

### <span data-ttu-id="67647-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="67647-111">Example 1</span></span>
```
PS C:\> Remove-AzServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1
```

<span data-ttu-id="67647-112">네임 스페이스에서 서비스 버스 대기열을 제거 합니다 `SB-Queue_exampl1` `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="67647-112">Removes the Service Bus queue `SB-Queue_exampl1` from the namespace `SB-Example1`.</span></span>

### <span data-ttu-id="67647-113">예제 2.1-InputObject-Using 변수:</span><span class="sxs-lookup"><span data-stu-id="67647-113">Example 2.1 - InputObject - Using variable:</span></span>
```
PS C:\> $inputobject = Get-AzServiceBusQueue <params>
PS C:\> Remove-AzServiceBusQueue -InputObject $inputobject
```

<span data-ttu-id="67647-114">-InputObject 매개 변수에 대 한 $inputobject에 제공 된 서비스 버스 대기열을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="67647-114">Removes the Service Bus queue provided in the $inputobject for -InputObject parameter</span></span>

### <span data-ttu-id="67647-115">예제 2.1-InputObject-Using 파이핑:</span><span class="sxs-lookup"><span data-stu-id="67647-115">Example 2.1 - InputObject - Using Piping:</span></span>
```
PS C:\>  Get-AzServiceBusQueue <params> | Remove-AzServiceBusQueue
```

### <span data-ttu-id="67647-116">예제 3.1-ResourceId-변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="67647-116">Example 3.1 - ResourceId - Using variable:</span></span>
```
PS c:\> $resourceid = Get-AzServiceBusQueue <params>
PS C:\> Remove-AzServiceBusQueue -ResourceId $resourceid.Id
```

<span data-ttu-id="67647-117">-ResourceId 매개 변수에 대 한 $resourceid/문자열의 ARM id에 제공 된 서비스 버스 대기열을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="67647-117">Removes the Service Bus queue provided in the ARM id in $resourceid/string for -ResourceId parameter</span></span>

### <span data-ttu-id="67647-118">예제 3.2-ResourceId-string으로 전달:</span><span class="sxs-lookup"><span data-stu-id="67647-118">Example 3.2 - ResourceId - passing as string:</span></span>
```
PS C:\> Remove-AzServiceBusQueue -ResourceId "/subscriptions/xxxx-xxxxx-xxxxx-xxxxxx-xxxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.ServiceBus/namespaces/NamespaceName/queues/QueueName"
```

## <span data-ttu-id="67647-119">변수</span><span class="sxs-lookup"><span data-stu-id="67647-119">PARAMETERS</span></span>

### <span data-ttu-id="67647-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="67647-120">-AsJob</span></span>
<span data-ttu-id="67647-121">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="67647-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="67647-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67647-122">-DefaultProfile</span></span>
<span data-ttu-id="67647-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="67647-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67647-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="67647-124">-InputObject</span></span>
<span data-ttu-id="67647-125">Service Bus 큐 개체</span><span class="sxs-lookup"><span data-stu-id="67647-125">Service Bus Queue Object</span></span>

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

### <span data-ttu-id="67647-126">-이름</span><span class="sxs-lookup"><span data-stu-id="67647-126">-Name</span></span>
<span data-ttu-id="67647-127">큐 이름</span><span class="sxs-lookup"><span data-stu-id="67647-127">Queue Name</span></span>

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

### <span data-ttu-id="67647-128">-Namespace</span><span class="sxs-lookup"><span data-stu-id="67647-128">-Namespace</span></span>
<span data-ttu-id="67647-129">네임 스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="67647-129">Namespace Name</span></span>

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

### <span data-ttu-id="67647-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="67647-130">-PassThru</span></span>
<span data-ttu-id="67647-131">명령이 성공적으로 실행 되 면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="67647-131">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="67647-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67647-132">-ResourceGroupName</span></span>
<span data-ttu-id="67647-133">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="67647-133">The name of the resource group</span></span>

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

### <span data-ttu-id="67647-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="67647-134">-ResourceId</span></span>
<span data-ttu-id="67647-135">Service Bus 큐 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="67647-135">Service Bus Queue Resource Id</span></span>

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

### <span data-ttu-id="67647-136">-확인</span><span class="sxs-lookup"><span data-stu-id="67647-136">-Confirm</span></span>
<span data-ttu-id="67647-137">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="67647-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67647-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67647-138">-WhatIf</span></span>
<span data-ttu-id="67647-139">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="67647-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67647-140">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="67647-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67647-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67647-141">CommonParameters</span></span>
<span data-ttu-id="67647-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="67647-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67647-143">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67647-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67647-144">입력</span><span class="sxs-lookup"><span data-stu-id="67647-144">INPUTS</span></span>

### <span data-ttu-id="67647-145">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="67647-145">System.String</span></span>

### <span data-ttu-id="67647-146">ServiceBus. a m/.</span><span class="sxs-lookup"><span data-stu-id="67647-146">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="67647-147">출력</span><span class="sxs-lookup"><span data-stu-id="67647-147">OUTPUTS</span></span>

### <span data-ttu-id="67647-148">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="67647-148">System.Boolean</span></span>

## <span data-ttu-id="67647-149">상속자</span><span class="sxs-lookup"><span data-stu-id="67647-149">NOTES</span></span>

## <span data-ttu-id="67647-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="67647-150">RELATED LINKS</span></span>
