---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 818C2250-DE43-409E-AC68-B4A7E945401E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvpnclientrevokedcertificate
schema: 2.0.0
ms.openlocfilehash: ce4d2c61feb20c750d908b6f235d89dafa713e62
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882841"
---
# <span data-ttu-id="a5fc4-101">Remove-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="a5fc4-101">Remove-AzureRmVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="a5fc4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5fc4-102">SYNOPSIS</span></span>
<span data-ttu-id="a5fc4-103">VPN 클라이언트 해지 인증서를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fc4-103">Removes a VPN client-revocation certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a5fc4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a5fc4-104">SYNTAX</span></span>

```
Remove-AzureRmVpnClientRevokedCertificate -VpnClientRevokedCertificateName <String>
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a5fc4-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a5fc4-105">DESCRIPTION</span></span>
<span data-ttu-id="a5fc4-106">**AzureRmVpnClientRevokedCertificate** cmdlet은 가상 네트워크 게이트웨이에서 클라이언트 해지 인증서를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fc4-106">The **Remove-AzureRmVpnClientRevokedCertificate** cmdlet removes a client-revocation certificate from a virtual network gateway.</span></span>
<span data-ttu-id="a5fc4-107">클라이언트 해지 인증서는 클라이언트 컴퓨터가 인증을 위해 지정 된 인증서를 사용 하지 못하도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fc4-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="a5fc4-108">클라이언트 철회 인증서를 제거한 경우 클라이언트 컴퓨터는 이전에 금지 된 인증서를 사용 하 여 VPN (가상 사설망) 연결을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a5fc4-108">If you remove a client-revocation certificate client computers can then use the previously-banned certificate to make a virtual private network (VPN) connection.</span></span>

## <span data-ttu-id="a5fc4-109">예제의</span><span class="sxs-lookup"><span data-stu-id="a5fc4-109">EXAMPLES</span></span>

### <span data-ttu-id="a5fc4-110">예제 1: 가상 네트워크 게이트웨이에서 클라이언트 해지 인증서 제거</span><span class="sxs-lookup"><span data-stu-id="a5fc4-110">Example 1: Remove a client-revocation certificate from a virtual network gateway</span></span>
```
PS C:\>Remove-AzureRmVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName"ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate"-Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="a5fc4-111">이 명령은 ContosoVirtualNetwork 이라는 가상 네트워크 게이트웨이에서 클라이언트 해지 인증서를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fc4-111">This command removes a client-revocation certificate from a virtual network gateway named ContosoVirtualNetwork.</span></span>
<span data-ttu-id="a5fc4-112">클라이언트 해지 인증서를 제거 하려면 인증서 이름과 인증서 지문을 모두 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fc4-112">In order to remove a client-revocation certificate, you must specify both the certificate name and the certificate thumbprint.</span></span>

## <span data-ttu-id="a5fc4-113">변수</span><span class="sxs-lookup"><span data-stu-id="a5fc4-113">PARAMETERS</span></span>

### <span data-ttu-id="a5fc4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5fc4-114">-DefaultProfile</span></span>
<span data-ttu-id="a5fc4-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a5fc4-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a5fc4-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5fc4-116">-ResourceGroupName</span></span>
<span data-ttu-id="a5fc4-117">가상 네트워크 게이트웨이가 할당 되는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fc4-117">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>

<span data-ttu-id="a5fc4-118">리소스 그룹은 인벤터리 관리 및 일반 Azure 관리를 간소화 하기 위해 항목을 분류 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fc4-118">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="a5fc4-119">-지문</span><span class="sxs-lookup"><span data-stu-id="a5fc4-119">-Thumbprint</span></span>
<span data-ttu-id="a5fc4-120">제거할 인증서의 고유 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fc4-120">Specifies the unique identifier of the certificate being removed.</span></span>

<span data-ttu-id="a5fc4-121">다음과 같은 Windows PowerShell 명령을 사용 하 여 인증서에 대 한 지문 정보를 반환할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a5fc4-121">You can return thumbprint information for your certificates by using a Windows PowerShell command similar to this:</span></span>

`Get-ChildItem -Path "Cert:\LocalMachine\Root"`

<span data-ttu-id="a5fc4-122">앞의 명령은 루트 인증서 저장소에 있는 모든 로컬 컴퓨터 인증서에 대 한 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fc4-122">The preceding command returns information for all the Local Computer certificates found in the Root certificate store.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5fc4-123">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="a5fc4-123">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="a5fc4-124">인증서가 할당 된 가상 네트워크 게이트웨이의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fc4-124">Specifies the name of the virtual network gateway that the certificate is assigned to.</span></span>

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

### <span data-ttu-id="a5fc4-125">-VpnClientRevokedCertificateName</span><span class="sxs-lookup"><span data-stu-id="a5fc4-125">-VpnClientRevokedCertificateName</span></span>
<span data-ttu-id="a5fc4-126">제거할 VPN 클라이언트 인증서의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fc4-126">Specifies the name of the VPN client certificate being removed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5fc4-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5fc4-127">CommonParameters</span></span>
<span data-ttu-id="a5fc4-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fc4-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5fc4-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5fc4-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5fc4-130">입력</span><span class="sxs-lookup"><span data-stu-id="a5fc4-130">INPUTS</span></span>

## <span data-ttu-id="a5fc4-131">출력</span><span class="sxs-lookup"><span data-stu-id="a5fc4-131">OUTPUTS</span></span>

## <span data-ttu-id="a5fc4-132">상속자</span><span class="sxs-lookup"><span data-stu-id="a5fc4-132">NOTES</span></span>

## <span data-ttu-id="a5fc4-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a5fc4-133">RELATED LINKS</span></span>

[<span data-ttu-id="a5fc4-134">추가-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="a5fc4-134">Add-AzureRmVpnClientRevokedCertificate</span></span>](./Add-AzureRmVpnClientRevokedCertificate.md)

[<span data-ttu-id="a5fc4-135">Get-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="a5fc4-135">Get-AzureRmVpnClientRevokedCertificate</span></span>](./Get-AzureRmVpnClientRevokedCertificate.md)

[<span data-ttu-id="a5fc4-136">새로운 AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="a5fc4-136">New-AzureRmVpnClientRevokedCertificate</span></span>](./New-AzureRmVpnClientRevokedCertificate.md)


