---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: DF95285F-97F4-4064-8E27-EE6E93843E55
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0a14865c986bf6439df833a38f87835792a6e3c5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045626"
---
# <span data-ttu-id="0325b-101">Get-AzureRemoteAppVpnDevice</span><span class="sxs-lookup"><span data-stu-id="0325b-101">Get-AzureRemoteAppVpnDevice</span></span>

## <span data-ttu-id="0325b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0325b-102">SYNOPSIS</span></span>
<span data-ttu-id="0325b-103">VPN 장치에 대 한 정보를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="0325b-103">Retrieves information about a VPN device.</span></span>

## <span data-ttu-id="0325b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0325b-104">SYNTAX</span></span>

```
Get-AzureRemoteAppVpnDevice [-VNetName] <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="0325b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0325b-105">DESCRIPTION</span></span>
<span data-ttu-id="0325b-106">**AzureRemoteAppVpnDevice** cmdlet은 가상 개인 네트워크 (VPN) 장치에 대 한 정보를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="0325b-106">The **Get-AzureRemoteAppVpnDevice** cmdlet retrieves information about a virtual private network (VPN) device.</span></span>

## <span data-ttu-id="0325b-107">예제의</span><span class="sxs-lookup"><span data-stu-id="0325b-107">EXAMPLES</span></span>

### <span data-ttu-id="0325b-108">예제 1: 가상 네트워크에 사용할 수 있는 VPN 장치 구성 반환</span><span class="sxs-lookup"><span data-stu-id="0325b-108">Example 1: Return the available VPN device configurations for a virtual network</span></span>
```
PS C:\> Get-AzureRemoteVpnDevice -VNetName "ContosoVNet"


Name                   Platforms

----                   ---------

Cisco Systems, Inc.    {ASA 5500 Series Adaptive Security Appliances, ASR 1000 Series Aggregation Services Routers, ASR 1000 Series Aggregation Services Routers - Dynamic Routing, ISR Series Integrated Services Routers...} 

Juniper Networks, Inc. {SRX Series Routers, SRX Series Routers - Dynamic Routing, J Series Routers, J Series Routers - Dynamic Routing...} 

Microsoft Corporation  {RRAS}
```

<span data-ttu-id="0325b-109">이 명령은 지정 된 가상 네트워크에 대해 사용 가능한 VPN 장치 구성을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="0325b-109">This command returns the available VPN device configurations for the specified virtual network.</span></span>

## <span data-ttu-id="0325b-110">변수</span><span class="sxs-lookup"><span data-stu-id="0325b-110">PARAMETERS</span></span>

### <span data-ttu-id="0325b-111">-프로필</span><span class="sxs-lookup"><span data-stu-id="0325b-111">-Profile</span></span>
<span data-ttu-id="0325b-112">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0325b-112">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0325b-113">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="0325b-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0325b-114">-VNetName</span><span class="sxs-lookup"><span data-stu-id="0325b-114">-VNetName</span></span>
<span data-ttu-id="0325b-115">Azure RemoteApp 가상 네트워크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0325b-115">Specifies the name of the Azure RemoteApp virtual network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0325b-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0325b-116">CommonParameters</span></span>
<span data-ttu-id="0325b-117">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0325b-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0325b-118">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0325b-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0325b-119">입력</span><span class="sxs-lookup"><span data-stu-id="0325b-119">INPUTS</span></span>

## <span data-ttu-id="0325b-120">출력</span><span class="sxs-lookup"><span data-stu-id="0325b-120">OUTPUTS</span></span>

### <span data-ttu-id="0325b-121">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0325b-121">System.String</span></span>

## <span data-ttu-id="0325b-122">상속자</span><span class="sxs-lookup"><span data-stu-id="0325b-122">NOTES</span></span>

## <span data-ttu-id="0325b-123">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0325b-123">RELATED LINKS</span></span>

[<span data-ttu-id="0325b-124">Get-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="0325b-124">Get-AzureRemoteAppVNet</span></span>](./Get-AzureRemoteAppVNet.md)

[<span data-ttu-id="0325b-125">Get-AzureRemoteAppVpnDeviceConfigScript</span><span class="sxs-lookup"><span data-stu-id="0325b-125">Get-AzureRemoteAppVpnDeviceConfigScript</span></span>](./Get-AzureRemoteAppVpnDeviceConfigScript.md)


