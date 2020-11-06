---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/set-azurermeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubConsumerGroup.md
ms.openlocfilehash: 52038de3d0bb8f07fdfe5abf0978e306a1959a94
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530336"
---
# <span data-ttu-id="0583a-101">Set-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="0583a-101">Set-AzureRmEventHubConsumerGroup</span></span>

## <span data-ttu-id="0583a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0583a-102">SYNOPSIS</span></span>
<span data-ttu-id="0583a-103">지정 된 이벤트 허브 소비자 그룹을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="0583a-103">Updates the specified Event Hubs consumer group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0583a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0583a-104">SYNTAX</span></span>

```
Set-AzureRmEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [[-UserMetadata] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0583a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0583a-105">DESCRIPTION</span></span>
<span data-ttu-id="0583a-106">Set-AzureRmEventHubConsumerGroup cmdlet은 지정 된 이벤트 허브 소비자 그룹을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="0583a-106">The Set-AzureRmEventHubConsumerGroup cmdlet updates the specified Event Hubs consumer group.</span></span>

## <span data-ttu-id="0583a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="0583a-107">EXAMPLES</span></span>

### <span data-ttu-id="0583a-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="0583a-108">Example 1</span></span>
```
PS C:\> Set-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName -UserMetadata "Testing"
```

<span data-ttu-id="0583a-109">소비자 그룹 MyConsumerGroupName의 사용자 메타 데이터 \` \` 를 "테스트"로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0583a-109">Sets the user metadata of the consumer group \`MyConsumerGroupName\` to "Testing."</span></span>

## <span data-ttu-id="0583a-110">변수</span><span class="sxs-lookup"><span data-stu-id="0583a-110">PARAMETERS</span></span>

### <span data-ttu-id="0583a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0583a-111">-DefaultProfile</span></span>
<span data-ttu-id="0583a-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0583a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0583a-113">-EventHub</span><span class="sxs-lookup"><span data-stu-id="0583a-113">-EventHub</span></span>
<span data-ttu-id="0583a-114">EventHub 이름</span><span class="sxs-lookup"><span data-stu-id="0583a-114">EventHub Name</span></span>

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

### <span data-ttu-id="0583a-115">-이름</span><span class="sxs-lookup"><span data-stu-id="0583a-115">-Name</span></span>
<span data-ttu-id="0583a-116">ConsumerGroup 이름</span><span class="sxs-lookup"><span data-stu-id="0583a-116">ConsumerGroup Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ConsumerGroupName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0583a-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="0583a-117">-Namespace</span></span>
<span data-ttu-id="0583a-118">네임 스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="0583a-118">Namespace Name</span></span>

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

### <span data-ttu-id="0583a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0583a-119">-ResourceGroupName</span></span>
<span data-ttu-id="0583a-120">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="0583a-120">Resource Group Name</span></span>

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

### <span data-ttu-id="0583a-121">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="0583a-121">-UserMetadata</span></span>
<span data-ttu-id="0583a-122">ConsumerGroup에 대 한 사용자 메타 데이터</span><span class="sxs-lookup"><span data-stu-id="0583a-122">User Metadata for ConsumerGroup</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0583a-123">-확인</span><span class="sxs-lookup"><span data-stu-id="0583a-123">-Confirm</span></span>
<span data-ttu-id="0583a-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0583a-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0583a-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0583a-125">-WhatIf</span></span>
<span data-ttu-id="0583a-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0583a-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0583a-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0583a-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0583a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0583a-128">CommonParameters</span></span>
<span data-ttu-id="0583a-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0583a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0583a-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0583a-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0583a-131">입력</span><span class="sxs-lookup"><span data-stu-id="0583a-131">INPUTS</span></span>

### <span data-ttu-id="0583a-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0583a-132">System.String</span></span>

## <span data-ttu-id="0583a-133">출력</span><span class="sxs-lookup"><span data-stu-id="0583a-133">OUTPUTS</span></span>

### <span data-ttu-id="0583a-134">PSConsumerGroupAttributes (.).</span><span class="sxs-lookup"><span data-stu-id="0583a-134">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>

## <span data-ttu-id="0583a-135">상속자</span><span class="sxs-lookup"><span data-stu-id="0583a-135">NOTES</span></span>

## <span data-ttu-id="0583a-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0583a-136">RELATED LINKS</span></span>
