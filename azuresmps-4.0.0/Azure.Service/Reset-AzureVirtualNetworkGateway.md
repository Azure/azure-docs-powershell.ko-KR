---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: CD735391-62A8-40EC-B2F1-9044DC0676CA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1cc46fb250a7bc76d05193ea231c81d61668e853
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046090"
---
# <span data-ttu-id="80c08-101">Reset-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="80c08-101">Reset-AzureVirtualNetworkGateway</span></span>

## <span data-ttu-id="80c08-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80c08-102">SYNOPSIS</span></span>
<span data-ttu-id="80c08-103">가상 네트워크 게이트웨이를 다시 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="80c08-103">Resets a virtual network gateway.</span></span>

## <span data-ttu-id="80c08-104">구문과</span><span class="sxs-lookup"><span data-stu-id="80c08-104">SYNTAX</span></span>

```
Reset-AzureVirtualNetworkGateway -GatewayId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="80c08-105">설명은</span><span class="sxs-lookup"><span data-stu-id="80c08-105">DESCRIPTION</span></span>
<span data-ttu-id="80c08-106">**AzureVirtualNetworkGateway** cmdlet이 가상 네트워크 게이트웨이를 다시 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="80c08-106">The **Reset-AzureVirtualNetworkGateway** cmdlet resets a virtual network gateway.</span></span>

## <span data-ttu-id="80c08-107">예제의</span><span class="sxs-lookup"><span data-stu-id="80c08-107">EXAMPLES</span></span>

## <span data-ttu-id="80c08-108">변수</span><span class="sxs-lookup"><span data-stu-id="80c08-108">PARAMETERS</span></span>

### <span data-ttu-id="80c08-109">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="80c08-109">-GatewayId</span></span>
<span data-ttu-id="80c08-110">게이트웨이의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="80c08-110">Specifies the ID of a gateway.</span></span>

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

### <span data-ttu-id="80c08-111">-프로필</span><span class="sxs-lookup"><span data-stu-id="80c08-111">-Profile</span></span>
<span data-ttu-id="80c08-112">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="80c08-112">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="80c08-113">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="80c08-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80c08-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80c08-114">CommonParameters</span></span>
<span data-ttu-id="80c08-115">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="80c08-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80c08-116">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80c08-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80c08-117">입력</span><span class="sxs-lookup"><span data-stu-id="80c08-117">INPUTS</span></span>

## <span data-ttu-id="80c08-118">출력</span><span class="sxs-lookup"><span data-stu-id="80c08-118">OUTPUTS</span></span>

## <span data-ttu-id="80c08-119">상속자</span><span class="sxs-lookup"><span data-stu-id="80c08-119">NOTES</span></span>

## <span data-ttu-id="80c08-120">관련 링크</span><span class="sxs-lookup"><span data-stu-id="80c08-120">RELATED LINKS</span></span>

[<span data-ttu-id="80c08-121">Get-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="80c08-121">Get-AzureVirtualNetworkGateway</span></span>](./Get-AzureVirtualNetworkGateway.md)

[<span data-ttu-id="80c08-122">새로운 AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="80c08-122">New-AzureVirtualNetworkGateway</span></span>](./New-AzureVirtualNetworkGateway.md)

[<span data-ttu-id="80c08-123">제거-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="80c08-123">Remove-AzureVirtualNetworkGateway</span></span>](./Remove-AzureVirtualNetworkGateway.md)

[<span data-ttu-id="80c08-124">크기 조정-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="80c08-124">Resize-AzureVirtualNetworkGateway</span></span>](./Resize-AzureVirtualNetworkGateway.md)


