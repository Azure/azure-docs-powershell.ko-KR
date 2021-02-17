---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B9153CA9-06D1-4EF3-9863-D649C2EBAEAA
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVpnClientRootCertificate.md
ms.openlocfilehash: efb8640f765468432a2927f865ce9f67c7b9164f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207005"
---
# <span data-ttu-id="912e3-101">Add-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="912e3-101">Add-AzVpnClientRootCertificate</span></span>

## <span data-ttu-id="912e3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="912e3-102">SYNOPSIS</span></span>
<span data-ttu-id="912e3-103">VPN 클라이언트 루트 인증서를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="912e3-103">Adds a VPN client root certificate.</span></span>

## <span data-ttu-id="912e3-104">구문</span><span class="sxs-lookup"><span data-stu-id="912e3-104">SYNTAX</span></span>

```
Add-AzVpnClientRootCertificate -VpnClientRootCertificateName <String> -VirtualNetworkGatewayName <String>
 -ResourceGroupName <String> -PublicCertData <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="912e3-105">설명</span><span class="sxs-lookup"><span data-stu-id="912e3-105">DESCRIPTION</span></span>
<span data-ttu-id="912e3-106">**Add-AzVpnClientRootCertificate** cmdlet은 가상 네트워크 게이트웨이에 루트 인증서를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="912e3-106">The **Add-AzVpnClientRootCertificate** cmdlet adds a root certificate to a virtual network gateway.</span></span>
<span data-ttu-id="912e3-107">루트 인증서는 루트 인증 기관을 식별하는 X.509 인증서입니다.</span><span class="sxs-lookup"><span data-stu-id="912e3-107">Root certificates are X.509 certificates that identify your Root Certification Authority.</span></span>
<span data-ttu-id="912e3-108">기본적으로 게이트웨이에서 사용되는 모든 인증서는 루트 인증서를 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="912e3-108">By design, all certificates used on the gateway trust the root certificate.</span></span>
<span data-ttu-id="912e3-109">이 cmdlet은 기존 인증서를 게이트웨이 루트 인증서로 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="912e3-109">This cmdlet assigns an existing certificate as a gateway root certificate.</span></span>
<span data-ttu-id="912e3-110">X.509 인증서를 사용할 수 없는 경우 공개 키 인프라를 통해 인증서를 생성하거나 인증서 생성기(예: makecert.exe.</span><span class="sxs-lookup"><span data-stu-id="912e3-110">If you do not have an X.509 certificate available you can generate one through your public key infrastructure or use a certificate generator such as makecert.exe.</span></span>
<span data-ttu-id="912e3-111">루트 인증서를 추가하려면 인증서 이름을 지정하고 인증서의 텍스트 전용 표현을 제공해야 합니다(자세한 내용은 *PublicCertData* 매개 변수 참조).</span><span class="sxs-lookup"><span data-stu-id="912e3-111">To add a root certificate, you must specify the certificate name and provide a text-only representation of the certificate (see *the PublicCertData* parameter for more information).</span></span>
<span data-ttu-id="912e3-112">Azure를 사용하면 게이트웨이에 두 개 이상의 루트 인증서를 할당할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="912e3-112">Azure allows you to assign more than one root certificate to a gateway.</span></span>
<span data-ttu-id="912e3-113">여러 루트 인증서는 여러 회사의 사용자를 포함 하는 조직에 의해 배포되는 경우가 종종 있습니다.</span><span class="sxs-lookup"><span data-stu-id="912e3-113">Multiple root certificates are often deployed by organizations that include users from more than one company.</span></span>

## <span data-ttu-id="912e3-114">예제</span><span class="sxs-lookup"><span data-stu-id="912e3-114">EXAMPLES</span></span>

### <span data-ttu-id="912e3-115">예제 1: 가상 게이트웨이에 클라이언트 루트 인증서 추가</span><span class="sxs-lookup"><span data-stu-id="912e3-115">Example 1: Add a client root certificate to a virtual gateway</span></span>
```
PS C:\>$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> Add-AzVpnClientRootCertificate -PublicCertData $CertificateText -ResourceGroupName "ContosoResourceGroup" -VirtualNetworkGatewayName "ContosoVirtualGateway" -VpnClientRootCertificateName "ContosoClientRootCertificate"
```

<span data-ttu-id="912e3-116">이 예제에서는 ContosoVirtualGateway라는 가상 게이트웨이에 클라이언트 루트 인증서를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="912e3-116">This example adds a client root certificate to a virtual gateway named ContosoVirtualGateway.</span></span>
<span data-ttu-id="912e3-117">첫 번째 명령은 **Get-Content** cmdlet을 사용하여 루트 인증서의 이전에 내보낼 텍스트 표현을 얻게 하여 해당 텍스트 데이터를 $Text.</span><span class="sxs-lookup"><span data-stu-id="912e3-117">The first command uses the **Get-Content** cmdlet to get a previously-exported text representation of the root certificate and stores that text data the variable named $Text.</span></span>
<span data-ttu-id="912e3-118">그런 다음, 두 번째 명령은 for 루프를 사용하여 첫 번째 줄과 마지막 줄을 제외한 모든 텍스트를 추출합니다.</span><span class="sxs-lookup"><span data-stu-id="912e3-118">The second command then uses a for loop to extract all the text except for the first line and the last line.</span></span>
<span data-ttu-id="912e3-119">추출된 텍스트는 이 변수에 $CertificateText.</span><span class="sxs-lookup"><span data-stu-id="912e3-119">The extracted text is stored in a variable named $CertificateText.</span></span>
<span data-ttu-id="912e3-120">그런 다음, 세 번째 명령은 **Add-AzVpnClientRootCertificate** cmdlet과 함께 $CertificateText 저장된 텍스트를 사용하여 루트 인증서를 게이트웨이에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="912e3-120">The third command then uses the text stored in $CertificateText with the **Add-AzVpnClientRootCertificate** cmdlet to add the root certificate to the gateway.</span></span>

## <span data-ttu-id="912e3-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="912e3-121">PARAMETERS</span></span>

### <span data-ttu-id="912e3-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="912e3-122">-DefaultProfile</span></span>
<span data-ttu-id="912e3-123">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="912e3-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="912e3-124">-PublicCertData</span><span class="sxs-lookup"><span data-stu-id="912e3-124">-PublicCertData</span></span>
<span data-ttu-id="912e3-125">추가할 루트 인증서의 텍스트 표현을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="912e3-125">Specifies the text representation of the root certificate to be added.</span></span>
<span data-ttu-id="912e3-126">텍스트 표현을 얻습니다. 인증서를 .cer 형식으로 내보내고(Base64 인코딩 사용) 결과 파일을 텍스트 편집기에서 열 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="912e3-126">To obtain the text representation, export your certificate in .cer format (using Base64 encoding), then open the resulting file in a text editor.</span></span>
<span data-ttu-id="912e3-127">이 경우 다음과 유사한 출력이 표시됩니다(실제 출력에는 여기에 표시된 약어 샘플보다 더 많은 텍스트 줄이 포함되어 있습니다. ----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HgUNEW8343NMJ end CERTIFICATE ----- END CERTIFICATE ----- PublicCertData는 파일의 첫 번째 줄(----- BEGIN CERTIFICATE -----)과 마지막 줄(----- END CERTIFICATE -----) 사이의 모든 줄로 ----- 있습니다.</span><span class="sxs-lookup"><span data-stu-id="912e3-127">When you do that, you will see output similar to the following (note that the actual output will contain many more lines of text than the abbreviated sample shown here): ----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w ----- END CERTIFICATE ----- The PublicCertData is made up of all the lines between the first line (----- BEGIN CERTIFICATE -----) and the last line (----- END CERTIFICATE -----) in the file.</span></span>
<span data-ttu-id="912e3-128">이와 유사한 명령으로 이 Windows PowerShell 검색할 수 있습니다. `$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"`
`$CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text\[$i\]}`</span><span class="sxs-lookup"><span data-stu-id="912e3-128">You can retrieve this data by using Windows PowerShell commands similar to this: `$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"`
`$CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text\[$i\]}`</span></span>

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

