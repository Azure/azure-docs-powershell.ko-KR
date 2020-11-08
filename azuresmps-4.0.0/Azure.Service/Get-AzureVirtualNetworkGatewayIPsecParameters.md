---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 425008DB-9761-42F1-8D6D-F35757A3CA6C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 37aa0718c4faa637b16ccde61f5e5b241bb9aa92
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046515"
---
# <span data-ttu-id="1a655-101">Get-AzureVirtualNetworkGatewayIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="1a655-101">Get-AzureVirtualNetworkGatewayIPsecParameters</span></span>

## <span data-ttu-id="1a655-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a655-102">SYNOPSIS</span></span>
<span data-ttu-id="1a655-103">Azure 가상 네트워크 게이트웨이에 대 한 IPsec 매개 변수를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1a655-103">Gets the IPsec parameters for an Azure virtual network gateway.</span></span>

## <span data-ttu-id="1a655-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1a655-104">SYNTAX</span></span>

```
Get-AzureVirtualNetworkGatewayIPsecParameters -GatewayId <String> -ConnectedEntityId <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="1a655-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1a655-105">DESCRIPTION</span></span>
<span data-ttu-id="1a655-106">**AzureVirtualNetworkGatewayIPsecParameters** Cmdlet은 Azure 가상 네트워크 게이트웨이에 대 한 IPsec 매개 변수를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1a655-106">The **Get-AzureVirtualNetworkGatewayIPsecParameters** cmdlet gets the IPsec parameters for an Azure virtual network gateway.</span></span>

## <span data-ttu-id="1a655-107">예제의</span><span class="sxs-lookup"><span data-stu-id="1a655-107">EXAMPLES</span></span>

## <span data-ttu-id="1a655-108">변수</span><span class="sxs-lookup"><span data-stu-id="1a655-108">PARAMETERS</span></span>

### <span data-ttu-id="1a655-109">-ConnectedEntityId</span><span class="sxs-lookup"><span data-stu-id="1a655-109">-ConnectedEntityId</span></span>
<span data-ttu-id="1a655-110">연결 된 enty의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a655-110">Specifies the ID of a connected entitiy.</span></span>

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

### <span data-ttu-id="1a655-111">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="1a655-111">-GatewayId</span></span>
<span data-ttu-id="1a655-112">게이트웨이의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a655-112">Specifies the ID of a gateway.</span></span>

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

### <span data-ttu-id="1a655-113">-프로필</span><span class="sxs-lookup"><span data-stu-id="1a655-113">-Profile</span></span>
<span data-ttu-id="1a655-114">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a655-114">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="1a655-115">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="1a655-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1a655-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a655-116">CommonParameters</span></span>
<span data-ttu-id="1a655-117">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a655-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a655-118">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a655-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a655-119">입력</span><span class="sxs-lookup"><span data-stu-id="1a655-119">INPUTS</span></span>

## <span data-ttu-id="1a655-120">출력</span><span class="sxs-lookup"><span data-stu-id="1a655-120">OUTPUTS</span></span>

## <span data-ttu-id="1a655-121">상속자</span><span class="sxs-lookup"><span data-stu-id="1a655-121">NOTES</span></span>

## <span data-ttu-id="1a655-122">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1a655-122">RELATED LINKS</span></span>

[<span data-ttu-id="1a655-123">Set-AzureVirtualNetworkGatewayIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="1a655-123">Set-AzureVirtualNetworkGatewayIPsecParameters</span></span>](./Set-AzureVirtualNetworkGatewayIPsecParameters.md)


