---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 70899AAC-BF64-4FFA-9DAF-92E859D0B271
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3b30172f947c1c8bf39a8be84039d9166d6ea290
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046414"
---
# <span data-ttu-id="e3041-101">Set-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="e3041-101">Set-AzureVNetGateway</span></span>

## <span data-ttu-id="e3041-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3041-102">SYNOPSIS</span></span>
<span data-ttu-id="e3041-103">Azure 가상 네트워크에 대 한 VPN 게이트웨이를 사용 하거나 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3041-103">Enables or disables a VPN gateway for an Azure virtual network.</span></span>

## <span data-ttu-id="e3041-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e3041-104">SYNTAX</span></span>

### <span data-ttu-id="e3041-105">연결 (기본값)</span><span class="sxs-lookup"><span data-stu-id="e3041-105">Connect (Default)</span></span>
```
Set-AzureVNetGateway [-Connect] -VNetName <String> -LocalNetworkSiteName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="e3041-106">끊고</span><span class="sxs-lookup"><span data-stu-id="e3041-106">Disconnect</span></span>
```
Set-AzureVNetGateway [-Disconnect] -VNetName <String> -LocalNetworkSiteName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e3041-107">설명은</span><span class="sxs-lookup"><span data-stu-id="e3041-107">DESCRIPTION</span></span>
<span data-ttu-id="e3041-108">**Set-AzureVNetGateway** Cmdlet은 Azure 가상 네트워크에 대 한 VPN (가상 사설망) 게이트웨이를 사용 하거나 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3041-108">The **Set-AzureVNetGateway** cmdlet enables or disables a virtual private network (VPN) gateway for an Azure virtual network.</span></span>
<span data-ttu-id="e3041-109">가상 네트워크 게이트웨이는 가상 네트워크에 연결 하기 위한 VPN 끝점입니다.</span><span class="sxs-lookup"><span data-stu-id="e3041-109">A virtual network gateway is a VPN endpoint for connecting to a virtual network.</span></span>
<span data-ttu-id="e3041-110">*연결* 또는 *연결 끊기* 매개 변수를 지정 하 여 온-프레미스 로컬 네트워크 사이트와 가상 네트워크 간의 VPN 연결을 사용 하거나 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3041-110">Specify the *Connect* or *Disconnect* parameter to enable or disable the VPN connection between an on-premises local network site and a virtual network.</span></span>

## <span data-ttu-id="e3041-111">예제의</span><span class="sxs-lookup"><span data-stu-id="e3041-111">EXAMPLES</span></span>

### <span data-ttu-id="e3041-112">예제 1: 가상 네트워크에 가상 네트워크 게이트웨이 사용</span><span class="sxs-lookup"><span data-stu-id="e3041-112">Example 1: Enable a virtual network gateway for a virtual network</span></span>
```
PS C:\> Set-AzureVNetGateway -Connect -VnetName "ContosoProdNet" -LocalNetworkSiteName "ContosoBranchOffice"
```

<span data-ttu-id="e3041-113">이 명령을 사용 하면 ContosoProdNet 이라는 Azure 가상 네트워크와 ContosoBranchOffice 라는 로컬 네트워크 사이트의 VPN 장치 간에 가상 네트워크 게이트웨이를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e3041-113">This command enables the virtual network gateway between the Azure virtual network named ContosoProdNet and the VPN device for the local network site named ContosoBranchOffice.</span></span>

### <span data-ttu-id="e3041-114">예제 2: 가상 네트워크에 대 한 가상 네트워크 게이트웨이 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="e3041-114">Example 2: Disable a virtual network gateway for a virtual network</span></span>
```
PS C:\> Set-AzureVNetGateway -Disconnect -VnetName "ContosoProdNet" -LocalNetworkSiteName "ContosoBranchOffice"
```

