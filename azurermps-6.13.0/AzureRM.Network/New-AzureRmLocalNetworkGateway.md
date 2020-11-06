---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 59BE802E-C061-4E25-A446-B00B0BA36019
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLocalNetworkGateway.md
ms.openlocfilehash: bec6ded02853fbcfc08db38f0e627433d1d1ae10
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530187"
---
# <span data-ttu-id="46869-101">New-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="46869-101">New-AzureRmLocalNetworkGateway</span></span>

## <span data-ttu-id="46869-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46869-102">SYNOPSIS</span></span>
<span data-ttu-id="46869-103">로컬 네트워크 게이트웨이 만들기</span><span class="sxs-lookup"><span data-stu-id="46869-103">Creates a Local Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="46869-104">구문과</span><span class="sxs-lookup"><span data-stu-id="46869-104">SYNTAX</span></span>

```
New-AzureRmLocalNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-GatewayIpAddress <String>] [-AddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-Asn <UInt32>] [-BgpPeeringAddress <String>] [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46869-105">설명은</span><span class="sxs-lookup"><span data-stu-id="46869-105">DESCRIPTION</span></span>
<span data-ttu-id="46869-106">로컬 네트워크 게이트웨이는 온-프레미스의 VPN 장치를 나타내는 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="46869-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>
<span data-ttu-id="46869-107">**AzureRmLocalNetworkGateway** cmdlet은 게이트웨이의 이름, 리소스 그룹 이름, 위치, IP 주소, 그리고 Azure에 연결 되는 온-프레미스 네트워크의 주소 접두사에 따라 프레미스 게이트웨이를 나타내는 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="46869-107">The **New-AzureRmLocalNetworkGateway** cmdlet creates the object representing your on-prem gateway based on the Name, Resource Group Name, Location, and IP Address of the gateway, as well as the Address Prefix of the On-Premises network which will be connecting to Azure.</span></span>

## <span data-ttu-id="46869-108">예제의</span><span class="sxs-lookup"><span data-stu-id="46869-108">EXAMPLES</span></span>

### <span data-ttu-id="46869-109">1: 로컬 네트워크 게이트웨이 만들기</span><span class="sxs-lookup"><span data-stu-id="46869-109">1: Create a Local Network Gateway</span></span>
```
New-AzureRmLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG -Location "West US" -GatewayIpAddress 23.99.221.164 -AddressPrefix "10.5.51.0/24"
```

<span data-ttu-id="46869-110">"서쪽 US"의 리소스 그룹 "myRG" 내에서 이름이 "myLocalGW" 인 로컬 네트워크 게이트웨이의 개체를 만들고 IP 주소 "23.99.221.164" 및 주소 접두사 "10.5.51.0/24" 온-프레미스를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="46869-110">Creates the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG" in location "West US" with the IP address "23.99.221.164" and the address prefix "10.5.51.0/24" on-prem.</span></span>

## <span data-ttu-id="46869-111">변수</span><span class="sxs-lookup"><span data-stu-id="46869-111">PARAMETERS</span></span>

### <span data-ttu-id="46869-112">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="46869-112">-AddressPrefix</span></span>
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

### <span data-ttu-id="46869-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="46869-113">-AsJob</span></span>
<span data-ttu-id="46869-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="46869-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="46869-115">-Asn</span><span class="sxs-lookup"><span data-stu-id="46869-115">-Asn</span></span>
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

### <span data-ttu-id="46869-116">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="46869-116">-BgpPeeringAddress</span></span>
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

### <span data-ttu-id="46869-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46869-117">-DefaultProfile</span></span>
<span data-ttu-id="46869-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="46869-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="46869-119">-Force</span><span class="sxs-lookup"><span data-stu-id="46869-119">-Force</span></span>
<span data-ttu-id="46869-120">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="46869-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="46869-121">-게이트웨이 Ipaddress</span><span class="sxs-lookup"><span data-stu-id="46869-121">-GatewayIpAddress</span></span>
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

### <span data-ttu-id="46869-122">-위치</span><span class="sxs-lookup"><span data-stu-id="46869-122">-Location</span></span>
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

### <span data-ttu-id="46869-123">-이름</span><span class="sxs-lookup"><span data-stu-id="46869-123">-Name</span></span>
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

### <span data-ttu-id="46869-124">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="46869-124">-PeerWeight</span></span>
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

### <span data-ttu-id="46869-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46869-125">-ResourceGroupName</span></span>
<span data-ttu-id="46869-126">로컬 네트워크 게이트웨이가 속한 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="46869-126">Specifies the resource group that the local network gateway belongs to.</span></span>

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

### <span data-ttu-id="46869-127">태그</span><span class="sxs-lookup"><span data-stu-id="46869-127">-Tag</span></span>
<span data-ttu-id="46869-128">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="46869-128">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="46869-129">예: @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="46869-129">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="46869-130">-확인</span><span class="sxs-lookup"><span data-stu-id="46869-130">-Confirm</span></span>
<span data-ttu-id="46869-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="46869-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46869-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46869-132">-WhatIf</span></span>
<span data-ttu-id="46869-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="46869-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46869-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="46869-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46869-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46869-135">CommonParameters</span></span>
<span data-ttu-id="46869-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="46869-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46869-137">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46869-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46869-138">입력</span><span class="sxs-lookup"><span data-stu-id="46869-138">INPUTS</span></span>

### <span data-ttu-id="46869-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="46869-139">System.String</span></span>

### <span data-ttu-id="46869-140">System.webserver. List ' 1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="46869-140">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="46869-141">시스템. UInt32</span><span class="sxs-lookup"><span data-stu-id="46869-141">System.UInt32</span></span>

### <span data-ttu-id="46869-142">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="46869-142">System.Int32</span></span>

### <span data-ttu-id="46869-143">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="46869-143">System.Collections.Hashtable</span></span>

## <span data-ttu-id="46869-144">출력</span><span class="sxs-lookup"><span data-stu-id="46869-144">OUTPUTS</span></span>

### <span data-ttu-id="46869-145">Microsoft. 네트워크. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="46869-145">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="46869-146">상속자</span><span class="sxs-lookup"><span data-stu-id="46869-146">NOTES</span></span>

## <span data-ttu-id="46869-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="46869-147">RELATED LINKS</span></span>

[<span data-ttu-id="46869-148">Get-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="46869-148">Get-AzureRmLocalNetworkGateway</span></span>](./Get-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="46869-149">제거-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="46869-149">Remove-AzureRmLocalNetworkGateway</span></span>](./Remove-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="46869-150">Set-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="46869-150">Set-AzureRmLocalNetworkGateway</span></span>](./Set-AzureRmLocalNetworkGateway.md)
