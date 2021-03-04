---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallpolicyintrusiondetectionbypasstraffic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyIntrusionDetectionBypassTraffic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyIntrusionDetectionBypassTraffic.md
ms.openlocfilehash: dd15a93fc2df022a0b016f9dae4845da13240534
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981696"
---
# <span data-ttu-id="e3d07-101">New-AzFirewallPolicyIntrusionDetectionBypassTraffic</span><span class="sxs-lookup"><span data-stu-id="e3d07-101">New-AzFirewallPolicyIntrusionDetectionBypassTraffic</span></span>

## <span data-ttu-id="e3d07-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3d07-102">SYNOPSIS</span></span>
<span data-ttu-id="e3d07-103">새 Azure 방화벽 정책 침입 감지 우회 트래픽 설정 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e3d07-103">Creates a new Azure Firewall Policy Intrusion Detection Bypass Traffic Setting</span></span>

## <span data-ttu-id="e3d07-104">구문</span><span class="sxs-lookup"><span data-stu-id="e3d07-104">SYNTAX</span></span>

```
New-AzFirewallPolicyIntrusionDetectionBypassTraffic -Name <String> [-Description <String>] -Protocol <String>
 [-SourceAddress <String[]>] [-DestinationAddress <String[]>] [-SourceIpGroup <String[]>]
 [-DestinationIpGroup <String[]>] -DestinationPort <String[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3d07-105">설명</span><span class="sxs-lookup"><span data-stu-id="e3d07-105">DESCRIPTION</span></span>
<span data-ttu-id="e3d07-106">**New-AzFirewallPolicyIntrusionDetectionBypassTraffic** cmdlet은 Azure 방화벽 정책 침입 감지 우회 트래픽 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e3d07-106">The **New-AzFirewallPolicyIntrusionDetectionBypassTraffic** cmdlet creates an Azure Firewall Policy Intrusion Detection Bypass Traffic Object.</span></span>

## <span data-ttu-id="e3d07-107">예제</span><span class="sxs-lookup"><span data-stu-id="e3d07-107">EXAMPLES</span></span>

### <span data-ttu-id="e3d07-108">예제 1: 1.</span><span class="sxs-lookup"><span data-stu-id="e3d07-108">Example 1: 1.</span></span> <span data-ttu-id="e3d07-109">특정 포트 및 원본 주소를 사용하여 우회 트래픽 만들기</span><span class="sxs-lookup"><span data-stu-id="e3d07-109">Create bypass traffic with specific port and source address</span></span>
```powershell
PS C:\> $bypass = New-AzFirewallPolicyIntrusionDetectionBypassTraffic -Name "bypass-setting" -Protocol "TCP" -DestinationPort "80" -SourceAddress "10.0.0.0" -DestinationAddress "*"
PS C:\> New-AzFirewallPolicyIntrusionDetection -Mode "Deny" -BypassTraffic $bypass
```

<span data-ttu-id="e3d07-110">이 예제에서는 우회 트래픽 설정을 사용하여 침입 감지를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e3d07-110">This example creates intrusion detection with bypass traffic setting</span></span>

## <span data-ttu-id="e3d07-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="e3d07-111">PARAMETERS</span></span>

### <span data-ttu-id="e3d07-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3d07-112">-DefaultProfile</span></span>
<span data-ttu-id="e3d07-113">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e3d07-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3d07-114">-Description</span><span class="sxs-lookup"><span data-stu-id="e3d07-114">-Description</span></span>
<span data-ttu-id="e3d07-115">설정 설명을 무시합니다.</span><span class="sxs-lookup"><span data-stu-id="e3d07-115">Bypass setting description.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3d07-116">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="e3d07-116">-DestinationAddress</span></span>
<span data-ttu-id="e3d07-117">대상 IP 주소 또는 범위 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="e3d07-117">List of destination IP addresses or ranges.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3d07-118">-DestinationIpGroup</span><span class="sxs-lookup"><span data-stu-id="e3d07-118">-DestinationIpGroup</span></span>
<span data-ttu-id="e3d07-119">대상 IpGroups 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="e3d07-119">List of destination IpGroups.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3d07-120">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="e3d07-120">-DestinationPort</span></span>
<span data-ttu-id="e3d07-121">대상 포트 또는 범위 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="e3d07-121">List of destination ports or ranges.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3d07-122">-Name</span><span class="sxs-lookup"><span data-stu-id="e3d07-122">-Name</span></span>
<span data-ttu-id="e3d07-123">설정 이름을 무시합니다.</span><span class="sxs-lookup"><span data-stu-id="e3d07-123">Bypass setting name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3d07-124">-Protocol</span><span class="sxs-lookup"><span data-stu-id="e3d07-124">-Protocol</span></span>
<span data-ttu-id="e3d07-125">설정 프로토콜을 무시합니다.</span><span class="sxs-lookup"><span data-stu-id="e3d07-125">Bypass setting protocol.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: TCP, UDP, ICMP, ANY

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3d07-126">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="e3d07-126">-SourceAddress</span></span>
<span data-ttu-id="e3d07-127">원본 IP 주소 또는 범위 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="e3d07-127">List of source IP addresses or ranges.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3d07-128">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="e3d07-128">-SourceIpGroup</span></span>
<span data-ttu-id="e3d07-129">원본 IpGroups 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="e3d07-129">List of source IpGroups.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3d07-130">-확인</span><span class="sxs-lookup"><span data-stu-id="e3d07-130">-Confirm</span></span>
<span data-ttu-id="e3d07-131">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e3d07-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3d07-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3d07-132">-WhatIf</span></span>
<span data-ttu-id="e3d07-133">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="e3d07-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3d07-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e3d07-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3d07-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3d07-135">CommonParameters</span></span>
<span data-ttu-id="e3d07-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e3d07-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3d07-137">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e3d07-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3d07-138">입력</span><span class="sxs-lookup"><span data-stu-id="e3d07-138">INPUTS</span></span>

### <span data-ttu-id="e3d07-139">없음</span><span class="sxs-lookup"><span data-stu-id="e3d07-139">None</span></span>

## <span data-ttu-id="e3d07-140">출력</span><span class="sxs-lookup"><span data-stu-id="e3d07-140">OUTPUTS</span></span>

### <span data-ttu-id="e3d07-141">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyIntrusionDetectionBypassTrafficSetting</span><span class="sxs-lookup"><span data-stu-id="e3d07-141">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyIntrusionDetectionBypassTrafficSetting</span></span>

## <span data-ttu-id="e3d07-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e3d07-142">NOTES</span></span>

## <span data-ttu-id="e3d07-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e3d07-143">RELATED LINKS</span></span>
