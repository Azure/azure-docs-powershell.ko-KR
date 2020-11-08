---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: B6881AEC-7DFD-43F8-92A9-7AB56323B86F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 36476b34f74c44facf84ba2246afd0b6d8e49007
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045994"
---
# <span data-ttu-id="f3f8c-101">New-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="f3f8c-101">New-AzureRemoteAppVNet</span></span>

## <span data-ttu-id="f3f8c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3f8c-102">SYNOPSIS</span></span>
<span data-ttu-id="f3f8c-103">Azure RemoteApp 가상 네트워크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f3f8c-103">Creates an Azure RemoteApp virtual network.</span></span>

## <span data-ttu-id="f3f8c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f3f8c-104">SYNTAX</span></span>

```
New-AzureRemoteAppVNet -VNetName <String> -VirtualNetworkAddressSpace <String[]>
 -LocalNetworkAddressSpace <String[]> -DnsServerIpAddress <String[]> -VpnDeviceIpAddress <String>
 [-Location] <String> -GatewayType <GatewayType> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="f3f8c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f3f8c-105">DESCRIPTION</span></span>
<span data-ttu-id="f3f8c-106">**새 AzureRemoteAppVNet** Cmdlet은 Azure RemoteApp 가상 네트워크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f3f8c-106">The **New-AzureRemoteAppVNet** cmdlet creates an Azure RemoteApp virtual network.</span></span>

## <span data-ttu-id="f3f8c-107">예제의</span><span class="sxs-lookup"><span data-stu-id="f3f8c-107">EXAMPLES</span></span>

### <span data-ttu-id="f3f8c-108">예제 1: 가상 네트워크 만들기</span><span class="sxs-lookup"><span data-stu-id="f3f8c-108">Example 1: Create a virtual network</span></span>
```
PS C:\> New-AzureRemoteAppVnet -VNetName "ContosoVNet" -DnsServerIpAddress "192.168.0.5" -LocalNetworkAddressSpace "192.168.0.0/24" -Location "Central US" -VirtualNetworkAddressSpace "10.10.0.0/24" -VpnDeviceIpAddress "131.107.33.200" -GatewayType StaticRouting

TrackingId

----------

