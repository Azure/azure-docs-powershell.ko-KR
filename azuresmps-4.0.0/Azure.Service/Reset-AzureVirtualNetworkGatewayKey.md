---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 4F1E69B8-15FB-495F-B910-04E450D3215F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8a5b53f909b840a761d40f79a311fb61b7e2337b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046088"
---
# <span data-ttu-id="e4690-101">Reset-AzureVirtualNetworkGatewayKey</span><span class="sxs-lookup"><span data-stu-id="e4690-101">Reset-AzureVirtualNetworkGatewayKey</span></span>

## <span data-ttu-id="e4690-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4690-102">SYNOPSIS</span></span>
<span data-ttu-id="e4690-103">가상 네트워크 게이트웨이 키를 다시 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4690-103">Resets a virtual network gateway key.</span></span>

## <span data-ttu-id="e4690-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e4690-104">SYNTAX</span></span>

```
Reset-AzureVirtualNetworkGatewayKey -GatewayId <String> -ConnectedEntityId <String> -keyLength <Int32>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e4690-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e4690-105">DESCRIPTION</span></span>
<span data-ttu-id="e4690-106">**AzureVirtualNetworkGatewayKey** cmdlet은 가상 네트워크 게이트웨이 키를 재설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4690-106">The **Reset-AzureVirtualNetworkGatewayKey** cmdlet resets a virtual network gateway key.</span></span>

## <span data-ttu-id="e4690-107">예제의</span><span class="sxs-lookup"><span data-stu-id="e4690-107">EXAMPLES</span></span>

## <span data-ttu-id="e4690-108">변수</span><span class="sxs-lookup"><span data-stu-id="e4690-108">PARAMETERS</span></span>

### <span data-ttu-id="e4690-109">-ConnectedEntityId</span><span class="sxs-lookup"><span data-stu-id="e4690-109">-ConnectedEntityId</span></span>
<span data-ttu-id="e4690-110">연결 된 엔터티의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4690-110">Specifies the ID of a connected entity.</span></span>

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

### <span data-ttu-id="e4690-111">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="e4690-111">-GatewayId</span></span>
<span data-ttu-id="e4690-112">게이트웨이의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4690-112">Specifies the ID of a gateway.</span></span>

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

### <span data-ttu-id="e4690-113">-keyLength</span><span class="sxs-lookup"><span data-stu-id="e4690-113">-keyLength</span></span>
<span data-ttu-id="e4690-114">키 길이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4690-114">Specifies the key length.</span></span>

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

### <span data-ttu-id="e4690-115">-프로필</span><span class="sxs-lookup"><span data-stu-id="e4690-115">-Profile</span></span>
<span data-ttu-id="e4690-116">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4690-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e4690-117">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="e4690-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e4690-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4690-118">CommonParameters</span></span>
<span data-ttu-id="e4690-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4690-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4690-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4690-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4690-121">입력</span><span class="sxs-lookup"><span data-stu-id="e4690-121">INPUTS</span></span>

## <span data-ttu-id="e4690-122">출력</span><span class="sxs-lookup"><span data-stu-id="e4690-122">OUTPUTS</span></span>

## <span data-ttu-id="e4690-123">상속자</span><span class="sxs-lookup"><span data-stu-id="e4690-123">NOTES</span></span>

## <span data-ttu-id="e4690-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e4690-124">RELATED LINKS</span></span>

[<span data-ttu-id="e4690-125">Get-AzureVirtualNetworkGatewayKey</span><span class="sxs-lookup"><span data-stu-id="e4690-125">Get-AzureVirtualNetworkGatewayKey</span></span>](./Get-AzureVirtualNetworkGatewayKey.md)

[<span data-ttu-id="e4690-126">Set-AzureVirtualNetworkGatewayKey</span><span class="sxs-lookup"><span data-stu-id="e4690-126">Set-AzureVirtualNetworkGatewayKey</span></span>](./Set-AzureVirtualNetworkGatewayKey.md)
