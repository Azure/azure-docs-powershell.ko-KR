---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 818C2250-DE43-409E-AC68-B4A7E945401E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientRevokedCertificate.md
ms.openlocfilehash: 861ea7bcfbfbe8a713934e2dc80a4448a2a98c48
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869646"
---
# <span data-ttu-id="f08c5-101">Remove-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="f08c5-101">Remove-AzVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="f08c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f08c5-102">SYNOPSIS</span></span>
<span data-ttu-id="f08c5-103">VPN 클라이언트 해지 인증서를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="f08c5-103">Removes a VPN client-revocation certificate.</span></span>

## <span data-ttu-id="f08c5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f08c5-104">SYNTAX</span></span>

```
Remove-AzVpnClientRevokedCertificate -VpnClientRevokedCertificateName <String>
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f08c5-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f08c5-105">DESCRIPTION</span></span>
<span data-ttu-id="f08c5-106">**AzVpnClientRevokedCertificate** cmdlet은 가상 네트워크 게이트웨이에서 클라이언트 해지 인증서를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="f08c5-106">The **Remove-AzVpnClientRevokedCertificate** cmdlet removes a client-revocation certificate from a virtual network gateway.</span></span>
<span data-ttu-id="f08c5-107">클라이언트 해지 인증서는 클라이언트 컴퓨터가 인증을 위해 지정 된 인증서를 사용 하지 못하도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="f08c5-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="f08c5-108">클라이언트 철회 인증서를 제거한 경우 클라이언트 컴퓨터는 이전에 금지 된 인증서를 사용 하 여 VPN (가상 사설망) 연결을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f08c5-108">If you remove a client-revocation certificate client computers can then use the previously-banned certificate to make a virtual private network (VPN) connection.</span></span>

## <span data-ttu-id="f08c5-109">예제의</span><span class="sxs-lookup"><span data-stu-id="f08c5-109">EXAMPLES</span></span>

### <span data-ttu-id="f08c5-110">예제 1: 가상 네트워크 게이트웨이에서 클라이언트 해지 인증서 제거</span><span class="sxs-lookup"><span data-stu-id="f08c5-110">Example 1: Remove a client-revocation certificate from a virtual network gateway</span></span>
```
PS C:\>Remove-AzVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName"ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate"-Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="f08c5-111">이 명령은 ContosoVirtualNetwork 이라는 가상 네트워크 게이트웨이에서 클라이언트 해지 인증서를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="f08c5-111">This command removes a client-revocation certificate from a virtual network gateway named ContosoVirtualNetwork.</span></span>
<span data-ttu-id="f08c5-112">클라이언트 해지 인증서를 제거 하려면 인증서 이름과 인증서 지문을 모두 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f08c5-112">In order to remove a client-revocation certificate, you must specify both the certificate name and the certificate thumbprint.</span></span>

## <span data-ttu-id="f08c5-113">변수</span><span class="sxs-lookup"><span data-stu-id="f08c5-113">PARAMETERS</span></span>

### <span data-ttu-id="f08c5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f08c5-114">-DefaultProfile</span></span>
<span data-ttu-id="f08c5-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f08c5-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f08c5-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f08c5-116">-ResourceGroupName</span></span>
<span data-ttu-id="f08c5-117">가상 네트워크 게이트웨이가 할당 되는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f08c5-117">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>
<span data-ttu-id="f08c5-118">리소스 그룹은 인벤터리 관리 및 일반 Azure 관리를 간소화 하기 위해 항목을 분류 합니다.</span><span class="sxs-lookup"><span data-stu-id="f08c5-118">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="f08c5-119">-지문</span><span class="sxs-lookup"><span data-stu-id="f08c5-119">-Thumbprint</span></span>
<span data-ttu-id="f08c5-120">제거할 인증서의 고유 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f08c5-120">Specifies the unique identifier of the certificate being removed.</span></span>
<span data-ttu-id="f08c5-121">다음과 같은 Windows PowerShell 명령을 사용 하 여 인증서에 대 한 지문 정보를 반환할 수 있습니다. `Get-ChildItem -Path "Cert:\LocalMachine\Root"`</span><span class="sxs-lookup"><span data-stu-id="f08c5-121">You can return thumbprint information for your certificates by using a Windows PowerShell command similar to this: `Get-ChildItem -Path "Cert:\LocalMachine\Root"`</span></span>
<span data-ttu-id="f08c5-122">앞의 명령은 루트 인증서 저장소에 있는 모든 로컬 컴퓨터 인증서에 대 한 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="f08c5-122">The preceding command returns information for all the Local Computer certificates found in the Root certificate store.</span></span>

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

### <span data-ttu-id="f08c5-123">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="f08c5-123">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="f08c5-124">인증서가 할당 된 가상 네트워크 게이트웨이의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f08c5-124">Specifies the name of the virtual network gateway that the certificate is assigned to.</span></span>

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

### <span data-ttu-id="f08c5-125">-VpnClientRevokedCertificateName</span><span class="sxs-lookup"><span data-stu-id="f08c5-125">-VpnClientRevokedCertificateName</span></span>
<span data-ttu-id="f08c5-126">제거할 VPN 클라이언트 인증서의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f08c5-126">Specifies the name of the VPN client certificate being removed.</span></span>

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

### <span data-ttu-id="f08c5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f08c5-127">CommonParameters</span></span>
<span data-ttu-id="f08c5-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f08c5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f08c5-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f08c5-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f08c5-130">입력</span><span class="sxs-lookup"><span data-stu-id="f08c5-130">INPUTS</span></span>

### <span data-ttu-id="f08c5-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f08c5-131">System.String</span></span>

## <span data-ttu-id="f08c5-132">출력</span><span class="sxs-lookup"><span data-stu-id="f08c5-132">OUTPUTS</span></span>

### <span data-ttu-id="f08c5-133">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="f08c5-133">System.Boolean</span></span>

## <span data-ttu-id="f08c5-134">상속자</span><span class="sxs-lookup"><span data-stu-id="f08c5-134">NOTES</span></span>

## <span data-ttu-id="f08c5-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f08c5-135">RELATED LINKS</span></span>

[<span data-ttu-id="f08c5-136">추가-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="f08c5-136">Add-AzVpnClientRevokedCertificate</span></span>](./Add-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="f08c5-137">Get-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="f08c5-137">Get-AzVpnClientRevokedCertificate</span></span>](./Get-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="f08c5-138">새로운 AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="f08c5-138">New-AzVpnClientRevokedCertificate</span></span>](./New-AzVpnClientRevokedCertificate.md)


