---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: BCB64535-FF37-46EF-85AF-7286BB67787B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermvirtualnetworkgatewayipconfig
schema: 2.0.0
ms.openlocfilehash: 340baa4b7a7d0afaf0e0523cb8c2f14f8270bf7c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93883017"
---
# <span data-ttu-id="60759-101">Add-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="60759-101">Add-AzureRmVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="60759-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60759-102">SYNOPSIS</span></span>
<span data-ttu-id="60759-103">가상 네트워크 게이트웨이에 IP 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="60759-103">Adds an IP configuration to a virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="60759-104">구문과</span><span class="sxs-lookup"><span data-stu-id="60759-104">SYNTAX</span></span>

### <span data-ttu-id="60759-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="60759-105">SetByResourceId</span></span>
```
Add-AzureRmVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-PrivateIpAddress <String>] [-SubnetId <String>] [-PublicIpAddressId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60759-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="60759-106">SetByResource</span></span>
```
Add-AzureRmVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-PrivateIpAddress <String>] [-Subnet <PSSubnet>] [-PublicIpAddress <PSPublicIpAddress>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60759-107">설명은</span><span class="sxs-lookup"><span data-stu-id="60759-107">DESCRIPTION</span></span>
<span data-ttu-id="60759-108">**Add-AzureRmVirtualNetworkGatewayIpConfig** cmdlet은 가상 네트워크 게이트웨이에 IP 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="60759-108">The **Add-AzureRmVirtualNetworkGatewayIpConfig** cmdlet adds an IP configuration to a virtual network gateway.</span></span>

## <span data-ttu-id="60759-109">예제의</span><span class="sxs-lookup"><span data-stu-id="60759-109">EXAMPLES</span></span>

### <span data-ttu-id="60759-110">raid-1</span><span class="sxs-lookup"><span data-stu-id="60759-110">1:</span></span>
```

```

## <span data-ttu-id="60759-111">변수</span><span class="sxs-lookup"><span data-stu-id="60759-111">PARAMETERS</span></span>

### <span data-ttu-id="60759-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60759-112">-DefaultProfile</span></span>
<span data-ttu-id="60759-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="60759-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="60759-114">-이름</span><span class="sxs-lookup"><span data-stu-id="60759-114">-Name</span></span>
<span data-ttu-id="60759-115">추가할 게이트웨이 IP 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="60759-115">Specifies the name of the gateway IP configuration to add.</span></span>

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

### <span data-ttu-id="60759-116">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="60759-116">-PrivateIpAddress</span></span>
<span data-ttu-id="60759-117">개인 IP 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="60759-117">Specifies the private IP address.</span></span>

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

### <span data-ttu-id="60759-118">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="60759-118">-PublicIpAddress</span></span>
<span data-ttu-id="60759-119">공용 IP 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="60759-119">Specifies the public IP address.</span></span>

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

### <span data-ttu-id="60759-120">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="60759-120">-PublicIpAddressId</span></span>
<span data-ttu-id="60759-121">공용 IP 주소의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="60759-121">Specifies the ID of the public IP address.</span></span>

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

### <span data-ttu-id="60759-122">-서브넷</span><span class="sxs-lookup"><span data-stu-id="60759-122">-Subnet</span></span>
<span data-ttu-id="60759-123">**Pssubnet** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="60759-123">Specifies a **PSSubnet** object.</span></span>

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

### <span data-ttu-id="60759-124">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="60759-124">-SubnetId</span></span>
<span data-ttu-id="60759-125">서브넷의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="60759-125">Specifies the ID of the subnet.</span></span>

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

### <span data-ttu-id="60759-126">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="60759-126">-VirtualNetworkGateway</span></span>
<span data-ttu-id="60759-127">**PSVirtualNetworkGateway** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="60759-127">Specifies a **PSVirtualNetworkGateway** object.</span></span>
<span data-ttu-id="60759-128">이 cmdlet은 사용자가 지정 하는 **PSVirtualNetworkGateway** 개체를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="60759-128">This cmdlet modifies the **PSVirtualNetworkGateway** object that you specify.</span></span>
<span data-ttu-id="60759-129">Get-AzureRmVirtualNetworkGateway cmdlet을 사용 하 여 **PSVirtualNetworkGateway** 개체를 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="60759-129">You can use the Get-AzureRmVirtualNetworkGateway cmdlet to retrieve a **PSVirtualNetworkGateway** object.</span></span>

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

### <span data-ttu-id="60759-130">-확인</span><span class="sxs-lookup"><span data-stu-id="60759-130">-Confirm</span></span>
<span data-ttu-id="60759-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="60759-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60759-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60759-132">-WhatIf</span></span>
<span data-ttu-id="60759-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="60759-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60759-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="60759-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60759-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60759-135">CommonParameters</span></span>
<span data-ttu-id="60759-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="60759-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60759-137">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60759-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60759-138">입력</span><span class="sxs-lookup"><span data-stu-id="60759-138">INPUTS</span></span>

### <span data-ttu-id="60759-139">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="60759-139">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="60759-140">' VirtualNetworkGateway ' 매개 변수는 파이프라인에서 ' PSVirtualNetworkGateway ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="60759-140">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="60759-141">출력</span><span class="sxs-lookup"><span data-stu-id="60759-141">OUTPUTS</span></span>

### <span data-ttu-id="60759-142">PSVirtualNetworkGateway에 대 한.</span><span class="sxs-lookup"><span data-stu-id="60759-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="60759-143">상속자</span><span class="sxs-lookup"><span data-stu-id="60759-143">NOTES</span></span>

## <span data-ttu-id="60759-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="60759-144">RELATED LINKS</span></span>

[<span data-ttu-id="60759-145">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="60759-145">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="60759-146">새로운 AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="60759-146">New-AzureRmVirtualNetworkGatewayIpConfig</span></span>](./New-AzureRmVirtualNetworkGatewayIpConfig.md)

[<span data-ttu-id="60759-147">제거-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="60759-147">Remove-AzureRmVirtualNetworkGatewayIpConfig</span></span>](./Remove-AzureRmVirtualNetworkGatewayIpConfig.md)


