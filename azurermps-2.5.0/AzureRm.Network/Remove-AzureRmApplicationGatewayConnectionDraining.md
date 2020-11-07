---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayconnectiondraining
schema: 2.0.0
ms.openlocfilehash: 751e27600d81a24005ea0a9200d3efa1d1647597
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882882"
---
# <span data-ttu-id="b3eac-101">Remove-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="b3eac-101">Remove-AzureRmApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="b3eac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3eac-102">SYNOPSIS</span></span>
<span data-ttu-id="b3eac-103">백 엔드 HTTP 설정 개체의 연결 드레이닝 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3eac-103">Removes the connection draining configuration of a back-end HTTP settings object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b3eac-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b3eac-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayConnectionDraining
 -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b3eac-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b3eac-105">DESCRIPTION</span></span>
<span data-ttu-id="b3eac-106">**AzureRmApplicationGatewayConnectionDraining** cmdlet은 백 엔드 HTTP 설정 개체의 연결 드레이닝 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3eac-106">The **Remove-AzureRmApplicationGatewayConnectionDraining** cmdlet removes the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="b3eac-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b3eac-107">EXAMPLES</span></span>

### <span data-ttu-id="b3eac-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="b3eac-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzureRmApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> Remove-AzureRmApplicationGatewayConnectionDraining -BackendHttpSettings $Settings
```

<span data-ttu-id="b3eac-109">첫 번째 명령은 ResourceGroup01 이라는 리소스 그룹에서 ApplicationGateway01 라는 응용 프로그램 게이트웨이를 가져와이를 $AppGw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3eac-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="b3eac-110">두 번째 명령은 $AppGw에 대 한 Settings01 라는 백 엔드 HTTP 설정을 가져오고 $Settings 변수에 설정을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3eac-110">The second command gets the back-end HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>
<span data-ttu-id="b3eac-111">마지막 명령은 $Settings에 저장 된 백 엔드 HTTP 설정의 연결 드레이닝 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3eac-111">The last command removes the connection draining configuration of the back-end HTTP settings stored in $Settings.</span></span>

## <span data-ttu-id="b3eac-112">변수</span><span class="sxs-lookup"><span data-stu-id="b3eac-112">PARAMETERS</span></span>

### <span data-ttu-id="b3eac-113">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="b3eac-113">-BackendHttpSettings</span></span>
<span data-ttu-id="b3eac-114">백 엔드 http 설정</span><span class="sxs-lookup"><span data-stu-id="b3eac-114">The backend http settings</span></span>

```yaml
Type: PSApplicationGatewayBackendHttpSettings
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b3eac-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3eac-115">-DefaultProfile</span></span>
<span data-ttu-id="b3eac-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b3eac-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b3eac-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3eac-117">CommonParameters</span></span>
<span data-ttu-id="b3eac-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3eac-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3eac-119">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3eac-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3eac-120">입력</span><span class="sxs-lookup"><span data-stu-id="b3eac-120">INPUTS</span></span>

### <span data-ttu-id="b3eac-121">PSApplicationGatewayBackendHttpSettings에 대 한.</span><span class="sxs-lookup"><span data-stu-id="b3eac-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="b3eac-122">출력</span><span class="sxs-lookup"><span data-stu-id="b3eac-122">OUTPUTS</span></span>

### <span data-ttu-id="b3eac-123">PSApplicationGatewayBackendHttpSettings에 대 한.</span><span class="sxs-lookup"><span data-stu-id="b3eac-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="b3eac-124">상속자</span><span class="sxs-lookup"><span data-stu-id="b3eac-124">NOTES</span></span>

## <span data-ttu-id="b3eac-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b3eac-125">RELATED LINKS</span></span>

[<span data-ttu-id="b3eac-126">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b3eac-126">Get-AzureRmApplicationGateway</span></span>](./Get-AzureRmApplicationGateway.md)

[<span data-ttu-id="b3eac-127">Get-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="b3eac-127">Get-AzureRmApplicationGatewayBackendHttpSettings</span></span>](./Get-AzureRmApplicationGatewayBackendHttpSettings.md)

[<span data-ttu-id="b3eac-128">Get-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="b3eac-128">Get-AzureRmApplicationGatewayConnectionDraining</span></span>](./Get-AzureRmApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="b3eac-129">새로운 AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="b3eac-129">New-AzureRmApplicationGatewayConnectionDraining</span></span>](./New-AzureRmApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="b3eac-130">Set-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="b3eac-130">Set-AzureRmApplicationGatewayConnectionDraining</span></span>](./Set-AzureRmApplicationGatewayConnectionDraining.md)

