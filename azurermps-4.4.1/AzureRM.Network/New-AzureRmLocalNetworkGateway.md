---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 59BE802E-C061-4E25-A446-B00B0BA36019
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLocalNetworkGateway.md
ms.openlocfilehash: 3acfbf1462a1f0ae75d95b9f3976c46fd07676f4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533963"
---
# <span data-ttu-id="d86b4-101">New-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d86b4-101">New-AzureRmLocalNetworkGateway</span></span>

## <span data-ttu-id="d86b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d86b4-102">SYNOPSIS</span></span>
<span data-ttu-id="d86b4-103">로컬 네트워크 게이트웨이 만들기</span><span class="sxs-lookup"><span data-stu-id="d86b4-103">Creates a Local Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d86b4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d86b4-104">SYNTAX</span></span>

```
New-AzureRmLocalNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-GatewayIpAddress <String>] [-AddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-Asn <UInt32>] [-BgpPeeringAddress <String>] [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d86b4-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d86b4-105">DESCRIPTION</span></span>
<span data-ttu-id="d86b4-106">로컬 네트워크 게이트웨이는 온-프레미스의 VPN 장치를 나타내는 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="d86b4-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>

<span data-ttu-id="d86b4-107">**AzureRmLocalNetworkGateway** cmdlet은 게이트웨이의 이름, 리소스 그룹 이름, 위치, IP 주소, 그리고 Azure에 연결 되는 온-프레미스 네트워크의 주소 접두사에 따라 프레미스 게이트웨이를 나타내는 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d86b4-107">The **New-AzureRmLocalNetworkGateway** cmdlet creates the object representing your on-prem gateway based on the Name, Resource Group Name, Location, and IP Address of the gateway, as well as the Address Prefix of the On-Premises network which will be connecting to Azure.</span></span>

## <span data-ttu-id="d86b4-108">예제의</span><span class="sxs-lookup"><span data-stu-id="d86b4-108">EXAMPLES</span></span>

### <span data-ttu-id="d86b4-109">1: 로컬 네트워크 게이트웨이 만들기</span><span class="sxs-lookup"><span data-stu-id="d86b4-109">1: Create a Local Network Gateway</span></span>
```
New-AzureRmLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG -Location "West US" -GatewayIpAddress 23.99.221.164 -AddressPrefix "10.5.51.0/24"
```

<span data-ttu-id="d86b4-110">"서쪽 US"의 리소스 그룹 "myRG" 내에서 이름이 "myLocalGW" 인 로컬 네트워크 게이트웨이의 개체를 만들고 IP 주소 "23.99.221.164" 및 주소 접두사 "10.5.51.0/24" 온-프레미스를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d86b4-110">Creates the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG" in location "West US" with the IP address "23.99.221.164" and the address prefix "10.5.51.0/24" on-prem.</span></span>

## <span data-ttu-id="d86b4-111">변수</span><span class="sxs-lookup"><span data-stu-id="d86b4-111">PARAMETERS</span></span>

### <span data-ttu-id="d86b4-112">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="d86b4-112">-AddressPrefix</span></span>
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

### <span data-ttu-id="d86b4-113">-Asn</span><span class="sxs-lookup"><span data-stu-id="d86b4-113">-Asn</span></span>
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

### <span data-ttu-id="d86b4-114">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="d86b4-114">-BgpPeeringAddress</span></span>
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

### <span data-ttu-id="d86b4-115">-Force</span><span class="sxs-lookup"><span data-stu-id="d86b4-115">-Force</span></span>
<span data-ttu-id="d86b4-116">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="d86b4-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d86b4-117">-게이트웨이 Ipaddress</span><span class="sxs-lookup"><span data-stu-id="d86b4-117">-GatewayIpAddress</span></span>
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

### <span data-ttu-id="d86b4-118">-위치</span><span class="sxs-lookup"><span data-stu-id="d86b4-118">-Location</span></span>
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

### <span data-ttu-id="d86b4-119">-이름</span><span class="sxs-lookup"><span data-stu-id="d86b4-119">-Name</span></span>
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

### <span data-ttu-id="d86b4-120">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="d86b4-120">-PeerWeight</span></span>
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

### <span data-ttu-id="d86b4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d86b4-121">-ResourceGroupName</span></span>
<span data-ttu-id="d86b4-122">로컬 네트워크 게이트웨이가 속한 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d86b4-122">Specifies the resource group that the local network gateway belongs to.</span></span>

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

### <span data-ttu-id="d86b4-123">태그</span><span class="sxs-lookup"><span data-stu-id="d86b4-123">-Tag</span></span>
<span data-ttu-id="d86b4-124">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="d86b4-124">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="d86b4-125">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="d86b4-125">For example:</span></span>

<span data-ttu-id="d86b4-126">@ {key0 = "value0", key1 = $null, key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="d86b4-126">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="d86b4-127">-확인</span><span class="sxs-lookup"><span data-stu-id="d86b4-127">-Confirm</span></span>
<span data-ttu-id="d86b4-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d86b4-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d86b4-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d86b4-129">-WhatIf</span></span>
<span data-ttu-id="d86b4-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d86b4-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d86b4-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d86b4-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d86b4-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d86b4-132">-DefaultProfile</span></span>
<span data-ttu-id="d86b4-133">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d86b4-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d86b4-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d86b4-134">CommonParameters</span></span>
<span data-ttu-id="d86b4-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d86b4-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d86b4-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d86b4-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d86b4-137">입력</span><span class="sxs-lookup"><span data-stu-id="d86b4-137">INPUTS</span></span>

## <span data-ttu-id="d86b4-138">출력</span><span class="sxs-lookup"><span data-stu-id="d86b4-138">OUTPUTS</span></span>

### <span data-ttu-id="d86b4-139">Microsoft. 네트워크. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d86b4-139">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="d86b4-140">상속자</span><span class="sxs-lookup"><span data-stu-id="d86b4-140">NOTES</span></span>

## <span data-ttu-id="d86b4-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d86b4-141">RELATED LINKS</span></span>

[<span data-ttu-id="d86b4-142">Get-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d86b4-142">Get-AzureRmLocalNetworkGateway</span></span>](./Get-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="d86b4-143">제거-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d86b4-143">Remove-AzureRmLocalNetworkGateway</span></span>](./Remove-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="d86b4-144">Set-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d86b4-144">Set-AzureRmLocalNetworkGateway</span></span>](./Set-AzureRmLocalNetworkGateway.md)
