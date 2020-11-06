---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusTopic.md
ms.openlocfilehash: 099088bb560606990baa4f1774d8f46c5f68f04b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529157"
---
# <span data-ttu-id="c1ba7-101">New-AzureRmServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="c1ba7-101">New-AzureRmServiceBusTopic</span></span>

## <span data-ttu-id="c1ba7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c1ba7-102">SYNOPSIS</span></span>
<span data-ttu-id="c1ba7-103">지정 된 Service Bus 네임 스페이스에 새 Service Bus 항목을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c1ba7-103">Creates a new Service Bus topic in  the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c1ba7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c1ba7-104">SYNTAX</span></span>

```
New-AzureRmServiceBusTopic -ResourceGroupName <String> -Namespace <String> -Name <String>
 -EnablePartitioning <Boolean> [-AutoDeleteOnIdle <String>] [-DefaultMessageTimeToLive <String>]
 [-DuplicateDetectionHistoryTimeWindow <String>] [-EnableBatchedOperations <Boolean>]
 [-EnableExpress <Boolean>] [-EnableSubscriptionPartitioning <Boolean>]
 [-FilteringMessagesBeforePublishing <Boolean>] [-IsAnonymousAccessible <Boolean>] [-IsExpress <Boolean>]
 [-MaxSizeInMegabytes <Int64>] [-RequiresDuplicateDetection <Boolean>] [-SupportOrdering <Boolean>]
 [-SizeInBytes <Int64>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c1ba7-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c1ba7-105">DESCRIPTION</span></span>
<span data-ttu-id="c1ba7-106">**새 AzureRmServiceBusTopic** cmdlet은 지정 된 service bus 네임 스페이스에 새 service bus 항목을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c1ba7-106">The **New-AzureRmServiceBusTopic** cmdlet creates a new Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="c1ba7-107">예제의</span><span class="sxs-lookup"><span data-stu-id="c1ba7-107">EXAMPLES</span></span>

### <span data-ttu-id="c1ba7-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="c1ba7-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -EnablePartitioning $True
```