b0ca9d1b-d1b9-4f24-9a08-5e021926587f
```

<span data-ttu-id="f3f8c-109">이 명령은 ContosoVNet 이라는 가상 네트워크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f3f8c-109">This command creates a virtual network named ContosoVNet.</span></span>

<span data-ttu-id="f3f8c-110">작업의 상태를 확인 하려면이 cmdlet이 반환 하는 추적 ID와 함께 **AzureRemoteAppOperationResult** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3f8c-110">To determine the status of the operation, use the **Get-AzureRemoteAppOperationResult** cmdlet with the tracking ID that this cmdlet returns.</span></span>

## <span data-ttu-id="f3f8c-111">변수</span><span class="sxs-lookup"><span data-stu-id="f3f8c-111">PARAMETERS</span></span>

### <span data-ttu-id="f3f8c-112">-DnsServerIpAddress</span><span class="sxs-lookup"><span data-stu-id="f3f8c-112">-DnsServerIpAddress</span></span>
<span data-ttu-id="f3f8c-113">DNS 서버의 IPv4 주소 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3f8c-113">Specifies an array of the IPv4 addresses of the DNS servers.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f3f8c-114">-게이트웨이 종류</span><span class="sxs-lookup"><span data-stu-id="f3f8c-114">-GatewayType</span></span>
<span data-ttu-id="f3f8c-115">사용할 게이트웨이 라우팅 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3f8c-115">Specifies the type of gateway routing to use.</span></span>
<span data-ttu-id="f3f8c-116">이 매개 변수에 허용 되는 값은 StaticRouting 또는 DynamicRouting.</span><span class="sxs-lookup"><span data-stu-id="f3f8c-116">The acceptable values for this parameter are:  StaticRouting or DynamicRouting.</span></span>

```yaml
Type: GatewayType
Parameter Sets: (All)
Aliases: 
Accepted values: StaticRouting, DynamicRouting

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f3f8c-117">-LocalNetworkAddressSpace</span><span class="sxs-lookup"><span data-stu-id="f3f8c-117">-LocalNetworkAddressSpace</span></span>
<span data-ttu-id="f3f8c-118">CIDR (클래스 없는 도메인간 라우팅) 표기법으로 로컬 네트워크 주소 공간을 지정 하는 문자열의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3f8c-118">Specifies an array of strings that specify the local network address space, in Classless Interdomain Routing (CIDR) notation.</span></span>
<span data-ttu-id="f3f8c-119">이 주소 공간은 *VirtualNetworkAddressSpace* 매개 변수에서 지정 하는 가상 네트워크 주소 공간과 중복 되 면 안 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f3f8c-119">This address space must not overlap with the virtual network address space that the *VirtualNetworkAddressSpace* parameter specifies.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f3f8c-120">-위치</span><span class="sxs-lookup"><span data-stu-id="f3f8c-120">-Location</span></span>
<span data-ttu-id="f3f8c-121">가상 네트워크를 만들 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3f8c-121">Specifies the location in which to create the virtual network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f3f8c-122">-프로필</span><span class="sxs-lookup"><span data-stu-id="f3f8c-122">-Profile</span></span>
<span data-ttu-id="f3f8c-123">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3f8c-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f3f8c-124">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="f3f8c-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f3f8c-125">-VirtualNetworkAddressSpace</span><span class="sxs-lookup"><span data-stu-id="f3f8c-125">-VirtualNetworkAddressSpace</span></span>
<span data-ttu-id="f3f8c-126">CIDR 표기법으로 가상 네트워크 주소 공간을 지정 하는 문자열 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3f8c-126">Specifies an array of string that specify the virtual network address space in CIDR notation.</span></span>
<span data-ttu-id="f3f8c-127">이것은 개인 IP 주소 범위에 있어야 하며, *LocalNetworkAddressSpace* 매개 변수에서 지정 하는 로컬 네트워크 주소 공간과 중복 될 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="f3f8c-127">This must be in the private IP address range and cannot overlap with the local network address space that the *LocalNetworkAddressSpace* parameter specifies.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f3f8c-128">-VNetName</span><span class="sxs-lookup"><span data-stu-id="f3f8c-128">-VNetName</span></span>
<span data-ttu-id="f3f8c-129">Azure RemoteApp 가상 네트워크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3f8c-129">Specifies the name of the Azure RemoteApp virtual network.</span></span>

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

### <span data-ttu-id="f3f8c-130">-VpnDeviceIpAddress</span><span class="sxs-lookup"><span data-stu-id="f3f8c-130">-VpnDeviceIpAddress</span></span>
<span data-ttu-id="f3f8c-131">VPN (가상 개인 네트워크) 장치의 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3f8c-131">Specifies the address of the virtual private network (VPN) device.</span></span>
<span data-ttu-id="f3f8c-132">이것은 공공 주소 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3f8c-132">This must be a public-facing address.</span></span>

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

### <span data-ttu-id="f3f8c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3f8c-133">CommonParameters</span></span>
<span data-ttu-id="f3f8c-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3f8c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3f8c-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3f8c-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3f8c-136">입력</span><span class="sxs-lookup"><span data-stu-id="f3f8c-136">INPUTS</span></span>

## <span data-ttu-id="f3f8c-137">출력</span><span class="sxs-lookup"><span data-stu-id="f3f8c-137">OUTPUTS</span></span>

## <span data-ttu-id="f3f8c-138">상속자</span><span class="sxs-lookup"><span data-stu-id="f3f8c-138">NOTES</span></span>

## <span data-ttu-id="f3f8c-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f3f8c-139">RELATED LINKS</span></span>

[<span data-ttu-id="f3f8c-140">Get-AzureRemoteAppOperationResult</span><span class="sxs-lookup"><span data-stu-id="f3f8c-140">Get-AzureRemoteAppOperationResult</span></span>](./Get-AzureRemoteAppOperationResult.md)

[<span data-ttu-id="f3f8c-141">Get-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="f3f8c-141">Get-AzureRemoteAppVNet</span></span>](./Get-AzureRemoteAppVNet.md)

[<span data-ttu-id="f3f8c-142">제거-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="f3f8c-142">Remove-AzureRemoteAppVNet</span></span>](./Remove-AzureRemoteAppVNet.md)

[<span data-ttu-id="f3f8c-143">Set-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="f3f8c-143">Set-AzureRemoteAppVNet</span></span>](./Set-AzureRemoteAppVNet.md)


