---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubNamespaceAuthorizationRule.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: dc384ca6056ef13d5517241d550bacddf2e7d0d5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537244"
---
# <span data-ttu-id="b341b-101">New-AzureRmEventHubNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="b341b-101">New-AzureRmEventHubNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="b341b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b341b-102">SYNOPSIS</span></span>
<span data-ttu-id="b341b-103">지정 된 네임 스페이스에 대 한 새 권한 부여 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b341b-103">Creates a new authorization rule on the specified namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b341b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b341b-104">SYNTAX</span></span>

```
New-AzureRmEventHubNamespaceAuthorizationRule [-ResourceGroupName] <String> [-NamespaceName] <String>
 [-AuthorizationRuleName] <String> [-Rights] <String[]> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="b341b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b341b-105">DESCRIPTION</span></span>
<span data-ttu-id="b341b-106">New-AzureRmEventHubNamespaceAuthorizationRule cmdlet은 지정 된 이벤트 허브 네임 스페이스에 대 한 새 권한 부여 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b341b-106">The New-AzureRmEventHubNamespaceAuthorizationRule cmdlet creates a new authorization rule on the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="b341b-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b341b-107">EXAMPLES</span></span>

### <span data-ttu-id="b341b-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="b341b-108">Example 1</span></span>
```
PS C:\> New-AzureRmEventHubNamespaceAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName -Rights @("Listen","Send")
```

<span data-ttu-id="b341b-109">\` \` \` \` 리소스 그룹 MyResourceGroupName에서 이벤트 허브 네임 스페이스 MyNamespaceName에 대 한 수신 대기 및 보내기 권한을 사용 하 여 \` MyAuthRuleName \` 권한 부여 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b341b-109">Creates the authorization rule \`MyAuthRuleName\` with Listen and Send rights, for Event Hubs namespace \`MyNamespaceName\`, in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="b341b-110">변수</span><span class="sxs-lookup"><span data-stu-id="b341b-110">PARAMETERS</span></span>

### <span data-ttu-id="b341b-111">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="b341b-111">-AuthorizationRuleName</span></span>
<span data-ttu-id="b341b-112">권한 부여 규칙 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b341b-112">Authorization rule name.</span></span>

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

### <span data-ttu-id="b341b-113">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="b341b-113">-NamespaceName</span></span>
<span data-ttu-id="b341b-114">이벤트 허브 네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b341b-114">The Event Hubs namespace name.</span></span>

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

### <span data-ttu-id="b341b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b341b-115">-ResourceGroupName</span></span>
<span data-ttu-id="b341b-116">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b341b-116">Resource group name.</span></span>

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

### <span data-ttu-id="b341b-117">-권한</span><span class="sxs-lookup"><span data-stu-id="b341b-117">-Rights</span></span>
<span data-ttu-id="b341b-118">권한 (예: @ ("수신", "보내기", "관리")</span><span class="sxs-lookup"><span data-stu-id="b341b-118">Rights;for example,  @("Listen","Send","Manage")</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b341b-119">-확인</span><span class="sxs-lookup"><span data-stu-id="b341b-119">-Confirm</span></span>
<span data-ttu-id="b341b-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b341b-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b341b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b341b-121">-WhatIf</span></span>
<span data-ttu-id="b341b-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b341b-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b341b-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b341b-123">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="b341b-124">입력</span><span class="sxs-lookup"><span data-stu-id="b341b-124">INPUTS</span></span>

### <span data-ttu-id="b341b-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b341b-125">System.String</span></span>

## <span data-ttu-id="b341b-126">출력</span><span class="sxs-lookup"><span data-stu-id="b341b-126">OUTPUTS</span></span>

### <span data-ttu-id="b341b-127">Microsoft. \*. a. a.</span><span class="sxs-lookup"><span data-stu-id="b341b-127">Microsoft.Azure.Commands.EventHub.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="b341b-128">상속자</span><span class="sxs-lookup"><span data-stu-id="b341b-128">NOTES</span></span>

## <span data-ttu-id="b341b-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b341b-129">RELATED LINKS</span></span>

