---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 818C2250-DE43-409E-AC68-B4A7E945401E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVpnClientRevokedCertificate.md
ms.openlocfilehash: 7c6457e30140e10c5e6746c69a213f5ac4932cc9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533952"
---
# <span data-ttu-id="b5be5-101">Remove-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="b5be5-101">Remove-AzureRmVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="b5be5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5be5-102">SYNOPSIS</span></span>
<span data-ttu-id="b5be5-103">VPN 클라이언트 해지 인증서를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5be5-103">Removes a VPN client-revocation certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b5be5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b5be5-104">SYNTAX</span></span>

```
Remove-AzureRmVpnClientRevokedCertificate -VpnClientRevokedCertificateName <String>
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b5be5-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b5be5-105">DESCRIPTION</span></span>
<span data-ttu-id="b5be5-106">**AzureRmVpnClientRevokedCertificate** cmdlet은 가상 네트워크 게이트웨이에서 클라이언트 해지 인증서를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5be5-106">The **Remove-AzureRmVpnClientRevokedCertificate** cmdlet removes a client-revocation certificate from a virtual network gateway.</span></span>
<span data-ttu-id="b5be5-107">클라이언트 해지 인증서는 클라이언트 컴퓨터가 인증을 위해 지정 된 인증서를 사용 하지 못하도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5be5-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="b5be5-108">클라이언트 철회 인증서를 제거한 경우 클라이언트 컴퓨터는 이전에 금지 된 인증서를 사용 하 여 VPN (가상 사설망) 연결을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b5be5-108">If you remove a client-revocation certificate client computers can then use the previously-banned certificate to make a virtual private network (VPN) connection.</span></span>

## <span data-ttu-id="b5be5-109">예제의</span><span class="sxs-lookup"><span data-stu-id="b5be5-109">EXAMPLES</span></span>

### <span data-ttu-id="b5be5-110">예제 1: 가상 네트워크 게이트웨이에서 클라이언트 해지 인증서 제거</span><span class="sxs-lookup"><span data-stu-id="b5be5-110">Example 1: Remove a client-revocation certificate from a virtual network gateway</span></span>
```
PS C:\>Remove-AzureRmVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName"ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate"-Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="b5be5-111">이 명령은 ContosoVirtualNetwork 이라는 가상 네트워크 게이트웨이에서 클라이언트 해지 인증서를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5be5-111">This command removes a client-revocation certificate from a virtual network gateway named ContosoVirtualNetwork.</span></span>
<span data-ttu-id="b5be5-112">클라이언트 해지 인증서를 제거 하려면 인증서 이름과 인증서 지문을 모두 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5be5-112">In order to remove a client-revocation certificate, you must specify both the certificate name and the certificate thumbprint.</span></span>

## <span data-ttu-id="b5be5-113">변수</span><span class="sxs-lookup"><span data-stu-id="b5be5-113">PARAMETERS</span></span>

### <span data-ttu-id="b5be5-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5be5-114">-ResourceGroupName</span></span>
<span data-ttu-id="b5be5-115">가상 네트워크 게이트웨이가 할당 되는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5be5-115">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>

<span data-ttu-id="b5be5-116">리소스 그룹은 인벤터리 관리 및 일반 Azure 관리를 간소화 하기 위해 항목을 분류 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5be5-116">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="b5be5-117">-지문</span><span class="sxs-lookup"><span data-stu-id="b5be5-117">-Thumbprint</span></span>
<span data-ttu-id="b5be5-118">제거할 인증서의 고유 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5be5-118">Specifies the unique identifier of the certificate being removed.</span></span>

<span data-ttu-id="b5be5-119">다음과 같은 Windows PowerShell 명령을 사용 하 여 인증서에 대 한 지문 정보를 반환할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b5be5-119">You can return thumbprint information for your certificates by using a Windows PowerShell command similar to this:</span></span>

`Get-ChildItem -Path "Cert:\LocalMachine\Root"`

<span data-ttu-id="b5be5-120">앞의 명령은 루트 인증서 저장소에 있는 모든 로컬 컴퓨터 인증서에 대 한 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5be5-120">The preceding command returns information for all the Local Computer certificates found in the Root certificate store.</span></span>

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

### <span data-ttu-id="b5be5-121">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="b5be5-121">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="b5be5-122">인증서가 할당 된 가상 네트워크 게이트웨이의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5be5-122">Specifies the name of the virtual network gateway that the certificate is assigned to.</span></span>

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

### <span data-ttu-id="b5be5-123">-VpnClientRevokedCertificateName</span><span class="sxs-lookup"><span data-stu-id="b5be5-123">-VpnClientRevokedCertificateName</span></span>
<span data-ttu-id="b5be5-124">제거할 VPN 클라이언트 인증서의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5be5-124">Specifies the name of the VPN client certificate being removed.</span></span>

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

### <span data-ttu-id="b5be5-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5be5-125">-DefaultProfile</span></span>
<span data-ttu-id="b5be5-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b5be5-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b5be5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5be5-127">CommonParameters</span></span>
<span data-ttu-id="b5be5-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5be5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5be5-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5be5-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5be5-130">입력</span><span class="sxs-lookup"><span data-stu-id="b5be5-130">INPUTS</span></span>

## <span data-ttu-id="b5be5-131">출력</span><span class="sxs-lookup"><span data-stu-id="b5be5-131">OUTPUTS</span></span>

## <span data-ttu-id="b5be5-132">상속자</span><span class="sxs-lookup"><span data-stu-id="b5be5-132">NOTES</span></span>

## <span data-ttu-id="b5be5-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b5be5-133">RELATED LINKS</span></span>

[<span data-ttu-id="b5be5-134">추가-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="b5be5-134">Add-AzureRmVpnClientRevokedCertificate</span></span>](./Add-AzureRmVpnClientRevokedCertificate.md)

[<span data-ttu-id="b5be5-135">Get-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="b5be5-135">Get-AzureRmVpnClientRevokedCertificate</span></span>](./Get-AzureRmVpnClientRevokedCertificate.md)

[<span data-ttu-id="b5be5-136">새로운 AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="b5be5-136">New-AzureRmVpnClientRevokedCertificate</span></span>](./New-AzureRmVpnClientRevokedCertificate.md)


