---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 910239BE-9E48-4DC5-85EA-CC6D466FE62F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppSSLBinding.md
ms.openlocfilehash: 99d7d4a0feeb0f548ef65d06234eecb1ad2baf6c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536903"
---
# <span data-ttu-id="5190c-101">New-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="5190c-101">New-AzureRmWebAppSSLBinding</span></span>

## <span data-ttu-id="5190c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5190c-102">SYNOPSIS</span></span>
<span data-ttu-id="5190c-103">Azure Web App에 대 한 SSL 인증서 바인딩을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5190c-103">Creates an SSL certificate binding for an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5190c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5190c-104">SYNTAX</span></span>

### <span data-ttu-id="5190c-105">S1</span><span class="sxs-lookup"><span data-stu-id="5190c-105">S1</span></span>
```
New-AzureRmWebAppSSLBinding [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>]
 [-Name] <String> [[-SslState] <SslState>] [-CertificateFilePath] <String> [-CertificatePassword] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5190c-106">구성원과</span><span class="sxs-lookup"><span data-stu-id="5190c-106">S2</span></span>
```
New-AzureRmWebAppSSLBinding [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>]
 [-Name] <String> [[-SslState] <SslState>] [-Thumbprint] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5190c-107">시스템이</span><span class="sxs-lookup"><span data-stu-id="5190c-107">S3</span></span>
```
New-AzureRmWebAppSSLBinding [-WebApp] <Site> [-Name] <String> [[-SslState] <SslState>]
 [-CertificateFilePath] <String> [-CertificatePassword] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5190c-108">S4</span><span class="sxs-lookup"><span data-stu-id="5190c-108">S4</span></span>
```
New-AzureRmWebAppSSLBinding [-WebApp] <Site> [-Name] <String> [[-SslState] <SslState>] [-Thumbprint] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5190c-109">설명은</span><span class="sxs-lookup"><span data-stu-id="5190c-109">DESCRIPTION</span></span>
<span data-ttu-id="5190c-110">**AzureRmWebAppSSLBinding** Cmdlet은 Azure Web App에 대 한 SSL (Secure Socket Layer) 인증서 바인딩을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5190c-110">The **New-AzureRmWebAppSSLBinding** cmdlet creates a Secure Socket Layer (SSL) certificate binding for an Azure Web App.</span></span>
<span data-ttu-id="5190c-111">Cmdlet은 다음과 같은 두 가지 방법으로 SSL 바인딩을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5190c-111">The cmdlet creates an SSL binding in two ways:</span></span> 

- <span data-ttu-id="5190c-112">웹 앱을 기존 인증서에 바인딩할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5190c-112">You can bind a Web App to an existing certificate.</span></span>
- <span data-ttu-id="5190c-113">새 인증서를 업로드 한 다음 웹 앱을 새 인증서에 바인딩할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5190c-113">You can upload a new certificate and then bind the Web App to this new certificate.</span></span>

<span data-ttu-id="5190c-114">사용 하는 방법에 관계 없이 인증서와 웹 앱은 동일한 Azure 리소스 그룹과 연결 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5190c-114">Regardless of which approach you use, the certificate and the Web App must be associated with the same Azure resource group.</span></span>
<span data-ttu-id="5190c-115">리소스 그룹 A에 웹 앱이 있고 리소스 그룹 B의 인증서에 웹 앱을 바인딩하는 경우 유일한 방법은 리소스 그룹 A에 인증서 복사본을 업로드 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="5190c-115">If you have a Web App in Resource Group A and you want to bind that Web App to a certificate in Resource Group B, the only way to do that is to upload a copy of the certificate to Resource Group A.</span></span>

<span data-ttu-id="5190c-116">새 인증서를 업로드 하는 경우 Azure SSL 인증서에 대 한 다음 요구 사항을 염두에 두어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5190c-116">If you upload a new certificate, keep in mind the following requirements for an Azure SSL certificate:</span></span> 

- <span data-ttu-id="5190c-117">인증서에는 개인 키가 포함 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5190c-117">The certificate must contain a private key.</span></span> 
- <span data-ttu-id="5190c-118">인증서는 PFX (개인 정보 교환) 형식을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5190c-118">The certificate must use the Personal Information Exchange (PFX) format.</span></span> 
- <span data-ttu-id="5190c-119">인증서의 주체 이름은 웹 앱에 액세스 하는 데 사용 되는 도메인과 일치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5190c-119">The certificate's subject name must match the domain used to access the Web App.</span></span> 
- <span data-ttu-id="5190c-120">인증서는 최소 2048 비트 암호화를 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5190c-120">The certificate must use a minimum of 2048-bit encryption.</span></span>

## <span data-ttu-id="5190c-121">예제의</span><span class="sxs-lookup"><span data-stu-id="5190c-121">EXAMPLES</span></span>

