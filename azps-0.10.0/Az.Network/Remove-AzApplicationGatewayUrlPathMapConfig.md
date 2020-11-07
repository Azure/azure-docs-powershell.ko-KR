---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: E43C8D2A-A6B5-4259-94B9-353FBC15F5A8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 51428d44c2fc5ce29259924f71617317b163ac29
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875351"
---
# <span data-ttu-id="e8d8f-101">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="e8d8f-101">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="e8d8f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8d8f-102">SYNOPSIS</span></span>
<span data-ttu-id="e8d8f-103">백 엔드 서버 풀에 대 한 URL 경로 매핑을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8d8f-103">Removes URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="e8d8f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e8d8f-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayUrlPathMapConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e8d8f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e8d8f-105">DESCRIPTION</span></span>
<span data-ttu-id="e8d8f-106">**AzApplicationGatewayUrlPathMapConfig** cmdlet은 백 엔드 서버 풀에 대 한 URL 경로 매핑을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8d8f-106">The **Remove-AzApplicationGatewayUrlPathMapConfig** cmdlet removes URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="e8d8f-107">예제의</span><span class="sxs-lookup"><span data-stu-id="e8d8f-107">EXAMPLES</span></span>

### <span data-ttu-id="e8d8f-108">raid-1</span><span class="sxs-lookup"><span data-stu-id="e8d8f-108">1:</span></span>
```

```

## <span data-ttu-id="e8d8f-109">변수</span><span class="sxs-lookup"><span data-stu-id="e8d8f-109">PARAMETERS</span></span>

### <span data-ttu-id="e8d8f-110">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e8d8f-110">-ApplicationGateway</span></span>
<span data-ttu-id="e8d8f-111">이 cmdlet이 URL 경로 맵 구성을 제거할 응용 프로그램 게이트웨이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8d8f-111">Specifies the application gateway to which this cmdlet removes URL path map configuration.</span></span>

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

### <span data-ttu-id="e8d8f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8d8f-112">-DefaultProfile</span></span>
<span data-ttu-id="e8d8f-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e8d8f-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e8d8f-114">-이름</span><span class="sxs-lookup"><span data-stu-id="e8d8f-114">-Name</span></span>
<span data-ttu-id="e8d8f-115">이 cmdlet이 백 엔드 서버에서 제거 하는 URL 경로 맵 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8d8f-115">Specifies the URL path map name that this cmdlet removes from the backend server.</span></span>

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

### <span data-ttu-id="e8d8f-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8d8f-116">CommonParameters</span></span>
<span data-ttu-id="e8d8f-117">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8d8f-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8d8f-118">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8d8f-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8d8f-119">입력</span><span class="sxs-lookup"><span data-stu-id="e8d8f-119">INPUTS</span></span>

### <span data-ttu-id="e8d8f-120">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e8d8f-120">PSApplicationGateway</span></span>
<span data-ttu-id="e8d8f-121">' ApplicationGateway ' 매개 변수는 파이프라인에서 ' PSApplicationGateway ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8d8f-121">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="e8d8f-122">출력</span><span class="sxs-lookup"><span data-stu-id="e8d8f-122">OUTPUTS</span></span>

### <span data-ttu-id="e8d8f-123">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e8d8f-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e8d8f-124">상속자</span><span class="sxs-lookup"><span data-stu-id="e8d8f-124">NOTES</span></span>

## <span data-ttu-id="e8d8f-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e8d8f-125">RELATED LINKS</span></span>

[<span data-ttu-id="e8d8f-126">추가-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="e8d8f-126">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="e8d8f-127">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="e8d8f-127">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="e8d8f-128">새로운 AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="e8d8f-128">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="e8d8f-129">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="e8d8f-129">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


