---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 90FB7B88-844E-4783-A10F-04D7BA47C030
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVpnClientRevokedCertificate.md
ms.openlocfilehash: 041fc967bc5834ba21f96e75e2f5cdc3687d234c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93870317"
---
# <span data-ttu-id="9cae3-101">Add-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="9cae3-101">Add-AzVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="9cae3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9cae3-102">SYNOPSIS</span></span>
<span data-ttu-id="9cae3-103">VPN 클라이언트 해지 인증서를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="9cae3-103">Adds a VPN client-revocation certificate.</span></span>

## <span data-ttu-id="9cae3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9cae3-104">SYNTAX</span></span>

```
Add-AzVpnClientRevokedCertificate -VpnClientRevokedCertificateName <String> -VirtualNetworkGatewayName <String>
 -ResourceGroupName <String> -Thumbprint <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9cae3-105">설명은</span><span class="sxs-lookup"><span data-stu-id="9cae3-105">DESCRIPTION</span></span>
<span data-ttu-id="9cae3-106">**Add-AzVpnClientRevokedCertificate** cmdlet은 가상 네트워크 게이트웨이에 클라이언트 해지 인증서를 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="9cae3-106">The **Add-AzVpnClientRevokedCertificate** cmdlet assigns a client-revocation certificate to a virtual network gateway.</span></span>
<span data-ttu-id="9cae3-107">클라이언트 해지 인증서는 클라이언트 컴퓨터가 인증을 위해 지정 된 인증서를 사용 하지 못하도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="9cae3-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="9cae3-108">이 cmdlet을 사용 하려면 인증서 이름과 인증서 지문을 모두 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9cae3-108">You need to specify both the certificate name and the certificate thumbprint to use this cmdlet.</span></span>

## <span data-ttu-id="9cae3-109">예제의</span><span class="sxs-lookup"><span data-stu-id="9cae3-109">EXAMPLES</span></span>

### <span data-ttu-id="9cae3-110">예제 1: 가상 네트워크 게이트웨이에 새 클라이언트-해지 인증서 추가</span><span class="sxs-lookup"><span data-stu-id="9cae3-110">Example 1: Add a new client-revocation certificate to a virtual network gateway</span></span>
```
PS C:\>Add-AzVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate"-Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="9cae3-111">이 명령은 ContosoVirtualNetwork 이라는 가상 네트워크 게이트웨이에 새 클라이언트 해지 인증서를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="9cae3-111">This command adds a new client-revocation certificate to the virtual network gateway named ContosoVirtualNetwork.</span></span>
<span data-ttu-id="9cae3-112">인증서를 추가 하려면 인증서 이름과 인증서 지문을 모두 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9cae3-112">In order to add the certificate, you must specify both the certificate name and the certificate thumbprint.</span></span>

## <span data-ttu-id="9cae3-113">변수</span><span class="sxs-lookup"><span data-stu-id="9cae3-113">PARAMETERS</span></span>

### <span data-ttu-id="9cae3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cae3-114">-DefaultProfile</span></span>
<span data-ttu-id="9cae3-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9cae3-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9cae3-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9cae3-116">-ResourceGroupName</span></span>
<span data-ttu-id="9cae3-117">가상 네트워크 게이트웨이가 할당 되는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9cae3-117">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>
<span data-ttu-id="9cae3-118">리소스 그룹은 인벤터리 관리 및 일반 Azure 관리를 간소화 하기 위해 항목을 분류 합니다.</span><span class="sxs-lookup"><span data-stu-id="9cae3-118">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="9cae3-119">-지문</span><span class="sxs-lookup"><span data-stu-id="9cae3-119">-Thumbprint</span></span>
<span data-ttu-id="9cae3-120">추가할 인증서의 고유 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9cae3-120">Specifies the unique identifier of the certificate being added.</span></span>
<span data-ttu-id="9cae3-121">예:-손도장 "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3" 다음과 유사한 Windows PowerShell 명령을 사용 하 여 인증서에 대 한 지문 정보를 얻을 수 있습니다 `Get-ChildItem -Path Cert:\LocalMachine\Root` .</span><span class="sxs-lookup"><span data-stu-id="9cae3-121">For example: -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3" You can get thumbprint information for your certificates by using a Windows PowerShell command similar to this: `Get-ChildItem -Path Cert:\LocalMachine\Root`.</span></span>
<span data-ttu-id="9cae3-122">앞의 명령은 루트 인증서 저장소에 있는 모든 로컬 컴퓨터 인증서에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9cae3-122">The preceding command gets information for all the local computer certificates found in the root certificate store.</span></span>

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

### <span data-ttu-id="9cae3-123">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="9cae3-123">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="9cae3-124">인증서를 추가 해야 하는 가상 네트워크 게이트웨이의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9cae3-124">Specifies the name of the virtual network gateway where the certificate should be added.</span></span>

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

### <span data-ttu-id="9cae3-125">-VpnClientRevokedCertificateName</span><span class="sxs-lookup"><span data-stu-id="9cae3-125">-VpnClientRevokedCertificateName</span></span>
<span data-ttu-id="9cae3-126">추가할 VPN 클라이언트 인증서의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9cae3-126">Specifies the name of the VPN client certificate to be added.</span></span>

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

### <span data-ttu-id="9cae3-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cae3-127">CommonParameters</span></span>
<span data-ttu-id="9cae3-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9cae3-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cae3-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9cae3-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cae3-130">입력</span><span class="sxs-lookup"><span data-stu-id="9cae3-130">INPUTS</span></span>

### <span data-ttu-id="9cae3-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9cae3-131">System.String</span></span>

## <span data-ttu-id="9cae3-132">출력</span><span class="sxs-lookup"><span data-stu-id="9cae3-132">OUTPUTS</span></span>

### <span data-ttu-id="9cae3-133">PSVpnClientRevokedCertificate에 대 한.</span><span class="sxs-lookup"><span data-stu-id="9cae3-133">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="9cae3-134">상속자</span><span class="sxs-lookup"><span data-stu-id="9cae3-134">NOTES</span></span>

## <span data-ttu-id="9cae3-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9cae3-135">RELATED LINKS</span></span>

[<span data-ttu-id="9cae3-136">Get-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="9cae3-136">Get-AzVpnClientRevokedCertificate</span></span>](./Get-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="9cae3-137">새로운 AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="9cae3-137">New-AzVpnClientRevokedCertificate</span></span>](./New-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="9cae3-138">제거-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="9cae3-138">Remove-AzVpnClientRevokedCertificate</span></span>](./Remove-AzVpnClientRevokedCertificate.md)


