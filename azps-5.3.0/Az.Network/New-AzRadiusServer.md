---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azradiusserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRadiusServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRadiusServer.md
ms.openlocfilehash: 0f92f09d3caf481f845c96942fd038a82c1078ee
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490972"
---
# <span data-ttu-id="4678b-101">New-AzRadiusServer</span><span class="sxs-lookup"><span data-stu-id="4678b-101">New-AzRadiusServer</span></span>

## <span data-ttu-id="4678b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4678b-102">SYNOPSIS</span></span>
<span data-ttu-id="4678b-103">외부 반경 서버 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4678b-103">Creates an external radius server configuration</span></span>

## <span data-ttu-id="4678b-104">구문</span><span class="sxs-lookup"><span data-stu-id="4678b-104">SYNTAX</span></span>

```
New-AzRadiusServer -RadiusServerAddress <String> -RadiusServerSecret <SecureString>
 [-RadiusServerScore <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4678b-105">설명</span><span class="sxs-lookup"><span data-stu-id="4678b-105">DESCRIPTION</span></span>
<span data-ttu-id="4678b-106">이 New-AzRadiusServer cmdlet은 가상 네트워크 게이트웨이 및 VPN 서버 구성에 사용할 외부 반경 서버 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4678b-106">The New-AzRadiusServer cmdlet creates an external radius server configuration to be used in virtual network gateway and VPN server configuration.</span></span>

## <span data-ttu-id="4678b-107">예제</span><span class="sxs-lookup"><span data-stu-id="4678b-107">EXAMPLES</span></span>

### <span data-ttu-id="4678b-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="4678b-108">Example 1</span></span>
```powershell
PS C:\> $radiusServer1 = New-AzRadiusServer -RadiusServerAddress 10.1.0.1 -RadiusServerSecret $radiuspd -RadiusServerScore 30
PS C:\> $radiusServer2 = New-AzRadiusServer -RadiusServerAddress 10.1.0.2 -RadiusServerSecret $radiuspd -RadiusServerScore 1
PS C:\> New-AzVirtualNetworkGateway -ResourceGroupName $rgname -name $rname -location $location -IpConfigurations $vnetIpConfig -GatewayType Vpn -VpnType RouteBased -EnableBgp $false -GatewaySku VpnGw1 -VpnClientAddressPool 201.169.0.0/16 -VpnClientProtocol "IkeV2" -RadiusServerList $radiusServers
```

<span data-ttu-id="4678b-109">새 가상 네트워크 게이트웨이에서 P2S를 구성하는 데 사용할 여러 외부 반경 서버 구성을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="4678b-109">Creating multiple external radius server configurations to be used for configuring P2S on a new virtual network gateway.</span></span>

## <span data-ttu-id="4678b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4678b-110">PARAMETERS</span></span>

### <span data-ttu-id="4678b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4678b-111">-DefaultProfile</span></span>
<span data-ttu-id="4678b-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4678b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4678b-113">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="4678b-113">-RadiusServerAddress</span></span>
<span data-ttu-id="4678b-114">외부 반경 서버 주소</span><span class="sxs-lookup"><span data-stu-id="4678b-114">External radius server address</span></span>

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

### <span data-ttu-id="4678b-115">-RadiusServerScore</span><span class="sxs-lookup"><span data-stu-id="4678b-115">-RadiusServerScore</span></span>
<span data-ttu-id="4678b-116">외부 반경 서버 점수</span><span class="sxs-lookup"><span data-stu-id="4678b-116">External radius server score</span></span>

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

### <span data-ttu-id="4678b-117">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="4678b-117">-RadiusServerSecret</span></span>
<span data-ttu-id="4678b-118">외부 반경 서버 비밀</span><span class="sxs-lookup"><span data-stu-id="4678b-118">External radius server secret</span></span>

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

### <span data-ttu-id="4678b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4678b-119">CommonParameters</span></span>
<span data-ttu-id="4678b-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4678b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4678b-121">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4678b-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4678b-122">입력</span><span class="sxs-lookup"><span data-stu-id="4678b-122">INPUTS</span></span>

### <span data-ttu-id="4678b-123">System.String</span><span class="sxs-lookup"><span data-stu-id="4678b-123">System.String</span></span>

### <span data-ttu-id="4678b-124">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="4678b-124">System.Security.SecureString</span></span>

### <span data-ttu-id="4678b-125">System.Int32</span><span class="sxs-lookup"><span data-stu-id="4678b-125">System.Int32</span></span>

## <span data-ttu-id="4678b-126">출력</span><span class="sxs-lookup"><span data-stu-id="4678b-126">OUTPUTS</span></span>

### <span data-ttu-id="4678b-127">Microsoft.Azure.Commands.Network.Models.PSRadiusServer</span><span class="sxs-lookup"><span data-stu-id="4678b-127">Microsoft.Azure.Commands.Network.Models.PSRadiusServer</span></span>

## <span data-ttu-id="4678b-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4678b-128">NOTES</span></span>

## <span data-ttu-id="4678b-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4678b-129">RELATED LINKS</span></span>
