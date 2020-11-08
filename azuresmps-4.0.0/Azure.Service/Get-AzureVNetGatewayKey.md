---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 8AD101BA-9275-4B2B-BB31-99FC34B8D1E8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1ac1d91bc084c9e1b17debf154b2a44c144ce312
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046275"
---
# <span data-ttu-id="d2463-101">Get-AzureVNetGatewayKey</span><span class="sxs-lookup"><span data-stu-id="d2463-101">Get-AzureVNetGatewayKey</span></span>

## <span data-ttu-id="d2463-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2463-102">SYNOPSIS</span></span>
<span data-ttu-id="d2463-103">가상 네트워크 게이트웨이와 로컬 네트워크 사이트 간 연결에 대 한 미리 공유한 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d2463-103">Gets the pre-shared key for the connection between a virtual network gateway and a local network site.</span></span>

## <span data-ttu-id="d2463-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d2463-104">SYNTAX</span></span>

```
Get-AzureVNetGatewayKey -VNetName <String> -LocalNetworkSiteName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="d2463-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d2463-105">DESCRIPTION</span></span>
<span data-ttu-id="d2463-106">**Get-Azurevnet2| 키** cmdlet은 가상 네트워크 게이트웨이와 로컬 네트워크 사이트 간 연결에 대 한 미리 공유한 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d2463-106">The **Get-AzureVNetGatewayKey** cmdlet gets the pre-shared key for the connection between a virtual network gateway and a local network site.</span></span>

## <span data-ttu-id="d2463-107">예제의</span><span class="sxs-lookup"><span data-stu-id="d2463-107">EXAMPLES</span></span>

## <span data-ttu-id="d2463-108">변수</span><span class="sxs-lookup"><span data-stu-id="d2463-108">PARAMETERS</span></span>

### <span data-ttu-id="d2463-109">-LocalNetworkSiteName</span><span class="sxs-lookup"><span data-stu-id="d2463-109">-LocalNetworkSiteName</span></span>
<span data-ttu-id="d2463-110">가상 네트워크 게이트웨이에 연결 하는 로컬 네트워크 사이트의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2463-110">Specifies the name of the local network site that connects to the virtual network gateway.</span></span>

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

### <span data-ttu-id="d2463-111">-프로필</span><span class="sxs-lookup"><span data-stu-id="d2463-111">-Profile</span></span>
<span data-ttu-id="d2463-112">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2463-112">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="d2463-113">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="d2463-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d2463-114">-VNetName</span><span class="sxs-lookup"><span data-stu-id="d2463-114">-VNetName</span></span>
<span data-ttu-id="d2463-115">이 cmdlet이 연결에 대 한 공유 키를 가져오는 가상 네트워크를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2463-115">Specifies the virtual network for which this cmdlet gets the shared key for connections.</span></span>

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

### <span data-ttu-id="d2463-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2463-116">CommonParameters</span></span>
<span data-ttu-id="d2463-117">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2463-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2463-118">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2463-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2463-119">입력</span><span class="sxs-lookup"><span data-stu-id="d2463-119">INPUTS</span></span>

## <span data-ttu-id="d2463-120">출력</span><span class="sxs-lookup"><span data-stu-id="d2463-120">OUTPUTS</span></span>

## <span data-ttu-id="d2463-121">상속자</span><span class="sxs-lookup"><span data-stu-id="d2463-121">NOTES</span></span>

## <span data-ttu-id="d2463-122">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d2463-122">RELATED LINKS</span></span>

[<span data-ttu-id="d2463-123">Set-Azurevnet2| Key</span><span class="sxs-lookup"><span data-stu-id="d2463-123">Set-AzureVNetGatewayKey</span></span>](./Set-AzureVNetGatewayKey.md)


