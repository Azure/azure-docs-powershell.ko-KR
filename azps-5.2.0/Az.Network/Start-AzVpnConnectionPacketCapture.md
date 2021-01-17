---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-azvpnconnectionpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVpnConnectionPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVpnConnectionPacketCapture.md
ms.openlocfilehash: 720b81b858799e2930ed3d2cdd45e25220697e6a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98365044"
---
# <span data-ttu-id="e89c7-101">Start-AzVpnConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e89c7-101">Start-AzVpnConnectionPacketCapture</span></span>

## <span data-ttu-id="e89c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e89c7-102">SYNOPSIS</span></span>
<span data-ttu-id="e89c7-103">Vpn 연결에서 패킷 캡처 작업을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="e89c7-103">Starts Packet Capture Operation on a Vpn Connection.</span></span>

## <span data-ttu-id="e89c7-104">구문</span><span class="sxs-lookup"><span data-stu-id="e89c7-104">SYNTAX</span></span>

### <span data-ttu-id="e89c7-105">ByVpnConnectionName(기본값)</span><span class="sxs-lookup"><span data-stu-id="e89c7-105">ByVpnConnectionName (Default)</span></span>
```
Start-AzVpnConnectionPacketCapture -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-FilterData <String>] -LinkConnectionName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e89c7-106">ByVpnConnectionObject</span><span class="sxs-lookup"><span data-stu-id="e89c7-106">ByVpnConnectionObject</span></span>
```
Start-AzVpnConnectionPacketCapture -InputObject <PSVpnConnection> [-FilterData <String>]
 -LinkConnectionName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e89c7-107">ByVpnConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="e89c7-107">ByVpnConnectionResourceId</span></span>
```
Start-AzVpnConnectionPacketCapture -ResourceId <String> [-FilterData <String>] -LinkConnectionName <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e89c7-108">설명</span><span class="sxs-lookup"><span data-stu-id="e89c7-108">DESCRIPTION</span></span>
<span data-ttu-id="e89c7-109">Vpn 연결에서 패킷 캡처 작업을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="e89c7-109">Starts Packet Capture Operation on a Vpn Connection.</span></span>

## <span data-ttu-id="e89c7-110">예제</span><span class="sxs-lookup"><span data-stu-id="e89c7-110">EXAMPLES</span></span>

### <span data-ttu-id="e89c7-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="e89c7-111">Example 1</span></span>
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

### <span data-ttu-id="e89c7-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="e89c7-112">Example 2</span></span>
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

## <span data-ttu-id="e89c7-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e89c7-113">PARAMETERS</span></span>

### <span data-ttu-id="e89c7-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e89c7-114">-AsJob</span></span>
<span data-ttu-id="e89c7-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="e89c7-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e89c7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e89c7-116">-DefaultProfile</span></span>
<span data-ttu-id="e89c7-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e89c7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e89c7-118">-FilterData</span><span class="sxs-lookup"><span data-stu-id="e89c7-118">-FilterData</span></span>
<span data-ttu-id="e89c7-119">Vpn 연결에서 패킷 캡처를 시작하는 필터 옵션입니다.</span><span class="sxs-lookup"><span data-stu-id="e89c7-119">Filter options for start packet capture on Vpn connection.</span></span>

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

### <span data-ttu-id="e89c7-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e89c7-120">-InputObject</span></span>
<span data-ttu-id="e89c7-121">패킷 캡처를 시작할 Vpn 연결 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="e89c7-121">The Vpn connection object where packet capture to be started.</span></span>

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

### <span data-ttu-id="e89c7-122">-LinkConnectionName</span><span class="sxs-lookup"><span data-stu-id="e89c7-122">-LinkConnectionName</span></span>
<span data-ttu-id="e89c7-123">SiteLinkConnection의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e89c7-123">The names of the SiteLinkConnection.</span></span>

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

### <span data-ttu-id="e89c7-124">-Name</span><span class="sxs-lookup"><span data-stu-id="e89c7-124">-Name</span></span>
<span data-ttu-id="e89c7-125">패킷 캡처를 시작할 Vpn 연결 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e89c7-125">The Vpn connection name where packet capture to be started.</span></span>

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

### <span data-ttu-id="e89c7-126">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="e89c7-126">-ParentResourceName</span></span>
<span data-ttu-id="e89c7-127">부모 Vpngateway의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e89c7-127">The name of the Parent Vpngateway.</span></span>

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

### <span data-ttu-id="e89c7-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e89c7-128">-ResourceGroupName</span></span>
<span data-ttu-id="e89c7-129">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e89c7-129">The resource group name.</span></span>

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

### <span data-ttu-id="e89c7-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e89c7-130">-ResourceId</span></span>
<span data-ttu-id="e89c7-131">패킷 캡처를 시작할 VpnConnection의 Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="e89c7-131">The Azure resource ID of the VpnConnection where packet capture to be started.</span></span>

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

### <span data-ttu-id="e89c7-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e89c7-132">-Confirm</span></span>
<span data-ttu-id="e89c7-133">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e89c7-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e89c7-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e89c7-134">-WhatIf</span></span>
<span data-ttu-id="e89c7-135">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="e89c7-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e89c7-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e89c7-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e89c7-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e89c7-137">CommonParameters</span></span>
<span data-ttu-id="e89c7-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e89c7-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e89c7-139">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e89c7-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e89c7-140">입력</span><span class="sxs-lookup"><span data-stu-id="e89c7-140">INPUTS</span></span>

### <span data-ttu-id="e89c7-141">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="e89c7-141">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

### <span data-ttu-id="e89c7-142">System.String</span><span class="sxs-lookup"><span data-stu-id="e89c7-142">System.String</span></span>

## <span data-ttu-id="e89c7-143">출력</span><span class="sxs-lookup"><span data-stu-id="e89c7-143">OUTPUTS</span></span>

### <span data-ttu-id="e89c7-144">Microsoft.Azure.Commands.Network.Models.PSVpnConnectionPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="e89c7-144">Microsoft.Azure.Commands.Network.Models.PSVpnConnectionPacketCaptureResult</span></span>

## <span data-ttu-id="e89c7-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e89c7-145">NOTES</span></span>

## <span data-ttu-id="e89c7-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e89c7-146">RELATED LINKS</span></span>

[<span data-ttu-id="e89c7-147">Stop-AzVpnConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e89c7-147">Stop-AzVpnConnectionPacketCapture</span></span>](./Stop-AzVpnConnectionPacketCapture.md)