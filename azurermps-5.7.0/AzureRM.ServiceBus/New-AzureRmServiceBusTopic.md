---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/new-azurermservicebustopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusTopic.md
ms.openlocfilehash: a79afdbba1293c3340e499387b5df745d8b76228
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702838"
---
# <span data-ttu-id="22984-101">New-AzureRmServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="22984-101">New-AzureRmServiceBusTopic</span></span>

## <span data-ttu-id="22984-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22984-102">SYNOPSIS</span></span>
<span data-ttu-id="22984-103">지정 된 Service Bus 네임 스페이스에 새 Service Bus 항목을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="22984-103">Creates a new Service Bus topic in  the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="22984-104">구문과</span><span class="sxs-lookup"><span data-stu-id="22984-104">SYNTAX</span></span>

```
New-AzureRmServiceBusTopic [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -EnablePartitioning <Boolean> [-AutoDeleteOnIdle <String>] [-DefaultMessageTimeToLive <String>]
 [-DuplicateDetectionHistoryTimeWindow <String>] [-EnableBatchedOperations <Boolean>]
 [-EnableExpress <Boolean>] [-MaxSizeInMegabytes <Int64>] [-RequiresDuplicateDetection <Boolean>]
 [-SupportOrdering <Boolean>] [-SizeInBytes <Int64>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22984-105">설명은</span><span class="sxs-lookup"><span data-stu-id="22984-105">DESCRIPTION</span></span>
<span data-ttu-id="22984-106">**새 AzureRmServiceBusTopic** cmdlet은 지정 된 service bus 네임 스페이스에 새 service bus 항목을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="22984-106">The **New-AzureRmServiceBusTopic** cmdlet creates a new Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="22984-107">예제의</span><span class="sxs-lookup"><span data-stu-id="22984-107">EXAMPLES</span></span>

### <span data-ttu-id="22984-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="22984-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -EnablePartitioning $True

Name                                : SB-Topic_exampl1
Id                                  : /subscriptions/{subscription id}/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/S
                                      B-Topic_exampl1
Type                                : Microsoft.ServiceBus/Topic
AccessedAt                          : 
AutoDeleteOnIdle                    : 10675199.02:48:05.4775807
CreatedAt                           : 1/20/2017 3:16:42 AM
CountDetails                        : 
DefaultMessageTimeToLive            : 10675199.02:48:05.4775807
DuplicateDetectionHistoryTimeWindow : 
EnableBatchedOperations             : True
EnableExpress                       : False
EnablePartitioning                  : True
MaxSizeInMegabytes                  : 16384
RequiresDuplicateDetection          : False
SizeInBytes                         : 0
Status                              : Active
SubscriptionCount                   : 
SupportOrdering                     : False
UpdatedAt                           : 1/20/2017 3:16:43 AM

```
<span data-ttu-id="22984-109">`SB-Topic_exampl1`지정 된 Service bus 네임 스페이스에 새 Service bus 항목을 만듭니다 `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="22984-109">Creates a new Service Bus topic `SB-Topic_exampl1` in the specified Service Bus namespace `SB-Example1`.</span></span>

## <span data-ttu-id="22984-110">변수</span><span class="sxs-lookup"><span data-stu-id="22984-110">PARAMETERS</span></span>

### <span data-ttu-id="22984-111">-AutoDeleteOnIdle</span><span class="sxs-lookup"><span data-stu-id="22984-111">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="22984-112">이후 항목이 자동으로 삭제 되는 [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) 유휴 간격을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="22984-112">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval after which the topic is automatically deleted.</span></span> <span data-ttu-id="22984-113">최소 기간은 5 분입니다.</span><span class="sxs-lookup"><span data-stu-id="22984-113">The minimum duration is 5 minutes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22984-114">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="22984-114">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="22984-115">메시지가 서비스 버스에 전송 될 때부터 메시지가 만료 되는 기간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="22984-115">Specifies the duration after which the message expires, starting from when the message is sent to Service Bus.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22984-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22984-116">-DefaultProfile</span></span>
<span data-ttu-id="22984-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="22984-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="22984-118">-DuplicateDetectionHistoryTimeWindow</span><span class="sxs-lookup"><span data-stu-id="22984-118">-DuplicateDetectionHistoryTimeWindow</span></span>
<span data-ttu-id="22984-119">중복 검색 기록의 기간을 정의 하는 [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) 구조를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="22984-119">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) structure that defines the duration of the duplicate detection history.</span></span> <span data-ttu-id="22984-120">기본값은 10 분입니다.</span><span class="sxs-lookup"><span data-stu-id="22984-120">The default value is 10 minutes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22984-121">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="22984-121">-EnableBatchedOperations</span></span>
<span data-ttu-id="22984-122">서버 쪽 일괄 처리 된 작업을 사용할 수 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="22984-122">Indicates whether server-side batched operations are enabled.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22984-123">-EnableExpress</span><span class="sxs-lookup"><span data-stu-id="22984-123">-EnableExpress</span></span>
<span data-ttu-id="22984-124">Express 엔터티를 사용할 수 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="22984-124">Indicates whether Express Entities are enabled.</span></span> <span data-ttu-id="22984-125">Express 큐는 영구 저장소에 쓰기 전에 메모리의 메시지를 일시적으로 보관 합니다.</span><span class="sxs-lookup"><span data-stu-id="22984-125">An express queue holds a message in memory temporarily before writing it to persistent storage.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22984-126">-EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="22984-126">-EnablePartitioning</span></span>
<span data-ttu-id="22984-127">항목을 여러 메시지 브로커에서 분할할 수 있도록 설정할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="22984-127">Specifies whether to enable the topic to be partitioned across multiple message brokers.</span></span> 

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 
Accepted values: TRUE, FALSE

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22984-128">-MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="22984-128">-MaxSizeInMegabytes</span></span>
<span data-ttu-id="22984-129">주제에 대 한 최대 크기 (mb)로, 항목에 할당 된 메모리 크기입니다.</span><span class="sxs-lookup"><span data-stu-id="22984-129">The maximum size of the topic in megabytes, which is the size of memory allocated for the topic.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22984-130">-이름</span><span class="sxs-lookup"><span data-stu-id="22984-130">-Name</span></span>
<span data-ttu-id="22984-131">주제 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="22984-131">Topic Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22984-132">-Namespace</span><span class="sxs-lookup"><span data-stu-id="22984-132">-Namespace</span></span>
<span data-ttu-id="22984-133">네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="22984-133">Namespace Name.</span></span>

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

### <span data-ttu-id="22984-134">-RequiresDuplicateDetection</span><span class="sxs-lookup"><span data-stu-id="22984-134">-RequiresDuplicateDetection</span></span>
<span data-ttu-id="22984-135">주제에 중복 검색이 필요한 지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="22984-135">Indicates whether the topic requires duplication detection.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22984-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22984-136">-ResourceGroupName</span></span>
<span data-ttu-id="22984-137">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="22984-137">The name of the resource group</span></span>

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

### <span data-ttu-id="22984-138">-SizeInBytes</span><span class="sxs-lookup"><span data-stu-id="22984-138">-SizeInBytes</span></span>
<span data-ttu-id="22984-139">항목의 크기 (바이트)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="22984-139">Specifies the size of the topic in bytes.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22984-140">-지원 순서</span><span class="sxs-lookup"><span data-stu-id="22984-140">-SupportOrdering</span></span>
<span data-ttu-id="22984-141">항목이 정렬을 지원 하는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="22984-141">Indicates whether the topic supports ordering.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22984-142">-확인</span><span class="sxs-lookup"><span data-stu-id="22984-142">-Confirm</span></span>
<span data-ttu-id="22984-143">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="22984-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22984-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22984-144">-WhatIf</span></span>
<span data-ttu-id="22984-145">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="22984-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22984-146">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="22984-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22984-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22984-147">CommonParameters</span></span>
<span data-ttu-id="22984-148">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="22984-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22984-149">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22984-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22984-150">입력</span><span class="sxs-lookup"><span data-stu-id="22984-150">INPUTS</span></span>

### <span data-ttu-id="22984-151">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="22984-151">System.String</span></span>
<span data-ttu-id="22984-152">시스템. Nullable \` 1 \[ \[ 시스템 부울, mscorlib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = B77a5c561934e089 \] \] System. Nullable \` 1 \[ \[ System.webserver, mscorlib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = b77a5c561934e089\]\]</span><span class="sxs-lookup"><span data-stu-id="22984-152">System.Nullable\`1\[\[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089\]\] System.Nullable\`1\[\[System.Int64, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089\]\]</span></span>

### <span data-ttu-id="22984-153">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="22984-153">-ResourceGroup</span></span>
 <span data-ttu-id="22984-154">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="22984-154">System.String</span></span>

### <span data-ttu-id="22984-155">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="22984-155">-NamespaceName</span></span>
 <span data-ttu-id="22984-156">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="22984-156">System.String</span></span>

### <span data-ttu-id="22984-157">-TopicName</span><span class="sxs-lookup"><span data-stu-id="22984-157">-TopicName</span></span>
 <span data-ttu-id="22984-158">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="22984-158">System.String</span></span>

### <span data-ttu-id="22984-159">-EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="22984-159">-EnablePartitioning</span></span>
 <span data-ttu-id="22984-160">시스템 부울 인가요?</span><span class="sxs-lookup"><span data-stu-id="22984-160">System.Boolean?</span></span>

## <span data-ttu-id="22984-161">출력</span><span class="sxs-lookup"><span data-stu-id="22984-161">OUTPUTS</span></span>

### <span data-ttu-id="22984-162">ServiceBus. a. m/.Ppstop특성</span><span class="sxs-lookup"><span data-stu-id="22984-162">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="22984-163">상속자</span><span class="sxs-lookup"><span data-stu-id="22984-163">NOTES</span></span>

## <span data-ttu-id="22984-164">관련 링크</span><span class="sxs-lookup"><span data-stu-id="22984-164">RELATED LINKS</span></span>

