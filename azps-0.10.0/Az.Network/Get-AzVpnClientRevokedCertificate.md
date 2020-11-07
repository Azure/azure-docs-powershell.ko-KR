---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 05626BF7-F886-4C76-8FC2-DDF783DEB539
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVpnClientRevokedCertificate.md
ms.openlocfilehash: 3151ffb45064d1cb85b69d11a1ccbd49d4c045e8
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875489"
---
# <span data-ttu-id="b5c81-101">Get-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="b5c81-101">Get-AzVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="b5c81-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5c81-102">SYNOPSIS</span></span>
<span data-ttu-id="b5c81-103">VPN 클라이언트 해지 인증서에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b5c81-103">Gets information about VPN client-revocation certificates.</span></span>

## <span data-ttu-id="b5c81-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b5c81-104">SYNTAX</span></span>

```
Get-AzVpnClientRevokedCertificate [-VpnClientRevokedCertificateName <String>]
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b5c81-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b5c81-105">DESCRIPTION</span></span>
<span data-ttu-id="b5c81-106">**AzVpnClientRevokedCertificate** cmdlet은 가상 네트워크 게이트웨이에 할당 된 클라이언트 해지 인증서에 대 한 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5c81-106">The **Get-AzVpnClientRevokedCertificate** cmdlet returns information about the client-revocation certificates assigned to a virtual network gateway.</span></span>
<span data-ttu-id="b5c81-107">클라이언트 해지 인증서는 클라이언트 컴퓨터가 인증을 위해 지정 된 인증서를 사용 하지 못하도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5c81-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="b5c81-108">**Get-AzVpnClientRevokedCertificate** 를 사용 하면 게이트웨이에서 모든 클라이언트 해지 인증서에 대 한 정보를 반환 하거나 *VpnClientRevokedCertificateName* 매개 변수를 사용 하 여 단일 인증서에 대 한 정보를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b5c81-108">**Get-AzVpnClientRevokedCertificate** enables you to return information about all the client-revocation certificates on the gateway or, by using the *VpnClientRevokedCertificateName* parameter, to get information about a single certificate.</span></span>

## <span data-ttu-id="b5c81-109">예제의</span><span class="sxs-lookup"><span data-stu-id="b5c81-109">EXAMPLES</span></span>

### <span data-ttu-id="b5c81-110">예제 1: 모든 클라이언트 철회 인증서에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="b5c81-110">Example 1: Get information about all client-revocation certificates</span></span>
```
PS C:\>Get-AzVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="b5c81-111">이 명령은 ContosoVirtualNetworkGateway 이라는 가상 네트워크 게이트웨이에 연결 된 모든 클라이언트 해지 인증서에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b5c81-111">This command gets information about all the client-revocation certificates associated with the virtual network gateway named ContosoVirtualNetworkGateway.</span></span>

### <span data-ttu-id="b5c81-112">예제 2: 특정 클라이언트 해지 인증서에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="b5c81-112">Example 2: Get information about specific client-revocation certificates</span></span>
```
PS C:\>Get-AzVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate"
```

<span data-ttu-id="b5c81-113">이 명령은 예제 1에 표시 된 명령의 변형입니다.</span><span class="sxs-lookup"><span data-stu-id="b5c81-113">This command is a variation of the command shown in Example 1.</span></span>
<span data-ttu-id="b5c81-114">그러나이 경우 *VpnClientRevokedCertificateName* 매개 변수는 반환 된 데이터를 특정 클라이언트로 제한 하는 데 사용 됩니다 (해지 된 인증서: 이름이 ContosoRevokedClientCertificate 인 인증서).</span><span class="sxs-lookup"><span data-stu-id="b5c81-114">In this case, however, the *VpnClientRevokedCertificateName* parameter is used to limit the returned data to a specific client-revoked certificate: the certificate with the name ContosoRevokedClientCertificate.</span></span>

## <span data-ttu-id="b5c81-115">변수</span><span class="sxs-lookup"><span data-stu-id="b5c81-115">PARAMETERS</span></span>

### <span data-ttu-id="b5c81-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5c81-116">-DefaultProfile</span></span>
<span data-ttu-id="b5c81-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b5c81-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b5c81-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5c81-118">-ResourceGroupName</span></span>
<span data-ttu-id="b5c81-119">가상 네트워크 게이트웨이가 할당 되는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5c81-119">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>

<span data-ttu-id="b5c81-120">리소스 그룹은 인벤터리 관리 및 일반 Azure 관리를 간소화 하기 위해 항목을 분류 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5c81-120">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="b5c81-121">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="b5c81-121">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="b5c81-122">해지 된 인증서 정보가 할당 되는 가상 네트워크 게이트웨이의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5c81-122">Specifies the name of the virtual network gateway where the revoked certificate information is assigned.</span></span>

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

### <span data-ttu-id="b5c81-123">-VpnClientRevokedCertificateName</span><span class="sxs-lookup"><span data-stu-id="b5c81-123">-VpnClientRevokedCertificateName</span></span>
<span data-ttu-id="b5c81-124">이 cmdlet이 가져오는 VPN 클라이언트 인증서의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5c81-124">Specifies the name of the VPN client certificate that this cmdlet gets.</span></span>

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

### <span data-ttu-id="b5c81-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5c81-125">CommonParameters</span></span>
<span data-ttu-id="b5c81-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5c81-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5c81-127">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5c81-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5c81-128">입력</span><span class="sxs-lookup"><span data-stu-id="b5c81-128">INPUTS</span></span>

## <span data-ttu-id="b5c81-129">출력</span><span class="sxs-lookup"><span data-stu-id="b5c81-129">OUTPUTS</span></span>

###  
<span data-ttu-id="b5c81-130">**Get-AzVpnClientRevokedCertificate** **PSVpnClientRevokedCertificate** 개체의 인스턴스를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5c81-130">**Get-AzVpnClientRevokedCertificate** returns instances of the **Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate** object.</span></span>

## <span data-ttu-id="b5c81-131">상속자</span><span class="sxs-lookup"><span data-stu-id="b5c81-131">NOTES</span></span>

## <span data-ttu-id="b5c81-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b5c81-132">RELATED LINKS</span></span>

[<span data-ttu-id="b5c81-133">추가-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="b5c81-133">Add-AzVpnClientRevokedCertificate</span></span>](./Add-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="b5c81-134">새로운 AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="b5c81-134">New-AzVpnClientRevokedCertificate</span></span>](./New-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="b5c81-135">제거-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="b5c81-135">Remove-AzVpnClientRevokedCertificate</span></span>](./Remove-AzVpnClientRevokedCertificate.md)