<span data-ttu-id="e3041-115">이 명령은 ContosoProdNet 이라는 Azure 가상 네트워크와 ContosoBranchOffice 라는 로컬 네트워크 사이트의 VPN 장치 간 가상 네트워크 게이트웨이를 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3041-115">This command disables the virtual network gateway between the Azure virtual network named ContosoProdNet and the VPN device for the local network site named ContosoBranchOffice.</span></span>

## <span data-ttu-id="e3041-116">변수</span><span class="sxs-lookup"><span data-stu-id="e3041-116">PARAMETERS</span></span>

### <span data-ttu-id="e3041-117">-연결</span><span class="sxs-lookup"><span data-stu-id="e3041-117">-Connect</span></span>
<span data-ttu-id="e3041-118">이 cmdlet이 가상 네트워크와 로컬 네트워크 사이트 간의 VPN 연결을 사용할 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="e3041-118">Indicates that this cmdlet enables the VPN connection between a virtual network and a local network site.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Connect
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3041-119">-연결 끊기</span><span class="sxs-lookup"><span data-stu-id="e3041-119">-Disconnect</span></span>
<span data-ttu-id="e3041-120">이 cmdlet이 가상 네트워크와 로컬 네트워크 사이트 간 VPN 연결을 사용 하지 않도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3041-120">Indicates that this cmdlet disables the VPN connection between a virtual network and a local network site.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Disconnect
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3041-121">-LocalNetworkSiteName</span><span class="sxs-lookup"><span data-stu-id="e3041-121">-LocalNetworkSiteName</span></span>
<span data-ttu-id="e3041-122">이 cmdlet이 VPN 연결을 사용 하거나 사용 하지 않도록 설정 하는 온-프레미스 로컬 네트워크 사이트의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3041-122">Specifies the name of the on-premises local network site for which this cmdlet enables or disables the VPN connection.</span></span>

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

### <span data-ttu-id="e3041-123">-프로필</span><span class="sxs-lookup"><span data-stu-id="e3041-123">-Profile</span></span>
<span data-ttu-id="e3041-124">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3041-124">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="e3041-125">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="e3041-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e3041-126">-VNetName</span><span class="sxs-lookup"><span data-stu-id="e3041-126">-VNetName</span></span>
<span data-ttu-id="e3041-127">이 cmdlet이 VPN 연결을 사용 하거나 사용 하지 않도록 설정 하는 가상 네트워크를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3041-127">Specifies the virtual network for which this cmdlet enables or disables the VPN connection.</span></span>

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

### <span data-ttu-id="e3041-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3041-128">CommonParameters</span></span>
<span data-ttu-id="e3041-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3041-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3041-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3041-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3041-131">입력</span><span class="sxs-lookup"><span data-stu-id="e3041-131">INPUTS</span></span>

## <span data-ttu-id="e3041-132">출력</span><span class="sxs-lookup"><span data-stu-id="e3041-132">OUTPUTS</span></span>

## <span data-ttu-id="e3041-133">상속자</span><span class="sxs-lookup"><span data-stu-id="e3041-133">NOTES</span></span>

## <span data-ttu-id="e3041-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e3041-134">RELATED LINKS</span></span>

[<span data-ttu-id="e3041-135">Get-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="e3041-135">Get-AzureVNetGateway</span></span>](./Get-AzureVNetGateway.md)

[<span data-ttu-id="e3041-136">새-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="e3041-136">New-AzureVNetGateway</span></span>](./New-AzureVNetGateway.md)

[<span data-ttu-id="e3041-137">-AzureVNetGateway 제거</span><span class="sxs-lookup"><span data-stu-id="e3041-137">Remove-AzureVNetGateway</span></span>](./Remove-AzureVNetGateway.md)

[<span data-ttu-id="e3041-138">Reset-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="e3041-138">Reset-AzureVNetGateway</span></span>](./Reset-AzureVNetGateway.md)

[<span data-ttu-id="e3041-139">크기 조정-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="e3041-139">Resize-AzureVNetGateway</span></span>](./Resize-AzureVNetGateway.md)


