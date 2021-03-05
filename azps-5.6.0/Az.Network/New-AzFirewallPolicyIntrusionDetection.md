---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallpolicyintrusiondetection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyIntrusionDetection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyIntrusionDetection.md
ms.openlocfilehash: 3587917e1a4216445e59b182ce6307c7a94684bf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996492"
---
# <span data-ttu-id="ed62c-101">New-AzFirewallPolicyIntrusionDetection</span><span class="sxs-lookup"><span data-stu-id="ed62c-101">New-AzFirewallPolicyIntrusionDetection</span></span>

## <span data-ttu-id="ed62c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed62c-102">SYNOPSIS</span></span>
<span data-ttu-id="ed62c-103">방화벽 정책과 연결하기 위해 새 Azure 방화벽 정책 침입 감지를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ed62c-103">Creates a new Azure Firewall Policy Intrusion Detection to associate with Firewall Policy</span></span>

## <span data-ttu-id="ed62c-104">구문</span><span class="sxs-lookup"><span data-stu-id="ed62c-104">SYNTAX</span></span>

```
New-AzFirewallPolicyIntrusionDetection -Mode <String>
 [-SignatureOverride <PSAzureFirewallPolicyIntrusionDetectionSignatureOverride[]>]
 [-BypassTraffic <PSAzureFirewallPolicyIntrusionDetectionBypassTrafficSetting[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed62c-105">설명</span><span class="sxs-lookup"><span data-stu-id="ed62c-105">DESCRIPTION</span></span>
<span data-ttu-id="ed62c-106">**New-AzFirewallPolicyIntrusionDetection** cmdlet은 Azure 방화벽 정책 침입 감지 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ed62c-106">The **New-AzFirewallPolicyIntrusionDetection** cmdlet creates an Azure Firewall Policy Intrusion Detection Object.</span></span>

## <span data-ttu-id="ed62c-107">예제</span><span class="sxs-lookup"><span data-stu-id="ed62c-107">EXAMPLES</span></span>

### <span data-ttu-id="ed62c-108">예제 1: 1.</span><span class="sxs-lookup"><span data-stu-id="ed62c-108">Example 1: 1.</span></span> <span data-ttu-id="ed62c-109">모드로 침입 감지 만들기</span><span class="sxs-lookup"><span data-stu-id="ed62c-109">Create intrusion detection with mode</span></span>
```powershell
PS C:\> New-AzFirewallPolicyIntrusionDetection -Mode "Alert"
```

<span data-ttu-id="ed62c-110">이 예제에서는 경고(검색) 모드를 통해 침입 감지를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ed62c-110">This example creates intrusion detection with Alert (detection) mode</span></span>

### <span data-ttu-id="ed62c-111">예제 2: 2.</span><span class="sxs-lookup"><span data-stu-id="ed62c-111">Example 2: 2.</span></span> <span data-ttu-id="ed62c-112">서명을 오버라이드하여 침입 감지 만들기</span><span class="sxs-lookup"><span data-stu-id="ed62c-112">Create intrusion detection with signature overrides</span></span>
```powershell
PS C:\> $signatureOverride = New-AzFirewallPolicyIntrusionDetectionSignatureOverride -Id "123456798" -Mode "Deny"
PS C:\> New-AzFirewallPolicyIntrusionDetection -Mode "Alert" -SignatureOverride $signatureOverride
```

<span data-ttu-id="ed62c-113">이 예제에서는 특정 서명을 오버라이드하여 침입 감지를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ed62c-113">This example creates intrusion detection with specific signature override</span></span>

### <span data-ttu-id="ed62c-114">예제 3: 3.</span><span class="sxs-lookup"><span data-stu-id="ed62c-114">Example 3: 3.</span></span> <span data-ttu-id="ed62c-115">우회 트래픽 설정으로 구성된 침입 감지를 사용하여 방화벽 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="ed62c-115">Create firewall policy with intrusion detection configured with bypass traffic setting</span></span>
```powershell
PS C:\> $bypass = New-AzFirewallPolicyIntrusionDetectionBypassTraffic -Name "bypass-setting" -Protocol "TCP" -DestinationPort "80" -SourceAddress "10.0.0.0" -DestinationAddress "10.0.0.0"
PS C:\> $intrusionDetection = New-AzFirewallPolicyIntrusionDetection -Mode "Deny" -BypassTraffic $bypass
PS C:\> New-AzFirewallPolicy -Name fp1 -Location "westus2" -ResourceGroup TestRg -SkuTier "Premium" -IntrusionDetection $intrusionDetection
```

<span data-ttu-id="ed62c-116">이 예제에서는 우회 트래픽 설정을 사용하여 침입 감지를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ed62c-116">This example creates intrusion detection with bypass traffic setting</span></span>

## <span data-ttu-id="ed62c-117">매개 변수</span><span class="sxs-lookup"><span data-stu-id="ed62c-117">PARAMETERS</span></span>

### <span data-ttu-id="ed62c-118">-BypassTraffic</span><span class="sxs-lookup"><span data-stu-id="ed62c-118">-BypassTraffic</span></span>
<span data-ttu-id="ed62c-119">우회할 트래픽에 대한 규칙 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="ed62c-119">List of rules for traffic to bypass.</span></span>

```yaml
Type: PSAzureFirewallPolicyIntrusionDetectionBypassTrafficSetting[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed62c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed62c-120">-DefaultProfile</span></span>
<span data-ttu-id="ed62c-121">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ed62c-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed62c-122">-Mode</span><span class="sxs-lookup"><span data-stu-id="ed62c-122">-Mode</span></span>
<span data-ttu-id="ed62c-123">침입 감지 일반 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="ed62c-123">Intrusion Detection general state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Off, Alert, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed62c-124">-SignatureOverride</span><span class="sxs-lookup"><span data-stu-id="ed62c-124">-SignatureOverride</span></span>
<span data-ttu-id="ed62c-125">특정 서명 상태 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="ed62c-125">List of specific signatures states.</span></span>

```yaml
Type: PSAzureFirewallPolicyIntrusionDetectionSignatureOverride[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed62c-126">-확인</span><span class="sxs-lookup"><span data-stu-id="ed62c-126">-Confirm</span></span>
<span data-ttu-id="ed62c-127">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ed62c-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed62c-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed62c-128">-WhatIf</span></span>
<span data-ttu-id="ed62c-129">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="ed62c-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed62c-130">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ed62c-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed62c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed62c-131">CommonParameters</span></span>
<span data-ttu-id="ed62c-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ed62c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed62c-133">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ed62c-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed62c-134">입력</span><span class="sxs-lookup"><span data-stu-id="ed62c-134">INPUTS</span></span>

### <span data-ttu-id="ed62c-135">없음</span><span class="sxs-lookup"><span data-stu-id="ed62c-135">None</span></span>

## <span data-ttu-id="ed62c-136">출력</span><span class="sxs-lookup"><span data-stu-id="ed62c-136">OUTPUTS</span></span>

### <span data-ttu-id="ed62c-137">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyIntrusionDetection</span><span class="sxs-lookup"><span data-stu-id="ed62c-137">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyIntrusionDetection</span></span>

## <span data-ttu-id="ed62c-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ed62c-138">NOTES</span></span>

## <span data-ttu-id="ed62c-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ed62c-139">RELATED LINKS</span></span>
