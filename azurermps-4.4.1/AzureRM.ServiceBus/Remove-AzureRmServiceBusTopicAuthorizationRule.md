---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusTopicAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusTopicAuthorizationRule.md
ms.openlocfilehash: 5694d46e44931d59f79a5ac7b86ceabf7632f945
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536187"
---
# <span data-ttu-id="8d935-101">Remove-AzureRmServiceBusTopicAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="8d935-101">Remove-AzureRmServiceBusTopicAuthorizationRule</span></span>

## <span data-ttu-id="8d935-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d935-102">SYNOPSIS</span></span>
<span data-ttu-id="8d935-103">지정 된 Service Bus 네임 스페이스에서 주제의 권한 부여 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d935-103">Removes the authorization rule of a topic from the specified Service Bus Namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8d935-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8d935-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusTopicAuthorizationRule [-ResourceGroup] <String> -Namespace <String> -Topic <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8d935-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8d935-105">DESCRIPTION</span></span>
<span data-ttu-id="8d935-106">**AzureRmServiceBusTopicAuthorizationRule** cmdlet은 지정 된 Service Bus 네임 스페이스의 주제에 대 한 권한 부여 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d935-106">The **Remove-AzureRmServiceBusTopicAuthorizationRule** cmdlet removes the authorization rule of a topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="8d935-107">예제의</span><span class="sxs-lookup"><span data-stu-id="8d935-107">EXAMPLES</span></span>

### <span data-ttu-id="8d935-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="8d935-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusTopicAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -AuthorizationRuleName SBTopicAuthoRule1
```

<span data-ttu-id="8d935-109">네임 스페이스의 주제에 대 한 권한 부여 규칙을 제거 합니다 `SBTopicAuthoRule1` `SB-Topic_exampl1` `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="8d935-109">Removes the authorization rule `SBTopicAuthoRule1` of the topic `SB-Topic_exampl1` from the namespace `SB-Example1`.</span></span>

## <span data-ttu-id="8d935-110">변수</span><span class="sxs-lookup"><span data-stu-id="8d935-110">PARAMETERS</span></span>

### <span data-ttu-id="8d935-111">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8d935-111">-ResourceGroup</span></span>
<span data-ttu-id="8d935-112">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8d935-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="8d935-113">-확인</span><span class="sxs-lookup"><span data-stu-id="8d935-113">-Confirm</span></span>
<span data-ttu-id="8d935-114">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d935-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d935-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d935-115">-WhatIf</span></span>
<span data-ttu-id="8d935-116">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8d935-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d935-117">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8d935-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d935-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d935-118">-DefaultProfile</span></span>
<span data-ttu-id="8d935-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8d935-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8d935-120">-이름</span><span class="sxs-lookup"><span data-stu-id="8d935-120">-Name</span></span>
<span data-ttu-id="8d935-121">주제 AuthorizationRule 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8d935-121">Topic AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="8d935-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="8d935-122">-Namespace</span></span>
<span data-ttu-id="8d935-123">네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8d935-123">Namespace Name.</span></span>

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

### <span data-ttu-id="8d935-124">-주제</span><span class="sxs-lookup"><span data-stu-id="8d935-124">-Topic</span></span>
<span data-ttu-id="8d935-125">주제 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8d935-125">Topic Name.</span></span>

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

### <span data-ttu-id="8d935-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d935-126">CommonParameters</span></span>
<span data-ttu-id="8d935-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d935-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d935-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d935-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d935-129">입력</span><span class="sxs-lookup"><span data-stu-id="8d935-129">INPUTS</span></span>

### <span data-ttu-id="8d935-130">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8d935-130">-ResourceGroup</span></span>
 <span data-ttu-id="8d935-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8d935-131">System.String</span></span>

### <span data-ttu-id="8d935-132">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="8d935-132">-NamespaceName</span></span>
 <span data-ttu-id="8d935-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8d935-133">System.String</span></span>

### <span data-ttu-id="8d935-134">-TopicName</span><span class="sxs-lookup"><span data-stu-id="8d935-134">-TopicName</span></span>
 <span data-ttu-id="8d935-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8d935-135">System.String</span></span>

### <span data-ttu-id="8d935-136">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="8d935-136">-AuthorizationRuleName</span></span>
 <span data-ttu-id="8d935-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8d935-137">System.String</span></span>

## <span data-ttu-id="8d935-138">출력</span><span class="sxs-lookup"><span data-stu-id="8d935-138">OUTPUTS</span></span>

### <span data-ttu-id="8d935-139">System. 개체</span><span class="sxs-lookup"><span data-stu-id="8d935-139">System.Object</span></span>

## <span data-ttu-id="8d935-140">상속자</span><span class="sxs-lookup"><span data-stu-id="8d935-140">NOTES</span></span>

## <span data-ttu-id="8d935-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8d935-141">RELATED LINKS</span></span>

