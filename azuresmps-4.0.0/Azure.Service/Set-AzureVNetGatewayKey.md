---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 1AB168AA-F466-4C7C-9AD7-0BC7AEEBC932
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8daca2a335f063264fb2e6734948cc1353946e8a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045810"
---
# <span data-ttu-id="63fae-101">Set-AzureVNetGatewayKey</span><span class="sxs-lookup"><span data-stu-id="63fae-101">Set-AzureVNetGatewayKey</span></span>

## <span data-ttu-id="63fae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="63fae-102">SYNOPSIS</span></span>
<span data-ttu-id="63fae-103">Azure VPN 게이트웨이와 로컬 네트워크 사이트 간 연결에 미리 공유한 키를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="63fae-103">Sets the pre-shared key for the connection between an Azure VPN gateway and a local network site.</span></span>

## <span data-ttu-id="63fae-104">구문과</span><span class="sxs-lookup"><span data-stu-id="63fae-104">SYNTAX</span></span>

```
Set-AzureVNetGatewayKey -VNetName <String> -LocalNetworkSiteName <String> -SharedKey <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="63fae-105">설명은</span><span class="sxs-lookup"><span data-stu-id="63fae-105">DESCRIPTION</span></span>
<span data-ttu-id="63fae-106">**Set-Azurevnet네트워크 키** Cmdlet은 Azure VPN (가상 사설망) 게이트웨이 및 온-프레미스 로컬 네트워크 사이트 간 연결에 미리 공유한 키를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="63fae-106">The **Set-AzureVNetGatewayKey** cmdlet sets the pre-shared key for the connection between an Azure virtual private network (VPN) gateway and an on-premises local network site.</span></span>
<span data-ttu-id="63fae-107">키는 로컬 네트워크 사이트의 게이트웨이에서 구성 된 키와 동일 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="63fae-107">The key must be equal to the key configured on the gateway of the local network site.</span></span>
<span data-ttu-id="63fae-108">키가 일치 하지 않으면 연결을 설정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="63fae-108">If the keys do not match, a connection cannot establish.</span></span>

## <span data-ttu-id="63fae-109">예제의</span><span class="sxs-lookup"><span data-stu-id="63fae-109">EXAMPLES</span></span>

## <span data-ttu-id="63fae-110">변수</span><span class="sxs-lookup"><span data-stu-id="63fae-110">PARAMETERS</span></span>

### <span data-ttu-id="63fae-111">-LocalNetworkSiteName</span><span class="sxs-lookup"><span data-stu-id="63fae-111">-LocalNetworkSiteName</span></span>
<span data-ttu-id="63fae-112">가상 네트워크 게이트웨이에 연결 하는 로컬 네트워크 사이트의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="63fae-112">Specifies the name of the local network site that connects to the virtual network gateway.</span></span>

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

### <span data-ttu-id="63fae-113">-프로필</span><span class="sxs-lookup"><span data-stu-id="63fae-113">-Profile</span></span>
<span data-ttu-id="63fae-114">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="63fae-114">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="63fae-115">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="63fae-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="63fae-116">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="63fae-116">-SharedKey</span></span>
<span data-ttu-id="63fae-117">VPN 게이트웨이에 할당할 공유 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="63fae-117">Specifies the shared key to assign to the VPN gateway.</span></span>
<span data-ttu-id="63fae-118">값은 128 자를 넘지 않는 alpha 숫자 문자열 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="63fae-118">The value must be an alpha-numerical string no longer than 128 characters.</span></span>

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

### <span data-ttu-id="63fae-119">-VNetName</span><span class="sxs-lookup"><span data-stu-id="63fae-119">-VNetName</span></span>
<span data-ttu-id="63fae-120">이 cmdlet이 연결에 대 한 공유 키를 설정 하는 가상 네트워크를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="63fae-120">Specifies the virtual network for which this cmdlet sets the shared key for the connection.</span></span>

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

### <span data-ttu-id="63fae-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63fae-121">CommonParameters</span></span>
<span data-ttu-id="63fae-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="63fae-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63fae-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63fae-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63fae-124">입력</span><span class="sxs-lookup"><span data-stu-id="63fae-124">INPUTS</span></span>

## <span data-ttu-id="63fae-125">출력</span><span class="sxs-lookup"><span data-stu-id="63fae-125">OUTPUTS</span></span>

## <span data-ttu-id="63fae-126">상속자</span><span class="sxs-lookup"><span data-stu-id="63fae-126">NOTES</span></span>

## <span data-ttu-id="63fae-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="63fae-127">RELATED LINKS</span></span>

[<span data-ttu-id="63fae-128">Get-Azurevnet게이트웨이 키</span><span class="sxs-lookup"><span data-stu-id="63fae-128">Get-AzureVNetGatewayKey</span></span>](./Get-AzureVNetGatewayKey.md)


