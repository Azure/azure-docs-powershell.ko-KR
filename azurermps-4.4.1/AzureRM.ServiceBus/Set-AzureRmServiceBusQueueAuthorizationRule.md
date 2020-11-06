---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusQueueAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusQueueAuthorizationRule.md
ms.openlocfilehash: 166b47a231b2ca6fc2cf74137212e60123f25445
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536172"
---
# <span data-ttu-id="ec282-101">Set-AzureRmServiceBusQueueAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="ec282-101">Set-AzureRmServiceBusQueueAuthorizationRule</span></span>

## <span data-ttu-id="ec282-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec282-102">SYNOPSIS</span></span>
<span data-ttu-id="ec282-103">지정 된 Service Bus 큐에 대해 지정한 권한 부여 규칙 설명을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec282-103">Updates the specified authorization rule description for the given Service Bus queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ec282-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ec282-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusQueueAuthorizationRule [-ResourceGroup] <String> [-NamespaceName] <String>
 [-QueueName] <String> [-AuthRuleObj] <SharedAccessAuthorizationRuleAttributes>
 [[-AuthorizationRuleName] <String>] [[-Rights] <String[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec282-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ec282-105">DESCRIPTION</span></span>
<span data-ttu-id="ec282-106">**Set-AzureRmServiceBusQueueAuthorizationRule** cmdlet은 지정 된 Service Bus 큐에 대 한 설명을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec282-106">The **Set-AzureRmServiceBusQueueAuthorizationRule** cmdlet updates the description for the specified authorization rule of the given Service Bus queue.</span></span>

## <span data-ttu-id="ec282-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ec282-107">EXAMPLES</span></span>

### <span data-ttu-id="ec282-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="ec282-108">Example 1</span></span>
```
PS C:\> $authRuleObj = Get-AzureRmServiceBusQueueAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -AuthorizationRuleName SBAuthoRule1

PS C:\> $authRuleObj.Rights.Add("Manage")

PS C:\> Set-AzureRmServiceBusQueueAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -AuthRuleObj $authRuleObj
```

<span data-ttu-id="ec282-109">큐의 권한 부여 규칙에 대 한 액세스 권한에 대 한 **관리** 를 추가 합니다 `SBAuthoRule1` `SB-Queue_exampl1` .</span><span class="sxs-lookup"><span data-stu-id="ec282-109">Adds **Manage** to the access rights of the authorization rule `SBAuthoRule1` of the queue `SB-Queue_exampl1`.</span></span>

## <span data-ttu-id="ec282-110">변수</span><span class="sxs-lookup"><span data-stu-id="ec282-110">PARAMETERS</span></span>

### <span data-ttu-id="ec282-111">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="ec282-111">-AuthorizationRuleName</span></span>
<span data-ttu-id="ec282-112">인증 규칙 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ec282-112">The authorization rule name.</span></span> <span data-ttu-id="ec282-113">**-Authruleobj** 가 지정 되지 않은 경우 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec282-113">Required if **-AuthruleObj** is not specified.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec282-114">-AuthRuleObj</span><span class="sxs-lookup"><span data-stu-id="ec282-114">-AuthRuleObj</span></span>
<span data-ttu-id="ec282-115">Service Bus 큐 권한 부여 규칙 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="ec282-115">The Service Bus queue authorization rule object.</span></span>

```yaml
Type: SharedAccessAuthorizationRuleAttributes
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec282-116">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="ec282-116">-NamespaceName</span></span>
<span data-ttu-id="ec282-117">Service Bus 네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ec282-117">The Service Bus namespace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec282-118">-QueueName</span><span class="sxs-lookup"><span data-stu-id="ec282-118">-QueueName</span></span>
<span data-ttu-id="ec282-119">Service Bus 큐 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ec282-119">The Service Bus queue name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec282-120">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ec282-120">-ResourceGroup</span></span>
<span data-ttu-id="ec282-121">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ec282-121">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec282-122">-권한</span><span class="sxs-lookup"><span data-stu-id="ec282-122">-Rights</span></span>
<span data-ttu-id="ec282-123">권한을 부여 합니다. 예를 들어 @ ("듣기", "Send", "관리").</span><span class="sxs-lookup"><span data-stu-id="ec282-123">The rights; for example @("Listen","Send","Manage").</span></span> <span data-ttu-id="ec282-124">' AuthruleObj '가 지정 되지 않은 경우 필수 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="ec282-124">Required if 'AuthruleObj' not specified.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec282-125">-확인</span><span class="sxs-lookup"><span data-stu-id="ec282-125">-Confirm</span></span>
<span data-ttu-id="ec282-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec282-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec282-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec282-127">-WhatIf</span></span>
<span data-ttu-id="ec282-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ec282-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec282-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ec282-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec282-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec282-130">CommonParameters</span></span>
<span data-ttu-id="ec282-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec282-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec282-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec282-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec282-133">입력</span><span class="sxs-lookup"><span data-stu-id="ec282-133">INPUTS</span></span>

### <span data-ttu-id="ec282-134">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ec282-134">-ResourceGroup</span></span>
 <span data-ttu-id="ec282-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ec282-135">System.String</span></span>

### <span data-ttu-id="ec282-136">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="ec282-136">-NamespaceName</span></span>
 <span data-ttu-id="ec282-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ec282-137">System.String</span></span>

### <span data-ttu-id="ec282-138">-QueueName</span><span class="sxs-lookup"><span data-stu-id="ec282-138">-QueueName</span></span>
 <span data-ttu-id="ec282-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ec282-139">System.String</span></span>

### <span data-ttu-id="ec282-140">-AuthRuleObj</span><span class="sxs-lookup"><span data-stu-id="ec282-140">-AuthRuleObj</span></span>
 <span data-ttu-id="ec282-141">ServiceBus. SharedAccessAuthorizationRuleAttributes 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ec282-141">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="ec282-142">출력</span><span class="sxs-lookup"><span data-stu-id="ec282-142">OUTPUTS</span></span>

### <span data-ttu-id="ec282-143">ServiceBus. SharedAccessAuthorizationRuleAttributes 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ec282-143">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="ec282-144">상속자</span><span class="sxs-lookup"><span data-stu-id="ec282-144">NOTES</span></span>

## <span data-ttu-id="ec282-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ec282-145">RELATED LINKS</span></span>

