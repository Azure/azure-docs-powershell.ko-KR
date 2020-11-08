---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: A34A2B01-A658-410E-8B68-98A6427DFC33
online version: ''
schema: 2.0.0
ms.openlocfilehash: 345d9048ea729b6fe954d2da5e01310be42c79ef
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046413"
---
# <span data-ttu-id="1bb15-101">Set-AzureVNetGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="1bb15-101">Set-AzureVNetGatewayDefaultSite</span></span>

## <span data-ttu-id="1bb15-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1bb15-102">SYNOPSIS</span></span>
<span data-ttu-id="1bb15-103">강제 터널링 트래픽에 대 한 기본 사이트를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1bb15-103">Sets the default site for forced tunneling traffic.</span></span>

## <span data-ttu-id="1bb15-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1bb15-104">SYNTAX</span></span>

```
Set-AzureVNetGatewayDefaultSite -VNetName <String> -DefaultSite <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="1bb15-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1bb15-105">DESCRIPTION</span></span>
<span data-ttu-id="1bb15-106">**Set-Azurevnet2| Defaultsite** cmdlet은 강제 터널링 트래픽을 위해 온-프레미스 사이트의 기본 경로를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1bb15-106">The **Set-AzureVNetGatewayDefaultSite** cmdlet sets the default route to the on-premises site for forced tunneling traffic.</span></span>
<span data-ttu-id="1bb15-107">이 명령은 가상 네트워크에 대 한 Azure VPN (가상 사설망) 게이트웨이에서 경로를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1bb15-107">This command sets the route on an Azure virtual private network (VPN) gateway for a virtual network.</span></span>

## <span data-ttu-id="1bb15-108">예제의</span><span class="sxs-lookup"><span data-stu-id="1bb15-108">EXAMPLES</span></span>

## <span data-ttu-id="1bb15-109">변수</span><span class="sxs-lookup"><span data-stu-id="1bb15-109">PARAMETERS</span></span>

### <span data-ttu-id="1bb15-110">-DefaultSite</span><span class="sxs-lookup"><span data-stu-id="1bb15-110">-DefaultSite</span></span>
<span data-ttu-id="1bb15-111">강제 터널링 트래픽에 대 한 온-프레미스 로컬 네트워크 사이트의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1bb15-111">Specifies the name of the on-premises local network site for forced tunneling traffic.</span></span>

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

### <span data-ttu-id="1bb15-112">-프로필</span><span class="sxs-lookup"><span data-stu-id="1bb15-112">-Profile</span></span>
<span data-ttu-id="1bb15-113">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1bb15-113">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1bb15-114">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="1bb15-114">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1bb15-115">-VNetName</span><span class="sxs-lookup"><span data-stu-id="1bb15-115">-VNetName</span></span>
<span data-ttu-id="1bb15-116">가상 네트워크를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1bb15-116">Specifies a virtual network.</span></span>
<span data-ttu-id="1bb15-117">이 cmdlet은이 매개 변수에서 지정 하는 가상 네트워크의 강제 터널링 트래픽에 대 한 VPN 게이트웨이의 기본 경로를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1bb15-117">This cmdlet sets the default route of the VPN gateway for forced tunneling traffic for the virtual network that this parameter specifies.</span></span>

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

### <span data-ttu-id="1bb15-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bb15-118">CommonParameters</span></span>
<span data-ttu-id="1bb15-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1bb15-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bb15-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1bb15-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bb15-121">입력</span><span class="sxs-lookup"><span data-stu-id="1bb15-121">INPUTS</span></span>

## <span data-ttu-id="1bb15-122">출력</span><span class="sxs-lookup"><span data-stu-id="1bb15-122">OUTPUTS</span></span>

## <span data-ttu-id="1bb15-123">상속자</span><span class="sxs-lookup"><span data-stu-id="1bb15-123">NOTES</span></span>

## <span data-ttu-id="1bb15-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1bb15-124">RELATED LINKS</span></span>

[<span data-ttu-id="1bb15-125">제거-Azurevnet2| Defaultsite</span><span class="sxs-lookup"><span data-stu-id="1bb15-125">Remove-AzureVNetGatewayDefaultSite</span></span>](./Remove-AzureVNetGatewayDefaultSite.md)
