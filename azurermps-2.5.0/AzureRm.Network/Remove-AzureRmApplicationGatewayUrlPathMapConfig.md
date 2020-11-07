---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: E43C8D2A-A6B5-4259-94B9-353FBC15F5A8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayurlpathmapconfig
schema: 2.0.0
ms.openlocfilehash: a0885534311dfef4498c9fc71be7f82d16b05277
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93880969"
---
# <span data-ttu-id="81618-101">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="81618-101">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="81618-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="81618-102">SYNOPSIS</span></span>
<span data-ttu-id="81618-103">백 엔드 서버 풀에 대 한 URL 경로 매핑을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="81618-103">Removes URL path mappings to a backend server pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="81618-104">구문과</span><span class="sxs-lookup"><span data-stu-id="81618-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayUrlPathMapConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="81618-105">설명은</span><span class="sxs-lookup"><span data-stu-id="81618-105">DESCRIPTION</span></span>
<span data-ttu-id="81618-106">**AzureRmApplicationGatewayUrlPathMapConfig** cmdlet은 백 엔드 서버 풀에 대 한 URL 경로 매핑을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="81618-106">The **Remove-AzureRmApplicationGatewayUrlPathMapConfig** cmdlet removes URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="81618-107">예제의</span><span class="sxs-lookup"><span data-stu-id="81618-107">EXAMPLES</span></span>

### <span data-ttu-id="81618-108">raid-1</span><span class="sxs-lookup"><span data-stu-id="81618-108">1:</span></span>
```

```

## <span data-ttu-id="81618-109">변수</span><span class="sxs-lookup"><span data-stu-id="81618-109">PARAMETERS</span></span>

### <span data-ttu-id="81618-110">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="81618-110">-ApplicationGateway</span></span>
<span data-ttu-id="81618-111">이 cmdlet이 URL 경로 맵 구성을 제거할 응용 프로그램 게이트웨이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="81618-111">Specifies the application gateway to which this cmdlet removes URL path map configuration.</span></span>

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

### <span data-ttu-id="81618-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81618-112">-DefaultProfile</span></span>
<span data-ttu-id="81618-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="81618-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="81618-114">-이름</span><span class="sxs-lookup"><span data-stu-id="81618-114">-Name</span></span>
<span data-ttu-id="81618-115">이 cmdlet이 백 엔드 서버에서 제거 하는 URL 경로 맵 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="81618-115">Specifies the URL path map name that this cmdlet removes from the backend server.</span></span>

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

### <span data-ttu-id="81618-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81618-116">CommonParameters</span></span>
<span data-ttu-id="81618-117">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="81618-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81618-118">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81618-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81618-119">입력</span><span class="sxs-lookup"><span data-stu-id="81618-119">INPUTS</span></span>

### <span data-ttu-id="81618-120">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="81618-120">PSApplicationGateway</span></span>
<span data-ttu-id="81618-121">' ApplicationGateway ' 매개 변수는 파이프라인에서 ' PSApplicationGateway ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="81618-121">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="81618-122">출력</span><span class="sxs-lookup"><span data-stu-id="81618-122">OUTPUTS</span></span>

### <span data-ttu-id="81618-123">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="81618-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="81618-124">상속자</span><span class="sxs-lookup"><span data-stu-id="81618-124">NOTES</span></span>

## <span data-ttu-id="81618-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="81618-125">RELATED LINKS</span></span>

[<span data-ttu-id="81618-126">추가-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="81618-126">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="81618-127">Get-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="81618-127">Get-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="81618-128">새로운 AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="81618-128">New-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./New-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="81618-129">Set-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="81618-129">Set-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzureRmApplicationGatewayUrlPathMapConfig.md)


