---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 90FB7B88-844E-4783-A10F-04D7BA47C030
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVpnClientRevokedCertificate.md
ms.openlocfilehash: c73f65866b2a23527540319744854e50f6639268
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703691"
---
# <span data-ttu-id="a434e-101">Add-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="a434e-101">Add-AzureRmVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="a434e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a434e-102">SYNOPSIS</span></span>
<span data-ttu-id="a434e-103">VPN 클라이언트 해지 인증서를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="a434e-103">Adds a VPN client-revocation certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a434e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a434e-104">SYNTAX</span></span>

```
Add-AzureRmVpnClientRevokedCertificate -VpnClientRevokedCertificateName <String>
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a434e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a434e-105">DESCRIPTION</span></span>
<span data-ttu-id="a434e-106">**Add-AzureRmVpnClientRevokedCertificate** cmdlet은 가상 네트워크 게이트웨이에 클라이언트 해지 인증서를 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="a434e-106">The **Add-AzureRmVpnClientRevokedCertificate** cmdlet assigns a client-revocation certificate to a virtual network gateway.</span></span>
<span data-ttu-id="a434e-107">클라이언트 해지 인증서는 클라이언트 컴퓨터가 인증을 위해 지정 된 인증서를 사용 하지 못하도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="a434e-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="a434e-108">이 cmdlet을 사용 하려면 인증서 이름과 인증서 지문을 모두 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a434e-108">You need to specify both the certificate name and the certificate thumbprint to use this cmdlet.</span></span>

## <span data-ttu-id="a434e-109">예제의</span><span class="sxs-lookup"><span data-stu-id="a434e-109">EXAMPLES</span></span>

### <span data-ttu-id="a434e-110">예제 1: 가상 네트워크 게이트웨이에 새 클라이언트-해지 인증서 추가</span><span class="sxs-lookup"><span data-stu-id="a434e-110">Example 1: Add a new client-revocation certificate to a virtual network gateway</span></span>
```
PS C:\>Add-AzureRmVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate"-Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="a434e-111">이 명령은 ContosoVirtualNetwork 이라는 가상 네트워크 게이트웨이에 새 클라이언트 해지 인증서를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="a434e-111">This command adds a new client-revocation certificate to the virtual network gateway named ContosoVirtualNetwork.</span></span>
<span data-ttu-id="a434e-112">인증서를 추가 하려면 인증서 이름과 인증서 지문을 모두 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a434e-112">In order to add the certificate, you must specify both the certificate name and the certificate thumbprint.</span></span>

## <span data-ttu-id="a434e-113">변수</span><span class="sxs-lookup"><span data-stu-id="a434e-113">PARAMETERS</span></span>

### <span data-ttu-id="a434e-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a434e-114">-ResourceGroupName</span></span>
<span data-ttu-id="a434e-115">가상 네트워크 게이트웨이가 할당 되는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a434e-115">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>

<span data-ttu-id="a434e-116">리소스 그룹은 인벤터리 관리 및 일반 Azure 관리를 간소화 하기 위해 항목을 분류 합니다.</span><span class="sxs-lookup"><span data-stu-id="a434e-116">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="a434e-117">-지문</span><span class="sxs-lookup"><span data-stu-id="a434e-117">-Thumbprint</span></span>
<span data-ttu-id="a434e-118">추가할 인증서의 고유 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a434e-118">Specifies the unique identifier of the certificate being added.</span></span>
<span data-ttu-id="a434e-119">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="a434e-119">For example:</span></span>

<span data-ttu-id="a434e-120">-지문 "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"</span><span class="sxs-lookup"><span data-stu-id="a434e-120">-Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"</span></span>

<span data-ttu-id="a434e-121">다음과 같은 Windows PowerShell 명령을 사용 하 여 인증서에 대 한 지문 정보를 가져올 수 있습니다 `Get-ChildItem -Path Cert:\LocalMachine\Root` .</span><span class="sxs-lookup"><span data-stu-id="a434e-121">You can get thumbprint information for your certificates by using a Windows PowerShell command similar to this: `Get-ChildItem -Path Cert:\LocalMachine\Root`.</span></span>

<span data-ttu-id="a434e-122">앞의 명령은 루트 인증서 저장소에 있는 모든 로컬 컴퓨터 인증서에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a434e-122">The preceding command gets information for all the local computer certificates found in the root certificate store.</span></span>

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

### <span data-ttu-id="a434e-123">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="a434e-123">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="a434e-124">인증서를 추가 해야 하는 가상 네트워크 게이트웨이의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a434e-124">Specifies the name of the virtual network gateway where the certificate should be added.</span></span>

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

### <span data-ttu-id="a434e-125">-VpnClientRevokedCertificateName</span><span class="sxs-lookup"><span data-stu-id="a434e-125">-VpnClientRevokedCertificateName</span></span>
<span data-ttu-id="a434e-126">추가할 VPN 클라이언트 인증서의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a434e-126">Specifies the name of the VPN client certificate to be added.</span></span>

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

### <span data-ttu-id="a434e-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a434e-127">-DefaultProfile</span></span>
<span data-ttu-id="a434e-128">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a434e-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a434e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a434e-129">CommonParameters</span></span>
<span data-ttu-id="a434e-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a434e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a434e-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a434e-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a434e-132">입력</span><span class="sxs-lookup"><span data-stu-id="a434e-132">INPUTS</span></span>

## <span data-ttu-id="a434e-133">출력</span><span class="sxs-lookup"><span data-stu-id="a434e-133">OUTPUTS</span></span>

### <span data-ttu-id="a434e-134">PSVpnClientRevokedCertificate에 대 한.</span><span class="sxs-lookup"><span data-stu-id="a434e-134">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="a434e-135">상속자</span><span class="sxs-lookup"><span data-stu-id="a434e-135">NOTES</span></span>

## <span data-ttu-id="a434e-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a434e-136">RELATED LINKS</span></span>

[<span data-ttu-id="a434e-137">Get-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="a434e-137">Get-AzureRmVpnClientRevokedCertificate</span></span>](./Get-AzureRmVpnClientRevokedCertificate.md)

[<span data-ttu-id="a434e-138">새로운 AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="a434e-138">New-AzureRmVpnClientRevokedCertificate</span></span>](./New-AzureRmVpnClientRevokedCertificate.md)

[<span data-ttu-id="a434e-139">제거-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="a434e-139">Remove-AzureRmVpnClientRevokedCertificate</span></span>](./Remove-AzureRmVpnClientRevokedCertificate.md)


