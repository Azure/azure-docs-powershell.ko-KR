---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F8C1DF39-1DAF-4BDB-8B0E-1BC3B5E82185
online version: https://docs.microsoft.com/powershell/module/az.network/set-azlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLocalNetworkGateway.md
ms.openlocfilehash: b2e4890d89ecaaebaa6c6c48847c756138824586
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003392"
---
# <span data-ttu-id="19064-101">Set-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="19064-101">Set-AzLocalNetworkGateway</span></span>

## <span data-ttu-id="19064-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19064-102">SYNOPSIS</span></span>
<span data-ttu-id="19064-103">로컬 네트워크 게이트웨이를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="19064-103">Modifies a local network gateway.</span></span>

## <span data-ttu-id="19064-104">구문</span><span class="sxs-lookup"><span data-stu-id="19064-104">SYNTAX</span></span>

```
Set-AzLocalNetworkGateway -LocalNetworkGateway <PSLocalNetworkGateway> [-AddressPrefix <String[]>]
 [-Asn <UInt32>] [-BgpPeeringAddress <String>] [-PeerWeight <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="19064-105">설명</span><span class="sxs-lookup"><span data-stu-id="19064-105">DESCRIPTION</span></span>
<span data-ttu-id="19064-106">**Set-AzLocalNetworkGateway** cmdlet은 로컬 네트워크 게이트웨이를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="19064-106">The **Set-AzLocalNetworkGateway** cmdlet modifies a local network gateway.</span></span>

## <span data-ttu-id="19064-107">예제</span><span class="sxs-lookup"><span data-stu-id="19064-107">EXAMPLES</span></span>

### <span data-ttu-id="19064-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="19064-108">Example 1</span></span>
<span data-ttu-id="19064-109">기존 게이트웨이에 대한 구성 설정</span><span class="sxs-lookup"><span data-stu-id="19064-109">Set configuration for an existing gateway</span></span>


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

## <span data-ttu-id="19064-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="19064-110">PARAMETERS</span></span>

### <span data-ttu-id="19064-111">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="19064-111">-AddressPrefix</span></span>
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

### <span data-ttu-id="19064-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="19064-112">-AsJob</span></span>
<span data-ttu-id="19064-113">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="19064-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="19064-114">-Asn</span><span class="sxs-lookup"><span data-stu-id="19064-114">-Asn</span></span>
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

### <span data-ttu-id="19064-115">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="19064-115">-BgpPeeringAddress</span></span>
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

### <span data-ttu-id="19064-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19064-116">-DefaultProfile</span></span>
<span data-ttu-id="19064-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="19064-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="19064-118">-LocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="19064-118">-LocalNetworkGateway</span></span>
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

### <span data-ttu-id="19064-119">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="19064-119">-PeerWeight</span></span>
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

### <span data-ttu-id="19064-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19064-120">CommonParameters</span></span>
<span data-ttu-id="19064-121">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="19064-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19064-122">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="19064-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19064-123">입력</span><span class="sxs-lookup"><span data-stu-id="19064-123">INPUTS</span></span>

### <span data-ttu-id="19064-124">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="19064-124">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="19064-125">System.String[]</span><span class="sxs-lookup"><span data-stu-id="19064-125">System.String[]</span></span>

### <span data-ttu-id="19064-126">System.UInt32</span><span class="sxs-lookup"><span data-stu-id="19064-126">System.UInt32</span></span>

### <span data-ttu-id="19064-127">System.String</span><span class="sxs-lookup"><span data-stu-id="19064-127">System.String</span></span>

### <span data-ttu-id="19064-128">System.Int32</span><span class="sxs-lookup"><span data-stu-id="19064-128">System.Int32</span></span>

## <span data-ttu-id="19064-129">출력</span><span class="sxs-lookup"><span data-stu-id="19064-129">OUTPUTS</span></span>

### <span data-ttu-id="19064-130">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="19064-130">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="19064-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="19064-131">NOTES</span></span>

## <span data-ttu-id="19064-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="19064-132">RELATED LINKS</span></span>

[<span data-ttu-id="19064-133">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="19064-133">Get-AzLocalNetworkGateway</span></span>](./Get-AzLocalNetworkGateway.md)

[<span data-ttu-id="19064-134">New-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="19064-134">New-AzLocalNetworkGateway</span></span>](./New-AzLocalNetworkGateway.md)

[<span data-ttu-id="19064-135">Remove-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="19064-135">Remove-AzLocalNetworkGateway</span></span>](./Remove-AzLocalNetworkGateway.md)
