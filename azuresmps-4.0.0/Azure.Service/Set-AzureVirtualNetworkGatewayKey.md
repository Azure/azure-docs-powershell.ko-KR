---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 8099942A-B6EB-4C01-9F57-378B0EB7B3C9
online version: ''
schema: 2.0.0
ms.openlocfilehash: 67c933b716095392a215543cfc61d334cd347835
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045437"
---
# <span data-ttu-id="3793f-101">Set-AzureVirtualNetworkGatewayKey</span><span class="sxs-lookup"><span data-stu-id="3793f-101">Set-AzureVirtualNetworkGatewayKey</span></span>

## <span data-ttu-id="3793f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3793f-102">SYNOPSIS</span></span>
<span data-ttu-id="3793f-103">Azure 가상 네트워크 게이트웨이의 키를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3793f-103">Sets the key for an Azure virtual network gateway.</span></span>

## <span data-ttu-id="3793f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3793f-104">SYNTAX</span></span>

```
Set-AzureVirtualNetworkGatewayKey -GatewayId <String> -ConnectedEntityId <String> -SharedKey <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3793f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="3793f-105">DESCRIPTION</span></span>
<span data-ttu-id="3793f-106">**AzureVirtualNetworkGatewayKey** Cmdlet은 Azure 가상 네트워크 게이트웨이의 키를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3793f-106">The **Set-AzureVirtualNetworkGatewayKey** cmdlet sets the key for an Azure virtual network gateway.</span></span>

## <span data-ttu-id="3793f-107">예제의</span><span class="sxs-lookup"><span data-stu-id="3793f-107">EXAMPLES</span></span>

## <span data-ttu-id="3793f-108">변수</span><span class="sxs-lookup"><span data-stu-id="3793f-108">PARAMETERS</span></span>

### <span data-ttu-id="3793f-109">-ConnectedEntityId</span><span class="sxs-lookup"><span data-stu-id="3793f-109">-ConnectedEntityId</span></span>
<span data-ttu-id="3793f-110">연결 된 엔터티의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3793f-110">Specifies the ID of a connected entity.</span></span>

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

### <span data-ttu-id="3793f-111">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="3793f-111">-GatewayId</span></span>
<span data-ttu-id="3793f-112">게이트웨이의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3793f-112">Specifies the ID of a gateway.</span></span>

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

### <span data-ttu-id="3793f-113">-프로필</span><span class="sxs-lookup"><span data-stu-id="3793f-113">-Profile</span></span>
<span data-ttu-id="3793f-114">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3793f-114">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="3793f-115">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="3793f-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3793f-116">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="3793f-116">-SharedKey</span></span>
<span data-ttu-id="3793f-117">공유 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3793f-117">Specifies a shared key.</span></span>

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

### <span data-ttu-id="3793f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3793f-118">CommonParameters</span></span>
<span data-ttu-id="3793f-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3793f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3793f-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3793f-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3793f-121">입력</span><span class="sxs-lookup"><span data-stu-id="3793f-121">INPUTS</span></span>

## <span data-ttu-id="3793f-122">출력</span><span class="sxs-lookup"><span data-stu-id="3793f-122">OUTPUTS</span></span>

## <span data-ttu-id="3793f-123">상속자</span><span class="sxs-lookup"><span data-stu-id="3793f-123">NOTES</span></span>

## <span data-ttu-id="3793f-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3793f-124">RELATED LINKS</span></span>

[<span data-ttu-id="3793f-125">Get-AzureVirtualNetworkGatewayKey</span><span class="sxs-lookup"><span data-stu-id="3793f-125">Get-AzureVirtualNetworkGatewayKey</span></span>](./Get-AzureVirtualNetworkGatewayKey.md)

[<span data-ttu-id="3793f-126">다시 설정-AzureVirtualNetworkGatewayKey</span><span class="sxs-lookup"><span data-stu-id="3793f-126">Reset-AzureVirtualNetworkGatewayKey</span></span>](./Reset-AzureVirtualNetworkGatewayKey.md)


