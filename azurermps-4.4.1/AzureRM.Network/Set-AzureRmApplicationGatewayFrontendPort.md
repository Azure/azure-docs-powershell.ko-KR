---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 85C0A1C3-FC6D-496A-B6B5-8DC2A73B8032
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayFrontendPort.md
ms.openlocfilehash: 1c6a5ffee2f4a8b358f483fee2904fe1a7a970da
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525479"
---
# <span data-ttu-id="533f4-101">Set-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="533f4-101">Set-AzureRmApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="533f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="533f4-102">SYNOPSIS</span></span>
<span data-ttu-id="533f4-103">응용 프로그램 게이트웨이의 프런트 엔드 포트를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="533f4-103">Modifies a front-end port for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="533f4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="533f4-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayFrontendPort -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Port <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="533f4-105">설명은</span><span class="sxs-lookup"><span data-stu-id="533f4-105">DESCRIPTION</span></span>
<span data-ttu-id="533f4-106">**AzureRmApplicationGatewayFrontendPort** cmdlet은 응용 프로그램 게이트웨이의 프런트 엔드 포트를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="533f4-106">The **Set-AzureRmApplicationGatewayFrontendPort** cmdlet modifies a front-end port for an application gateway.</span></span>

## <span data-ttu-id="533f4-107">예제의</span><span class="sxs-lookup"><span data-stu-id="533f4-107">EXAMPLES</span></span>

### <span data-ttu-id="533f4-108">예제 1: 응용 프로그램 게이트웨이 프런트 엔드 포트 설정 80</span><span class="sxs-lookup"><span data-stu-id="533f4-108">Example 1: Set an application gateway front-end port to 80</span></span>
```
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayFrontendPort -ApplicationGateway $AppGw -Name "FrontEndPort01" -Port 80
```

<span data-ttu-id="533f4-109">첫 번째 명령은 ResourceGroup01 이라는 리소스 그룹에 속하는 ApplicationGateway01 라는 응용 프로그램 게이트웨이를 가져온 다음이를 $AppGw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="533f4-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="533f4-110">두 번째 명령은 FrontEndPort01 이라는 프런트 엔드 포트에 대해 포트 80을 사용 하도록 $AppGw에서 게이트웨이를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="533f4-110">The second command modifies the gateway in $AppGw to use port 80 for the front-end port named FrontEndPort01.</span></span>

## <span data-ttu-id="533f4-111">변수</span><span class="sxs-lookup"><span data-stu-id="533f4-111">PARAMETERS</span></span>

### <span data-ttu-id="533f4-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="533f4-112">-ApplicationGateway</span></span>
<span data-ttu-id="533f4-113">이 cmdlet이 프런트 엔드 포트를 연결 하는 응용 프로그램 게이트웨이 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="533f4-113">Specifies the application gateway object with which this cmdlet associates the front-end port.</span></span>

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

### <span data-ttu-id="533f4-114">-이름</span><span class="sxs-lookup"><span data-stu-id="533f4-114">-Name</span></span>
<span data-ttu-id="533f4-115">수정할 프런트 엔드 포트의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="533f4-115">Specifies the name of the front-end port to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="533f4-116">-포트</span><span class="sxs-lookup"><span data-stu-id="533f4-116">-Port</span></span>
<span data-ttu-id="533f4-117">프런트 엔드 포트에 사용할 포트 번호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="533f4-117">Specifies the port number to use for the front-end port.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="533f4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="533f4-118">-DefaultProfile</span></span>
<span data-ttu-id="533f4-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="533f4-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="533f4-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="533f4-120">CommonParameters</span></span>
<span data-ttu-id="533f4-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="533f4-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="533f4-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="533f4-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="533f4-123">입력</span><span class="sxs-lookup"><span data-stu-id="533f4-123">INPUTS</span></span>

### <span data-ttu-id="533f4-124">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="533f4-124">PSApplicationGateway</span></span>
<span data-ttu-id="533f4-125">' ApplicationGateway ' 매개 변수는 파이프라인에서 ' PSApplicationGateway ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="533f4-125">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="533f4-126">출력</span><span class="sxs-lookup"><span data-stu-id="533f4-126">OUTPUTS</span></span>

### <span data-ttu-id="533f4-127">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="533f4-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="533f4-128">상속자</span><span class="sxs-lookup"><span data-stu-id="533f4-128">NOTES</span></span>

## <span data-ttu-id="533f4-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="533f4-129">RELATED LINKS</span></span>

[<span data-ttu-id="533f4-130">추가-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="533f4-130">Add-AzureRmApplicationGatewayFrontendPort</span></span>](./Add-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="533f4-131">Get-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="533f4-131">Get-AzureRmApplicationGatewayFrontendPort</span></span>](./Get-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="533f4-132">새로운 AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="533f4-132">New-AzureRmApplicationGatewayFrontendPort</span></span>](./New-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="533f4-133">제거-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="533f4-133">Remove-AzureRmApplicationGatewayFrontendPort</span></span>](./Remove-AzureRmApplicationGatewayFrontendPort.md)