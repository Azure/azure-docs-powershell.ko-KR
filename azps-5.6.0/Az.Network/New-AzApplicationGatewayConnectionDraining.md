---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: b5bfedea118aa3770bac3141d05db379a4655906
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006219"
---
# <span data-ttu-id="015aa-101">New-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="015aa-101">New-AzApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="015aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="015aa-102">SYNOPSIS</span></span>
<span data-ttu-id="015aa-103">백 엔드 HTTP 설정에 대한 새 연결 드레인 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="015aa-103">Creates a new connection draining configuration for back-end HTTP settings.</span></span>

## <span data-ttu-id="015aa-104">구문</span><span class="sxs-lookup"><span data-stu-id="015aa-104">SYNTAX</span></span>

```
New-AzApplicationGatewayConnectionDraining -Enabled <Boolean> -DrainTimeoutInSec <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="015aa-105">설명</span><span class="sxs-lookup"><span data-stu-id="015aa-105">DESCRIPTION</span></span>
<span data-ttu-id="015aa-106">**New-AzApplicationGatewayConnectionDraining** cmdlet은 백 엔드 HTTP 설정에 대한 새 연결 드레인 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="015aa-106">The **New-AzApplicationGatewayConnectionDraining** cmdlet creates a new connection draining configuration for back-end HTTP settings.</span></span>

## <span data-ttu-id="015aa-107">예제</span><span class="sxs-lookup"><span data-stu-id="015aa-107">EXAMPLES</span></span>

### <span data-ttu-id="015aa-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="015aa-108">Example 1</span></span>
```
PS C:\> $connectionDraining = New-AzApplicationGatewayConnectionDraining -Enabled $True -DrainTimeoutInSec 42
```

<span data-ttu-id="015aa-109">이 명령은 True 및 DrainTimeoutInSec로 설정된 새 연결 드레인 구성을 42초로 설정하고 새 연결 드레인 구성을 $connectionDraining.</span><span class="sxs-lookup"><span data-stu-id="015aa-109">The command creates a new connection draining configuration with Enabled set to True and DrainTimeoutInSec set to 42 seconds and stores it in $connectionDraining.</span></span>

## <span data-ttu-id="015aa-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="015aa-110">PARAMETERS</span></span>

### <span data-ttu-id="015aa-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="015aa-111">-DefaultProfile</span></span>
<span data-ttu-id="015aa-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="015aa-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="015aa-113">-DrainTimeoutInSec</span><span class="sxs-lookup"><span data-stu-id="015aa-113">-DrainTimeoutInSec</span></span>
<span data-ttu-id="015aa-114">연결 드레인이 활성 상태인 초 수입니다.</span><span class="sxs-lookup"><span data-stu-id="015aa-114">The number of seconds connection draining is active.</span></span>
<span data-ttu-id="015aa-115">허용되는 값은 1초에서 3600초까지입니다.</span><span class="sxs-lookup"><span data-stu-id="015aa-115">Acceptable values are from 1 second to 3600 seconds.</span></span>

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

### <span data-ttu-id="015aa-116">-사용하도록 설정</span><span class="sxs-lookup"><span data-stu-id="015aa-116">-Enabled</span></span>
<span data-ttu-id="015aa-117">연결 드레인을 사용하도록 설정하는지 여부를 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="015aa-117">Whether connection draining is enabled or not.</span></span>

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

### <span data-ttu-id="015aa-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="015aa-118">CommonParameters</span></span>
<span data-ttu-id="015aa-119">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="015aa-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="015aa-120">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="015aa-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="015aa-121">입력</span><span class="sxs-lookup"><span data-stu-id="015aa-121">INPUTS</span></span>

### <span data-ttu-id="015aa-122">없음</span><span class="sxs-lookup"><span data-stu-id="015aa-122">None</span></span>

## <span data-ttu-id="015aa-123">출력</span><span class="sxs-lookup"><span data-stu-id="015aa-123">OUTPUTS</span></span>

### <span data-ttu-id="015aa-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="015aa-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="015aa-125">참고 사항</span><span class="sxs-lookup"><span data-stu-id="015aa-125">NOTES</span></span>

## <span data-ttu-id="015aa-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="015aa-126">RELATED LINKS</span></span>

[<span data-ttu-id="015aa-127">Get-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="015aa-127">Get-AzApplicationGatewayConnectionDraining</span></span>](./Get-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="015aa-128">Remove-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="015aa-128">Remove-AzApplicationGatewayConnectionDraining</span></span>](./Remove-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="015aa-129">Set-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="015aa-129">Set-AzApplicationGatewayConnectionDraining</span></span>](./Set-AzApplicationGatewayConnectionDraining.md)

