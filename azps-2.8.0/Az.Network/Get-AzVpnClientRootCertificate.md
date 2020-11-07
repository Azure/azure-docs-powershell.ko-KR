---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 16754F70-9619-4F68-86E9-5C8B27812707
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientRootCertificate.md
ms.openlocfilehash: 847f1c06975e9bef570c5ab3fdaf5f6f3e4a99d6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93870034"
---
# <span data-ttu-id="6ba8c-101">Get-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="6ba8c-101">Get-AzVpnClientRootCertificate</span></span>

## <span data-ttu-id="6ba8c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ba8c-102">SYNOPSIS</span></span>
<span data-ttu-id="6ba8c-103">VPN 루트 인증서에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6ba8c-103">Gets information about VPN root certificates.</span></span>

## <span data-ttu-id="6ba8c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6ba8c-104">SYNTAX</span></span>

```
Get-AzVpnClientRootCertificate [-VpnClientRootCertificateName <String>] -VirtualNetworkGatewayName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6ba8c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="6ba8c-105">DESCRIPTION</span></span>
<span data-ttu-id="6ba8c-106">**Get-AzVpnClientRootCertificate** cmdlet은 가상 네트워크 게이트웨이에 할당 된 루트 인증서에 대 한 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ba8c-106">The **Get-AzVpnClientRootCertificate** cmdlet returns information about the root certificates assigned to a virtual network gateway.</span></span>
<span data-ttu-id="6ba8c-107">루트 인증서는 루트 인증 기관을 식별 하는 x.509 인증서입니다. 게이트웨이에서 사용 되는 다른 모든 인증서는 루트 인증서를 신뢰 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ba8c-107">Root certificates are X.509 certificates that identify your Root Certification Authority: all other certificates used on the gateway trust the root certificate.</span></span>
<span data-ttu-id="6ba8c-108">기본적으로 **Get-AzVpnClientRootCertificate** 는 게이트웨이에 할당 된 모든 루트 인증서에 대 한 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ba8c-108">By default, **Get-AzVpnClientRootCertificate** returns information about all the root certificates assigned to a gateway.</span></span>
<span data-ttu-id="6ba8c-109">(게이트웨이에서는 루트 인증서가 두 개 이상 있을 수 있습니다.) 그러나 **VpnClientRootCertificateName** 매개 변수를 포함 하 여 반환 된 데이터를 특정 인증서로 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6ba8c-109">(Gateways can have more than one root certificate.) However, by including the **VpnClientRootCertificateName** parameter you can limit the returned data to a specific certificate.</span></span>

## <span data-ttu-id="6ba8c-110">예제의</span><span class="sxs-lookup"><span data-stu-id="6ba8c-110">EXAMPLES</span></span>

### <span data-ttu-id="6ba8c-111">예제 1: 모든 루트 인증서에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="6ba8c-111">Example 1: Get information about all root certificates</span></span>
```
PS C:\>Get-AzVpnClientRootCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="6ba8c-112">이 명령은 ContosoVirtualNetwork 이라는 가상 네트워크 게이트웨이에 할당 된 모든 루트 인증서에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6ba8c-112">This command gets information about all the root certificates assigned to a virtual network gateway named ContosoVirtualNetwork.</span></span>

### <span data-ttu-id="6ba8c-113">예제 2: 특정 루트 인증서에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="6ba8c-113">Example 2: Get information about specific root certificates</span></span>
```
PS C:\>Get-AzVpnClientRootCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRootCertificateName "ContosoRootClientCertificate"
```

<span data-ttu-id="6ba8c-114">이 명령은 예제 1에 표시 된 명령의 변형입니다.</span><span class="sxs-lookup"><span data-stu-id="6ba8c-114">This command is a variation of the command shown in Example 1.</span></span>
<span data-ttu-id="6ba8c-115">그러나이 경우 반환 된 데이터를 특정 루트 인증서로 제한 하기 위해 *VpnClientRootCertificateName* 매개 변수가 포함 됩니다. ContosoRootClientCertificate.</span><span class="sxs-lookup"><span data-stu-id="6ba8c-115">In this case, however, the *VpnClientRootCertificateName* parameter is included in order to limit the returned data to a specific root certificate: ContosoRootClientCertificate.</span></span>

## <span data-ttu-id="6ba8c-116">변수</span><span class="sxs-lookup"><span data-stu-id="6ba8c-116">PARAMETERS</span></span>

### <span data-ttu-id="6ba8c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ba8c-117">-DefaultProfile</span></span>
<span data-ttu-id="6ba8c-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6ba8c-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ba8c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ba8c-119">-ResourceGroupName</span></span>
<span data-ttu-id="6ba8c-120">가상 네트워크 게이트웨이가 할당 되는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ba8c-120">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>
<span data-ttu-id="6ba8c-121">리소스 그룹은 인벤터리 관리 및 일반 Azure 관리를 간소화 하기 위해 항목을 분류 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ba8c-121">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ba8c-122">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="6ba8c-122">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="6ba8c-123">루트 인증서가 할당 된 가상 네트워크 게이트웨이의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ba8c-123">Specifies the name of the virtual network gateway where the root certificate is assigned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ba8c-124">-VpnClientRootCertificateName</span><span class="sxs-lookup"><span data-stu-id="6ba8c-124">-VpnClientRootCertificateName</span></span>
<span data-ttu-id="6ba8c-125">이 cmdlet이 가져오는 클라이언트 루트 인증서의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ba8c-125">Specifies the name of the client root certificate that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ba8c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ba8c-126">CommonParameters</span></span>
<span data-ttu-id="6ba8c-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ba8c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ba8c-128">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6ba8c-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ba8c-129">입력</span><span class="sxs-lookup"><span data-stu-id="6ba8c-129">INPUTS</span></span>

### <span data-ttu-id="6ba8c-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="6ba8c-130">System.String</span></span>

## <span data-ttu-id="6ba8c-131">출력</span><span class="sxs-lookup"><span data-stu-id="6ba8c-131">OUTPUTS</span></span>

### <span data-ttu-id="6ba8c-132">PSVpnClientRootCertificate에 대 한.</span><span class="sxs-lookup"><span data-stu-id="6ba8c-132">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate</span></span>

## <span data-ttu-id="6ba8c-133">상속자</span><span class="sxs-lookup"><span data-stu-id="6ba8c-133">NOTES</span></span>

## <span data-ttu-id="6ba8c-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6ba8c-134">RELATED LINKS</span></span>

[<span data-ttu-id="6ba8c-135">추가-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="6ba8c-135">Add-AzVpnClientRootCertificate</span></span>](./Add-AzVpnClientRootCertificate.md)

[<span data-ttu-id="6ba8c-136">새로운 AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="6ba8c-136">New-AzVpnClientRootCertificate</span></span>](./New-AzVpnClientRootCertificate.md)

[<span data-ttu-id="6ba8c-137">제거-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="6ba8c-137">Remove-AzVpnClientRootCertificate</span></span>](./Remove-AzVpnClientRootCertificate.md)


