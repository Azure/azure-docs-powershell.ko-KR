---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/set-azurermservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusQueue.md
ms.openlocfilehash: 785685981c38248fba944cc9e3809a2de1f32e71
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529717"
---
# <span data-ttu-id="40f5b-101">Set-AzureRmServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="40f5b-101">Set-AzureRmServiceBusQueue</span></span>

## <span data-ttu-id="40f5b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40f5b-102">SYNOPSIS</span></span>
<span data-ttu-id="40f5b-103">지정 된 Service Bus 네임 스페이스의 Service Bus 큐에 대 한 설명을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="40f5b-103">Updates the description of a Service Bus queue in the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="40f5b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="40f5b-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusQueue [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject] <QueueAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="40f5b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="40f5b-105">DESCRIPTION</span></span>
<span data-ttu-id="40f5b-106">**Set-AzureRmServiceBusQueue** cmdlet은 지정 된 service bus 네임 스페이스의 service bus 큐에 대 한 설명을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="40f5b-106">The **Set-AzureRmServiceBusQueue** cmdlet updates the description for the Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="40f5b-107">예제의</span><span class="sxs-lookup"><span data-stu-id="40f5b-107">EXAMPLES</span></span>

### <span data-ttu-id="40f5b-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="40f5b-108">Example 1</span></span>
```
PS C:\> $QueueObj = Get-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1

PS C:\> $QueueObj.DeadLetteringOnMessageExpiration = $True
PS C:\> $QueueObj.SupportOrdering = $True

PS C:\> Set-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -QueueObj $QueueObj

Name                                : SB-Queue_exampl1
LockDuration                        : 
AccessedAt                          : 1/1/0001 12:00:00 AM
AutoDeleteOnIdle                    : 10675199.02:48:05.4775807
CreatedAt                           : 1/20/2017 2:51:34 AM
DefaultMessageTimeToLive            : 10675199.02:48:05.4775807
DuplicateDetectionHistoryTimeWindow : 
DeadLetteringOnMessageExpiration    : False
EnableExpress                       : False
EnablePartitioning                  : True
MaxDeliveryCount                    : 
MaxSizeInMegabytes                  : 16384
MessageCount                        : 
CountDetails                        : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails
RequiresDuplicateDetection          : False
RequiresSession                     : False
SizeInBytes                         : 
Status                              : Active
UpdatedAt                           : 1/20/2017 6:16:18 PM
```

<span data-ttu-id="40f5b-109">지정한 네임 스페이스의 새 설명으로 지정 된 큐를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="40f5b-109">Updates the specified queue with a new description in the specified namespace.</span></span> <span data-ttu-id="40f5b-110">이 예제에서는 **DeadLetteringOnMessageExpiration** 속성을 **True** 로, **supportordering** 를 **true** 로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="40f5b-110">This example updates the **DeadLetteringOnMessageExpiration** property to **true** and **SupportOrdering** to **true**.</span></span>

## <span data-ttu-id="40f5b-111">변수</span><span class="sxs-lookup"><span data-stu-id="40f5b-111">PARAMETERS</span></span>

### <span data-ttu-id="40f5b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40f5b-112">-DefaultProfile</span></span>
<span data-ttu-id="40f5b-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="40f5b-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="40f5b-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="40f5b-114">-InputObject</span></span>
<span data-ttu-id="40f5b-115">ServiceBus 정의.</span><span class="sxs-lookup"><span data-stu-id="40f5b-115">ServiceBus definition.</span></span>

```yaml
Type: PSQueueAttributes
Parameter Sets: (All)
Aliases: QueueObj

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40f5b-116">-이름</span><span class="sxs-lookup"><span data-stu-id="40f5b-116">-Name</span></span>
<span data-ttu-id="40f5b-117">큐 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="40f5b-117">Queue Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: QueueName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40f5b-118">-Namespace</span><span class="sxs-lookup"><span data-stu-id="40f5b-118">-Namespace</span></span>
<span data-ttu-id="40f5b-119">네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="40f5b-119">Namespace Name.</span></span>

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

### <span data-ttu-id="40f5b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40f5b-120">-ResourceGroupName</span></span>
<span data-ttu-id="40f5b-121">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="40f5b-121">The name of the resource group</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40f5b-122">-확인</span><span class="sxs-lookup"><span data-stu-id="40f5b-122">-Confirm</span></span>
<span data-ttu-id="40f5b-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="40f5b-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40f5b-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40f5b-124">-WhatIf</span></span>
<span data-ttu-id="40f5b-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="40f5b-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40f5b-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="40f5b-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40f5b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40f5b-127">CommonParameters</span></span>
<span data-ttu-id="40f5b-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="40f5b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40f5b-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40f5b-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40f5b-130">입력</span><span class="sxs-lookup"><span data-stu-id="40f5b-130">INPUTS</span></span>

### <span data-ttu-id="40f5b-131">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="40f5b-131">-ResourceGroup</span></span>
 <span data-ttu-id="40f5b-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="40f5b-132">System.String</span></span>

### <span data-ttu-id="40f5b-133">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="40f5b-133">-NamespaceName</span></span>
 <span data-ttu-id="40f5b-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="40f5b-134">System.String</span></span>

### <span data-ttu-id="40f5b-135">-QueueName</span><span class="sxs-lookup"><span data-stu-id="40f5b-135">-QueueName</span></span>
 <span data-ttu-id="40f5b-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="40f5b-136">System.String</span></span>

### <span data-ttu-id="40f5b-137">-QueueObj</span><span class="sxs-lookup"><span data-stu-id="40f5b-137">-QueueObj</span></span>
 <span data-ttu-id="40f5b-138">ServiceBus. a m/.</span><span class="sxs-lookup"><span data-stu-id="40f5b-138">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="40f5b-139">출력</span><span class="sxs-lookup"><span data-stu-id="40f5b-139">OUTPUTS</span></span>

### <span data-ttu-id="40f5b-140">ServiceBus. a m/.</span><span class="sxs-lookup"><span data-stu-id="40f5b-140">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="40f5b-141">상속자</span><span class="sxs-lookup"><span data-stu-id="40f5b-141">NOTES</span></span>

## <span data-ttu-id="40f5b-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="40f5b-142">RELATED LINKS</span></span>

