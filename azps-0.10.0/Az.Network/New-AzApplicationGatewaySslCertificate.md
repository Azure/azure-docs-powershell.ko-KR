---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6FFE1B64-C80B-423D-A043-55C90A224752
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: 60d46a3d61f0799618107e9bc0727a3ff31fc337
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875454"
---
# <span data-ttu-id="5240a-101">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="5240a-101">New-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="5240a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5240a-102">SYNOPSIS</span></span>
<span data-ttu-id="5240a-103">Azure application gateway에 대 한 SSL 인증서를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5240a-103">Creates an SSL certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="5240a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5240a-104">SYNTAX</span></span>

```
New-AzApplicationGatewaySslCertificate -Name <String> -CertificateFile <String> -Password <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5240a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5240a-105">DESCRIPTION</span></span>
<span data-ttu-id="5240a-106">**AzApplicationGatewaySslCertificate** Cmdlet은 Azure application gateway에 대 한 SSL 인증서를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5240a-106">The **New-AzApplicationGatewaySslCertificate** cmdlet creates an SSL certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="5240a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="5240a-107">EXAMPLES</span></span>

### <span data-ttu-id="5240a-108">예제 1: Azure application gateway에 대 한 SSL 인증서를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5240a-108">Example 1: Create an SSL certificate for an Azure application gateway.</span></span>
```
PS C:\> $password = ConvertTo-SecureString "P@ssw0rd" -AsPlainText -Force
PS C:\> $cert = New-AzApplicationGatewaySslCertificate -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="5240a-109">이 명령은 기본 응용 프로그램 게이트웨이에 대 한 Cert01 이라는 SSL 인증서를 만들고 결과를 명명 된 변수 $Cert에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="5240a-109">This command creates a SSL certificate named Cert01 for the default application gateway and stores the result in the variable named $Cert.</span></span>

## <span data-ttu-id="5240a-110">변수</span><span class="sxs-lookup"><span data-stu-id="5240a-110">PARAMETERS</span></span>

### <span data-ttu-id="5240a-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="5240a-111">-CertificateFile</span></span>
<span data-ttu-id="5240a-112">이 cmdlet이 만드는 SSL 인증서의 .pfx 파일 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5240a-112">Specifies the path of the .pfx file of the SSL certificate that this cmdlet creates.</span></span>

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

### <span data-ttu-id="5240a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5240a-113">-DefaultProfile</span></span>
<span data-ttu-id="5240a-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5240a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5240a-115">-이름</span><span class="sxs-lookup"><span data-stu-id="5240a-115">-Name</span></span>
<span data-ttu-id="5240a-116">이 cmdlet이 만드는 SSL 인증서의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5240a-116">Specifies the name of the SSL certificate that this cmdlet creates.</span></span>

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

### <span data-ttu-id="5240a-117">-암호</span><span class="sxs-lookup"><span data-stu-id="5240a-117">-Password</span></span>
<span data-ttu-id="5240a-118">이 cmdlet이 만드는 SSL의 암호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5240a-118">Specifies the password of the SSL that this cmdlet creates.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5240a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5240a-119">CommonParameters</span></span>
<span data-ttu-id="5240a-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5240a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5240a-121">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5240a-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5240a-122">입력</span><span class="sxs-lookup"><span data-stu-id="5240a-122">INPUTS</span></span>

### <span data-ttu-id="5240a-123">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="5240a-123">System.String</span></span>

## <span data-ttu-id="5240a-124">출력</span><span class="sxs-lookup"><span data-stu-id="5240a-124">OUTPUTS</span></span>

### <span data-ttu-id="5240a-125">PSApplicationGatewaySslCertificate에 대 한.</span><span class="sxs-lookup"><span data-stu-id="5240a-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="5240a-126">상속자</span><span class="sxs-lookup"><span data-stu-id="5240a-126">NOTES</span></span>

## <span data-ttu-id="5240a-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5240a-127">RELATED LINKS</span></span>

[<span data-ttu-id="5240a-128">추가-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="5240a-128">Add-AzApplicationGatewaySslCertificate</span></span>](./Add-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="5240a-129">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="5240a-129">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="5240a-130">제거-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="5240a-130">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="5240a-131">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="5240a-131">Set-AzApplicationGatewaySslCertificate</span></span>](./Set-AzApplicationGatewaySslCertificate.md)


