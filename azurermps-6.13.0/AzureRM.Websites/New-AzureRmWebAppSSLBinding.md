---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 910239BE-9E48-4DC5-85EA-CC6D466FE62F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/new-azurermwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppSSLBinding.md
ms.openlocfilehash: 33efe02dd463334745e39d846d0b43c2ccd9dd6b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93704090"
---
# <span data-ttu-id="46b1b-101">New-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="46b1b-101">New-AzureRmWebAppSSLBinding</span></span>

## <span data-ttu-id="46b1b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46b1b-102">SYNOPSIS</span></span>
<span data-ttu-id="46b1b-103">Azure Web App에 대 한 SSL 인증서 바인딩을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="46b1b-103">Creates an SSL certificate binding for an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="46b1b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="46b1b-104">SYNTAX</span></span>

### <span data-ttu-id="46b1b-105">S1</span><span class="sxs-lookup"><span data-stu-id="46b1b-105">S1</span></span>
```
New-AzureRmWebAppSSLBinding [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>]
 [-Name] <String> [[-SslState] <SslState>] [-CertificateFilePath] <String> [-CertificatePassword] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="46b1b-106">구성원과</span><span class="sxs-lookup"><span data-stu-id="46b1b-106">S2</span></span>
```
New-AzureRmWebAppSSLBinding [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>]
 [-Name] <String> [[-SslState] <SslState>] [-Thumbprint] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="46b1b-107">시스템이</span><span class="sxs-lookup"><span data-stu-id="46b1b-107">S3</span></span>
```
New-AzureRmWebAppSSLBinding [-WebApp] <PSSite> [-Name] <String> [[-SslState] <SslState>]
 [-CertificateFilePath] <String> [-CertificatePassword] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="46b1b-108">S4</span><span class="sxs-lookup"><span data-stu-id="46b1b-108">S4</span></span>
```
New-AzureRmWebAppSSLBinding [-WebApp] <PSSite> [-Name] <String> [[-SslState] <SslState>] [-Thumbprint] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="46b1b-109">설명은</span><span class="sxs-lookup"><span data-stu-id="46b1b-109">DESCRIPTION</span></span>
<span data-ttu-id="46b1b-110">**AzureRmWebAppSSLBinding** Cmdlet은 Azure Web App에 대 한 SSL (Secure Socket Layer) 인증서 바인딩을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="46b1b-110">The **New-AzureRmWebAppSSLBinding** cmdlet creates a Secure Socket Layer (SSL) certificate binding for an Azure Web App.</span></span>
<span data-ttu-id="46b1b-111">Cmdlet은 다음과 같은 두 가지 방법으로 SSL 바인딩을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="46b1b-111">The cmdlet creates an SSL binding in two ways:</span></span> 
- <span data-ttu-id="46b1b-112">웹 앱을 기존 인증서에 바인딩할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="46b1b-112">You can bind a Web App to an existing certificate.</span></span>
- <span data-ttu-id="46b1b-113">새 인증서를 업로드 한 다음 웹 앱을 새 인증서에 바인딩할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="46b1b-113">You can upload a new certificate and then bind the Web App to this new certificate.</span></span>
<span data-ttu-id="46b1b-114">사용 하는 방법에 관계 없이 인증서와 웹 앱은 동일한 Azure 리소스 그룹과 연결 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="46b1b-114">Regardless of which approach you use, the certificate and the Web App must be associated with the same Azure resource group.</span></span>
<span data-ttu-id="46b1b-115">리소스 그룹 A에 웹 앱이 있고 리소스 그룹 B의 인증서에 웹 앱을 바인딩하는 경우 유일한 방법은 리소스 그룹 A에 인증서 복사본을 업로드 하는 것입니다. 새 인증서를 업로드 하는 경우 Azure SSL 인증서에 대 한 다음 요구 사항을 염두에 두어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="46b1b-115">If you have a Web App in Resource Group A and you want to bind that Web App to a certificate in Resource Group B, the only way to do that is to upload a copy of the certificate to Resource Group A. If you upload a new certificate, keep in mind the following requirements for an Azure SSL certificate:</span></span> 
- <span data-ttu-id="46b1b-116">인증서에는 개인 키가 포함 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="46b1b-116">The certificate must contain a private key.</span></span> 
- <span data-ttu-id="46b1b-117">인증서는 PFX (개인 정보 교환) 형식을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="46b1b-117">The certificate must use the Personal Information Exchange (PFX) format.</span></span> 
- <span data-ttu-id="46b1b-118">인증서의 주체 이름은 웹 앱에 액세스 하는 데 사용 되는 도메인과 일치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="46b1b-118">The certificate's subject name must match the domain used to access the Web App.</span></span> 
- <span data-ttu-id="46b1b-119">인증서는 최소 2048 비트 암호화를 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="46b1b-119">The certificate must use a minimum of 2048-bit encryption.</span></span>

