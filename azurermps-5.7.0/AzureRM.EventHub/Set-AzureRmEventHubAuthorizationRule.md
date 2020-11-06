---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/set-azurermeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubAuthorizationRule.md
ms.openlocfilehash: 4965fb6047ca31d2c5b70276a777235d2a3cb050
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530526"
---
# <span data-ttu-id="2ad43-101">Set-AzureRmEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="2ad43-101">Set-AzureRmEventHubAuthorizationRule</span></span>

## <span data-ttu-id="2ad43-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ad43-102">SYNOPSIS</span></span>
<span data-ttu-id="2ad43-103">이벤트 허브에서 지정 된 권한 부여 규칙을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ad43-103">Updates the specified authorization rule on an Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2ad43-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2ad43-104">SYNTAX</span></span>

### <span data-ttu-id="2ad43-105">NamespaceAuthorizationRuleSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="2ad43-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ad43-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="2ad43-106">EventhubAuthorizationRuleSet</span></span>
```
Set-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ad43-107">AuthoRuleInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="2ad43-107">AuthoRuleInputObjectSet</span></span>
```
Set-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSSharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ad43-108">설명은</span><span class="sxs-lookup"><span data-stu-id="2ad43-108">DESCRIPTION</span></span>
<span data-ttu-id="2ad43-109">Set-AzureRmEventHubAuthorizationRule cmdlet은 지정 된 이벤트 허브에서 지정 된 권한 부여 규칙을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ad43-109">The Set-AzureRmEventHubAuthorizationRule cmdlet updates the specified authorization rule on the given Event Hub.</span></span>

## <span data-ttu-id="2ad43-110">예제의</span><span class="sxs-lookup"><span data-stu-id="2ad43-110">EXAMPLES</span></span>

### <span data-ttu-id="2ad43-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="2ad43-111">Example 1</span></span>
```
PS C:\> Set-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName -Rights @("Manage")
```

<span data-ttu-id="2ad43-112">\` \` \` \` 네임 스페이스 MyNamespaceName으로 범위가 지정 된 이벤트 허브 MyEventHubName에 대 한 관리 권한을 부여 하도록 권한 \` 부여 규칙 MyAuthRuleName를 업데이트 합니다 \` .</span><span class="sxs-lookup"><span data-stu-id="2ad43-112">Updates the authorization rule \`MyAuthRuleName\` to grant Manage rights to the Event Hub \`MyEventHubName\`, scoped by the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="2ad43-113">변수</span><span class="sxs-lookup"><span data-stu-id="2ad43-113">PARAMETERS</span></span>

### <span data-ttu-id="2ad43-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ad43-114">-DefaultProfile</span></span>
<span data-ttu-id="2ad43-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2ad43-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ad43-116">-EventHub</span><span class="sxs-lookup"><span data-stu-id="2ad43-116">-EventHub</span></span>
<span data-ttu-id="2ad43-117">EventHub 이름</span><span class="sxs-lookup"><span data-stu-id="2ad43-117">EventHub Name</span></span>

```yaml
Type: String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ad43-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2ad43-118">-InputObject</span></span>
<span data-ttu-id="2ad43-119">AuthorizationRule 개체</span><span class="sxs-lookup"><span data-stu-id="2ad43-119">AuthorizationRule Object</span></span>

```yaml
Type: PSSharedAccessAuthorizationRuleAttributes
Parameter Sets: NamespaceAuthorizationRuleSet, EventhubAuthorizationRuleSet
Aliases: AuthRuleObj

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: PSSharedAccessAuthorizationRuleAttributes
Parameter Sets: AuthoRuleInputObjectSet
Aliases: AuthRuleObj

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2ad43-120">-이름</span><span class="sxs-lookup"><span data-stu-id="2ad43-120">-Name</span></span>
<span data-ttu-id="2ad43-121">AuthorizationRule 이름</span><span class="sxs-lookup"><span data-stu-id="2ad43-121">AuthorizationRule Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ad43-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="2ad43-122">-Namespace</span></span>
<span data-ttu-id="2ad43-123">네임 스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="2ad43-123">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: NamespaceAuthorizationRuleSet, EventhubAuthorizationRuleSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ad43-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ad43-124">-ResourceGroupName</span></span>
<span data-ttu-id="2ad43-125">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="2ad43-125">Resource Group Name</span></span>

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

### <span data-ttu-id="2ad43-126">-권한</span><span class="sxs-lookup"><span data-stu-id="2ad43-126">-Rights</span></span>
<span data-ttu-id="2ad43-127">권한 (예: @ ("듣기", "보내기", "관리")</span><span class="sxs-lookup"><span data-stu-id="2ad43-127">Rights, e.g. @("Listen","Send","Manage")</span></span>

```yaml
Type: String[]
Parameter Sets: NamespaceAuthorizationRuleSet, EventhubAuthorizationRuleSet
Aliases:
Accepted values: Listen, Send, Manage

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String[]
Parameter Sets: AuthoRulePropertiesSet
Aliases:
Accepted values: Listen, Send, Manage

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ad43-128">-확인</span><span class="sxs-lookup"><span data-stu-id="2ad43-128">-Confirm</span></span>
<span data-ttu-id="2ad43-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ad43-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ad43-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ad43-130">-WhatIf</span></span>
<span data-ttu-id="2ad43-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2ad43-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ad43-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2ad43-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ad43-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ad43-133">CommonParameters</span></span>
<span data-ttu-id="2ad43-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ad43-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="2ad43-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ad43-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ad43-136">입력</span><span class="sxs-lookup"><span data-stu-id="2ad43-136">INPUTS</span></span>

### <span data-ttu-id="2ad43-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="2ad43-137">System.String</span></span>
<span data-ttu-id="2ad43-138">Microsoft. Azure. PSSharedAccessAuthorizationRuleAttributes 시스템. String []</span><span class="sxs-lookup"><span data-stu-id="2ad43-138">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes System.String[]</span></span>


## <span data-ttu-id="2ad43-139">출력</span><span class="sxs-lookup"><span data-stu-id="2ad43-139">OUTPUTS</span></span>

### <span data-ttu-id="2ad43-140">Microsoft. ' EventHub. ' PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="2ad43-140">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>


## <span data-ttu-id="2ad43-141">상속자</span><span class="sxs-lookup"><span data-stu-id="2ad43-141">NOTES</span></span>

## <span data-ttu-id="2ad43-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2ad43-142">RELATED LINKS</span></span>
