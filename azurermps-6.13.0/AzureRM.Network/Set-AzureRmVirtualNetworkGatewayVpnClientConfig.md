---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: EFB0D7A6-0C8A-4514-873D-672641CCCAF3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworkgatewayvpnclientconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayVpnClientConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayVpnClientConfig.md
ms.openlocfilehash: 6d2830836fd29edea2843fad4be1892edfa7fbb8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529452"
---
# <span data-ttu-id="ee54e-101">Set-AzureRmVirtualNetworkGatewayVpnClientConfig</span><span class="sxs-lookup"><span data-stu-id="ee54e-101">Set-AzureRmVirtualNetworkGatewayVpnClientConfig</span></span>

## <span data-ttu-id="ee54e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee54e-102">SYNOPSIS</span></span>
<span data-ttu-id="ee54e-103">가상 네트워크 게이트웨이의 VPN 클라이언트 주소 풀을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee54e-103">Sets the VPN client address pool for a virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ee54e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ee54e-104">SYNTAX</span></span>

### <span data-ttu-id="ee54e-105">기본값 (기본값)</span><span class="sxs-lookup"><span data-stu-id="ee54e-105">Default (Default)</span></span>
```
Set-AzureRmVirtualNetworkGatewayVpnClientConfig -VirtualNetworkGateway <PSVirtualNetworkGateway>
 -VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee54e-106">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="ee54e-106">RadiusServerConfiguration</span></span>
```
Set-AzureRmVirtualNetworkGatewayVpnClientConfig -VirtualNetworkGateway <PSVirtualNetworkGateway>
 -VpnClientAddressPool <System.Collections.Generic.List`1[System.String]> -RadiusServerAddress <String>
 -RadiusServerSecret <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ee54e-107">설명은</span><span class="sxs-lookup"><span data-stu-id="ee54e-107">DESCRIPTION</span></span>
<span data-ttu-id="ee54e-108">**AzureRmVirtualNetworkVpnClientConfig** cmdlet은 가상 네트워크 게이트웨이의 클라이언트 주소 풀을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee54e-108">The **Set-AzureRmVirtualNetworkVpnClientConfig** cmdlet configures the client address pool for a virtual network gateway.</span></span>
<span data-ttu-id="ee54e-109">이 게이트웨이에 연결 하는 VPN (가상 사설망) 클라이언트에이 주소 풀의 IP 주소가 할당 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ee54e-109">Virtual private network (VPN) clients that connect to this gateway will be assigned an IP address from this address pool.</span></span>

## <span data-ttu-id="ee54e-110">예제의</span><span class="sxs-lookup"><span data-stu-id="ee54e-110">EXAMPLES</span></span>

### <span data-ttu-id="ee54e-111">예제 1: 가상 네트워크 게이트웨이에 VPN 클라이언트 주소 풀 할당</span><span class="sxs-lookup"><span data-stu-id="ee54e-111">Example 1: Assign a VPN client address pool to a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Set-AzureRmVirtualNetworkGatewayVpnClientConfig -VirtualNetworkGateway $Gateway -VpnClientAddressPool "10.0.0.0/16"
```

<span data-ttu-id="ee54e-112">이 예제에서는 VPN 클라이언트 주소 풀을 ContosoVirtualGateway 이라는 가상 네트워크 게이트웨이에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee54e-112">This example assigns a VPN client address pool to a virtual network gateway named ContosoVirtualGateway.</span></span>
<span data-ttu-id="ee54e-113">첫 번째 명령은 gateway에 대 한 개체 참조를 만들고 개체는 $Gateway 라는 변수에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ee54e-113">The first command creates an object reference to the gateway and the object is stored in a variable named $Gateway.</span></span>
<span data-ttu-id="ee54e-114">그런 다음이 예제의 두 번째 명령은 **Set-AzureRmVirtualNetworkGatewayVpnClientConfig** cmdlet을 사용 하 여 주소 풀 10.0.0.0/16을 ContosoVirtualGateway에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee54e-114">The second command in the example then uses the **Set-AzureRmVirtualNetworkGatewayVpnClientConfig** cmdlet to assign the address pool 10.0.0.0/16 to ContosoVirtualGateway.</span></span>