## <span data-ttu-id="46b1b-120">예제의</span><span class="sxs-lookup"><span data-stu-id="46b1b-120">EXAMPLES</span></span>

### <span data-ttu-id="46b1b-121">예제 1: 웹 앱에 인증서 바인딩</span><span class="sxs-lookup"><span data-stu-id="46b1b-121">Example 1: Bind a certificate to a Web App</span></span>
```
PS C:\>New-AzureRmWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3" -Name "www.contoso.com"
```

<span data-ttu-id="46b1b-122">이 명령은 기존 Azure 인증서 (지문이 E3A38EBA60CAA1C162785A2E1C44A15AD450199C3 인 인증서)를 ContosoWebApp 이라는 웹 앱에 바인딩합니다.</span><span class="sxs-lookup"><span data-stu-id="46b1b-122">This command binds an existing Azure certificate (a certificate with the Thumbprint E3A38EBA60CAA1C162785A2E1C44A15AD450199C3) to the web app named ContosoWebApp.</span></span>

## <span data-ttu-id="46b1b-123">변수</span><span class="sxs-lookup"><span data-stu-id="46b1b-123">PARAMETERS</span></span>

### <span data-ttu-id="46b1b-124">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="46b1b-124">-CertificateFilePath</span></span>
<span data-ttu-id="46b1b-125">업로드할 인증서의 파일 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="46b1b-125">Specifies the file path for the certificate to be uploaded.</span></span>
<span data-ttu-id="46b1b-126">*Certificatefilepath* 매개 변수는 인증서가 아직 Azure에 업로드 되지 않은 경우에만 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="46b1b-126">The *CertificateFilePath* parameter is only required if the certificate has not yet been uploaded to Azure.</span></span>

```yaml
Type: System.String
Parameter Sets: S1, S3
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46b1b-127">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="46b1b-127">-CertificatePassword</span></span>
<span data-ttu-id="46b1b-128">인증서 암호를 해독 합니다.</span><span class="sxs-lookup"><span data-stu-id="46b1b-128">Specifies the decryption password for the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: S1, S3
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46b1b-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46b1b-129">-DefaultProfile</span></span>
<span data-ttu-id="46b1b-130">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="46b1b-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="46b1b-131">-이름</span><span class="sxs-lookup"><span data-stu-id="46b1b-131">-Name</span></span>
<span data-ttu-id="46b1b-132">웹 앱의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="46b1b-132">Specifies the name of the Web App.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46b1b-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46b1b-133">-ResourceGroupName</span></span>
<span data-ttu-id="46b1b-134">인증서가 할당 되는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="46b1b-134">Specifies the name of the resource group that the certificate is assigned to.</span></span>
<span data-ttu-id="46b1b-135">동일한 명령에서 *ResourceGroupName* 매개 변수와 *web app* 매개 변수를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="46b1b-135">You cannot use the *ResourceGroupName* parameter and the *WebApp* parameter in the same command.</span></span>

```yaml
Type: System.String
Parameter Sets: S1, S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46b1b-136">-슬롯</span><span class="sxs-lookup"><span data-stu-id="46b1b-136">-Slot</span></span>
<span data-ttu-id="46b1b-137">웹 앱 배포 슬롯의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="46b1b-137">Specifies the name of the Web App deployment slot.</span></span>
<span data-ttu-id="46b1b-138">Get-AzureRMWebAppSlot cmdlet을 사용 하 여 슬롯을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="46b1b-138">You can use the Get-AzureRMWebAppSlot cmdlet to get a slot.</span></span>
<span data-ttu-id="46b1b-139">배포 슬롯은 인터넷을 통해 해당 앱에 액세스할 수 없는 웹 앱을 준비 하 고 유효성을 검사할 수 있는 방법을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="46b1b-139">Deployment slots provide a way for you to stage and validate web apps without those apps being accessible over the Internet.</span></span>
<span data-ttu-id="46b1b-140">일반적으로 변경 내용을 준비 사이트에 배포 하 고 해당 변경의 유효성을 검사 한 다음 프로덕션 (인터넷 액세스 가능) 사이트에 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="46b1b-140">Typically you will deploy your changes to a staging site, validate those changes, and then deploy to the production (Internet-accessible) site.</span></span>

