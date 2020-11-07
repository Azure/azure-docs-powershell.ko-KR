---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 40E56EC1-3327-4DFF-8262-E2EEBB5E4447
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewall.md
ms.openlocfilehash: 7937af38c7dd0becd57604a0a7c00e5d1f584e6c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93700014"
---
# <span data-ttu-id="75a38-101">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="75a38-101">Set-AzFirewall</span></span>

## <span data-ttu-id="75a38-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75a38-102">SYNOPSIS</span></span>
<span data-ttu-id="75a38-103">수정 된 방화벽을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="75a38-103">Saves a modified Firewall.</span></span>

## <span data-ttu-id="75a38-104">구문과</span><span class="sxs-lookup"><span data-stu-id="75a38-104">SYNTAX</span></span>

```
Set-AzFirewall -AzureFirewall <PSAzureFirewall> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75a38-105">설명은</span><span class="sxs-lookup"><span data-stu-id="75a38-105">DESCRIPTION</span></span>
<span data-ttu-id="75a38-106">**AzFirewall** Cmdlet은 Azure 방화벽을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="75a38-106">The **Set-AzFirewall** cmdlet updates an Azure Firewall.</span></span>

## <span data-ttu-id="75a38-107">예제의</span><span class="sxs-lookup"><span data-stu-id="75a38-107">EXAMPLES</span></span>

### <span data-ttu-id="75a38-108">1: 방화벽 응용 프로그램 규칙 모음의 우선 순위 업데이트</span><span class="sxs-lookup"><span data-stu-id="75a38-108">1:  Update priority of a Firewall application rule collection</span></span>
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$ruleCollection = $azFw.GetApplicationRuleCollectionByName("ruleCollectionName")
$ruleCollection.Priority = 101
Set-AzFirewall -AzureFirewall $azFw
```

<span data-ttu-id="75a38-109">이 예제에서는 Azure 방화벽의 기존 규칙 컬렉션에 대 한 우선 순위를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="75a38-109">This example updates the priority of an existing rule collection of an Azure Firewall.</span></span>
<span data-ttu-id="75a38-110">"Rg" 리소스 그룹의 Azure 방화벽 "AzureFirewall"에 "ruleCollectionName" 이라는 응용 프로그램 규칙 컬렉션이 포함 되어 있는 경우 위의 명령은 해당 규칙 모음의 우선 순위를 변경 하 고 나중에 Azure 방화벽을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="75a38-110">Assuming Azure Firewall "AzureFirewall" in resource group "rg" contains an application rule collection named "ruleCollectionName", the commands above will change the priority of that rule collection and update the Azure Firewall afterwards.</span></span> <span data-ttu-id="75a38-111">Set-AzFirewall 명령이 없으면 로컬 $azFw 개체에서 수행 된 모든 작업이 서버에 반영 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="75a38-111">Without the Set-AzFirewall command, all operations performed on the local $azFw object are not reflected on the server.</span></span>

### <span data-ttu-id="75a38-112">2: Azure 방화벽을 만들고 나중에 응용 프로그램 규칙 컬렉션 설정</span><span class="sxs-lookup"><span data-stu-id="75a38-112">2:  Create a Azure Firewall and set an application rule collection later</span></span>
```
$azFw = New-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg" -VirtualNetworkName "vnet-name" -PublicIpName "pip-name"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$RuleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
$azFw.ApplicationRuleCollections = $RuleCollection

$azFw | Set-AzFirewall
```

<span data-ttu-id="75a38-113">이 예제에서는 응용 프로그램 규칙 컬렉션 없이 방화벽을 먼저 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="75a38-113">In this example, a Firewall is created first without any application rule collections.</span></span> <span data-ttu-id="75a38-114">나중에 응용 프로그램 규칙과 응용 프로그램 규칙 컬렉션이 만들어지고, 방화벽 개체는 클라우드의 실제 구성에 영향을 주지 않고 메모리에서 수정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="75a38-114">Afterwards a Application Rule and Application Rule Collection are created, then the Firewall object is modified in memory, without affecting the real configuration in cloud.</span></span> <span data-ttu-id="75a38-115">클라우드에 변경 내용을 반영 하려면 Set-AzFirewall를 호출 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="75a38-115">For changes to be reflected in cloud, Set-AzFirewall must be called.</span></span>

### <span data-ttu-id="75a38-116">3: Azure 방화벽의 위협 업데이트 인텔 작동 모드</span><span class="sxs-lookup"><span data-stu-id="75a38-116">3:  Update Threat Intel operation mode of Azure Firewall</span></span>
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.ThreatIntelMode = "Deny"
Set-AzFirewall -Firewall $azFw
```

<span data-ttu-id="75a38-117">이 예제에서는 리소스 그룹 "rg"에서 Azure 방화벽 "AzureFirewall"의 위협 Intel 작업 모드를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="75a38-117">This example updates the Threat Intel operation mode of Azure Firewall "AzureFirewall" in resource group "rg".</span></span>
<span data-ttu-id="75a38-118">Set-AzFirewall 명령이 없으면 로컬 $azFw 개체에서 수행 된 모든 작업이 서버에 반영 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="75a38-118">Without the Set-AzFirewall command, all operations performed on the local $azFw object are not reflected on the server.</span></span>

## <span data-ttu-id="75a38-119">변수</span><span class="sxs-lookup"><span data-stu-id="75a38-119">PARAMETERS</span></span>

### <span data-ttu-id="75a38-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="75a38-120">-AsJob</span></span>
<span data-ttu-id="75a38-121">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="75a38-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="75a38-122">-AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="75a38-122">-AzureFirewall</span></span>
<span data-ttu-id="75a38-123">AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="75a38-123">The AzureFirewall</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewall
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="75a38-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75a38-124">-DefaultProfile</span></span>
<span data-ttu-id="75a38-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="75a38-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="75a38-126">-확인</span><span class="sxs-lookup"><span data-stu-id="75a38-126">-Confirm</span></span>
<span data-ttu-id="75a38-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="75a38-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75a38-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75a38-128">-WhatIf</span></span>
<span data-ttu-id="75a38-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="75a38-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="75a38-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="75a38-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75a38-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75a38-131">CommonParameters</span></span>
<span data-ttu-id="75a38-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="75a38-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75a38-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75a38-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75a38-134">입력</span><span class="sxs-lookup"><span data-stu-id="75a38-134">INPUTS</span></span>

### <span data-ttu-id="75a38-135">Microsoft. \* PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="75a38-135">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="75a38-136">출력</span><span class="sxs-lookup"><span data-stu-id="75a38-136">OUTPUTS</span></span>

### <span data-ttu-id="75a38-137">Microsoft. \* PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="75a38-137">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="75a38-138">상속자</span><span class="sxs-lookup"><span data-stu-id="75a38-138">NOTES</span></span>

## <span data-ttu-id="75a38-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="75a38-139">RELATED LINKS</span></span>

[<span data-ttu-id="75a38-140">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="75a38-140">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="75a38-141">새로운 AzFirewall</span><span class="sxs-lookup"><span data-stu-id="75a38-141">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="75a38-142">제거-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="75a38-142">Remove-AzFirewall</span></span>](./Remove-AzFirewall.md)
