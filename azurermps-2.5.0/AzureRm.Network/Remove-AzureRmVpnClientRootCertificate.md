---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5D857FF6-A27D-4031-948D-8A69D24B4AD4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvpnclientrootcertificate
schema: 2.0.0
ms.openlocfilehash: 66c026e3e1ec05d94b8dc19b2ceedd92d4fc0200
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882569"
---
# <span data-ttu-id="1e4f9-101">Remove-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="1e4f9-101">Remove-AzureRmVpnClientRootCertificate</span></span>

## <span data-ttu-id="1e4f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e4f9-102">SYNOPSIS</span></span>
<span data-ttu-id="1e4f9-103">기존 VPN 클라이언트 루트 인증서를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e4f9-103">Removes an existing VPN client root certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1e4f9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1e4f9-104">SYNTAX</span></span>

```
Remove-AzureRmVpnClientRootCertificate -VpnClientRootCertificateName <String>
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> -PublicCertData <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1e4f9-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1e4f9-105">DESCRIPTION</span></span>
<span data-ttu-id="1e4f9-106">**AzureRmVpnClientRootCertificate** cmdlet은 가상 네트워크 게이트웨이에서 지정 된 루트 인증서를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e4f9-106">The **Remove-AzureRmVpnClientRootCertificate** cmdlet removes the specified root certificate from a virtual network gateway.</span></span>
<span data-ttu-id="1e4f9-107">루트 인증서는 루트 인증 기관을 식별 하는 x.509 인증서입니다. 게이트웨이에서 사용 되는 다른 모든 인증서는 루트 인증서를 신뢰 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e4f9-107">Root certificates are X.509 certificates that identify your Root Certification Authority: all other certificates used on the gateway trust the root certificate.</span></span>
<span data-ttu-id="1e4f9-108">루트 인증서를 제거 하면 인증을 위해 인증서를 사용 하는 컴퓨터가 더 이상 게이트웨이에 연결할 수 없게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1e4f9-108">If you remove a root certificate computers that use the certificate for authentication purposes will no longer be able to connect to the gateway.</span></span>

<span data-ttu-id="1e4f9-109">**AzureRmVpnClientRootCertificate** 을 사용할 때는 인증서 이름과 인증서 데이터의 텍스트 표현을 모두 제공 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e4f9-109">When you use **Remove-AzureRmVpnClientRootCertificate** , you must supply both the certificate name and a text representation of the certificate data.</span></span>
<span data-ttu-id="1e4f9-110">인증서의 텍스트 표현에 대 한 자세한 내용은 *Publiccertdata* 매개 변수 설명을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="1e4f9-110">For more information about the text representation of a certificate see the *PublicCertData* parameter description.</span></span>

## <span data-ttu-id="1e4f9-111">예제의</span><span class="sxs-lookup"><span data-stu-id="1e4f9-111">EXAMPLES</span></span>

### <span data-ttu-id="1e4f9-112">예제 1: 가상 네트워크 게이트웨이에서 클라이언트 루트 인증서 제거</span><span class="sxs-lookup"><span data-stu-id="1e4f9-112">Example 1: Remove a client root certificate from a virtual network gateway</span></span>
```
PS C:\>$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertficate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> Remove-AzureRmVpnClientRootCertificate -PublicCertData $CertificateText -ResourceGroupName "ContosoResourceGroup" -VirtualNetworkGatewayName "ContosoVirtualGateway"-VpnClientRootCertificateName "ContosoRootCertificate"
```

<span data-ttu-id="1e4f9-113">이 예제에서는 가상 네트워크 게이트웨이 ContosoVirtualGateway에서 ContosoRootCertificate 이라는 클라이언트 루트 인증서를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e4f9-113">This example removes a client root certificate named ContosoRootCertificate from the virtual network gateway ContosoVirtualGateway.</span></span>

<span data-ttu-id="1e4f9-114">첫 번째 명령은 **콘텐츠 가져오기** cmdlet을 사용 하 여 이전에 내보낸 인증서의 텍스트 표현을 가져옵니다. 이 텍스트 표현은 $Text 이라는 변수에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1e4f9-114">The first command uses the **Get-Content** cmdlet to get a previously-exported text representation of the certificate; this text representation is stored in a variable named $Text.</span></span>

<span data-ttu-id="1e4f9-115">두 번째 명령은 for 루프를 사용 하 여 첫 번째 줄과 마지막 줄을 제외한 $Text에서 모든 텍스트의 압축을 풉니다.</span><span class="sxs-lookup"><span data-stu-id="1e4f9-115">The second command then uses a for loop to extract all the text in $Text except for the first line and the last line.</span></span>
<span data-ttu-id="1e4f9-116">추출 된이 텍스트는 $CertificateText 라는 변수에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1e4f9-116">This extracted text is stored in a variable named $CertificateText.</span></span>

<span data-ttu-id="1e4f9-117">세 번째 명령은 **AzureRmVpnClientRootCertificate** cmdlet과 함께 $CertificateText 변수에 저장 된 정보를 사용 하 여 게이트웨이에서 인증서를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e4f9-117">The third command uses the information stored in the $CertificateText variable along with the **Remove-AzureRmVpnClientRootCertificate** cmdlet to remove the certificate from the gateway.</span></span>

## <span data-ttu-id="1e4f9-118">변수</span><span class="sxs-lookup"><span data-stu-id="1e4f9-118">PARAMETERS</span></span>

### <span data-ttu-id="1e4f9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e4f9-119">-DefaultProfile</span></span>
<span data-ttu-id="1e4f9-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1e4f9-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1e4f9-121">-PublicCertData</span><span class="sxs-lookup"><span data-stu-id="1e4f9-121">-PublicCertData</span></span>
<span data-ttu-id="1e4f9-122">제거할 루트 인증서의 텍스트 표현을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e4f9-122">Specifies the text representation of the root certificate to be removed.</span></span>
<span data-ttu-id="1e4f9-123">텍스트 표현을 얻으려면 .cer 형식 (Base64 사용)에서 인증서를 내보낸 다음 텍스트 편집기에서 결과 파일을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="1e4f9-123">To obtain the text representation, export your certificate in .cer format (using Base64) encoding, then open the resulting file in a text editor.</span></span>
<span data-ttu-id="1e4f9-124">다음과 유사한 출력이 표시 되어야 합니다 (실제 출력에는 여기에 표시 된 간략 한 샘플 보다 많은 줄의 텍스트가 포함 됨).</span><span class="sxs-lookup"><span data-stu-id="1e4f9-124">You should see output similar to the following (note that the actual output will contain many more lines of text than the abbreviated sample shown here):</span></span>

<span data-ttu-id="1e4f9-125">인증서-----MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w-----인증서-----시작-----</span><span class="sxs-lookup"><span data-stu-id="1e4f9-125">----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w ----- END CERTIFICATE -----</span></span>

<span data-ttu-id="1e4f9-126">PublicCertData는 파일의 첫 번째 줄 (-----시작 인증서-----)과 마지막 줄 (-----종료 인증서-----) 사이의 모든 줄로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1e4f9-126">The PublicCertData is made up of all the lines between the first line (----- BEGIN CERTIFICATE -----) and the last line (----- END CERTIFICATE -----) in the file.</span></span>
<span data-ttu-id="1e4f9-127">다음과 유사한 Windows PowerShell 명령을 사용 하 여 PublicCertData를 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1e4f9-127">You can retrieve the PublicCertData using Windows PowerShell commands similar to this:</span></span>

<span data-ttu-id="1e4f9-128">$Text = Get-Content-경로 "C:\Azure\Certificates\ExportedCertficate.cer" $CertificateText = ($i = 1, $i-lt $Text. Length-1, $i + +) {$Text \[ $i \] }</span><span class="sxs-lookup"><span data-stu-id="1e4f9-128">$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertficate.cer" $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text\[$i\]}</span></span>

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

### <span data-ttu-id="1e4f9-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e4f9-129">-ResourceGroupName</span></span>
<span data-ttu-id="1e4f9-130">가상 네트워크 게이트웨이가 할당 되는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e4f9-130">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>

<span data-ttu-id="1e4f9-131">리소스 그룹은 인벤터리 관리 및 일반 Azure 관리를 간소화 하기 위해 항목을 분류 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e4f9-131">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="1e4f9-132">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="1e4f9-132">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="1e4f9-133">인증서를 제거 하는 가상 네트워크 게이트웨이의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e4f9-133">Specifies the name of the virtual network gateway that the certificate is removed from.</span></span>

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

### <span data-ttu-id="1e4f9-134">-VpnClientRootCertificateName</span><span class="sxs-lookup"><span data-stu-id="1e4f9-134">-VpnClientRootCertificateName</span></span>
<span data-ttu-id="1e4f9-135">이 cmdlet이 제거 하는 클라이언트 루트 인증서의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e4f9-135">Specifies the name of the client root certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="1e4f9-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e4f9-136">CommonParameters</span></span>
<span data-ttu-id="1e4f9-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e4f9-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e4f9-138">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e4f9-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e4f9-139">입력</span><span class="sxs-lookup"><span data-stu-id="1e4f9-139">INPUTS</span></span>

## <span data-ttu-id="1e4f9-140">출력</span><span class="sxs-lookup"><span data-stu-id="1e4f9-140">OUTPUTS</span></span>

## <span data-ttu-id="1e4f9-141">상속자</span><span class="sxs-lookup"><span data-stu-id="1e4f9-141">NOTES</span></span>

## <span data-ttu-id="1e4f9-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1e4f9-142">RELATED LINKS</span></span>

[<span data-ttu-id="1e4f9-143">추가-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="1e4f9-143">Add-AzureRmVpnClientRootCertificate</span></span>](./Add-AzureRmVpnClientRootCertificate.md)

[<span data-ttu-id="1e4f9-144">Get-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="1e4f9-144">Get-AzureRmVpnClientRootCertificate</span></span>](./Get-AzureRmVpnClientRootCertificate.md)

[<span data-ttu-id="1e4f9-145">새로운 AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="1e4f9-145">New-AzureRmVpnClientRootCertificate</span></span>](./New-AzureRmVpnClientRootCertificate.md)


