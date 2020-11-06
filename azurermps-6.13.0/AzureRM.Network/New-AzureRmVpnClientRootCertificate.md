---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C54AC64C-DA21-443E-8CFE-6CCAC6152C2B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnClientRootCertificate.md
ms.openlocfilehash: 18d634650248ea03c43b8ea24ec15aa3a2b79528
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529499"
---
# <span data-ttu-id="96468-101">New-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="96468-101">New-AzureRmVpnClientRootCertificate</span></span>

## <span data-ttu-id="96468-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="96468-102">SYNOPSIS</span></span>
<span data-ttu-id="96468-103">새 VPN 클라이언트 루트 인증서를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="96468-103">Creates a new VPN client root certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="96468-104">구문과</span><span class="sxs-lookup"><span data-stu-id="96468-104">SYNTAX</span></span>

```
New-AzureRmVpnClientRootCertificate -Name <String> -PublicCertData <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="96468-105">설명은</span><span class="sxs-lookup"><span data-stu-id="96468-105">DESCRIPTION</span></span>
<span data-ttu-id="96468-106">**AzureRmVpnClientRootCertificate** cmdlet은 가상 네트워크 게이트웨이에서 사용할 새 VPN 루트 인증서를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="96468-106">The **New-AzureRmVpnClientRootCertificate** cmdlet creates a new VPN root certificate for use on a virtual network gateway.</span></span>
<span data-ttu-id="96468-107">루트 인증서는 루트 인증 기관을 식별 하는 x.509 인증서입니다. 게이트웨이에서 사용 되는 다른 모든 인증서는 루트 인증서를 신뢰 합니다.</span><span class="sxs-lookup"><span data-stu-id="96468-107">Root certificates are X.509 certificates that identify your Root Certification Authority: all other certificates used on the gateway trust the root certificate.</span></span>
<span data-ttu-id="96468-108">이 cmdlet은 가상 게이트웨이에 할당 되지 않은 독립 실행형 인증서를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="96468-108">This cmdlet creates a stand-alone certificate that is not assigned to a virtual gateway.</span></span>
<span data-ttu-id="96468-109">대신 새 게이트웨이를 만들 때 **AzureRmVpnClientRootCertificate** 에서 만든 인증서가 New-AzureRmVirtualNetworkGateway cmdlet과 함께 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="96468-109">Instead, the certificate created by **New-AzureRmVpnClientRootCertificate** is used in conjunction with the New-AzureRmVirtualNetworkGateway cmdlet when creating a new gateway.</span></span>
<span data-ttu-id="96468-110">예를 들어 새 인증서를 만들고이를 $Certificate 이라는 변수에 저장 한다고 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="96468-110">For example, suppose you create a new certificate and store it in a variable named $Certificate.</span></span>
<span data-ttu-id="96468-111">그런 다음 새 가상 게이트웨이를 만들 때 해당 인증서 개체를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="96468-111">You can then use that certificate object when creating a new virtual gateway.</span></span>
<span data-ttu-id="96468-112">예를 들어 `New-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRootCertificates $Certificate`</span><span class="sxs-lookup"><span data-stu-id="96468-112">For instance, `New-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRootCertificates $Certificate`</span></span>
<span data-ttu-id="96468-113">자세한 내용은 New-AzureRmVirtualNetworkGateway cmdlet에 대 한 설명서를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="96468-113">For more information, see the documentation for the New-AzureRmVirtualNetworkGateway cmdlet.</span></span>

## <span data-ttu-id="96468-114">예제의</span><span class="sxs-lookup"><span data-stu-id="96468-114">EXAMPLES</span></span>

### <span data-ttu-id="96468-115">예제 1: aclient 루트 인증서 만들기</span><span class="sxs-lookup"><span data-stu-id="96468-115">Example 1: Create aclient root certificate</span></span>
```
PS C:\> $Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertficate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> $Certificate = New-AzureRmVpnClientRootCertificate -PublicCertData $CertificateText -Name "ContosoClientRootCertificate"
```

<span data-ttu-id="96468-116">이 예제에서는 클라이언트 루트 인증서를 만들고 $Certificate 이라는 변수에 인증서 개체를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="96468-116">This example creates a client root certificate and store the certificate object in a variable named $Certificate.</span></span>
<span data-ttu-id="96468-117">그런 다음 새 가상 네트워크 게이트웨이에이 변수를 추가 하 여 루트 인증서를 **AzureRmVirtualNetworkGateway** cmdlet에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="96468-117">This variable can then be used by the **New-AzureRmVirtualNetworkGateway** cmdlet to add a root certificate to a new virtual network gateway.</span></span>
<span data-ttu-id="96468-118">첫 번째 명령은 **콘텐츠 가져오기** cmdlet을 사용 하 여 루트 인증서의 이전에 내보낸 텍스트 표현을 가져옵니다. 해당 텍스트 데이터는 $Text 라는 변수에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="96468-118">The first command uses the **Get-Content** cmdlet to get a previously exported text representation of the root certificate; that text data is stored in a variable named $Text.</span></span>
<span data-ttu-id="96468-119">두 번째 명령은 for 루프를 사용 하 여 첫 번째 줄과 마지막 줄을 제외한 모든 텍스트를 추출 하 고, 추출 된 텍스트를 $CertificateText 라는 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="96468-119">The second command then uses a for loop to extract all the text except for the first line and the last line, storing the extracted text in a variable named $CertificateText.</span></span>
<span data-ttu-id="96468-120">세 번째 명령은 **AzureRmVpnClientRootCertificate** cmdlet을 사용 하 여 인증서를 만들고 생성 된 개체를 $Certificate 이라는 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="96468-120">The third command uses the **New-AzureRmVpnClientRootCertificate** cmdlet to create the certificate, storing the created object in a variable named $Certificate.</span></span>

## <span data-ttu-id="96468-121">변수</span><span class="sxs-lookup"><span data-stu-id="96468-121">PARAMETERS</span></span>

### <span data-ttu-id="96468-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96468-122">-DefaultProfile</span></span>
<span data-ttu-id="96468-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="96468-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="96468-124">-이름</span><span class="sxs-lookup"><span data-stu-id="96468-124">-Name</span></span>
<span data-ttu-id="96468-125">새 클라이언트 루트 인증서의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="96468-125">Specifies a name for the new client root certificate.</span></span>

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

### <span data-ttu-id="96468-126">-PublicCertData</span><span class="sxs-lookup"><span data-stu-id="96468-126">-PublicCertData</span></span>
<span data-ttu-id="96468-127">추가할 루트 인증서의 텍스트 표현을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="96468-127">Specifies a text representation of the root certificate to be added.</span></span>
<span data-ttu-id="96468-128">텍스트 표현을 얻으려면 .cer 형식 (Base64 인코딩 사용)으로 인증서를 내보낸 다음 텍스트 편집기에서 결과 파일을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="96468-128">To obtain the text representation, export your certificate in .cer format (using Base64 encoding), then open the resulting file in a text editor.</span></span>
<span data-ttu-id="96468-129">다음과 유사한 출력이 표시 됩니다 (실제 출력에는 여기에 표시 된 간략 한 샘플 보다 많은 줄의 텍스트가 포함 됨).----------MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w-----인증서를 시작 하는-----PublicCertData는 첫 번째 줄 (-----시작 인증서-----)과 마지막 줄 (-----END CERTIFICATE-----) 사이의 모든 줄로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="96468-129">You should see output similar to this (note that the actual output will contain many more lines of text than the abbreviated sample shown here): ----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w ----- END CERTIFICATE ----- The PublicCertData is made up of all the lines between the first line (----- BEGIN CERTIFICATE -----) and the last line (----- END CERTIFICATE -----) in the file.</span></span>
<span data-ttu-id="96468-130">다음과 같은 Windows PowerShell 명령을 사용 하 여 PublicCertData를 검색할 수 있습니다. $Text = Get-Content-경로 "C:\Azure\Certificates\ExportedCertficate.cer" $CertificateText = for ($i = 1; $i + +) {$Text \[ $i \] }</span><span class="sxs-lookup"><span data-stu-id="96468-130">You can retrieve the PublicCertData by using Windows PowerShell commands similar to this: $Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertficate.cer" $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text\[$i\]}</span></span>

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

### <span data-ttu-id="96468-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96468-131">CommonParameters</span></span>
<span data-ttu-id="96468-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="96468-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96468-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96468-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96468-134">입력</span><span class="sxs-lookup"><span data-stu-id="96468-134">INPUTS</span></span>

### <span data-ttu-id="96468-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="96468-135">System.String</span></span>

## <span data-ttu-id="96468-136">출력</span><span class="sxs-lookup"><span data-stu-id="96468-136">OUTPUTS</span></span>

### <span data-ttu-id="96468-137">PSVpnClientRootCertificate에 대 한.</span><span class="sxs-lookup"><span data-stu-id="96468-137">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate</span></span>

## <span data-ttu-id="96468-138">상속자</span><span class="sxs-lookup"><span data-stu-id="96468-138">NOTES</span></span>

## <span data-ttu-id="96468-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="96468-139">RELATED LINKS</span></span>

[<span data-ttu-id="96468-140">추가-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="96468-140">Add-AzureRmVpnClientRootCertificate</span></span>](./Add-AzureRmVpnClientRootCertificate.md)

[<span data-ttu-id="96468-141">Get-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="96468-141">Get-AzureRmVpnClientRootCertificate</span></span>](./Get-AzureRmVpnClientRootCertificate.md)

[<span data-ttu-id="96468-142">제거-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="96468-142">Remove-AzureRmVpnClientRootCertificate</span></span>](./Remove-AzureRmVpnClientRootCertificate.md)