### <span data-ttu-id="5190c-122">예제 1: 웹 앱에 인증서 바인딩</span><span class="sxs-lookup"><span data-stu-id="5190c-122">Example 1: Bind a certificate to a Web App</span></span>
```
PS C:\>New-AzureRmWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3" -Name "www.contoso.com" -CertificatePassword "p@ssw0rd"
```

<span data-ttu-id="5190c-123">이 명령은 기존 Azure 인증서 (지문이 E3A38EBA60CAA1C162785A2E1C44A15AD450199C3 인 인증서)를 ContosoWebApp 이라는 웹 앱에 바인딩합니다.</span><span class="sxs-lookup"><span data-stu-id="5190c-123">This command binds an existing Azure certificate (a certificate with the Thumbprint E3A38EBA60CAA1C162785A2E1C44A15AD450199C3) to the web app named ContosoWebApp.</span></span>

### <span data-ttu-id="5190c-124">예제 2: 인증서를 업로드 하 고 웹 앱에 바인딩</span><span class="sxs-lookup"><span data-stu-id="5190c-124">Example 2: Upload a certificate and bind it to a Web App</span></span>
```
PS C:\>New-AzureRmWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3" -Name "www.contoso.com" -CertificatePassword "p@ssw0rd" -CertificateFilePath "C:\Certificates\ContosoWebSite.pfx"
```

<span data-ttu-id="5190c-125">예제 2에서는 인증서 E3A38EBA60CAA1C162785A2E1C44A15AD450199C3를 ContosoWebApp 이라는 웹 앱에도 바인딩합니다.</span><span class="sxs-lookup"><span data-stu-id="5190c-125">Example 2 also binds the certificate E3A38EBA60CAA1C162785A2E1C44A15AD450199C3 to the Web App named ContosoWebApp.</span></span>
<span data-ttu-id="5190c-126">그러나이 경우 인증서는 아직 Azure에 업로드 되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="5190c-126">In this case, however, the certificate has not yet been uploaded to Azure.</span></span>
<span data-ttu-id="5190c-127">따라서 *Certificatefilepath* 매개 변수는 인증서의 로컬 복사본을 지정 하는 데 사용 됩니다. PFX 파일.</span><span class="sxs-lookup"><span data-stu-id="5190c-127">Because of that, the *CertificateFilePath* parameter is used to specify the local copy of the certificate .PFX file.</span></span>
<span data-ttu-id="5190c-128">이 인증서가 Azure에 업로드 되 고 새 SSL 바인딩이 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5190c-128">This certificate will be uploaded to Azure and then the new SSL bindings will be created.</span></span>

## <span data-ttu-id="5190c-129">변수</span><span class="sxs-lookup"><span data-stu-id="5190c-129">PARAMETERS</span></span>

### <span data-ttu-id="5190c-130">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="5190c-130">-CertificateFilePath</span></span>
<span data-ttu-id="5190c-131">업로드할 인증서의 파일 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5190c-131">Specifies the file path for the certificate to be uploaded.</span></span>

<span data-ttu-id="5190c-132">*Certificatefilepath* 매개 변수는 인증서가 아직 Azure에 업로드 되지 않은 경우에만 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="5190c-132">The *CertificateFilePath* parameter is only required if the certificate has not yet been uploaded to Azure.</span></span>

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

### <span data-ttu-id="5190c-133">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="5190c-133">-CertificatePassword</span></span>
<span data-ttu-id="5190c-134">인증서 암호를 해독 합니다.</span><span class="sxs-lookup"><span data-stu-id="5190c-134">Specifies the decryption password for the certificate.</span></span>

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

### <span data-ttu-id="5190c-135">-이름</span><span class="sxs-lookup"><span data-stu-id="5190c-135">-Name</span></span>
<span data-ttu-id="5190c-136">웹 앱의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5190c-136">Specifies the name of the Web App.</span></span>

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

### <span data-ttu-id="5190c-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5190c-137">-ResourceGroupName</span></span>
<span data-ttu-id="5190c-138">인증서가 할당 되는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5190c-138">Specifies the name of the resource group that the certificate is assigned to.</span></span>

<span data-ttu-id="5190c-139">동일한 명령에서 *ResourceGroupName* 매개 변수와 *web app* 매개 변수를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="5190c-139">You cannot use the *ResourceGroupName* parameter and the *WebApp* parameter in the same command.</span></span>

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

### <span data-ttu-id="5190c-140">-슬롯</span><span class="sxs-lookup"><span data-stu-id="5190c-140">-Slot</span></span>
<span data-ttu-id="5190c-141">웹 앱 배포 슬롯의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5190c-141">Specifies the name of the Web App deployment slot.</span></span>
<span data-ttu-id="5190c-142">Get-AzureRMWebAppSlot cmdlet을 사용 하 여 슬롯을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5190c-142">You can use the Get-AzureRMWebAppSlot cmdlet to get a slot.</span></span>

