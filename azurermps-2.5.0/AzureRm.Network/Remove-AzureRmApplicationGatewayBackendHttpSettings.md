---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewaybackendhttpsettings
schema: 2.0.0
ms.openlocfilehash: 71ce0dd8d4c5988dfc5cd4226ee76dcec46042ff
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93881349"
---
# <span data-ttu-id="1508c-101">Remove-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="1508c-101">Remove-AzureRmApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="1508c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1508c-102">SYNOPSIS</span></span>
<span data-ttu-id="1508c-103">응용 프로그램 게이트웨이에서 백 엔드 HTTP 설정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1508c-103">Removes back-end HTTP settings from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1508c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1508c-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayBackendHttpSettings -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1508c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1508c-105">DESCRIPTION</span></span>
<span data-ttu-id="1508c-106">Remove-AzureRmApplicationGatewayBackendHttpSettings cmdlet은 Azure application gateway에서 백 엔드 HTTP (하이퍼텍스트 전송 프로토콜) 설정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1508c-106">The Remove-AzureRmApplicationGatewayBackendHttpSettings cmdlet removes back-end Hypertext Transfer Protocol (HTTP) settings from an Azure application gateway.</span></span>

## <span data-ttu-id="1508c-107">예제의</span><span class="sxs-lookup"><span data-stu-id="1508c-107">EXAMPLES</span></span>

### <span data-ttu-id="1508c-108">예제 1: 응용 프로그램 게이트웨이에서 백 엔드 HTTP 설정 제거</span><span class="sxs-lookup"><span data-stu-id="1508c-108">Example 1: Remove back-end HTTP settings from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayBackendHttpSettings -ApplicationGateway $AppGw -Name "BackEndSetting02"
```

<span data-ttu-id="1508c-109">첫 번째 명령은 ResourceGroup01 이라는 리소스 그룹에 속하고이를 $AppGw 변수에 저장 하는 ApplicationGateway01 라는 응용 프로그램 게이트웨이를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1508c-109">The first command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="1508c-110">두 번째 명령은 $AppGw에 저장 된 응용 프로그램 게이트웨이에서 BackEndSetting02 이라는 백 엔드 HTTP 설정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1508c-110">The second command removes the back-end HTTP setting named BackEndSetting02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="1508c-111">변수</span><span class="sxs-lookup"><span data-stu-id="1508c-111">PARAMETERS</span></span>

### <span data-ttu-id="1508c-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1508c-112">-ApplicationGateway</span></span>
<span data-ttu-id="1508c-113">이 cmdlet이 백 엔드 HTTP 설정을 제거 하는 응용 프로그램 게이트웨이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1508c-113">Specifies the application gateway from which this cmdlet removes back-end HTTP settings.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1508c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1508c-114">-DefaultProfile</span></span>
<span data-ttu-id="1508c-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1508c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1508c-116">-이름</span><span class="sxs-lookup"><span data-stu-id="1508c-116">-Name</span></span>
<span data-ttu-id="1508c-117">이 cmdlet이 제거 하는 백 엔드 HTTP 설정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1508c-117">Specifies the name of the back-end HTTP settings that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1508c-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1508c-118">CommonParameters</span></span>
<span data-ttu-id="1508c-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1508c-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1508c-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1508c-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1508c-121">입력</span><span class="sxs-lookup"><span data-stu-id="1508c-121">INPUTS</span></span>

### <span data-ttu-id="1508c-122">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="1508c-122">System.String</span></span>

## <span data-ttu-id="1508c-123">출력</span><span class="sxs-lookup"><span data-stu-id="1508c-123">OUTPUTS</span></span>

### <span data-ttu-id="1508c-124">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1508c-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1508c-125">상속자</span><span class="sxs-lookup"><span data-stu-id="1508c-125">NOTES</span></span>

## <span data-ttu-id="1508c-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1508c-126">RELATED LINKS</span></span>

[<span data-ttu-id="1508c-127">추가-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="1508c-127">Add-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="1508c-128">새로운 AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="1508c-128">New-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="1508c-129">Get-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="1508c-129">Get-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="1508c-130">Set-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="1508c-130">Set-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()
