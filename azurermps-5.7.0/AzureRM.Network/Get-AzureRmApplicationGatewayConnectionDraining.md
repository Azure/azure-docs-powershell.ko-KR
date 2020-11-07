---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayConnectionDraining.md
ms.openlocfilehash: 0c50f8b7fdd4a2093a734f3759bf6a893e56a8bb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703024"
---
# <span data-ttu-id="2ee37-101">Get-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="2ee37-101">Get-AzureRmApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="2ee37-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ee37-102">SYNOPSIS</span></span>
<span data-ttu-id="2ee37-103">백 엔드 HTTP 설정 개체의 연결 드레이닝 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2ee37-103">Gets the connection draining configuration of a back-end HTTP settings object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2ee37-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2ee37-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayConnectionDraining -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2ee37-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2ee37-105">DESCRIPTION</span></span>
<span data-ttu-id="2ee37-106">**AzureRmApplicationGatewayConnectionDraining** cmdlet은 백 엔드 HTTP 설정 개체의 연결 드레이닝 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2ee37-106">The **Get-AzureRmApplicationGatewayConnectionDraining** cmdlet gets the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="2ee37-107">예제의</span><span class="sxs-lookup"><span data-stu-id="2ee37-107">EXAMPLES</span></span>

### <span data-ttu-id="2ee37-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="2ee37-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzureRmApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> $ConnectionDraining = Get-AzureRmApplicationGatewayConnectionDraining -BackendHttpSettings $Settings
```

<span data-ttu-id="2ee37-109">첫 번째 명령은 ResourceGroup01 이라는 리소스 그룹에서 ApplicationGateway01 라는 응용 프로그램 게이트웨이를 가져와이를 $AppGw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ee37-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="2ee37-110">두 번째 명령은 $AppGw에 대 한 Settings01 라는 백 엔드 HTTP 설정을 가져오고 $Settings 변수에 설정을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ee37-110">The second command gets the back-end HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>
<span data-ttu-id="2ee37-111">마지막 명령은 백 엔드 HTTP 설정 $Settings의 연결 드레이닝 구성을 가져와 $ConnectionDraining 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ee37-111">The last command gets the connection draining configuration from the back-end HTTP settings $Settings and stores it in the $ConnectionDraining variable.</span></span>

## <span data-ttu-id="2ee37-112">변수</span><span class="sxs-lookup"><span data-stu-id="2ee37-112">PARAMETERS</span></span>

### <span data-ttu-id="2ee37-113">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="2ee37-113">-BackendHttpSettings</span></span>
<span data-ttu-id="2ee37-114">백 엔드 http 설정</span><span class="sxs-lookup"><span data-stu-id="2ee37-114">The backend http settings</span></span>

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

### <span data-ttu-id="2ee37-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ee37-115">-DefaultProfile</span></span>
<span data-ttu-id="2ee37-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2ee37-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2ee37-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ee37-117">CommonParameters</span></span>
<span data-ttu-id="2ee37-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ee37-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ee37-119">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ee37-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ee37-120">입력</span><span class="sxs-lookup"><span data-stu-id="2ee37-120">INPUTS</span></span>

### <span data-ttu-id="2ee37-121">PSApplicationGatewayBackendHttpSettings에 대 한.</span><span class="sxs-lookup"><span data-stu-id="2ee37-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="2ee37-122">출력</span><span class="sxs-lookup"><span data-stu-id="2ee37-122">OUTPUTS</span></span>

### <span data-ttu-id="2ee37-123">Microsoft. 네트워크 모델. Psapplication게이트웨이 Connection드레이닝</span><span class="sxs-lookup"><span data-stu-id="2ee37-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="2ee37-124">상속자</span><span class="sxs-lookup"><span data-stu-id="2ee37-124">NOTES</span></span>

## <span data-ttu-id="2ee37-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2ee37-125">RELATED LINKS</span></span>

[<span data-ttu-id="2ee37-126">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2ee37-126">Get-AzureRmApplicationGateway</span></span>](./Get-AzureRmApplicationGateway.md)

[<span data-ttu-id="2ee37-127">Get-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="2ee37-127">Get-AzureRmApplicationGatewayBackendHttpSettings</span></span>](./Get-AzureRmApplicationGatewayBackendHttpSettings.md)

[<span data-ttu-id="2ee37-128">새로운 AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="2ee37-128">New-AzureRmApplicationGatewayConnectionDraining</span></span>](./New-AzureRmApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="2ee37-129">제거-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="2ee37-129">Remove-AzureRmApplicationGatewayConnectionDraining</span></span>](./Remove-AzureRmApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="2ee37-130">Set-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="2ee37-130">Set-AzureRmApplicationGatewayConnectionDraining</span></span>](./Set-AzureRmApplicationGatewayConnectionDraining.md)
