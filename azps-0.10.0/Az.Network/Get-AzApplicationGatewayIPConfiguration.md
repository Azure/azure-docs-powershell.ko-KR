---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 35562212-283C-4BB2-8B12-C3617A6760D0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: c7912f1a5d0539a0c81aff930cd94cb944e45bb7
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875625"
---
# <span data-ttu-id="dc415-101">Get-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="dc415-101">Get-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="dc415-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc415-102">SYNOPSIS</span></span>
<span data-ttu-id="dc415-103">응용 프로그램 게이트웨이의 IP 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dc415-103">Gets the IP configuration of an application gateway.</span></span>

## <span data-ttu-id="dc415-104">구문과</span><span class="sxs-lookup"><span data-stu-id="dc415-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayIPConfiguration [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dc415-105">설명은</span><span class="sxs-lookup"><span data-stu-id="dc415-105">DESCRIPTION</span></span>
<span data-ttu-id="dc415-106">**Get-AzApplicationGatewayIPConfiguration** cmdlet은 응용 프로그램 게이트웨이의 IP 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dc415-106">The **Get-AzApplicationGatewayIPConfiguration** cmdlet gets the IP configuration of an application gateway.</span></span>
<span data-ttu-id="dc415-107">IP 구성에는 응용 프로그램 게이트웨이가 배포 된 서브넷이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="dc415-107">The IP configuration contains the subnet in which the application gateway is deployed.</span></span>

## <span data-ttu-id="dc415-108">예제의</span><span class="sxs-lookup"><span data-stu-id="dc415-108">EXAMPLES</span></span>

### <span data-ttu-id="dc415-109">예제 1: 특정 IP 구성 가져오기</span><span class="sxs-lookup"><span data-stu-id="dc415-109">Example 1: Get a specific IP configuration</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $GatewaySubnet = Get-AzApplicationGatewayIPConfiguration -Name "GatewaySubnet01" -ApplicationGateway $AppGw
```

<span data-ttu-id="dc415-110">첫 번째 명령은 응용 프로그램 게이트웨이를 가져와 $AppGw 변수에 저장 합니다. 두 번째 명령은 $AppGw에 저장 된 게이트웨이에서 GateSubnet01 이라는 IP 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dc415-110">The first command gets an application gateway and stores it in the $AppGw variable.The second command gets an IP configuration named GateSubnet01 from the gateway stored in $AppGw.</span></span>

### <span data-ttu-id="dc415-111">예제 2: IP 구성 목록 가져오기</span><span class="sxs-lookup"><span data-stu-id="dc415-111">Example 2: Get a list of IP configurations</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $GatewaySubnets = Get-AzApplicationGatewayIPConfiguration -ApplicationGateway $AppGw
```

<span data-ttu-id="dc415-112">첫 번째 명령은 응용 프로그램 게이트웨이를 가져와 $AppGw 변수에 저장 합니다. 두 번째 명령은 모든 IP 구성 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dc415-112">The first command gets an application gateway and stores it in the $AppGw variable.The second command gets a list of all IP configurations.</span></span>

## <span data-ttu-id="dc415-113">변수</span><span class="sxs-lookup"><span data-stu-id="dc415-113">PARAMETERS</span></span>

### <span data-ttu-id="dc415-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="dc415-114">-ApplicationGateway</span></span>
<span data-ttu-id="dc415-115">IP 구성을 포함 하는 응용 프로그램 게이트웨이 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc415-115">Specifies the application gateway object that contains IP configuration.</span></span>

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

### <span data-ttu-id="dc415-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc415-116">-DefaultProfile</span></span>
<span data-ttu-id="dc415-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="dc415-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dc415-118">-이름</span><span class="sxs-lookup"><span data-stu-id="dc415-118">-Name</span></span>
<span data-ttu-id="dc415-119">이 cmdlet이 가져오는 IP 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc415-119">Specifies the name of the IP configuration which this cmdlet gets.</span></span>

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

### <span data-ttu-id="dc415-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc415-120">CommonParameters</span></span>
<span data-ttu-id="dc415-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc415-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc415-122">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc415-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc415-123">입력</span><span class="sxs-lookup"><span data-stu-id="dc415-123">INPUTS</span></span>

### <span data-ttu-id="dc415-124">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="dc415-124">System.String</span></span>

## <span data-ttu-id="dc415-125">출력</span><span class="sxs-lookup"><span data-stu-id="dc415-125">OUTPUTS</span></span>

### <span data-ttu-id="dc415-126">Microsoft. \*. m i m. 모델. m m m m i m a.</span><span class="sxs-lookup"><span data-stu-id="dc415-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="dc415-127">상속자</span><span class="sxs-lookup"><span data-stu-id="dc415-127">NOTES</span></span>

## <span data-ttu-id="dc415-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dc415-128">RELATED LINKS</span></span>

[<span data-ttu-id="dc415-129">추가-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="dc415-129">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="dc415-130">새로운 AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="dc415-130">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="dc415-131">제거-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="dc415-131">Remove-AzApplicationGatewayIPConfiguration</span></span>](./Remove-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="dc415-132">Set-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="dc415-132">Set-AzApplicationGatewayIPConfiguration</span></span>](./Set-AzApplicationGatewayIPConfiguration.md)


