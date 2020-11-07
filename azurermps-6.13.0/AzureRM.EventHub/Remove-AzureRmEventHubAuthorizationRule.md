---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/remove-azurermeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubAuthorizationRule.md
ms.openlocfilehash: 35e3889603dc7e86a7d10679864adfd34a880b66
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702615"
---
# <span data-ttu-id="1f1a5-101">Remove-AzureRmEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="1f1a5-101">Remove-AzureRmEventHubAuthorizationRule</span></span>

## <span data-ttu-id="1f1a5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f1a5-102">SYNOPSIS</span></span>
<span data-ttu-id="1f1a5-103">지정 된 이벤트 허브 권한 부여 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f1a5-103">Removes the specified Event Hub authorization rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f1a5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1f1a5-104">SYNTAX</span></span>

### <span data-ttu-id="1f1a5-105">NamespaceAuthorizationRuleSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="1f1a5-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f1a5-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="1f1a5-106">EventhubAuthorizationRuleSet</span></span>
```
Remove-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String>
 [-EventHub] <String> [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f1a5-107">설명은</span><span class="sxs-lookup"><span data-stu-id="1f1a5-107">DESCRIPTION</span></span>
<span data-ttu-id="1f1a5-108">Remove-AzureRmEventHubAuthorizationRule cmdlet은 지정 된 이벤트 허브에서 지정한 권한 부여 규칙을 제거 하 고 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f1a5-108">The Remove-AzureRmEventHubAuthorizationRule cmdlet removes and deletes the specified authorization rule from the given Event Hub.</span></span>

## <span data-ttu-id="1f1a5-109">예제의</span><span class="sxs-lookup"><span data-stu-id="1f1a5-109">EXAMPLES</span></span>

### <span data-ttu-id="1f1a5-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="1f1a5-110">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName
```

<span data-ttu-id="1f1a5-111">\` \` 네임 스페이스 MyNamespaceName에서 권한 부여 규칙 MyAuthRuleName를 제거 합니다 \` \` .</span><span class="sxs-lookup"><span data-stu-id="1f1a5-111">Removes the authorization rule \`MyAuthRuleName\` from the Namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="1f1a5-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="1f1a5-112">Example 2</span></span>
```
PS C:\> Remove-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName
```

<span data-ttu-id="1f1a5-113">\` \` 이벤트 허브 MyEventHubName에서 권한 부여 규칙 MyAuthRuleName를 제거 합니다 \` \` .</span><span class="sxs-lookup"><span data-stu-id="1f1a5-113">Removes the authorization rule \`MyAuthRuleName\` from the Event Hub \`MyEventHubName\`.</span></span>

## <span data-ttu-id="1f1a5-114">변수</span><span class="sxs-lookup"><span data-stu-id="1f1a5-114">PARAMETERS</span></span>

### <span data-ttu-id="1f1a5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f1a5-115">-DefaultProfile</span></span>
<span data-ttu-id="1f1a5-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1f1a5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f1a5-117">-EventHub</span><span class="sxs-lookup"><span data-stu-id="1f1a5-117">-EventHub</span></span>
<span data-ttu-id="1f1a5-118">EventHub 이름</span><span class="sxs-lookup"><span data-stu-id="1f1a5-118">EventHub Name</span></span>

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

### <span data-ttu-id="1f1a5-119">-Force</span><span class="sxs-lookup"><span data-stu-id="1f1a5-119">-Force</span></span>
<span data-ttu-id="1f1a5-120">확인 메시지 표시 안 함</span><span class="sxs-lookup"><span data-stu-id="1f1a5-120">Do not ask for confirmation</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f1a5-121">-이름</span><span class="sxs-lookup"><span data-stu-id="1f1a5-121">-Name</span></span>
<span data-ttu-id="1f1a5-122">AuthorizationRule 이름</span><span class="sxs-lookup"><span data-stu-id="1f1a5-122">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="1f1a5-123">-Namespace</span><span class="sxs-lookup"><span data-stu-id="1f1a5-123">-Namespace</span></span>
<span data-ttu-id="1f1a5-124">네임 스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="1f1a5-124">Namespace Name</span></span>

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

### <span data-ttu-id="1f1a5-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1f1a5-125">-PassThru</span></span>
<span data-ttu-id="1f1a5-126">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f1a5-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="1f1a5-127">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1f1a5-127">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f1a5-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f1a5-128">-ResourceGroupName</span></span>
<span data-ttu-id="1f1a5-129">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="1f1a5-129">Resource Group Name</span></span>

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

### <span data-ttu-id="1f1a5-130">-확인</span><span class="sxs-lookup"><span data-stu-id="1f1a5-130">-Confirm</span></span>
<span data-ttu-id="1f1a5-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f1a5-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f1a5-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f1a5-132">-WhatIf</span></span>
<span data-ttu-id="1f1a5-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1f1a5-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f1a5-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1f1a5-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f1a5-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f1a5-135">CommonParameters</span></span>
<span data-ttu-id="1f1a5-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f1a5-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f1a5-137">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f1a5-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f1a5-138">입력</span><span class="sxs-lookup"><span data-stu-id="1f1a5-138">INPUTS</span></span>

### <span data-ttu-id="1f1a5-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="1f1a5-139">System.String</span></span>

## <span data-ttu-id="1f1a5-140">출력</span><span class="sxs-lookup"><span data-stu-id="1f1a5-140">OUTPUTS</span></span>

### <span data-ttu-id="1f1a5-141">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="1f1a5-141">System.Boolean</span></span>

## <span data-ttu-id="1f1a5-142">상속자</span><span class="sxs-lookup"><span data-stu-id="1f1a5-142">NOTES</span></span>

## <span data-ttu-id="1f1a5-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1f1a5-143">RELATED LINKS</span></span>
