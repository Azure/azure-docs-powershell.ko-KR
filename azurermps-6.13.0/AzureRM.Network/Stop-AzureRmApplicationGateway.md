---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2C9609E8-0D8B-471B-9F0E-672BF55C3A0E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/stop-azurermapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Stop-AzureRmApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Stop-AzureRmApplicationGateway.md
ms.openlocfilehash: a235ae8ad4467e135e85599300869bcb36805a30
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702788"
---
# <span data-ttu-id="75b95-101">Stop-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="75b95-101">Stop-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="75b95-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75b95-102">SYNOPSIS</span></span>
<span data-ttu-id="75b95-103">응용 프로그램 게이트웨이를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="75b95-103">Stops an application gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="75b95-104">구문과</span><span class="sxs-lookup"><span data-stu-id="75b95-104">SYNTAX</span></span>

```
Stop-AzureRmApplicationGateway -ApplicationGateway <PSApplicationGateway> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="75b95-105">설명은</span><span class="sxs-lookup"><span data-stu-id="75b95-105">DESCRIPTION</span></span>
<span data-ttu-id="75b95-106">**AzureRmApplicationGateway** cmdlet은 응용 프로그램 게이트웨이를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="75b95-106">The **Stop-AzureRmApplicationGateway** cmdlet stops an application gateway.</span></span>

## <span data-ttu-id="75b95-107">예제의</span><span class="sxs-lookup"><span data-stu-id="75b95-107">EXAMPLES</span></span>

### <span data-ttu-id="75b95-108">예제 1: 응용 프로그램 게이트웨이 중지</span><span class="sxs-lookup"><span data-stu-id="75b95-108">Example 1: Stop an application gateway</span></span>
```
PS C:\>Stop-AzureRmApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="75b95-109">이 명령은 $AppGw 변수에 저장 된 응용 프로그램 게이트웨이를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="75b95-109">This command stops the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="75b95-110">변수</span><span class="sxs-lookup"><span data-stu-id="75b95-110">PARAMETERS</span></span>

### <span data-ttu-id="75b95-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="75b95-111">-ApplicationGateway</span></span>
<span data-ttu-id="75b95-112">이 cmdlet이 중지 하는 응용 프로그램 게이트웨이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="75b95-112">Specifies the application gateway that this cmdlet stops.</span></span>

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

### <span data-ttu-id="75b95-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="75b95-113">-AsJob</span></span>
<span data-ttu-id="75b95-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="75b95-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="75b95-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75b95-115">-DefaultProfile</span></span>
<span data-ttu-id="75b95-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="75b95-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="75b95-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75b95-117">CommonParameters</span></span>
<span data-ttu-id="75b95-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="75b95-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75b95-119">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75b95-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75b95-120">입력</span><span class="sxs-lookup"><span data-stu-id="75b95-120">INPUTS</span></span>

### <span data-ttu-id="75b95-121">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="75b95-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="75b95-122">매개 변수: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="75b95-122">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="75b95-123">출력</span><span class="sxs-lookup"><span data-stu-id="75b95-123">OUTPUTS</span></span>

### <span data-ttu-id="75b95-124">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="75b95-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="75b95-125">상속자</span><span class="sxs-lookup"><span data-stu-id="75b95-125">NOTES</span></span>

## <span data-ttu-id="75b95-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="75b95-126">RELATED LINKS</span></span>

[<span data-ttu-id="75b95-127">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="75b95-127">Get-AzureRmApplicationGateway</span></span>](./Get-AzureRmApplicationGateway.md)

[<span data-ttu-id="75b95-128">새로운 AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="75b95-128">New-AzureRmApplicationGateway</span></span>](./New-AzureRmApplicationGateway.md)

[<span data-ttu-id="75b95-129">제거-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="75b95-129">Remove-AzureRmApplicationGateway</span></span>](./Remove-AzureRmApplicationGateway.md)

[<span data-ttu-id="75b95-130">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="75b95-130">Set-AzureRmApplicationGateway</span></span>](./Set-AzureRmApplicationGateway.md)

[<span data-ttu-id="75b95-131">시작-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="75b95-131">Start-AzureRmApplicationGateway</span></span>](./Start-AzureRmApplicationGateway.md)


