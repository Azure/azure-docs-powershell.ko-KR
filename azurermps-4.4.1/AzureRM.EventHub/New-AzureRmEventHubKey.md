---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubKey.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 3bd06ea2534298ba81cd546e8fa6e8de02fa5928
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537243"
---
# <span data-ttu-id="f9bd3-101">New-AzureRmEventHubKey</span><span class="sxs-lookup"><span data-stu-id="f9bd3-101">New-AzureRmEventHubKey</span></span>

## <span data-ttu-id="f9bd3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f9bd3-102">SYNOPSIS</span></span>
<span data-ttu-id="f9bd3-103">지정 된 이벤트 허브 권한 부여 규칙에 대 한 새 기본 또는 보조 키를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f9bd3-103">Creates a new primary or secondary key for the specified Event Hubs authorization rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f9bd3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f9bd3-104">SYNTAX</span></span>

### <span data-ttu-id="f9bd3-105">NamespaceAuthorizationRuleSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="f9bd3-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzureRmEventHubKey -ResourceGroupName <String> -Namespace <String> -Name <String> -RegenerateKey <String>
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="f9bd3-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="f9bd3-106">EventhubAuthorizationRuleSet</span></span>
```
New-AzureRmEventHubKey -ResourceGroupName <String> [-Namespace <String>] -EventHub <String> -Name <String>
 -RegenerateKey <String> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="f9bd3-107">설명은</span><span class="sxs-lookup"><span data-stu-id="f9bd3-107">DESCRIPTION</span></span>
<span data-ttu-id="f9bd3-108">New-AzureRmEventHubKey cmdlet은 지정 된 이벤트 허브 권한 부여 규칙에 대 한 기본 또는 보조 SAS 키를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9bd3-108">The New-AzureRmEventHubKey cmdlet regenerates the primary or secondary SAS key for the specified Event Hubs authorization rule.</span></span>

## <span data-ttu-id="f9bd3-109">예제의</span><span class="sxs-lookup"><span data-stu-id="f9bd3-109">EXAMPLES</span></span>

### <span data-ttu-id="f9bd3-110">예제 1.1</span><span class="sxs-lookup"><span data-stu-id="f9bd3-110">Example 1.1</span></span>
```
PS C:\> New-AzureRmEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName -RegenerateKey PrimaryKey
```

<span data-ttu-id="f9bd3-111">권한 부여 규칙 MyAuthRuleName에 대 한 기본 키를 다시 생성 \` \` 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9bd3-111">Regenerates the primary key for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="f9bd3-112">예제 1.2</span><span class="sxs-lookup"><span data-stu-id="f9bd3-112">Example 1.2</span></span>
```
PS C:\> New-AzureRmEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName -RegenerateKey PrimaryKey
```

<span data-ttu-id="f9bd3-113">권한 부여 규칙 MyAuthRuleName에 대 한 기본 키를 다시 생성 \` \` 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9bd3-113">Regenerates the primary key for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="f9bd3-114">예제 2.1</span><span class="sxs-lookup"><span data-stu-id="f9bd3-114">Example 2.1</span></span>
```
PS C:\> New-AzureRmEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName -RegenerateKey SecondaryKey
```

### <span data-ttu-id="f9bd3-115">예제 2.2</span><span class="sxs-lookup"><span data-stu-id="f9bd3-115">Example 2.2</span></span>
```
PS C:\> New-AzureRmEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName -RegenerateKey SecondaryKey
```

<span data-ttu-id="f9bd3-116">권한 부여 규칙 MyAuthRuleName에 대 한 보조 키를 다시 생성 \` \` 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9bd3-116">Regenerates the secondary key for the authorization rule \`MyAuthRuleName\`.</span></span>

## <span data-ttu-id="f9bd3-117">변수</span><span class="sxs-lookup"><span data-stu-id="f9bd3-117">PARAMETERS</span></span>

### <span data-ttu-id="f9bd3-118">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="f9bd3-118">-RegenerateKey</span></span>
<span data-ttu-id="f9bd3-119">다시 생성 하는 키: \` PrimaryKey \` 또는 \` secondarykey \` 입니다.</span><span class="sxs-lookup"><span data-stu-id="f9bd3-119">Key to regenerate: \`PrimaryKey\` or \`SecondaryKey\`.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9bd3-120">-확인</span><span class="sxs-lookup"><span data-stu-id="f9bd3-120">-Confirm</span></span>
<span data-ttu-id="f9bd3-121">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9bd3-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9bd3-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9bd3-122">-WhatIf</span></span>
<span data-ttu-id="f9bd3-123">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f9bd3-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9bd3-124">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f9bd3-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9bd3-125">-EventHub</span><span class="sxs-lookup"><span data-stu-id="f9bd3-125">-EventHub</span></span>
<span data-ttu-id="f9bd3-126">EventHub 이름.</span><span class="sxs-lookup"><span data-stu-id="f9bd3-126">EventHub Name.</span></span>

```yaml
Type: String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: EventHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9bd3-127">-이름</span><span class="sxs-lookup"><span data-stu-id="f9bd3-127">-Name</span></span>
<span data-ttu-id="f9bd3-128">AuthorizationRule 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f9bd3-128">AuthorizationRule Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9bd3-129">-Namespace</span><span class="sxs-lookup"><span data-stu-id="f9bd3-129">-Namespace</span></span>
<span data-ttu-id="f9bd3-130">네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f9bd3-130">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: NamespaceAuthorizationRuleSet
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: NamespaceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9bd3-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9bd3-131">-ResourceGroupName</span></span>
<span data-ttu-id="f9bd3-132">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f9bd3-132">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="f9bd3-133">입력</span><span class="sxs-lookup"><span data-stu-id="f9bd3-133">INPUTS</span></span>

### <span data-ttu-id="f9bd3-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f9bd3-134">System.String</span></span>

## <span data-ttu-id="f9bd3-135">출력</span><span class="sxs-lookup"><span data-stu-id="f9bd3-135">OUTPUTS</span></span>

### <span data-ttu-id="f9bd3-136">ListKeysAttributes (.).</span><span class="sxs-lookup"><span data-stu-id="f9bd3-136">Microsoft.Azure.Commands.EventHub.Models.ListKeysAttributes</span></span>

## <span data-ttu-id="f9bd3-137">상속자</span><span class="sxs-lookup"><span data-stu-id="f9bd3-137">NOTES</span></span>

## <span data-ttu-id="f9bd3-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f9bd3-138">RELATED LINKS</span></span>

