---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementsystemcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementSystemCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementSystemCertificate.md
ms.openlocfilehash: fa64e9bade3a6cd8ec4edc8e04956c97306328ea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524731"
---
# <span data-ttu-id="eebc7-101">New-AzureRmApiManagementSystemCertificate</span><span class="sxs-lookup"><span data-stu-id="eebc7-101">New-AzureRmApiManagementSystemCertificate</span></span>

## <span data-ttu-id="eebc7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eebc7-102">SYNOPSIS</span></span>
<span data-ttu-id="eebc7-103">의 인스턴스를 만듭니다 `PsApiManagementSystemCertificate` .</span><span class="sxs-lookup"><span data-stu-id="eebc7-103">Creates an instance of `PsApiManagementSystemCertificate`.</span></span> <span data-ttu-id="eebc7-104">인증서는 개인 CA에 의해 발급 될 수 있으며 API Management 서비스에 설치 `CertificateAuthority` 되거나 `Root` 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="eebc7-104">The certificate can be issued by private CA's and will be installed on the API Management service into `CertificateAuthority` or `Root` store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eebc7-105">구문과</span><span class="sxs-lookup"><span data-stu-id="eebc7-105">SYNTAX</span></span>

```
New-AzureRmApiManagementSystemCertificate -StoreName <String> -PfxPath <String> [-PfxPassword <SecureString>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eebc7-106">설명은</span><span class="sxs-lookup"><span data-stu-id="eebc7-106">DESCRIPTION</span></span>
<span data-ttu-id="eebc7-107">**AzureRmApiManagementSystemCertificate** Cmdlet은 **PsApiManagementSystemCertificate** 의 인스턴스를 만드는 도우미 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="eebc7-107">The **New-AzureRmApiManagementSystemCertificate** cmdlet is a helper command that creates an instance of **PsApiManagementSystemCertificate**.</span></span>
<span data-ttu-id="eebc7-108">이 명령은 New-AzureRmApiManagement 및 Set-AzureRmApiManagement cmdlet에 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="eebc7-108">This command is used with the New-AzureRmApiManagement and Set-AzureRmApiManagement cmdlet.</span></span>

## <span data-ttu-id="eebc7-109">예제의</span><span class="sxs-lookup"><span data-stu-id="eebc7-109">EXAMPLES</span></span>

### <span data-ttu-id="eebc7-110">예제 1: 파일의 Ssl 인증서를 사용 하 여 PsApiManagementSystemCertificate의 인스턴스 만들기 및 초기화</span><span class="sxs-lookup"><span data-stu-id="eebc7-110">Example 1: Create and initialize an instance of PsApiManagementSystemCertificate using an Ssl Certificate from file</span></span>
```powershell
PS C:\>$rootCa = New-AzureRmApiManagementSystemCertificate -StoreName "Root" -PfxPath "C:\contoso\certificates\privateCa.cer"
PS C:\>$systemCert = @($rootCa)
PS C:\>New-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -SystemCertificateConfiguration $systemCert
```

<span data-ttu-id="eebc7-111">이 명령은 루트 CA 인증서를 사용 하 여 **PsApiManagementSystemCertificate** 인스턴스를 만들고 초기화 합니다.</span><span class="sxs-lookup"><span data-stu-id="eebc7-111">This command creates and initializes an instance of **PsApiManagementSystemCertificate** with a root CA certificate.</span></span> <span data-ttu-id="eebc7-112">그런 다음 루트 저장소에 CA 인증서를 설치 하는 API Management 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="eebc7-112">It then creates and API Management service which installs the CA cert to the Root store.</span></span>

## <span data-ttu-id="eebc7-113">변수</span><span class="sxs-lookup"><span data-stu-id="eebc7-113">PARAMETERS</span></span>

### <span data-ttu-id="eebc7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eebc7-114">-DefaultProfile</span></span>
<span data-ttu-id="eebc7-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="eebc7-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eebc7-116">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="eebc7-116">-PfxPassword</span></span>
<span data-ttu-id="eebc7-117">.Pfx 인증서 파일의 암호입니다.</span><span class="sxs-lookup"><span data-stu-id="eebc7-117">Password for the .pfx certificate file.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eebc7-118">-PfxPath</span><span class="sxs-lookup"><span data-stu-id="eebc7-118">-PfxPath</span></span>
<span data-ttu-id="eebc7-119">.Pfx 인증서 파일의 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="eebc7-119">Path to a .pfx certificate file.</span></span>

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

### <span data-ttu-id="eebc7-120">-StoreName</span><span class="sxs-lookup"><span data-stu-id="eebc7-120">-StoreName</span></span>
<span data-ttu-id="eebc7-121">인증서 StoreName</span><span class="sxs-lookup"><span data-stu-id="eebc7-121">Certificate StoreName</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: CertificateAuthority, Root

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eebc7-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eebc7-122">CommonParameters</span></span>
<span data-ttu-id="eebc7-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="eebc7-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eebc7-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eebc7-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eebc7-125">입력</span><span class="sxs-lookup"><span data-stu-id="eebc7-125">INPUTS</span></span>

### <span data-ttu-id="eebc7-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="eebc7-126">System.String</span></span>

### <span data-ttu-id="eebc7-127">System.webserver</span><span class="sxs-lookup"><span data-stu-id="eebc7-127">System.Security.SecureString</span></span>

## <span data-ttu-id="eebc7-128">출력</span><span class="sxs-lookup"><span data-stu-id="eebc7-128">OUTPUTS</span></span>

### <span data-ttu-id="eebc7-129">ApiManagement. PsApiManagementSystemCertificate/.</span><span class="sxs-lookup"><span data-stu-id="eebc7-129">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSystemCertificate</span></span>

## <span data-ttu-id="eebc7-130">상속자</span><span class="sxs-lookup"><span data-stu-id="eebc7-130">NOTES</span></span>

## <span data-ttu-id="eebc7-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="eebc7-131">RELATED LINKS</span></span>

[<span data-ttu-id="eebc7-132">새로운 AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="eebc7-132">New-AzureRmApiManagement</span></span>](./New-AzureRmApiManagement.md)

[<span data-ttu-id="eebc7-133">Set-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="eebc7-133">Set-AzureRmApiManagement</span></span>](./Set-AzureRmApiManagement.md)
