---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: B9153CA9-06D1-4EF3-9863-D649C2EBAEAA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVpnClientRootCertificate.md
ms.openlocfilehash: 11b4d3cca8d7cad8d3fb4cfcc4e256d1934592d0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526800"
---
# <span data-ttu-id="e1257-101">Add-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="e1257-101">Add-AzureRmVpnClientRootCertificate</span></span>

## <span data-ttu-id="e1257-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1257-102">SYNOPSIS</span></span>
<span data-ttu-id="e1257-103">VPN 클라이언트 루트 인증서를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1257-103">Adds a VPN client root certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e1257-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e1257-104">SYNTAX</span></span>

```
Add-AzureRmVpnClientRootCertificate -VpnClientRootCertificateName <String> -VirtualNetworkGatewayName <String>
 -ResourceGroupName <String> -PublicCertData <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e1257-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e1257-105">DESCRIPTION</span></span>
<span data-ttu-id="e1257-106">**Add-AzureRmVpnClientRootCertificate** cmdlet은 가상 네트워크 게이트웨이에 루트 인증서를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1257-106">The **Add-AzureRmVpnClientRootCertificate** cmdlet adds a root certificate to a virtual network gateway.</span></span>
<span data-ttu-id="e1257-107">루트 인증서는 루트 인증 기관을 식별 하는 x.509 인증서입니다.</span><span class="sxs-lookup"><span data-stu-id="e1257-107">Root certificates are X.509 certificates that identify your Root Certification Authority.</span></span>
<span data-ttu-id="e1257-108">설계상 게이트웨이에서 사용 되는 모든 인증서는 루트 인증서를 신뢰 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1257-108">By design, all certificates used on the gateway trust the root certificate.</span></span>

<span data-ttu-id="e1257-109">이 cmdlet은 기존 인증서를 게이트웨이 루트 인증서로 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1257-109">This cmdlet assigns an existing certificate as a gateway root certificate.</span></span>
<span data-ttu-id="e1257-110">X.509 인증서를 사용할 수 없는 경우 공개 키 인프라를 통해 하나를 생성 하거나 makecert.exe 등의 인증서 생성기를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e1257-110">If you do not have an X.509 certificate available you can generate one through your public key infrastructure or use a certificate generator such as makecert.exe.</span></span>

<span data-ttu-id="e1257-111">루트 인증서를 추가 하려면 인증서 이름을 지정 하 고 인증서의 텍스트 전용 표현을 제공 해야 합니다 (자세한 내용은 *PublicCertData* 매개 변수 참조).</span><span class="sxs-lookup"><span data-stu-id="e1257-111">To add a root certificate, you must specify the certificate name and provide a text-only representation of the certificate (see *the PublicCertData* parameter for more information).</span></span>
<span data-ttu-id="e1257-112">Azure를 사용 하 여 게이트웨이에 두 개 이상의 루트 인증서를 할당할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e1257-112">Azure allows you to assign more than one root certificate to a gateway.</span></span>
<span data-ttu-id="e1257-113">여러 루트 인증서는 두 개 이상의 회사의 사용자를 포함 하는 조직에 의해 배포 되는 경우가 많습니다.</span><span class="sxs-lookup"><span data-stu-id="e1257-113">Multiple root certificates are often deployed by organizations that include users from more than one company.</span></span>

## <span data-ttu-id="e1257-114">예제의</span><span class="sxs-lookup"><span data-stu-id="e1257-114">EXAMPLES</span></span>

### <span data-ttu-id="e1257-115">예제 1: 가상 게이트웨이에 클라이언트 루트 인증서 추가</span><span class="sxs-lookup"><span data-stu-id="e1257-115">Example 1: Add a client root certificate to a virtual gateway</span></span>
```
PS C:\>$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertficate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> Add-AzureRmVpnClientRootCertificate -PublicCertData $CertificateText -ResourceGroupName "ContosoResourceGroup" -VirtualNetworkGatewayName "ContosoVirtualGateway" -VpnClientRootCertificateName "ContosoClientRootCertificate"
```

<span data-ttu-id="e1257-116">이 예제에서는 클라이언트 루트 인증서를 ContosoVirtualGateway 이라는 가상 게이트웨이에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1257-116">This example adds a client root certificate to a virtual gateway named ContosoVirtualGateway.</span></span>

<span data-ttu-id="e1257-117">첫 번째 명령은 **가져오기-내용** cmdlet을 사용 하 여 루트 인증서의 이전 내보낸 텍스트 표현을 가져오고 해당 텍스트 데이터를 $Text 라는 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1257-117">The first command uses the **Get-Content** cmdlet to get a previously-exported text representation of the root certificate and stores that text data the variable named $Text.</span></span>

<span data-ttu-id="e1257-118">두 번째 명령은 for 루프를 사용 하 여 첫 번째 줄과 마지막 줄을 제외한 모든 텍스트를 추출 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1257-118">The second command then uses a for loop to extract all the text except for the first line and the last line.</span></span>
<span data-ttu-id="e1257-119">추출 된 텍스트는 $CertificateText 라는 변수에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e1257-119">The extracted text is stored in a variable named $CertificateText.</span></span>

<span data-ttu-id="e1257-120">세 번째 명령은 **AzureRmVpnClientRootCertificate** cmdlet을 사용 하 여 $CertificateText에 저장 된 텍스트를 사용 하 여 게이트웨이에서 루트 인증서를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1257-120">The third command then uses the text stored in $CertificateText with the **Add-AzureRmVpnClientRootCertificate** cmdlet to add the root certificate to the gateway.</span></span>

## <span data-ttu-id="e1257-121">변수</span><span class="sxs-lookup"><span data-stu-id="e1257-121">PARAMETERS</span></span>

### <span data-ttu-id="e1257-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1257-122">-DefaultProfile</span></span>
<span data-ttu-id="e1257-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e1257-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e1257-124">-PublicCertData</span><span class="sxs-lookup"><span data-stu-id="e1257-124">-PublicCertData</span></span>
<span data-ttu-id="e1257-125">추가할 루트 인증서의 텍스트 표현을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1257-125">Specifies the text representation of the root certificate to be added.</span></span>
<span data-ttu-id="e1257-126">텍스트 표현을 얻으려면 .cer 형식 (Base64 인코딩 사용)으로 인증서를 내보낸 다음 텍스트 편집기에서 결과 파일을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="e1257-126">To obtain the text representation, export your certificate in .cer format (using Base64 encoding), then open the resulting file in a text editor.</span></span>
<span data-ttu-id="e1257-127">이렇게 하면 다음과 유사한 출력이 표시 됩니다 (실제 출력에는 여기에 표시 된 간략 한 샘플 보다 많은 줄의 텍스트가 포함 됨).</span><span class="sxs-lookup"><span data-stu-id="e1257-127">When you do that, you will see output similar to the following (note that the actual output will contain many more lines of text than the abbreviated sample shown here):</span></span>

<span data-ttu-id="e1257-128">인증서-----MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w-----인증서-----시작-----</span><span class="sxs-lookup"><span data-stu-id="e1257-128">----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w ----- END CERTIFICATE -----</span></span>

<span data-ttu-id="e1257-129">PublicCertData는 파일의 첫 번째 줄 (-----시작 인증서-----)과 마지막 줄 (-----종료 인증서-----) 사이의 모든 줄로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e1257-129">The PublicCertData is made up of all the lines between the first line (----- BEGIN CERTIFICATE -----) and the last line (----- END CERTIFICATE -----) in the file.</span></span>
<span data-ttu-id="e1257-130">다음과 유사한 Windows PowerShell 명령을 사용 하 여이 데이터를 검색할 수 있습니다. `$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertficate.cer"`
`$CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text\[$i\]}`</span><span class="sxs-lookup"><span data-stu-id="e1257-130">You can retrieve this data  by using Windows PowerShell commands similar to this: `$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertficate.cer"`
`$CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text\[$i\]}`</span></span>

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

