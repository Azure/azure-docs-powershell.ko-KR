---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: BCB64535-FF37-46EF-85AF-7286BB67787B
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualnetworkgatewayipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: 31790ead292c9146aa73f41c56e79f3bdf51c715
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875661"
---
# <span data-ttu-id="ada40-101">Add-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="ada40-101">Add-AzVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="ada40-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ada40-102">SYNOPSIS</span></span>
<span data-ttu-id="ada40-103">가상 네트워크 게이트웨이에 IP 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="ada40-103">Adds an IP configuration to a virtual network gateway.</span></span>

## <span data-ttu-id="ada40-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ada40-104">SYNTAX</span></span>

### <span data-ttu-id="ada40-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="ada40-105">SetByResourceId</span></span>
```
Add-AzVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-PrivateIpAddress <String>] [-SubnetId <String>] [-PublicIpAddressId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ada40-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="ada40-106">SetByResource</span></span>
```
Add-AzVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-PrivateIpAddress <String>] [-Subnet <PSSubnet>] [-PublicIpAddress <PSPublicIpAddress>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ada40-107">설명은</span><span class="sxs-lookup"><span data-stu-id="ada40-107">DESCRIPTION</span></span>
<span data-ttu-id="ada40-108">**Add-AzVirtualNetworkGatewayIpConfig** cmdlet은 가상 네트워크 게이트웨이에 IP 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="ada40-108">The **Add-AzVirtualNetworkGatewayIpConfig** cmdlet adds an IP configuration to a virtual network gateway.</span></span>

## <span data-ttu-id="ada40-109">예제의</span><span class="sxs-lookup"><span data-stu-id="ada40-109">EXAMPLES</span></span>

### <span data-ttu-id="ada40-110">raid-1</span><span class="sxs-lookup"><span data-stu-id="ada40-110">1:</span></span>
```

```

## <span data-ttu-id="ada40-111">변수</span><span class="sxs-lookup"><span data-stu-id="ada40-111">PARAMETERS</span></span>

### <span data-ttu-id="ada40-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ada40-112">-DefaultProfile</span></span>
<span data-ttu-id="ada40-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ada40-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ada40-114">-이름</span><span class="sxs-lookup"><span data-stu-id="ada40-114">-Name</span></span>
<span data-ttu-id="ada40-115">추가할 게이트웨이 IP 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ada40-115">Specifies the name of the gateway IP configuration to add.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ada40-116">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="ada40-116">-PrivateIpAddress</span></span>
<span data-ttu-id="ada40-117">개인 IP 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ada40-117">Specifies the private IP address.</span></span>

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

### <span data-ttu-id="ada40-118">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="ada40-118">-PublicIpAddress</span></span>
<span data-ttu-id="ada40-119">공용 IP 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ada40-119">Specifies the public IP address.</span></span>

```yaml
Type: PSPublicIpAddress
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ada40-120">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="ada40-120">-PublicIpAddressId</span></span>
<span data-ttu-id="ada40-121">공용 IP 주소의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ada40-121">Specifies the ID of the public IP address.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ada40-122">-서브넷</span><span class="sxs-lookup"><span data-stu-id="ada40-122">-Subnet</span></span>
<span data-ttu-id="ada40-123">**Pssubnet** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ada40-123">Specifies a **PSSubnet** object.</span></span>

```yaml
Type: PSSubnet
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ada40-124">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="ada40-124">-SubnetId</span></span>
<span data-ttu-id="ada40-125">서브넷의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ada40-125">Specifies the ID of the subnet.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ada40-126">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ada40-126">-VirtualNetworkGateway</span></span>
<span data-ttu-id="ada40-127">**PSVirtualNetworkGateway** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ada40-127">Specifies a **PSVirtualNetworkGateway** object.</span></span>
<span data-ttu-id="ada40-128">이 cmdlet은 사용자가 지정 하는 **PSVirtualNetworkGateway** 개체를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ada40-128">This cmdlet modifies the **PSVirtualNetworkGateway** object that you specify.</span></span>
<span data-ttu-id="ada40-129">Get-AzVirtualNetworkGateway cmdlet을 사용 하 여 **PSVirtualNetworkGateway** 개체를 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ada40-129">You can use the Get-AzVirtualNetworkGateway cmdlet to retrieve a **PSVirtualNetworkGateway** object.</span></span>

```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ada40-130">-확인</span><span class="sxs-lookup"><span data-stu-id="ada40-130">-Confirm</span></span>
<span data-ttu-id="ada40-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ada40-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ada40-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ada40-132">-WhatIf</span></span>
<span data-ttu-id="ada40-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ada40-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ada40-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ada40-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ada40-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ada40-135">CommonParameters</span></span>
<span data-ttu-id="ada40-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ada40-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ada40-137">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ada40-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ada40-138">입력</span><span class="sxs-lookup"><span data-stu-id="ada40-138">INPUTS</span></span>

### <span data-ttu-id="ada40-139">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ada40-139">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="ada40-140">' VirtualNetworkGateway ' 매개 변수는 파이프라인에서 ' PSVirtualNetworkGateway ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ada40-140">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="ada40-141">출력</span><span class="sxs-lookup"><span data-stu-id="ada40-141">OUTPUTS</span></span>

### <span data-ttu-id="ada40-142">PSVirtualNetworkGateway에 대 한.</span><span class="sxs-lookup"><span data-stu-id="ada40-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="ada40-143">상속자</span><span class="sxs-lookup"><span data-stu-id="ada40-143">NOTES</span></span>

## <span data-ttu-id="ada40-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ada40-144">RELATED LINKS</span></span>

[<span data-ttu-id="ada40-145">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ada40-145">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="ada40-146">새로운 AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="ada40-146">New-AzVirtualNetworkGatewayIpConfig</span></span>](./New-AzVirtualNetworkGatewayIpConfig.md)

[<span data-ttu-id="ada40-147">제거-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="ada40-147">Remove-AzVirtualNetworkGatewayIpConfig</span></span>](./Remove-AzVirtualNetworkGatewayIpConfig.md)