### <span data-ttu-id="ee54e-115">예제 2: 기존 게이트웨이에서 외부 radius 기반 인증 구성</span><span class="sxs-lookup"><span data-stu-id="ee54e-115">Example 2: Configure external radius based authentication on existing gateway</span></span>
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> $Secure_String_Pwd = ConvertTo-SecureString "TestRadiusServerPassword" -AsPlainText -Force
PS C:\> Set-AzureRmVirtualNetworkGatewayVpnClientConfig -VirtualNetworkGateway $Gateway -VpnClientAddressPool "10.0.0.0/16" -RadiusServerAddress "TestRadiusServer" -RadiusServerSecret $Secure_String_Pwd
```

<span data-ttu-id="ee54e-116">이 예제에서는 VPN 클라이언트 주소 풀을 ContosoVirtualGateway 이라는 가상 네트워크 게이트웨이에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee54e-116">This example assigns a VPN client address pool to a virtual network gateway named ContosoVirtualGateway.</span></span>
<span data-ttu-id="ee54e-117">첫 번째 명령은 gateway에 대 한 개체 참조를 만들고 개체는 $Gateway 라는 변수에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ee54e-117">The first command creates an object reference to the gateway and the object is stored in a variable named $Gateway.</span></span>
<span data-ttu-id="ee54e-118">그런 다음이 예제의 두 번째 명령은 **Set-AzureRmVirtualNetworkGatewayVpnClientConfig** cmdlet을 사용 하 여 주소 풀 10.0.0.0/16을 ContosoVirtualGateway에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee54e-118">The second command in the example then uses the **Set-AzureRmVirtualNetworkGatewayVpnClientConfig** cmdlet to assign the address pool 10.0.0.0/16 to ContosoVirtualGateway.</span></span> <span data-ttu-id="ee54e-119">또한 vpn 클라이언트에 대 한 인증에 사용할 외부 radius 서버 "TestRadiusServer"를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee54e-119">It also configures the external radius server "TestRadiusServer" to be used for authentication for vpn clients.</span></span>

## <span data-ttu-id="ee54e-120">변수</span><span class="sxs-lookup"><span data-stu-id="ee54e-120">PARAMETERS</span></span>

### <span data-ttu-id="ee54e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee54e-121">-DefaultProfile</span></span>
<span data-ttu-id="ee54e-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ee54e-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ee54e-123">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="ee54e-123">-RadiusServerAddress</span></span>
<span data-ttu-id="ee54e-124">P2S 외부 Radius 서버 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="ee54e-124">P2S External Radius server address.</span></span>

```yaml
Type: System.String
Parameter Sets: RadiusServerConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee54e-125">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="ee54e-125">-RadiusServerSecret</span></span>
<span data-ttu-id="ee54e-126">P2S 외부 Radius 서버 비밀.</span><span class="sxs-lookup"><span data-stu-id="ee54e-126">P2S External Radius server secret.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: RadiusServerConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee54e-127">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ee54e-127">-VirtualNetworkGateway</span></span>
<span data-ttu-id="ee54e-128">이 cmdlet이 수정 하는 VPN 클라이언트 구성 설정이 포함 된 가상 네트워크 게이트웨이에 대 한 개체 참조를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee54e-128">Specifies an object reference to the virtual network gateway that contains the VPN client configuration settings that this cmdlet modifies.</span></span>
<span data-ttu-id="ee54e-129">Get-AzureRmVirtualNetworkGateway를 사용 하 고 게이트웨이의 이름을 지정 하 여 가상 네트워크 게이트웨이에 대 한 개체 참조를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ee54e-129">You can create an object reference to a virtual network gateway by using the Get-AzureRmVirtualNetworkGateway and specifying the name of the gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ee54e-130">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="ee54e-130">-VpnClientAddressPool</span></span>
<span data-ttu-id="ee54e-131">이 게이트웨이에 연결 하는 클라이언트에 할당할 IP 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee54e-131">Specifies the IP addresses to be assigned to clients connecting to this gateway</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee54e-132">-확인</span><span class="sxs-lookup"><span data-stu-id="ee54e-132">-Confirm</span></span>
<span data-ttu-id="ee54e-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee54e-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee54e-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee54e-134">-WhatIf</span></span>
<span data-ttu-id="ee54e-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ee54e-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ee54e-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ee54e-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee54e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee54e-137">CommonParameters</span></span>
<span data-ttu-id="ee54e-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee54e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee54e-139">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee54e-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee54e-140">입력</span><span class="sxs-lookup"><span data-stu-id="ee54e-140">INPUTS</span></span>

### <span data-ttu-id="ee54e-141">PSVirtualNetworkGateway에 대 한.</span><span class="sxs-lookup"><span data-stu-id="ee54e-141">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>
<span data-ttu-id="ee54e-142">매개 변수: VirtualNetworkGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ee54e-142">Parameters: VirtualNetworkGateway (ByValue)</span></span>

### <span data-ttu-id="ee54e-143">System.webserver. List ' 1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="ee54e-143">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="ee54e-144">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ee54e-144">System.String</span></span>

### <span data-ttu-id="ee54e-145">System.webserver</span><span class="sxs-lookup"><span data-stu-id="ee54e-145">System.Security.SecureString</span></span>

## <span data-ttu-id="ee54e-146">출력</span><span class="sxs-lookup"><span data-stu-id="ee54e-146">OUTPUTS</span></span>

### <span data-ttu-id="ee54e-147">PSVirtualNetworkGateway에 대 한.</span><span class="sxs-lookup"><span data-stu-id="ee54e-147">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="ee54e-148">상속자</span><span class="sxs-lookup"><span data-stu-id="ee54e-148">NOTES</span></span>

## <span data-ttu-id="ee54e-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ee54e-149">RELATED LINKS</span></span>

[<span data-ttu-id="ee54e-150">Get-AzureRmVpnClientPackage</span><span class="sxs-lookup"><span data-stu-id="ee54e-150">Get-AzureRmVpnClientPackage</span></span>](./Get-AzureRmVpnClientPackage.md)

[<span data-ttu-id="ee54e-151">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ee54e-151">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="ee54e-152">크기 조정-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ee54e-152">Resize-AzureRmVirtualNetworkGateway</span></span>](./Resize-AzureRmVirtualNetworkGateway.md)


