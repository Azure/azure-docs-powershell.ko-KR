---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 05626BF7-F886-4C76-8FC2-DDF783DEB539
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientRevokedCertificate.md
ms.openlocfilehash: 04bc51a7040cae1310fd3c4fe51fd45c425fad8e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187105"
---
# <span data-ttu-id="e2937-101">Get-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="e2937-101">Get-AzVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="e2937-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2937-102">SYNOPSIS</span></span>
<span data-ttu-id="e2937-103">VPN 클라이언트 해지 인증서에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e2937-103">Gets information about VPN client-revocation certificates.</span></span>

## <span data-ttu-id="e2937-104">구문</span><span class="sxs-lookup"><span data-stu-id="e2937-104">SYNTAX</span></span>

```
Get-AzVpnClientRevokedCertificate [-VpnClientRevokedCertificateName <String>]
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e2937-105">설명</span><span class="sxs-lookup"><span data-stu-id="e2937-105">DESCRIPTION</span></span>
<span data-ttu-id="e2937-106">**Get-AzVpnClientRevokedCertificate** cmdlet은 가상 네트워크 게이트웨이에 할당된 클라이언트 해지 인증서에 대한 정보를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="e2937-106">The **Get-AzVpnClientRevokedCertificate** cmdlet returns information about the client-revocation certificates assigned to a virtual network gateway.</span></span>
<span data-ttu-id="e2937-107">클라이언트 해지 인증서는 클라이언트 컴퓨터가 인증에 지정된 인증서를 사용하지 못하도록 방지합니다.</span><span class="sxs-lookup"><span data-stu-id="e2937-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="e2937-108">**Get-AzVpnClientRevokedCertificate를** 사용하면 게이트웨이의 모든 클라이언트 해지 인증서에 대한 정보를 반환하거나 *VpnClientRevokedCertificateName* 매개 변수를 사용하여 단일 인증서에 대한 정보를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e2937-108">**Get-AzVpnClientRevokedCertificate** enables you to return information about all the client-revocation certificates on the gateway or, by using the *VpnClientRevokedCertificateName* parameter, to get information about a single certificate.</span></span>

## <span data-ttu-id="e2937-109">예제</span><span class="sxs-lookup"><span data-stu-id="e2937-109">EXAMPLES</span></span>

### <span data-ttu-id="e2937-110">예제 1: 모든 클라이언트 해지 인증서에 대한 정보 얻기</span><span class="sxs-lookup"><span data-stu-id="e2937-110">Example 1: Get information about all client-revocation certificates</span></span>
```
PS C:\>Get-AzVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="e2937-111">이 명령은 ContosoVirtualNetworkGateway라는 가상 네트워크 게이트웨이와 연결된 모든 클라이언트 해지 인증서에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e2937-111">This command gets information about all the client-revocation certificates associated with the virtual network gateway named ContosoVirtualNetworkGateway.</span></span>

### <span data-ttu-id="e2937-112">예제 2: 특정 클라이언트 해지 인증서에 대한 정보 얻기</span><span class="sxs-lookup"><span data-stu-id="e2937-112">Example 2: Get information about specific client-revocation certificates</span></span>
```
PS C:\>Get-AzVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate"
```

<span data-ttu-id="e2937-113">이 명령은 예제 1에 표시된 명령의 변형입니다.</span><span class="sxs-lookup"><span data-stu-id="e2937-113">This command is a variation of the command shown in Example 1.</span></span>
<span data-ttu-id="e2937-114">그러나 이 경우 *VpnClientRevokedCertificateName* 매개 변수를 사용하여 반환된 데이터를 특정 클라이언트 해지된 인증서(ContosoRevokedClientCertificate 이름이 있는 인증서)로 제한합니다.</span><span class="sxs-lookup"><span data-stu-id="e2937-114">In this case, however, the *VpnClientRevokedCertificateName* parameter is used to limit the returned data to a specific client-revoked certificate: the certificate with the name ContosoRevokedClientCertificate.</span></span>

## <span data-ttu-id="e2937-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e2937-115">PARAMETERS</span></span>

### <span data-ttu-id="e2937-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2937-116">-DefaultProfile</span></span>
<span data-ttu-id="e2937-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e2937-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e2937-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2937-118">-ResourceGroupName</span></span>
<span data-ttu-id="e2937-119">가상 네트워크 게이트웨이가 할당된 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e2937-119">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>
<span data-ttu-id="e2937-120">리소스 그룹은 재고 관리 및 일반 Azure 관리를 간소화하는 데 도움이 되는 항목을 분류합니다.</span><span class="sxs-lookup"><span data-stu-id="e2937-120">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="e2937-121">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="e2937-121">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="e2937-122">해지된 인증서 정보가 할당된 가상 네트워크 게이트웨이의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e2937-122">Specifies the name of the virtual network gateway where the revoked certificate information is assigned.</span></span>

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

### <span data-ttu-id="e2937-123">-VpnClientRevokedCertificateName</span><span class="sxs-lookup"><span data-stu-id="e2937-123">-VpnClientRevokedCertificateName</span></span>
<span data-ttu-id="e2937-124">이 cmdlet이 제공하는 VPN 클라이언트 인증서의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e2937-124">Specifies the name of the VPN client certificate that this cmdlet gets.</span></span>

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

### <span data-ttu-id="e2937-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2937-125">CommonParameters</span></span>
<span data-ttu-id="e2937-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e2937-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2937-127">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e2937-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2937-128">입력</span><span class="sxs-lookup"><span data-stu-id="e2937-128">INPUTS</span></span>

### <span data-ttu-id="e2937-129">System.String</span><span class="sxs-lookup"><span data-stu-id="e2937-129">System.String</span></span>

## <span data-ttu-id="e2937-130">출력</span><span class="sxs-lookup"><span data-stu-id="e2937-130">OUTPUTS</span></span>

### <span data-ttu-id="e2937-131">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="e2937-131">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="e2937-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e2937-132">NOTES</span></span>

## <span data-ttu-id="e2937-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e2937-133">RELATED LINKS</span></span>

[<span data-ttu-id="e2937-134">Add-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="e2937-134">Add-AzVpnClientRevokedCertificate</span></span>](./Add-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="e2937-135">New-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="e2937-135">New-AzVpnClientRevokedCertificate</span></span>](./New-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="e2937-136">Remove-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="e2937-136">Remove-AzVpnClientRevokedCertificate</span></span>](./Remove-AzVpnClientRevokedCertificate.md)


