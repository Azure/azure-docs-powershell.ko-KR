---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 95731734-EDCA-432A-A7BF-94D1E3725FB2
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Start-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Start-AzApplicationGateway.md
ms.openlocfilehash: 8c37ed72659c8b5ab00d54a7ecbe9622cb9f553b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876530"
---
# <span data-ttu-id="389f6-101">Start-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="389f6-101">Start-AzApplicationGateway</span></span>

## <span data-ttu-id="389f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="389f6-102">SYNOPSIS</span></span>
<span data-ttu-id="389f6-103">응용 프로그램 게이트웨이를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="389f6-103">Starts an application gateway.</span></span>

## <span data-ttu-id="389f6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="389f6-104">SYNTAX</span></span>

```
Start-AzApplicationGateway -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="389f6-105">설명은</span><span class="sxs-lookup"><span data-stu-id="389f6-105">DESCRIPTION</span></span>
<span data-ttu-id="389f6-106">**AzApplicationGateway** Cmdlet은 Azure application gateway를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="389f6-106">The **Start-AzApplicationGateway** cmdlet starts an Azure application gateway</span></span>

## <span data-ttu-id="389f6-107">예제의</span><span class="sxs-lookup"><span data-stu-id="389f6-107">EXAMPLES</span></span>

### <span data-ttu-id="389f6-108">Example1: 응용 프로그램 게이트웨이 시작</span><span class="sxs-lookup"><span data-stu-id="389f6-108">Example1: Start an application gateway</span></span>
```
PS C:\>$AppGw = Start-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="389f6-109">이 명령은 $AppGw 변수에 저장 된 응용 프로그램 게이트웨이를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="389f6-109">This command starts the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="389f6-110">변수</span><span class="sxs-lookup"><span data-stu-id="389f6-110">PARAMETERS</span></span>

### <span data-ttu-id="389f6-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="389f6-111">-ApplicationGateway</span></span>
<span data-ttu-id="389f6-112">이 cmdlet이 시작 하는 응용 프로그램 게이트웨이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="389f6-112">Specifies the application gateway that this cmdlet starts.</span></span>

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

### <span data-ttu-id="389f6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="389f6-113">-DefaultProfile</span></span>
<span data-ttu-id="389f6-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="389f6-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="389f6-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="389f6-115">CommonParameters</span></span>
<span data-ttu-id="389f6-116">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="389f6-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="389f6-117">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="389f6-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="389f6-118">입력</span><span class="sxs-lookup"><span data-stu-id="389f6-118">INPUTS</span></span>

### <span data-ttu-id="389f6-119">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="389f6-119">System.String</span></span>

## <span data-ttu-id="389f6-120">출력</span><span class="sxs-lookup"><span data-stu-id="389f6-120">OUTPUTS</span></span>

### <span data-ttu-id="389f6-121">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="389f6-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="389f6-122">상속자</span><span class="sxs-lookup"><span data-stu-id="389f6-122">NOTES</span></span>

## <span data-ttu-id="389f6-123">관련 링크</span><span class="sxs-lookup"><span data-stu-id="389f6-123">RELATED LINKS</span></span>

[<span data-ttu-id="389f6-124">중지-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="389f6-124">Stop-AzApplicationGateway</span></span>](./Stop-AzApplicationGateway.md)


