---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 90FB7B88-844E-4783-A10F-04D7BA47C030
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVpnClientRevokedCertificate.md
ms.openlocfilehash: 8e7c2b8d4e26e45fff0c81f5bf3fecd10e40cd7a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207013"
---
# <span data-ttu-id="9cc44-101">Add-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="9cc44-101">Add-AzVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="9cc44-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9cc44-102">SYNOPSIS</span></span>
<span data-ttu-id="9cc44-103">VPN 클라이언트 해지 인증서를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="9cc44-103">Adds a VPN client-revocation certificate.</span></span>

## <span data-ttu-id="9cc44-104">구문</span><span class="sxs-lookup"><span data-stu-id="9cc44-104">SYNTAX</span></span>

```
Add-AzVpnClientRevokedCertificate -VpnClientRevokedCertificateName <String> -VirtualNetworkGatewayName <String>
 -ResourceGroupName <String> -Thumbprint <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9cc44-105">설명</span><span class="sxs-lookup"><span data-stu-id="9cc44-105">DESCRIPTION</span></span>
<span data-ttu-id="9cc44-106">**Add-AzVpnClientRevokedCertificate** cmdlet은 클라이언트 해지 인증서를 가상 네트워크 게이트웨이에 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="9cc44-106">The **Add-AzVpnClientRevokedCertificate** cmdlet assigns a client-revocation certificate to a virtual network gateway.</span></span>
<span data-ttu-id="9cc44-107">클라이언트 해지 인증서는 클라이언트 컴퓨터가 인증에 지정된 인증서를 사용하지 못하도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="9cc44-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="9cc44-108">이 cmdlet을 사용하려면 인증서 이름과 인증서 지문을 모두 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9cc44-108">You need to specify both the certificate name and the certificate thumbprint to use this cmdlet.</span></span>

## <span data-ttu-id="9cc44-109">예제</span><span class="sxs-lookup"><span data-stu-id="9cc44-109">EXAMPLES</span></span>

### <span data-ttu-id="9cc44-110">예제 1: 가상 네트워크 게이트웨이에 새 클라이언트 해지 인증서 추가</span><span class="sxs-lookup"><span data-stu-id="9cc44-110">Example 1: Add a new client-revocation certificate to a virtual network gateway</span></span>
```powershell
PS C:\>Add-AzVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="9cc44-111">이 명령은 ContosoVirtualNetwork라는 가상 네트워크 게이트웨이에 새 클라이언트 해지 인증서를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="9cc44-111">This command adds a new client-revocation certificate to the virtual network gateway named ContosoVirtualNetwork.</span></span>
<span data-ttu-id="9cc44-112">인증서를 추가하려면 인증서 이름과 인증서 지문을 모두 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9cc44-112">In order to add the certificate, you must specify both the certificate name and the certificate thumbprint.</span></span>

## <span data-ttu-id="9cc44-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9cc44-113">PARAMETERS</span></span>

### <span data-ttu-id="9cc44-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cc44-114">-DefaultProfile</span></span>
<span data-ttu-id="9cc44-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9cc44-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9cc44-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9cc44-116">-ResourceGroupName</span></span>
<span data-ttu-id="9cc44-117">가상 네트워크 게이트웨이가 할당된 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9cc44-117">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>
<span data-ttu-id="9cc44-118">리소스 그룹은 재고 관리 및 일반 Azure 관리를 간소화하는 데 도움이 되는 항목을 분류합니다.</span><span class="sxs-lookup"><span data-stu-id="9cc44-118">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="9cc44-119">-Thumbprint</span><span class="sxs-lookup"><span data-stu-id="9cc44-119">-Thumbprint</span></span>
<span data-ttu-id="9cc44-120">추가할 인증서의 고유 식별자를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9cc44-120">Specifies the unique identifier of the certificate being added.</span></span>
<span data-ttu-id="9cc44-121">예: -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3" 다음과 유사한 Windows PowerShell 명령을 사용하여 인증서에 대한 지문 정보를 얻을 수 `Get-ChildItem -Path Cert:\LocalMachine\Root` 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9cc44-121">For example: -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3" You can get thumbprint information for your certificates by using a Windows PowerShell command similar to this: `Get-ChildItem -Path Cert:\LocalMachine\Root`.</span></span>
<span data-ttu-id="9cc44-122">이전 명령은 루트 인증서 저장소에 있는 모든 로컬 컴퓨터 인증서에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="9cc44-122">The preceding command gets information for all the local computer certificates found in the root certificate store.</span></span>

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

### <span data-ttu-id="9cc44-123">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="9cc44-123">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="9cc44-124">인증서를 추가해야 하는 가상 네트워크 게이트웨이의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9cc44-124">Specifies the name of the virtual network gateway where the certificate should be added.</span></span>

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

### <span data-ttu-id="9cc44-125">-VpnClientRevokedCertificateName</span><span class="sxs-lookup"><span data-stu-id="9cc44-125">-VpnClientRevokedCertificateName</span></span>
<span data-ttu-id="9cc44-126">추가할 VPN 클라이언트 인증서의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9cc44-126">Specifies the name of the VPN client certificate to be added.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cc44-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cc44-127">CommonParameters</span></span>
<span data-ttu-id="9cc44-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9cc44-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cc44-129">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="9cc44-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cc44-130">입력</span><span class="sxs-lookup"><span data-stu-id="9cc44-130">INPUTS</span></span>

### <span data-ttu-id="9cc44-131">System.String</span><span class="sxs-lookup"><span data-stu-id="9cc44-131">System.String</span></span>

## <span data-ttu-id="9cc44-132">출력</span><span class="sxs-lookup"><span data-stu-id="9cc44-132">OUTPUTS</span></span>

### <span data-ttu-id="9cc44-133">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="9cc44-133">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="9cc44-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9cc44-134">NOTES</span></span>

## <span data-ttu-id="9cc44-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9cc44-135">RELATED LINKS</span></span>

[<span data-ttu-id="9cc44-136">Get-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="9cc44-136">Get-AzVpnClientRevokedCertificate</span></span>](./Get-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="9cc44-137">New-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="9cc44-137">New-AzVpnClientRevokedCertificate</span></span>](./New-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="9cc44-138">Remove-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="9cc44-138">Remove-AzVpnClientRevokedCertificate</span></span>](./Remove-AzVpnClientRevokedCertificate.md)


