---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: C85576C1-182B-467E-9620-A475728E20D2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3715b07c66d76c824e684976f18de4ecea64cdb1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046036"
---
# <span data-ttu-id="d751c-101">Set-AzureVNetGatewayIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="d751c-101">Set-AzureVNetGatewayIPsecParameters</span></span>

## <span data-ttu-id="d751c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d751c-102">SYNOPSIS</span></span>
<span data-ttu-id="d751c-103">가상 네트워크 게이트웨이와 로컬 네트워크 사이트 간 연결에 대 한 IPsec 매개 변수를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d751c-103">Sets IPsec parameters for the connection between a virtual network gateway and a local network site.</span></span>

## <span data-ttu-id="d751c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d751c-104">SYNTAX</span></span>

```
Set-AzureVNetGatewayIPsecParameters -VNetName <String> -LocalNetworkSiteName <String>
 [-EncryptionType <String>] [-PfsGroup <String>] [-SADataSizeKilobytes <Int32>] [-SALifetimeSeconds <Int32>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d751c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d751c-105">DESCRIPTION</span></span>
<span data-ttu-id="d751c-106">**Set-Azurevnet2| 매개 변수** cmdlet은 가상 네트워크 게이트웨이와 로컬 네트워크 사이트 간 연결에 대 한 IPsec (인터넷 프로토콜 보안) 및 IKE (인터넷 키 교환) 매개 변수를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d751c-106">The **Set-AzureVNetGatewayIPsecParameters** cmdlet sets Internet Protocol security (IPsec) and Internet Key Exchange (IKE) parameters for the connection between a virtual network gateway and a local network site.</span></span>

## <span data-ttu-id="d751c-107">예제의</span><span class="sxs-lookup"><span data-stu-id="d751c-107">EXAMPLES</span></span>

## <span data-ttu-id="d751c-108">변수</span><span class="sxs-lookup"><span data-stu-id="d751c-108">PARAMETERS</span></span>

### <span data-ttu-id="d751c-109">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="d751c-109">-EncryptionType</span></span>
<span data-ttu-id="d751c-110">가상 네트워크 게이트웨이의 암호화 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d751c-110">Specifies the encryption type for the virtual network gateway.</span></span>
<span data-ttu-id="d751c-111">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="d751c-111">Valid values are:</span></span> 

- <span data-ttu-id="d751c-112">NoEncryption</span><span class="sxs-lookup"><span data-stu-id="d751c-112">NoEncryption</span></span> 
- <span data-ttu-id="d751c-113">RequireEncryption</span><span class="sxs-lookup"><span data-stu-id="d751c-113">RequireEncryption</span></span>

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

### <span data-ttu-id="d751c-114">-LocalNetworkSiteName</span><span class="sxs-lookup"><span data-stu-id="d751c-114">-LocalNetworkSiteName</span></span>
<span data-ttu-id="d751c-115">이 cmdlet이 IPsec 및 IKE 매개 변수를 구성 하는 로컬 네트워크 사이트 연결의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d751c-115">Specifies the name of the local network site connection on which this cmdlet configures the IPsec and IKE parameters.</span></span>

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

### <span data-ttu-id="d751c-116">-PfsGroup</span><span class="sxs-lookup"><span data-stu-id="d751c-116">-PfsGroup</span></span>
<span data-ttu-id="d751c-117">전달 완전 보안 (PFS) 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d751c-117">Specifies the perfect forward secrecy (PFS) group.</span></span>
<span data-ttu-id="d751c-118">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="d751c-118">Valid values are:</span></span> 

- <span data-ttu-id="d751c-119">PFS1</span><span class="sxs-lookup"><span data-stu-id="d751c-119">PFS1</span></span> 
- <span data-ttu-id="d751c-120">않아야</span><span class="sxs-lookup"><span data-stu-id="d751c-120">None</span></span>

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

### <span data-ttu-id="d751c-121">-프로필</span><span class="sxs-lookup"><span data-stu-id="d751c-121">-Profile</span></span>
<span data-ttu-id="d751c-122">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d751c-122">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="d751c-123">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="d751c-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d751c-124">-SADataSizeKilobytes</span><span class="sxs-lookup"><span data-stu-id="d751c-124">-SADataSizeKilobytes</span></span>
<span data-ttu-id="d751c-125">SA (보안 연결)의 크기 (kb)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d751c-125">Specifies the size, in kilobytes, of the security association (SA).</span></span>

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

### <span data-ttu-id="d751c-126">-SALifetimeSeconds</span><span class="sxs-lookup"><span data-stu-id="d751c-126">-SALifetimeSeconds</span></span>
<span data-ttu-id="d751c-127">보안 연결의 기간 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d751c-127">Specifies the period, in seconds, of the security association.</span></span>

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

### <span data-ttu-id="d751c-128">-VNetName</span><span class="sxs-lookup"><span data-stu-id="d751c-128">-VNetName</span></span>
<span data-ttu-id="d751c-129">이 cmdlet이 연결에 대 한 IPsec 매개 변수를 설정 하는 가상 네트워크를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d751c-129">Specifies the virtual network for which this cmdlet sets IPsec parameters for the connection.</span></span>

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

### <span data-ttu-id="d751c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d751c-130">CommonParameters</span></span>
<span data-ttu-id="d751c-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d751c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d751c-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d751c-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d751c-133">입력</span><span class="sxs-lookup"><span data-stu-id="d751c-133">INPUTS</span></span>

## <span data-ttu-id="d751c-134">출력</span><span class="sxs-lookup"><span data-stu-id="d751c-134">OUTPUTS</span></span>

## <span data-ttu-id="d751c-135">상속자</span><span class="sxs-lookup"><span data-stu-id="d751c-135">NOTES</span></span>

## <span data-ttu-id="d751c-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d751c-136">RELATED LINKS</span></span>

[<span data-ttu-id="d751c-137">Get-Azurevnet2| 매개 변수</span><span class="sxs-lookup"><span data-stu-id="d751c-137">Get-AzureVNetGatewayIPsecParameters</span></span>](./Get-AzureVNetGatewayIPsecParameters.md)


