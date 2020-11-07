---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusNamespaceAuthorizationRule.md
ms.openlocfilehash: a56f9b27e19868d22eed94fbcf7717fbe1c68b39
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711234"
---
# <span data-ttu-id="48f3a-101">Set-AzureRmServiceBusNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="48f3a-101">Set-AzureRmServiceBusNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="48f3a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="48f3a-102">SYNOPSIS</span></span>
<span data-ttu-id="48f3a-103">주어진 Service Bus 네임 스페이스에 대해 지정 된 권한 부여 규칙 설명을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="48f3a-103">Updates the specified authorization rule description for the given Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="48f3a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="48f3a-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusNamespaceAuthorizationRule [-ResourceGroup] <String> -Namespace <String>
 -InputObj <SharedAccessAuthorizationRuleAttributes> [-Name <String>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48f3a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="48f3a-105">DESCRIPTION</span></span>
<span data-ttu-id="48f3a-106">**AzureRmServiceBusNamespaceAuthorizationRule** cmdlet은 지정 된 Service Bus 네임 스페이스에서 지정한 권한 부여 규칙에 대 한 설명을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="48f3a-106">The **Set-AzureRmServiceBusNamespaceAuthorizationRule** cmdlet updates the description for the specified authorization rule in the given Service Bus namespace.</span></span>

## <span data-ttu-id="48f3a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="48f3a-107">EXAMPLES</span></span>

### <span data-ttu-id="48f3a-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="48f3a-108">Example 1</span></span>
```
PS C:\> $authRuleObj = Get-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -AuthorizationRuleName AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -AuthRuleObj $authRuleObj
```

<span data-ttu-id="48f3a-109">네임 스페이스의 권한 부여 규칙에 대 한 액세스 권한에서 **관리** 를 제거 합니다 `AuthoRule1` `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="48f3a-109">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in namespace `SB-Example1`.</span></span>

## <span data-ttu-id="48f3a-110">변수</span><span class="sxs-lookup"><span data-stu-id="48f3a-110">PARAMETERS</span></span>

### <span data-ttu-id="48f3a-111">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="48f3a-111">-ResourceGroup</span></span>
<span data-ttu-id="48f3a-112">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="48f3a-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="48f3a-113">-권한</span><span class="sxs-lookup"><span data-stu-id="48f3a-113">-Rights</span></span>
<span data-ttu-id="48f3a-114">권리가 예를 들어 @ ("듣기", "Send", "관리").</span><span class="sxs-lookup"><span data-stu-id="48f3a-114">Rights; for example @("Listen","Send","Manage").</span></span> <span data-ttu-id="48f3a-115">**Authruleobj** 가 지정 되지 않은 경우 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="48f3a-115">Required if **AuthruleObj** is not specified.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48f3a-116">-확인</span><span class="sxs-lookup"><span data-stu-id="48f3a-116">-Confirm</span></span>
<span data-ttu-id="48f3a-117">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="48f3a-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48f3a-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48f3a-118">-WhatIf</span></span>
<span data-ttu-id="48f3a-119">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="48f3a-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="48f3a-120">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="48f3a-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48f3a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48f3a-121">-DefaultProfile</span></span>
<span data-ttu-id="48f3a-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="48f3a-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="48f3a-123">-InputObj</span><span class="sxs-lookup"><span data-stu-id="48f3a-123">-InputObj</span></span>
<span data-ttu-id="48f3a-124">ServiceBus 네임 스페이스 AuthorizationRule 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="48f3a-124">ServiceBus NameSpace AuthorizationRule Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes
Parameter Sets: (All)
Aliases: AuthRuleObj

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48f3a-125">-이름</span><span class="sxs-lookup"><span data-stu-id="48f3a-125">-Name</span></span>
<span data-ttu-id="48f3a-126">AuthorizationRule Name-' AuthruleObj '가 지정 되지 않은 경우 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="48f3a-126">AuthorizationRule Name - Required if 'AuthruleObj' not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48f3a-127">-Namespace</span><span class="sxs-lookup"><span data-stu-id="48f3a-127">-Namespace</span></span>
<span data-ttu-id="48f3a-128">ServiceBus 네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="48f3a-128">ServiceBus Namespace Name.</span></span>

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

### <span data-ttu-id="48f3a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48f3a-129">CommonParameters</span></span>
<span data-ttu-id="48f3a-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="48f3a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48f3a-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48f3a-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48f3a-132">입력</span><span class="sxs-lookup"><span data-stu-id="48f3a-132">INPUTS</span></span>

### <span data-ttu-id="48f3a-133">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="48f3a-133">-ResourceGroup</span></span>
 <span data-ttu-id="48f3a-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="48f3a-134">System.String</span></span>

### <span data-ttu-id="48f3a-135">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="48f3a-135">-NamespaceName</span></span>
 <span data-ttu-id="48f3a-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="48f3a-136">System.String</span></span>

### <span data-ttu-id="48f3a-137">-AuthRuleObj</span><span class="sxs-lookup"><span data-stu-id="48f3a-137">-AuthRuleObj</span></span>
 <span data-ttu-id="48f3a-138">ServiceBus. SharedAccessAuthorizationRuleAttributes 있습니다.</span><span class="sxs-lookup"><span data-stu-id="48f3a-138">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="48f3a-139">출력</span><span class="sxs-lookup"><span data-stu-id="48f3a-139">OUTPUTS</span></span>

### <span data-ttu-id="48f3a-140">ServiceBus. SharedAccessAuthorizationRuleAttributes 있습니다.</span><span class="sxs-lookup"><span data-stu-id="48f3a-140">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes</span></span>
<span data-ttu-id="48f3a-141">Id:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/AuthorizationRules/AuthoRule1 유형: Microsoft. ServiceBus/AuthorizationRules 이름: AuthoRule1 Location: Tags: Rights: {Listen, Send}</span><span class="sxs-lookup"><span data-stu-id="48f3a-141">Id       : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/AuthorizationRules/AuthoRule1 Type     : Microsoft.ServiceBus/AuthorizationRules Name     : AuthoRule1 Location : Tags     : Rights   : {Listen, Send}</span></span>

## <span data-ttu-id="48f3a-142">상속자</span><span class="sxs-lookup"><span data-stu-id="48f3a-142">NOTES</span></span>

## <span data-ttu-id="48f3a-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="48f3a-143">RELATED LINKS</span></span>

