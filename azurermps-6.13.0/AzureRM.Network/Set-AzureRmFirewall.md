---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 40E56EC1-3327-4DFF-8262-E2EEBB5E4447
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmFirewall.md
ms.openlocfilehash: 8f2c2560ac8ca0787a8a0eb8d37fb5242f4a915e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524379"
---
# <span data-ttu-id="c11f4-101">Set-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="c11f4-101">Set-AzureRmFirewall</span></span>

## <span data-ttu-id="c11f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c11f4-102">SYNOPSIS</span></span>
<span data-ttu-id="c11f4-103">수정 된 방화벽을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="c11f4-103">Saves a modified Firewall.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c11f4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c11f4-104">SYNTAX</span></span>

```
Set-AzureRmFirewall -AzureFirewall <PSAzureFirewall> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c11f4-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c11f4-105">DESCRIPTION</span></span>
<span data-ttu-id="c11f4-106">**AzureRmFirewall** Cmdlet은 Azure 방화벽을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="c11f4-106">The **Set-AzureRmFirewall** cmdlet updates an Azure Firewall.</span></span>

## <span data-ttu-id="c11f4-107">예제의</span><span class="sxs-lookup"><span data-stu-id="c11f4-107">EXAMPLES</span></span>

### <span data-ttu-id="c11f4-108">1: 방화벽 응용 프로그램 규칙 모음의 우선 순위 업데이트</span><span class="sxs-lookup"><span data-stu-id="c11f4-108">1:  Update priority of a Firewall application rule collection</span></span>
```
$azFw = Get-AzureRmFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$ruleCollection = $azFw.GetApplicationRuleCollectionByName("ruleCollectionName")
$ruleCollection.Priority = 101
Set-AzureRmFirewall -Firewall $azFw
```

<span data-ttu-id="c11f4-109">이 예제에서는 Azure 방화벽의 기존 규칙 컬렉션에 대 한 우선 순위를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="c11f4-109">This example updates the priority of an existing rule collection of an Azure Firewall.</span></span>
<span data-ttu-id="c11f4-110">"Rg" 리소스 그룹의 Azure 방화벽 "AzureFirewall"에 "ruleCollectionName" 이라는 응용 프로그램 규칙 컬렉션이 포함 되어 있는 경우 위의 명령은 해당 규칙 모음의 우선 순위를 변경 하 고 나중에 Azure 방화벽을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="c11f4-110">Assuming Azure Firewall "AzureFirewall" in resource group "rg" contains an application rule collection named "ruleCollectionName", the commands above will change the priority of that rule collection and update the Azure Firewall afterwards.</span></span> <span data-ttu-id="c11f4-111">Set-AzureRmFirewall 명령이 없으면 로컬 $azFw 개체에서 수행 된 모든 작업이 서버에 반영 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c11f4-111">Without the Set-AzureRmFirewall command, all operations performed on the local $azFw object are not reflected on the server.</span></span>

### <span data-ttu-id="c11f4-112">2: Azure 방화벽을 만들고 나중에 응용 프로그램 규칙 컬렉션 설정</span><span class="sxs-lookup"><span data-stu-id="c11f4-112">2:  Create a Azure Firewall and set an application rule collection later</span></span>
```
$azFw = New-AzureRmFirewall -Name "AzureFirewall" -ResourceGroupName "rg" -VirtualNetworkName "vnet-name" -PublicIpName "pip-name"

$rule = New-AzureRmFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$RuleCollection = New-AzureRmFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
$azFw.ApplicationRuleCollections = $RuleCollection

$azFw | Set-AzureRmFirewall
```

<span data-ttu-id="c11f4-113">이 예제에서는 응용 프로그램 규칙 컬렉션 없이 방화벽을 먼저 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c11f4-113">In this example, a Firewall is created first without any application rule collections.</span></span> <span data-ttu-id="c11f4-114">나중에 응용 프로그램 규칙과 응용 프로그램 규칙 컬렉션이 만들어지고, 방화벽 개체는 클라우드의 실제 구성에 영향을 주지 않고 메모리에서 수정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c11f4-114">Afterwards a Application Rule and Application Rule Collection are created, then the Firewall object is modified in memory, without affecting the real configuration in cloud.</span></span> <span data-ttu-id="c11f4-115">클라우드에 변경 내용을 반영 하려면 Set-AzureRmFirewall를 호출 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c11f4-115">For changes to be reflected in cloud, Set-AzureRmFirewall must be called.</span></span>

## <span data-ttu-id="c11f4-116">변수</span><span class="sxs-lookup"><span data-stu-id="c11f4-116">PARAMETERS</span></span>

### <span data-ttu-id="c11f4-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c11f4-117">-AsJob</span></span>
<span data-ttu-id="c11f4-118">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="c11f4-118">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c11f4-119">-AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="c11f4-119">-AzureFirewall</span></span>
<span data-ttu-id="c11f4-120">AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="c11f4-120">The AzureFirewall</span></span>

```yaml
Type: PSAzureFirewall
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c11f4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c11f4-121">-DefaultProfile</span></span>
<span data-ttu-id="c11f4-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c11f4-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c11f4-123">-확인</span><span class="sxs-lookup"><span data-stu-id="c11f4-123">-Confirm</span></span>
<span data-ttu-id="c11f4-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c11f4-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c11f4-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c11f4-125">-WhatIf</span></span>
<span data-ttu-id="c11f4-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c11f4-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c11f4-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c11f4-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c11f4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c11f4-128">CommonParameters</span></span>
<span data-ttu-id="c11f4-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c11f4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c11f4-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c11f4-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c11f4-131">입력</span><span class="sxs-lookup"><span data-stu-id="c11f4-131">INPUTS</span></span>

### <span data-ttu-id="c11f4-132">PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="c11f4-132">PSAzureFirewall</span></span>
<span data-ttu-id="c11f4-133">' AzureFirewall ' 매개 변수는 파이프라인에서 ' PSAzureFirewall ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c11f4-133">Parameter 'AzureFirewall' accepts value of type 'PSAzureFirewall' from the pipeline</span></span>

## <span data-ttu-id="c11f4-134">출력</span><span class="sxs-lookup"><span data-stu-id="c11f4-134">OUTPUTS</span></span>

### <span data-ttu-id="c11f4-135">Microsoft. \* PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="c11f4-135">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="c11f4-136">상속자</span><span class="sxs-lookup"><span data-stu-id="c11f4-136">NOTES</span></span>

## <span data-ttu-id="c11f4-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c11f4-137">RELATED LINKS</span></span>

[<span data-ttu-id="c11f4-138">Get-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="c11f4-138">Get-AzureRmFirewall</span></span>](./Get-AzureRmFirewall.md)

[<span data-ttu-id="c11f4-139">새로운 AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="c11f4-139">New-AzureRmFirewall</span></span>](./New-AzureRmFirewall.md)

[<span data-ttu-id="c11f4-140">제거-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="c11f4-140">Remove-AzureRmFirewall</span></span>](./Remove-AzureRmFirewall.md)
