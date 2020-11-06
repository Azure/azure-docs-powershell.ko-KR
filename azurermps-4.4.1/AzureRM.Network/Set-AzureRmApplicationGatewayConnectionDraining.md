---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayConnectionDraining.md
ms.openlocfilehash: 9da0f53f6dbea616a1f1cbea7ef08e71b05df17b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537084"
---
# <span data-ttu-id="bc0de-101">Set-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="bc0de-101">Set-AzureRmApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="bc0de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc0de-102">SYNOPSIS</span></span>
<span data-ttu-id="bc0de-103">백 엔드 HTTP 설정 개체의 연결 드레이닝 구성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc0de-103">Modifies the connection draining configuration of a back-end HTTP settings object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bc0de-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bc0de-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayConnectionDraining -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 -Enabled <Boolean> -DrainTimeoutInSec <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bc0de-105">설명은</span><span class="sxs-lookup"><span data-stu-id="bc0de-105">DESCRIPTION</span></span>
<span data-ttu-id="bc0de-106">**Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** cmdlet은 백 엔드 HTTP 설정 개체의 연결 드레이닝 구성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc0de-106">The **Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** cmdlet modifies the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="bc0de-107">예제의</span><span class="sxs-lookup"><span data-stu-id="bc0de-107">EXAMPLES</span></span>

### <span data-ttu-id="bc0de-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="bc0de-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzureRmApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> Set-AzureRmApplicationGatewayConnectionDraining -BackendHttpSettings $poolSetting02 -Enabled $False -DrainTimeoutInSec 3600
```

<span data-ttu-id="bc0de-109">첫 번째 명령은 ResourceGroup01 이라는 리소스 그룹에서 ApplicationGateway01 라는 응용 프로그램 게이트웨이를 가져와이를 $AppGw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc0de-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="bc0de-110">두 번째 명령은 $AppGw에 대 한 Settings01 라는 백 엔드 HTTP 설정을 가져오고 $Settings 변수에 설정을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc0de-110">The second command gets the back-end HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>
<span data-ttu-id="bc0de-111">마지막 명령은 $Settings에 저장 된 백 엔드 HTTP 설정 개체의 연결 드레이닝 구성을 False로 설정 하 고 DrainTimeoutInSec를 3600로 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc0de-111">The last command modifies the connection draining configuration of the back-end HTTP settings object stored in $Settings by setting Enabled to False and DrainTimeoutInSec to 3600.</span></span>

## <span data-ttu-id="bc0de-112">변수</span><span class="sxs-lookup"><span data-stu-id="bc0de-112">PARAMETERS</span></span>

### <span data-ttu-id="bc0de-113">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="bc0de-113">-BackendHttpSettings</span></span>
<span data-ttu-id="bc0de-114">백 엔드 http 설정</span><span class="sxs-lookup"><span data-stu-id="bc0de-114">The backend http settings</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bc0de-115">-DrainTimeoutInSec</span><span class="sxs-lookup"><span data-stu-id="bc0de-115">-DrainTimeoutInSec</span></span>
<span data-ttu-id="bc0de-116">연결 드레이닝이 활성 상태인 시간 (초)입니다.</span><span class="sxs-lookup"><span data-stu-id="bc0de-116">The number of seconds connection draining is active.</span></span>
<span data-ttu-id="bc0de-117">허용 되는 값은 1 초에서 3600 초 사이입니다.</span><span class="sxs-lookup"><span data-stu-id="bc0de-117">Acceptable values are from 1 second to 3600 seconds.</span></span>

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

### <span data-ttu-id="bc0de-118">-사용</span><span class="sxs-lookup"><span data-stu-id="bc0de-118">-Enabled</span></span>
<span data-ttu-id="bc0de-119">연결 드레이닝이 사용 되는지 여부입니다.</span><span class="sxs-lookup"><span data-stu-id="bc0de-119">Whether connection draining is enabled or not.</span></span>

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

### <span data-ttu-id="bc0de-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc0de-120">-DefaultProfile</span></span>
<span data-ttu-id="bc0de-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bc0de-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bc0de-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc0de-122">CommonParameters</span></span>
<span data-ttu-id="bc0de-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc0de-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc0de-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc0de-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc0de-125">입력</span><span class="sxs-lookup"><span data-stu-id="bc0de-125">INPUTS</span></span>

### <span data-ttu-id="bc0de-126">PSApplicationGatewayBackendHttpSettings에 대 한.</span><span class="sxs-lookup"><span data-stu-id="bc0de-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="bc0de-127">출력</span><span class="sxs-lookup"><span data-stu-id="bc0de-127">OUTPUTS</span></span>

### <span data-ttu-id="bc0de-128">PSApplicationGatewayBackendHttpSettings에 대 한.</span><span class="sxs-lookup"><span data-stu-id="bc0de-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="bc0de-129">상속자</span><span class="sxs-lookup"><span data-stu-id="bc0de-129">NOTES</span></span>

## <span data-ttu-id="bc0de-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bc0de-130">RELATED LINKS</span></span>

[<span data-ttu-id="bc0de-131">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bc0de-131">Get-AzureRmApplicationGateway</span></span>](./Get-AzureRmApplicationGateway.md)

[<span data-ttu-id="bc0de-132">Get-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="bc0de-132">Get-AzureRmApplicationGatewayBackendHttpSettings</span></span>](./Get-AzureRmApplicationGatewayBackendHttpSettings.md)

[<span data-ttu-id="bc0de-133">Get-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="bc0de-133">Get-AzureRmApplicationGatewayConnectionDraining</span></span>](./Get-AzureRmApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="bc0de-134">새로운 AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="bc0de-134">New-AzureRmApplicationGatewayConnectionDraining</span></span>](./New-AzureRmApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="bc0de-135">제거-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="bc0de-135">Remove-AzureRmApplicationGatewayConnectionDraining</span></span>](./Remove-AzureRmApplicationGatewayConnectionDraining.md)

