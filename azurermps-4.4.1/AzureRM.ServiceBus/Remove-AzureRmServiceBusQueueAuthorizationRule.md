---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusQueueAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusQueueAuthorizationRule.md
ms.openlocfilehash: 93efa23e802c3470d1bd1470cadd0f070cc34422
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529144"
---
# <span data-ttu-id="e06aa-101">Remove-AzureRmServiceBusQueueAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="e06aa-101">Remove-AzureRmServiceBusQueueAuthorizationRule</span></span>

## <span data-ttu-id="e06aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e06aa-102">SYNOPSIS</span></span>
<span data-ttu-id="e06aa-103">지정 된 Service Bus 네임 스페이스에서 큐의 권한 부여 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e06aa-103">Removes the authorization rule of a queue from the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e06aa-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e06aa-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusQueueAuthorizationRule [-ResourceGroup] <String> -Namespace <String> -Queue <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e06aa-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e06aa-105">DESCRIPTION</span></span>
<span data-ttu-id="e06aa-106">**AzureRmServiceBusQueueAuthorizationRule** cmdlet은 지정 된 Service Bus 네임 스페이스에서 큐의 권한 부여 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e06aa-106">The **Remove-AzureRmServiceBusQueueAuthorizationRule** cmdlet removes the authorization rule of a queue from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="e06aa-107">예제의</span><span class="sxs-lookup"><span data-stu-id="e06aa-107">EXAMPLES</span></span>

### <span data-ttu-id="e06aa-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="e06aa-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusQueueAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -AuthorizationRuleName SBAuthoRule1
```

<span data-ttu-id="e06aa-109">`SBAuthoRule1`네임 스페이스에서 큐의 권한 부여 규칙을 제거 합니다 `SB-Queue_exampl1` `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="e06aa-109">Removes the authorization rule `SBAuthoRule1` of the queue `SB-Queue_exampl1` from the namespace `SB-Example1`.</span></span>

## <span data-ttu-id="e06aa-110">변수</span><span class="sxs-lookup"><span data-stu-id="e06aa-110">PARAMETERS</span></span>

### <span data-ttu-id="e06aa-111">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e06aa-111">-ResourceGroup</span></span>
<span data-ttu-id="e06aa-112">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e06aa-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="e06aa-113">-확인</span><span class="sxs-lookup"><span data-stu-id="e06aa-113">-Confirm</span></span>
<span data-ttu-id="e06aa-114">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e06aa-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e06aa-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e06aa-115">-WhatIf</span></span>
<span data-ttu-id="e06aa-116">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e06aa-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e06aa-117">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e06aa-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e06aa-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e06aa-118">-DefaultProfile</span></span>
<span data-ttu-id="e06aa-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e06aa-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e06aa-120">-이름</span><span class="sxs-lookup"><span data-stu-id="e06aa-120">-Name</span></span>
<span data-ttu-id="e06aa-121">큐 AuthorizationRule 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e06aa-121">Queue AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="e06aa-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="e06aa-122">-Namespace</span></span>
<span data-ttu-id="e06aa-123">네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e06aa-123">Namespace Name.</span></span>

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

### <span data-ttu-id="e06aa-124">-큐</span><span class="sxs-lookup"><span data-stu-id="e06aa-124">-Queue</span></span>
<span data-ttu-id="e06aa-125">큐 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e06aa-125">Queue Name.</span></span>

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

### <span data-ttu-id="e06aa-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e06aa-126">CommonParameters</span></span>
<span data-ttu-id="e06aa-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e06aa-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e06aa-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e06aa-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e06aa-129">입력</span><span class="sxs-lookup"><span data-stu-id="e06aa-129">INPUTS</span></span>

### <span data-ttu-id="e06aa-130">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e06aa-130">-ResourceGroup</span></span>
 <span data-ttu-id="e06aa-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e06aa-131">System.String</span></span>

### <span data-ttu-id="e06aa-132">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="e06aa-132">-NamespaceName</span></span>
 <span data-ttu-id="e06aa-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e06aa-133">System.String</span></span>

### <span data-ttu-id="e06aa-134">-QueueName</span><span class="sxs-lookup"><span data-stu-id="e06aa-134">-QueueName</span></span>
 <span data-ttu-id="e06aa-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e06aa-135">System.String</span></span>

### <span data-ttu-id="e06aa-136">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="e06aa-136">-AuthorizationRuleName</span></span>
 <span data-ttu-id="e06aa-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e06aa-137">System.String</span></span>

## <span data-ttu-id="e06aa-138">출력</span><span class="sxs-lookup"><span data-stu-id="e06aa-138">OUTPUTS</span></span>

### <span data-ttu-id="e06aa-139">System. 개체</span><span class="sxs-lookup"><span data-stu-id="e06aa-139">System.Object</span></span>

## <span data-ttu-id="e06aa-140">상속자</span><span class="sxs-lookup"><span data-stu-id="e06aa-140">NOTES</span></span>

## <span data-ttu-id="e06aa-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e06aa-141">RELATED LINKS</span></span>