<span data-ttu-id="5190c-143">배포 슬롯은 인터넷을 통해 해당 앱에 액세스할 수 없는 웹 앱을 준비 하 고 유효성을 검사할 수 있는 방법을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="5190c-143">Deployment slots provide a way for you to stage and validate web apps without those apps being accessible over the Internet.</span></span>
<span data-ttu-id="5190c-144">일반적으로 변경 내용을 준비 사이트에 배포 하 고 해당 변경의 유효성을 검사 한 다음 프로덕션 (인터넷 액세스 가능) 사이트에 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="5190c-144">Typically you will deploy your changes to a staging site, validate those changes, and then deploy to the production (Internet-accessible) site.</span></span>

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

### <span data-ttu-id="5190c-145">-SslState</span><span class="sxs-lookup"><span data-stu-id="5190c-145">-SslState</span></span>
<span data-ttu-id="5190c-146">인증서를 사용할 수 있는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5190c-146">Specifies whether the certificate is enabled.</span></span>
<span data-ttu-id="5190c-147">*Sslstate* 매개 변수를 1로 설정 하 여 인증서를 활성화 하거나, *sslstate* 를 0으로 설정 하 여 인증서를 비활성화 합니다.</span><span class="sxs-lookup"><span data-stu-id="5190c-147">Set the *SSLState* parameter to 1 to enable the certificate, or set *SSLState* to 0 to disable the certificate.</span></span>

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

### <span data-ttu-id="5190c-148">-지문</span><span class="sxs-lookup"><span data-stu-id="5190c-148">-Thumbprint</span></span>
<span data-ttu-id="5190c-149">인증서에 대 한 고유 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5190c-149">Specifies the unique identifier for the certificate.</span></span>

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

### <span data-ttu-id="5190c-150">-Web app</span><span class="sxs-lookup"><span data-stu-id="5190c-150">-WebApp</span></span>
<span data-ttu-id="5190c-151">웹 앱을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5190c-151">Specifies a Web App.</span></span>
<span data-ttu-id="5190c-152">웹 앱을 가져오려면 Get-AzureRmWebApp cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5190c-152">To get a Web App, use the Get-AzureRmWebApp cmdlet.</span></span>

<span data-ttu-id="5190c-153">*ResourceGroupName* 매개 변수 및/또는 *webappname* 과 동일한 명령에서 *web app* 매개 변수를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="5190c-153">You cannot use the *WebApp* parameter in the same command as the *ResourceGroupName* parameter and/or the *WebAppName*.</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: S3, S4
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5190c-154">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="5190c-154">-WebAppName</span></span>
<span data-ttu-id="5190c-155">새 SSL 바인딩이 생성 되는 웹 앱의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5190c-155">Specifies the name of the Web App for which the new SSL binding is being created.</span></span>

<span data-ttu-id="5190c-156">동일한 명령에서 *Webappname* 매개 변수와 *web app* 매개 변수를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="5190c-156">You cannot use the *WebAppName* parameter and the *WebApp* parameter in the same command.</span></span>

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

### <span data-ttu-id="5190c-157">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5190c-157">-DefaultProfile</span></span>
<span data-ttu-id="5190c-158">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5190c-158">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5190c-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5190c-159">CommonParameters</span></span>
<span data-ttu-id="5190c-160">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5190c-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5190c-161">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5190c-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5190c-162">입력</span><span class="sxs-lookup"><span data-stu-id="5190c-162">INPUTS</span></span>

### <span data-ttu-id="5190c-163">Site</span><span class="sxs-lookup"><span data-stu-id="5190c-163">Site</span></span>
<span data-ttu-id="5190c-164">' Web app ' 매개 변수는 파이프라인에서 ' Site ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5190c-164">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="5190c-165">출력</span><span class="sxs-lookup"><span data-stu-id="5190c-165">OUTPUTS</span></span>

## <span data-ttu-id="5190c-166">상속자</span><span class="sxs-lookup"><span data-stu-id="5190c-166">NOTES</span></span>

## <span data-ttu-id="5190c-167">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5190c-167">RELATED LINKS</span></span>

[<span data-ttu-id="5190c-168">Get-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="5190c-168">Get-AzureRmWebAppSSLBinding</span></span>](./Get-AzureRmWebAppSSLBinding.md)

[<span data-ttu-id="5190c-169">제거-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="5190c-169">Remove-AzureRmWebAppSSLBinding</span></span>](./Remove-AzureRmWebAppSSLBinding.md)

[<span data-ttu-id="5190c-170">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="5190c-170">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="5190c-171">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="5190c-171">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)


