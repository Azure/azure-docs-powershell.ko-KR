---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 973E1E53-983F-45A7-A7CF-18A8D96EC4E6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnClientRevokedCertificate.md
ms.openlocfilehash: 8e1f85cbb90e1318c6eab595ef00929ceb1a5b1e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527431"
---
# <span data-ttu-id="e2015-101">New-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="e2015-101">New-AzureRmVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="e2015-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2015-102">SYNOPSIS</span></span>
<span data-ttu-id="e2015-103">새 VPN 클라이언트 해지 인증서를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e2015-103">Creates a new VPN client-revocation certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e2015-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e2015-104">SYNTAX</span></span>

```
New-AzureRmVpnClientRevokedCertificate -Name <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e2015-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e2015-105">DESCRIPTION</span></span>
<span data-ttu-id="e2015-106">**AzureRmVpnClientRevokedCertificate** cmdlet은 가상 네트워크 게이트웨이에서 사용할 새 VPN (가상 사설망) 클라이언트 해지 인증서를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e2015-106">The **New-AzureRmVpnClientRevokedCertificate** cmdlet creates a new virtual private network (VPN) client-revocation certificate for use on a virtual network gateway.</span></span>
<span data-ttu-id="e2015-107">클라이언트 해지 인증서는 클라이언트 컴퓨터가 인증을 위해 지정 된 인증서를 사용 하지 못하도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2015-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>

<span data-ttu-id="e2015-108">이 cmdlet은 가상 게이트웨이에 할당 되지 않은 독립 실행형 인증서를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e2015-108">This cmdlet creates a stand-alone certificate that is not assigned to a virtual gateway.</span></span>
<span data-ttu-id="e2015-109">대신 새 게이트웨이를 만들 때 **AzureRmVpnClientRevokedCertificate** 에서 만든 인증서가 New-AzureRmVirtualNetworkGateway cmdlet과 함께 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e2015-109">Instead, the certificate created by **New-AzureRmVpnClientRevokedCertificate** is used in conjunction with the New-AzureRmVirtualNetworkGateway cmdlet when it creates a new gateway.</span></span>
<span data-ttu-id="e2015-110">예를 들어 새 인증서를 만들고이를 $Certificate 이라는 변수에 저장 한다고 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2015-110">For instance, suppose you create a new certificate and store it in a variable named $Certificate.</span></span>
<span data-ttu-id="e2015-111">그런 다음 새 가상 게이트웨이를 만들 때 해당 인증서 개체를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e2015-111">You can then use that certificate object when you create a new virtual gateway.</span></span>
<span data-ttu-id="e2015-112">예를 들어</span><span class="sxs-lookup"><span data-stu-id="e2015-112">For instance,</span></span>

`New-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRevokedCertificates $Certificate`

<span data-ttu-id="e2015-113">자세한 내용은 New-AzureRmVirtualNetworkGateway cmdlet에 대 한 설명서를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e2015-113">For more information, see the documentation for the New-AzureRmVirtualNetworkGateway cmdlet.</span></span>

## <span data-ttu-id="e2015-114">예제의</span><span class="sxs-lookup"><span data-stu-id="e2015-114">EXAMPLES</span></span>

### <span data-ttu-id="e2015-115">예제 1: 새 클라이언트 만들기-해지 된 인증서</span><span class="sxs-lookup"><span data-stu-id="e2015-115">Example 1: Create a new client-revoked certificate</span></span>
```
PS C:\>$Certificate = New-AzureRmVpnClientRevokedCertificate -Name "ContosoClientRevokedCertificate" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="e2015-116">이 명령은 새 클라이언트-해지 된 인증서를 만들고 $Certificate 이라는 변수에 인증서 개체를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2015-116">This command creates a new client-revoked certificate and stores the certificate object in a variable named $Certificate.</span></span>
<span data-ttu-id="e2015-117">그런 다음 새 가상 네트워크 게이트웨이에 인증서를 추가 하기 위해 **AzureRmVirtualNetworkGateway** cmdlet에서이 변수를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e2015-117">This variable can then be used by the **New-AzureRmVirtualNetworkGateway** cmdlet to add the certificate to a new virtual network gateway.</span></span>

## <span data-ttu-id="e2015-118">변수</span><span class="sxs-lookup"><span data-stu-id="e2015-118">PARAMETERS</span></span>

### <span data-ttu-id="e2015-119">-이름</span><span class="sxs-lookup"><span data-stu-id="e2015-119">-Name</span></span>
<span data-ttu-id="e2015-120">새 클라이언트 해지 인증서의 고유한 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2015-120">Specifies a unique name for the new client-revocation certificate.</span></span>

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

### <span data-ttu-id="e2015-121">-지문</span><span class="sxs-lookup"><span data-stu-id="e2015-121">-Thumbprint</span></span>
<span data-ttu-id="e2015-122">추가할 인증서의 고유 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2015-122">Specifies the unique identifier of the certificate being added.</span></span>

<span data-ttu-id="e2015-123">다음과 같은 Windows PowerShell 명령을 사용 하 여 인증서에 대 한 지문 정보를 반환할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e2015-123">You can return thumbprint information for your certificates by using a Windows PowerShell command similar to this:</span></span>

`Get-ChildItem -Path Cert:\LocalMachine\Root`

<span data-ttu-id="e2015-124">앞의 명령은 루트 인증서 저장소에 있는 모든 로컬 컴퓨터 인증서에 대 한 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2015-124">The preceding command returns information for all the Local Computer certificates found in the Root certificate store.</span></span>

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

### <span data-ttu-id="e2015-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2015-125">-DefaultProfile</span></span>
<span data-ttu-id="e2015-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e2015-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e2015-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2015-127">CommonParameters</span></span>
<span data-ttu-id="e2015-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2015-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2015-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2015-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2015-130">입력</span><span class="sxs-lookup"><span data-stu-id="e2015-130">INPUTS</span></span>

###  
<span data-ttu-id="e2015-131">이 cmdlet은 파이프라인 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e2015-131">This cmdlet does not accept pipelined input.</span></span>

## <span data-ttu-id="e2015-132">출력</span><span class="sxs-lookup"><span data-stu-id="e2015-132">OUTPUTS</span></span>

###  
<span data-ttu-id="e2015-133">이 cmdlet은 **PSVpnClientRevokedCertificate** 개체의 새 인스턴스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e2015-133">This cmdlet creates new instances of the **Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate** object.</span></span>

## <span data-ttu-id="e2015-134">상속자</span><span class="sxs-lookup"><span data-stu-id="e2015-134">NOTES</span></span>

## <span data-ttu-id="e2015-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e2015-135">RELATED LINKS</span></span>

[<span data-ttu-id="e2015-136">추가-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="e2015-136">Add-AzureRmVpnClientRevokedCertificate</span></span>](./Add-AzureRmVpnClientRevokedCertificate.md)

[<span data-ttu-id="e2015-137">Get-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="e2015-137">Get-AzureRmVpnClientRevokedCertificate</span></span>](./Get-AzureRmVpnClientRevokedCertificate.md)

[<span data-ttu-id="e2015-138">제거-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="e2015-138">Remove-AzureRmVpnClientRevokedCertificate</span></span>](./Remove-AzureRmVpnClientRevokedCertificate.md)


