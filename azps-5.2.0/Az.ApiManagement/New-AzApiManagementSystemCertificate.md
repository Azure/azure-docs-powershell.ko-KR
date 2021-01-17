---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementsystemcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSystemCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSystemCertificate.md
ms.openlocfilehash: 657a1b729bfa5de8b62c58ed590b5cbf2cf7dca8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98350294"
---
# <span data-ttu-id="31cf8-101">New-AzApiManagementSystemCertificate</span><span class="sxs-lookup"><span data-stu-id="31cf8-101">New-AzApiManagementSystemCertificate</span></span>

## <span data-ttu-id="31cf8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31cf8-102">SYNOPSIS</span></span>
<span data-ttu-id="31cf8-103">.의 `PsApiManagementSystemCertificate` 인스턴스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="31cf8-103">Creates an instance of `PsApiManagementSystemCertificate`.</span></span> <span data-ttu-id="31cf8-104">인증서는 개인 CA에서 발급할 수 있으며 API Management 서비스에 설치하거나 `CertificateAuthority` `Root` 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="31cf8-104">The certificate can be issued by private CA's and will be installed on the API Management service into `CertificateAuthority` or `Root` store.</span></span>

## <span data-ttu-id="31cf8-105">구문</span><span class="sxs-lookup"><span data-stu-id="31cf8-105">SYNTAX</span></span>

```
New-AzApiManagementSystemCertificate -StoreName <String> -PfxPath <String> [-PfxPassword <SecureString>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31cf8-106">설명</span><span class="sxs-lookup"><span data-stu-id="31cf8-106">DESCRIPTION</span></span>
<span data-ttu-id="31cf8-107">**New-AzApiManagementSystemCertificate** cmdlet은 **PsApiManagementSystemCertificate의** 인스턴스를 만드는 도우미 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="31cf8-107">The **New-AzApiManagementSystemCertificate** cmdlet is a helper command that creates an instance of **PsApiManagementSystemCertificate**.</span></span>
<span data-ttu-id="31cf8-108">이 명령은 New-AzApiManagement cmdlet과 Set-AzApiManagement 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="31cf8-108">This command is used with the New-AzApiManagement and Set-AzApiManagement cmdlet.</span></span>

## <span data-ttu-id="31cf8-109">예제</span><span class="sxs-lookup"><span data-stu-id="31cf8-109">EXAMPLES</span></span>

### <span data-ttu-id="31cf8-110">예제 1: 파일에서 Ssl 인증서를 사용하여 PsApiManagementSystemCertificate 인스턴스 만들기 및 초기화</span><span class="sxs-lookup"><span data-stu-id="31cf8-110">Example 1: Create and initialize an instance of PsApiManagementSystemCertificate using an Ssl Certificate from file</span></span>
```powershell
PS C:\>$rootCa = New-AzApiManagementSystemCertificate -StoreName "Root" -PfxPath "C:\contoso\certificates\privateCa.cer"
PS C:\>$systemCert = @($rootCa)
PS C:\>New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -SystemCertificateConfiguration $systemCert
```

<span data-ttu-id="31cf8-111">이 명령은 루트 CA 인증서를 사용하여 **PsApiManagementSystemCertificate의** 인스턴스를 만들고 초기화합니다.</span><span class="sxs-lookup"><span data-stu-id="31cf8-111">This command creates and initializes an instance of **PsApiManagementSystemCertificate** with a root CA certificate.</span></span> <span data-ttu-id="31cf8-112">그런 다음 루트 저장소에 CA 인증을 설치하는 API Management 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="31cf8-112">It then creates and API Management service which installs the CA cert to the Root store.</span></span>

## <span data-ttu-id="31cf8-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="31cf8-113">PARAMETERS</span></span>

### <span data-ttu-id="31cf8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31cf8-114">-DefaultProfile</span></span>
<span data-ttu-id="31cf8-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="31cf8-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31cf8-116">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="31cf8-116">-PfxPassword</span></span>
<span data-ttu-id="31cf8-117">.pfx 인증서 파일의 암호입니다.</span><span class="sxs-lookup"><span data-stu-id="31cf8-117">Password for the .pfx certificate file.</span></span>

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

### <span data-ttu-id="31cf8-118">-PfxPath</span><span class="sxs-lookup"><span data-stu-id="31cf8-118">-PfxPath</span></span>
<span data-ttu-id="31cf8-119">.pfx 인증서 파일의 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="31cf8-119">Path to a .pfx certificate file.</span></span>

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

### <span data-ttu-id="31cf8-120">-StoreName</span><span class="sxs-lookup"><span data-stu-id="31cf8-120">-StoreName</span></span>
<span data-ttu-id="31cf8-121">Certificate StoreName</span><span class="sxs-lookup"><span data-stu-id="31cf8-121">Certificate StoreName</span></span>

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

### <span data-ttu-id="31cf8-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31cf8-122">CommonParameters</span></span>
<span data-ttu-id="31cf8-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="31cf8-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31cf8-124">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="31cf8-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31cf8-125">입력</span><span class="sxs-lookup"><span data-stu-id="31cf8-125">INPUTS</span></span>

### <span data-ttu-id="31cf8-126">System.String</span><span class="sxs-lookup"><span data-stu-id="31cf8-126">System.String</span></span>

### <span data-ttu-id="31cf8-127">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="31cf8-127">System.Security.SecureString</span></span>

## <span data-ttu-id="31cf8-128">출력</span><span class="sxs-lookup"><span data-stu-id="31cf8-128">OUTPUTS</span></span>

### <span data-ttu-id="31cf8-129">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSystemCertificate</span><span class="sxs-lookup"><span data-stu-id="31cf8-129">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSystemCertificate</span></span>

## <span data-ttu-id="31cf8-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="31cf8-130">NOTES</span></span>

## <span data-ttu-id="31cf8-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="31cf8-131">RELATED LINKS</span></span>

[<span data-ttu-id="31cf8-132">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="31cf8-132">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="31cf8-133">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="31cf8-133">Set-AzApiManagement</span></span>](./Set-AzApiManagement.md)