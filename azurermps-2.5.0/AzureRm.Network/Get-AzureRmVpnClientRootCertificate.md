---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 16754F70-9619-4F68-86E9-5C8B27812707
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvpnclientrootcertificate
schema: 2.0.0
ms.openlocfilehash: 7c3ee4e2c640417a7ba3d6cd78c2c8ea0691fff3
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93881405"
---
# <span data-ttu-id="68fd8-101">Get-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="68fd8-101">Get-AzureRmVpnClientRootCertificate</span></span>

## <span data-ttu-id="68fd8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="68fd8-102">SYNOPSIS</span></span>
<span data-ttu-id="68fd8-103">VPN 루트 인증서에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="68fd8-103">Gets information about VPN root certificates.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="68fd8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="68fd8-104">SYNTAX</span></span>

```
Get-AzureRmVpnClientRootCertificate [-VpnClientRootCertificateName <String>]
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="68fd8-105">설명은</span><span class="sxs-lookup"><span data-stu-id="68fd8-105">DESCRIPTION</span></span>
<span data-ttu-id="68fd8-106">**Get-AzureRmVpnClientRootCertificate** cmdlet은 가상 네트워크 게이트웨이에 할당 된 루트 인증서에 대 한 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="68fd8-106">The **Get-AzureRmVpnClientRootCertificate** cmdlet returns information about the root certificates assigned to a virtual network gateway.</span></span>
<span data-ttu-id="68fd8-107">루트 인증서는 루트 인증 기관을 식별 하는 x.509 인증서입니다. 게이트웨이에서 사용 되는 다른 모든 인증서는 루트 인증서를 신뢰 합니다.</span><span class="sxs-lookup"><span data-stu-id="68fd8-107">Root certificates are X.509 certificates that identify your Root Certification Authority: all other certificates used on the gateway trust the root certificate.</span></span>

<span data-ttu-id="68fd8-108">기본적으로 **Get-AzureRmVpnClientRootCertificate** 는 게이트웨이에 할당 된 모든 루트 인증서에 대 한 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="68fd8-108">By default, **Get-AzureRmVpnClientRootCertificate** returns information about all the root certificates assigned to a gateway.</span></span>
<span data-ttu-id="68fd8-109">(게이트웨이에서는 루트 인증서가 두 개 이상 있을 수 있습니다.) 그러나 **VpnClientRootCertificateName** 매개 변수를 포함 하 여 반환 된 데이터를 특정 인증서로 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="68fd8-109">(Gateways can have more than one root certificate.) However, by including the **VpnClientRootCertificateName** parameter you can limit the returned data to a specific certificate.</span></span>

## <span data-ttu-id="68fd8-110">예제의</span><span class="sxs-lookup"><span data-stu-id="68fd8-110">EXAMPLES</span></span>

### <span data-ttu-id="68fd8-111">예제 1: 모든 루트 인증서에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="68fd8-111">Example 1: Get information about all root certificates</span></span>
```
PS C:\>Get-AzureRmVpnClientRootCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="68fd8-112">이 명령은 ContosoVirtualNetwork 이라는 가상 네트워크 게이트웨이에 할당 된 모든 루트 인증서에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="68fd8-112">This command gets information about all the root certificates assigned to a virtual network gateway named ContosoVirtualNetwork.</span></span>

### <span data-ttu-id="68fd8-113">예제 2: 특정 루트 인증서에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="68fd8-113">Example 2: Get information about specific root certificates</span></span>
```
PS C:\>Get-AzureRmVpnClientRootCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRootCertificateName "ContosoRootClientCertificate"
```

<span data-ttu-id="68fd8-114">이 명령은 예제 1에 표시 된 명령의 변형입니다.</span><span class="sxs-lookup"><span data-stu-id="68fd8-114">This command is a variation of the command shown in Example 1.</span></span>
<span data-ttu-id="68fd8-115">그러나이 경우 반환 된 데이터를 특정 루트 인증서로 제한 하기 위해 *VpnClientRootCertificateName* 매개 변수가 포함 됩니다. ContosoRootClientCertificate.</span><span class="sxs-lookup"><span data-stu-id="68fd8-115">In this case, however, the *VpnClientRootCertificateName* parameter is included in order to limit the returned data to a specific root certificate: ContosoRootClientCertificate.</span></span>

## <span data-ttu-id="68fd8-116">변수</span><span class="sxs-lookup"><span data-stu-id="68fd8-116">PARAMETERS</span></span>

### <span data-ttu-id="68fd8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68fd8-117">-DefaultProfile</span></span>
<span data-ttu-id="68fd8-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="68fd8-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68fd8-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68fd8-119">-ResourceGroupName</span></span>
<span data-ttu-id="68fd8-120">가상 네트워크 게이트웨이가 할당 되는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="68fd8-120">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>

<span data-ttu-id="68fd8-121">리소스 그룹은 인벤터리 관리 및 일반 Azure 관리를 간소화 하기 위해 항목을 분류 합니다.</span><span class="sxs-lookup"><span data-stu-id="68fd8-121">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68fd8-122">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="68fd8-122">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="68fd8-123">루트 인증서가 할당 된 가상 네트워크 게이트웨이의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="68fd8-123">Specifies the name of the virtual network gateway where the root certificate is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68fd8-124">-VpnClientRootCertificateName</span><span class="sxs-lookup"><span data-stu-id="68fd8-124">-VpnClientRootCertificateName</span></span>
<span data-ttu-id="68fd8-125">이 cmdlet이 가져오는 클라이언트 루트 인증서의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="68fd8-125">Specifies the name of the client root certificate that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68fd8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68fd8-126">CommonParameters</span></span>
<span data-ttu-id="68fd8-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="68fd8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68fd8-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68fd8-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68fd8-129">입력</span><span class="sxs-lookup"><span data-stu-id="68fd8-129">INPUTS</span></span>

## <span data-ttu-id="68fd8-130">출력</span><span class="sxs-lookup"><span data-stu-id="68fd8-130">OUTPUTS</span></span>

###  
<span data-ttu-id="68fd8-131">**Get-AzureRmVpnClientRootCertificate** 는 **PSVpnClientRootCertificate** 개체의 인스턴스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="68fd8-131">**Get-AzureRmVpnClientRootCertificate** gets instances of the **Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate** object.</span></span>

## <span data-ttu-id="68fd8-132">상속자</span><span class="sxs-lookup"><span data-stu-id="68fd8-132">NOTES</span></span>

## <span data-ttu-id="68fd8-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="68fd8-133">RELATED LINKS</span></span>

[<span data-ttu-id="68fd8-134">추가-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="68fd8-134">Add-AzureRmVpnClientRootCertificate</span></span>](./Add-AzureRmVpnClientRootCertificate.md)

[<span data-ttu-id="68fd8-135">새로운 AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="68fd8-135">New-AzureRmVpnClientRootCertificate</span></span>](./New-AzureRmVpnClientRootCertificate.md)

[<span data-ttu-id="68fd8-136">제거-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="68fd8-136">Remove-AzureRmVpnClientRootCertificate</span></span>](./Remove-AzureRmVpnClientRootCertificate.md)


