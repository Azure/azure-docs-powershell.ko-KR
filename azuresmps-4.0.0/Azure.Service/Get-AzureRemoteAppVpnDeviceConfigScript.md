---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: D0E8B2BD-D68F-477A-9D66-C27AB737960D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 59423aa3de5ae91abe82090054fac61f3901363c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045625"
---
# <span data-ttu-id="a2e85-101">Get-AzureRemoteAppVpnDeviceConfigScript</span><span class="sxs-lookup"><span data-stu-id="a2e85-101">Get-AzureRemoteAppVpnDeviceConfigScript</span></span>

## <span data-ttu-id="a2e85-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2e85-102">SYNOPSIS</span></span>
<span data-ttu-id="a2e85-103">Azure RemoteApp VPN 장치에 대 한 구성 스크립트를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2e85-103">Retrieves the configuration script for an Azure RemoteApp VPN device.</span></span>

## <span data-ttu-id="a2e85-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a2e85-104">SYNTAX</span></span>

```
Get-AzureRemoteAppVpnDeviceConfigScript [-VNetName] <String> [-Vendor] <String> [-Platform] <String>
 [-OSFamily] <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="a2e85-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a2e85-105">DESCRIPTION</span></span>
<span data-ttu-id="a2e85-106">**AzureRemoteAppVpnDeviceConfigScript** Cmdlet은 AZURE RemoteApp VPN (가상 사설망) 장치에 대 한 구성 스크립트를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2e85-106">The **Get-AzureRemoteAppVpnDeviceConfigScript** cmdlet retrieves the configuration script for an Azure RemoteApp virtual private network (VPN) device.</span></span>

## <span data-ttu-id="a2e85-107">예제의</span><span class="sxs-lookup"><span data-stu-id="a2e85-107">EXAMPLES</span></span>

### <span data-ttu-id="a2e85-108">예제 1: VPN 장치에 대 한 구성 스크립트 가져오기</span><span class="sxs-lookup"><span data-stu-id="a2e85-108">Example 1: Get a configuration script for a VPN device</span></span>
```
PS C:\> Get-AzureRemoteAppVpnDeviceConfigScript -VNetName "ContosoVNet" -Vendor "Microsoft Corporation" -OSFamily "Windows Server 2012 R2"
```

<span data-ttu-id="a2e85-109">이 명령은 ContosoVNet 이라는 가상 네트워크에 대 한 VPN 장치를 구성 하는 데 사용 되는 스크립트 또는 구성 파일을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2e85-109">This command returns the script or configuration file used to configure the VPN device for the virtual network named ContosoVNet.</span></span>
<span data-ttu-id="a2e85-110">해당 장치에 대 한 일반적인 방법으로이 스크립트나 구성 파일을 실행 하거나 VPN 장치에 로드 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2e85-110">This script or configuration file should be run or loaded onto the VPN device in the typical manner for that device.</span></span>
<span data-ttu-id="a2e85-111">각 장치에 대 한 고유한 요구 사항은 VPN 장치 공급 업체에 문의 하세요.</span><span class="sxs-lookup"><span data-stu-id="a2e85-111">Consult the VPN device vendor for the unique requirements for each device.</span></span>

## <span data-ttu-id="a2e85-112">변수</span><span class="sxs-lookup"><span data-stu-id="a2e85-112">PARAMETERS</span></span>

### <span data-ttu-id="a2e85-113">-OSFamily</span><span class="sxs-lookup"><span data-stu-id="a2e85-113">-OSFamily</span></span>
<span data-ttu-id="a2e85-114">디바이스 플랫폼에서 실행 되는 OS (운영 체제) 패밀리를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2e85-114">Specifies the operating system (OS) family that runs on the device platform.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a2e85-115">-플랫폼</span><span class="sxs-lookup"><span data-stu-id="a2e85-115">-Platform</span></span>
<span data-ttu-id="a2e85-116">디바이스 플랫폼을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2e85-116">Specifies the device platform.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a2e85-117">-프로필</span><span class="sxs-lookup"><span data-stu-id="a2e85-117">-Profile</span></span>
<span data-ttu-id="a2e85-118">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2e85-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a2e85-119">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="a2e85-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a2e85-120">-공급 업체</span><span class="sxs-lookup"><span data-stu-id="a2e85-120">-Vendor</span></span>
<span data-ttu-id="a2e85-121">VPN 장치의 공급 업체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2e85-121">Specifies the vendor of the VPN device.</span></span>

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

### <span data-ttu-id="a2e85-122">-VNetName</span><span class="sxs-lookup"><span data-stu-id="a2e85-122">-VNetName</span></span>
<span data-ttu-id="a2e85-123">Azure RemoteApp 가상 네트워크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2e85-123">Specifies the name of an Azure RemoteApp virtual network.</span></span>

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

### <span data-ttu-id="a2e85-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2e85-124">CommonParameters</span></span>
<span data-ttu-id="a2e85-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2e85-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2e85-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2e85-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2e85-127">입력</span><span class="sxs-lookup"><span data-stu-id="a2e85-127">INPUTS</span></span>

## <span data-ttu-id="a2e85-128">출력</span><span class="sxs-lookup"><span data-stu-id="a2e85-128">OUTPUTS</span></span>

## <span data-ttu-id="a2e85-129">상속자</span><span class="sxs-lookup"><span data-stu-id="a2e85-129">NOTES</span></span>

## <span data-ttu-id="a2e85-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a2e85-130">RELATED LINKS</span></span>

[<span data-ttu-id="a2e85-131">Get-AzureRemoteAppVpnDevice</span><span class="sxs-lookup"><span data-stu-id="a2e85-131">Get-AzureRemoteAppVpnDevice</span></span>](./Get-AzureRemoteAppVpnDevice.md)


