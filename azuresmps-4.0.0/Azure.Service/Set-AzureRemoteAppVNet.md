---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 97B96661-E60A-4505-AD06-D2A541DB820E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 19f7b09d26df88591e03acf8b01842efdead05e2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046052"
---
# <span data-ttu-id="c81f3-101">Set-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="c81f3-101">Set-AzureRemoteAppVNet</span></span>

## <span data-ttu-id="c81f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c81f3-102">SYNOPSIS</span></span>
<span data-ttu-id="c81f3-103">Azure RemoteApp 가상 네트워크의 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c81f3-103">Sets the properties of an Azure RemoteApp virtual network.</span></span>

## <span data-ttu-id="c81f3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c81f3-104">SYNTAX</span></span>

```
Set-AzureRemoteAppVNet -VNetName <String> [-VirtualNetworkAddressSpace <String[]>]
 [-LocalNetworkAddressSpace <String[]>] [-DnsServerIpAddress <String[]>] [-VpnDeviceIpAddress <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c81f3-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c81f3-105">DESCRIPTION</span></span>
<span data-ttu-id="c81f3-106">**Set-AzureRemoteAppVNet** Cmdlet은 Azure RemoteApp 가상 네트워크의 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c81f3-106">The **Set-AzureRemoteAppVNet** cmdlet sets the properties of an Azure RemoteApp virtual network.</span></span>

## <span data-ttu-id="c81f3-107">예제의</span><span class="sxs-lookup"><span data-stu-id="c81f3-107">EXAMPLES</span></span>

### <span data-ttu-id="c81f3-108">예제 1: 가상 네트워크의 속성 설정</span><span class="sxs-lookup"><span data-stu-id="c81f3-108">Example 1: Set the properties of a virtual network</span></span>
```
PS C:\> Set-AzureRemoteAppVnet -VNetName "ContosoVNet" -DnsServerIpAddress "131.253.33.200" -LocalNetworkAddressSpace "192.168.0.0/24" -VirtualNetworkAddressSpace "10.10.0.0/24" -VpnDeviceIpAddress "131.253.33.200"
```

<span data-ttu-id="c81f3-109">이 명령은 ContosoVNet 이라는 가상 네트워크의 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c81f3-109">This command sets the properties of a virtual network named ContosoVNet.</span></span>

## <span data-ttu-id="c81f3-110">변수</span><span class="sxs-lookup"><span data-stu-id="c81f3-110">PARAMETERS</span></span>

### <span data-ttu-id="c81f3-111">-DnsServerIpAddress</span><span class="sxs-lookup"><span data-stu-id="c81f3-111">-DnsServerIpAddress</span></span>
<span data-ttu-id="c81f3-112">DNS 서버의 IPv4 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c81f3-112">Specifies the IPv4 addresses of the DNS servers.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c81f3-113">-LocalNetworkAddressSpace</span><span class="sxs-lookup"><span data-stu-id="c81f3-113">-LocalNetworkAddressSpace</span></span>
<span data-ttu-id="c81f3-114">CIDR (클래스 Inter-Domain Routing) 표기법에서 로컬 네트워크 주소 공간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c81f3-114">Specifies the local network address space, in Classes Inter-Domain Routing (CIDR) notation.</span></span>
<span data-ttu-id="c81f3-115">이는 가상 네트워크 주소 공간과 겹치지 않아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c81f3-115">This must not overlap the virtual network address space.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c81f3-116">-프로필</span><span class="sxs-lookup"><span data-stu-id="c81f3-116">-Profile</span></span>
<span data-ttu-id="c81f3-117">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c81f3-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c81f3-118">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="c81f3-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c81f3-119">-VirtualNetworkAddressSpace</span><span class="sxs-lookup"><span data-stu-id="c81f3-119">-VirtualNetworkAddressSpace</span></span>
<span data-ttu-id="c81f3-120">CIDR 표기법으로 가상 네트워크 주소 공간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c81f3-120">Specifies the virtual network address space in CIDR notation.</span></span>
<span data-ttu-id="c81f3-121">이것은 개인 IP 주소 범위에 있어야 하며 로컬 네트워크 주소 공간과 겹칠 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="c81f3-121">This must be in the private IP address range and cannot overlap the local network address space.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c81f3-122">-VNetName</span><span class="sxs-lookup"><span data-stu-id="c81f3-122">-VNetName</span></span>
<span data-ttu-id="c81f3-123">Azure RemoteApp 가상 네트워크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c81f3-123">Specifies the name of the Azure RemoteApp virtual network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c81f3-124">-VpnDeviceIpAddress</span><span class="sxs-lookup"><span data-stu-id="c81f3-124">-VpnDeviceIpAddress</span></span>
<span data-ttu-id="c81f3-125">VPN (가상 개인 네트워크) 장치의 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c81f3-125">Specifies the address of the Virtual Private Network (VPN) device.</span></span>
<span data-ttu-id="c81f3-126">이것은 공공 주소 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c81f3-126">This must be a public-facing address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c81f3-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c81f3-127">CommonParameters</span></span>
<span data-ttu-id="c81f3-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c81f3-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c81f3-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c81f3-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c81f3-130">입력</span><span class="sxs-lookup"><span data-stu-id="c81f3-130">INPUTS</span></span>

## <span data-ttu-id="c81f3-131">출력</span><span class="sxs-lookup"><span data-stu-id="c81f3-131">OUTPUTS</span></span>

## <span data-ttu-id="c81f3-132">상속자</span><span class="sxs-lookup"><span data-stu-id="c81f3-132">NOTES</span></span>

## <span data-ttu-id="c81f3-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c81f3-133">RELATED LINKS</span></span>

[<span data-ttu-id="c81f3-134">Get-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="c81f3-134">Get-AzureRemoteAppVNet</span></span>](./Get-AzureRemoteAppVNet.md)


