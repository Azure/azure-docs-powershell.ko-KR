---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-azvirtualnetworkgatewaypacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVirtualnetworkGatewayPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVirtualnetworkGatewayPacketCapture.md
ms.openlocfilehash: b0010134ac6b819afc3e8621b11d5530a08008a8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98347913"
---
# <span data-ttu-id="4e9f3-101">Start-AzVirtualnetworkGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4e9f3-101">Start-AzVirtualnetworkGatewayPacketCapture</span></span>

## <span data-ttu-id="4e9f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4e9f3-102">SYNOPSIS</span></span>
<span data-ttu-id="4e9f3-103">Virtual Network 게이트웨이에서 패킷 캡처 작업을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="4e9f3-103">Starts Packet Capture Operation on a Virtual Network Gateway.</span></span>

## <span data-ttu-id="4e9f3-104">구문</span><span class="sxs-lookup"><span data-stu-id="4e9f3-104">SYNTAX</span></span>

### <span data-ttu-id="4e9f3-105">ByName(기본값)</span><span class="sxs-lookup"><span data-stu-id="4e9f3-105">ByName (Default)</span></span>
```
Start-AzVirtualnetworkGatewayPacketCapture -ResourceGroupName <String> -Name <String> [-FilterData <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e9f3-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="4e9f3-106">ByInputObject</span></span>
```
Start-AzVirtualnetworkGatewayPacketCapture -InputObject <PSVirtualNetworkGateway> [-FilterData <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e9f3-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="4e9f3-107">ByResourceId</span></span>
```
Start-AzVirtualnetworkGatewayPacketCapture -ResourceId <String> [-FilterData <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e9f3-108">설명</span><span class="sxs-lookup"><span data-stu-id="4e9f3-108">DESCRIPTION</span></span>
<span data-ttu-id="4e9f3-109">Virtual Network 게이트웨이에서 패킷 캡처 작업을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="4e9f3-109">Starts Packet Capture Operation on a Virtual Network Gateway.</span></span>

## <span data-ttu-id="4e9f3-110">예제</span><span class="sxs-lookup"><span data-stu-id="4e9f3-110">EXAMPLES</span></span>

### <span data-ttu-id="4e9f3-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="4e9f3-111">Example 1</span></span>
```powershell
Start-AzVirtualnetworkGatewayPacketCapture -ResourceGroupName "PktCaptureTestSite2RG" -Name "PktCaptureTestSite2VNG"

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
### <span data-ttu-id="4e9f3-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="4e9f3-112">Example 2</span></span>
```powershell
$a="{`"TracingFlags`":11,`"MaxPacketBufferSize`":120,`"MaxFileSize`":500,`"Filters`":[{`"SourceSubnets`":[`"10.19.0.4/32`",`"10.20.0.4/32`"],`"DestinationSubnets`":[`"10.20.0.4/32`",`"10.19.0.4/32`"],`"TcpFlags`":-1,`"Protocol`":[6],`"CaptureSingleDirectionTrafficOnly`":true}]}"
Start-AzVirtualnetworkGatewayPacketCapture -ResourceGroupName "PktCaptureTestSite2RG" -Name "PktCaptureTestSite2VNG" -FilterData $a

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
### <span data-ttu-id="4e9f3-113">예제 3</span><span class="sxs-lookup"><span data-stu-id="4e9f3-113">Example 3</span></span>
<span data-ttu-id="4e9f3-114">모든 내부 및 외부 패킷 캡처에 대한 패킷 캡처 예제</span><span class="sxs-lookup"><span data-stu-id="4e9f3-114">Packet Capture example for capture all inner and outer packets</span></span>
```powershell
$a = "{`"TracingFlags`": 11,`"MaxPacketBufferSize`": 120,`"MaxFileSize`": 500,`"Filters`" :[{`"CaptureSingleDirectionTrafficOnly`": false}]}"
Start-AzVirtualnetworkGatewayPacketCapture -ResourceGroupName "PktCaptureTestSite2RG" -Name "PktCaptureTestSite2VNG" -FilterData $a

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

## <span data-ttu-id="4e9f3-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4e9f3-115">PARAMETERS</span></span>

### <span data-ttu-id="4e9f3-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4e9f3-116">-AsJob</span></span>
<span data-ttu-id="4e9f3-117">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="4e9f3-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4e9f3-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4e9f3-118">-Confirm</span></span>
<span data-ttu-id="4e9f3-119">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4e9f3-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e9f3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e9f3-120">-DefaultProfile</span></span>
<span data-ttu-id="4e9f3-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4e9f3-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e9f3-122">-FilterData</span><span class="sxs-lookup"><span data-stu-id="4e9f3-122">-FilterData</span></span>
<span data-ttu-id="4e9f3-123">가상 네트워크 게이트웨이에서 패킷 캡처를 시작하는 필터 옵션입니다.</span><span class="sxs-lookup"><span data-stu-id="4e9f3-123">Filter options for start packet capture on virtual network gateway.</span></span>

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

### <span data-ttu-id="4e9f3-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4e9f3-124">-InputObject</span></span>
<span data-ttu-id="4e9f3-125">패킷 캡처를 시작할 가상 네트워크 게이트웨이 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="4e9f3-125">The virtual network gateway object where packet capture to be started.</span></span>

```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: ByInputObject
Aliases: VirtualNetworkGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4e9f3-126">-Name</span><span class="sxs-lookup"><span data-stu-id="4e9f3-126">-Name</span></span>
<span data-ttu-id="4e9f3-127">패킷 캡처를 시작할 가상 네트워크 게이트웨이 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4e9f3-127">The virtual network gateway name where packet capture is to be started.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: ResourceName, VirtualNetworkGatewayName, GatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e9f3-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e9f3-128">-ResourceGroupName</span></span>
<span data-ttu-id="4e9f3-129">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4e9f3-129">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e9f3-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4e9f3-130">-ResourceId</span></span>
<span data-ttu-id="4e9f3-131">패킷 캡처를 시작할 VirtualNetworkGateway의 Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="4e9f3-131">The Azure resource ID of the VirtualNetworkGateway where packet capture to be started.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e9f3-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e9f3-132">-WhatIf</span></span>
<span data-ttu-id="4e9f3-133">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="4e9f3-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e9f3-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4e9f3-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e9f3-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e9f3-135">CommonParameters</span></span>
<span data-ttu-id="4e9f3-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4e9f3-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e9f3-137">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4e9f3-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e9f3-138">입력</span><span class="sxs-lookup"><span data-stu-id="4e9f3-138">INPUTS</span></span>

### <span data-ttu-id="4e9f3-139">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="4e9f3-139">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="4e9f3-140">System.String</span><span class="sxs-lookup"><span data-stu-id="4e9f3-140">System.String</span></span>

## <span data-ttu-id="4e9f3-141">출력</span><span class="sxs-lookup"><span data-stu-id="4e9f3-141">OUTPUTS</span></span>

### <span data-ttu-id="4e9f3-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="4e9f3-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayPacketCaptureResult</span></span>

## <span data-ttu-id="4e9f3-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4e9f3-143">NOTES</span></span>

## <span data-ttu-id="4e9f3-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4e9f3-144">RELATED LINKS</span></span>
[<span data-ttu-id="4e9f3-145">Stop-AzVirtualnetworkGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4e9f3-145">Stop-AzVirtualnetworkGatewayPacketCapture</span></span>](./Stop-AzVirtualnetworkGatewayPacketCapture.md)