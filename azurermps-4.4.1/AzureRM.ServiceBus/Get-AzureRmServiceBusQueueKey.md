---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusQueueKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusQueueKey.md
ms.openlocfilehash: 4faca15a0c348ee1011789db5acd227c06ee1b85
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533839"
---
# <span data-ttu-id="adac4-101">Get-AzureRmServiceBusQueueKey</span><span class="sxs-lookup"><span data-stu-id="adac4-101">Get-AzureRmServiceBusQueueKey</span></span>

## <span data-ttu-id="adac4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="adac4-102">SYNOPSIS</span></span>
<span data-ttu-id="adac4-103">지정 된 Service Bus 큐에 대 한 기본 및 보조 연결 문자열을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="adac4-103">Gets the primary and secondary connection strings for the given Service Bus queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="adac4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="adac4-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusQueueKey [-ResourceGroup] <String> -Namespace <String> -Queue <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="adac4-105">설명은</span><span class="sxs-lookup"><span data-stu-id="adac4-105">DESCRIPTION</span></span>
<span data-ttu-id="adac4-106">**AzureRmServiceBusQueueKey** cmdlet은 지정 된 Service Bus 큐에 대 한 기본 및 보조 연결 문자열을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="adac4-106">The **Get-AzureRmServiceBusQueueKey** cmdlet returns the primary and secondary connection strings for the given Service Bus queue.</span></span> 

## <span data-ttu-id="adac4-107">예제의</span><span class="sxs-lookup"><span data-stu-id="adac4-107">EXAMPLES</span></span>

### <span data-ttu-id="adac4-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="adac4-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusQueueKey -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -AuthorizationRuleName SBAuthoRule1
```

<span data-ttu-id="adac4-109">지정 된 Service Bus 큐에 대 한 기본 및 보조 연결 문자열을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="adac4-109">Returns the primary and secondary connection strings for the specified Service Bus queue.</span></span>

## <span data-ttu-id="adac4-110">변수</span><span class="sxs-lookup"><span data-stu-id="adac4-110">PARAMETERS</span></span>

### <span data-ttu-id="adac4-111">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="adac4-111">-ResourceGroup</span></span>
<span data-ttu-id="adac4-112">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="adac4-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="adac4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adac4-113">-DefaultProfile</span></span>
<span data-ttu-id="adac4-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="adac4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="adac4-115">-이름</span><span class="sxs-lookup"><span data-stu-id="adac4-115">-Name</span></span>
<span data-ttu-id="adac4-116">ServiceBus 대기열 AuthorizationRule 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="adac4-116">ServiceBus Queue AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="adac4-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="adac4-117">-Namespace</span></span>
<span data-ttu-id="adac4-118">ServiceBus 네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="adac4-118">ServiceBus Namespace Name.</span></span>

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

### <span data-ttu-id="adac4-119">-큐</span><span class="sxs-lookup"><span data-stu-id="adac4-119">-Queue</span></span>
<span data-ttu-id="adac4-120">ServiceBus 대기열 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="adac4-120">ServiceBus Queue Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: QueueName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="adac4-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adac4-121">CommonParameters</span></span>
<span data-ttu-id="adac4-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="adac4-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adac4-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="adac4-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adac4-124">입력</span><span class="sxs-lookup"><span data-stu-id="adac4-124">INPUTS</span></span>

### <span data-ttu-id="adac4-125">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="adac4-125">-ResourceGroup</span></span>
 <span data-ttu-id="adac4-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="adac4-126">System.String</span></span>
 

### <span data-ttu-id="adac4-127">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="adac4-127">-NamespaceName</span></span>
 <span data-ttu-id="adac4-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="adac4-128">System.String</span></span>
 

### <span data-ttu-id="adac4-129">-QueueName</span><span class="sxs-lookup"><span data-stu-id="adac4-129">-QueueName</span></span>
 <span data-ttu-id="adac4-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="adac4-130">System.String</span></span>
 

### <span data-ttu-id="adac4-131">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="adac4-131">-AuthorizationRuleName</span></span>
 <span data-ttu-id="adac4-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="adac4-132">System.String</span></span>

## <span data-ttu-id="adac4-133">출력</span><span class="sxs-lookup"><span data-stu-id="adac4-133">OUTPUTS</span></span>

### <span data-ttu-id="adac4-134">ServiceBus. ListKeysAttributes/.</span><span class="sxs-lookup"><span data-stu-id="adac4-134">Microsoft.Azure.Commands.ServiceBus.Models.ListKeysAttributes</span></span>
<span data-ttu-id="adac4-135">PrimaryConnectionString: 끝점 = sb://sb-example1.servicebus.windows.net/; SharedAccessKeyName = SBAuthoRule1 SharedAccessKey = {SharedAccessKey-value} EntityPath = SB-Queue_e xampl1 SecondaryConnectionString: Endpoint = SB://sb-example1.servicebus.windows.net/; SharedAccessKeyName = SBAuthoRule1 SharedAccessKey = {SharedAccessKey-value} EntityPath = SB-Queue_e xampl1 PrimaryKey: {PrimaryKey 값} SecondaryKey: {SecondaryKey 값} KeyName: SBAuthoRule1</span><span class="sxs-lookup"><span data-stu-id="adac4-135">PrimaryConnectionString   : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=SBAuthoRule1;SharedAccessKey={SharedAccessKey-value};EntityPath=SB-Queue_e xampl1 SecondaryConnectionString : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=SBAuthoRule1;SharedAccessKey={SharedAccessKey-value};EntityPath=SB-Queue_e xampl1 PrimaryKey                : {PrimaryKey value} SecondaryKey              : {SecondaryKey value} KeyName                   : SBAuthoRule1</span></span>

## <span data-ttu-id="adac4-136">상속자</span><span class="sxs-lookup"><span data-stu-id="adac4-136">NOTES</span></span>

## <span data-ttu-id="adac4-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="adac4-137">RELATED LINKS</span></span>

