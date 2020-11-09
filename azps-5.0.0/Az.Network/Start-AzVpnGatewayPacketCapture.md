---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/Start-AzVpnGatewayPacketCapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVpnGatewayPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVpnGatewayPacketCapture.md
ms.openlocfilehash: 931c01b925416a7b1357d1eac15806035eef46d4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94311285"
---
# <span data-ttu-id="4b351-101">Start-AzVpnGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4b351-101">Start-AzVpnGatewayPacketCapture</span></span>

## <span data-ttu-id="4b351-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b351-102">SYNOPSIS</span></span>
<span data-ttu-id="4b351-103">Vpn 게이트웨이에서 패킷 캡처 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b351-103">Starts Packet Capture Operation on a Vpn Gateway.</span></span>

## <span data-ttu-id="4b351-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4b351-104">SYNTAX</span></span>

### <span data-ttu-id="4b351-105">ByVpnGatewayName (기본값)</span><span class="sxs-lookup"><span data-stu-id="4b351-105">ByVpnGatewayName (Default)</span></span>
```
Start-AzVpnGatewayPacketCapture -ResourceGroupName <String> -Name <String> [-FilterData <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b351-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="4b351-106">ByVpnGatewayObject</span></span>
```
Start-AzVpnGatewayPacketCapture -InputObject <PSVpnGateway> [-FilterData <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b351-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="4b351-107">ByVpnGatewayResourceId</span></span>
```
Start-AzVpnGatewayPacketCapture -ResourceId <String> [-FilterData <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b351-108">설명은</span><span class="sxs-lookup"><span data-stu-id="4b351-108">DESCRIPTION</span></span>
<span data-ttu-id="4b351-109">Vpn 게이트웨이에서 패킷 캡처 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b351-109">Starts Packet Capture Operation on a Vpn Gateway.</span></span>

## <span data-ttu-id="4b351-110">예제의</span><span class="sxs-lookup"><span data-stu-id="4b351-110">EXAMPLES</span></span>

### <span data-ttu-id="4b351-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="4b351-111">Example 1</span></span>
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

### <span data-ttu-id="4b351-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="4b351-112">Example 2</span></span>
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

## <span data-ttu-id="4b351-113">변수</span><span class="sxs-lookup"><span data-stu-id="4b351-113">PARAMETERS</span></span>

### <span data-ttu-id="4b351-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4b351-114">-AsJob</span></span>
<span data-ttu-id="4b351-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="4b351-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4b351-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b351-116">-DefaultProfile</span></span>
<span data-ttu-id="4b351-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4b351-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b351-118">-FilterData</span><span class="sxs-lookup"><span data-stu-id="4b351-118">-FilterData</span></span>
<span data-ttu-id="4b351-119">Vpn 게이트웨이에서 시작 하는 패킷 캡처에 대 한 필터 옵션입니다.</span><span class="sxs-lookup"><span data-stu-id="4b351-119">Filter options for start packet capture on Vpn Gateway.</span></span>

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

### <span data-ttu-id="4b351-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4b351-120">-InputObject</span></span>
<span data-ttu-id="4b351-121">패킷을 캡처 시작 하는 Vpn 게이트웨이 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="4b351-121">The Vpn Gateway object where packet capture to be started.</span></span>

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

### <span data-ttu-id="4b351-122">-이름</span><span class="sxs-lookup"><span data-stu-id="4b351-122">-Name</span></span>
<span data-ttu-id="4b351-123">패킷 캡처를 시작할 Vpn 게이트웨이 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4b351-123">The Vpn Gateway name where packet capture is to be started.</span></span>

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

### <span data-ttu-id="4b351-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b351-124">-ResourceGroupName</span></span>
<span data-ttu-id="4b351-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4b351-125">The resource group name.</span></span>

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

### <span data-ttu-id="4b351-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4b351-126">-ResourceId</span></span>
<span data-ttu-id="4b351-127">패킷 캡처가 시작 되는 VpnGateway의 Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="4b351-127">The Azure resource ID of the VpnGateway where packet capture to be started.</span></span>

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

### <span data-ttu-id="4b351-128">-확인</span><span class="sxs-lookup"><span data-stu-id="4b351-128">-Confirm</span></span>
<span data-ttu-id="4b351-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b351-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b351-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b351-130">-WhatIf</span></span>
<span data-ttu-id="4b351-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4b351-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b351-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4b351-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b351-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b351-133">CommonParameters</span></span>
<span data-ttu-id="4b351-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b351-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b351-135">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="4b351-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b351-136">입력</span><span class="sxs-lookup"><span data-stu-id="4b351-136">INPUTS</span></span>

### <span data-ttu-id="4b351-137">PSVpnGateway에 대 한.</span><span class="sxs-lookup"><span data-stu-id="4b351-137">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="4b351-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="4b351-138">System.String</span></span>

## <span data-ttu-id="4b351-139">출력</span><span class="sxs-lookup"><span data-stu-id="4b351-139">OUTPUTS</span></span>

### <span data-ttu-id="4b351-140">PSVpnGatewayPacketCaptureResult에 대 한.</span><span class="sxs-lookup"><span data-stu-id="4b351-140">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayPacketCaptureResult</span></span>

## <span data-ttu-id="4b351-141">상속자</span><span class="sxs-lookup"><span data-stu-id="4b351-141">NOTES</span></span>

## <span data-ttu-id="4b351-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4b351-142">RELATED LINKS</span></span>

[<span data-ttu-id="4b351-143">중지-AzVpnGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4b351-143">Stop-AzVpnGatewayPacketCapture</span></span>](./Stop-AzVpnGatewayPacketCapture.md)