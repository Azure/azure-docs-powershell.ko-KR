---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: 679a1311526f7fa5028c83e6571001d14b2ff3f5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214398"
---
# <span data-ttu-id="34672-101">New-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="34672-101">New-AzApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="34672-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34672-102">SYNOPSIS</span></span>
<span data-ttu-id="34672-103">백 엔드 HTTP 설정에 대 한 새 연결 드레이닝 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="34672-103">Creates a new connection draining configuration for back-end HTTP settings.</span></span>

## <span data-ttu-id="34672-104">구문과</span><span class="sxs-lookup"><span data-stu-id="34672-104">SYNTAX</span></span>

```
New-AzApplicationGatewayConnectionDraining -Enabled <Boolean> -DrainTimeoutInSec <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="34672-105">설명은</span><span class="sxs-lookup"><span data-stu-id="34672-105">DESCRIPTION</span></span>
<span data-ttu-id="34672-106">**새 AzApplicationGatewayConnectionDraining** cmdlet은 백 엔드 HTTP 설정에 대 한 새 연결 드레이닝 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="34672-106">The **New-AzApplicationGatewayConnectionDraining** cmdlet creates a new connection draining configuration for back-end HTTP settings.</span></span>

## <span data-ttu-id="34672-107">예제의</span><span class="sxs-lookup"><span data-stu-id="34672-107">EXAMPLES</span></span>

### <span data-ttu-id="34672-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="34672-108">Example 1</span></span>
```
PS C:\> $connectionDraining = New-AzApplicationGatewayConnectionDraining -Enabled $True -DrainTimeoutInSec 42
```

<span data-ttu-id="34672-109">이 명령은 Enabled가 True로 설정 된 새 연결 드레이닝 구성을 만들고 DrainTimeoutInSec를 42 초로 설정 하 고이를 $connectionDraining에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="34672-109">The command creates a new connection draining configuration with Enabled set to True and DrainTimeoutInSec set to 42 seconds and stores it in $connectionDraining.</span></span>

## <span data-ttu-id="34672-110">변수</span><span class="sxs-lookup"><span data-stu-id="34672-110">PARAMETERS</span></span>

### <span data-ttu-id="34672-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34672-111">-DefaultProfile</span></span>
<span data-ttu-id="34672-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="34672-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="34672-113">-DrainTimeoutInSec</span><span class="sxs-lookup"><span data-stu-id="34672-113">-DrainTimeoutInSec</span></span>
<span data-ttu-id="34672-114">연결 드레이닝이 활성 상태인 시간 (초)입니다.</span><span class="sxs-lookup"><span data-stu-id="34672-114">The number of seconds connection draining is active.</span></span>
<span data-ttu-id="34672-115">허용 되는 값은 1 초에서 3600 초 사이입니다.</span><span class="sxs-lookup"><span data-stu-id="34672-115">Acceptable values are from 1 second to 3600 seconds.</span></span>

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

### <span data-ttu-id="34672-116">-사용</span><span class="sxs-lookup"><span data-stu-id="34672-116">-Enabled</span></span>
<span data-ttu-id="34672-117">연결 드레이닝이 사용 되는지 여부입니다.</span><span class="sxs-lookup"><span data-stu-id="34672-117">Whether connection draining is enabled or not.</span></span>

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

### <span data-ttu-id="34672-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34672-118">CommonParameters</span></span>
<span data-ttu-id="34672-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="34672-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34672-120">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34672-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34672-121">입력</span><span class="sxs-lookup"><span data-stu-id="34672-121">INPUTS</span></span>

### <span data-ttu-id="34672-122">않아야</span><span class="sxs-lookup"><span data-stu-id="34672-122">None</span></span>

## <span data-ttu-id="34672-123">출력</span><span class="sxs-lookup"><span data-stu-id="34672-123">OUTPUTS</span></span>

### <span data-ttu-id="34672-124">Microsoft. 네트워크 모델. Psapplication게이트웨이 Connection드레이닝</span><span class="sxs-lookup"><span data-stu-id="34672-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="34672-125">상속자</span><span class="sxs-lookup"><span data-stu-id="34672-125">NOTES</span></span>

## <span data-ttu-id="34672-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="34672-126">RELATED LINKS</span></span>

[<span data-ttu-id="34672-127">Get-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="34672-127">Get-AzApplicationGatewayConnectionDraining</span></span>](./Get-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="34672-128">제거-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="34672-128">Remove-AzApplicationGatewayConnectionDraining</span></span>](./Remove-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="34672-129">Set-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="34672-129">Set-AzApplicationGatewayConnectionDraining</span></span>](./Set-AzApplicationGatewayConnectionDraining.md)

