---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 59BE802E-C061-4E25-A446-B00B0BA36019
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLocalNetworkGateway.md
ms.openlocfilehash: 7f4a7568139cc41827e94c5bf538d11e2aa3dee4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193644"
---
# <span data-ttu-id="6a0e4-101">New-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="6a0e4-101">New-AzLocalNetworkGateway</span></span>

## <span data-ttu-id="6a0e4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a0e4-102">SYNOPSIS</span></span>
<span data-ttu-id="6a0e4-103">로컬 네트워크 게이트웨이를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6a0e4-103">Creates a Local Network Gateway</span></span>

## <span data-ttu-id="6a0e4-104">구문</span><span class="sxs-lookup"><span data-stu-id="6a0e4-104">SYNTAX</span></span>

### <span data-ttu-id="6a0e4-105">ByLocalNetworkGatewayIpAddress</span><span class="sxs-lookup"><span data-stu-id="6a0e4-105">ByLocalNetworkGatewayIpAddress</span></span>
```
New-AzLocalNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-GatewayIpAddress <String>] [-AddressPrefix <String[]>] [-Asn <UInt32>] [-BgpPeeringAddress <String>]
 [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a0e4-106">ByLocalNetworkGatewayFqdn</span><span class="sxs-lookup"><span data-stu-id="6a0e4-106">ByLocalNetworkGatewayFqdn</span></span>
```
New-AzLocalNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String> [-Fqdn <String>]
 [-AddressPrefix <String[]>] [-Asn <UInt32>] [-BgpPeeringAddress <String>] [-PeerWeight <Int32>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6a0e4-107">설명</span><span class="sxs-lookup"><span data-stu-id="6a0e4-107">DESCRIPTION</span></span>
<span data-ttu-id="6a0e4-108">로컬 네트워크 게이트웨이는 VPN 디바이스 On-프레미스를 나타내는 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="6a0e4-108">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>
<span data-ttu-id="6a0e4-109">**New-AzLocalNetworkGateway** cmdlet은 게이트웨이의 이름, 리소스 그룹 이름, 위치 및 IP 주소와 Azure에 연결할 On-프레미스 네트워크의 주소 주소를 기반으로 하여 프레미스 게이트웨이를 나타내는 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6a0e4-109">The **New-AzLocalNetworkGateway** cmdlet creates the object representing your on-prem gateway based on the Name, Resource Group Name, Location, and IP Address of the gateway, as well as the Address Prefix of the On-Premises network which will be connecting to Azure.</span></span>

## <span data-ttu-id="6a0e4-110">예제</span><span class="sxs-lookup"><span data-stu-id="6a0e4-110">EXAMPLES</span></span>

### <span data-ttu-id="6a0e4-111">예제 1: 로컬 네트워크 게이트웨이 만들기</span><span class="sxs-lookup"><span data-stu-id="6a0e4-111">Example 1: Create a Local Network Gateway</span></span>
```powershell
New-AzLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG -Location "West US" -GatewayIpAddress 23.99.221.164 -AddressPrefix "10.5.51.0/24"
```

<span data-ttu-id="6a0e4-112">IP 주소가 "23.99.221.164"이고 주소가 "10.5.51.0/24"인 "미국 서부"의 리소스 그룹 "myRG" 내에 "myLocalGW"라는 이름으로 로컬 네트워크 게이트웨이의 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6a0e4-112">Creates the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG" in location "West US" with the IP address "23.99.221.164" and the address prefix "10.5.51.0/24" on-prem.</span></span>

## <span data-ttu-id="6a0e4-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6a0e4-113">PARAMETERS</span></span>

### <span data-ttu-id="6a0e4-114">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="6a0e4-114">-AddressPrefix</span></span>
```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a0e4-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6a0e4-115">-AsJob</span></span>
<span data-ttu-id="6a0e4-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="6a0e4-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6a0e4-117">-Asn</span><span class="sxs-lookup"><span data-stu-id="6a0e4-117">-Asn</span></span>
```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a0e4-118">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="6a0e4-118">-BgpPeeringAddress</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a0e4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a0e4-119">-DefaultProfile</span></span>
<span data-ttu-id="6a0e4-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6a0e4-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6a0e4-121">-Force</span><span class="sxs-lookup"><span data-stu-id="6a0e4-121">-Force</span></span>
<span data-ttu-id="6a0e4-122">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="6a0e4-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6a0e4-123">-Fqdn</span><span class="sxs-lookup"><span data-stu-id="6a0e4-123">-Fqdn</span></span>
<span data-ttu-id="6a0e4-124">로컬 네트워크 게이트웨이의 FQDN입니다.</span><span class="sxs-lookup"><span data-stu-id="6a0e4-124">FQDN of local network gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: ByLocalNetworkGatewayFqdn
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a0e4-125">-GatewayIpAddress</span><span class="sxs-lookup"><span data-stu-id="6a0e4-125">-GatewayIpAddress</span></span>
```yaml
Type: System.String
Parameter Sets: ByLocalNetworkGatewayIpAddress
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a0e4-126">-Location</span><span class="sxs-lookup"><span data-stu-id="6a0e4-126">-Location</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a0e4-127">-Name</span><span class="sxs-lookup"><span data-stu-id="6a0e4-127">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a0e4-128">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="6a0e4-128">-PeerWeight</span></span>
```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a0e4-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a0e4-129">-ResourceGroupName</span></span>
<span data-ttu-id="6a0e4-130">로컬 네트워크 게이트웨이가 속한 리소스 그룹을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6a0e4-130">Specifies the resource group that the local network gateway belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a0e4-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="6a0e4-131">-Tag</span></span>
<span data-ttu-id="6a0e4-132">해시 테이블 형식의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="6a0e4-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="6a0e4-133">예: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="6a0e4-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a0e4-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6a0e4-134">-Confirm</span></span>
<span data-ttu-id="6a0e4-135">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="6a0e4-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a0e4-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a0e4-136">-WhatIf</span></span>
<span data-ttu-id="6a0e4-137">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="6a0e4-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a0e4-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6a0e4-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a0e4-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a0e4-139">CommonParameters</span></span>
<span data-ttu-id="6a0e4-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6a0e4-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a0e4-141">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6a0e4-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a0e4-142">입력</span><span class="sxs-lookup"><span data-stu-id="6a0e4-142">INPUTS</span></span>

### <span data-ttu-id="6a0e4-143">System.String</span><span class="sxs-lookup"><span data-stu-id="6a0e4-143">System.String</span></span>

### <span data-ttu-id="6a0e4-144">System.String[]</span><span class="sxs-lookup"><span data-stu-id="6a0e4-144">System.String[]</span></span>

### <span data-ttu-id="6a0e4-145">System.UInt32</span><span class="sxs-lookup"><span data-stu-id="6a0e4-145">System.UInt32</span></span>

### <span data-ttu-id="6a0e4-146">System.Int32</span><span class="sxs-lookup"><span data-stu-id="6a0e4-146">System.Int32</span></span>

### <span data-ttu-id="6a0e4-147">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="6a0e4-147">System.Collections.Hashtable</span></span>

## <span data-ttu-id="6a0e4-148">출력</span><span class="sxs-lookup"><span data-stu-id="6a0e4-148">OUTPUTS</span></span>

### <span data-ttu-id="6a0e4-149">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="6a0e4-149">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="6a0e4-150">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6a0e4-150">NOTES</span></span>

## <span data-ttu-id="6a0e4-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6a0e4-151">RELATED LINKS</span></span>

[<span data-ttu-id="6a0e4-152">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="6a0e4-152">Get-AzLocalNetworkGateway</span></span>](./Get-AzLocalNetworkGateway.md)

[<span data-ttu-id="6a0e4-153">Remove-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="6a0e4-153">Remove-AzLocalNetworkGateway</span></span>](./Remove-AzLocalNetworkGateway.md)

[<span data-ttu-id="6a0e4-154">Set-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="6a0e4-154">Set-AzLocalNetworkGateway</span></span>](./Set-AzLocalNetworkGateway.md)
