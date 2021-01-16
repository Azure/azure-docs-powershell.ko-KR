---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/get-azrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayAuthorizationRule.md
ms.openlocfilehash: af83820d33b9f36d93cc7623001d22a6cb5e0212
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98357190"
---
# <span data-ttu-id="f9667-101">Get-AzRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="f9667-101">Get-AzRelayAuthorizationRule</span></span>

## <span data-ttu-id="f9667-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f9667-102">SYNOPSIS</span></span>
<span data-ttu-id="f9667-103">지정된 Relay 엔터티(네임스페이스/WcfRelay/HybridConnection)에 대해 지정된 권한 부여 규칙에 대한 설명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f9667-103">Gets the description of a specified authorization rule for a given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="f9667-104">구문</span><span class="sxs-lookup"><span data-stu-id="f9667-104">SYNTAX</span></span>

### <span data-ttu-id="f9667-105">NamespaceAuthorizationRuleSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="f9667-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f9667-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="f9667-106">WcfRelayAuthorizationRuleSet</span></span>
```
Get-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f9667-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="f9667-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Get-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f9667-108">설명</span><span class="sxs-lookup"><span data-stu-id="f9667-108">DESCRIPTION</span></span>
<span data-ttu-id="f9667-109">**Get-AzRelayAuthorizationRule** cmdlet은 지정된 Relay 엔터티(네임스페이스/WcfRelay/HybridConnection)에서 지정된 권한 부여 규칙에 대한 설명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f9667-109">The **Get-AzRelayAuthorizationRule** cmdlet gets the description of the specified authorization rule in the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="f9667-110">예제</span><span class="sxs-lookup"><span data-stu-id="f9667-110">EXAMPLES</span></span>

### <span data-ttu-id="f9667-111">예제 1: 네임스페이스</span><span class="sxs-lookup"><span data-stu-id="f9667-111">Example 1: Namespace</span></span>
```powershell
PS C:\> Get-AzRelayNamespaceAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/Aut
         hoRule1
```

<span data-ttu-id="f9667-112">지정된 네임스페이스에 대해 지정된 권한 부여 규칙 설명을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="f9667-112">Returns the specified authorization rule description for a specified namespace.</span></span>

### <span data-ttu-id="f9667-113">예제 2: WcfRelay</span><span class="sxs-lookup"><span data-stu-id="f9667-113">Example 2: WcfRelay</span></span>
```powershell
PS C:\>Get-AzWcfRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay
         1/authorizationRules/AuthoRule1
```

<span data-ttu-id="f9667-114">지정된 WcfRelay에 대해 지정된 권한 부여 규칙 설명을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="f9667-114">Returns the specified authorization rule description for a given WcfRelay.</span></span>

### <span data-ttu-id="f9667-115">예제 3: HybridConnection</span><span class="sxs-lookup"><span data-stu-id="f9667-115">Example 3: HybridConnection</span></span>
```powershell
PS C:\> Get-AzRelayHybridConnectionAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnections TestHybridConnection -Name AuthoRule1

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/Test
         HybridConnection/authorizationRules/AuthoRule1
```

<span data-ttu-id="f9667-116">지정된 HybridConnection에 대해 지정된 권한 부여 규칙 설명을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="f9667-116">Returns the specified authorization rule description for a given HybridConnection.</span></span>

## <span data-ttu-id="f9667-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f9667-117">PARAMETERS</span></span>

### <span data-ttu-id="f9667-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9667-118">-DefaultProfile</span></span>
<span data-ttu-id="f9667-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f9667-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9667-120">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="f9667-120">-HybridConnection</span></span>
<span data-ttu-id="f9667-121">HybridConnection 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f9667-121">HybridConnection Name.</span></span>

```yaml
Type: System.String
Parameter Sets: HybridConnectionAuthorizationRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9667-122">-Name</span><span class="sxs-lookup"><span data-stu-id="f9667-122">-Name</span></span>
<span data-ttu-id="f9667-123">AuthorizationRule 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f9667-123">AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9667-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="f9667-124">-Namespace</span></span>
<span data-ttu-id="f9667-125">네임스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f9667-125">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceAuthorizationRuleSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9667-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9667-126">-ResourceGroupName</span></span>
<span data-ttu-id="f9667-127">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f9667-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="f9667-128">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="f9667-128">-WcfRelay</span></span>
<span data-ttu-id="f9667-129">WcfRelay 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f9667-129">WcfRelay Name.</span></span>

```yaml
Type: System.String
Parameter Sets: WcfRelayAuthorizationRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9667-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9667-130">CommonParameters</span></span>
<span data-ttu-id="f9667-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f9667-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9667-132">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="f9667-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9667-133">입력</span><span class="sxs-lookup"><span data-stu-id="f9667-133">INPUTS</span></span>

### <span data-ttu-id="f9667-134">System.String</span><span class="sxs-lookup"><span data-stu-id="f9667-134">System.String</span></span>

## <span data-ttu-id="f9667-135">출력</span><span class="sxs-lookup"><span data-stu-id="f9667-135">OUTPUTS</span></span>

### <span data-ttu-id="f9667-136">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="f9667-136">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="f9667-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f9667-137">NOTES</span></span>

## <span data-ttu-id="f9667-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f9667-138">RELATED LINKS</span></span>
