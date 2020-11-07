---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayconnectiondraining
schema: 2.0.0
ms.openlocfilehash: 6e17db790cd776e8662c4c445e53604dcb8929de
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93881393"
---
# <span data-ttu-id="205d8-101">New-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="205d8-101">New-AzureRmApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="205d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="205d8-102">SYNOPSIS</span></span>
<span data-ttu-id="205d8-103">백 엔드 HTTP 설정에 대 한 새 연결 드레이닝 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="205d8-103">Creates a new connection draining configuration for back-end HTTP settings.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="205d8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="205d8-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayConnectionDraining -Enabled <Boolean> -DrainTimeoutInSec <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="205d8-105">설명은</span><span class="sxs-lookup"><span data-stu-id="205d8-105">DESCRIPTION</span></span>
<span data-ttu-id="205d8-106">**새 AzureRmApplicationGatewayConnectionDraining** cmdlet은 백 엔드 HTTP 설정에 대 한 새 연결 드레이닝 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="205d8-106">The **New-AzureRmApplicationGatewayConnectionDraining** cmdlet creates a new connection draining configuration for back-end HTTP settings.</span></span>

## <span data-ttu-id="205d8-107">예제의</span><span class="sxs-lookup"><span data-stu-id="205d8-107">EXAMPLES</span></span>

### <span data-ttu-id="205d8-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="205d8-108">Example 1</span></span>
```
PS C:\> $connectionDraining = New-AzureRmApplicationGatewayConnectionDraining -Enabled $True -DrainTimeoutInSec 42
```

<span data-ttu-id="205d8-109">이 명령은 Enabled가 True로 설정 된 새 연결 드레이닝 구성을 만들고 DrainTimeoutInSec를 42 초로 설정 하 고이를 $connectionDraining에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="205d8-109">The command creates a new connection draining configuration with Enabled set to True and DrainTimeoutInSec set to 42 seconds and stores it in $connectionDraining.</span></span>

## <span data-ttu-id="205d8-110">변수</span><span class="sxs-lookup"><span data-stu-id="205d8-110">PARAMETERS</span></span>

### <span data-ttu-id="205d8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="205d8-111">-DefaultProfile</span></span>
<span data-ttu-id="205d8-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="205d8-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="205d8-113">-DrainTimeoutInSec</span><span class="sxs-lookup"><span data-stu-id="205d8-113">-DrainTimeoutInSec</span></span>
<span data-ttu-id="205d8-114">연결 드레이닝이 활성 상태인 시간 (초)입니다.</span><span class="sxs-lookup"><span data-stu-id="205d8-114">The number of seconds connection draining is active.</span></span>
<span data-ttu-id="205d8-115">허용 되는 값은 1 초에서 3600 초 사이입니다.</span><span class="sxs-lookup"><span data-stu-id="205d8-115">Acceptable values are from 1 second to 3600 seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="205d8-116">-사용</span><span class="sxs-lookup"><span data-stu-id="205d8-116">-Enabled</span></span>
<span data-ttu-id="205d8-117">연결 드레이닝이 사용 되는지 여부입니다.</span><span class="sxs-lookup"><span data-stu-id="205d8-117">Whether connection draining is enabled or not.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="205d8-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="205d8-118">CommonParameters</span></span>
<span data-ttu-id="205d8-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="205d8-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="205d8-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="205d8-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="205d8-121">입력</span><span class="sxs-lookup"><span data-stu-id="205d8-121">INPUTS</span></span>

### <span data-ttu-id="205d8-122">않아야</span><span class="sxs-lookup"><span data-stu-id="205d8-122">None</span></span>

## <span data-ttu-id="205d8-123">출력</span><span class="sxs-lookup"><span data-stu-id="205d8-123">OUTPUTS</span></span>

### <span data-ttu-id="205d8-124">Microsoft. 네트워크 모델. Psapplication게이트웨이 Connection드레이닝</span><span class="sxs-lookup"><span data-stu-id="205d8-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="205d8-125">상속자</span><span class="sxs-lookup"><span data-stu-id="205d8-125">NOTES</span></span>

## <span data-ttu-id="205d8-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="205d8-126">RELATED LINKS</span></span>

[<span data-ttu-id="205d8-127">Get-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="205d8-127">Get-AzureRmApplicationGatewayConnectionDraining</span></span>](./Get-AzureRmApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="205d8-128">제거-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="205d8-128">Remove-AzureRmApplicationGatewayConnectionDraining</span></span>](./Remove-AzureRmApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="205d8-129">Set-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="205d8-129">Set-AzureRmApplicationGatewayConnectionDraining</span></span>](./Set-AzureRmApplicationGatewayConnectionDraining.md)

