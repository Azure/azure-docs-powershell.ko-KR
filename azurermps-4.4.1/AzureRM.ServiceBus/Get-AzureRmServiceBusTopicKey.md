---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusTopicKey.md
ms.openlocfilehash: 24041c299f2f242126f265ad232db3e0c5d526b0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93535435"
---
# <span data-ttu-id="afe01-101">Get-AzureRmServiceBusTopicKey</span><span class="sxs-lookup"><span data-stu-id="afe01-101">Get-AzureRmServiceBusTopicKey</span></span>

## <span data-ttu-id="afe01-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="afe01-102">SYNOPSIS</span></span>
<span data-ttu-id="afe01-103">Service Bus 항목에 대 한 기본 및 보조 연결 문자열을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="afe01-103">Gets the primary and secondary connection strings for the Service Bus topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="afe01-104">구문과</span><span class="sxs-lookup"><span data-stu-id="afe01-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusTopicKey [-ResourceGroup] <String> -Namespace <String> -Topic <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="afe01-105">설명은</span><span class="sxs-lookup"><span data-stu-id="afe01-105">DESCRIPTION</span></span>
<span data-ttu-id="afe01-106">**AzureRmServiceBusTopicKey** cmdlet은 지정 된 Service Bus 항목에 대 한 기본 및 보조 연결 문자열을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="afe01-106">The **Get-AzureRmServiceBusTopicKey** cmdlet returns the primary and secondary connection strings for the given Service Bus topic.</span></span>

## <span data-ttu-id="afe01-107">예제의</span><span class="sxs-lookup"><span data-stu-id="afe01-107">EXAMPLES</span></span>

### <span data-ttu-id="afe01-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="afe01-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusTopicKey -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -AuthorizationRuleName SBTopicAuthoRule1
```

<span data-ttu-id="afe01-109">지정 된 Service Bus 주제에 대 한 기본 및 보조 연결 문자열을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="afe01-109">Returns the primary and secondary connection strings for the specified Service Bus topic.</span></span>

## <span data-ttu-id="afe01-110">변수</span><span class="sxs-lookup"><span data-stu-id="afe01-110">PARAMETERS</span></span>

### <span data-ttu-id="afe01-111">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="afe01-111">-ResourceGroup</span></span>
<span data-ttu-id="afe01-112">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="afe01-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="afe01-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afe01-113">-DefaultProfile</span></span>
<span data-ttu-id="afe01-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="afe01-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="afe01-115">-이름</span><span class="sxs-lookup"><span data-stu-id="afe01-115">-Name</span></span>
<span data-ttu-id="afe01-116">주제 AuthorizationRule 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="afe01-116">Topic AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="afe01-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="afe01-117">-Namespace</span></span>
<span data-ttu-id="afe01-118">네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="afe01-118">Namespace Name.</span></span>

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

### <span data-ttu-id="afe01-119">-주제</span><span class="sxs-lookup"><span data-stu-id="afe01-119">-Topic</span></span>
<span data-ttu-id="afe01-120">주제 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="afe01-120">Topic Name.</span></span>

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

### <span data-ttu-id="afe01-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afe01-121">CommonParameters</span></span>
<span data-ttu-id="afe01-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="afe01-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afe01-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="afe01-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afe01-124">입력</span><span class="sxs-lookup"><span data-stu-id="afe01-124">INPUTS</span></span>

### <span data-ttu-id="afe01-125">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="afe01-125">-ResourceGroup</span></span>
 <span data-ttu-id="afe01-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="afe01-126">System.String</span></span>
 

### <span data-ttu-id="afe01-127">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="afe01-127">-NamespaceName</span></span>
 <span data-ttu-id="afe01-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="afe01-128">System.String</span></span>
 

### <span data-ttu-id="afe01-129">-TopicName</span><span class="sxs-lookup"><span data-stu-id="afe01-129">-TopicName</span></span>
 <span data-ttu-id="afe01-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="afe01-130">System.String</span></span>
 

### <span data-ttu-id="afe01-131">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="afe01-131">-AuthorizationRuleName</span></span>
 <span data-ttu-id="afe01-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="afe01-132">System.String</span></span>

## <span data-ttu-id="afe01-133">출력</span><span class="sxs-lookup"><span data-stu-id="afe01-133">OUTPUTS</span></span>

### <span data-ttu-id="afe01-134">ServiceBus. ListKeysAttributes/.</span><span class="sxs-lookup"><span data-stu-id="afe01-134">Microsoft.Azure.Commands.ServiceBus.Models.ListKeysAttributes</span></span>
<span data-ttu-id="afe01-135">PrimaryConnectionString: 끝점 = sb://sb-example1.servicebus.windows.net/; SharedAccessKeyName = SBTopicAuthoRule1 SharedAccessKey = {SharedAccessKey-value} EntityPath = SB-pic_exampl1 SecondaryConnectionString: Endpoint = sb://sb-example1.servicebus.windows.net/; SharedAccessKeyName = SBTopicAuthoRule1 SharedAccessKey = {SharedAccessKey-value} EntityPath = SB-pic_exampl1 PrimaryKey: {PrimaryKey 값} SecondaryKey: {SecondaryKey 값} KeyName: SBTopicAuthoRule1</span><span class="sxs-lookup"><span data-stu-id="afe01-135">PrimaryConnectionString   : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=SBTopicAuthoRule1;SharedAccessKey={SharedAccessKey-value};EntityPath=SB-To pic_exampl1 SecondaryConnectionString : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=SBTopicAuthoRule1;SharedAccessKey={SharedAccessKey-value};EntityPath=SB-To pic_exampl1 PrimaryKey                : {PrimaryKey value} SecondaryKey              : {SecondaryKey value} KeyName                   : SBTopicAuthoRule1</span></span>

## <span data-ttu-id="afe01-136">상속자</span><span class="sxs-lookup"><span data-stu-id="afe01-136">NOTES</span></span>

## <span data-ttu-id="afe01-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="afe01-137">RELATED LINKS</span></span>

