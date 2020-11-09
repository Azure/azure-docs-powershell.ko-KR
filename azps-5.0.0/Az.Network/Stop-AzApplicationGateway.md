---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2C9609E8-0D8B-471B-9F0E-672BF55C3A0E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzApplicationGateway.md
ms.openlocfilehash: 4c7001bf69e6dc8f418f1bc56867154bf9d769ce
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94311276"
---
# <span data-ttu-id="26575-101">Stop-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="26575-101">Stop-AzApplicationGateway</span></span>

## <span data-ttu-id="26575-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26575-102">SYNOPSIS</span></span>
<span data-ttu-id="26575-103">응용 프로그램 게이트웨이를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="26575-103">Stops an application gateway</span></span>

## <span data-ttu-id="26575-104">구문과</span><span class="sxs-lookup"><span data-stu-id="26575-104">SYNTAX</span></span>

```
Stop-AzApplicationGateway -ApplicationGateway <PSApplicationGateway> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="26575-105">설명은</span><span class="sxs-lookup"><span data-stu-id="26575-105">DESCRIPTION</span></span>
<span data-ttu-id="26575-106">**AzApplicationGateway** cmdlet은 응용 프로그램 게이트웨이를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="26575-106">The **Stop-AzApplicationGateway** cmdlet stops an application gateway.</span></span>

## <span data-ttu-id="26575-107">예제의</span><span class="sxs-lookup"><span data-stu-id="26575-107">EXAMPLES</span></span>

### <span data-ttu-id="26575-108">예제 1: 응용 프로그램 게이트웨이 중지</span><span class="sxs-lookup"><span data-stu-id="26575-108">Example 1: Stop an application gateway</span></span>
```
PS C:\>Stop-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="26575-109">이 명령은 $AppGw 변수에 저장 된 응용 프로그램 게이트웨이를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="26575-109">This command stops the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="26575-110">변수</span><span class="sxs-lookup"><span data-stu-id="26575-110">PARAMETERS</span></span>

### <span data-ttu-id="26575-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="26575-111">-ApplicationGateway</span></span>
<span data-ttu-id="26575-112">이 cmdlet이 중지 하는 응용 프로그램 게이트웨이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="26575-112">Specifies the application gateway that this cmdlet stops.</span></span>

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

### <span data-ttu-id="26575-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="26575-113">-AsJob</span></span>
<span data-ttu-id="26575-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="26575-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26575-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26575-115">-DefaultProfile</span></span>
<span data-ttu-id="26575-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="26575-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26575-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26575-117">CommonParameters</span></span>
<span data-ttu-id="26575-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="26575-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26575-119">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26575-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26575-120">입력</span><span class="sxs-lookup"><span data-stu-id="26575-120">INPUTS</span></span>

### <span data-ttu-id="26575-121">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="26575-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="26575-122">출력</span><span class="sxs-lookup"><span data-stu-id="26575-122">OUTPUTS</span></span>

### <span data-ttu-id="26575-123">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="26575-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="26575-124">상속자</span><span class="sxs-lookup"><span data-stu-id="26575-124">NOTES</span></span>

## <span data-ttu-id="26575-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="26575-125">RELATED LINKS</span></span>

[<span data-ttu-id="26575-126">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="26575-126">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="26575-127">새로운 AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="26575-127">New-AzApplicationGateway</span></span>](./New-AzApplicationGateway.md)

[<span data-ttu-id="26575-128">제거-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="26575-128">Remove-AzApplicationGateway</span></span>](./Remove-AzApplicationGateway.md)

[<span data-ttu-id="26575-129">Set-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="26575-129">Set-AzApplicationGateway</span></span>](./Set-AzApplicationGateway.md)

[<span data-ttu-id="26575-130">시작-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="26575-130">Start-AzApplicationGateway</span></span>](./Start-AzApplicationGateway.md)


