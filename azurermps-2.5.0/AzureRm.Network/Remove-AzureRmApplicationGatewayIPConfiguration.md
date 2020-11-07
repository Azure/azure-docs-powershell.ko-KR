---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6943BB5C-D709-4A80-AF5E-DC9501C20680
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayipconfiguration
schema: 2.0.0
ms.openlocfilehash: 901d8209cc18a5d64285bf45f7169d55d3c7a41e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882598"
---
# <span data-ttu-id="28486-101">Remove-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="28486-101">Remove-AzureRmApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="28486-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="28486-102">SYNOPSIS</span></span>
<span data-ttu-id="28486-103">응용 프로그램 게이트웨이에서 IP 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="28486-103">Removes an IP configuration from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="28486-104">구문과</span><span class="sxs-lookup"><span data-stu-id="28486-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayIPConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="28486-105">설명은</span><span class="sxs-lookup"><span data-stu-id="28486-105">DESCRIPTION</span></span>
<span data-ttu-id="28486-106">**AzureRmApplicationGatewayIPConfiguration** Cmdlet은 Azure 응용 프로그램 게이트웨이에서 IP 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="28486-106">The **Remove-AzureRmApplicationGatewayIPConfiguration** cmdlet removes an IP configuration from an Azure application gateway.</span></span>

## <span data-ttu-id="28486-107">예제의</span><span class="sxs-lookup"><span data-stu-id="28486-107">EXAMPLES</span></span>

### <span data-ttu-id="28486-108">예제 1: Azure 응용 프로그램 게이트웨이에서 IP 구성 제거</span><span class="sxs-lookup"><span data-stu-id="28486-108">Example 1: Remove an IP configuration from an Azure application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "Subnet02"
```

<span data-ttu-id="28486-109">첫 번째 명령은 응용 프로그램 게이트웨이를 가져와 $AppGw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="28486-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="28486-110">두 번째 명령은 $AppGw에 저장 된 응용 프로그램 게이트웨이에서 Subnet02 이라는 IP 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="28486-110">The second command removes the IP configuration named Subnet02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="28486-111">변수</span><span class="sxs-lookup"><span data-stu-id="28486-111">PARAMETERS</span></span>

### <span data-ttu-id="28486-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="28486-112">-ApplicationGateway</span></span>
<span data-ttu-id="28486-113">IP 구성을 제거할 응용 프로그램 게이트웨이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="28486-113">Specifies the application gateway from which to remove an IP configuration.</span></span>

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

### <span data-ttu-id="28486-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28486-114">-DefaultProfile</span></span>
<span data-ttu-id="28486-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="28486-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="28486-116">-이름</span><span class="sxs-lookup"><span data-stu-id="28486-116">-Name</span></span>
<span data-ttu-id="28486-117">제거할 IP 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="28486-117">Specifies the name of the IP configuration to remove.</span></span>

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

### <span data-ttu-id="28486-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28486-118">CommonParameters</span></span>
<span data-ttu-id="28486-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="28486-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28486-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28486-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28486-121">입력</span><span class="sxs-lookup"><span data-stu-id="28486-121">INPUTS</span></span>

### <span data-ttu-id="28486-122">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="28486-122">System.String</span></span>

## <span data-ttu-id="28486-123">출력</span><span class="sxs-lookup"><span data-stu-id="28486-123">OUTPUTS</span></span>

### <span data-ttu-id="28486-124">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="28486-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="28486-125">상속자</span><span class="sxs-lookup"><span data-stu-id="28486-125">NOTES</span></span>

## <span data-ttu-id="28486-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="28486-126">RELATED LINKS</span></span>

[<span data-ttu-id="28486-127">추가-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="28486-127">Add-AzureRmApplicationGatewayIPConfiguration</span></span>](./Add-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="28486-128">Get-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="28486-128">Get-AzureRmApplicationGatewayIPConfiguration</span></span>](./Get-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="28486-129">새로운 AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="28486-129">New-AzureRmApplicationGatewayIPConfiguration</span></span>](./New-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="28486-130">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="28486-130">Set-AzureRmApplicationGatewayIPConfiguration</span></span>](./Set-AzureRmApplicationGatewayIPConfiguration.md)


