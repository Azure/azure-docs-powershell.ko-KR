---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F8C1DF39-1DAF-4BDB-8B0E-1BC3B5E82185
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLocalNetworkGateway.md
ms.openlocfilehash: ac93b104a8ccc1afbeb41bcd11910b76f7d4039f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94219197"
---
# <span data-ttu-id="5e9bb-101">Set-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="5e9bb-101">Set-AzLocalNetworkGateway</span></span>

## <span data-ttu-id="5e9bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e9bb-102">SYNOPSIS</span></span>
<span data-ttu-id="5e9bb-103">로컬 네트워크 게이트웨이를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e9bb-103">Modifies a local network gateway.</span></span>

## <span data-ttu-id="5e9bb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5e9bb-104">SYNTAX</span></span>

```
Set-AzLocalNetworkGateway -LocalNetworkGateway <PSLocalNetworkGateway> [-AddressPrefix <String[]>]
 [-Asn <UInt32>] [-BgpPeeringAddress <String>] [-PeerWeight <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5e9bb-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5e9bb-105">DESCRIPTION</span></span>
<span data-ttu-id="5e9bb-106">**Set-AzLocalNetworkGateway** cmdlet은 로컬 네트워크 게이트웨이를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e9bb-106">The **Set-AzLocalNetworkGateway** cmdlet modifies a local network gateway.</span></span>

## <span data-ttu-id="5e9bb-107">예제의</span><span class="sxs-lookup"><span data-stu-id="5e9bb-107">EXAMPLES</span></span>

### <span data-ttu-id="5e9bb-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="5e9bb-108">Example 1</span></span>
<span data-ttu-id="5e9bb-109">기존 게이트웨이에 대 한 구성 설정</span><span class="sxs-lookup"><span data-stu-id="5e9bb-109">Set configuration for an existing gateway</span></span>


```
$lgw = Get-AzLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG
Set-AzLocalNetworkGateway -LocalNetworkGateway $lgw

Name                     : myLocalGW
ResourceGroupName        : TestRG1
Location                 : westus
Id                       : /subscriptions/81ab786c-56eb-4a4d-bb5f-f60329772466/resourceGroups/TestRG1/providers/Microso
                           ft.Network/localNetworkGateways/myLocalGW
Etag                     : W/"d2de6968-315e-411d-a4b8-a8c335abe61b"
ResourceGuid             : 393acf8b-dbb8-4b08-a9ea-c714570710e1
ProvisioningState        : Succeeded
Tags                     :
GatewayIpAddress         : 1.2.3.4
LocalNetworkAddressSpace : {
                             "AddressPrefixes": []
                           }
BgpSettings              : null
```

## <span data-ttu-id="5e9bb-110">변수</span><span class="sxs-lookup"><span data-stu-id="5e9bb-110">PARAMETERS</span></span>

### <span data-ttu-id="5e9bb-111">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="5e9bb-111">-AddressPrefix</span></span>
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

### <span data-ttu-id="5e9bb-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5e9bb-112">-AsJob</span></span>
<span data-ttu-id="5e9bb-113">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="5e9bb-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5e9bb-114">-Asn</span><span class="sxs-lookup"><span data-stu-id="5e9bb-114">-Asn</span></span>
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

### <span data-ttu-id="5e9bb-115">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="5e9bb-115">-BgpPeeringAddress</span></span>
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

### <span data-ttu-id="5e9bb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e9bb-116">-DefaultProfile</span></span>
<span data-ttu-id="5e9bb-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5e9bb-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5e9bb-118">-LocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="5e9bb-118">-LocalNetworkGateway</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5e9bb-119">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="5e9bb-119">-PeerWeight</span></span>
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

### <span data-ttu-id="5e9bb-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e9bb-120">CommonParameters</span></span>
<span data-ttu-id="5e9bb-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e9bb-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e9bb-122">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e9bb-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e9bb-123">입력</span><span class="sxs-lookup"><span data-stu-id="5e9bb-123">INPUTS</span></span>

### <span data-ttu-id="5e9bb-124">Microsoft. 네트워크. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="5e9bb-124">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="5e9bb-125">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="5e9bb-125">System.String[]</span></span>

### <span data-ttu-id="5e9bb-126">시스템. UInt32</span><span class="sxs-lookup"><span data-stu-id="5e9bb-126">System.UInt32</span></span>

### <span data-ttu-id="5e9bb-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="5e9bb-127">System.String</span></span>

### <span data-ttu-id="5e9bb-128">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="5e9bb-128">System.Int32</span></span>

## <span data-ttu-id="5e9bb-129">출력</span><span class="sxs-lookup"><span data-stu-id="5e9bb-129">OUTPUTS</span></span>

### <span data-ttu-id="5e9bb-130">Microsoft. 네트워크. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="5e9bb-130">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="5e9bb-131">상속자</span><span class="sxs-lookup"><span data-stu-id="5e9bb-131">NOTES</span></span>

## <span data-ttu-id="5e9bb-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5e9bb-132">RELATED LINKS</span></span>

[<span data-ttu-id="5e9bb-133">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="5e9bb-133">Get-AzLocalNetworkGateway</span></span>](./Get-AzLocalNetworkGateway.md)

[<span data-ttu-id="5e9bb-134">새로운 AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="5e9bb-134">New-AzLocalNetworkGateway</span></span>](./New-AzLocalNetworkGateway.md)

[<span data-ttu-id="5e9bb-135">제거-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="5e9bb-135">Remove-AzLocalNetworkGateway</span></span>](./Remove-AzLocalNetworkGateway.md)
