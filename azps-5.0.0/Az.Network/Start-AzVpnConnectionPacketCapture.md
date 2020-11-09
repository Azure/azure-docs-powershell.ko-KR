---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-azvpnconnectionpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVpnConnectionPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVpnConnectionPacketCapture.md
ms.openlocfilehash: 720b81b858799e2930ed3d2cdd45e25220697e6a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94311273"
---
# <span data-ttu-id="14ce3-101">Start-AzVpnConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="14ce3-101">Start-AzVpnConnectionPacketCapture</span></span>

## <span data-ttu-id="14ce3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14ce3-102">SYNOPSIS</span></span>
<span data-ttu-id="14ce3-103">Vpn 연결에서 패킷 캡처 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="14ce3-103">Starts Packet Capture Operation on a Vpn Connection.</span></span>

## <span data-ttu-id="14ce3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="14ce3-104">SYNTAX</span></span>

### <span data-ttu-id="14ce3-105">ByVpnConnectionName (기본값)</span><span class="sxs-lookup"><span data-stu-id="14ce3-105">ByVpnConnectionName (Default)</span></span>
```
Start-AzVpnConnectionPacketCapture -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-FilterData <String>] -LinkConnectionName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14ce3-106">ByVpnConnectionObject</span><span class="sxs-lookup"><span data-stu-id="14ce3-106">ByVpnConnectionObject</span></span>
```
Start-AzVpnConnectionPacketCapture -InputObject <PSVpnConnection> [-FilterData <String>]
 -LinkConnectionName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="14ce3-107">ByVpnConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="14ce3-107">ByVpnConnectionResourceId</span></span>
```
Start-AzVpnConnectionPacketCapture -ResourceId <String> [-FilterData <String>] -LinkConnectionName <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14ce3-108">설명은</span><span class="sxs-lookup"><span data-stu-id="14ce3-108">DESCRIPTION</span></span>
<span data-ttu-id="14ce3-109">Vpn 연결에서 패킷 캡처 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="14ce3-109">Starts Packet Capture Operation on a Vpn Connection.</span></span>

## <span data-ttu-id="14ce3-110">예제의</span><span class="sxs-lookup"><span data-stu-id="14ce3-110">EXAMPLES</span></span>

### <span data-ttu-id="14ce3-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="14ce3-111">Example 1</span></span>
```powershell
Start-AzVpnConnectionPacketCapture -ResourceGroupName "PktCaptureTestSite2RG" -Name "PktCaptureTestSite2Site1Cn" -ParentResourceName "VpnGw1" -LinkConnectionName "PktCaptureTestSite2Site1CnLink1"
Code              : Succeeded
EndTime           : 10/1/2019 12:52:37 AM
StartTime         : 10/1/2019 12:52:25 AM
ResultsText       :
LinkConnectionName: PktCaptureTestSite2Site1CnLink1
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

### <span data-ttu-id="14ce3-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="14ce3-112">Example 2</span></span>
```powershell
$a="{`"TracingFlags`":11,`"MaxPacketBufferSize`":120,`"MaxFileSize`":500,`"Filters`":[{`"SourceSubnets`":[`"10.19.0.4/32`",`"10.20.0.4/32`"],`"DestinationSubnets`":[`"10.20.0.4/32`",`"10.19.0.4/32`"],`"IpSubnetValueAsAny`":true,`"TcpFlags`":-1,`"PortValueAsAny`":true,`"CaptureSingleDirectionTrafficOnly`":true}]}"
Start-AzVpnConnectionPacketCapture -ResourceGroupName "PktCaptureTestSite2RG" -Name "PktCaptureTestSite2Site1Cn" -ParentResourceName "VpnGw1" -LinkConnectionName "PktCaptureTestSite2Site1CnLink1,PktCaptureTestSite2Site1CnLink1" -FilterData $a 
Code              : Succeeded
EndTime           : 10/1/2019 12:52:37 AM
StartTime         : 10/1/2019 12:52:25 AM
ResultsText       :
LinkConnectionName: PktCaptureTestSite2Site1CnLink1,PktCaptureTestSite2Site1CnLink1
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