### <span data-ttu-id="e1257-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1257-131">-ResourceGroupName</span></span>
<span data-ttu-id="e1257-132">루트 인증서가 할당 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1257-132">Specifies the name of the resource group that the root certificate is assigned to.</span></span>

<span data-ttu-id="e1257-133">리소스 그룹은 인벤터리 관리 및 일반 Azure 관리를 간소화 하기 위해 항목을 분류 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1257-133">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="e1257-134">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="e1257-134">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="e1257-135">인증서가 추가 되는 가상 네트워크 게이트웨이의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1257-135">Specifies the name of the virtual network gateway where the certificate is added.</span></span>

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

### <span data-ttu-id="e1257-136">-VpnClientRootCertificateName</span><span class="sxs-lookup"><span data-stu-id="e1257-136">-VpnClientRootCertificateName</span></span>
<span data-ttu-id="e1257-137">이 cmdlet에 추가 되는 클라이언트 루트 인증서의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1257-137">Specifies the name of the client root certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="e1257-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1257-138">CommonParameters</span></span>
<span data-ttu-id="e1257-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1257-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1257-140">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1257-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1257-141">입력</span><span class="sxs-lookup"><span data-stu-id="e1257-141">INPUTS</span></span>

### <span data-ttu-id="e1257-142">않아야</span><span class="sxs-lookup"><span data-stu-id="e1257-142">None</span></span>
<span data-ttu-id="e1257-143">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e1257-143">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e1257-144">출력</span><span class="sxs-lookup"><span data-stu-id="e1257-144">OUTPUTS</span></span>

### <span data-ttu-id="e1257-145">PSVpnClientRootCertificate에 대 한.</span><span class="sxs-lookup"><span data-stu-id="e1257-145">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate</span></span>

## <span data-ttu-id="e1257-146">상속자</span><span class="sxs-lookup"><span data-stu-id="e1257-146">NOTES</span></span>

## <span data-ttu-id="e1257-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e1257-147">RELATED LINKS</span></span>

[<span data-ttu-id="e1257-148">Get-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="e1257-148">Get-AzureRmVpnClientRootCertificate</span></span>](./Get-AzureRmVpnClientRootCertificate.md)

[<span data-ttu-id="e1257-149">새로운 AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="e1257-149">New-AzureRmVpnClientRootCertificate</span></span>](./New-AzureRmVpnClientRootCertificate.md)

[<span data-ttu-id="e1257-150">제거-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="e1257-150">Remove-AzureRmVpnClientRootCertificate</span></span>](./Remove-AzureRmVpnClientRootCertificate.md)


