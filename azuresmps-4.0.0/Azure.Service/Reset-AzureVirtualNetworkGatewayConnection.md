---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 09642B94-E888-4A22-9E8E-62109DB9394E
online version: ''
schema: 2.0.0
ms.openlocfilehash: f42a788f29f8546e6f402f1685f4c91aa3d7e5cb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046089"
---
# <span data-ttu-id="ec7c9-101">Reset-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="ec7c9-101">Reset-AzureVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="ec7c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec7c9-102">SYNOPSIS</span></span>
<span data-ttu-id="ec7c9-103">가상 네트워크 게이트웨이 연결을 다시 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec7c9-103">Resets a virtual network gateway connection.</span></span>

## <span data-ttu-id="ec7c9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ec7c9-104">SYNTAX</span></span>

```
Reset-AzureVirtualNetworkGatewayConnection -GatewayId <String> -ConnectedEntityId <String>
 -RoutingWeight <Int32> [-SharedKey <String>] [-EnableBgp <Boolean>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="ec7c9-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ec7c9-105">DESCRIPTION</span></span>
<span data-ttu-id="ec7c9-106">**AzureVirtualNetworkGatewayConnection** cmdlet은 가상 네트워크 게이트웨이 연결을 다시 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec7c9-106">The **Reset-AzureVirtualNetworkGatewayConnection** cmdlet resets a virtual network gateway connection.</span></span>

## <span data-ttu-id="ec7c9-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ec7c9-107">EXAMPLES</span></span>

## <span data-ttu-id="ec7c9-108">변수</span><span class="sxs-lookup"><span data-stu-id="ec7c9-108">PARAMETERS</span></span>

### <span data-ttu-id="ec7c9-109">-ConnectedEntityId</span><span class="sxs-lookup"><span data-stu-id="ec7c9-109">-ConnectedEntityId</span></span>
<span data-ttu-id="ec7c9-110">연결 된 엔터티의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec7c9-110">Specifies the ID of a connected entity.</span></span>

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

### <span data-ttu-id="ec7c9-111">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="ec7c9-111">-EnableBgp</span></span>
<span data-ttu-id="ec7c9-112">BGP (Border Gateway Protocol)를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec7c9-112">Enables Border Gateway Protocol (BGP).</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec7c9-113">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="ec7c9-113">-GatewayId</span></span>
<span data-ttu-id="ec7c9-114">게이트웨이의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec7c9-114">Specifies the ID of a gateway.</span></span>

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

### <span data-ttu-id="ec7c9-115">-프로필</span><span class="sxs-lookup"><span data-stu-id="ec7c9-115">-Profile</span></span>
<span data-ttu-id="ec7c9-116">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec7c9-116">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="ec7c9-117">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="ec7c9-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ec7c9-118">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="ec7c9-118">-RoutingWeight</span></span>
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec7c9-119">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="ec7c9-119">-SharedKey</span></span>
<span data-ttu-id="ec7c9-120">공유 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec7c9-120">Specifies a shared key.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec7c9-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec7c9-121">CommonParameters</span></span>
<span data-ttu-id="ec7c9-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec7c9-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec7c9-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec7c9-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec7c9-124">입력</span><span class="sxs-lookup"><span data-stu-id="ec7c9-124">INPUTS</span></span>

## <span data-ttu-id="ec7c9-125">출력</span><span class="sxs-lookup"><span data-stu-id="ec7c9-125">OUTPUTS</span></span>

## <span data-ttu-id="ec7c9-126">상속자</span><span class="sxs-lookup"><span data-stu-id="ec7c9-126">NOTES</span></span>

## <span data-ttu-id="ec7c9-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ec7c9-127">RELATED LINKS</span></span>

[<span data-ttu-id="ec7c9-128">Get-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="ec7c9-128">Get-AzureVirtualNetworkGatewayConnection</span></span>](./Get-AzureVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="ec7c9-129">새로운 AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="ec7c9-129">New-AzureVirtualNetworkGatewayConnection</span></span>](./New-AzureVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="ec7c9-130">제거-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="ec7c9-130">Remove-AzureVirtualNetworkGatewayConnection</span></span>](./Remove-AzureVirtualNetworkGatewayConnection.md)


