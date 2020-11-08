---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 4522E93F-6AC9-4A37-88B8-CCCCE15A5879
online version: ''
schema: 2.0.0
ms.openlocfilehash: fcfc41e06f6847612c275817560e8593b76f6bac
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045471"
---
# <span data-ttu-id="02517-101">Reset-AzureRemoteAppVpnSharedKey</span><span class="sxs-lookup"><span data-stu-id="02517-101">Reset-AzureRemoteAppVpnSharedKey</span></span>

## <span data-ttu-id="02517-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02517-102">SYNOPSIS</span></span>
<span data-ttu-id="02517-103">Azure RemoteApp VPN 공유 키를 다시 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="02517-103">Resets the Azure RemoteApp VPN shared key.</span></span>

## <span data-ttu-id="02517-104">구문과</span><span class="sxs-lookup"><span data-stu-id="02517-104">SYNTAX</span></span>

```
Reset-AzureRemoteAppVpnSharedKey [-VNetName] <String> [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="02517-105">설명은</span><span class="sxs-lookup"><span data-stu-id="02517-105">DESCRIPTION</span></span>
<span data-ttu-id="02517-106">**AzureRemoteAppVpnSharedKey** Cmdlet은 AZURE RemoteApp VPN (가상 사설망) 공유 키를 초기화 합니다.</span><span class="sxs-lookup"><span data-stu-id="02517-106">The **Reset-AzureRemoteAppVpnSharedKey** cmdlet resets the Azure RemoteApp virtual private network (VPN) shared key.</span></span>

## <span data-ttu-id="02517-107">예제의</span><span class="sxs-lookup"><span data-stu-id="02517-107">EXAMPLES</span></span>

### <span data-ttu-id="02517-108">예제 1: 가상 네트워크에서 공유 키 다시 설정</span><span class="sxs-lookup"><span data-stu-id="02517-108">Example 1: Reset the shared key on a virtual network</span></span>
```
PS C:\> Reset-AzureRemoteAppVpnSharedKey -VNetName "ContosoVNet"
```

<span data-ttu-id="02517-109">이 명령은 ContosoVNet 이라는 가상 네트워크에서 공유 키를 다시 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="02517-109">This command resets the shared key on the virtual network named ContosoVNet.</span></span>
<span data-ttu-id="02517-110">새 공유 키가 VPN 장치에서 구성 될 때까지 온-프레미스 네트워크에 대 한 VPN 연결이 오프 라인 상태로 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="02517-110">The VPN connection to the on-premises network remains offline until the new shared key is configured on the VPN device.</span></span>
<span data-ttu-id="02517-111">VPN 장치를 구성 하려면 **AzureRemoteAppVpnDeviceConfigScript** cmdlet을 사용 하 여 vpn 장치에 대 한 올바른 스크립트 또는 구성 파일을 검색 한 다음 해당 스크립트나 구성 파일을 vpn 장치에 로드 하세요.</span><span class="sxs-lookup"><span data-stu-id="02517-111">To configure the VPN device, use the **Get-AzureRemoteAppVpnDeviceConfigScript** cmdlet to retrieve the correct script or configuration file for your VPN device, then load that script or configuration file onto the VPN device.</span></span>

## <span data-ttu-id="02517-112">변수</span><span class="sxs-lookup"><span data-stu-id="02517-112">PARAMETERS</span></span>

### <span data-ttu-id="02517-113">-프로필</span><span class="sxs-lookup"><span data-stu-id="02517-113">-Profile</span></span>
<span data-ttu-id="02517-114">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="02517-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="02517-115">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="02517-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="02517-116">-VNetName</span><span class="sxs-lookup"><span data-stu-id="02517-116">-VNetName</span></span>
<span data-ttu-id="02517-117">Azure RemoteApp 가상 네트워크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="02517-117">Specifies the name of the Azure RemoteApp virtual network.</span></span>

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

### <span data-ttu-id="02517-118">-확인</span><span class="sxs-lookup"><span data-stu-id="02517-118">-Confirm</span></span>
<span data-ttu-id="02517-119">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="02517-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02517-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02517-120">-WhatIf</span></span>
<span data-ttu-id="02517-121">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="02517-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02517-122">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="02517-122">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02517-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02517-123">CommonParameters</span></span>
<span data-ttu-id="02517-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="02517-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02517-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02517-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02517-126">입력</span><span class="sxs-lookup"><span data-stu-id="02517-126">INPUTS</span></span>

## <span data-ttu-id="02517-127">출력</span><span class="sxs-lookup"><span data-stu-id="02517-127">OUTPUTS</span></span>

### <span data-ttu-id="02517-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="02517-128">System.String</span></span>

## <span data-ttu-id="02517-129">상속자</span><span class="sxs-lookup"><span data-stu-id="02517-129">NOTES</span></span>

## <span data-ttu-id="02517-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="02517-130">RELATED LINKS</span></span>

[<span data-ttu-id="02517-131">Get-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="02517-131">Get-AzureRemoteAppVNet</span></span>](./Get-AzureRemoteAppVNet.md)

[<span data-ttu-id="02517-132">Get-AzureRemoteAppVpnDeviceConfigScript</span><span class="sxs-lookup"><span data-stu-id="02517-132">Get-AzureRemoteAppVpnDeviceConfigScript</span></span>](./Get-AzureRemoteAppVpnDeviceConfigScript.md)


