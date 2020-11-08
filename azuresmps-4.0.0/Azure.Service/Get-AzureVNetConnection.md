---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 7B749B29-9820-4E23-B5AF-F5535251629A
online version: ''
schema: 2.0.0
ms.openlocfilehash: ec94df29fb23dd7c82d79304c2e48aab225ed224
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046287"
---
# <span data-ttu-id="d24e0-101">Get-AzureVNetConnection</span><span class="sxs-lookup"><span data-stu-id="d24e0-101">Get-AzureVNetConnection</span></span>

## <span data-ttu-id="d24e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d24e0-102">SYNOPSIS</span></span>
<span data-ttu-id="d24e0-103">Azure 가상 네트워크에 대 한 연결을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d24e0-103">Gets connections to an Azure virtual network.</span></span>

## <span data-ttu-id="d24e0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d24e0-104">SYNTAX</span></span>

```
Get-AzureVNetConnection -VNetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d24e0-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d24e0-105">DESCRIPTION</span></span>
<span data-ttu-id="d24e0-106">**Get-AzureVNetConnection** Cmdlet은 Azure 가상 네트워크에 대 한 모든 활성 가상 개인 네트워크 (VPN) 연결을 지정 하는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="d24e0-106">The **Get-AzureVNetConnection** cmdlet returns an object that specifies all active virtual private network (VPN) connections to an Azure virtual network.</span></span>
<span data-ttu-id="d24e0-107">VPN 연결에는 교차 프레미스 사이트 간 Vpn 및 가상 네트워크 (가상 네트워크 연결)가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d24e0-107">VPN connections include cross premises site-to-site VPNs and virtual network to virtual network connections.</span></span>

## <span data-ttu-id="d24e0-108">예제의</span><span class="sxs-lookup"><span data-stu-id="d24e0-108">EXAMPLES</span></span>

## <span data-ttu-id="d24e0-109">변수</span><span class="sxs-lookup"><span data-stu-id="d24e0-109">PARAMETERS</span></span>

### <span data-ttu-id="d24e0-110">-프로필</span><span class="sxs-lookup"><span data-stu-id="d24e0-110">-Profile</span></span>
<span data-ttu-id="d24e0-111">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d24e0-111">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d24e0-112">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="d24e0-112">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d24e0-113">-VNetName</span><span class="sxs-lookup"><span data-stu-id="d24e0-113">-VNetName</span></span>
<span data-ttu-id="d24e0-114">이 cmdlet이 연결을 반환 하는 가상 네트워크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d24e0-114">Specifies the name of the virtual network from which this cmdlet returns connections.</span></span>

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

### <span data-ttu-id="d24e0-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d24e0-115">CommonParameters</span></span>
<span data-ttu-id="d24e0-116">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d24e0-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d24e0-117">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d24e0-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d24e0-118">입력</span><span class="sxs-lookup"><span data-stu-id="d24e0-118">INPUTS</span></span>

## <span data-ttu-id="d24e0-119">출력</span><span class="sxs-lookup"><span data-stu-id="d24e0-119">OUTPUTS</span></span>

## <span data-ttu-id="d24e0-120">상속자</span><span class="sxs-lookup"><span data-stu-id="d24e0-120">NOTES</span></span>

## <span data-ttu-id="d24e0-121">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d24e0-121">RELATED LINKS</span></span>

