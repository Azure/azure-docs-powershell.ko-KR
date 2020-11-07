---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusTopicAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusTopicAuthorizationRule.md
ms.openlocfilehash: bbc6c0119f0f8f424b508adc38b5de80cd097734
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93710944"
---
# <span data-ttu-id="46e30-101">Set-AzureRmServiceBusTopicAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="46e30-101">Set-AzureRmServiceBusTopicAuthorizationRule</span></span>

## <span data-ttu-id="46e30-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46e30-102">SYNOPSIS</span></span>
<span data-ttu-id="46e30-103">지정 된 Service Bus 항목에 대해 지정한 권한 부여 규칙 설명을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="46e30-103">Updates the specified authorization rule description for the given Service Bus topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="46e30-104">구문과</span><span class="sxs-lookup"><span data-stu-id="46e30-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusTopicAuthorizationRule [-ResourceGroup] <String> -Namespace <String> -Topic <String>
 -InputObj <SharedAccessAuthorizationRuleAttributes> [-Name <String>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46e30-105">설명은</span><span class="sxs-lookup"><span data-stu-id="46e30-105">DESCRIPTION</span></span>
<span data-ttu-id="46e30-106">**Set-AzureRmServiceBusTopicAuthorizationRule** cmdlet은 지정 된 Service Bus 항목에 대 한 설명을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="46e30-106">The **Set-AzureRmServiceBusTopicAuthorizationRule** cmdlet updates the description for the specified authorization rule of the given Service Bus topic.</span></span>

## <span data-ttu-id="46e30-107">예제의</span><span class="sxs-lookup"><span data-stu-id="46e30-107">EXAMPLES</span></span>

### <span data-ttu-id="46e30-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="46e30-108">Example 1</span></span>
```
PS C:\> $authRuleObj = Get-AzureRmServiceBusTopicAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -AuthorizationRuleName SBTopicAuthoRule1

PS C:\> $authRuleObj.Rights.Add("Manage")

PS C:\> Set-AzureRmServiceBusTopicAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -AuthRuleObj $authRuleObj
```

<span data-ttu-id="46e30-109">항목에 대 한 권한 부여 규칙의 액세스 권한에 대 한 **관리** 를 추가 `SBTopicAuthoRule1` `SB-Topic_exampl1` 합니다.</span><span class="sxs-lookup"><span data-stu-id="46e30-109">Adds **Manage** to the access rights of the authorization rule `SBTopicAuthoRule1` on topic `SB-Topic_exampl1`.</span></span>

## <span data-ttu-id="46e30-110">변수</span><span class="sxs-lookup"><span data-stu-id="46e30-110">PARAMETERS</span></span>

### <span data-ttu-id="46e30-111">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="46e30-111">-ResourceGroup</span></span>
<span data-ttu-id="46e30-112">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="46e30-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="46e30-113">-권한</span><span class="sxs-lookup"><span data-stu-id="46e30-113">-Rights</span></span>
<span data-ttu-id="46e30-114">권리가 예를 들어 @ ("수신", "보내기", "관리").</span><span class="sxs-lookup"><span data-stu-id="46e30-114">Rights; for example, @("Listen","Send","Manage").</span></span> <span data-ttu-id="46e30-115">**-Authruleobj** 가 지정 되지 않은 경우 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="46e30-115">Required if **-AuthruleObj** is not specified.</span></span>

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

### <span data-ttu-id="46e30-116">-확인</span><span class="sxs-lookup"><span data-stu-id="46e30-116">-Confirm</span></span>
<span data-ttu-id="46e30-117">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="46e30-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46e30-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46e30-118">-WhatIf</span></span>
<span data-ttu-id="46e30-119">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="46e30-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46e30-120">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="46e30-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46e30-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46e30-121">-DefaultProfile</span></span>
<span data-ttu-id="46e30-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="46e30-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="46e30-123">-InputObj</span><span class="sxs-lookup"><span data-stu-id="46e30-123">-InputObj</span></span>
<span data-ttu-id="46e30-124">ServiceBus Topic AuthorizationRule 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="46e30-124">ServiceBus Topic AuthorizationRule Object.</span></span>

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

### <span data-ttu-id="46e30-125">-이름</span><span class="sxs-lookup"><span data-stu-id="46e30-125">-Name</span></span>
<span data-ttu-id="46e30-126">AuthorizationRule Name-' AuthruleObj '가 지정 되지 않은 경우 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="46e30-126">AuthorizationRule Name - Required if 'AuthruleObj' not specified.</span></span>

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

### <span data-ttu-id="46e30-127">-Namespace</span><span class="sxs-lookup"><span data-stu-id="46e30-127">-Namespace</span></span>
<span data-ttu-id="46e30-128">네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="46e30-128">Namespace Name.</span></span>

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

### <span data-ttu-id="46e30-129">-주제</span><span class="sxs-lookup"><span data-stu-id="46e30-129">-Topic</span></span>
<span data-ttu-id="46e30-130">주제 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="46e30-130">Topic Name.</span></span>

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

### <span data-ttu-id="46e30-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46e30-131">CommonParameters</span></span>
<span data-ttu-id="46e30-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="46e30-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46e30-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46e30-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46e30-134">입력</span><span class="sxs-lookup"><span data-stu-id="46e30-134">INPUTS</span></span>

### <span data-ttu-id="46e30-135">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="46e30-135">-ResourceGroup</span></span>
 <span data-ttu-id="46e30-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="46e30-136">System.String</span></span>

### <span data-ttu-id="46e30-137">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="46e30-137">-NamespaceName</span></span>
 <span data-ttu-id="46e30-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="46e30-138">System.String</span></span>

### <span data-ttu-id="46e30-139">-TopicName</span><span class="sxs-lookup"><span data-stu-id="46e30-139">-TopicName</span></span>
 <span data-ttu-id="46e30-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="46e30-140">System.String</span></span>

### <span data-ttu-id="46e30-141">-AuthRuleObj</span><span class="sxs-lookup"><span data-stu-id="46e30-141">-AuthRuleObj</span></span>
 <span data-ttu-id="46e30-142">ServiceBus. SharedAccessAuthorizationRuleAttributes 있습니다.</span><span class="sxs-lookup"><span data-stu-id="46e30-142">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="46e30-143">출력</span><span class="sxs-lookup"><span data-stu-id="46e30-143">OUTPUTS</span></span>

### <span data-ttu-id="46e30-144">ServiceBus. SharedAccessAuthorizationRuleAttributes 있습니다.</span><span class="sxs-lookup"><span data-stu-id="46e30-144">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes</span></span>
<span data-ttu-id="46e30-145">Id:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/SB-Topic_exampl1/authorization SBTopicAuthoRule1 Type: Microsoft. ServiceBus/AuthorizationRules 이름: SBTopicAuthoRule1 Location: 서쪽 US 태그: Rights: {듣기, 보내기, 관리}</span><span class="sxs-lookup"><span data-stu-id="46e30-145">Id       : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/SB-Topic_exampl1/authorization Rules/SBTopicAuthoRule1 Type     : Microsoft.ServiceBus/AuthorizationRules Name     : SBTopicAuthoRule1 Location : West US Tags     : Rights   : {Listen, Send, Manage}</span></span>

## <span data-ttu-id="46e30-146">상속자</span><span class="sxs-lookup"><span data-stu-id="46e30-146">NOTES</span></span>

## <span data-ttu-id="46e30-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="46e30-147">RELATED LINKS</span></span>

