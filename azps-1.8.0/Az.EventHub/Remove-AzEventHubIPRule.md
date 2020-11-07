---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubiprule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubIPRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubIPRule.md
ms.openlocfilehash: 81ef5519face98b8a2a01787fa8d3f1ee97dff0f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93700827"
---
# <span data-ttu-id="05c81-101">Remove-AzEventHubIPRule</span><span class="sxs-lookup"><span data-stu-id="05c81-101">Remove-AzEventHubIPRule</span></span>

## <span data-ttu-id="05c81-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05c81-102">SYNOPSIS</span></span>
<span data-ttu-id="05c81-103">지정 된 네임 스페이스의 NetworkRuleSet에 대 한 단일 삭제 규칙 제거</span><span class="sxs-lookup"><span data-stu-id="05c81-103">Remove a single IPrule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="05c81-104">구문과</span><span class="sxs-lookup"><span data-stu-id="05c81-104">SYNTAX</span></span>

### <span data-ttu-id="05c81-105">IPRulePropertiesParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="05c81-105">IPRulePropertiesParameterSet (Default)</span></span>
```
Remove-AzEventHubIPRule [-ResourceGroupName] <String> [-Name] <String> [-IpMask] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05c81-106">IPRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="05c81-106">IPRuleInputObjectParameterSet</span></span>
```
Remove-AzEventHubIPRule [-ResourceGroupName] <String> [-Name] <String>
 [-IpRuleObject] <PSNWRuleSetIpRulesAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="05c81-107">설명은</span><span class="sxs-lookup"><span data-stu-id="05c81-107">DESCRIPTION</span></span>
<span data-ttu-id="05c81-108">지정 된 네임 스페이스의 NetworkRuleSet에 대 한 단일 삭제 규칙 제거</span><span class="sxs-lookup"><span data-stu-id="05c81-108">Remove a single IPrule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="05c81-109">예제의</span><span class="sxs-lookup"><span data-stu-id="05c81-109">EXAMPLES</span></span>

### <span data-ttu-id="05c81-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="05c81-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubIPRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -IpMask "11.22.33.44"
```

<span data-ttu-id="05c81-111">지정 된 네임 스페이스의 네트워크 규칙 집합에 대 한 IpMask를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="05c81-111">Removes IpMask of the NetworkRuleSet of the given namespace</span></span>

## <span data-ttu-id="05c81-112">변수</span><span class="sxs-lookup"><span data-stu-id="05c81-112">PARAMETERS</span></span>

### <span data-ttu-id="05c81-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="05c81-113">-AsJob</span></span>
<span data-ttu-id="05c81-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="05c81-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="05c81-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05c81-115">-DefaultProfile</span></span>
<span data-ttu-id="05c81-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="05c81-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="05c81-117">-IpMask</span><span class="sxs-lookup"><span data-stu-id="05c81-117">-IpMask</span></span>
<span data-ttu-id="05c81-118">서브넷 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="05c81-118">Subnet Resource ID</span></span>

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

### <span data-ttu-id="05c81-119">-IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="05c81-119">-IpRuleObject</span></span>
<span data-ttu-id="05c81-120">IPRule 구성 개체</span><span class="sxs-lookup"><span data-stu-id="05c81-120">IPRule Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes
Parameter Sets: IPRuleInputObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="05c81-121">-이름</span><span class="sxs-lookup"><span data-stu-id="05c81-121">-Name</span></span>
<span data-ttu-id="05c81-122">네임 스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="05c81-122">Namespace Name</span></span>

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

### <span data-ttu-id="05c81-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="05c81-123">-PassThru</span></span>
<span data-ttu-id="05c81-124">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="05c81-124">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="05c81-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05c81-125">-ResourceGroupName</span></span>
<span data-ttu-id="05c81-126">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="05c81-126">Resource Group Name</span></span>

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

### <span data-ttu-id="05c81-127">-확인</span><span class="sxs-lookup"><span data-stu-id="05c81-127">-Confirm</span></span>
<span data-ttu-id="05c81-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="05c81-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05c81-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05c81-129">-WhatIf</span></span>
<span data-ttu-id="05c81-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="05c81-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05c81-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="05c81-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05c81-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05c81-132">CommonParameters</span></span>
<span data-ttu-id="05c81-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="05c81-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="05c81-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05c81-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05c81-135">입력</span><span class="sxs-lookup"><span data-stu-id="05c81-135">INPUTS</span></span>

### <span data-ttu-id="05c81-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="05c81-136">System.String</span></span>

### <span data-ttu-id="05c81-137">PSNWRuleSetIpRulesAttributes (.).</span><span class="sxs-lookup"><span data-stu-id="05c81-137">Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes</span></span>

## <span data-ttu-id="05c81-138">출력</span><span class="sxs-lookup"><span data-stu-id="05c81-138">OUTPUTS</span></span>

### <span data-ttu-id="05c81-139">Microsoft. \*. a. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="05c81-139">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="05c81-140">상속자</span><span class="sxs-lookup"><span data-stu-id="05c81-140">NOTES</span></span>

## <span data-ttu-id="05c81-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="05c81-141">RELATED LINKS</span></span>