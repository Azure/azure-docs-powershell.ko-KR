---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusNetworkRuleSet.md
ms.openlocfilehash: 6c803f399bf88c6e4887441ec9f9bd50c058361b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034757"
---
# <span data-ttu-id="eea08-101">Remove-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="eea08-101">Remove-AzServiceBusNetworkRuleSet</span></span>

## <span data-ttu-id="eea08-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eea08-102">SYNOPSIS</span></span>
<span data-ttu-id="eea08-103">지정 된 네임 스페이스에 대 한 네트워크 규칙 집합을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="eea08-103">Removes the NetworkRuleSet for the Given Namespace</span></span>

## <span data-ttu-id="eea08-104">구문과</span><span class="sxs-lookup"><span data-stu-id="eea08-104">SYNTAX</span></span>

### <span data-ttu-id="eea08-105">Networkruleset속성 집합 (기본값)</span><span class="sxs-lookup"><span data-stu-id="eea08-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eea08-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="eea08-106">NamespaceInputObjectSet</span></span>
```
Remove-AzServiceBusNetworkRuleSet [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eea08-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="eea08-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Remove-AzServiceBusNetworkRuleSet [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eea08-108">설명은</span><span class="sxs-lookup"><span data-stu-id="eea08-108">DESCRIPTION</span></span>
<span data-ttu-id="eea08-109">지정 된 네임 스페이스에 대 한 네트워크 규칙 집합을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="eea08-109">Removes the NetworkRuleSet for the Given Namespace</span></span>

## <span data-ttu-id="eea08-110">예제의</span><span class="sxs-lookup"><span data-stu-id="eea08-110">EXAMPLES</span></span>

### <span data-ttu-id="eea08-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="eea08-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusNetworkRuleSet -ResourceGroupName  v-ajnavtest -Namespace ServiceBus-Namespace1-1375
```

<span data-ttu-id="eea08-112">Name: 기본 DefaultAction: Allow Id:/subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1375/networkRuleSets/default Type: Microsoft ServiceBus/네임 스페이스/네트워크 규칙 집합 IpRules: VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="eea08-112">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1375/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 

<span data-ttu-id="eea08-113">지정 된 "ServiceBus-Namespace1-1375" 네임 스페이스에 대 한 NetworkRuleSet를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="eea08-113">Deletes the NetworkRuleSet for the Given "ServiceBus-Namespace1-1375" namespace</span></span> 

### <span data-ttu-id="eea08-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="eea08-114">Example 2</span></span>
```powershell
PS C:\> Remove-AzServiceBusNetworkRuleSet -InputObject $result1375
```
<span data-ttu-id="eea08-115">Name: 기본 DefaultAction: Allow Id:/subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace-1375/networkRuleSets/default Type: Microsoft. EventHub/네임 스페이스/NetworkRuleSet 집합 IpRules: VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="eea08-115">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace-1375/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 

<span data-ttu-id="eea08-116">InputObject를 사용 하 여 NetworkRuleSet 집합을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="eea08-116">Deletes the NetworkRuleSet using InputObject</span></span> 

### <span data-ttu-id="eea08-117">예제 3</span><span class="sxs-lookup"><span data-stu-id="eea08-117">Example 3</span></span>
```powershell
PS C:\> Remove-AzServiceBusNetworkRuleSet -ResourceId /SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace1-1375
```
<span data-ttu-id="eea08-118">Name: 기본 DefaultAction: Allow Id:/subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace-1375/networkRuleSets/default Type: Microsoft. EventHub/네임 스페이스/NetworkRuleSet 집합 IpRules: VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="eea08-118">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace-1375/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 

<span data-ttu-id="eea08-119">네임 스페이스 ResourceId를 사용 하 여 네트워크 규칙 집합을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="eea08-119">Deletes the NetworkRuleSet using ResourceId of the Namespace</span></span>


## <span data-ttu-id="eea08-120">변수</span><span class="sxs-lookup"><span data-stu-id="eea08-120">PARAMETERS</span></span>

### <span data-ttu-id="eea08-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eea08-121">-AsJob</span></span>
<span data-ttu-id="eea08-122">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="eea08-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="eea08-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eea08-123">-DefaultProfile</span></span>
<span data-ttu-id="eea08-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="eea08-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eea08-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eea08-125">-InputObject</span></span>
<span data-ttu-id="eea08-126">네임 스페이스 개체</span><span class="sxs-lookup"><span data-stu-id="eea08-126">Namespace Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eea08-127">-이름</span><span class="sxs-lookup"><span data-stu-id="eea08-127">-Name</span></span>
<span data-ttu-id="eea08-128">네임 스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="eea08-128">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eea08-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eea08-129">-PassThru</span></span>
<span data-ttu-id="eea08-130">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="eea08-130">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="eea08-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eea08-131">-ResourceGroupName</span></span>
<span data-ttu-id="eea08-132">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="eea08-132">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eea08-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eea08-133">-ResourceId</span></span>
<span data-ttu-id="eea08-134">네임 스페이스 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="eea08-134">Namespace Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eea08-135">-확인</span><span class="sxs-lookup"><span data-stu-id="eea08-135">-Confirm</span></span>
<span data-ttu-id="eea08-136">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="eea08-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eea08-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eea08-137">-WhatIf</span></span>
<span data-ttu-id="eea08-138">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="eea08-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eea08-139">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="eea08-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eea08-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eea08-140">CommonParameters</span></span>
<span data-ttu-id="eea08-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="eea08-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="eea08-142">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eea08-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eea08-143">입력</span><span class="sxs-lookup"><span data-stu-id="eea08-143">INPUTS</span></span>

### <span data-ttu-id="eea08-144">ServiceBus. PSNamespaceAttributes/.</span><span class="sxs-lookup"><span data-stu-id="eea08-144">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

### <span data-ttu-id="eea08-145">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="eea08-145">System.String</span></span>

## <span data-ttu-id="eea08-146">출력</span><span class="sxs-lookup"><span data-stu-id="eea08-146">OUTPUTS</span></span>

### <span data-ttu-id="eea08-147">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="eea08-147">System.Boolean</span></span>

## <span data-ttu-id="eea08-148">상속자</span><span class="sxs-lookup"><span data-stu-id="eea08-148">NOTES</span></span>

## <span data-ttu-id="eea08-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="eea08-149">RELATED LINKS</span></span>