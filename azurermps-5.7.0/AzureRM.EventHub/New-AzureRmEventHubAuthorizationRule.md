---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/new-azurermeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubAuthorizationRule.md
ms.openlocfilehash: ae7fe44bf0fd3eccb157cefd6f57dade203d4fb2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93704025"
---
# <span data-ttu-id="b5aef-101">New-AzureRmEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="b5aef-101">New-AzureRmEventHubAuthorizationRule</span></span>

## <span data-ttu-id="b5aef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5aef-102">SYNOPSIS</span></span>
<span data-ttu-id="b5aef-103">네임 스페이스 또는 eventhub에 대 한 새 이벤트 허브 권한 부여 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b5aef-103">Creates a new Event Hubs authorization rule for namespace or eventhub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b5aef-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b5aef-104">SYNTAX</span></span>

### <span data-ttu-id="b5aef-105">NamespaceAuthorizationRuleSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="b5aef-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5aef-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="b5aef-106">EventhubAuthorizationRuleSet</span></span>
```
New-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b5aef-107">설명은</span><span class="sxs-lookup"><span data-stu-id="b5aef-107">DESCRIPTION</span></span>
<span data-ttu-id="b5aef-108">New-AzureRmEventHubAuthorizationRule cmdlet은 새 이벤트 허브 권한 부여 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b5aef-108">The New-AzureRmEventHubAuthorizationRule cmdlet creates a new Event Hubs authorization rule.</span></span>

## <span data-ttu-id="b5aef-109">예제의</span><span class="sxs-lookup"><span data-stu-id="b5aef-109">EXAMPLES</span></span>

### <span data-ttu-id="b5aef-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="b5aef-110">Example 1</span></span>
```
PS C:\> New-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName -Rights @("Listen","Send")
```

<span data-ttu-id="b5aef-111">\` \` \` 리소스 그룹 MyResourceGroupName를 사용 하 여 MyNamespaceName 네임 스페이스에 대 한 수신 대기 및 보내기 권한을 부여 하 MyAuthRuleName 권한 부여 규칙을 만듭니다 \` \` \` .</span><span class="sxs-lookup"><span data-stu-id="b5aef-111">Creates an authorization rule \`MyAuthRuleName\` granting Listen and Send rights to the namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="b5aef-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="b5aef-112">Example 2</span></span>
```
PS C:\> New-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName -Rights @("Listen","Send")
```

<span data-ttu-id="b5aef-113">\` \` \` \` \` 리소스 그룹 MyResourceGroupName를 사용 하 여 네임 스페이스 MyNamespaceName의 이벤트 허브 MyEventHubName에 대 한 수신 \` 대기 및 \` 보내기 권한을 부여 \` MyAuthRuleName는 권한 부여 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b5aef-113">Creates an authorization rule \`MyAuthRuleName\` granting Listen and Send rights to the Event Hub \`MyEventHubName\` in namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="b5aef-114">변수</span><span class="sxs-lookup"><span data-stu-id="b5aef-114">PARAMETERS</span></span>

### <span data-ttu-id="b5aef-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5aef-115">-DefaultProfile</span></span>
<span data-ttu-id="b5aef-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b5aef-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5aef-117">-EventHub</span><span class="sxs-lookup"><span data-stu-id="b5aef-117">-EventHub</span></span>
<span data-ttu-id="b5aef-118">EventHub 이름</span><span class="sxs-lookup"><span data-stu-id="b5aef-118">EventHub Name</span></span>

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

### <span data-ttu-id="b5aef-119">-이름</span><span class="sxs-lookup"><span data-stu-id="b5aef-119">-Name</span></span>
<span data-ttu-id="b5aef-120">AuthorizationRule 이름</span><span class="sxs-lookup"><span data-stu-id="b5aef-120">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="b5aef-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="b5aef-121">-Namespace</span></span>
<span data-ttu-id="b5aef-122">네임 스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="b5aef-122">Namespace Name</span></span>

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

### <span data-ttu-id="b5aef-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5aef-123">-ResourceGroupName</span></span>
<span data-ttu-id="b5aef-124">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="b5aef-124">Resource Group Name</span></span>

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

### <span data-ttu-id="b5aef-125">-권한</span><span class="sxs-lookup"><span data-stu-id="b5aef-125">-Rights</span></span>
<span data-ttu-id="b5aef-126">권한 (예: "듣기", "보내기", "관리")</span><span class="sxs-lookup"><span data-stu-id="b5aef-126">Rights, e.g. "Listen","Send","Manage"</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:
Accepted values: Listen, Send, Manage

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5aef-127">-확인</span><span class="sxs-lookup"><span data-stu-id="b5aef-127">-Confirm</span></span>
<span data-ttu-id="b5aef-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5aef-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5aef-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5aef-129">-WhatIf</span></span>
<span data-ttu-id="b5aef-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b5aef-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5aef-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b5aef-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5aef-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5aef-132">CommonParameters</span></span>
<span data-ttu-id="b5aef-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5aef-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="b5aef-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5aef-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5aef-135">입력</span><span class="sxs-lookup"><span data-stu-id="b5aef-135">INPUTS</span></span>

### <span data-ttu-id="b5aef-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b5aef-136">System.String</span></span>
<span data-ttu-id="b5aef-137">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="b5aef-137">System.String[]</span></span>


## <span data-ttu-id="b5aef-138">출력</span><span class="sxs-lookup"><span data-stu-id="b5aef-138">OUTPUTS</span></span>

### <span data-ttu-id="b5aef-139">Microsoft. ' EventHub. ' PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="b5aef-139">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>


## <span data-ttu-id="b5aef-140">상속자</span><span class="sxs-lookup"><span data-stu-id="b5aef-140">NOTES</span></span>

## <span data-ttu-id="b5aef-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b5aef-141">RELATED LINKS</span></span>
