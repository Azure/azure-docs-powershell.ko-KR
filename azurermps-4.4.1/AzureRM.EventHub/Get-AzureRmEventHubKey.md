---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubKey.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: f4f28ee3f07127803e6187f00565ee8d4caf3084
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537263"
---
# <span data-ttu-id="65d50-101">Get-AzureRmEventHubKey</span><span class="sxs-lookup"><span data-stu-id="65d50-101">Get-AzureRmEventHubKey</span></span>

## <span data-ttu-id="65d50-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65d50-102">SYNOPSIS</span></span>
<span data-ttu-id="65d50-103">지정 된 이벤트 허브 권한 부여 규칙의 기본 키 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="65d50-103">Gets the primary key details of the specified Event Hubs authorization rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="65d50-104">구문과</span><span class="sxs-lookup"><span data-stu-id="65d50-104">SYNTAX</span></span>

### <span data-ttu-id="65d50-105">NamespaceAuthorizationRuleSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="65d50-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmEventHubKey [-ResourceGroupName] <String> -Namespace <String> -Name <String>
```

### <span data-ttu-id="65d50-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="65d50-106">EventhubAuthorizationRuleSet</span></span>
```
Get-AzureRmEventHubKey [-ResourceGroupName] <String> [-Namespace <String>] -EventHub <String> -Name <String>
```

## <span data-ttu-id="65d50-107">설명은</span><span class="sxs-lookup"><span data-stu-id="65d50-107">DESCRIPTION</span></span>
<span data-ttu-id="65d50-108">Get-AzureRmEventHubKey cmdlet은 지정 된 이벤트 허브 권한 부여 규칙에 대 한 기본 및 보조 connectionstrings 및 키 세부 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="65d50-108">The Get-AzureRmEventHubKey cmdlet returns Primary and Secondary connectionstrings and keys details of the specified Event Hubs authorization rule.</span></span>

## <span data-ttu-id="65d50-109">예제의</span><span class="sxs-lookup"><span data-stu-id="65d50-109">EXAMPLES</span></span>

### <span data-ttu-id="65d50-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="65d50-110">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName
```

<span data-ttu-id="65d50-111">권한 부여 규칙 MyAuthRuleName에 대 한 기본 및 보조 connectionstrings 및 키의 세부 정보를 가져옵니다 \` \` .</span><span class="sxs-lookup"><span data-stu-id="65d50-111">Gets details of Primary and Secondary connectionstrings and keys for the authorization rule \`MyAuthRuleName\`.</span></span>

## <span data-ttu-id="65d50-112">변수</span><span class="sxs-lookup"><span data-stu-id="65d50-112">PARAMETERS</span></span>

### <span data-ttu-id="65d50-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65d50-113">-ResourceGroupName</span></span>
<span data-ttu-id="65d50-114">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="65d50-114">Resource group name.</span></span>

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

### <span data-ttu-id="65d50-115">-EventHub</span><span class="sxs-lookup"><span data-stu-id="65d50-115">-EventHub</span></span>
<span data-ttu-id="65d50-116">EventHub 이름.</span><span class="sxs-lookup"><span data-stu-id="65d50-116">EventHub Name.</span></span>

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

### <span data-ttu-id="65d50-117">-이름</span><span class="sxs-lookup"><span data-stu-id="65d50-117">-Name</span></span>
<span data-ttu-id="65d50-118">AuthorizationRule 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="65d50-118">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="65d50-119">-Namespace</span><span class="sxs-lookup"><span data-stu-id="65d50-119">-Namespace</span></span>
<span data-ttu-id="65d50-120">네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="65d50-120">Namespace Name.</span></span>

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

## <span data-ttu-id="65d50-121">입력</span><span class="sxs-lookup"><span data-stu-id="65d50-121">INPUTS</span></span>

### <span data-ttu-id="65d50-122">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="65d50-122">System.String</span></span>

## <span data-ttu-id="65d50-123">출력</span><span class="sxs-lookup"><span data-stu-id="65d50-123">OUTPUTS</span></span>

### <span data-ttu-id="65d50-124">ListKeysAttributes (.).</span><span class="sxs-lookup"><span data-stu-id="65d50-124">Microsoft.Azure.Commands.EventHub.Models.ListKeysAttributes</span></span>

## <span data-ttu-id="65d50-125">상속자</span><span class="sxs-lookup"><span data-stu-id="65d50-125">NOTES</span></span>

## <span data-ttu-id="65d50-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="65d50-126">RELATED LINKS</span></span>

