---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: f9be647a4c6cb9d5198edcc766a20b3588e7626b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527871"
---
# <span data-ttu-id="7eb6d-101">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="7eb6d-101">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="7eb6d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7eb6d-102">SYNOPSIS</span></span>
<span data-ttu-id="7eb6d-103">Application Gateway의 자동 크기 조정 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7eb6d-103">Gets the Autoscale Configuration of the Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7eb6d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7eb6d-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayAutoscaleConfiguration -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7eb6d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="7eb6d-105">DESCRIPTION</span></span>
<span data-ttu-id="7eb6d-106">**AzureRmApplicationGatewayAutoscaleConfiguration** Cmdlet은 Application Gateway의 자동 크기 조정 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7eb6d-106">The **Get-AzureRmApplicationGatewayAutoscaleConfiguration** cmdlet gets Autoscale Configuration of the Application Gateway.</span></span>

## <span data-ttu-id="7eb6d-107">예제의</span><span class="sxs-lookup"><span data-stu-id="7eb6d-107">EXAMPLES</span></span>

### <span data-ttu-id="7eb6d-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="7eb6d-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzureRmApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $autoscaleConfiguration = Get-AzureRmApplicationGatewayAutoscaleConfiguration -ApplicationGateway $gw
PS C:\> $autoscaleConfiguration.MinCapacity
```

<span data-ttu-id="7eb6d-109">첫 번째 명령은 응용 프로그램 게이트웨이를 가져와 $gw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="7eb6d-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="7eb6d-110">두 번째 명령은 applicationg 게이트웨이에서 자동 크기 조정 구성을 추출 합니다.</span><span class="sxs-lookup"><span data-stu-id="7eb6d-110">The second command extracts out the autoscale configuration from the applicationg gateway.</span></span>

## <span data-ttu-id="7eb6d-111">변수</span><span class="sxs-lookup"><span data-stu-id="7eb6d-111">PARAMETERS</span></span>

### <span data-ttu-id="7eb6d-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7eb6d-112">-ApplicationGateway</span></span>
<span data-ttu-id="7eb6d-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7eb6d-113">The applicationGateway</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7eb6d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7eb6d-114">-DefaultProfile</span></span>
<span data-ttu-id="7eb6d-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7eb6d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7eb6d-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7eb6d-116">CommonParameters</span></span>
<span data-ttu-id="7eb6d-117">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7eb6d-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7eb6d-118">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7eb6d-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7eb6d-119">입력</span><span class="sxs-lookup"><span data-stu-id="7eb6d-119">INPUTS</span></span>

### <span data-ttu-id="7eb6d-120">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7eb6d-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7eb6d-121">출력</span><span class="sxs-lookup"><span data-stu-id="7eb6d-121">OUTPUTS</span></span>

### <span data-ttu-id="7eb6d-122">PSApplicationGatewayAutoscaleConfiguration에 대 한.</span><span class="sxs-lookup"><span data-stu-id="7eb6d-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="7eb6d-123">상속자</span><span class="sxs-lookup"><span data-stu-id="7eb6d-123">NOTES</span></span>

## <span data-ttu-id="7eb6d-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7eb6d-124">RELATED LINKS</span></span>
