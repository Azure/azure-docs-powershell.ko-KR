---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespaceAuthorizationRule.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: bad0e86061a5ffaa937209d778d5eaa83e29879d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711574"
---
# <span data-ttu-id="a6a8b-101">Get-AzureRmEventHubNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="a6a8b-101">Get-AzureRmEventHubNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="a6a8b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6a8b-102">SYNOPSIS</span></span>
<span data-ttu-id="a6a8b-103">Eventubs 네임 스페이스 권한 부여 규칙의 세부 정보를 가져오거나 권한 부여 규칙의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a6a8b-103">Gets the details of an Eventubs namespace authorization rule, or gets a list of authorization rules.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a6a8b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a6a8b-104">SYNTAX</span></span>

```
Get-AzureRmEventHubNamespaceAuthorizationRule [-ResourceGroupName] <String> [-NamespaceName] <String>
 [[-AuthorizationRuleName] <String>]
```

## <span data-ttu-id="a6a8b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a6a8b-105">DESCRIPTION</span></span>
<span data-ttu-id="a6a8b-106">Get-AzureRmEventHubNamespaceAuthorizationRule cmdlet은 지정 된 이벤트 허브 네임 스페이스 권한 부여 규칙 또는 네임 스페이스 권한 부여 규칙 목록에 대 한 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a6a8b-106">The Get-AzureRmEventHubNamespaceAuthorizationRule cmdlet gets either the details of a specified Event Hubs namespace authorization rule, or a list of namespace authorization rules.</span></span>
<span data-ttu-id="a6a8b-107">권한 부여 규칙 이름을 제공 하는 경우 단일 인증 규칙의 세부 정보가 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a6a8b-107">If the authorization rule name is provided, the details of a single authorization rule is returned.</span></span>
<span data-ttu-id="a6a8b-108">권한 부여 규칙 이름을 제공 하지 않으면 네임 스페이스의 모든 권한 부여 규칙 목록이 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a6a8b-108">If an authorization rule name is not provided, a list of all authorization rules in the namespace is returned.</span></span>

## <span data-ttu-id="a6a8b-109">예제의</span><span class="sxs-lookup"><span data-stu-id="a6a8b-109">EXAMPLES</span></span>

### <span data-ttu-id="a6a8b-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="a6a8b-110">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubNamespaceAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName
```

<span data-ttu-id="a6a8b-111">\` \` \` \` 리소스 그룹 MyResourceGroupName를 사용 하 여 이벤트 허브 네임 스페이스 MyNamespaceName에 있는 \` 권한 부여 규칙 MyAuthRuleName를 반환 합니다 \` .</span><span class="sxs-lookup"><span data-stu-id="a6a8b-111">Returns the authorization rule \`MyAuthRuleName\` in the Event Hubs namespace \`MyNamespaceName\`, with the resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="a6a8b-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="a6a8b-112">Example 2</span></span>
```
PS C:\> Get-AzureRmEventHubNamespaceAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName RootManageSharedAccessKey
```

<span data-ttu-id="a6a8b-113">\` \` \` \` 리소스 그룹 MyResourceGroupName를 사용 하 여 이벤트 허브 네임 스페이스 MyNamespaceName에서 \` 기본 권한 부여 규칙 RootManageSharedAccessKey를 반환 합니다 \` .</span><span class="sxs-lookup"><span data-stu-id="a6a8b-113">Returns the default authorization rule \`RootManageSharedAccessKey\` in the Event Hubs namespace \`MyNamespaceName\`, with the resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="a6a8b-114">예제 3</span><span class="sxs-lookup"><span data-stu-id="a6a8b-114">Example 3</span></span>
```
PS C:\> Get-AzureRmEventHubNamespaceAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName
```

<span data-ttu-id="a6a8b-115">\` \` 리소스 그룹 MyResourceGroupName를 사용 하 여 이벤트 허브 네임 스페이스 MyNamespaceName의 모든 권한 부여 규칙을 반환 합니다 \` \` .</span><span class="sxs-lookup"><span data-stu-id="a6a8b-115">Returns all authorization rules in the Event Hubs namespace \`MyNamespaceName\`, with the resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="a6a8b-116">변수</span><span class="sxs-lookup"><span data-stu-id="a6a8b-116">PARAMETERS</span></span>

### <span data-ttu-id="a6a8b-117">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="a6a8b-117">-AuthorizationRuleName</span></span>
<span data-ttu-id="a6a8b-118">이벤트 허브 네임 스페이스 권한 부여 규칙 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a6a8b-118">The Event Hubs namespace authorization rule name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6a8b-119">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="a6a8b-119">-NamespaceName</span></span>
<span data-ttu-id="a6a8b-120">이벤트 허브 네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a6a8b-120">The Event Hubs namespace name.</span></span>

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

### <span data-ttu-id="a6a8b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6a8b-121">-ResourceGroupName</span></span>
<span data-ttu-id="a6a8b-122">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a6a8b-122">Resource group name.</span></span>

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

## <span data-ttu-id="a6a8b-123">입력</span><span class="sxs-lookup"><span data-stu-id="a6a8b-123">INPUTS</span></span>

### <span data-ttu-id="a6a8b-124">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a6a8b-124">System.String</span></span>

## <span data-ttu-id="a6a8b-125">출력</span><span class="sxs-lookup"><span data-stu-id="a6a8b-125">OUTPUTS</span></span>

### <span data-ttu-id="a6a8b-126">System.webserver. List ' 1 [[Microsoft Azure.]. a n [[0.0.1.0]. SharedAccessAuthorizationRuleAttributes, Microsoft Azure. 명령. EventHub, Version =, Culture = 중립, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="a6a8b-126">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventHub.Models.SharedAccessAuthorizationRuleAttributes, Microsoft.Azure.Commands.EventHub, Version=0.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="a6a8b-127">상속자</span><span class="sxs-lookup"><span data-stu-id="a6a8b-127">NOTES</span></span>

## <span data-ttu-id="a6a8b-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a6a8b-128">RELATED LINKS</span></span>

