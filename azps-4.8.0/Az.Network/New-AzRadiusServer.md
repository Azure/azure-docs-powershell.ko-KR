---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azradiusserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRadiusServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRadiusServer.md
ms.openlocfilehash: 0f92f09d3caf481f845c96942fd038a82c1078ee
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056177"
---
# <span data-ttu-id="6ed3f-101">New-AzRadiusServer</span><span class="sxs-lookup"><span data-stu-id="6ed3f-101">New-AzRadiusServer</span></span>

## <span data-ttu-id="6ed3f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ed3f-102">SYNOPSIS</span></span>
<span data-ttu-id="6ed3f-103">외부 radius 서버 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6ed3f-103">Creates an external radius server configuration</span></span>

## <span data-ttu-id="6ed3f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6ed3f-104">SYNTAX</span></span>

```
New-AzRadiusServer -RadiusServerAddress <String> -RadiusServerSecret <SecureString>
 [-RadiusServerScore <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6ed3f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="6ed3f-105">DESCRIPTION</span></span>
<span data-ttu-id="6ed3f-106">New-AzRadiusServer cmdlet은 가상 네트워크 게이트웨이 및 VPN 서버 구성에서 사용할 외부 radius 서버 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6ed3f-106">The New-AzRadiusServer cmdlet creates an external radius server configuration to be used in virtual network gateway and VPN server configuration.</span></span>

## <span data-ttu-id="6ed3f-107">예제의</span><span class="sxs-lookup"><span data-stu-id="6ed3f-107">EXAMPLES</span></span>

### <span data-ttu-id="6ed3f-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="6ed3f-108">Example 1</span></span>
```powershell
PS C:\> $radiusServer1 = New-AzRadiusServer -RadiusServerAddress 10.1.0.1 -RadiusServerSecret $radiuspd -RadiusServerScore 30
PS C:\> $radiusServer2 = New-AzRadiusServer -RadiusServerAddress 10.1.0.2 -RadiusServerSecret $radiuspd -RadiusServerScore 1
PS C:\> New-AzVirtualNetworkGateway -ResourceGroupName $rgname -name $rname -location $location -IpConfigurations $vnetIpConfig -GatewayType Vpn -VpnType RouteBased -EnableBgp $false -GatewaySku VpnGw1 -VpnClientAddressPool 201.169.0.0/16 -VpnClientProtocol "IkeV2" -RadiusServerList $radiusServers
```

<span data-ttu-id="6ed3f-109">새 가상 네트워크 게이트웨이에서 P2S를 구성 하는 데 사용할 여러 외부 radius 서버 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6ed3f-109">Creating multiple external radius server configurations to be used for configuring P2S on a new virtual network gateway.</span></span>

## <span data-ttu-id="6ed3f-110">변수</span><span class="sxs-lookup"><span data-stu-id="6ed3f-110">PARAMETERS</span></span>

### <span data-ttu-id="6ed3f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ed3f-111">-DefaultProfile</span></span>
<span data-ttu-id="6ed3f-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6ed3f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ed3f-113">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="6ed3f-113">-RadiusServerAddress</span></span>
<span data-ttu-id="6ed3f-114">외부 radius 서버 주소</span><span class="sxs-lookup"><span data-stu-id="6ed3f-114">External radius server address</span></span>

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

### <span data-ttu-id="6ed3f-115">-RadiusServerScore</span><span class="sxs-lookup"><span data-stu-id="6ed3f-115">-RadiusServerScore</span></span>
<span data-ttu-id="6ed3f-116">외부 radius 서버 점수</span><span class="sxs-lookup"><span data-stu-id="6ed3f-116">External radius server score</span></span>

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

### <span data-ttu-id="6ed3f-117">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="6ed3f-117">-RadiusServerSecret</span></span>
<span data-ttu-id="6ed3f-118">외부 radius 서버 비밀</span><span class="sxs-lookup"><span data-stu-id="6ed3f-118">External radius server secret</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ed3f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ed3f-119">CommonParameters</span></span>
<span data-ttu-id="6ed3f-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ed3f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ed3f-121">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6ed3f-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ed3f-122">입력</span><span class="sxs-lookup"><span data-stu-id="6ed3f-122">INPUTS</span></span>

### <span data-ttu-id="6ed3f-123">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="6ed3f-123">System.String</span></span>

### <span data-ttu-id="6ed3f-124">System.webserver</span><span class="sxs-lookup"><span data-stu-id="6ed3f-124">System.Security.SecureString</span></span>

### <span data-ttu-id="6ed3f-125">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="6ed3f-125">System.Int32</span></span>

## <span data-ttu-id="6ed3f-126">출력</span><span class="sxs-lookup"><span data-stu-id="6ed3f-126">OUTPUTS</span></span>

### <span data-ttu-id="6ed3f-127">PSRadiusServer에 대 한.</span><span class="sxs-lookup"><span data-stu-id="6ed3f-127">Microsoft.Azure.Commands.Network.Models.PSRadiusServer</span></span>

## <span data-ttu-id="6ed3f-128">상속자</span><span class="sxs-lookup"><span data-stu-id="6ed3f-128">NOTES</span></span>

## <span data-ttu-id="6ed3f-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6ed3f-129">RELATED LINKS</span></span>
