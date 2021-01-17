---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: 679a1311526f7fa5028c83e6571001d14b2ff3f5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98339998"
---
# <span data-ttu-id="7a90c-101">New-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="7a90c-101">New-AzApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="7a90c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a90c-102">SYNOPSIS</span></span>
<span data-ttu-id="7a90c-103">백 엔드 HTTP 설정에 대한 새 연결 드레인 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7a90c-103">Creates a new connection draining configuration for back-end HTTP settings.</span></span>

## <span data-ttu-id="7a90c-104">구문</span><span class="sxs-lookup"><span data-stu-id="7a90c-104">SYNTAX</span></span>

```
New-AzApplicationGatewayConnectionDraining -Enabled <Boolean> -DrainTimeoutInSec <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7a90c-105">설명</span><span class="sxs-lookup"><span data-stu-id="7a90c-105">DESCRIPTION</span></span>
<span data-ttu-id="7a90c-106">**New-AzApplicationGatewayConnectionDraining** cmdlet은 백 엔드 HTTP 설정에 대한 새 연결 드레이팅 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7a90c-106">The **New-AzApplicationGatewayConnectionDraining** cmdlet creates a new connection draining configuration for back-end HTTP settings.</span></span>

## <span data-ttu-id="7a90c-107">예제</span><span class="sxs-lookup"><span data-stu-id="7a90c-107">EXAMPLES</span></span>

### <span data-ttu-id="7a90c-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="7a90c-108">Example 1</span></span>
```
PS C:\> $connectionDraining = New-AzApplicationGatewayConnectionDraining -Enabled $True -DrainTimeoutInSec 42
```

<span data-ttu-id="7a90c-109">이 명령은 Enabled를 True로 설정하고 DrainTimeoutInSec을 42초로 설정하여 새 연결 드레인 구성을 만들고 이 구성을 $connectionDraining.</span><span class="sxs-lookup"><span data-stu-id="7a90c-109">The command creates a new connection draining configuration with Enabled set to True and DrainTimeoutInSec set to 42 seconds and stores it in $connectionDraining.</span></span>

## <span data-ttu-id="7a90c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7a90c-110">PARAMETERS</span></span>

### <span data-ttu-id="7a90c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a90c-111">-DefaultProfile</span></span>
<span data-ttu-id="7a90c-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7a90c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7a90c-113">-DrainTimeoutInSec</span><span class="sxs-lookup"><span data-stu-id="7a90c-113">-DrainTimeoutInSec</span></span>
<span data-ttu-id="7a90c-114">연결 드레인이 활성 상태인 시간(초)입니다.</span><span class="sxs-lookup"><span data-stu-id="7a90c-114">The number of seconds connection draining is active.</span></span>
<span data-ttu-id="7a90c-115">허용되는 값은 1초에서 3600초까지입니다.</span><span class="sxs-lookup"><span data-stu-id="7a90c-115">Acceptable values are from 1 second to 3600 seconds.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a90c-116">-Enabled</span><span class="sxs-lookup"><span data-stu-id="7a90c-116">-Enabled</span></span>
<span data-ttu-id="7a90c-117">연결 드레인을 사용하도록 설정하는지 여부입니다.</span><span class="sxs-lookup"><span data-stu-id="7a90c-117">Whether connection draining is enabled or not.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a90c-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a90c-118">CommonParameters</span></span>
<span data-ttu-id="7a90c-119">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7a90c-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a90c-120">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="7a90c-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a90c-121">입력</span><span class="sxs-lookup"><span data-stu-id="7a90c-121">INPUTS</span></span>

### <span data-ttu-id="7a90c-122">없음</span><span class="sxs-lookup"><span data-stu-id="7a90c-122">None</span></span>

## <span data-ttu-id="7a90c-123">출력</span><span class="sxs-lookup"><span data-stu-id="7a90c-123">OUTPUTS</span></span>

### <span data-ttu-id="7a90c-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="7a90c-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="7a90c-125">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7a90c-125">NOTES</span></span>

## <span data-ttu-id="7a90c-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7a90c-126">RELATED LINKS</span></span>

[<span data-ttu-id="7a90c-127">Get-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="7a90c-127">Get-AzApplicationGatewayConnectionDraining</span></span>](./Get-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="7a90c-128">Remove-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="7a90c-128">Remove-AzApplicationGatewayConnectionDraining</span></span>](./Remove-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="7a90c-129">Set-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="7a90c-129">Set-AzApplicationGatewayConnectionDraining</span></span>](./Set-AzApplicationGatewayConnectionDraining.md)

