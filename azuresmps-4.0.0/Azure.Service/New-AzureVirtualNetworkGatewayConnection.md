---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: E3C0C3AA-3941-469E-A6CC-A92ADD7377B4
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2bf6824219879af52549d7815d65dcb502a2a752
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046185"
---
# <span data-ttu-id="2302f-101">New-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="2302f-101">New-AzureVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="2302f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2302f-102">SYNOPSIS</span></span>
<span data-ttu-id="2302f-103">Azure 가상 게이트웨이 네트워크 연결을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2302f-103">Creates an Azure virtual gateway network connection.</span></span>

## <span data-ttu-id="2302f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2302f-104">SYNTAX</span></span>

```
New-AzureVirtualNetworkGatewayConnection -ConnectedEntityId <String> -GatewayConnectionName <String>
 -GatewayConnectionType <String> [-RoutingWeight <Int32>] [-SharedKey <String>]
 -VirtualNetworkGatewayId <String> [-EnableBgp <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="2302f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2302f-105">DESCRIPTION</span></span>
<span data-ttu-id="2302f-106">**AzureVirtualNetworkGatewayConnection** Cmdlet은 Azure virtual gateway 네트워크 연결을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2302f-106">The **New-AzureVirtualNetworkGatewayConnection** cmdlet creates an Azure virtual gateway network connection.</span></span>

## <span data-ttu-id="2302f-107">예제의</span><span class="sxs-lookup"><span data-stu-id="2302f-107">EXAMPLES</span></span>

## <span data-ttu-id="2302f-108">변수</span><span class="sxs-lookup"><span data-stu-id="2302f-108">PARAMETERS</span></span>

### <span data-ttu-id="2302f-109">-ConnectedEntityId</span><span class="sxs-lookup"><span data-stu-id="2302f-109">-ConnectedEntityId</span></span>
<span data-ttu-id="2302f-110">연결 된 엔터티의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2302f-110">Specifies the ID of a connected entity.</span></span>

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

### <span data-ttu-id="2302f-111">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="2302f-111">-EnableBgp</span></span>
<span data-ttu-id="2302f-112">BGP (Border Gateway Protocol)를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2302f-112">Enables Border Gateway Protocol (BGP).</span></span>

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

### <span data-ttu-id="2302f-113">-GatewayConnectionName</span><span class="sxs-lookup"><span data-stu-id="2302f-113">-GatewayConnectionName</span></span>
<span data-ttu-id="2302f-114">게이트웨이 연결의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2302f-114">Specifies a name for the gateway connection.</span></span>

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

### <span data-ttu-id="2302f-115">-게이트웨이 Connectiontype</span><span class="sxs-lookup"><span data-stu-id="2302f-115">-GatewayConnectionType</span></span>
<span data-ttu-id="2302f-116">게이트웨이 연결 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2302f-116">Specifies the type of gateway connection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2302f-117">-프로필</span><span class="sxs-lookup"><span data-stu-id="2302f-117">-Profile</span></span>
<span data-ttu-id="2302f-118">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2302f-118">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="2302f-119">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="2302f-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2302f-120">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="2302f-120">-RoutingWeight</span></span>
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2302f-121">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="2302f-121">-SharedKey</span></span>
<span data-ttu-id="2302f-122">공유 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2302f-122">Specifies a shared key.</span></span>

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

### <span data-ttu-id="2302f-123">-VirtualNetworkGatewayId</span><span class="sxs-lookup"><span data-stu-id="2302f-123">-VirtualNetworkGatewayId</span></span>
<span data-ttu-id="2302f-124">가상 네트워크 게이트웨이의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2302f-124">Specifies the ID of a virtual network gateway.</span></span>

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

### <span data-ttu-id="2302f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2302f-125">CommonParameters</span></span>
<span data-ttu-id="2302f-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2302f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2302f-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2302f-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2302f-128">입력</span><span class="sxs-lookup"><span data-stu-id="2302f-128">INPUTS</span></span>

## <span data-ttu-id="2302f-129">출력</span><span class="sxs-lookup"><span data-stu-id="2302f-129">OUTPUTS</span></span>

## <span data-ttu-id="2302f-130">상속자</span><span class="sxs-lookup"><span data-stu-id="2302f-130">NOTES</span></span>

## <span data-ttu-id="2302f-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2302f-131">RELATED LINKS</span></span>

[<span data-ttu-id="2302f-132">Get-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="2302f-132">Get-AzureVirtualNetworkGatewayConnection</span></span>](./Get-AzureVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="2302f-133">제거-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="2302f-133">Remove-AzureVirtualNetworkGatewayConnection</span></span>](./Remove-AzureVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="2302f-134">다시 설정-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="2302f-134">Reset-AzureVirtualNetworkGatewayConnection</span></span>](./Reset-AzureVirtualNetworkGatewayConnection.md)


