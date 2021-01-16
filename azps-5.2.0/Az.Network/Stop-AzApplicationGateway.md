---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2C9609E8-0D8B-471B-9F0E-672BF55C3A0E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzApplicationGateway.md
ms.openlocfilehash: 4c7001bf69e6dc8f418f1bc56867154bf9d769ce
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98363483"
---
# <span data-ttu-id="fec61-101">Stop-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fec61-101">Stop-AzApplicationGateway</span></span>

## <span data-ttu-id="fec61-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fec61-102">SYNOPSIS</span></span>
<span data-ttu-id="fec61-103">애플리케이션 게이트웨이를 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="fec61-103">Stops an application gateway</span></span>

## <span data-ttu-id="fec61-104">구문</span><span class="sxs-lookup"><span data-stu-id="fec61-104">SYNTAX</span></span>

```
Stop-AzApplicationGateway -ApplicationGateway <PSApplicationGateway> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fec61-105">설명</span><span class="sxs-lookup"><span data-stu-id="fec61-105">DESCRIPTION</span></span>
<span data-ttu-id="fec61-106">**Stop-AzApplicationGateway** cmdlet은 애플리케이션 게이트웨이를 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="fec61-106">The **Stop-AzApplicationGateway** cmdlet stops an application gateway.</span></span>

## <span data-ttu-id="fec61-107">예제</span><span class="sxs-lookup"><span data-stu-id="fec61-107">EXAMPLES</span></span>

### <span data-ttu-id="fec61-108">예제 1: 애플리케이션 게이트웨이 중지</span><span class="sxs-lookup"><span data-stu-id="fec61-108">Example 1: Stop an application gateway</span></span>
```
PS C:\>Stop-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="fec61-109">이 명령은 애플리케이션 변수에 저장된 애플리케이션 게이트웨이를 $AppGw 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="fec61-109">This command stops the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="fec61-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fec61-110">PARAMETERS</span></span>

### <span data-ttu-id="fec61-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fec61-111">-ApplicationGateway</span></span>
<span data-ttu-id="fec61-112">이 cmdlet이 중지하는 애플리케이션 게이트웨이를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fec61-112">Specifies the application gateway that this cmdlet stops.</span></span>

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

### <span data-ttu-id="fec61-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fec61-113">-AsJob</span></span>
<span data-ttu-id="fec61-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="fec61-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fec61-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fec61-115">-DefaultProfile</span></span>
<span data-ttu-id="fec61-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fec61-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fec61-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fec61-117">CommonParameters</span></span>
<span data-ttu-id="fec61-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="fec61-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fec61-119">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="fec61-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fec61-120">입력</span><span class="sxs-lookup"><span data-stu-id="fec61-120">INPUTS</span></span>

### <span data-ttu-id="fec61-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fec61-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="fec61-122">출력</span><span class="sxs-lookup"><span data-stu-id="fec61-122">OUTPUTS</span></span>

### <span data-ttu-id="fec61-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fec61-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="fec61-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="fec61-124">NOTES</span></span>

## <span data-ttu-id="fec61-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fec61-125">RELATED LINKS</span></span>

[<span data-ttu-id="fec61-126">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fec61-126">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="fec61-127">New-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fec61-127">New-AzApplicationGateway</span></span>](./New-AzApplicationGateway.md)

[<span data-ttu-id="fec61-128">Remove-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fec61-128">Remove-AzApplicationGateway</span></span>](./Remove-AzApplicationGateway.md)

[<span data-ttu-id="fec61-129">Set-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fec61-129">Set-AzApplicationGateway</span></span>](./Set-AzApplicationGateway.md)

[<span data-ttu-id="fec61-130">Start-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fec61-130">Start-AzApplicationGateway</span></span>](./Start-AzApplicationGateway.md)