<span data-ttu-id="c1ba7-109">`SB-Topic_exampl1`지정 된 Service bus 네임 스페이스에 새 Service bus 항목을 만듭니다 `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="c1ba7-109">Creates a new Service Bus topic `SB-Topic_exampl1` in the specified Service Bus namespace `SB-Example1`.</span></span>

## <span data-ttu-id="c1ba7-110">변수</span><span class="sxs-lookup"><span data-stu-id="c1ba7-110">PARAMETERS</span></span>

### <span data-ttu-id="c1ba7-111">-AutoDeleteOnIdle</span><span class="sxs-lookup"><span data-stu-id="c1ba7-111">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="c1ba7-112">이후 항목이 자동으로 삭제 되는 [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) 유휴 간격을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1ba7-112">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval after which the topic is automatically deleted.</span></span> <span data-ttu-id="c1ba7-113">최소 기간은 5 분입니다.</span><span class="sxs-lookup"><span data-stu-id="c1ba7-113">The minimum duration is 5 minutes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1ba7-114">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="c1ba7-114">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="c1ba7-115">메시지가 서비스 버스에 전송 될 때부터 메시지가 만료 되는 기간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1ba7-115">Specifies the duration after which the message expires, starting from when the message is sent to Service Bus.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1ba7-116">-DuplicateDetectionHistoryTimeWindow</span><span class="sxs-lookup"><span data-stu-id="c1ba7-116">-DuplicateDetectionHistoryTimeWindow</span></span>
<span data-ttu-id="c1ba7-117">중복 검색 기록의 기간을 정의 하는 [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) 구조를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1ba7-117">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) structure that defines the duration of the duplicate detection history.</span></span> <span data-ttu-id="c1ba7-118">기본값은 10 분입니다.</span><span class="sxs-lookup"><span data-stu-id="c1ba7-118">The default value is 10 minutes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1ba7-119">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="c1ba7-119">-EnableBatchedOperations</span></span>
<span data-ttu-id="c1ba7-120">서버 쪽 일괄 처리 된 작업을 사용할 수 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="c1ba7-120">Indicates whether server-side batched operations are enabled.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1ba7-121">-EnableExpress</span><span class="sxs-lookup"><span data-stu-id="c1ba7-121">-EnableExpress</span></span>
<span data-ttu-id="c1ba7-122">Express 엔터티를 사용할 수 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="c1ba7-122">Indicates whether Express Entities are enabled.</span></span> <span data-ttu-id="c1ba7-123">Express 큐는 영구 저장소에 쓰기 전에 메모리의 메시지를 일시적으로 보관 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1ba7-123">An express queue holds a message in memory temporarily before writing it to persistent storage.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1ba7-124">-EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="c1ba7-124">-EnablePartitioning</span></span>
<span data-ttu-id="c1ba7-125">항목을 여러 메시지 브로커에서 분할할 수 있도록 설정할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1ba7-125">Specifies whether to enable the topic to be partitioned across multiple message brokers.</span></span> 

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 
Accepted values: TRUE, FALSE

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1ba7-126">-EnableSubscriptionPartitioning</span><span class="sxs-lookup"><span data-stu-id="c1ba7-126">-EnableSubscriptionPartitioning</span></span>
<span data-ttu-id="c1ba7-127">구독 분할을 사용할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1ba7-127">Specifies whether to enable subscription partitioning.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1ba7-128">-FilteringMessagesBeforePublishing</span><span class="sxs-lookup"><span data-stu-id="c1ba7-128">-FilteringMessagesBeforePublishing</span></span>
<span data-ttu-id="c1ba7-129">게시 하기 전에 메시지에 필터링을 사용할 수 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="c1ba7-129">Indicates whether filtering is enabled for messages before publishing.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1ba7-130">-IsAnonymousAccessible</span><span class="sxs-lookup"><span data-stu-id="c1ba7-130">-IsAnonymousAccessible</span></span>
<span data-ttu-id="c1ba7-131">메시지에서 익명 액세스를 허용 하는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="c1ba7-131">Indicates whether the message allows anonymous access.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1ba7-132">-IsExpress</span><span class="sxs-lookup"><span data-stu-id="c1ba7-132">-IsExpress</span></span>
<span data-ttu-id="c1ba7-133">주제를 표현할 수 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="c1ba7-133">Indicates whether the topic is express enabled.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1ba7-134">-MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="c1ba7-134">-MaxSizeInMegabytes</span></span>
<span data-ttu-id="c1ba7-135">주제에 대 한 최대 크기 (mb)로, 항목에 할당 된 메모리 크기입니다.</span><span class="sxs-lookup"><span data-stu-id="c1ba7-135">The maximum size of the topic in megabytes, which is the size of memory allocated for the topic.</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1ba7-136">-RequiresDuplicateDetection</span><span class="sxs-lookup"><span data-stu-id="c1ba7-136">-RequiresDuplicateDetection</span></span>
<span data-ttu-id="c1ba7-137">주제에 중복 검색이 필요한 지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="c1ba7-137">Indicates whether the topic requires duplication detection.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1ba7-138">-SizeInBytes</span><span class="sxs-lookup"><span data-stu-id="c1ba7-138">-SizeInBytes</span></span>
<span data-ttu-id="c1ba7-139">항목의 크기 (바이트)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1ba7-139">Specifies the size of the topic in bytes.</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1ba7-140">-지원 순서</span><span class="sxs-lookup"><span data-stu-id="c1ba7-140">-SupportOrdering</span></span>
<span data-ttu-id="c1ba7-141">항목이 정렬을 지원 하는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="c1ba7-141">Indicates whether the topic supports ordering.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1ba7-142">-확인</span><span class="sxs-lookup"><span data-stu-id="c1ba7-142">-Confirm</span></span>
<span data-ttu-id="c1ba7-143">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1ba7-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1ba7-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1ba7-144">-WhatIf</span></span>
<span data-ttu-id="c1ba7-145">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c1ba7-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1ba7-146">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c1ba7-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1ba7-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1ba7-147">-DefaultProfile</span></span>
<span data-ttu-id="c1ba7-148">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c1ba7-148">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c1ba7-149">-이름</span><span class="sxs-lookup"><span data-stu-id="c1ba7-149">-Name</span></span>
<span data-ttu-id="c1ba7-150">주제 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c1ba7-150">Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1ba7-151">-Namespace</span><span class="sxs-lookup"><span data-stu-id="c1ba7-151">-Namespace</span></span>
<span data-ttu-id="c1ba7-152">네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c1ba7-152">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1ba7-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1ba7-153">-ResourceGroupName</span></span>
<span data-ttu-id="c1ba7-154">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c1ba7-154">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1ba7-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1ba7-155">CommonParameters</span></span>
<span data-ttu-id="c1ba7-156">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1ba7-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1ba7-157">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1ba7-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1ba7-158">입력</span><span class="sxs-lookup"><span data-stu-id="c1ba7-158">INPUTS</span></span>

### <span data-ttu-id="c1ba7-159">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c1ba7-159">System.String</span></span>
<span data-ttu-id="c1ba7-160">시스템. Nullable \` 1 \[ \[ 시스템 부울, mscorlib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = B77a5c561934e089 \] \] System. Nullable \` 1 \[ \[ System.webserver, mscorlib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = b77a5c561934e089\]\]</span><span class="sxs-lookup"><span data-stu-id="c1ba7-160">System.Nullable\`1\[\[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089\]\] System.Nullable\`1\[\[System.Int64, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089\]\]</span></span>

### <span data-ttu-id="c1ba7-161">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c1ba7-161">-ResourceGroup</span></span>
 <span data-ttu-id="c1ba7-162">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c1ba7-162">System.String</span></span>

### <span data-ttu-id="c1ba7-163">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="c1ba7-163">-NamespaceName</span></span>
 <span data-ttu-id="c1ba7-164">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c1ba7-164">System.String</span></span>

### <span data-ttu-id="c1ba7-165">-TopicName</span><span class="sxs-lookup"><span data-stu-id="c1ba7-165">-TopicName</span></span>
 <span data-ttu-id="c1ba7-166">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c1ba7-166">System.String</span></span>

### <span data-ttu-id="c1ba7-167">-EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="c1ba7-167">-EnablePartitioning</span></span>
 <span data-ttu-id="c1ba7-168">시스템 부울 인가요?</span><span class="sxs-lookup"><span data-stu-id="c1ba7-168">System.Boolean?</span></span>

## <span data-ttu-id="c1ba7-169">출력</span><span class="sxs-lookup"><span data-stu-id="c1ba7-169">OUTPUTS</span></span>

### <span data-ttu-id="c1ba7-170">ServiceBus. TopicAttributes/.</span><span class="sxs-lookup"><span data-stu-id="c1ba7-170">Microsoft.Azure.Commands.ServiceBus.Models.TopicAttributes</span></span>
<span data-ttu-id="c1ba7-171">이름: SB-Topic_exampl1 위치: 서쪽 미국 Id:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/S B-Topic_exampl1 Type: ServiceBus/Topic AccessedAt: AutoDeleteOnIdle: 10675199.02:48:05.4775807 EntityAvailabilityStatus: CreatedAt: 1/20/2017 3:16:42 AM: DefaultMessageTimeToLive 10675199.02:05.4775807: True EnableExpress: False Enableexpress: True DuplicateDetectionHistoryTimeWindow: False EnableBatchedOperations: False EnableSubscriptionPartitioning: false FilteringMessagesBeforePublishing: False MaxSizeInMegabytes: 16384 IsAnonymousAccessible: false, Active Subscriptioninbytes: 0 상태: 활성 구독 개수: SupportOrdering: False IsExpress: 1/20/2017 3:16:43 AM</span><span class="sxs-lookup"><span data-stu-id="c1ba7-171">Name                                : SB-Topic_exampl1 Location                            : West US Id                                  : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/S B-Topic_exampl1 Type                                : Microsoft.ServiceBus/Topic AccessedAt                          : AutoDeleteOnIdle                    : 10675199.02:48:05.4775807 EntityAvailabilityStatus            : CreatedAt                           : 1/20/2017 3:16:42 AM CountDetails                        : DefaultMessageTimeToLive            : 10675199.02:48:05.4775807 DuplicateDetectionHistoryTimeWindow : EnableBatchedOperations             : True EnableExpress                       : False EnablePartitioning                  : True EnableSubscriptionPartitioning      : False FilteringMessagesBeforePublishing   : False IsAnonymousAccessible               : False IsExpress                           : False MaxSizeInMegabytes                  : 16384 RequiresDuplicateDetection          : False SizeInBytes                         : 0 Status                              : Active SubscriptionCount                   : SupportOrdering                     : False UpdatedAt                           : 1/20/2017 3:16:43 AM</span></span>

## <span data-ttu-id="c1ba7-172">상속자</span><span class="sxs-lookup"><span data-stu-id="c1ba7-172">NOTES</span></span>

## <span data-ttu-id="c1ba7-173">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c1ba7-173">RELATED LINKS</span></span>