```yaml
Type: System.String
Parameter Sets: S1, S2
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46b1b-141">-SslState</span><span class="sxs-lookup"><span data-stu-id="46b1b-141">-SslState</span></span>
<span data-ttu-id="46b1b-142">인증서를 사용할 수 있는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="46b1b-142">Specifies whether the certificate is enabled.</span></span>
<span data-ttu-id="46b1b-143">*Sslstate* 매개 변수를 1로 설정 하 여 인증서를 활성화 하거나, *sslstate* 를 0으로 설정 하 여 인증서를 비활성화 합니다.</span><span class="sxs-lookup"><span data-stu-id="46b1b-143">Set the *SSLState* parameter to 1 to enable the certificate, or set *SSLState* to 0 to disable the certificate.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.WebSites.Models.SslState]
Parameter Sets: (All)
Aliases:
Accepted values: Disabled, SniEnabled, IpBasedEnabled

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46b1b-144">-지문</span><span class="sxs-lookup"><span data-stu-id="46b1b-144">-Thumbprint</span></span>
<span data-ttu-id="46b1b-145">인증서에 대 한 고유 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="46b1b-145">Specifies the unique identifier for the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: S2, S4
Aliases:

Required: True
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46b1b-146">-Web app</span><span class="sxs-lookup"><span data-stu-id="46b1b-146">-WebApp</span></span>
<span data-ttu-id="46b1b-147">웹 앱을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="46b1b-147">Specifies a Web App.</span></span>
<span data-ttu-id="46b1b-148">웹 앱을 가져오려면 Get-AzureRmWebApp cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="46b1b-148">To get a Web App, use the Get-AzureRmWebApp cmdlet.</span></span>
<span data-ttu-id="46b1b-149">*ResourceGroupName* 매개 변수 및/또는 *webappname* 과 동일한 명령에서 *web app* 매개 변수를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="46b1b-149">You cannot use the *WebApp* parameter in the same command as the *ResourceGroupName* parameter and/or the *WebAppName*.</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S3, S4
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="46b1b-150">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="46b1b-150">-WebAppName</span></span>
<span data-ttu-id="46b1b-151">새 SSL 바인딩이 생성 되는 웹 앱의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="46b1b-151">Specifies the name of the Web App for which the new SSL binding is being created.</span></span>
<span data-ttu-id="46b1b-152">동일한 명령에서 *Webappname* 매개 변수와 *web app* 매개 변수를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="46b1b-152">You cannot use the *WebAppName* parameter and the *WebApp* parameter in the same command.</span></span>

```yaml
Type: System.String
Parameter Sets: S1, S2
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46b1b-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46b1b-153">CommonParameters</span></span>
<span data-ttu-id="46b1b-154">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="46b1b-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46b1b-155">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46b1b-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46b1b-156">입력</span><span class="sxs-lookup"><span data-stu-id="46b1b-156">INPUTS</span></span>

### <span data-ttu-id="46b1b-157">Microsoft. Azure. 사이트</span><span class="sxs-lookup"><span data-stu-id="46b1b-157">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="46b1b-158">매개 변수: Web app (ByValue)</span><span class="sxs-lookup"><span data-stu-id="46b1b-158">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="46b1b-159">출력</span><span class="sxs-lookup"><span data-stu-id="46b1b-159">OUTPUTS</span></span>

### <span data-ttu-id="46b1b-160">Microsoft. Azure. 관리. i m m 네임 스페이스. i m m Namesslstate</span><span class="sxs-lookup"><span data-stu-id="46b1b-160">Microsoft.Azure.Management.WebSites.Models.HostNameSslState</span></span>

## <span data-ttu-id="46b1b-161">상속자</span><span class="sxs-lookup"><span data-stu-id="46b1b-161">NOTES</span></span>

## <span data-ttu-id="46b1b-162">관련 링크</span><span class="sxs-lookup"><span data-stu-id="46b1b-162">RELATED LINKS</span></span>

[<span data-ttu-id="46b1b-163">Get-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="46b1b-163">Get-AzureRmWebAppSSLBinding</span></span>](./Get-AzureRmWebAppSSLBinding.md)

[<span data-ttu-id="46b1b-164">제거-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="46b1b-164">Remove-AzureRmWebAppSSLBinding</span></span>](./Remove-AzureRmWebAppSSLBinding.md)

[<span data-ttu-id="46b1b-165">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="46b1b-165">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="46b1b-166">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="46b1b-166">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)


