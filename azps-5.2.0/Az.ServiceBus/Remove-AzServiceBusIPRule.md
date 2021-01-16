---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusiprule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusIPRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusIPRule.md
ms.openlocfilehash: 90c832d36017aa02a05d972a7b6e26fffd93937e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98358478"
---
# <span data-ttu-id="ae407-101">Remove-AzServiceBusIPRule</span><span class="sxs-lookup"><span data-stu-id="ae407-101">Remove-AzServiceBusIPRule</span></span>

## <span data-ttu-id="ae407-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae407-102">SYNOPSIS</span></span>
<span data-ttu-id="ae407-103">주어진 네임스페이스의 NetworkRuleSet에 대한 단일 IP 규칙 제거</span><span class="sxs-lookup"><span data-stu-id="ae407-103">Remove a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="ae407-104">구문</span><span class="sxs-lookup"><span data-stu-id="ae407-104">SYNTAX</span></span>

### <span data-ttu-id="ae407-105">IPRulePropertiesParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="ae407-105">IPRulePropertiesParameterSet (Default)</span></span>
```
Remove-AzServiceBusIPRule [-ResourceGroupName] <String> [-Name] <String> [-IpMask] <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae407-106">IPRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ae407-106">IPRuleInputObjectParameterSet</span></span>
```
Remove-AzServiceBusIPRule [-ResourceGroupName] <String> [-Name] <String>
 [-IpRuleObject] <PSNWRuleSetIpRulesAttributes> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae407-107">설명</span><span class="sxs-lookup"><span data-stu-id="ae407-107">DESCRIPTION</span></span>
<span data-ttu-id="ae407-108">주어진 네임스페이스의 NetworkRuleSet에 대한 단일 IP 규칙 제거</span><span class="sxs-lookup"><span data-stu-id="ae407-108">Remove a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="ae407-109">예제</span><span class="sxs-lookup"><span data-stu-id="ae407-109">EXAMPLES</span></span>

### <span data-ttu-id="ae407-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="ae407-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusIPRule -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-2389 -IpMask "11.22.33.44"
```

<span data-ttu-id="ae407-111">주어진 네임스페이스의 NetworkRuleSet의 IpMask를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="ae407-111">Removes IpMask of the NetworkRuleSet of the given namespace</span></span>

## <span data-ttu-id="ae407-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ae407-112">PARAMETERS</span></span>

### <span data-ttu-id="ae407-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ae407-113">-AsJob</span></span>
<span data-ttu-id="ae407-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="ae407-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ae407-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae407-115">-DefaultProfile</span></span>
<span data-ttu-id="ae407-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ae407-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae407-117">-IpMask</span><span class="sxs-lookup"><span data-stu-id="ae407-117">-IpMask</span></span>
<span data-ttu-id="ae407-118">서브넷 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="ae407-118">Subnet Resource ID</span></span>

```yaml
Type: System.String
Parameter Sets: IPRulePropertiesParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae407-119">-IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="ae407-119">-IpRuleObject</span></span>
<span data-ttu-id="ae407-120">IPRule 구성 개체</span><span class="sxs-lookup"><span data-stu-id="ae407-120">IPRule Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes
Parameter Sets: IPRuleInputObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ae407-121">-Name</span><span class="sxs-lookup"><span data-stu-id="ae407-121">-Name</span></span>
<span data-ttu-id="ae407-122">네임스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="ae407-122">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae407-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ae407-123">-PassThru</span></span>
<span data-ttu-id="ae407-124">{{PassThru 설명 채우기}}</span><span class="sxs-lookup"><span data-stu-id="ae407-124">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="ae407-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae407-125">-ResourceGroupName</span></span>
<span data-ttu-id="ae407-126">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="ae407-126">Resource Group Name</span></span>

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

### <span data-ttu-id="ae407-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ae407-127">-Confirm</span></span>
<span data-ttu-id="ae407-128">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ae407-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae407-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae407-129">-WhatIf</span></span>
<span data-ttu-id="ae407-130">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="ae407-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae407-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ae407-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae407-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae407-132">CommonParameters</span></span>
<span data-ttu-id="ae407-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ae407-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="ae407-134">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="ae407-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae407-135">입력</span><span class="sxs-lookup"><span data-stu-id="ae407-135">INPUTS</span></span>

### <span data-ttu-id="ae407-136">System.String</span><span class="sxs-lookup"><span data-stu-id="ae407-136">System.String</span></span>

### <span data-ttu-id="ae407-137">Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="ae407-137">Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes</span></span>

## <span data-ttu-id="ae407-138">출력</span><span class="sxs-lookup"><span data-stu-id="ae407-138">OUTPUTS</span></span>

### <span data-ttu-id="ae407-139">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="ae407-139">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="ae407-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ae407-140">NOTES</span></span>

## <span data-ttu-id="ae407-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ae407-141">RELATED LINKS</span></span>
