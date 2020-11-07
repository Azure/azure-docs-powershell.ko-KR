---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusNamespaceAuthorizationRule.md
ms.openlocfilehash: 6e20ceb2a6809e1e6010263563006468753cd41c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93710946"
---
# <span data-ttu-id="18188-101">New-AzureRmServiceBusNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="18188-101">New-AzureRmServiceBusNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="18188-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18188-102">SYNOPSIS</span></span>
<span data-ttu-id="18188-103">지정 된 Service Bus 네임 스페이스에 대 한 새 권한 부여 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="18188-103">Creates a new authorization rule for the specified Service Bus namespace</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="18188-104">구문과</span><span class="sxs-lookup"><span data-stu-id="18188-104">SYNTAX</span></span>

```
New-AzureRmServiceBusNamespaceAuthorizationRule [-ResourceGroup] <String> -Namespace <String> -Name <String>
 [-Rights] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="18188-105">설명은</span><span class="sxs-lookup"><span data-stu-id="18188-105">DESCRIPTION</span></span>
<span data-ttu-id="18188-106">**AzureRmServiceBusNamespaceAuthorizationRule** cmdlet은 지정 된 Service Bus 네임 스페이스에 대 한 새 권한 부여 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="18188-106">The **New-AzureRmServiceBusNamespaceAuthorizationRule** cmdlet creates a new authorization rule for the specified Service Bus namespace.</span></span>

## <span data-ttu-id="18188-107">예제의</span><span class="sxs-lookup"><span data-stu-id="18188-107">EXAMPLES</span></span>

### <span data-ttu-id="18188-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="18188-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -AuthorizationRuleName AuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="18188-109">`AuthoRule1`네임 스페이스에 대 한 **수신** 및 **보내기** 권한을 사용 하 여 만듭니다 `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="18188-109">Creates `AuthoRule1` with **Listen** and **Send** rights for the namespace `SB-Example1`.</span></span>

## <span data-ttu-id="18188-110">변수</span><span class="sxs-lookup"><span data-stu-id="18188-110">PARAMETERS</span></span>

### <span data-ttu-id="18188-111">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="18188-111">-ResourceGroup</span></span>
<span data-ttu-id="18188-112">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="18188-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="18188-113">-권한</span><span class="sxs-lookup"><span data-stu-id="18188-113">-Rights</span></span>
<span data-ttu-id="18188-114">권한을 부여 합니다. 예를 들어 @ ("수신", "보내기", "관리")</span><span class="sxs-lookup"><span data-stu-id="18188-114">The Rights; for example, @("Listen","Send","Manage")</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18188-115">-확인</span><span class="sxs-lookup"><span data-stu-id="18188-115">-Confirm</span></span>
<span data-ttu-id="18188-116">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="18188-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18188-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18188-117">-WhatIf</span></span>
<span data-ttu-id="18188-118">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="18188-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18188-119">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="18188-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18188-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18188-120">-DefaultProfile</span></span>
<span data-ttu-id="18188-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="18188-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="18188-122">-이름</span><span class="sxs-lookup"><span data-stu-id="18188-122">-Name</span></span>
<span data-ttu-id="18188-123">AuthorizationRule 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="18188-123">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="18188-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="18188-124">-Namespace</span></span>
<span data-ttu-id="18188-125">ServiceBus 네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="18188-125">ServiceBus Namespace Name.</span></span>

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

### <span data-ttu-id="18188-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18188-126">CommonParameters</span></span>
<span data-ttu-id="18188-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="18188-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18188-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18188-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18188-129">입력</span><span class="sxs-lookup"><span data-stu-id="18188-129">INPUTS</span></span>

### <span data-ttu-id="18188-130">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="18188-130">-ResourceGroup</span></span>
 <span data-ttu-id="18188-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="18188-131">System.String</span></span>
 

### <span data-ttu-id="18188-132">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="18188-132">-NamespaceName</span></span>
 <span data-ttu-id="18188-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="18188-133">System.String</span></span>
 

### <span data-ttu-id="18188-134">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="18188-134">-AuthorizationRuleName</span></span>
 <span data-ttu-id="18188-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="18188-135">System.String</span></span>
 

### <span data-ttu-id="18188-136">-권한</span><span class="sxs-lookup"><span data-stu-id="18188-136">-Rights</span></span>
 <span data-ttu-id="18188-137">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="18188-137">System.String []</span></span>

## <span data-ttu-id="18188-138">출력</span><span class="sxs-lookup"><span data-stu-id="18188-138">OUTPUTS</span></span>

### <span data-ttu-id="18188-139">ServiceBus. SharedAccessAuthorizationRuleAttributes 있습니다.</span><span class="sxs-lookup"><span data-stu-id="18188-139">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes</span></span>
<span data-ttu-id="18188-140">Id:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/AuthorizationRules/AuthoRule1 유형: Microsoft. ServiceBus/AuthorizationRules 이름: AuthoRule1 Location: Tags: Rights: {Listen, Send}</span><span class="sxs-lookup"><span data-stu-id="18188-140">Id       : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/AuthorizationRules/AuthoRule1 Type     : Microsoft.ServiceBus/AuthorizationRules Name     : AuthoRule1 Location : Tags     : Rights   : {Listen, Send}</span></span>

## <span data-ttu-id="18188-141">상속자</span><span class="sxs-lookup"><span data-stu-id="18188-141">NOTES</span></span>

## <span data-ttu-id="18188-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="18188-142">RELATED LINKS</span></span>

