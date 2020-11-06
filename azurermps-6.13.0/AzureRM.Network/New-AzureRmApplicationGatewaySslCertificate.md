---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6FFE1B64-C80B-423D-A043-55C90A224752
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewaySslCertificate.md
ms.openlocfilehash: 37ad789afeaf8776eeab1c8977dfab8b4cd2681a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532427"
---
# <span data-ttu-id="39b0f-101">New-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="39b0f-101">New-AzureRmApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="39b0f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39b0f-102">SYNOPSIS</span></span>
<span data-ttu-id="39b0f-103">Azure application gateway에 대 한 SSL 인증서를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="39b0f-103">Creates an SSL certificate for an Azure application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="39b0f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="39b0f-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewaySslCertificate -Name <String> -CertificateFile <String> -Password <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="39b0f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="39b0f-105">DESCRIPTION</span></span>
<span data-ttu-id="39b0f-106">**AzureRmApplicationGatewaySslCertificate** Cmdlet은 Azure application gateway에 대 한 SSL 인증서를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="39b0f-106">The **New-AzureRmApplicationGatewaySslCertificate** cmdlet creates an SSL certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="39b0f-107">예제의</span><span class="sxs-lookup"><span data-stu-id="39b0f-107">EXAMPLES</span></span>

### <span data-ttu-id="39b0f-108">예제 1: Azure application gateway에 대 한 SSL 인증서를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="39b0f-108">Example 1: Create an SSL certificate for an Azure application gateway.</span></span>
```
PS C:\> $password = ConvertTo-SecureString "P@ssw0rd" -AsPlainText -Force
PS C:\> $cert = New-AzureRmApplicationGatewaySslCertificate -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="39b0f-109">이 명령은 기본 응용 프로그램 게이트웨이에 대 한 Cert01 이라는 SSL 인증서를 만들고 결과를 명명 된 변수 $Cert에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="39b0f-109">This command creates a SSL certificate named Cert01 for the default application gateway and stores the result in the variable named $Cert.</span></span>

## <span data-ttu-id="39b0f-110">변수</span><span class="sxs-lookup"><span data-stu-id="39b0f-110">PARAMETERS</span></span>

### <span data-ttu-id="39b0f-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="39b0f-111">-CertificateFile</span></span>
<span data-ttu-id="39b0f-112">이 cmdlet이 만드는 SSL 인증서의 .pfx 파일 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39b0f-112">Specifies the path of the .pfx file of the SSL certificate that this cmdlet creates.</span></span>

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

### <span data-ttu-id="39b0f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39b0f-113">-DefaultProfile</span></span>
<span data-ttu-id="39b0f-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="39b0f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="39b0f-115">-이름</span><span class="sxs-lookup"><span data-stu-id="39b0f-115">-Name</span></span>
<span data-ttu-id="39b0f-116">이 cmdlet이 만드는 SSL 인증서의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39b0f-116">Specifies the name of the SSL certificate that this cmdlet creates.</span></span>

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

### <span data-ttu-id="39b0f-117">-암호</span><span class="sxs-lookup"><span data-stu-id="39b0f-117">-Password</span></span>
<span data-ttu-id="39b0f-118">이 cmdlet이 만드는 SSL의 암호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39b0f-118">Specifies the password of the SSL that this cmdlet creates.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39b0f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39b0f-119">CommonParameters</span></span>
<span data-ttu-id="39b0f-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="39b0f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39b0f-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39b0f-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39b0f-122">입력</span><span class="sxs-lookup"><span data-stu-id="39b0f-122">INPUTS</span></span>

### <span data-ttu-id="39b0f-123">않아야</span><span class="sxs-lookup"><span data-stu-id="39b0f-123">None</span></span>

## <span data-ttu-id="39b0f-124">출력</span><span class="sxs-lookup"><span data-stu-id="39b0f-124">OUTPUTS</span></span>

### <span data-ttu-id="39b0f-125">PSApplicationGatewaySslCertificate에 대 한.</span><span class="sxs-lookup"><span data-stu-id="39b0f-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="39b0f-126">상속자</span><span class="sxs-lookup"><span data-stu-id="39b0f-126">NOTES</span></span>

## <span data-ttu-id="39b0f-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="39b0f-127">RELATED LINKS</span></span>

[<span data-ttu-id="39b0f-128">추가-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="39b0f-128">Add-AzureRmApplicationGatewaySslCertificate</span></span>](./Add-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="39b0f-129">Get-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="39b0f-129">Get-AzureRmApplicationGatewaySslCertificate</span></span>](./Get-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="39b0f-130">제거-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="39b0f-130">Remove-AzureRmApplicationGatewaySslCertificate</span></span>](./Remove-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="39b0f-131">Set-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="39b0f-131">Set-AzureRmApplicationGatewaySslCertificate</span></span>](./Set-AzureRmApplicationGatewaySslCertificate.md)


