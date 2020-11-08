---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: B7E2561D-0FE8-4B34-9188-E89AA0B5C9DD
online version: ''
schema: 2.0.0
ms.openlocfilehash: dce79fc891018c3100140581e89639dbc76b543d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046276"
---
# <span data-ttu-id="a3e98-101">Get-AzureVNetGatewayIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="a3e98-101">Get-AzureVNetGatewayIPsecParameters</span></span>

## <span data-ttu-id="a3e98-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3e98-102">SYNOPSIS</span></span>
<span data-ttu-id="a3e98-103">가상 네트워크 게이트웨이와 로컬 네트워크 사이트 간 연결에 대 한 IPsec 매개 변수를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a3e98-103">Gets IPsec parameters for the connection between a virtual network gateway and a local network site.</span></span>

## <span data-ttu-id="a3e98-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a3e98-104">SYNTAX</span></span>

```
Get-AzureVNetGatewayIPsecParameters -VNetName <String> -LocalNetworkSiteName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="a3e98-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a3e98-105">DESCRIPTION</span></span>
<span data-ttu-id="a3e98-106">**Get-Azurevnet2| 매개 변수** cmdlet은 가상 네트워크 게이트웨이와 로컬 네트워크 사이트 간 연결에 대 한 현재 IPsec (인터넷 프로토콜 보안) 및 IKE (Internet Key Exchange) 매개 변수를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a3e98-106">The **Get-AzureVNetGatewayIPsecParameters** cmdlet gets current Internet Protocol security (IPsec) and Internet Key Exchange (IKE) parameters for the connection between a virtual network gateway and a local network site.</span></span>

## <span data-ttu-id="a3e98-107">예제의</span><span class="sxs-lookup"><span data-stu-id="a3e98-107">EXAMPLES</span></span>

## <span data-ttu-id="a3e98-108">변수</span><span class="sxs-lookup"><span data-stu-id="a3e98-108">PARAMETERS</span></span>

### <span data-ttu-id="a3e98-109">-LocalNetworkSiteName</span><span class="sxs-lookup"><span data-stu-id="a3e98-109">-LocalNetworkSiteName</span></span>
<span data-ttu-id="a3e98-110">가상 네트워크 게이트웨이에 연결 하는 로컬 네트워크 사이트의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3e98-110">Specifies the name of the local network site that connects to the virtual network gateway.</span></span>

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

### <span data-ttu-id="a3e98-111">-프로필</span><span class="sxs-lookup"><span data-stu-id="a3e98-111">-Profile</span></span>
<span data-ttu-id="a3e98-112">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3e98-112">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="a3e98-113">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="a3e98-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a3e98-114">-VNetName</span><span class="sxs-lookup"><span data-stu-id="a3e98-114">-VNetName</span></span>
<span data-ttu-id="a3e98-115">이 cmdlet이 연결에 대 한 IPsec 매개 변수를 가져오는 가상 네트워크를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3e98-115">Specifies the virtual network for which this cmdlet gets IPsec parameters for the connection.</span></span>

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

### <span data-ttu-id="a3e98-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3e98-116">CommonParameters</span></span>
<span data-ttu-id="a3e98-117">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3e98-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3e98-118">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3e98-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3e98-119">입력</span><span class="sxs-lookup"><span data-stu-id="a3e98-119">INPUTS</span></span>

## <span data-ttu-id="a3e98-120">출력</span><span class="sxs-lookup"><span data-stu-id="a3e98-120">OUTPUTS</span></span>

## <span data-ttu-id="a3e98-121">상속자</span><span class="sxs-lookup"><span data-stu-id="a3e98-121">NOTES</span></span>

## <span data-ttu-id="a3e98-122">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a3e98-122">RELATED LINKS</span></span>

[<span data-ttu-id="a3e98-123">Set-Azurevnet2| 매개 변수</span><span class="sxs-lookup"><span data-stu-id="a3e98-123">Set-AzureVNetGatewayIPsecParameters</span></span>](./Set-AzureVNetGatewayIPsecParameters.md)


