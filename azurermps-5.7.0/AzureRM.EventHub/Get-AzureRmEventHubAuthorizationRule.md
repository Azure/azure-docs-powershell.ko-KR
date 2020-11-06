---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/get-azurermeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubAuthorizationRule.md
ms.openlocfilehash: 4d162122b82f592472fb31f1087db29faedf08cd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534823"
---
# <span data-ttu-id="8fe2d-101">Get-AzureRmEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="8fe2d-101">Get-AzureRmEventHubAuthorizationRule</span></span>

## <span data-ttu-id="8fe2d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8fe2d-102">SYNOPSIS</span></span>
<span data-ttu-id="8fe2d-103">권한 부여 규칙의 세부 정보를 가져오거나 권한 부여 규칙 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8fe2d-103">Gets the details of an authorization rule, or gets a list of authorization rules.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8fe2d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8fe2d-104">SYNTAX</span></span>

### <span data-ttu-id="8fe2d-105">NamespaceAuthorizationRuleSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="8fe2d-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8fe2d-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="8fe2d-106">EventhubAuthorizationRuleSet</span></span>
```
Get-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Eventhub] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8fe2d-107">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="8fe2d-107">AliasAuthoRuleSet</span></span>
```
Get-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8fe2d-108">설명은</span><span class="sxs-lookup"><span data-stu-id="8fe2d-108">DESCRIPTION</span></span>
<span data-ttu-id="8fe2d-109">Get-AzureRmEventHubAuthorizationRule cmdlet은 권한 부여 규칙의 세부 정보나 지정 된 이벤트 허브에 대 한 모든 권한 부여 규칙의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8fe2d-109">The Get-AzureRmEventHubAuthorizationRule cmdlet gets either the details of an authorization rule, or a list of all authorization rules for a specified Event Hub.</span></span>
<span data-ttu-id="8fe2d-110">권한 부여 규칙의 이름을 제공 하는 경우 해당 단일 인증 규칙의 세부 정보가 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8fe2d-110">If the name of an authorization rule is provided, the details of that single authorization rule are returned.</span></span>
<span data-ttu-id="8fe2d-111">권한 부여 규칙의 이름을 제공 하지 않으면 지정 된 이벤트 허브에 대 한 모든 권한 부여 규칙 목록이 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8fe2d-111">If the name of an authorization rule is not provided, a list of all authorization rules for the specified Event Hub is returned.</span></span>
<span data-ttu-id="8fe2d-112">(재해 복구) 별칭 이름이 제공 되 면 별칭에 대 한 네임 스페이스의 권한 부여 규칙에 대 한 세부 정보가 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8fe2d-112">If (Disaster Recovery) Alias name provided, the details of authorization rule of the Namespace for Alias configured is returned.</span></span> 

## <span data-ttu-id="8fe2d-113">예제의</span><span class="sxs-lookup"><span data-stu-id="8fe2d-113">EXAMPLES</span></span>

### <span data-ttu-id="8fe2d-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="8fe2d-114">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRule MyAuthRuleName
```

<span data-ttu-id="8fe2d-115">\` \` \` \` 네임 스페이스 MyNamespaceName로 범위가 지정 된 이벤트 허브 MyEventHubName에서 \` 권한 부여 규칙 MyAuthRuleName를 가져옵니다 \` .</span><span class="sxs-lookup"><span data-stu-id="8fe2d-115">Gets the authorization rule \`MyAuthRuleName\` in the Event Hub \`MyEventHubName\`, which is scoped by the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="8fe2d-116">예제 2</span><span class="sxs-lookup"><span data-stu-id="8fe2d-116">Example 2</span></span>
```
PS C:\> Get-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="8fe2d-117">\` \` MyNamespaceName 네임 스페이스의 범위를 지정 하는 이벤트 허브 MyEventHubName의 모든 권한 부여 규칙 목록을 가져옵니다 \` \` .</span><span class="sxs-lookup"><span data-stu-id="8fe2d-117">Gets a list of all authorization rules in the Event Hub \`MyEventHubName\`, which is scoped by the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="8fe2d-118">예제 3</span><span class="sxs-lookup"><span data-stu-id="8fe2d-118">Example 3</span></span>
```
PS C:\> Get-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AliasName MyAliasNameName -Name MyAuthRuleName
```

<span data-ttu-id="8fe2d-119">\` \` 네임 스페이스 MyNamespaceName에서 MyAuthRuleName 권한 부여 규칙을 가져옵니다 \` \` .</span><span class="sxs-lookup"><span data-stu-id="8fe2d-119">Gets the authorization rule \`MyAuthRuleName\` in the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="8fe2d-120">변수</span><span class="sxs-lookup"><span data-stu-id="8fe2d-120">PARAMETERS</span></span>

### <span data-ttu-id="8fe2d-121">-AliasName</span><span class="sxs-lookup"><span data-stu-id="8fe2d-121">-AliasName</span></span>
<span data-ttu-id="8fe2d-122">별칭 이름</span><span class="sxs-lookup"><span data-stu-id="8fe2d-122">Alias Name</span></span>

```yaml
Type: String
Parameter Sets: AliasAuthoRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fe2d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fe2d-123">-DefaultProfile</span></span>
<span data-ttu-id="8fe2d-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8fe2d-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fe2d-125">-Eventhub</span><span class="sxs-lookup"><span data-stu-id="8fe2d-125">-Eventhub</span></span>
<span data-ttu-id="8fe2d-126">Eventhub 이름</span><span class="sxs-lookup"><span data-stu-id="8fe2d-126">Eventhub Name</span></span>

```yaml
Type: String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fe2d-127">-이름</span><span class="sxs-lookup"><span data-stu-id="8fe2d-127">-Name</span></span>
<span data-ttu-id="8fe2d-128">AuthorizationRule 이름</span><span class="sxs-lookup"><span data-stu-id="8fe2d-128">AuthorizationRule Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fe2d-129">-Namespace</span><span class="sxs-lookup"><span data-stu-id="8fe2d-129">-Namespace</span></span>
<span data-ttu-id="8fe2d-130">네임 스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="8fe2d-130">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fe2d-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8fe2d-131">-ResourceGroupName</span></span>
<span data-ttu-id="8fe2d-132">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="8fe2d-132">Resource Group Name</span></span>

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

### <span data-ttu-id="8fe2d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fe2d-133">CommonParameters</span></span>
<span data-ttu-id="8fe2d-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8fe2d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="8fe2d-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8fe2d-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fe2d-136">입력</span><span class="sxs-lookup"><span data-stu-id="8fe2d-136">INPUTS</span></span>

### <span data-ttu-id="8fe2d-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8fe2d-137">System.String</span></span>


## <span data-ttu-id="8fe2d-138">출력</span><span class="sxs-lookup"><span data-stu-id="8fe2d-138">OUTPUTS</span></span>

### <span data-ttu-id="8fe2d-139">System.webserver. List ' 1 [[Microsoft Azure.]. PSSharedAccessAuthorizationRuleAttributes, Microsoft Azure. Commands. EventHub, Version = 0.5.0.0, Culture = 중립, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="8fe2d-139">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes, Microsoft.Azure.Commands.EventHub, Version=0.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>


## <span data-ttu-id="8fe2d-140">상속자</span><span class="sxs-lookup"><span data-stu-id="8fe2d-140">NOTES</span></span>

## <span data-ttu-id="8fe2d-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8fe2d-141">RELATED LINKS</span></span>
