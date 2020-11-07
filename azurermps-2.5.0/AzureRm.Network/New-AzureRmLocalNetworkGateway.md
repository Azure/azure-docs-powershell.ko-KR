---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 59BE802E-C061-4E25-A446-B00B0BA36019
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermlocalnetworkgateway
schema: 2.0.0
ms.openlocfilehash: c450d2f6fd3d9a9b0368a667573aadadbd218d8f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93881838"
---
# <span data-ttu-id="84e37-101">New-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="84e37-101">New-AzureRmLocalNetworkGateway</span></span>

## <span data-ttu-id="84e37-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="84e37-102">SYNOPSIS</span></span>
<span data-ttu-id="84e37-103">로컬 네트워크 게이트웨이 만들기</span><span class="sxs-lookup"><span data-stu-id="84e37-103">Creates a Local Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="84e37-104">구문과</span><span class="sxs-lookup"><span data-stu-id="84e37-104">SYNTAX</span></span>

```
New-AzureRmLocalNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-GatewayIpAddress <String>] [-AddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-Asn <UInt32>] [-BgpPeeringAddress <String>] [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84e37-105">설명은</span><span class="sxs-lookup"><span data-stu-id="84e37-105">DESCRIPTION</span></span>
<span data-ttu-id="84e37-106">로컬 네트워크 게이트웨이는 온-프레미스의 VPN 장치를 나타내는 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="84e37-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>

<span data-ttu-id="84e37-107">**AzureRmLocalNetworkGateway** cmdlet은 게이트웨이의 이름, 리소스 그룹 이름, 위치, IP 주소, 그리고 Azure에 연결 되는 온-프레미스 네트워크의 주소 접두사에 따라 프레미스 게이트웨이를 나타내는 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="84e37-107">The **New-AzureRmLocalNetworkGateway** cmdlet creates the object representing your on-prem gateway based on the Name, Resource Group Name, Location, and IP Address of the gateway, as well as the Address Prefix of the On-Premises network which will be connecting to Azure.</span></span>

## <span data-ttu-id="84e37-108">예제의</span><span class="sxs-lookup"><span data-stu-id="84e37-108">EXAMPLES</span></span>

### <span data-ttu-id="84e37-109">1: 로컬 네트워크 게이트웨이 만들기</span><span class="sxs-lookup"><span data-stu-id="84e37-109">1: Create a Local Network Gateway</span></span>
```
New-AzureRmLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG -Location "West US" -GatewayIpAddress 23.99.221.164 -AddressPrefix "10.5.51.0/24"
```

<span data-ttu-id="84e37-110">"서쪽 US"의 리소스 그룹 "myRG" 내에서 이름이 "myLocalGW" 인 로컬 네트워크 게이트웨이의 개체를 만들고 IP 주소 "23.99.221.164" 및 주소 접두사 "10.5.51.0/24" 온-프레미스를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="84e37-110">Creates the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG" in location "West US" with the IP address "23.99.221.164" and the address prefix "10.5.51.0/24" on-prem.</span></span>

## <span data-ttu-id="84e37-111">변수</span><span class="sxs-lookup"><span data-stu-id="84e37-111">PARAMETERS</span></span>

### <span data-ttu-id="84e37-112">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="84e37-112">-AddressPrefix</span></span>
```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84e37-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="84e37-113">-AsJob</span></span>
<span data-ttu-id="84e37-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="84e37-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="84e37-115">-Asn</span><span class="sxs-lookup"><span data-stu-id="84e37-115">-Asn</span></span>
```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84e37-116">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="84e37-116">-BgpPeeringAddress</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84e37-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84e37-117">-DefaultProfile</span></span>
<span data-ttu-id="84e37-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="84e37-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84e37-119">-Force</span><span class="sxs-lookup"><span data-stu-id="84e37-119">-Force</span></span>
<span data-ttu-id="84e37-120">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="84e37-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="84e37-121">-게이트웨이 Ipaddress</span><span class="sxs-lookup"><span data-stu-id="84e37-121">-GatewayIpAddress</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84e37-122">-위치</span><span class="sxs-lookup"><span data-stu-id="84e37-122">-Location</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84e37-123">-이름</span><span class="sxs-lookup"><span data-stu-id="84e37-123">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84e37-124">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="84e37-124">-PeerWeight</span></span>
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84e37-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84e37-125">-ResourceGroupName</span></span>
<span data-ttu-id="84e37-126">로컬 네트워크 게이트웨이가 속한 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="84e37-126">Specifies the resource group that the local network gateway belongs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84e37-127">태그</span><span class="sxs-lookup"><span data-stu-id="84e37-127">-Tag</span></span>
<span data-ttu-id="84e37-128">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="84e37-128">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="84e37-129">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="84e37-129">For example:</span></span>

<span data-ttu-id="84e37-130">@ {key0 = "value0", key1 = $null, key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="84e37-130">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84e37-131">-확인</span><span class="sxs-lookup"><span data-stu-id="84e37-131">-Confirm</span></span>
<span data-ttu-id="84e37-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="84e37-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84e37-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84e37-133">-WhatIf</span></span>
<span data-ttu-id="84e37-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="84e37-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84e37-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="84e37-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84e37-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84e37-136">CommonParameters</span></span>
<span data-ttu-id="84e37-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="84e37-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84e37-138">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84e37-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84e37-139">입력</span><span class="sxs-lookup"><span data-stu-id="84e37-139">INPUTS</span></span>

## <span data-ttu-id="84e37-140">출력</span><span class="sxs-lookup"><span data-stu-id="84e37-140">OUTPUTS</span></span>

### <span data-ttu-id="84e37-141">Microsoft. 네트워크. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="84e37-141">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="84e37-142">상속자</span><span class="sxs-lookup"><span data-stu-id="84e37-142">NOTES</span></span>

## <span data-ttu-id="84e37-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="84e37-143">RELATED LINKS</span></span>

[<span data-ttu-id="84e37-144">Get-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="84e37-144">Get-AzureRmLocalNetworkGateway</span></span>](./Get-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="84e37-145">제거-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="84e37-145">Remove-AzureRmLocalNetworkGateway</span></span>](./Remove-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="84e37-146">Set-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="84e37-146">Set-AzureRmLocalNetworkGateway</span></span>](./Set-AzureRmLocalNetworkGateway.md)
