---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 95731734-EDCA-432A-A7BF-94D1E3725FB2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/start-azurermapplicationgateway
schema: 2.0.0
ms.openlocfilehash: 382c4cd1b189e0dc95edd4824dec58a280dbb889
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882150"
---
# <span data-ttu-id="2aa63-101">Start-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2aa63-101">Start-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="2aa63-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2aa63-102">SYNOPSIS</span></span>
<span data-ttu-id="2aa63-103">응용 프로그램 게이트웨이를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aa63-103">Starts an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2aa63-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2aa63-104">SYNTAX</span></span>

```
Start-AzureRmApplicationGateway -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2aa63-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2aa63-105">DESCRIPTION</span></span>
<span data-ttu-id="2aa63-106">**AzureRmApplicationGateway** Cmdlet은 Azure application gateway를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aa63-106">The **Start-AzureRmApplicationGateway** cmdlet starts an Azure application gateway</span></span>

## <span data-ttu-id="2aa63-107">예제의</span><span class="sxs-lookup"><span data-stu-id="2aa63-107">EXAMPLES</span></span>

### <span data-ttu-id="2aa63-108">Example1: 응용 프로그램 게이트웨이 시작</span><span class="sxs-lookup"><span data-stu-id="2aa63-108">Example1: Start an application gateway</span></span>
```
PS C:\>$AppGw = Start-AzureRmApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="2aa63-109">이 명령은 $AppGw 변수에 저장 된 응용 프로그램 게이트웨이를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aa63-109">This command starts the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="2aa63-110">변수</span><span class="sxs-lookup"><span data-stu-id="2aa63-110">PARAMETERS</span></span>

### <span data-ttu-id="2aa63-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2aa63-111">-ApplicationGateway</span></span>
<span data-ttu-id="2aa63-112">이 cmdlet이 시작 하는 응용 프로그램 게이트웨이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aa63-112">Specifies the application gateway that this cmdlet starts.</span></span>

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

### <span data-ttu-id="2aa63-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2aa63-113">-DefaultProfile</span></span>
<span data-ttu-id="2aa63-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2aa63-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2aa63-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2aa63-115">CommonParameters</span></span>
<span data-ttu-id="2aa63-116">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aa63-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2aa63-117">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2aa63-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2aa63-118">입력</span><span class="sxs-lookup"><span data-stu-id="2aa63-118">INPUTS</span></span>

### <span data-ttu-id="2aa63-119">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="2aa63-119">System.String</span></span>

## <span data-ttu-id="2aa63-120">출력</span><span class="sxs-lookup"><span data-stu-id="2aa63-120">OUTPUTS</span></span>

### <span data-ttu-id="2aa63-121">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2aa63-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2aa63-122">상속자</span><span class="sxs-lookup"><span data-stu-id="2aa63-122">NOTES</span></span>

## <span data-ttu-id="2aa63-123">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2aa63-123">RELATED LINKS</span></span>

[<span data-ttu-id="2aa63-124">중지-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2aa63-124">Stop-AzureRmApplicationGateway</span></span>](./Stop-AzureRmApplicationGateway.md)


