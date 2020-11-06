---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/get-azurermrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayAuthorizationRule.md
ms.openlocfilehash: 333e3eeaaf7655c78d557eb104fa4a349a0c05e7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526623"
---
# <span data-ttu-id="8d597-101">Get-AzureRmRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="8d597-101">Get-AzureRmRelayAuthorizationRule</span></span>

## <span data-ttu-id="8d597-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d597-102">SYNOPSIS</span></span>
<span data-ttu-id="8d597-103">지정 된 릴레이 엔터티에 대해 지정 된 권한 부여 규칙에 대 한 설명을 가져옵니다 (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="8d597-103">Gets the description of a specified authorization rule for a given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8d597-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8d597-104">SYNTAX</span></span>

### <span data-ttu-id="8d597-105">NamespaceAuthorizationRuleSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="8d597-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8d597-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="8d597-106">WcfRelayAuthorizationRuleSet</span></span>
```
Get-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8d597-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="8d597-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Get-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>]
 [-HybridConnection] <String> [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8d597-108">설명은</span><span class="sxs-lookup"><span data-stu-id="8d597-108">DESCRIPTION</span></span>
<span data-ttu-id="8d597-109">**AzureRmRelayAuthorizationRule** cmdlet은 주어진 릴레이 엔터티에서 지정 된 권한 부여 규칙에 대 한 설명을 가져옵니다 (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="8d597-109">The **Get-AzureRmRelayAuthorizationRule** cmdlet gets the description of the specified authorization rule in the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="8d597-110">예제의</span><span class="sxs-lookup"><span data-stu-id="8d597-110">EXAMPLES</span></span>

### <span data-ttu-id="8d597-111">예제 1-네임 스페이스</span><span class="sxs-lookup"><span data-stu-id="8d597-111">Example 1 - Namespace</span></span>
```
PS C:\> Get-AzureRmRelayNamespaceAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1
```

<span data-ttu-id="8d597-112">지정 된 네임 스페이스에 대 한 지정 된 권한 부여 규칙 설명을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d597-112">Returns the specified authorization rule description for a specified namespace.</span></span>

### <span data-ttu-id="8d597-113">예제 2-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="8d597-113">Example 2 - WcfRelay</span></span>
```
PS C:\>Get-AzureRmWcfRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1
```

<span data-ttu-id="8d597-114">지정 된 WcfRelay에 대 한 지정 된 권한 부여 규칙 설명을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d597-114">Returns the specified authorization rule description for a given WcfRelay.</span></span>

### <span data-ttu-id="8d597-115">예제 3-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="8d597-115">Example 3 - HybridConnection</span></span>
```
PS C:\> Get-AzureRmRelayHybridConnectionAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnections TestHybridConnection -Name AuthoRule1
```

<span data-ttu-id="8d597-116">지정 된 HybridConnection에 대 한 지정 된 권한 부여 규칙 설명을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d597-116">Returns the specified authorization rule description for a given HybridConnection.</span></span>

## <span data-ttu-id="8d597-117">변수</span><span class="sxs-lookup"><span data-stu-id="8d597-117">PARAMETERS</span></span>

### <span data-ttu-id="8d597-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d597-118">-DefaultProfile</span></span>
<span data-ttu-id="8d597-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8d597-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8d597-120">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="8d597-120">-HybridConnection</span></span>
<span data-ttu-id="8d597-121">HybridConnection 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8d597-121">HybridConnection Name.</span></span>

```yaml
Type: String
Parameter Sets: HybridConnectionAuthorizationRuleSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d597-122">-이름</span><span class="sxs-lookup"><span data-stu-id="8d597-122">-Name</span></span>
<span data-ttu-id="8d597-123">AuthorizationRule 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8d597-123">AuthorizationRule Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d597-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="8d597-124">-Namespace</span></span>
<span data-ttu-id="8d597-125">네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8d597-125">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: NamespaceAuthorizationRuleSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d597-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d597-126">-ResourceGroupName</span></span>
<span data-ttu-id="8d597-127">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8d597-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="8d597-128">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="8d597-128">-WcfRelay</span></span>
<span data-ttu-id="8d597-129">WcfRelay 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8d597-129">WcfRelay Name.</span></span>

```yaml
Type: String
Parameter Sets: WcfRelayAuthorizationRuleSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d597-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d597-130">CommonParameters</span></span>
<span data-ttu-id="8d597-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d597-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d597-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d597-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d597-133">입력</span><span class="sxs-lookup"><span data-stu-id="8d597-133">INPUTS</span></span>

### <span data-ttu-id="8d597-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d597-134">-ResourceGroupName</span></span>
 <span data-ttu-id="8d597-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8d597-135">System.String</span></span> 

### <span data-ttu-id="8d597-136">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="8d597-136">-NamespaceName</span></span>
 <span data-ttu-id="8d597-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8d597-137">System.String</span></span> 
 

### <span data-ttu-id="8d597-138">-HybridConnectionsName</span><span class="sxs-lookup"><span data-stu-id="8d597-138">-HybridConnectionsName</span></span>
 <span data-ttu-id="8d597-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8d597-139">System.String</span></span> 

### <span data-ttu-id="8d597-140">-WcfRelayName</span><span class="sxs-lookup"><span data-stu-id="8d597-140">-WcfRelayName</span></span>
 <span data-ttu-id="8d597-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8d597-141">System.String</span></span> 

### <span data-ttu-id="8d597-142">-이름</span><span class="sxs-lookup"><span data-stu-id="8d597-142">-Name</span></span>
 <span data-ttu-id="8d597-143">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8d597-143">System.String</span></span>

## <span data-ttu-id="8d597-144">출력</span><span class="sxs-lookup"><span data-stu-id="8d597-144">OUTPUTS</span></span>

### <span data-ttu-id="8d597-145">System.webserver. List ' 1 [[Microsoft Azure. l t e. 모델. AuthorizationRuleAttributes, Microsoft Azure. Commands, Version = 0.1.0.0, Culture = 중립, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="8d597-145">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Relay.Models.AuthorizationRuleAttributes, Microsoft.Azure.Commands.Relay, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="8d597-146">예제 1-네임 스페이스</span><span class="sxs-lookup"><span data-stu-id="8d597-146">Example 1 - Namespace</span></span>
<span data-ttu-id="8d597-147">권한: {Listen, Send} 이름: AuthoRule1 Type: Microsoft. 릴레이/AuthorizationRules Id:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/Aut hoRule1</span><span class="sxs-lookup"><span data-stu-id="8d597-147">Rights : {Listen, Send} Name   : AuthoRule1 Type   : Microsoft.Relay/AuthorizationRules Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/Aut hoRule1</span></span>

### <span data-ttu-id="8d597-148">예제 2-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="8d597-148">Example 2 - WcfRelay</span></span>
<span data-ttu-id="8d597-149">권한: {Listen, Send} 이름: AuthoRule1 Type: Microsoft. Relay/AuthorizationRules Id:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay 1/authorizationRules/AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="8d597-149">Rights : {Listen, Send} Name   : AuthoRule1 Type   : Microsoft.Relay/AuthorizationRules Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay 1/authorizationRules/AuthoRule1</span></span>

### <span data-ttu-id="8d597-150">예제 3-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="8d597-150">Example 3 - HybridConnection</span></span>
<span data-ttu-id="8d597-151">권한: {Listen, Send} 이름: AuthoRule1 Type: Microsoft. Relay/AuthorizationRules Id:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/Test HybridConnection/authorizationRules/AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="8d597-151">Rights : {Listen, Send} Name   : AuthoRule1 Type   : Microsoft.Relay/AuthorizationRules Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/Test HybridConnection/authorizationRules/AuthoRule1</span></span>

## <span data-ttu-id="8d597-152">상속자</span><span class="sxs-lookup"><span data-stu-id="8d597-152">NOTES</span></span>

## <span data-ttu-id="8d597-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8d597-153">RELATED LINKS</span></span>

