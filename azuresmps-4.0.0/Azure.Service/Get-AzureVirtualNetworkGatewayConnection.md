---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 88AB3621-7C80-41BA-BE49-4F8F9C46BCF5
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1fb0fa13cb5ea155b945505fd3f99c28494c5dc0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046523"
---
# <span data-ttu-id="2ba28-101">Get-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="2ba28-101">Get-AzureVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="2ba28-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ba28-102">SYNOPSIS</span></span>
<span data-ttu-id="2ba28-103">가상 네트워크 게이트웨이 연결을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2ba28-103">Gets a virtual network gateway connection.</span></span>

## <span data-ttu-id="2ba28-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2ba28-104">SYNTAX</span></span>

```
Get-AzureVirtualNetworkGatewayConnection [-GatewayId <String>] [-ConnectedEntityId <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="2ba28-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2ba28-105">DESCRIPTION</span></span>
<span data-ttu-id="2ba28-106">**AzureVirtualNetworkGatewayConnection** Cmdlet은 Azure 가상 네트워크 게이트웨이 연결을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2ba28-106">The **Get-AzureVirtualNetworkGatewayConnection** cmdlet gets an Azure virtual network gateway connection.</span></span>

## <span data-ttu-id="2ba28-107">예제의</span><span class="sxs-lookup"><span data-stu-id="2ba28-107">EXAMPLES</span></span>

## <span data-ttu-id="2ba28-108">변수</span><span class="sxs-lookup"><span data-stu-id="2ba28-108">PARAMETERS</span></span>

### <span data-ttu-id="2ba28-109">-ConnectedEntityId</span><span class="sxs-lookup"><span data-stu-id="2ba28-109">-ConnectedEntityId</span></span>
<span data-ttu-id="2ba28-110">연결 된 엔터티의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ba28-110">Specifies the ID of a connected entity.</span></span>

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

### <span data-ttu-id="2ba28-111">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="2ba28-111">-GatewayId</span></span>
<span data-ttu-id="2ba28-112">게이트웨이의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ba28-112">Specifies the ID of the gateway.</span></span>

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

### <span data-ttu-id="2ba28-113">-프로필</span><span class="sxs-lookup"><span data-stu-id="2ba28-113">-Profile</span></span>
<span data-ttu-id="2ba28-114">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ba28-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2ba28-115">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="2ba28-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2ba28-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ba28-116">CommonParameters</span></span>
<span data-ttu-id="2ba28-117">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ba28-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ba28-118">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ba28-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ba28-119">입력</span><span class="sxs-lookup"><span data-stu-id="2ba28-119">INPUTS</span></span>

## <span data-ttu-id="2ba28-120">출력</span><span class="sxs-lookup"><span data-stu-id="2ba28-120">OUTPUTS</span></span>

## <span data-ttu-id="2ba28-121">상속자</span><span class="sxs-lookup"><span data-stu-id="2ba28-121">NOTES</span></span>

## <span data-ttu-id="2ba28-122">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2ba28-122">RELATED LINKS</span></span>

[<span data-ttu-id="2ba28-123">새로운 AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="2ba28-123">New-AzureVirtualNetworkGatewayConnection</span></span>](./New-AzureVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="2ba28-124">제거-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="2ba28-124">Remove-AzureVirtualNetworkGatewayConnection</span></span>](./Remove-AzureVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="2ba28-125">다시 설정-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="2ba28-125">Reset-AzureVirtualNetworkGatewayConnection</span></span>](./Reset-AzureVirtualNetworkGatewayConnection.md)
