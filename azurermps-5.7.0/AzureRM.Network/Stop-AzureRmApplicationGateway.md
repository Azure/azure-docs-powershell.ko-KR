---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2C9609E8-0D8B-471B-9F0E-672BF55C3A0E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/stop-azurermapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Stop-AzureRmApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Stop-AzureRmApplicationGateway.md
ms.openlocfilehash: cf8a639b6ebbe2b5ea7c0e07f212de3c742e7556
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530431"
---
# <span data-ttu-id="ac9e3-101">Stop-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ac9e3-101">Stop-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="ac9e3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ac9e3-102">SYNOPSIS</span></span>
<span data-ttu-id="ac9e3-103">응용 프로그램 게이트웨이를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac9e3-103">Stops an application gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ac9e3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ac9e3-104">SYNTAX</span></span>

```
Stop-AzureRmApplicationGateway -ApplicationGateway <PSApplicationGateway> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ac9e3-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ac9e3-105">DESCRIPTION</span></span>
<span data-ttu-id="ac9e3-106">**AzureRmApplicationGateway** cmdlet은 응용 프로그램 게이트웨이를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac9e3-106">The **Stop-AzureRmApplicationGateway** cmdlet stops an application gateway.</span></span>

## <span data-ttu-id="ac9e3-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ac9e3-107">EXAMPLES</span></span>

### <span data-ttu-id="ac9e3-108">예제 1: 응용 프로그램 게이트웨이 중지</span><span class="sxs-lookup"><span data-stu-id="ac9e3-108">Example 1: Stop an application gateway</span></span>
```
PS C:\>Stop-AzureRmApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="ac9e3-109">이 명령은 $AppGw 변수에 저장 된 응용 프로그램 게이트웨이를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac9e3-109">This command stops the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="ac9e3-110">변수</span><span class="sxs-lookup"><span data-stu-id="ac9e3-110">PARAMETERS</span></span>

### <span data-ttu-id="ac9e3-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ac9e3-111">-ApplicationGateway</span></span>
<span data-ttu-id="ac9e3-112">이 cmdlet이 중지 하는 응용 프로그램 게이트웨이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac9e3-112">Specifies the application gateway that this cmdlet stops.</span></span>

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

### <span data-ttu-id="ac9e3-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ac9e3-113">-AsJob</span></span>
<span data-ttu-id="ac9e3-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="ac9e3-114">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac9e3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac9e3-115">-DefaultProfile</span></span>
<span data-ttu-id="ac9e3-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ac9e3-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ac9e3-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac9e3-117">CommonParameters</span></span>
<span data-ttu-id="ac9e3-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac9e3-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac9e3-119">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac9e3-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac9e3-120">입력</span><span class="sxs-lookup"><span data-stu-id="ac9e3-120">INPUTS</span></span>

### <span data-ttu-id="ac9e3-121">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ac9e3-121">System.String</span></span>

## <span data-ttu-id="ac9e3-122">출력</span><span class="sxs-lookup"><span data-stu-id="ac9e3-122">OUTPUTS</span></span>

### <span data-ttu-id="ac9e3-123">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ac9e3-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ac9e3-124">상속자</span><span class="sxs-lookup"><span data-stu-id="ac9e3-124">NOTES</span></span>

## <span data-ttu-id="ac9e3-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ac9e3-125">RELATED LINKS</span></span>

[<span data-ttu-id="ac9e3-126">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ac9e3-126">Get-AzureRmApplicationGateway</span></span>](./Get-AzureRmApplicationGateway.md)

[<span data-ttu-id="ac9e3-127">새로운 AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ac9e3-127">New-AzureRmApplicationGateway</span></span>](./New-AzureRmApplicationGateway.md)

[<span data-ttu-id="ac9e3-128">제거-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ac9e3-128">Remove-AzureRmApplicationGateway</span></span>](./Remove-AzureRmApplicationGateway.md)

[<span data-ttu-id="ac9e3-129">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ac9e3-129">Set-AzureRmApplicationGateway</span></span>](./Set-AzureRmApplicationGateway.md)

[<span data-ttu-id="ac9e3-130">시작-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ac9e3-130">Start-AzureRmApplicationGateway</span></span>](./Start-AzureRmApplicationGateway.md)


