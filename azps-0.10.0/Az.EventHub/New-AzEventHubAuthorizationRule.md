---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/New-AzEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/New-AzEventHubAuthorizationRule.md
ms.openlocfilehash: c59a58e458ceed2c183978a8839de1cd864ffaa7
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875926"
---
# <span data-ttu-id="e9231-101">New-AzEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="e9231-101">New-AzEventHubAuthorizationRule</span></span>

## <span data-ttu-id="e9231-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9231-102">SYNOPSIS</span></span>
<span data-ttu-id="e9231-103">네임 스페이스 또는 eventhub에 대 한 새 이벤트 허브 권한 부여 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e9231-103">Creates a new Event Hubs authorization rule for namespace or eventhub.</span></span>

## <span data-ttu-id="e9231-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e9231-104">SYNTAX</span></span>

### <span data-ttu-id="e9231-105">NamespaceAuthorizationRuleSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="e9231-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9231-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="e9231-106">EventhubAuthorizationRuleSet</span></span>
```
New-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e9231-107">설명은</span><span class="sxs-lookup"><span data-stu-id="e9231-107">DESCRIPTION</span></span>
<span data-ttu-id="e9231-108">New-AzEventHubAuthorizationRule cmdlet은 새 이벤트 허브 권한 부여 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e9231-108">The New-AzEventHubAuthorizationRule cmdlet creates a new Event Hubs authorization rule.</span></span>

## <span data-ttu-id="e9231-109">예제의</span><span class="sxs-lookup"><span data-stu-id="e9231-109">EXAMPLES</span></span>

### <span data-ttu-id="e9231-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="e9231-110">Example 1</span></span>
```
PS C:\> New-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName -Rights @("Listen","Send")
```

<span data-ttu-id="e9231-111">\` \` \` 리소스 그룹 MyResourceGroupName를 사용 하 여 MyNamespaceName 네임 스페이스에 대 한 수신 대기 및 보내기 권한을 부여 하 MyAuthRuleName 권한 부여 규칙을 만듭니다 \` \` \` .</span><span class="sxs-lookup"><span data-stu-id="e9231-111">Creates an authorization rule \`MyAuthRuleName\` granting Listen and Send rights to the namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="e9231-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="e9231-112">Example 2</span></span>
```
PS C:\> New-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName -Rights @("Listen","Send")
```

<span data-ttu-id="e9231-113">\` \` \` \` \` 리소스 그룹 MyResourceGroupName를 사용 하 여 네임 스페이스 MyNamespaceName의 이벤트 허브 MyEventHubName에 대 한 수신 \` 대기 및 \` 보내기 권한을 부여 \` MyAuthRuleName는 권한 부여 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e9231-113">Creates an authorization rule \`MyAuthRuleName\` granting Listen and Send rights to the Event Hub \`MyEventHubName\` in namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="e9231-114">변수</span><span class="sxs-lookup"><span data-stu-id="e9231-114">PARAMETERS</span></span>

### <span data-ttu-id="e9231-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9231-115">-DefaultProfile</span></span>
<span data-ttu-id="e9231-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e9231-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9231-117">-EventHub</span><span class="sxs-lookup"><span data-stu-id="e9231-117">-EventHub</span></span>
<span data-ttu-id="e9231-118">EventHub 이름</span><span class="sxs-lookup"><span data-stu-id="e9231-118">EventHub Name</span></span>

```yaml
Type: System.String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9231-119">-이름</span><span class="sxs-lookup"><span data-stu-id="e9231-119">-Name</span></span>
<span data-ttu-id="e9231-120">AuthorizationRule 이름</span><span class="sxs-lookup"><span data-stu-id="e9231-120">AuthorizationRule Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9231-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="e9231-121">-Namespace</span></span>
<span data-ttu-id="e9231-122">네임 스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="e9231-122">Namespace Name</span></span>

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

### <span data-ttu-id="e9231-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9231-123">-ResourceGroupName</span></span>
<span data-ttu-id="e9231-124">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="e9231-124">Resource Group Name</span></span>

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

### <span data-ttu-id="e9231-125">-권한</span><span class="sxs-lookup"><span data-stu-id="e9231-125">-Rights</span></span>
<span data-ttu-id="e9231-126">권한 (예: "듣기", "보내기", "관리")</span><span class="sxs-lookup"><span data-stu-id="e9231-126">Rights, e.g. "Listen","Send","Manage"</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: Listen, Send, Manage

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9231-127">-확인</span><span class="sxs-lookup"><span data-stu-id="e9231-127">-Confirm</span></span>
<span data-ttu-id="e9231-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9231-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9231-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9231-129">-WhatIf</span></span>
<span data-ttu-id="e9231-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e9231-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9231-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e9231-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9231-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9231-132">CommonParameters</span></span>
<span data-ttu-id="e9231-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9231-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9231-134">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9231-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9231-135">입력</span><span class="sxs-lookup"><span data-stu-id="e9231-135">INPUTS</span></span>

### <span data-ttu-id="e9231-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e9231-136">System.String</span></span>

### <span data-ttu-id="e9231-137">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="e9231-137">System.String[]</span></span>

## <span data-ttu-id="e9231-138">출력</span><span class="sxs-lookup"><span data-stu-id="e9231-138">OUTPUTS</span></span>

### <span data-ttu-id="e9231-139">Microsoft. ' EventHub. ' PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="e9231-139">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="e9231-140">상속자</span><span class="sxs-lookup"><span data-stu-id="e9231-140">NOTES</span></span>

## <span data-ttu-id="e9231-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e9231-141">RELATED LINKS</span></span>
