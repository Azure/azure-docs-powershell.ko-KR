---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 973E1E53-983F-45A7-A7CF-18A8D96EC4E6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnClientRevokedCertificate.md
ms.openlocfilehash: 9f20b0540481c40326bc3656e3f65534c22f9b24
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529503"
---
# <span data-ttu-id="165f9-101">New-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="165f9-101">New-AzureRmVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="165f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="165f9-102">SYNOPSIS</span></span>
<span data-ttu-id="165f9-103">새 VPN 클라이언트 해지 인증서를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="165f9-103">Creates a new VPN client-revocation certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="165f9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="165f9-104">SYNTAX</span></span>

```
New-AzureRmVpnClientRevokedCertificate -Name <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="165f9-105">설명은</span><span class="sxs-lookup"><span data-stu-id="165f9-105">DESCRIPTION</span></span>
<span data-ttu-id="165f9-106">**AzureRmVpnClientRevokedCertificate** cmdlet은 가상 네트워크 게이트웨이에서 사용할 새 VPN (가상 사설망) 클라이언트 해지 인증서를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="165f9-106">The **New-AzureRmVpnClientRevokedCertificate** cmdlet creates a new virtual private network (VPN) client-revocation certificate for use on a virtual network gateway.</span></span>
<span data-ttu-id="165f9-107">클라이언트 해지 인증서는 클라이언트 컴퓨터가 인증을 위해 지정 된 인증서를 사용 하지 못하도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="165f9-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="165f9-108">이 cmdlet은 가상 게이트웨이에 할당 되지 않은 독립 실행형 인증서를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="165f9-108">This cmdlet creates a stand-alone certificate that is not assigned to a virtual gateway.</span></span>
<span data-ttu-id="165f9-109">대신 새 게이트웨이를 만들 때 **AzureRmVpnClientRevokedCertificate** 에서 만든 인증서가 New-AzureRmVirtualNetworkGateway cmdlet과 함께 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="165f9-109">Instead, the certificate created by **New-AzureRmVpnClientRevokedCertificate** is used in conjunction with the New-AzureRmVirtualNetworkGateway cmdlet when it creates a new gateway.</span></span>
<span data-ttu-id="165f9-110">예를 들어 새 인증서를 만들고이를 $Certificate 이라는 변수에 저장 한다고 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="165f9-110">For instance, suppose you create a new certificate and store it in a variable named $Certificate.</span></span>
<span data-ttu-id="165f9-111">그런 다음 새 가상 게이트웨이를 만들 때 해당 인증서 개체를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="165f9-111">You can then use that certificate object when you create a new virtual gateway.</span></span>
<span data-ttu-id="165f9-112">예를 들어 `New-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRevokedCertificates $Certificate`</span><span class="sxs-lookup"><span data-stu-id="165f9-112">For instance, `New-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRevokedCertificates $Certificate`</span></span>
<span data-ttu-id="165f9-113">자세한 내용은 New-AzureRmVirtualNetworkGateway cmdlet에 대 한 설명서를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="165f9-113">For more information, see the documentation for the New-AzureRmVirtualNetworkGateway cmdlet.</span></span>

## <span data-ttu-id="165f9-114">예제의</span><span class="sxs-lookup"><span data-stu-id="165f9-114">EXAMPLES</span></span>

### <span data-ttu-id="165f9-115">예제 1: 새 클라이언트 만들기-해지 된 인증서</span><span class="sxs-lookup"><span data-stu-id="165f9-115">Example 1: Create a new client-revoked certificate</span></span>
```
PS C:\>$Certificate = New-AzureRmVpnClientRevokedCertificate -Name "ContosoClientRevokedCertificate" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="165f9-116">이 명령은 새 클라이언트-해지 된 인증서를 만들고 $Certificate 이라는 변수에 인증서 개체를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="165f9-116">This command creates a new client-revoked certificate and stores the certificate object in a variable named $Certificate.</span></span>
<span data-ttu-id="165f9-117">그런 다음 새 가상 네트워크 게이트웨이에 인증서를 추가 하기 위해 **AzureRmVirtualNetworkGateway** cmdlet에서이 변수를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="165f9-117">This variable can then be used by the **New-AzureRmVirtualNetworkGateway** cmdlet to add the certificate to a new virtual network gateway.</span></span>

## <span data-ttu-id="165f9-118">변수</span><span class="sxs-lookup"><span data-stu-id="165f9-118">PARAMETERS</span></span>

### <span data-ttu-id="165f9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="165f9-119">-DefaultProfile</span></span>
<span data-ttu-id="165f9-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="165f9-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="165f9-121">-이름</span><span class="sxs-lookup"><span data-stu-id="165f9-121">-Name</span></span>
<span data-ttu-id="165f9-122">새 클라이언트 해지 인증서의 고유한 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="165f9-122">Specifies a unique name for the new client-revocation certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="165f9-123">-지문</span><span class="sxs-lookup"><span data-stu-id="165f9-123">-Thumbprint</span></span>
<span data-ttu-id="165f9-124">추가할 인증서의 고유 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="165f9-124">Specifies the unique identifier of the certificate being added.</span></span>
<span data-ttu-id="165f9-125">다음과 같은 Windows PowerShell 명령을 사용 하 여 인증서에 대 한 지문 정보를 반환할 수 있습니다. `Get-ChildItem -Path Cert:\LocalMachine\Root`</span><span class="sxs-lookup"><span data-stu-id="165f9-125">You can return thumbprint information for your certificates by using a Windows PowerShell command similar to this: `Get-ChildItem -Path Cert:\LocalMachine\Root`</span></span>
<span data-ttu-id="165f9-126">앞의 명령은 루트 인증서 저장소에 있는 모든 로컬 컴퓨터 인증서에 대 한 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="165f9-126">The preceding command returns information for all the Local Computer certificates found in the Root certificate store.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="165f9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="165f9-127">CommonParameters</span></span>
<span data-ttu-id="165f9-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="165f9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="165f9-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="165f9-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="165f9-130">입력</span><span class="sxs-lookup"><span data-stu-id="165f9-130">INPUTS</span></span>

### <span data-ttu-id="165f9-131">않아야</span><span class="sxs-lookup"><span data-stu-id="165f9-131">None</span></span>

## <span data-ttu-id="165f9-132">출력</span><span class="sxs-lookup"><span data-stu-id="165f9-132">OUTPUTS</span></span>

### <span data-ttu-id="165f9-133">PSVpnClientRevokedCertificate에 대 한.</span><span class="sxs-lookup"><span data-stu-id="165f9-133">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="165f9-134">상속자</span><span class="sxs-lookup"><span data-stu-id="165f9-134">NOTES</span></span>

## <span data-ttu-id="165f9-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="165f9-135">RELATED LINKS</span></span>

[<span data-ttu-id="165f9-136">추가-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="165f9-136">Add-AzureRmVpnClientRevokedCertificate</span></span>](./Add-AzureRmVpnClientRevokedCertificate.md)

[<span data-ttu-id="165f9-137">Get-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="165f9-137">Get-AzureRmVpnClientRevokedCertificate</span></span>](./Get-AzureRmVpnClientRevokedCertificate.md)

[<span data-ttu-id="165f9-138">제거-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="165f9-138">Remove-AzureRmVpnClientRevokedCertificate</span></span>](./Remove-AzureRmVpnClientRevokedCertificate.md)


