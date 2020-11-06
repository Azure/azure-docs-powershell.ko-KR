---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 35562212-283C-4BB2-8B12-C3617A6760D0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 3ebe90d5f28adf0e7e4a9de66b04a1ea000cc69e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530464"
---
# <span data-ttu-id="82c2f-101">Get-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="82c2f-101">Get-AzureRmApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="82c2f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82c2f-102">SYNOPSIS</span></span>
<span data-ttu-id="82c2f-103">응용 프로그램 게이트웨이의 IP 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="82c2f-103">Gets the IP configuration of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="82c2f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="82c2f-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayIPConfiguration [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="82c2f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="82c2f-105">DESCRIPTION</span></span>
<span data-ttu-id="82c2f-106">**Get-AzureRmApplicationGatewayIPConfiguration** cmdlet은 응용 프로그램 게이트웨이의 IP 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="82c2f-106">The **Get-AzureRmApplicationGatewayIPConfiguration** cmdlet gets the IP configuration of an application gateway.</span></span>
<span data-ttu-id="82c2f-107">IP 구성에는 응용 프로그램 게이트웨이가 배포 된 서브넷이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="82c2f-107">The IP configuration contains the subnet in which the application gateway is deployed.</span></span>

## <span data-ttu-id="82c2f-108">예제의</span><span class="sxs-lookup"><span data-stu-id="82c2f-108">EXAMPLES</span></span>

### <span data-ttu-id="82c2f-109">예제 1: 특정 IP 구성 가져오기</span><span class="sxs-lookup"><span data-stu-id="82c2f-109">Example 1: Get a specific IP configuration</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $GatewaySubnet = Get-AzureRmApplicationGatewayIPConfiguration -Name "GatewaySubnet01" -ApplicationGateway $AppGw
```

<span data-ttu-id="82c2f-110">첫 번째 명령은 응용 프로그램 게이트웨이를 가져와 $AppGw 변수에 저장 합니다. 두 번째 명령은 $AppGw에 저장 된 게이트웨이에서 GateSubnet01 이라는 IP 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="82c2f-110">The first command gets an application gateway and stores it in the $AppGw variable.The second command gets an IP configuration named GateSubnet01 from the gateway stored in $AppGw.</span></span>

### <span data-ttu-id="82c2f-111">예제 2: IP 구성 목록 가져오기</span><span class="sxs-lookup"><span data-stu-id="82c2f-111">Example 2: Get a list of IP configurations</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $GatewaySubnets = Get-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway $AppGw
```

<span data-ttu-id="82c2f-112">첫 번째 명령은 응용 프로그램 게이트웨이를 가져와 $AppGw 변수에 저장 합니다. 두 번째 명령은 모든 IP 구성 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="82c2f-112">The first command gets an application gateway and stores it in the $AppGw variable.The second command gets a list of all IP configurations.</span></span>

## <span data-ttu-id="82c2f-113">변수</span><span class="sxs-lookup"><span data-stu-id="82c2f-113">PARAMETERS</span></span>

### <span data-ttu-id="82c2f-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="82c2f-114">-ApplicationGateway</span></span>
<span data-ttu-id="82c2f-115">IP 구성을 포함 하는 응용 프로그램 게이트웨이 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="82c2f-115">Specifies the application gateway object that contains IP configuration.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="82c2f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82c2f-116">-DefaultProfile</span></span>
<span data-ttu-id="82c2f-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="82c2f-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="82c2f-118">-이름</span><span class="sxs-lookup"><span data-stu-id="82c2f-118">-Name</span></span>
<span data-ttu-id="82c2f-119">이 cmdlet이 가져오는 IP 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="82c2f-119">Specifies the name of the IP configuration which this cmdlet gets.</span></span>

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

### <span data-ttu-id="82c2f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82c2f-120">CommonParameters</span></span>
<span data-ttu-id="82c2f-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="82c2f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82c2f-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82c2f-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82c2f-123">입력</span><span class="sxs-lookup"><span data-stu-id="82c2f-123">INPUTS</span></span>

### <span data-ttu-id="82c2f-124">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="82c2f-124">System.String</span></span>

## <span data-ttu-id="82c2f-125">출력</span><span class="sxs-lookup"><span data-stu-id="82c2f-125">OUTPUTS</span></span>

### <span data-ttu-id="82c2f-126">Microsoft. \*. m i m. 모델. m m m m i m a.</span><span class="sxs-lookup"><span data-stu-id="82c2f-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="82c2f-127">상속자</span><span class="sxs-lookup"><span data-stu-id="82c2f-127">NOTES</span></span>

## <span data-ttu-id="82c2f-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="82c2f-128">RELATED LINKS</span></span>

[<span data-ttu-id="82c2f-129">추가-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="82c2f-129">Add-AzureRmApplicationGatewayIPConfiguration</span></span>](./Add-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="82c2f-130">새로운 AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="82c2f-130">New-AzureRmApplicationGatewayIPConfiguration</span></span>](./New-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="82c2f-131">제거-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="82c2f-131">Remove-AzureRmApplicationGatewayIPConfiguration</span></span>](./Remove-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="82c2f-132">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="82c2f-132">Set-AzureRmApplicationGatewayIPConfiguration</span></span>](./Set-AzureRmApplicationGatewayIPConfiguration.md)


