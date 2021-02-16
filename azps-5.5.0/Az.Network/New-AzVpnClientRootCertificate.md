---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C54AC64C-DA21-443E-8CFE-6CCAC6152C2B
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRootCertificate.md
ms.openlocfilehash: 379ba58abe2d7a697c7dca5bdb31bc222159d367
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191833"
---
# <span data-ttu-id="cf89d-101">New-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="cf89d-101">New-AzVpnClientRootCertificate</span></span>

## <span data-ttu-id="cf89d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf89d-102">SYNOPSIS</span></span>
<span data-ttu-id="cf89d-103">새 VPN 클라이언트 루트 인증서를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="cf89d-103">Creates a new VPN client root certificate.</span></span>

## <span data-ttu-id="cf89d-104">구문</span><span class="sxs-lookup"><span data-stu-id="cf89d-104">SYNTAX</span></span>

```
New-AzVpnClientRootCertificate -Name <String> -PublicCertData <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cf89d-105">설명</span><span class="sxs-lookup"><span data-stu-id="cf89d-105">DESCRIPTION</span></span>
<span data-ttu-id="cf89d-106">**New-AzVpnClientRootCertificate** cmdlet은 가상 네트워크 게이트웨이에서 사용할 새 VPN 루트 인증서를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="cf89d-106">The **New-AzVpnClientRootCertificate** cmdlet creates a new VPN root certificate for use on a virtual network gateway.</span></span>
<span data-ttu-id="cf89d-107">루트 인증서는 루트 인증 기관을 식별하는 X.509 인증서입니다. 게이트웨이에서 사용되는 다른 모든 인증서는 루트 인증서를 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="cf89d-107">Root certificates are X.509 certificates that identify your Root Certification Authority: all other certificates used on the gateway trust the root certificate.</span></span>
<span data-ttu-id="cf89d-108">이 cmdlet은 가상 게이트웨이에 할당되지 않은 독립 실행형 인증서를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="cf89d-108">This cmdlet creates a stand-alone certificate that is not assigned to a virtual gateway.</span></span>
<span data-ttu-id="cf89d-109">대신 **New-AzVpnClientRootCertificate에서** 만든 인증서는 새 게이트웨이를 만들 때 New-AzVirtualNetworkGateway cmdlet과 함께 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="cf89d-109">Instead, the certificate created by **New-AzVpnClientRootCertificate** is used in conjunction with the New-AzVirtualNetworkGateway cmdlet when creating a new gateway.</span></span>
<span data-ttu-id="cf89d-110">예를 들어 새 인증서를 만들고 새 인증서를 새 인증서라는 변수에 저장했다고 $Certificate.</span><span class="sxs-lookup"><span data-stu-id="cf89d-110">For example, suppose you create a new certificate and store it in a variable named $Certificate.</span></span>
<span data-ttu-id="cf89d-111">그런 다음 새 가상 게이트웨이를 만들 때 해당 인증서 개체를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cf89d-111">You can then use that certificate object when creating a new virtual gateway.</span></span>
<span data-ttu-id="cf89d-112">예를 들어 `New-AzVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRootCertificates $Certificate`</span><span class="sxs-lookup"><span data-stu-id="cf89d-112">For instance, `New-AzVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRootCertificates $Certificate`</span></span>
<span data-ttu-id="cf89d-113">자세한 내용은 New-AzVirtualNetworkGateway cmdlet에 대한 설명서를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="cf89d-113">For more information, see the documentation for the New-AzVirtualNetworkGateway cmdlet.</span></span>

## <span data-ttu-id="cf89d-114">예제</span><span class="sxs-lookup"><span data-stu-id="cf89d-114">EXAMPLES</span></span>

### <span data-ttu-id="cf89d-115">예제 1: 클라이언트 루트 인증서 만들기</span><span class="sxs-lookup"><span data-stu-id="cf89d-115">Example 1: Create a client root certificate</span></span>
```
PS C:\> $Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> $Certificate = New-AzVpnClientRootCertificate -PublicCertData $CertificateText -Name "ContosoClientRootCertificate"
```

<span data-ttu-id="cf89d-116">이 예제에서는 클라이언트 루트 인증서를 만들고 인증서 개체를 $Certificate.</span><span class="sxs-lookup"><span data-stu-id="cf89d-116">This example creates a client root certificate and store the certificate object in a variable named $Certificate.</span></span>
<span data-ttu-id="cf89d-117">그런 다음 **New-AzVirtualNetworkGateway** cmdlet에서 이 변수를 사용하여 새 가상 네트워크 게이트웨이에 루트 인증서를 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cf89d-117">This variable can then be used by the **New-AzVirtualNetworkGateway** cmdlet to add a root certificate to a new virtual network gateway.</span></span>
<span data-ttu-id="cf89d-118">첫 번째 명령은 **Get-Content** cmdlet을 사용하여 루트 인증서의 이전에 내보낼 텍스트 표현을 얻게 됩니다. 텍스트 데이터는 이 변수에 $Text.</span><span class="sxs-lookup"><span data-stu-id="cf89d-118">The first command uses the **Get-Content** cmdlet to get a previously exported text representation of the root certificate; that text data is stored in a variable named $Text.</span></span>
<span data-ttu-id="cf89d-119">그런 다음, 두 번째 명령은 for 루프를 사용하여 첫 번째 줄과 마지막 줄을 제외한 모든 텍스트를 추출하여 추출된 텍스트를 $CertificateText.</span><span class="sxs-lookup"><span data-stu-id="cf89d-119">The second command then uses a for loop to extract all the text except for the first line and the last line, storing the extracted text in a variable named $CertificateText.</span></span>
<span data-ttu-id="cf89d-120">세 번째 명령은 **New-AzVpnClientRootCertificate** cmdlet을 사용하여 인증서를 만들고 만든 개체를 $Certificate.</span><span class="sxs-lookup"><span data-stu-id="cf89d-120">The third command uses the **New-AzVpnClientRootCertificate** cmdlet to create the certificate, storing the created object in a variable named $Certificate.</span></span>

## <span data-ttu-id="cf89d-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cf89d-121">PARAMETERS</span></span>

### <span data-ttu-id="cf89d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf89d-122">-DefaultProfile</span></span>
<span data-ttu-id="cf89d-123">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cf89d-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cf89d-124">-Name</span><span class="sxs-lookup"><span data-stu-id="cf89d-124">-Name</span></span>
<span data-ttu-id="cf89d-125">새 클라이언트 루트 인증서의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cf89d-125">Specifies a name for the new client root certificate.</span></span>

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

### <span data-ttu-id="cf89d-126">-PublicCertData</span><span class="sxs-lookup"><span data-stu-id="cf89d-126">-PublicCertData</span></span>
<span data-ttu-id="cf89d-127">추가할 루트 인증서의 텍스트 표현을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cf89d-127">Specifies a text representation of the root certificate to be added.</span></span>
<span data-ttu-id="cf89d-128">텍스트 표현을 얻습니다. 인증서를 .cer 형식으로 내보내고(Base64 인코딩 사용) 결과 파일을 텍스트 편집기에서 열 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cf89d-128">To obtain the text representation, export your certificate in .cer format (using Base64 encoding), then open the resulting file in a text editor.</span></span>
<span data-ttu-id="cf89d-129">이와 유사한 출력이 표시됩니다(실제 출력에는 여기에 표시된 약어 샘플보다 더 많은 텍스트 줄이 포함되어 있습니다. ----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HhgUNEW8343NMJklo 09982CVFAw8w ----- END CERTIFICATE ----- PublicCertData는 파일의 첫 번째 줄(----- BEGIN CERTIFICATE -----)과 마지막 줄(----- END CERTIFICATE -----) 사이의 모든 줄로 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cf89d-129">You should see output similar to this (note that the actual output will contain many more lines of text than the abbreviated sample shown here): ----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w ----- END CERTIFICATE ----- The PublicCertData is made up of all the lines between the first line (----- BEGIN CERTIFICATE -----) and the last line (----- END CERTIFICATE -----) in the file.</span></span>
<span data-ttu-id="cf89d-130">$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer" $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text $i } 명령을 사용하여 PublicCertD Windows PowerShell ata를 검색할 수 있습니다. \[ \]</span><span class="sxs-lookup"><span data-stu-id="cf89d-130">You can retrieve the PublicCertData by using Windows PowerShell commands similar to this: $Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer" $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text\[$i\]}</span></span>

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

### <span data-ttu-id="cf89d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf89d-131">CommonParameters</span></span>
<span data-ttu-id="cf89d-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="cf89d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf89d-133">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="cf89d-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf89d-134">입력</span><span class="sxs-lookup"><span data-stu-id="cf89d-134">INPUTS</span></span>

### <span data-ttu-id="cf89d-135">System.String</span><span class="sxs-lookup"><span data-stu-id="cf89d-135">System.String</span></span>

## <span data-ttu-id="cf89d-136">출력</span><span class="sxs-lookup"><span data-stu-id="cf89d-136">OUTPUTS</span></span>

### <span data-ttu-id="cf89d-137">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="cf89d-137">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate</span></span>

## <span data-ttu-id="cf89d-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="cf89d-138">NOTES</span></span>

## <span data-ttu-id="cf89d-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cf89d-139">RELATED LINKS</span></span>

[<span data-ttu-id="cf89d-140">Add-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="cf89d-140">Add-AzVpnClientRootCertificate</span></span>](./Add-AzVpnClientRootCertificate.md)

[<span data-ttu-id="cf89d-141">Get-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="cf89d-141">Get-AzVpnClientRootCertificate</span></span>](./Get-AzVpnClientRootCertificate.md)

[<span data-ttu-id="cf89d-142">Remove-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="cf89d-142">Remove-AzVpnClientRootCertificate</span></span>](./Remove-AzVpnClientRootCertificate.md)


