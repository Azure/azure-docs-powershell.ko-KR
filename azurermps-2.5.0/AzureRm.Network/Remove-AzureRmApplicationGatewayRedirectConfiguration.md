---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayredirectconfiguration
schema: 2.0.0
ms.openlocfilehash: ba979a12584d526ba7e3a36d13c44b51704b44f6
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93880986"
---
# <span data-ttu-id="2b8c2-101">Remove-AzureRmApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="2b8c2-101">Remove-AzureRmApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="2b8c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b8c2-102">SYNOPSIS</span></span>
<span data-ttu-id="2b8c2-103">기존 응용 프로그램 게이트웨이에서 리디렉션 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b8c2-103">Removes a redirect configuration from an existing Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2b8c2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2b8c2-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayRedirectConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2b8c2-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2b8c2-105">DESCRIPTION</span></span>
<span data-ttu-id="2b8c2-106">**AzureRmApplicationGatewayRedirectConfiguration** cmdlet은 기존 응용 프로그램 게이트웨이에서 리디렉션 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b8c2-106">The **Remove-AzureRmApplicationGatewayRedirectConfiguration** cmdlet removes a redirect configuration from an existing Application Gateway.</span></span>

## <span data-ttu-id="2b8c2-107">예제의</span><span class="sxs-lookup"><span data-stu-id="2b8c2-107">EXAMPLES</span></span>

### <span data-ttu-id="2b8c2-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="2b8c2-108">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\>$AppGw = Remove-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway $AppGw -Name "Redirect01"
```

<span data-ttu-id="2b8c2-109">첫 번째 명령은 응용 프로그램 게이트웨이를 가져와 $AppGw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b8c2-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="2b8c2-110">두 번째 명령은 $AppGw에 저장 된 응용 프로그램 게이트웨이에서 Redirect01 이라는 리디렉션 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b8c2-110">The second command removes the redirect configuration named Redirect01 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="2b8c2-111">변수</span><span class="sxs-lookup"><span data-stu-id="2b8c2-111">PARAMETERS</span></span>

### <span data-ttu-id="2b8c2-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2b8c2-112">-ApplicationGateway</span></span>
<span data-ttu-id="2b8c2-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2b8c2-113">The applicationGateway</span></span>

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

### <span data-ttu-id="2b8c2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b8c2-114">-DefaultProfile</span></span>
<span data-ttu-id="2b8c2-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2b8c2-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2b8c2-116">-이름</span><span class="sxs-lookup"><span data-stu-id="2b8c2-116">-Name</span></span>
<span data-ttu-id="2b8c2-117">리디렉션 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2b8c2-117">The name of the redirect configuration</span></span>

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

### <span data-ttu-id="2b8c2-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b8c2-118">CommonParameters</span></span>
<span data-ttu-id="2b8c2-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b8c2-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b8c2-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b8c2-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b8c2-121">입력</span><span class="sxs-lookup"><span data-stu-id="2b8c2-121">INPUTS</span></span>

### <span data-ttu-id="2b8c2-122">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2b8c2-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2b8c2-123">출력</span><span class="sxs-lookup"><span data-stu-id="2b8c2-123">OUTPUTS</span></span>

### <span data-ttu-id="2b8c2-124">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2b8c2-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2b8c2-125">상속자</span><span class="sxs-lookup"><span data-stu-id="2b8c2-125">NOTES</span></span>

## <span data-ttu-id="2b8c2-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2b8c2-126">RELATED LINKS</span></span>

