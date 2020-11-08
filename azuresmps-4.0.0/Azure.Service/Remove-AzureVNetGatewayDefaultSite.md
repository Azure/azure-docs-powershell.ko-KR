---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 67260128-D57B-4587-BB61-2475703ABA66
online version: ''
schema: 2.0.0
ms.openlocfilehash: 38aca36799c57dd5a135af99e4b99ab713d2b1ca
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045489"
---
# <span data-ttu-id="91b76-101">Remove-AzureVNetGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="91b76-101">Remove-AzureVNetGatewayDefaultSite</span></span>

## <span data-ttu-id="91b76-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91b76-102">SYNOPSIS</span></span>
<span data-ttu-id="91b76-103">강제 터널링 트래픽에 대 한 기본 경로를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="91b76-103">Removes the default route for forced tunneling traffic.</span></span>

## <span data-ttu-id="91b76-104">구문과</span><span class="sxs-lookup"><span data-stu-id="91b76-104">SYNTAX</span></span>

```
Remove-AzureVNetGatewayDefaultSite -VNetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="91b76-105">설명은</span><span class="sxs-lookup"><span data-stu-id="91b76-105">DESCRIPTION</span></span>
<span data-ttu-id="91b76-106">**Remove-Azurevnet2| Defaultsite** cmdlet은 강제 터널링 트래픽을 위해 온-프레미스 사이트의 기본 경로를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="91b76-106">The **Remove-AzureVNetGatewayDefaultSite** cmdlet removes the default route to the on-premises site for forced tunneling traffic.</span></span>
<span data-ttu-id="91b76-107">이 cmdlet은 가상 네트워크의 Azure virtual 사설 네트워크 (VPN) 게이트웨이에서 경로를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="91b76-107">This cmdlet removes the route from an Azure virtual private network (VPN) gateway for a virtual network.</span></span>

## <span data-ttu-id="91b76-108">예제의</span><span class="sxs-lookup"><span data-stu-id="91b76-108">EXAMPLES</span></span>

### <span data-ttu-id="91b76-109">예제 1: 기본 사이트에 대 한 경로 제거</span><span class="sxs-lookup"><span data-stu-id="91b76-109">Example 1: Remove a route to the default site</span></span>
```
PS C:\> Remove-AzureVNetGatewayDefaultSite -VnetName "ContosoVNet01"
```

<span data-ttu-id="91b76-110">이 명령은 ContosoVNet01 이라는 가상 네트워크의 VPN에서 기본 사이트에 대 한 경로를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="91b76-110">This command removes the route to the default site from the VPN of the virtual network named ContosoVNet01.</span></span>

## <span data-ttu-id="91b76-111">변수</span><span class="sxs-lookup"><span data-stu-id="91b76-111">PARAMETERS</span></span>

### <span data-ttu-id="91b76-112">-프로필</span><span class="sxs-lookup"><span data-stu-id="91b76-112">-Profile</span></span>
<span data-ttu-id="91b76-113">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="91b76-113">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="91b76-114">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="91b76-114">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="91b76-115">-VNetName</span><span class="sxs-lookup"><span data-stu-id="91b76-115">-VNetName</span></span>
<span data-ttu-id="91b76-116">가상 네트워크를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="91b76-116">Specifies a virtual network.</span></span>
<span data-ttu-id="91b76-117">이 cmdlet은이 매개 변수에서 지정 하는 가상 네트워크의 VPN 게이트웨이에서 기본 경로를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="91b76-117">This cmdlet removes the default route from the VPN gateway for the virtual network that this parameter specifies.</span></span>

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

### <span data-ttu-id="91b76-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91b76-118">CommonParameters</span></span>
<span data-ttu-id="91b76-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="91b76-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91b76-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91b76-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91b76-121">입력</span><span class="sxs-lookup"><span data-stu-id="91b76-121">INPUTS</span></span>

## <span data-ttu-id="91b76-122">출력</span><span class="sxs-lookup"><span data-stu-id="91b76-122">OUTPUTS</span></span>

## <span data-ttu-id="91b76-123">상속자</span><span class="sxs-lookup"><span data-stu-id="91b76-123">NOTES</span></span>

## <span data-ttu-id="91b76-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="91b76-124">RELATED LINKS</span></span>

[<span data-ttu-id="91b76-125">Set-Azurevnet게이트웨이 Defaultsite</span><span class="sxs-lookup"><span data-stu-id="91b76-125">Set-AzureVNetGatewayDefaultSite</span></span>](./Set-AzureVNetGatewayDefaultSite.md)
