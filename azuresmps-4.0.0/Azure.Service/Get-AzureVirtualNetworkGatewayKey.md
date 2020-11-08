---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 5F016D72-80EB-462D-9646-25EC4E33293E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 485b29130fd4b54c378f3ec19389b6c24ba86c63
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046513"
---
# <span data-ttu-id="79629-101">Get-AzureVirtualNetworkGatewayKey</span><span class="sxs-lookup"><span data-stu-id="79629-101">Get-AzureVirtualNetworkGatewayKey</span></span>

## <span data-ttu-id="79629-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79629-102">SYNOPSIS</span></span>
<span data-ttu-id="79629-103">Azure 가상 네트워크 게이트웨이의 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="79629-103">Gets the key for an Azure virtual network gateway.</span></span>

## <span data-ttu-id="79629-104">구문과</span><span class="sxs-lookup"><span data-stu-id="79629-104">SYNTAX</span></span>

```
Get-AzureVirtualNetworkGatewayKey -GatewayId <String> -ConnectedEntityId <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="79629-105">설명은</span><span class="sxs-lookup"><span data-stu-id="79629-105">DESCRIPTION</span></span>
<span data-ttu-id="79629-106">**AzureVirtualNetworkGatewayKey** Cmdlet은 Azure 가상 네트워크 게이트웨이의 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="79629-106">The **Get-AzureVirtualNetworkGatewayKey** cmdlet gets the key for an Azure virtual network gateway.</span></span>

## <span data-ttu-id="79629-107">예제의</span><span class="sxs-lookup"><span data-stu-id="79629-107">EXAMPLES</span></span>

## <span data-ttu-id="79629-108">변수</span><span class="sxs-lookup"><span data-stu-id="79629-108">PARAMETERS</span></span>

### <span data-ttu-id="79629-109">-ConnectedEntityId</span><span class="sxs-lookup"><span data-stu-id="79629-109">-ConnectedEntityId</span></span>
<span data-ttu-id="79629-110">연결 된 엔터티의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="79629-110">Specifies the ID of a connected entity.</span></span>

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

### <span data-ttu-id="79629-111">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="79629-111">-GatewayId</span></span>
<span data-ttu-id="79629-112">게이트웨이의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="79629-112">Specifies the ID of a gateway.</span></span>

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

### <span data-ttu-id="79629-113">-프로필</span><span class="sxs-lookup"><span data-stu-id="79629-113">-Profile</span></span>
<span data-ttu-id="79629-114">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="79629-114">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="79629-115">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="79629-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="79629-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79629-116">CommonParameters</span></span>
<span data-ttu-id="79629-117">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="79629-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79629-118">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79629-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79629-119">입력</span><span class="sxs-lookup"><span data-stu-id="79629-119">INPUTS</span></span>

## <span data-ttu-id="79629-120">출력</span><span class="sxs-lookup"><span data-stu-id="79629-120">OUTPUTS</span></span>

## <span data-ttu-id="79629-121">상속자</span><span class="sxs-lookup"><span data-stu-id="79629-121">NOTES</span></span>

## <span data-ttu-id="79629-122">관련 링크</span><span class="sxs-lookup"><span data-stu-id="79629-122">RELATED LINKS</span></span>

[<span data-ttu-id="79629-123">다시 설정-AzureVirtualNetworkGatewayKey</span><span class="sxs-lookup"><span data-stu-id="79629-123">Reset-AzureVirtualNetworkGatewayKey</span></span>](./Reset-AzureVirtualNetworkGatewayKey.md)

[<span data-ttu-id="79629-124">Set-AzureVirtualNetworkGatewayKey</span><span class="sxs-lookup"><span data-stu-id="79629-124">Set-AzureVirtualNetworkGatewayKey</span></span>](./Set-AzureVirtualNetworkGatewayKey.md)


