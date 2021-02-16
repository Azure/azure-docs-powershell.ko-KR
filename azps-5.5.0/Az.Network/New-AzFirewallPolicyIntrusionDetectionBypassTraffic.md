---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicyintrusiondetectionbypasstraffic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyIntrusionDetectionBypassTraffic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyIntrusionDetectionBypassTraffic.md
ms.openlocfilehash: c296c44c96d756dc0ca3a107d8eee265a9226b15
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184481"
---
# <span data-ttu-id="6b249-101">New-AzFirewallPolicyIntrusionDetectionBypassTraffic</span><span class="sxs-lookup"><span data-stu-id="6b249-101">New-AzFirewallPolicyIntrusionDetectionBypassTraffic</span></span>

## <span data-ttu-id="6b249-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b249-102">SYNOPSIS</span></span>
<span data-ttu-id="6b249-103">새 Azure Firewall 정책 침입 감지 우회 트래픽 설정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6b249-103">Creates a new Azure Firewall Policy Intrusion Detection Bypass Traffic Setting</span></span>

## <span data-ttu-id="6b249-104">구문</span><span class="sxs-lookup"><span data-stu-id="6b249-104">SYNTAX</span></span>

```
New-AzFirewallPolicyIntrusionDetectionBypassTraffic -Name <String> [-Description <String>] -Protocol <String>
 [-SourceAddress <String[]>] [-DestinationAddress <String[]>] [-SourceIpGroup <String[]>]
 [-DestinationIpGroup <String[]>] -DestinationPort <String[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b249-105">설명</span><span class="sxs-lookup"><span data-stu-id="6b249-105">DESCRIPTION</span></span>
<span data-ttu-id="6b249-106">**New-AzFirewallPolicyIntrusionDetectionBypassTraffic** cmdlet은 트래픽 개체를 무시하는 Azure Firewall 정책 침입 감지를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6b249-106">The **New-AzFirewallPolicyIntrusionDetectionBypassTraffic** cmdlet creates an Azure Firewall Policy Intrusion Detection Bypass Traffic Object.</span></span>

## <span data-ttu-id="6b249-107">예제</span><span class="sxs-lookup"><span data-stu-id="6b249-107">EXAMPLES</span></span>

### <span data-ttu-id="6b249-108">예제 1: 1.</span><span class="sxs-lookup"><span data-stu-id="6b249-108">Example 1: 1.</span></span> <span data-ttu-id="6b249-109">특정 포트 및 원본 주소를 사용하여 트래픽 우회 만들기</span><span class="sxs-lookup"><span data-stu-id="6b249-109">Create bypass traffic with specific port and source address</span></span>
```powershell
PS C:\> $bypass = New-AzFirewallPolicyIntrusionDetectionBypassTraffic -Name "bypass-setting" -Protocol "TCP" -DestinationPort "80" -SourceAddress "10.0.0.0" -DestinationAddress "*"
PS C:\> New-AzFirewallPolicyIntrusionDetection -Mode "Deny" -BypassTraffic $bypass
```

<span data-ttu-id="6b249-110">이 예제에서는 트래픽 우회 설정을 사용하여 침입 감지를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6b249-110">This example creates intrusion detection with bypass traffic setting</span></span>

## <span data-ttu-id="6b249-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6b249-111">PARAMETERS</span></span>

### <span data-ttu-id="6b249-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b249-112">-DefaultProfile</span></span>
<span data-ttu-id="6b249-113">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6b249-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6b249-114">-Description</span><span class="sxs-lookup"><span data-stu-id="6b249-114">-Description</span></span>
<span data-ttu-id="6b249-115">설정 설명을 무시합니다.</span><span class="sxs-lookup"><span data-stu-id="6b249-115">Bypass setting description.</span></span>

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

### <span data-ttu-id="6b249-116">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="6b249-116">-DestinationAddress</span></span>
<span data-ttu-id="6b249-117">대상 IP 주소 또는 범위 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="6b249-117">List of destination IP addresses or ranges.</span></span>

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

### <span data-ttu-id="6b249-118">-DestinationIpGroup</span><span class="sxs-lookup"><span data-stu-id="6b249-118">-DestinationIpGroup</span></span>
<span data-ttu-id="6b249-119">대상 IpGroups 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="6b249-119">List of destination IpGroups.</span></span>

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

### <span data-ttu-id="6b249-120">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="6b249-120">-DestinationPort</span></span>
<span data-ttu-id="6b249-121">대상 포트 또는 범위 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="6b249-121">List of destination ports or ranges.</span></span>

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

### <span data-ttu-id="6b249-122">-Name</span><span class="sxs-lookup"><span data-stu-id="6b249-122">-Name</span></span>
<span data-ttu-id="6b249-123">설정 이름을 무시합니다.</span><span class="sxs-lookup"><span data-stu-id="6b249-123">Bypass setting name.</span></span>

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

### <span data-ttu-id="6b249-124">-Protocol</span><span class="sxs-lookup"><span data-stu-id="6b249-124">-Protocol</span></span>
<span data-ttu-id="6b249-125">설정 프로토콜을 무시합니다.</span><span class="sxs-lookup"><span data-stu-id="6b249-125">Bypass setting protocol.</span></span>

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

### <span data-ttu-id="6b249-126">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="6b249-126">-SourceAddress</span></span>
<span data-ttu-id="6b249-127">원본 IP 주소 또는 범위 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="6b249-127">List of source IP addresses or ranges.</span></span>

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

### <span data-ttu-id="6b249-128">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="6b249-128">-SourceIpGroup</span></span>
<span data-ttu-id="6b249-129">원본 IpGroups 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="6b249-129">List of source IpGroups.</span></span>

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

### <span data-ttu-id="6b249-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6b249-130">-Confirm</span></span>
<span data-ttu-id="6b249-131">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="6b249-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b249-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b249-132">-WhatIf</span></span>
<span data-ttu-id="6b249-133">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="6b249-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b249-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6b249-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b249-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b249-135">CommonParameters</span></span>
<span data-ttu-id="6b249-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6b249-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b249-137">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6b249-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b249-138">입력</span><span class="sxs-lookup"><span data-stu-id="6b249-138">INPUTS</span></span>

### <span data-ttu-id="6b249-139">없음</span><span class="sxs-lookup"><span data-stu-id="6b249-139">None</span></span>

## <span data-ttu-id="6b249-140">출력</span><span class="sxs-lookup"><span data-stu-id="6b249-140">OUTPUTS</span></span>

### <span data-ttu-id="6b249-141">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyIntrusionDetectionBypassTrafficSetting</span><span class="sxs-lookup"><span data-stu-id="6b249-141">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyIntrusionDetectionBypassTrafficSetting</span></span>

## <span data-ttu-id="6b249-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6b249-142">NOTES</span></span>

## <span data-ttu-id="6b249-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6b249-143">RELATED LINKS</span></span>
