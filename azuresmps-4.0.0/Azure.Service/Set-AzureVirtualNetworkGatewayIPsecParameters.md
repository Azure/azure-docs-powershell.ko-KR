---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 150EE0DC-07CD-4E24-AF70-0C1A7BB61433
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8b663ced66318335afb1fe4c3bf0e6a1520ede7b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046412"
---
# <span data-ttu-id="206f5-101">Set-AzureVirtualNetworkGatewayIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="206f5-101">Set-AzureVirtualNetworkGatewayIPsecParameters</span></span>

## <span data-ttu-id="206f5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="206f5-102">SYNOPSIS</span></span>
<span data-ttu-id="206f5-103">가상 네트워크 게이트웨이의 IPsec 매개 변수를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="206f5-103">Sets IPsec parameters for a virtual network gateway.</span></span>

## <span data-ttu-id="206f5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="206f5-104">SYNTAX</span></span>

```
Set-AzureVirtualNetworkGatewayIPsecParameters -GatewayId <String> -ConnectedEntityId <String>
 [-EncryptionType <String>] [-PfsGroup <String>] [-SADataSizeKilobytes <Int32>] [-SALifetimeSeconds <Int32>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="206f5-105">설명은</span><span class="sxs-lookup"><span data-stu-id="206f5-105">DESCRIPTION</span></span>
<span data-ttu-id="206f5-106">**AzureVirtualNetworkGatewayIPsecParameters** cmdlet은 가상 네트워크 게이트웨이에 대 한 IPsec 매개 변수를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="206f5-106">The **Set-AzureVirtualNetworkGatewayIPsecParameters** cmdlet sets IPsec parameters for a virtual network gateway.</span></span>

## <span data-ttu-id="206f5-107">예제의</span><span class="sxs-lookup"><span data-stu-id="206f5-107">EXAMPLES</span></span>

## <span data-ttu-id="206f5-108">변수</span><span class="sxs-lookup"><span data-stu-id="206f5-108">PARAMETERS</span></span>

### <span data-ttu-id="206f5-109">-ConnectedEntityId</span><span class="sxs-lookup"><span data-stu-id="206f5-109">-ConnectedEntityId</span></span>
<span data-ttu-id="206f5-110">연결 된 엔터티의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="206f5-110">Specifies the ID of a connected entity.</span></span>

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

### <span data-ttu-id="206f5-111">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="206f5-111">-EncryptionType</span></span>
<span data-ttu-id="206f5-112">가상 네트워크 게이트웨이의 암호화 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="206f5-112">Specifies the encryption type for the virtual network gateway.</span></span>
<span data-ttu-id="206f5-113">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="206f5-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="206f5-114">NoEncryption</span><span class="sxs-lookup"><span data-stu-id="206f5-114">NoEncryption</span></span>
- <span data-ttu-id="206f5-115">RequireEncryption</span><span class="sxs-lookup"><span data-stu-id="206f5-115">RequireEncryption</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="206f5-116">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="206f5-116">-GatewayId</span></span>
<span data-ttu-id="206f5-117">게이트웨이의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="206f5-117">Specifies the ID of a gateway.</span></span>

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

### <span data-ttu-id="206f5-118">-PfsGroup</span><span class="sxs-lookup"><span data-stu-id="206f5-118">-PfsGroup</span></span>
<span data-ttu-id="206f5-119">전달 완전 보안 (PFS) 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="206f5-119">Specifies the perfect forward secrecy (PFS) group.</span></span>
<span data-ttu-id="206f5-120">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="206f5-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="206f5-121">PFS1</span><span class="sxs-lookup"><span data-stu-id="206f5-121">PFS1</span></span>
- <span data-ttu-id="206f5-122">않아야</span><span class="sxs-lookup"><span data-stu-id="206f5-122">None</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="206f5-123">-프로필</span><span class="sxs-lookup"><span data-stu-id="206f5-123">-Profile</span></span>
<span data-ttu-id="206f5-124">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="206f5-124">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="206f5-125">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="206f5-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="206f5-126">-SADataSizeKilobytes</span><span class="sxs-lookup"><span data-stu-id="206f5-126">-SADataSizeKilobytes</span></span>
<span data-ttu-id="206f5-127">SA (보안 연결)의 크기 (kb)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="206f5-127">Specifies the size, in kilobytes, of the security association (SA).</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="206f5-128">-SALifetimeSeconds</span><span class="sxs-lookup"><span data-stu-id="206f5-128">-SALifetimeSeconds</span></span>
<span data-ttu-id="206f5-129">보안 연결의 기간 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="206f5-129">Specifies the period, in seconds, of the security association.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="206f5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="206f5-130">CommonParameters</span></span>
<span data-ttu-id="206f5-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="206f5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="206f5-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="206f5-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="206f5-133">입력</span><span class="sxs-lookup"><span data-stu-id="206f5-133">INPUTS</span></span>

## <span data-ttu-id="206f5-134">출력</span><span class="sxs-lookup"><span data-stu-id="206f5-134">OUTPUTS</span></span>

## <span data-ttu-id="206f5-135">상속자</span><span class="sxs-lookup"><span data-stu-id="206f5-135">NOTES</span></span>

## <span data-ttu-id="206f5-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="206f5-136">RELATED LINKS</span></span>

[<span data-ttu-id="206f5-137">Get-AzureVirtualNetworkGatewayIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="206f5-137">Get-AzureVirtualNetworkGatewayIPsecParameters</span></span>](./Get-AzureVirtualNetworkGatewayIPsecParameters.md)


