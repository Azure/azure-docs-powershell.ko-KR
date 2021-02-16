---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: ec20d7caafe110f03e5a0ce3130247ec877d6af9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179892"
---
# <span data-ttu-id="3e36d-101">Get-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="3e36d-101">Get-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="3e36d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e36d-102">SYNOPSIS</span></span>
<span data-ttu-id="3e36d-103">Application Gateway에서 기존 상태 프로브 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="3e36d-103">Gets an existing health probe configuration from an Application Gateway.</span></span>

## <span data-ttu-id="3e36d-104">구문</span><span class="sxs-lookup"><span data-stu-id="3e36d-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayProbeConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3e36d-105">설명</span><span class="sxs-lookup"><span data-stu-id="3e36d-105">DESCRIPTION</span></span>
<span data-ttu-id="3e36d-106">Get-AzApplicationGatewayProbeConfig cmdlet은 Application Gateway에서 기존 상태 프로브 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="3e36d-106">The Get-AzApplicationGatewayProbeConfig cmdlet gets an existing health probe configuration from an Application Gateway.</span></span>

## <span data-ttu-id="3e36d-107">예제</span><span class="sxs-lookup"><span data-stu-id="3e36d-107">EXAMPLES</span></span>

### <span data-ttu-id="3e36d-108">예제 1: 애플리케이션 게이트웨이에서 기존 프로브를 얻다</span><span class="sxs-lookup"><span data-stu-id="3e36d-108">Example 1: Get an existing probe from an application gateway</span></span>
```
PS C:\>Get-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe02"
```

<span data-ttu-id="3e36d-109">이 명령은 게이트웨이라는 애플리케이션 게이트웨이에서 Probe02라는 상태 프로브를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="3e36d-109">This command gets the health probe named Probe02 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="3e36d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3e36d-110">PARAMETERS</span></span>

### <span data-ttu-id="3e36d-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3e36d-111">-ApplicationGateway</span></span>
<span data-ttu-id="3e36d-112">이 cmdlet이 프로브 구성을 받을 애플리케이션 게이트웨이를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3e36d-112">Specifies the application gateway to which this cmdlet gets a probe configuration.</span></span>

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

### <span data-ttu-id="3e36d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e36d-113">-DefaultProfile</span></span>
<span data-ttu-id="3e36d-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3e36d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3e36d-115">-Name</span><span class="sxs-lookup"><span data-stu-id="3e36d-115">-Name</span></span>
<span data-ttu-id="3e36d-116">프로브의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3e36d-116">Specifies the name of the probe.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e36d-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e36d-117">CommonParameters</span></span>
<span data-ttu-id="3e36d-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3e36d-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e36d-119">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3e36d-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e36d-120">입력</span><span class="sxs-lookup"><span data-stu-id="3e36d-120">INPUTS</span></span>

### <span data-ttu-id="3e36d-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3e36d-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3e36d-122">출력</span><span class="sxs-lookup"><span data-stu-id="3e36d-122">OUTPUTS</span></span>

### <span data-ttu-id="3e36d-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe</span><span class="sxs-lookup"><span data-stu-id="3e36d-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe</span></span>

## <span data-ttu-id="3e36d-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3e36d-124">NOTES</span></span>

## <span data-ttu-id="3e36d-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3e36d-125">RELATED LINKS</span></span>

[<span data-ttu-id="3e36d-126">기존 애플리케이션 게이트웨이에 프로브 추가</span><span class="sxs-lookup"><span data-stu-id="3e36d-126">Add a probe to an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway)

[<span data-ttu-id="3e36d-127">Add-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="3e36d-127">Add-AzApplicationGatewayProbeConfig</span></span>](./Add-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="3e36d-128">New-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="3e36d-128">New-AzApplicationGatewayProbeConfig</span></span>](./New-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="3e36d-129">Remove-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="3e36d-129">Remove-AzApplicationGatewayProbeConfig</span></span>](./Remove-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="3e36d-130">Set-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="3e36d-130">Set-AzApplicationGatewayProbeConfig</span></span>](./Set-AzApplicationGatewayProbeConfig.md)

