---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusNetworkRuleSet.md
ms.openlocfilehash: df8e85505a7aa62b883ecdc0536f9b3cd1352109
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699162"
---
# <span data-ttu-id="610ff-101">Remove-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="610ff-101">Remove-AzServiceBusNetworkRuleSet</span></span>

## <span data-ttu-id="610ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="610ff-102">SYNOPSIS</span></span>
<span data-ttu-id="610ff-103">지정 된 네임 스페이스에 대 한 NetwrokRuleSet를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="610ff-103">Removes the NetwrokRuleSet for the Given Namespace</span></span>

## <span data-ttu-id="610ff-104">구문과</span><span class="sxs-lookup"><span data-stu-id="610ff-104">SYNTAX</span></span>

### <span data-ttu-id="610ff-105">Networkruleset속성 집합 (기본값)</span><span class="sxs-lookup"><span data-stu-id="610ff-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="610ff-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="610ff-106">NamespaceInputObjectSet</span></span>
```
Remove-AzServiceBusNetworkRuleSet [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="610ff-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="610ff-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Remove-AzServiceBusNetworkRuleSet [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="610ff-108">설명은</span><span class="sxs-lookup"><span data-stu-id="610ff-108">DESCRIPTION</span></span>
<span data-ttu-id="610ff-109">지정 된 네임 스페이스에 대 한 NetwrokRuleSet를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="610ff-109">Removes the NetwrokRuleSet for the Given Namespace</span></span>

## <span data-ttu-id="610ff-110">예제의</span><span class="sxs-lookup"><span data-stu-id="610ff-110">EXAMPLES</span></span>

### <span data-ttu-id="610ff-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="610ff-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusNetworkRuleSet -ResourceGroupName  v-ajnavtest -Namespace ServiceBus-Namespace1-1375
```

<span data-ttu-id="610ff-112">Name: 기본 DefaultAction: Allow Id:/subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1375/networkRuleSets/default Type: Microsoft ServiceBus/네임 스페이스/네트워크 규칙 집합 IpRules: VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="610ff-112">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1375/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 

<span data-ttu-id="610ff-113">지정 된 "ServiceBus-Namespace1-1375" namesapce에 대 한 NetwrokRuleSet를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="610ff-113">Deletes the NetwrokRuleSet for the Given "ServiceBus-Namespace1-1375" namesapce</span></span> 

### <span data-ttu-id="610ff-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="610ff-114">Example 2</span></span>
```powershell
PS C:\> Remove-AzServiceBusNetworkRuleSet -InputObject $result1375
```
<span data-ttu-id="610ff-115">Name: 기본 DefaultAction: Allow Id:/subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace-1375/networkRuleSets/default Type: Microsoft. EventHub/네임 스페이스/NetworkRuleSet 집합 IpRules: VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="610ff-115">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace-1375/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 

<span data-ttu-id="610ff-116">InputObject를 사용 하 여 NetwrokRuleSet를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="610ff-116">Deletes the NetwrokRuleSet using InputObject</span></span> 

### <span data-ttu-id="610ff-117">예제 3</span><span class="sxs-lookup"><span data-stu-id="610ff-117">Example 3</span></span>
```powershell
PS C:\> Remove-AzServiceBusNetworkRuleSet -ResourceId /SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace1-1375
```
<span data-ttu-id="610ff-118">Name: 기본 DefaultAction: Allow Id:/subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace-1375/networkRuleSets/default Type: Microsoft. EventHub/네임 스페이스/NetworkRuleSet 집합 IpRules: VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="610ff-118">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace-1375/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 

<span data-ttu-id="610ff-119">Namepsace의 ResourceId를 사용 하 여 NetwrokRuleSet를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="610ff-119">Deletes the NetwrokRuleSet using ResourceId of the Namepsace</span></span>


## <span data-ttu-id="610ff-120">변수</span><span class="sxs-lookup"><span data-stu-id="610ff-120">PARAMETERS</span></span>

### <span data-ttu-id="610ff-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="610ff-121">-AsJob</span></span>
<span data-ttu-id="610ff-122">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="610ff-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="610ff-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="610ff-123">-DefaultProfile</span></span>
<span data-ttu-id="610ff-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="610ff-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="610ff-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="610ff-125">-InputObject</span></span>
<span data-ttu-id="610ff-126">네임 스페이스 개체</span><span class="sxs-lookup"><span data-stu-id="610ff-126">Namespace Object</span></span>

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

### <span data-ttu-id="610ff-127">-이름</span><span class="sxs-lookup"><span data-stu-id="610ff-127">-Name</span></span>
<span data-ttu-id="610ff-128">네임 스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="610ff-128">Namespace Name</span></span>

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

### <span data-ttu-id="610ff-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="610ff-129">-PassThru</span></span>
<span data-ttu-id="610ff-130">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="610ff-130">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="610ff-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="610ff-131">-ResourceGroupName</span></span>
<span data-ttu-id="610ff-132">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="610ff-132">Resource Group Name</span></span>

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

### <span data-ttu-id="610ff-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="610ff-133">-ResourceId</span></span>
<span data-ttu-id="610ff-134">네임 스페이스 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="610ff-134">Namespace Resource Id</span></span>

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

### <span data-ttu-id="610ff-135">-확인</span><span class="sxs-lookup"><span data-stu-id="610ff-135">-Confirm</span></span>
<span data-ttu-id="610ff-136">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="610ff-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="610ff-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="610ff-137">-WhatIf</span></span>
<span data-ttu-id="610ff-138">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="610ff-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="610ff-139">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="610ff-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="610ff-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="610ff-140">CommonParameters</span></span>
<span data-ttu-id="610ff-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="610ff-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="610ff-142">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="610ff-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="610ff-143">입력</span><span class="sxs-lookup"><span data-stu-id="610ff-143">INPUTS</span></span>

### <span data-ttu-id="610ff-144">ServiceBus. PSNamespaceAttributes/.</span><span class="sxs-lookup"><span data-stu-id="610ff-144">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

### <span data-ttu-id="610ff-145">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="610ff-145">System.String</span></span>

## <span data-ttu-id="610ff-146">출력</span><span class="sxs-lookup"><span data-stu-id="610ff-146">OUTPUTS</span></span>

### <span data-ttu-id="610ff-147">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="610ff-147">System.Boolean</span></span>

## <span data-ttu-id="610ff-148">상속자</span><span class="sxs-lookup"><span data-stu-id="610ff-148">NOTES</span></span>

## <span data-ttu-id="610ff-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="610ff-149">RELATED LINKS</span></span>
