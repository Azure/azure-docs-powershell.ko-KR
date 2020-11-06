---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 95731734-EDCA-432A-A7BF-94D1E3725FB2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/start-azurermapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Start-AzureRmApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Start-AzureRmApplicationGateway.md
ms.openlocfilehash: 2faa1b245a38a5ef66bb5131f79000218c39d55c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533695"
---
# <span data-ttu-id="11f64-101">Start-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="11f64-101">Start-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="11f64-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11f64-102">SYNOPSIS</span></span>
<span data-ttu-id="11f64-103">응용 프로그램 게이트웨이를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="11f64-103">Starts an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="11f64-104">구문과</span><span class="sxs-lookup"><span data-stu-id="11f64-104">SYNTAX</span></span>

```
Start-AzureRmApplicationGateway -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="11f64-105">설명은</span><span class="sxs-lookup"><span data-stu-id="11f64-105">DESCRIPTION</span></span>
<span data-ttu-id="11f64-106">**AzureRmApplicationGateway** Cmdlet은 Azure application gateway를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="11f64-106">The **Start-AzureRmApplicationGateway** cmdlet starts an Azure application gateway</span></span>

## <span data-ttu-id="11f64-107">예제의</span><span class="sxs-lookup"><span data-stu-id="11f64-107">EXAMPLES</span></span>

### <span data-ttu-id="11f64-108">Example1: 응용 프로그램 게이트웨이 시작</span><span class="sxs-lookup"><span data-stu-id="11f64-108">Example1: Start an application gateway</span></span>
```
PS C:\>$AppGw = Start-AzureRmApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="11f64-109">이 명령은 $AppGw 변수에 저장 된 응용 프로그램 게이트웨이를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="11f64-109">This command starts the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="11f64-110">변수</span><span class="sxs-lookup"><span data-stu-id="11f64-110">PARAMETERS</span></span>

### <span data-ttu-id="11f64-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="11f64-111">-ApplicationGateway</span></span>
<span data-ttu-id="11f64-112">이 cmdlet이 시작 하는 응용 프로그램 게이트웨이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11f64-112">Specifies the application gateway that this cmdlet starts.</span></span>

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

### <span data-ttu-id="11f64-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11f64-113">-DefaultProfile</span></span>
<span data-ttu-id="11f64-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="11f64-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="11f64-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11f64-115">CommonParameters</span></span>
<span data-ttu-id="11f64-116">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="11f64-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11f64-117">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11f64-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11f64-118">입력</span><span class="sxs-lookup"><span data-stu-id="11f64-118">INPUTS</span></span>

### <span data-ttu-id="11f64-119">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="11f64-119">System.String</span></span>

## <span data-ttu-id="11f64-120">출력</span><span class="sxs-lookup"><span data-stu-id="11f64-120">OUTPUTS</span></span>

### <span data-ttu-id="11f64-121">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="11f64-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="11f64-122">상속자</span><span class="sxs-lookup"><span data-stu-id="11f64-122">NOTES</span></span>

## <span data-ttu-id="11f64-123">관련 링크</span><span class="sxs-lookup"><span data-stu-id="11f64-123">RELATED LINKS</span></span>

[<span data-ttu-id="11f64-124">중지-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="11f64-124">Stop-AzureRmApplicationGateway</span></span>](./Stop-AzureRmApplicationGateway.md)


