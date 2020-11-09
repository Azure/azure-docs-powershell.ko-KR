---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-azvirtualnetworkgatewayconnectionpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVirtualNetworkGatewayConnectionPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVirtualNetworkGatewayConnectionPacketCapture.md
ms.openlocfilehash: d01fad830b9edcd8eced13a4f1e9317bb4930f9c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94311282"
---
# <span data-ttu-id="c47f7-101">Start-AzVirtualNetworkGatewayConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c47f7-101">Start-AzVirtualNetworkGatewayConnectionPacketCapture</span></span>

## <span data-ttu-id="c47f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c47f7-102">SYNOPSIS</span></span>
<span data-ttu-id="c47f7-103">가상 네트워크 게이트웨이 연결에서 패킷 캡처 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="c47f7-103">Starts Packet Capture Operation on a Virtual Network Gateway Connection.</span></span>

## <span data-ttu-id="c47f7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c47f7-104">SYNTAX</span></span>

### <span data-ttu-id="c47f7-105">ByName (기본값)</span><span class="sxs-lookup"><span data-stu-id="c47f7-105">ByName (Default)</span></span>
```
Start-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceGroupName <String> -Name <String>
 [-FilterData <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c47f7-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="c47f7-106">ByInputObject</span></span>
```
Start-AzVirtualNetworkGatewayConnectionPacketCapture -InputObject <PSVirtualNetworkGatewayConnection>
 [-FilterData <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c47f7-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c47f7-107">ByResourceId</span></span>
```
Start-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceId <String> [-FilterData <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c47f7-108">설명은</span><span class="sxs-lookup"><span data-stu-id="c47f7-108">DESCRIPTION</span></span>
<span data-ttu-id="c47f7-109">가상 네트워크 게이트웨이 연결에서 패킷 캡처 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="c47f7-109">Starts Packet Capture Operation on a Virtual Network Gateway Connection.</span></span>

## <span data-ttu-id="c47f7-110">예제의</span><span class="sxs-lookup"><span data-stu-id="c47f7-110">EXAMPLES</span></span>

### <span data-ttu-id="c47f7-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="c47f7-111">Example 1</span></span>
```powershell
Start-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceGroupName "PktCaptureTestSite2RG" -Name "PktCaptureTestSite2Site1Cn"

Code              : Succeeded
EndTime           : 10/1/2019 12:52:37 AM
StartTime         : 10/1/2019 12:52:25 AM
ResultsText       :
ResourceGroupName : PktCaptureTestSite2RG
Location          : centraluseuap
ResourceGuid      : ac70028f-5b88-4ad4-93d3-0b9a9172c382
Type              :
Tag               :
TagsTable         :
Name              : PktCaptureTestSite2Site1Cn
Etag              :
Id                :
```
### <span data-ttu-id="c47f7-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="c47f7-112">Example 2</span></span>
```powershell
$a="{`"TracingFlags`":11,`"MaxPacketBufferSize`":120,`"MaxFileSize`":500,`"Filters`":[{`"SourceSubnets`":[`"10.19.0.4/32`",`"10.20.0.4/32`"],`"DestinationSubnets`":[`"10.20.0.4/32`",`"10.19.0.4/32`"],`"TcpFlags`":-1,`"Protocol`":[6],`"CaptureSingleDirectionTrafficOnly`":true}]}"
Start-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceGroupName "PktCaptureTestSite2RG" -Name "PktCaptureTestSite2Site1Cn" -FilterData $a

Code              : Succeeded
EndTime           : 10/1/2019 12:52:37 AM
StartTime         : 10/1/2019 12:52:25 AM
ResultsText       :
ResourceGroupName : PktCaptureTestSite2RG
Location          : centraluseuap
ResourceGuid      : ac70028f-5b88-4ad4-93d3-0b9a9172c382
Type              :
Tag               :
TagsTable         :
Name              : PktCaptureTestSite2Site1Cn
Etag              :
Id                :
```
### <span data-ttu-id="c47f7-113">예제 3</span><span class="sxs-lookup"><span data-stu-id="c47f7-113">Example 3</span></span>
<span data-ttu-id="c47f7-114">모든 내부 및 외부 패킷을 캡처하기 위한 패킷 캡처 예제</span><span class="sxs-lookup"><span data-stu-id="c47f7-114">Packet Capture example for capture all inner and outer packets</span></span>
```powershell
$a = "{`"TracingFlags`": 11,`"MaxPacketBufferSize`": 120,`"MaxFileSize`": 500,`"Filters`" :[{`"CaptureSingleDirectionTrafficOnly`": false}]}"
Start-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceGroupName "PktCaptureTestSite2RG" -Name "PktCaptureTestSite2Site1Cn" -FilterData $a

Code              : Succeeded
EndTime           : 10/1/2019 12:52:37 AM
StartTime         : 10/1/2019 12:52:25 AM
ResultsText       :
ResourceGroupName : PktCaptureTestSite2RG
Location          : centraluseuap
ResourceGuid      : ac70028f-5b88-4ad4-93d3-0b9a9172c382
Type              :
Tag               :
TagsTable         :
Name              : PktCaptureTestSite2Site1Cn
Etag              :
Id                :
```

## <span data-ttu-id="c47f7-115">변수</span><span class="sxs-lookup"><span data-stu-id="c47f7-115">PARAMETERS</span></span>

### <span data-ttu-id="c47f7-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c47f7-116">-AsJob</span></span>
<span data-ttu-id="c47f7-117">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="c47f7-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c47f7-118">-확인</span><span class="sxs-lookup"><span data-stu-id="c47f7-118">-Confirm</span></span>
<span data-ttu-id="c47f7-119">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c47f7-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c47f7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c47f7-120">-DefaultProfile</span></span>
<span data-ttu-id="c47f7-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c47f7-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c47f7-122">-FilterData</span><span class="sxs-lookup"><span data-stu-id="c47f7-122">-FilterData</span></span>
<span data-ttu-id="c47f7-123">가상 네트워크 게이트웨이 연결의 시작 패킷 캡처에 대 한 필터 옵션입니다.</span><span class="sxs-lookup"><span data-stu-id="c47f7-123">Filter options for start packet capture on virtual network gateway connection.</span></span>

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

### <span data-ttu-id="c47f7-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c47f7-124">-InputObject</span></span>
<span data-ttu-id="c47f7-125">패킷 캡처가 시작 될 가상 네트워크 게이트웨이 연결 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="c47f7-125">The virtual network gateway connection object where packet capture to be started.</span></span>

```yaml
Type: PSVirtualNetworkGatewayConnection
Parameter Sets: ByInputObject
Aliases: VirtualNetworkGatewayConnection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c47f7-126">-이름</span><span class="sxs-lookup"><span data-stu-id="c47f7-126">-Name</span></span>
<span data-ttu-id="c47f7-127">패킷을 캡처를 시작할 가상 네트워크 게이트웨이 연결 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c47f7-127">The virtual network gateway connection name where packet capture to be started.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: ResourceName, VirtualNetworkGatewayConnectionName, ConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c47f7-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c47f7-128">-ResourceGroupName</span></span>
<span data-ttu-id="c47f7-129">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c47f7-129">The resource group name.</span></span>

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

### <span data-ttu-id="c47f7-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c47f7-130">-ResourceId</span></span>
<span data-ttu-id="c47f7-131">패킷 캡처가 시작 되는 VirtualNetworkGatewayConnection의 Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c47f7-131">The Azure resource ID of the VirtualNetworkGatewayConnection where packet capture to be started.</span></span>

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

### <span data-ttu-id="c47f7-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c47f7-132">-WhatIf</span></span>
<span data-ttu-id="c47f7-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c47f7-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c47f7-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c47f7-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c47f7-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c47f7-135">CommonParameters</span></span>
<span data-ttu-id="c47f7-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c47f7-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c47f7-137">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c47f7-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c47f7-138">입력</span><span class="sxs-lookup"><span data-stu-id="c47f7-138">INPUTS</span></span>

### <span data-ttu-id="c47f7-139">PSVirtualNetworkGatewayConnection에 대 한.</span><span class="sxs-lookup"><span data-stu-id="c47f7-139">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

### <span data-ttu-id="c47f7-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c47f7-140">System.String</span></span>

## <span data-ttu-id="c47f7-141">출력</span><span class="sxs-lookup"><span data-stu-id="c47f7-141">OUTPUTS</span></span>

### <span data-ttu-id="c47f7-142">PSVirtualNetworkGatewayPacketCaptureResult에 대 한.</span><span class="sxs-lookup"><span data-stu-id="c47f7-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayPacketCaptureResult</span></span>

## <span data-ttu-id="c47f7-143">상속자</span><span class="sxs-lookup"><span data-stu-id="c47f7-143">NOTES</span></span>

## <span data-ttu-id="c47f7-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c47f7-144">RELATED LINKS</span></span>
[<span data-ttu-id="c47f7-145">중지-AzVirtualNetworkGatewayConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c47f7-145">Stop-AzVirtualNetworkGatewayConnectionPacketCapture</span></span>](./Stop-AzVirtualNetworkGatewayConnectionPacketCapture.md)