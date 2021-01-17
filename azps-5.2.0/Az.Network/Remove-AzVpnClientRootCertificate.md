---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5D857FF6-A27D-4031-948D-8A69D24B4AD4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientRootCertificate.md
ms.openlocfilehash: 5cb4a57994ad8b15048bfc22dadefbbee031aaf7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98330578"
---
# <span data-ttu-id="cd85e-101">Remove-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="cd85e-101">Remove-AzVpnClientRootCertificate</span></span>

## <span data-ttu-id="cd85e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd85e-102">SYNOPSIS</span></span>
<span data-ttu-id="cd85e-103">기존 VPN 클라이언트 루트 인증서를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="cd85e-103">Removes an existing VPN client root certificate.</span></span>

## <span data-ttu-id="cd85e-104">구문</span><span class="sxs-lookup"><span data-stu-id="cd85e-104">SYNTAX</span></span>

```
Remove-AzVpnClientRootCertificate -VpnClientRootCertificateName <String> -VirtualNetworkGatewayName <String>
 -ResourceGroupName <String> -PublicCertData <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cd85e-105">설명</span><span class="sxs-lookup"><span data-stu-id="cd85e-105">DESCRIPTION</span></span>
<span data-ttu-id="cd85e-106">**Remove-AzVpnClientRootCertificate** cmdlet은 가상 네트워크 게이트웨이에서 지정된 루트 인증서를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="cd85e-106">The **Remove-AzVpnClientRootCertificate** cmdlet removes the specified root certificate from a virtual network gateway.</span></span>
<span data-ttu-id="cd85e-107">루트 인증서는 루트 인증 기관을 식별하는 X.509 인증서입니다. 게이트웨이에서 사용되는 다른 모든 인증서는 루트 인증서를 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="cd85e-107">Root certificates are X.509 certificates that identify your Root Certification Authority: all other certificates used on the gateway trust the root certificate.</span></span>
<span data-ttu-id="cd85e-108">인증 목적으로 인증서를 사용하는 루트 인증서 컴퓨터를 제거하면 게이트웨이에 더 이상 연결할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="cd85e-108">If you remove a root certificate computers that use the certificate for authentication purposes will no longer be able to connect to the gateway.</span></span>
<span data-ttu-id="cd85e-109">**Remove-AzVpnClientRootCertificate를** 사용하는 경우 인증서 이름과 인증서 데이터의 텍스트 표현을 모두 제공해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd85e-109">When you use **Remove-AzVpnClientRootCertificate**, you must supply both the certificate name and a text representation of the certificate data.</span></span>
<span data-ttu-id="cd85e-110">인증서의 텍스트 표현에 대한 자세한 내용은 *PublicCertData 매개* 변수 설명을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="cd85e-110">For more information about the text representation of a certificate see the *PublicCertData* parameter description.</span></span>

## <span data-ttu-id="cd85e-111">예제</span><span class="sxs-lookup"><span data-stu-id="cd85e-111">EXAMPLES</span></span>

### <span data-ttu-id="cd85e-112">예제 1: 가상 네트워크 게이트웨이에서 클라이언트 루트 인증서 제거</span><span class="sxs-lookup"><span data-stu-id="cd85e-112">Example 1: Remove a client root certificate from a virtual network gateway</span></span>
```powershell
PS C:\>$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> Remove-AzVpnClientRootCertificate -PublicCertData $CertificateText -ResourceGroupName "ContosoResourceGroup" -VirtualNetworkGatewayName "ContosoVirtualGateway" -VpnClientRootCertificateName "ContosoRootCertificate"
```

<span data-ttu-id="cd85e-113">이 예제에서는 ContosoVirtualGateway 가상 네트워크 게이트웨이에서 ContosoRootCertificate라는 클라이언트 루트 인증서를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="cd85e-113">This example removes a client root certificate named ContosoRootCertificate from the virtual network gateway ContosoVirtualGateway.</span></span>
<span data-ttu-id="cd85e-114">첫 번째 명령은 **Get-Content** cmdlet을 사용하여 이전에 내보낼 인증서의 텍스트 표현을 얻게 됩니다. 이 텍스트 표현은 $Text.</span><span class="sxs-lookup"><span data-stu-id="cd85e-114">The first command uses the **Get-Content** cmdlet to get a previously-exported text representation of the certificate; this text representation is stored in a variable named $Text.</span></span>
<span data-ttu-id="cd85e-115">그런 다음, 두 번째 명령은 for 루프를 사용하여 첫 번째 줄과 마지막 줄을 $Text 텍스트의 모든 텍스트를 추출합니다.</span><span class="sxs-lookup"><span data-stu-id="cd85e-115">The second command then uses a for loop to extract all the text in $Text except for the first line and the last line.</span></span>
<span data-ttu-id="cd85e-116">이 추출된 텍스트는 해당 텍스트의 이름에 따라 $CertificateText.</span><span class="sxs-lookup"><span data-stu-id="cd85e-116">This extracted text is stored in a variable named $CertificateText.</span></span>
<span data-ttu-id="cd85e-117">세 번째 명령은 **Remove-AzVpnClientRootCertificate** cmdlet과 함께 $CertificateText 변수에 저장된 정보를 사용하여 게이트웨이에서 인증서를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="cd85e-117">The third command uses the information stored in the $CertificateText variable along with the **Remove-AzVpnClientRootCertificate** cmdlet to remove the certificate from the gateway.</span></span>

## <span data-ttu-id="cd85e-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cd85e-118">PARAMETERS</span></span>

### <span data-ttu-id="cd85e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd85e-119">-DefaultProfile</span></span>
<span data-ttu-id="cd85e-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cd85e-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cd85e-121">-PublicCertData</span><span class="sxs-lookup"><span data-stu-id="cd85e-121">-PublicCertData</span></span>
<span data-ttu-id="cd85e-122">제거할 루트 인증서의 텍스트 표현을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cd85e-122">Specifies the text representation of the root certificate to be removed.</span></span>
<span data-ttu-id="cd85e-123">텍스트 표현을 얻습니다. 인증서를 .cer 형식(Base64 사용) 인코딩으로 내보내고 결과 파일을 텍스트 편집기에서 여는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="cd85e-123">To obtain the text representation, export your certificate in .cer format (using Base64) encoding, then open the resulting file in a text editor.</span></span>
<span data-ttu-id="cd85e-124">다음과 유사한 출력이 표시됩니다(실제 출력에는 여기에 표시된 약어 샘플보다 많은 텍스트 줄이 포함되어 있습니다. ----- BEGIN ----- CERTIFICATE ----- MIIC13FAAXC3671Auij9HhgUNEW8343NMJklo 09982CVVFAw8w ----- END CERTIFICATE ----- PublicCertData는 파일의 첫 번째 줄(----- BEGIN CERTIFICATE -----)과 마지막 줄(----- END CERTIFICATE -----) 사이의 모든 줄로 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cd85e-124">You should see output similar to the following (note that the actual output will contain many more lines of text than the abbreviated sample shown here): ----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w ----- END CERTIFICATE ----- The PublicCertData is made up of all the lines between the first line (----- BEGIN CERTIFICATE -----) and the last line (----- END CERTIFICATE -----) in the file.</span></span>
<span data-ttu-id="cd85e-125">$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer" $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text \[ $i } 명령을 사용하여 PublicCertD Windows PowerShell ata를 검색할 수 있습니다. \]</span><span class="sxs-lookup"><span data-stu-id="cd85e-125">You can retrieve the PublicCertData using Windows PowerShell commands similar to this: $Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer" $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text\[$i\]}</span></span>

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

### <span data-ttu-id="cd85e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd85e-126">-ResourceGroupName</span></span>
<span data-ttu-id="cd85e-127">가상 네트워크 게이트웨이가 할당된 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cd85e-127">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>
<span data-ttu-id="cd85e-128">리소스 그룹은 재고 관리 및 일반 Azure 관리를 간소화하는 데 도움이 되는 항목을 분류합니다.</span><span class="sxs-lookup"><span data-stu-id="cd85e-128">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="cd85e-129">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="cd85e-129">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="cd85e-130">인증서가 제거되는 가상 네트워크 게이트웨이의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cd85e-130">Specifies the name of the virtual network gateway that the certificate is removed from.</span></span>

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

### <span data-ttu-id="cd85e-131">-VpnClientRootCertificateName</span><span class="sxs-lookup"><span data-stu-id="cd85e-131">-VpnClientRootCertificateName</span></span>
<span data-ttu-id="cd85e-132">이 cmdlet이 제거하는 클라이언트 루트 인증서의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cd85e-132">Specifies the name of the client root certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="cd85e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd85e-133">CommonParameters</span></span>
<span data-ttu-id="cd85e-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="cd85e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd85e-135">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="cd85e-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd85e-136">입력</span><span class="sxs-lookup"><span data-stu-id="cd85e-136">INPUTS</span></span>

### <span data-ttu-id="cd85e-137">System.String</span><span class="sxs-lookup"><span data-stu-id="cd85e-137">System.String</span></span>

## <span data-ttu-id="cd85e-138">출력</span><span class="sxs-lookup"><span data-stu-id="cd85e-138">OUTPUTS</span></span>

### <span data-ttu-id="cd85e-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="cd85e-139">System.Boolean</span></span>

## <span data-ttu-id="cd85e-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="cd85e-140">NOTES</span></span>

## <span data-ttu-id="cd85e-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cd85e-141">RELATED LINKS</span></span>

[<span data-ttu-id="cd85e-142">Add-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="cd85e-142">Add-AzVpnClientRootCertificate</span></span>](./Add-AzVpnClientRootCertificate.md)

[<span data-ttu-id="cd85e-143">Get-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="cd85e-143">Get-AzVpnClientRootCertificate</span></span>](./Get-AzVpnClientRootCertificate.md)

[<span data-ttu-id="cd85e-144">New-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="cd85e-144">New-AzVpnClientRootCertificate</span></span>](./New-AzVpnClientRootCertificate.md)


