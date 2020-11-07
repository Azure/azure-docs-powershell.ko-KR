---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 95731734-EDCA-432A-A7BF-94D1E3725FB2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/start-azurermapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Start-AzureRmApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Start-AzureRmApplicationGateway.md
ms.openlocfilehash: 88ca18eca50f1e68eab8599ad79f902ff1fd2551
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702790"
---
# <span data-ttu-id="9534d-101">Start-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9534d-101">Start-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="9534d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9534d-102">SYNOPSIS</span></span>
<span data-ttu-id="9534d-103">응용 프로그램 게이트웨이를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="9534d-103">Starts an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9534d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9534d-104">SYNTAX</span></span>

```
Start-AzureRmApplicationGateway -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9534d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="9534d-105">DESCRIPTION</span></span>
<span data-ttu-id="9534d-106">**AzureRmApplicationGateway** Cmdlet은 Azure application gateway를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="9534d-106">The **Start-AzureRmApplicationGateway** cmdlet starts an Azure application gateway</span></span>

## <span data-ttu-id="9534d-107">예제의</span><span class="sxs-lookup"><span data-stu-id="9534d-107">EXAMPLES</span></span>

### <span data-ttu-id="9534d-108">Example1: 응용 프로그램 게이트웨이 시작</span><span class="sxs-lookup"><span data-stu-id="9534d-108">Example1: Start an application gateway</span></span>
```
PS C:\>$AppGw = Start-AzureRmApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="9534d-109">이 명령은 $AppGw 변수에 저장 된 응용 프로그램 게이트웨이를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="9534d-109">This command starts the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="9534d-110">변수</span><span class="sxs-lookup"><span data-stu-id="9534d-110">PARAMETERS</span></span>

### <span data-ttu-id="9534d-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9534d-111">-ApplicationGateway</span></span>
<span data-ttu-id="9534d-112">이 cmdlet이 시작 하는 응용 프로그램 게이트웨이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9534d-112">Specifies the application gateway that this cmdlet starts.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9534d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9534d-113">-DefaultProfile</span></span>
<span data-ttu-id="9534d-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9534d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9534d-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9534d-115">CommonParameters</span></span>
<span data-ttu-id="9534d-116">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9534d-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9534d-117">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9534d-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9534d-118">입력</span><span class="sxs-lookup"><span data-stu-id="9534d-118">INPUTS</span></span>

### <span data-ttu-id="9534d-119">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9534d-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="9534d-120">매개 변수: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="9534d-120">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="9534d-121">출력</span><span class="sxs-lookup"><span data-stu-id="9534d-121">OUTPUTS</span></span>

### <span data-ttu-id="9534d-122">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9534d-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9534d-123">상속자</span><span class="sxs-lookup"><span data-stu-id="9534d-123">NOTES</span></span>

## <span data-ttu-id="9534d-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9534d-124">RELATED LINKS</span></span>

[<span data-ttu-id="9534d-125">중지-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9534d-125">Stop-AzureRmApplicationGateway</span></span>](./Stop-AzureRmApplicationGateway.md)


