---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F8C1DF39-1DAF-4BDB-8B0E-1BC3B5E82185
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLocalNetworkGateway.md
ms.openlocfilehash: a37cb732aed95a2c31c970d83558a3eff8ab31c8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524376"
---
# <span data-ttu-id="bb9b3-101">Set-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="bb9b3-101">Set-AzureRmLocalNetworkGateway</span></span>

## <span data-ttu-id="bb9b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb9b3-102">SYNOPSIS</span></span>
<span data-ttu-id="bb9b3-103">로컬 네트워크 게이트웨이를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb9b3-103">Modifies a local network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bb9b3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bb9b3-104">SYNTAX</span></span>

```
Set-AzureRmLocalNetworkGateway -LocalNetworkGateway <PSLocalNetworkGateway>
 [-AddressPrefix <System.Collections.Generic.List`1[System.String]>] [-Asn <UInt32>]
 [-BgpPeeringAddress <String>] [-PeerWeight <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bb9b3-105">설명은</span><span class="sxs-lookup"><span data-stu-id="bb9b3-105">DESCRIPTION</span></span>
<span data-ttu-id="bb9b3-106">**Set-AzureRmLocalNetworkGateway** cmdlet은 로컬 네트워크 게이트웨이를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb9b3-106">The **Set-AzureRmLocalNetworkGateway** cmdlet modifies a local network gateway.</span></span>

## <span data-ttu-id="bb9b3-107">예제의</span><span class="sxs-lookup"><span data-stu-id="bb9b3-107">EXAMPLES</span></span>

### <span data-ttu-id="bb9b3-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="bb9b3-108">Example 1</span></span>
<span data-ttu-id="bb9b3-109">기존 게이트웨이에 대 한 구성 설정</span><span class="sxs-lookup"><span data-stu-id="bb9b3-109">Set configuration for an existing gateway</span></span>


```
$lgw = Get-AzureRmLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG
Set-AzureRmLocalNetworkGateway -LocalNetworkGateway $lgw

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

## <span data-ttu-id="bb9b3-110">변수</span><span class="sxs-lookup"><span data-stu-id="bb9b3-110">PARAMETERS</span></span>

### <span data-ttu-id="bb9b3-111">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="bb9b3-111">-AddressPrefix</span></span>
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

### <span data-ttu-id="bb9b3-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bb9b3-112">-AsJob</span></span>
<span data-ttu-id="bb9b3-113">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="bb9b3-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bb9b3-114">-Asn</span><span class="sxs-lookup"><span data-stu-id="bb9b3-114">-Asn</span></span>
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

### <span data-ttu-id="bb9b3-115">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="bb9b3-115">-BgpPeeringAddress</span></span>
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

### <span data-ttu-id="bb9b3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb9b3-116">-DefaultProfile</span></span>
<span data-ttu-id="bb9b3-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bb9b3-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bb9b3-118">-LocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="bb9b3-118">-LocalNetworkGateway</span></span>
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

### <span data-ttu-id="bb9b3-119">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="bb9b3-119">-PeerWeight</span></span>
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

### <span data-ttu-id="bb9b3-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb9b3-120">CommonParameters</span></span>
<span data-ttu-id="bb9b3-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb9b3-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb9b3-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb9b3-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb9b3-123">입력</span><span class="sxs-lookup"><span data-stu-id="bb9b3-123">INPUTS</span></span>

### <span data-ttu-id="bb9b3-124">Microsoft. 네트워크. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="bb9b3-124">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>
<span data-ttu-id="bb9b3-125">매개 변수: LocalNetworkGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="bb9b3-125">Parameters: LocalNetworkGateway (ByValue)</span></span>

### <span data-ttu-id="bb9b3-126">System.webserver. List ' 1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="bb9b3-126">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="bb9b3-127">시스템. UInt32</span><span class="sxs-lookup"><span data-stu-id="bb9b3-127">System.UInt32</span></span>

### <span data-ttu-id="bb9b3-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="bb9b3-128">System.String</span></span>

### <span data-ttu-id="bb9b3-129">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="bb9b3-129">System.Int32</span></span>

## <span data-ttu-id="bb9b3-130">출력</span><span class="sxs-lookup"><span data-stu-id="bb9b3-130">OUTPUTS</span></span>

### <span data-ttu-id="bb9b3-131">Microsoft. 네트워크. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="bb9b3-131">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="bb9b3-132">상속자</span><span class="sxs-lookup"><span data-stu-id="bb9b3-132">NOTES</span></span>

## <span data-ttu-id="bb9b3-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bb9b3-133">RELATED LINKS</span></span>

[<span data-ttu-id="bb9b3-134">Get-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="bb9b3-134">Get-AzureRmLocalNetworkGateway</span></span>](./Get-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="bb9b3-135">새로운 AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="bb9b3-135">New-AzureRmLocalNetworkGateway</span></span>](./New-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="bb9b3-136">제거-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="bb9b3-136">Remove-AzureRmLocalNetworkGateway</span></span>](./Remove-AzureRmLocalNetworkGateway.md)


