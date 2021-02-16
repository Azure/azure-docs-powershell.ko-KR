---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 973E1E53-983F-45A7-A7CF-18A8D96EC4E6
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRevokedCertificate.md
ms.openlocfilehash: ba9715b6f29cd45ba25f8b2d2ab85ba0d7ef7979
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193540"
---
# <span data-ttu-id="ba85c-101">New-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="ba85c-101">New-AzVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="ba85c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba85c-102">SYNOPSIS</span></span>
<span data-ttu-id="ba85c-103">새 VPN 클라이언트 해지 인증서를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ba85c-103">Creates a new VPN client-revocation certificate.</span></span>

## <span data-ttu-id="ba85c-104">구문</span><span class="sxs-lookup"><span data-stu-id="ba85c-104">SYNTAX</span></span>

```
New-AzVpnClientRevokedCertificate -Name <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ba85c-105">설명</span><span class="sxs-lookup"><span data-stu-id="ba85c-105">DESCRIPTION</span></span>
<span data-ttu-id="ba85c-106">**New-AzVpnClientRevokedCertificate** cmdlet은 가상 네트워크 게이트웨이에서 사용할 새 VPN(가상 사설망) 클라이언트 해지 인증서를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ba85c-106">The **New-AzVpnClientRevokedCertificate** cmdlet creates a new virtual private network (VPN) client-revocation certificate for use on a virtual network gateway.</span></span>
<span data-ttu-id="ba85c-107">클라이언트 해지 인증서는 클라이언트 컴퓨터가 인증에 지정된 인증서를 사용하지 못하도록 방지합니다.</span><span class="sxs-lookup"><span data-stu-id="ba85c-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="ba85c-108">이 cmdlet은 가상 게이트웨이에 할당되지 않은 독립 실행형 인증서를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ba85c-108">This cmdlet creates a stand-alone certificate that is not assigned to a virtual gateway.</span></span>
<span data-ttu-id="ba85c-109">대신 **New-AzVpnClientRevokedCertificate에서** 만든 인증서는 새 게이트웨이를 만들 때 New-AzVirtualNetworkGateway cmdlet과 함께 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="ba85c-109">Instead, the certificate created by **New-AzVpnClientRevokedCertificate** is used in conjunction with the New-AzVirtualNetworkGateway cmdlet when it creates a new gateway.</span></span>
<span data-ttu-id="ba85c-110">예를 들어 새 인증서를 만들고 새 인증서를 새 인증서라는 변수에 $Certificate.</span><span class="sxs-lookup"><span data-stu-id="ba85c-110">For instance, suppose you create a new certificate and store it in a variable named $Certificate.</span></span>
<span data-ttu-id="ba85c-111">그런 다음 새 가상 게이트웨이를 만들 때 해당 인증서 개체를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ba85c-111">You can then use that certificate object when you create a new virtual gateway.</span></span>
<span data-ttu-id="ba85c-112">예를 들어 `New-AzVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRevokedCertificates $Certificate`</span><span class="sxs-lookup"><span data-stu-id="ba85c-112">For instance, `New-AzVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRevokedCertificates $Certificate`</span></span>
<span data-ttu-id="ba85c-113">자세한 내용은 New-AzVirtualNetworkGateway cmdlet에 대한 설명서를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="ba85c-113">For more information, see the documentation for the New-AzVirtualNetworkGateway cmdlet.</span></span>

## <span data-ttu-id="ba85c-114">예제</span><span class="sxs-lookup"><span data-stu-id="ba85c-114">EXAMPLES</span></span>

### <span data-ttu-id="ba85c-115">예제 1: 새 클라이언트 해지 인증서 만들기</span><span class="sxs-lookup"><span data-stu-id="ba85c-115">Example 1: Create a new client-revoked certificate</span></span>
```
PS C:\>$Certificate = New-AzVpnClientRevokedCertificate -Name "ContosoClientRevokedCertificate" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="ba85c-116">이 명령은 새 클라이언트 해지 인증서를 만들고 인증서 개체를 $Certificate.</span><span class="sxs-lookup"><span data-stu-id="ba85c-116">This command creates a new client-revoked certificate and stores the certificate object in a variable named $Certificate.</span></span>
<span data-ttu-id="ba85c-117">그런 다음 **New-AzVirtualNetworkGateway** cmdlet에서 이 변수를 사용하여 새 가상 네트워크 게이트웨이에 인증서를 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ba85c-117">This variable can then be used by the **New-AzVirtualNetworkGateway** cmdlet to add the certificate to a new virtual network gateway.</span></span>

## <span data-ttu-id="ba85c-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ba85c-118">PARAMETERS</span></span>

### <span data-ttu-id="ba85c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba85c-119">-DefaultProfile</span></span>
<span data-ttu-id="ba85c-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ba85c-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ba85c-121">-Name</span><span class="sxs-lookup"><span data-stu-id="ba85c-121">-Name</span></span>
<span data-ttu-id="ba85c-122">새 클라이언트 해지 인증서의 고유한 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ba85c-122">Specifies a unique name for the new client-revocation certificate.</span></span>

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

### <span data-ttu-id="ba85c-123">-Thumbprint</span><span class="sxs-lookup"><span data-stu-id="ba85c-123">-Thumbprint</span></span>
<span data-ttu-id="ba85c-124">추가할 인증서의 고유 식별자를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ba85c-124">Specifies the unique identifier of the certificate being added.</span></span>
<span data-ttu-id="ba85c-125">이와 유사한 Windows PowerShell 명령을 사용하여 인증서에 대한 지문 정보를 반환할 수 있습니다. `Get-ChildItem -Path Cert:\LocalMachine\Root`</span><span class="sxs-lookup"><span data-stu-id="ba85c-125">You can return thumbprint information for your certificates by using a Windows PowerShell command similar to this: `Get-ChildItem -Path Cert:\LocalMachine\Root`</span></span>
<span data-ttu-id="ba85c-126">이전 명령은 루트 인증서 저장소에 있는 모든 로컬 컴퓨터 인증서에 대한 정보를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="ba85c-126">The preceding command returns information for all the Local Computer certificates found in the Root certificate store.</span></span>

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

### <span data-ttu-id="ba85c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba85c-127">CommonParameters</span></span>
<span data-ttu-id="ba85c-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ba85c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba85c-129">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="ba85c-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba85c-130">입력</span><span class="sxs-lookup"><span data-stu-id="ba85c-130">INPUTS</span></span>

### <span data-ttu-id="ba85c-131">없음</span><span class="sxs-lookup"><span data-stu-id="ba85c-131">None</span></span>

## <span data-ttu-id="ba85c-132">출력</span><span class="sxs-lookup"><span data-stu-id="ba85c-132">OUTPUTS</span></span>

### <span data-ttu-id="ba85c-133">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="ba85c-133">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="ba85c-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ba85c-134">NOTES</span></span>

## <span data-ttu-id="ba85c-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ba85c-135">RELATED LINKS</span></span>

[<span data-ttu-id="ba85c-136">Add-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="ba85c-136">Add-AzVpnClientRevokedCertificate</span></span>](./Add-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="ba85c-137">Get-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="ba85c-137">Get-AzVpnClientRevokedCertificate</span></span>](./Get-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="ba85c-138">Remove-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="ba85c-138">Remove-AzVpnClientRevokedCertificate</span></span>](./Remove-AzVpnClientRevokedCertificate.md)