## <span data-ttu-id="14ce3-113">변수</span><span class="sxs-lookup"><span data-stu-id="14ce3-113">PARAMETERS</span></span>

### <span data-ttu-id="14ce3-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="14ce3-114">-AsJob</span></span>
<span data-ttu-id="14ce3-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="14ce3-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="14ce3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14ce3-116">-DefaultProfile</span></span>
<span data-ttu-id="14ce3-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="14ce3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14ce3-118">-FilterData</span><span class="sxs-lookup"><span data-stu-id="14ce3-118">-FilterData</span></span>
<span data-ttu-id="14ce3-119">Vpn 연결의 패킷 캡처 시작에 대 한 필터 옵션입니다.</span><span class="sxs-lookup"><span data-stu-id="14ce3-119">Filter options for start packet capture on Vpn connection.</span></span>

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

### <span data-ttu-id="14ce3-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="14ce3-120">-InputObject</span></span>
<span data-ttu-id="14ce3-121">패킷을 캡처 시작 하는 Vpn 연결 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="14ce3-121">The Vpn connection object where packet capture to be started.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnConnection
Parameter Sets: ByVpnConnectionObject
Aliases: VpnConnection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="14ce3-122">-LinkConnectionName</span><span class="sxs-lookup"><span data-stu-id="14ce3-122">-LinkConnectionName</span></span>
<span data-ttu-id="14ce3-123">SiteLinkConnection의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="14ce3-123">The names of the SiteLinkConnection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14ce3-124">-이름</span><span class="sxs-lookup"><span data-stu-id="14ce3-124">-Name</span></span>
<span data-ttu-id="14ce3-125">패킷을 캡처를 시작할 Vpn 연결 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="14ce3-125">The Vpn connection name where packet capture to be started.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases: ResourceName, VpnConnectionName, ConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14ce3-126">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="14ce3-126">-ParentResourceName</span></span>
<span data-ttu-id="14ce3-127">부모 Vpngateway의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="14ce3-127">The name of the Parent Vpngateway.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases: ParentVpnGatewayName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14ce3-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14ce3-128">-ResourceGroupName</span></span>
<span data-ttu-id="14ce3-129">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="14ce3-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14ce3-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="14ce3-130">-ResourceId</span></span>
<span data-ttu-id="14ce3-131">패킷 캡처가 시작 되는 VpnConnection의 Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="14ce3-131">The Azure resource ID of the VpnConnection where packet capture to be started.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14ce3-132">-확인</span><span class="sxs-lookup"><span data-stu-id="14ce3-132">-Confirm</span></span>
<span data-ttu-id="14ce3-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="14ce3-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14ce3-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14ce3-134">-WhatIf</span></span>
<span data-ttu-id="14ce3-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="14ce3-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14ce3-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="14ce3-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14ce3-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14ce3-137">CommonParameters</span></span>
<span data-ttu-id="14ce3-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="14ce3-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14ce3-139">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="14ce3-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14ce3-140">입력</span><span class="sxs-lookup"><span data-stu-id="14ce3-140">INPUTS</span></span>

### <span data-ttu-id="14ce3-141">PSVpnConnection에 대 한.</span><span class="sxs-lookup"><span data-stu-id="14ce3-141">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

### <span data-ttu-id="14ce3-142">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="14ce3-142">System.String</span></span>

## <span data-ttu-id="14ce3-143">출력</span><span class="sxs-lookup"><span data-stu-id="14ce3-143">OUTPUTS</span></span>

### <span data-ttu-id="14ce3-144">PSVpnConnectionPacketCaptureResult에 대 한.</span><span class="sxs-lookup"><span data-stu-id="14ce3-144">Microsoft.Azure.Commands.Network.Models.PSVpnConnectionPacketCaptureResult</span></span>

## <span data-ttu-id="14ce3-145">상속자</span><span class="sxs-lookup"><span data-stu-id="14ce3-145">NOTES</span></span>

## <span data-ttu-id="14ce3-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="14ce3-146">RELATED LINKS</span></span>

[<span data-ttu-id="14ce3-147">중지-AzVpnConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="14ce3-147">Stop-AzVpnConnectionPacketCapture</span></span>](./Stop-AzVpnConnectionPacketCapture.md)