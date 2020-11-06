---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayProbeConfig.md
ms.openlocfilehash: 40a7e63150384ac3fa2c330c079d5377c836d52e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529496"
---
# <span data-ttu-id="7e767-101">Remove-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="7e767-101">Remove-AzureRmApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="7e767-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e767-102">SYNOPSIS</span></span>
<span data-ttu-id="7e767-103">기존 응용 프로그램 게이트웨이에서 상태 프로브를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e767-103">Removes a health probe from an existing application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7e767-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7e767-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayProbeConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7e767-105">설명은</span><span class="sxs-lookup"><span data-stu-id="7e767-105">DESCRIPTION</span></span>
<span data-ttu-id="7e767-106">Remove-AzureRmApplicationGatewayProbeConfig cmdlet은 기존 응용 프로그램 게이트웨이에서 heath probe를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e767-106">The Remove-AzureRmApplicationGatewayProbeConfig cmdlet removes a heath probe from an existing application gateway.</span></span>

## <span data-ttu-id="7e767-107">예제의</span><span class="sxs-lookup"><span data-stu-id="7e767-107">EXAMPLES</span></span>

### <span data-ttu-id="7e767-108">예제 1: 기존 응용 프로그램 게이트웨이에서 상태 프로브 제거</span><span class="sxs-lookup"><span data-stu-id="7e767-108">Example 1: Remove a health probe from an existing application gateway</span></span>
```
PS C:\>$Gateway = Remove-AzureRmApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe04"
```

<span data-ttu-id="7e767-109">이 명령은 Gateway 라는 응용 프로그램 게이트웨이에서 Probe04 이라는 상태 프로브를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e767-109">This command removes the health probe named Probe04 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="7e767-110">변수</span><span class="sxs-lookup"><span data-stu-id="7e767-110">PARAMETERS</span></span>

### <span data-ttu-id="7e767-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7e767-111">-ApplicationGateway</span></span>
<span data-ttu-id="7e767-112">이 cmdlet이 프로브를 제거 하는 응용 프로그램 게이트웨이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e767-112">Specifies the application gateway to which this cmdlet removes a probe.</span></span>

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

### <span data-ttu-id="7e767-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e767-113">-DefaultProfile</span></span>
<span data-ttu-id="7e767-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7e767-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7e767-115">-이름</span><span class="sxs-lookup"><span data-stu-id="7e767-115">-Name</span></span>
<span data-ttu-id="7e767-116">이 cmdlet이 제거할 프로브 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e767-116">Specifies the name of the probe for which this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e767-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e767-117">CommonParameters</span></span>
<span data-ttu-id="7e767-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e767-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e767-119">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e767-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e767-120">입력</span><span class="sxs-lookup"><span data-stu-id="7e767-120">INPUTS</span></span>

### <span data-ttu-id="7e767-121">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7e767-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="7e767-122">매개 변수: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7e767-122">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="7e767-123">출력</span><span class="sxs-lookup"><span data-stu-id="7e767-123">OUTPUTS</span></span>

### <span data-ttu-id="7e767-124">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7e767-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7e767-125">상속자</span><span class="sxs-lookup"><span data-stu-id="7e767-125">NOTES</span></span>

## <span data-ttu-id="7e767-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7e767-126">RELATED LINKS</span></span>

[<span data-ttu-id="7e767-127">기존 응용 프로그램 게이트웨이에서 프로브 제거</span><span class="sxs-lookup"><span data-stu-id="7e767-127">Remove a probe from an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#remove-a-probe-from-an-existing-application-gateway)

[<span data-ttu-id="7e767-128">추가-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="7e767-128">Add-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="7e767-129">Get-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="7e767-129">Get-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="7e767-130">새로운 AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="7e767-130">New-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="7e767-131">Set-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="7e767-131">Set-AzureRmApplicationGatewayProbeConfig</span></span>]()

