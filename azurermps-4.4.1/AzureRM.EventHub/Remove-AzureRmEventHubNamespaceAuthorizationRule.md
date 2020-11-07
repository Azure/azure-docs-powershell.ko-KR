---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubNamespaceAuthorizationRule.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 4a980edd1833b37b358f86d2e3ccb6a9efc8d836
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703120"
---
# <span data-ttu-id="479d1-101">Remove-AzureRmEventHubNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="479d1-101">Remove-AzureRmEventHubNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="479d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="479d1-102">SYNOPSIS</span></span>
<span data-ttu-id="479d1-103">지정 된 이벤트 허브 네임 스페이스에서 지정한 권한 부여 규칙을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="479d1-103">Deletes the specified authorization rule on the given Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="479d1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="479d1-104">SYNTAX</span></span>

```
Remove-AzureRmEventHubNamespaceAuthorizationRule [-ResourceGroupName] <String> [-NamespaceName] <String>
 [-AuthorizationRuleName] <String> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="479d1-105">설명은</span><span class="sxs-lookup"><span data-stu-id="479d1-105">DESCRIPTION</span></span>
<span data-ttu-id="479d1-106">Remove-AzureRmEventHubNamespaceAuthorizationRule cmdlet은 지정 된 이벤트 허브 네임 스페이스에서 지정한 권한 부여 규칙을 제거 하 고 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="479d1-106">The Remove-AzureRmEventHubNamespaceAuthorizationRule cmdlet removes and deletes the specified authorization rule on the given Event Hubs namespace.</span></span>

## <span data-ttu-id="479d1-107">예제의</span><span class="sxs-lookup"><span data-stu-id="479d1-107">EXAMPLES</span></span>

### <span data-ttu-id="479d1-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="479d1-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHubNamespaceAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName
```

<span data-ttu-id="479d1-109">\` \` 네임 스페이스 MyNamespaceName에서 권한 부여 규칙 MyAuthRuleName를 제거 합니다 \` \` .</span><span class="sxs-lookup"><span data-stu-id="479d1-109">Removes the authorization rule \`MyAuthRuleName\` from the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="479d1-110">변수</span><span class="sxs-lookup"><span data-stu-id="479d1-110">PARAMETERS</span></span>

### <span data-ttu-id="479d1-111">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="479d1-111">-AuthorizationRuleName</span></span>
<span data-ttu-id="479d1-112">이벤트 허브 네임 스페이스 권한 부여 규칙 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="479d1-112">The Event Hubs namespace authorization rule name.</span></span>

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

### <span data-ttu-id="479d1-113">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="479d1-113">-NamespaceName</span></span>
<span data-ttu-id="479d1-114">이벤트 허브 네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="479d1-114">The Event Hubs namespace name.</span></span>

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

### <span data-ttu-id="479d1-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="479d1-115">-ResourceGroupName</span></span>
<span data-ttu-id="479d1-116">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="479d1-116">Resource group name.</span></span>

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

### <span data-ttu-id="479d1-117">-확인</span><span class="sxs-lookup"><span data-stu-id="479d1-117">-Confirm</span></span>
<span data-ttu-id="479d1-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="479d1-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="479d1-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="479d1-119">-WhatIf</span></span>
<span data-ttu-id="479d1-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="479d1-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="479d1-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="479d1-121">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="479d1-122">입력</span><span class="sxs-lookup"><span data-stu-id="479d1-122">INPUTS</span></span>

### <span data-ttu-id="479d1-123">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="479d1-123">System.String</span></span>

## <span data-ttu-id="479d1-124">출력</span><span class="sxs-lookup"><span data-stu-id="479d1-124">OUTPUTS</span></span>

### <span data-ttu-id="479d1-125">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="479d1-125">System.Boolean</span></span>

## <span data-ttu-id="479d1-126">상속자</span><span class="sxs-lookup"><span data-stu-id="479d1-126">NOTES</span></span>

## <span data-ttu-id="479d1-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="479d1-127">RELATED LINKS</span></span>