### <span data-ttu-id="912e3-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="912e3-129">-ResourceGroupName</span></span>
<span data-ttu-id="912e3-130">루트 인증서가 할당된 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="912e3-130">Specifies the name of the resource group that the root certificate is assigned to.</span></span>
<span data-ttu-id="912e3-131">리소스 그룹은 재고 관리 및 일반 Azure 관리를 간소화하는 데 도움이 되는 항목을 분류합니다.</span><span class="sxs-lookup"><span data-stu-id="912e3-131">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="912e3-132">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="912e3-132">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="912e3-133">인증서가 추가되는 가상 네트워크 게이트웨이의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="912e3-133">Specifies the name of the virtual network gateway where the certificate is added.</span></span>

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

### <span data-ttu-id="912e3-134">-VpnClientRootCertificateName</span><span class="sxs-lookup"><span data-stu-id="912e3-134">-VpnClientRootCertificateName</span></span>
<span data-ttu-id="912e3-135">이 cmdlet이 추가하는 클라이언트 루트 인증서의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="912e3-135">Specifies the name of the client root certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="912e3-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="912e3-136">CommonParameters</span></span>
<span data-ttu-id="912e3-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="912e3-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="912e3-138">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="912e3-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="912e3-139">입력</span><span class="sxs-lookup"><span data-stu-id="912e3-139">INPUTS</span></span>

### <span data-ttu-id="912e3-140">System.String</span><span class="sxs-lookup"><span data-stu-id="912e3-140">System.String</span></span>

## <span data-ttu-id="912e3-141">출력</span><span class="sxs-lookup"><span data-stu-id="912e3-141">OUTPUTS</span></span>

### <span data-ttu-id="912e3-142">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="912e3-142">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate</span></span>

## <span data-ttu-id="912e3-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="912e3-143">NOTES</span></span>

## <span data-ttu-id="912e3-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="912e3-144">RELATED LINKS</span></span>

[<span data-ttu-id="912e3-145">Get-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="912e3-145">Get-AzVpnClientRootCertificate</span></span>](./Get-AzVpnClientRootCertificate.md)

[<span data-ttu-id="912e3-146">New-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="912e3-146">New-AzVpnClientRootCertificate</span></span>](./New-AzVpnClientRootCertificate.md)

[<span data-ttu-id="912e3-147">Remove-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="912e3-147">Remove-AzVpnClientRootCertificate</span></span>](./Remove-AzVpnClientRootCertificate.md)


