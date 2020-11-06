---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusQueue.md
ms.openlocfilehash: 8c5c614a041ff0e4ab9bc4fdc0aea944901d1efc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529143"
---
# <span data-ttu-id="6b4eb-101">Remove-AzureRmServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="6b4eb-101">Remove-AzureRmServiceBusQueue</span></span>

## <span data-ttu-id="6b4eb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b4eb-102">SYNOPSIS</span></span>
<span data-ttu-id="6b4eb-103">지정 된 Service Bus 네임 스페이스에서 큐를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b4eb-103">Removes the queue from the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6b4eb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6b4eb-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusQueue -ResourceGroupName <String> -Namespace <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b4eb-105">설명은</span><span class="sxs-lookup"><span data-stu-id="6b4eb-105">DESCRIPTION</span></span>
<span data-ttu-id="6b4eb-106">**AzureRmServiceBusQueue** cmdlet은 지정 된 Service Bus 네임 스페이스에서 큐를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b4eb-106">The **Remove-AzureRmServiceBusQueue** cmdlet removes the queue from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="6b4eb-107">예제의</span><span class="sxs-lookup"><span data-stu-id="6b4eb-107">EXAMPLES</span></span>

### <span data-ttu-id="6b4eb-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="6b4eb-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1
```

<span data-ttu-id="6b4eb-109">`SB-Queue_exampl1`네임 스페이스에서 큐를 제거 `SB-Example1` 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b4eb-109">Removes the queue `SB-Queue_exampl1` from the namespace `SB-Example1`.</span></span>

## <span data-ttu-id="6b4eb-110">변수</span><span class="sxs-lookup"><span data-stu-id="6b4eb-110">PARAMETERS</span></span>

### <span data-ttu-id="6b4eb-111">-확인</span><span class="sxs-lookup"><span data-stu-id="6b4eb-111">-Confirm</span></span>
<span data-ttu-id="6b4eb-112">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b4eb-112">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b4eb-113">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b4eb-113">-WhatIf</span></span>
<span data-ttu-id="6b4eb-114">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6b4eb-114">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b4eb-115">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6b4eb-115">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b4eb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b4eb-116">-DefaultProfile</span></span>
<span data-ttu-id="6b4eb-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6b4eb-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6b4eb-118">-이름</span><span class="sxs-lookup"><span data-stu-id="6b4eb-118">-Name</span></span>
<span data-ttu-id="6b4eb-119">큐 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6b4eb-119">Queue Name.</span></span>

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

### <span data-ttu-id="6b4eb-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="6b4eb-120">-Namespace</span></span>
<span data-ttu-id="6b4eb-121">네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6b4eb-121">Namespace Name.</span></span>

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

### <span data-ttu-id="6b4eb-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b4eb-122">-ResourceGroupName</span></span>
<span data-ttu-id="6b4eb-123">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6b4eb-123">The name of the resource group</span></span>

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

### <span data-ttu-id="6b4eb-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b4eb-124">CommonParameters</span></span>
<span data-ttu-id="6b4eb-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b4eb-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b4eb-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b4eb-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b4eb-127">입력</span><span class="sxs-lookup"><span data-stu-id="6b4eb-127">INPUTS</span></span>

### <span data-ttu-id="6b4eb-128">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6b4eb-128">-ResourceGroup</span></span>
 <span data-ttu-id="6b4eb-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="6b4eb-129">System.String</span></span>

### <span data-ttu-id="6b4eb-130">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="6b4eb-130">-NamespaceName</span></span>
 <span data-ttu-id="6b4eb-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="6b4eb-131">System.String</span></span>

### <span data-ttu-id="6b4eb-132">-QueueName</span><span class="sxs-lookup"><span data-stu-id="6b4eb-132">-QueueName</span></span>
 <span data-ttu-id="6b4eb-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="6b4eb-133">System.String</span></span>

## <span data-ttu-id="6b4eb-134">출력</span><span class="sxs-lookup"><span data-stu-id="6b4eb-134">OUTPUTS</span></span>

### <span data-ttu-id="6b4eb-135">System. 개체</span><span class="sxs-lookup"><span data-stu-id="6b4eb-135">System.Object</span></span>

## <span data-ttu-id="6b4eb-136">상속자</span><span class="sxs-lookup"><span data-stu-id="6b4eb-136">NOTES</span></span>

## <span data-ttu-id="6b4eb-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6b4eb-137">RELATED LINKS</span></span>

