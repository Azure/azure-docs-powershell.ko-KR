---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/Start-AzVpnGatewayPacketCapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVpnGatewayPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVpnGatewayPacketCapture.md
ms.openlocfilehash: 931c01b925416a7b1357d1eac15806035eef46d4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495098"
---
# <span data-ttu-id="cd5c2-101">Start-AzVpnGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="cd5c2-101">Start-AzVpnGatewayPacketCapture</span></span>

## <span data-ttu-id="cd5c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd5c2-102">SYNOPSIS</span></span>
<span data-ttu-id="cd5c2-103">Vpn Gateway에서 패킷 캡처 작업을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="cd5c2-103">Starts Packet Capture Operation on a Vpn Gateway.</span></span>

## <span data-ttu-id="cd5c2-104">구문</span><span class="sxs-lookup"><span data-stu-id="cd5c2-104">SYNTAX</span></span>

### <span data-ttu-id="cd5c2-105">ByVpnGatewayName(기본값)</span><span class="sxs-lookup"><span data-stu-id="cd5c2-105">ByVpnGatewayName (Default)</span></span>
```
Start-AzVpnGatewayPacketCapture -ResourceGroupName <String> -Name <String> [-FilterData <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd5c2-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="cd5c2-106">ByVpnGatewayObject</span></span>
```
Start-AzVpnGatewayPacketCapture -InputObject <PSVpnGateway> [-FilterData <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd5c2-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="cd5c2-107">ByVpnGatewayResourceId</span></span>
```
Start-AzVpnGatewayPacketCapture -ResourceId <String> [-FilterData <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd5c2-108">설명</span><span class="sxs-lookup"><span data-stu-id="cd5c2-108">DESCRIPTION</span></span>
<span data-ttu-id="cd5c2-109">Vpn Gateway에서 패킷 캡처 작업을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="cd5c2-109">Starts Packet Capture Operation on a Vpn Gateway.</span></span>

## <span data-ttu-id="cd5c2-110">예제</span><span class="sxs-lookup"><span data-stu-id="cd5c2-110">EXAMPLES</span></span>

### <span data-ttu-id="cd5c2-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="cd5c2-111">Example 1</span></span>
```powershell
Start-AzVpnGatewayPacketCapture -ResourceGroupName "PktCaptureTestSite2RG" -Name "PktCaptureTestSite2VNG"
Code              : Succeeded
EndTime           : 10/1/2019 12:57:27 AM
StartTime         : 10/1/2019 12:57:16 AM
ResultsText       :
ResourceGroupName : PktCaptureTestSite2RG
Location          : centraluseuap
ResourceGuid      : 161c0fff-f3fd-4698-9ab3-8ca9470de975
Type              :
Tag               :
TagsTable         :
Name              : PktCaptureTestSite2VNG
Etag              :
Id                :
```

### <span data-ttu-id="cd5c2-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="cd5c2-112">Example 2</span></span>
```powershell
$a="{`"TracingFlags`":11,`"MaxPacketBufferSize`":120,`"MaxFileSize`":500,`"Filters`":[{`"SourceSubnets`":[`"10.19.0.4/32`",`"10.20.0.4/32`"],`"DestinationSubnets`":[`"10.20.0.4/32`",`"10.19.0.4/32`"],`"TcpFlags`":-1,`"Protocol`":[6],`"CaptureSingleDirectionTrafficOnly`":true}]}"
Start-AzVpnGatewayPacketCapture -ResourceGroupName "PktCaptureTestSite2RG" -Name "PktCaptureTestSite2VNG" -FilterData $a
Code              : Succeeded
EndTime           : 10/1/2019 12:57:27 AM
StartTime         : 10/1/2019 12:57:16 AM
ResultsText       :
ResourceGroupName : PktCaptureTestSite2RG
Location          : centraluseuap
ResourceGuid      : 161c0fff-f3fd-4698-9ab3-8ca9470de975
Type              :
Tag               :
TagsTable         :
Name              : PktCaptureTestSite2VNG
Etag              :
Id                :
```

## <span data-ttu-id="cd5c2-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cd5c2-113">PARAMETERS</span></span>

### <span data-ttu-id="cd5c2-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cd5c2-114">-AsJob</span></span>
<span data-ttu-id="cd5c2-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="cd5c2-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cd5c2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd5c2-116">-DefaultProfile</span></span>
<span data-ttu-id="cd5c2-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cd5c2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd5c2-118">-FilterData</span><span class="sxs-lookup"><span data-stu-id="cd5c2-118">-FilterData</span></span>
<span data-ttu-id="cd5c2-119">Vpn Gateway에서 패킷 캡처를 시작하는 필터 옵션입니다.</span><span class="sxs-lookup"><span data-stu-id="cd5c2-119">Filter options for start packet capture on Vpn Gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd5c2-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cd5c2-120">-InputObject</span></span>
<span data-ttu-id="cd5c2-121">패킷 캡처를 시작할 Vpn Gateway 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="cd5c2-121">The Vpn Gateway object where packet capture to be started.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnGateway
Parameter Sets: ByVpnGatewayObject
Aliases: VpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cd5c2-122">-Name</span><span class="sxs-lookup"><span data-stu-id="cd5c2-122">-Name</span></span>
<span data-ttu-id="cd5c2-123">패킷 캡처를 시작할 Vpn Gateway 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cd5c2-123">The Vpn Gateway name where packet capture is to be started.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases: ResourceName, VpnGatewayName, GatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd5c2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd5c2-124">-ResourceGroupName</span></span>
<span data-ttu-id="cd5c2-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cd5c2-125">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd5c2-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cd5c2-126">-ResourceId</span></span>
<span data-ttu-id="cd5c2-127">패킷 캡처를 시작할 VpnGateway의 Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="cd5c2-127">The Azure resource ID of the VpnGateway where packet capture to be started.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd5c2-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cd5c2-128">-Confirm</span></span>
<span data-ttu-id="cd5c2-129">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="cd5c2-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd5c2-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd5c2-130">-WhatIf</span></span>
<span data-ttu-id="cd5c2-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="cd5c2-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd5c2-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cd5c2-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd5c2-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd5c2-133">CommonParameters</span></span>
<span data-ttu-id="cd5c2-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="cd5c2-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd5c2-135">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="cd5c2-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd5c2-136">입력</span><span class="sxs-lookup"><span data-stu-id="cd5c2-136">INPUTS</span></span>

### <span data-ttu-id="cd5c2-137">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="cd5c2-137">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="cd5c2-138">System.String</span><span class="sxs-lookup"><span data-stu-id="cd5c2-138">System.String</span></span>

## <span data-ttu-id="cd5c2-139">출력</span><span class="sxs-lookup"><span data-stu-id="cd5c2-139">OUTPUTS</span></span>

### <span data-ttu-id="cd5c2-140">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="cd5c2-140">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayPacketCaptureResult</span></span>

## <span data-ttu-id="cd5c2-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="cd5c2-141">NOTES</span></span>

## <span data-ttu-id="cd5c2-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cd5c2-142">RELATED LINKS</span></span>

[<span data-ttu-id="cd5c2-143">Stop-AzVpnGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="cd5c2-143">Stop-AzVpnGatewayPacketCapture</span></span>](./Stop-AzVpnGatewayPacketCapture.md)