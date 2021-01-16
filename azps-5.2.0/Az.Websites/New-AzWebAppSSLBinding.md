---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 910239BE-9E48-4DC5-85EA-CC6D466FE62F
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppSSLBinding.md
ms.openlocfilehash: 2fff18033febbab23083127628959d2fca9305a3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98367102"
---
# <span data-ttu-id="96ebb-101">New-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="96ebb-101">New-AzWebAppSSLBinding</span></span>

## <span data-ttu-id="96ebb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="96ebb-102">SYNOPSIS</span></span>
<span data-ttu-id="96ebb-103">Azure 웹앱에 대한 SSL 인증서 바인딩을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="96ebb-103">Creates an SSL certificate binding for an Azure Web App.</span></span>

## <span data-ttu-id="96ebb-104">구문</span><span class="sxs-lookup"><span data-stu-id="96ebb-104">SYNTAX</span></span>

### <span data-ttu-id="96ebb-105">S1</span><span class="sxs-lookup"><span data-stu-id="96ebb-105">S1</span></span>
```
New-AzWebAppSSLBinding [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>] [-Name] <String>
 [[-SslState] <SslState>] [-CertificateFilePath] <String> [-CertificatePassword] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="96ebb-106">S2</span><span class="sxs-lookup"><span data-stu-id="96ebb-106">S2</span></span>
```
New-AzWebAppSSLBinding [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>] [-Name] <String>
 [[-SslState] <SslState>] [-Thumbprint] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="96ebb-107">S3</span><span class="sxs-lookup"><span data-stu-id="96ebb-107">S3</span></span>
```
New-AzWebAppSSLBinding [-WebApp] <PSSite> [-Name] <String> [[-SslState] <SslState>]
 [-CertificateFilePath] <String> [-CertificatePassword] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="96ebb-108">S4</span><span class="sxs-lookup"><span data-stu-id="96ebb-108">S4</span></span>
```
New-AzWebAppSSLBinding [-WebApp] <PSSite> [-Name] <String> [[-SslState] <SslState>] [-Thumbprint] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="96ebb-109">설명</span><span class="sxs-lookup"><span data-stu-id="96ebb-109">DESCRIPTION</span></span>
<span data-ttu-id="96ebb-110">**New-AzWebAppSSLBinding** cmdlet은 Azure 웹앱에 대한 SSL(Secure Socket Layer) 인증서 바인딩을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="96ebb-110">The **New-AzWebAppSSLBinding** cmdlet creates a Secure Socket Layer (SSL) certificate binding for an Azure Web App.</span></span>
<span data-ttu-id="96ebb-111">cmdlet은 다음 두 가지 방법으로 SSL 바인딩을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="96ebb-111">The cmdlet creates an SSL binding in two ways:</span></span> 
- <span data-ttu-id="96ebb-112">기존 인증서에 웹앱을 바인딩할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="96ebb-112">You can bind a Web App to an existing certificate.</span></span>
- <span data-ttu-id="96ebb-113">새 인증서를 업로드한 다음 웹앱을 이 새 인증서에 바인딩할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="96ebb-113">You can upload a new certificate and then bind the Web App to this new certificate.</span></span>
<span data-ttu-id="96ebb-114">사용하는 방식에 관계없이 인증서와 웹앱은 동일한 Azure 리소스 그룹과 연결되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="96ebb-114">Regardless of which approach you use, the certificate and the Web App must be associated with the same Azure resource group.</span></span>
<span data-ttu-id="96ebb-115">리소스 그룹 A에 웹앱이 있는 경우 해당 웹앱을 리소스 그룹 B의 인증서에 바인딩하려는 경우 인증서 복사본을 리소스 그룹 A에 업로드하는 것이 유일한 방법입니다. 새 인증서를 업로드하는 경우 Azure SSL 인증서에 대한 다음 요구 사항에 유의하세요.</span><span class="sxs-lookup"><span data-stu-id="96ebb-115">If you have a Web App in Resource Group A and you want to bind that Web App to a certificate in Resource Group B, the only way to do that is to upload a copy of the certificate to Resource Group A. If you upload a new certificate, keep in mind the following requirements for an Azure SSL certificate:</span></span> 
- <span data-ttu-id="96ebb-116">인증서는 개인 키를 포함해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="96ebb-116">The certificate must contain a private key.</span></span> 
- <span data-ttu-id="96ebb-117">인증서는 PFX(개인 정보 교환) 형식을 사용해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="96ebb-117">The certificate must use the Personal Information Exchange (PFX) format.</span></span> 
- <span data-ttu-id="96ebb-118">인증서의 주체 이름은 웹앱에 액세스하는 데 사용되는 도메인과 일치해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="96ebb-118">The certificate's subject name must match the domain used to access the Web App.</span></span> 
- <span data-ttu-id="96ebb-119">인증서는 최소 2048비트 암호화를 사용해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="96ebb-119">The certificate must use a minimum of 2048-bit encryption.</span></span>

## <span data-ttu-id="96ebb-120">예제</span><span class="sxs-lookup"><span data-stu-id="96ebb-120">EXAMPLES</span></span>

### <span data-ttu-id="96ebb-121">예제 1: 웹앱에 인증서 바인딩</span><span class="sxs-lookup"><span data-stu-id="96ebb-121">Example 1: Bind a certificate to a Web App</span></span>
```powershell
PS C:\>New-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3" -Name "www.contoso.com"
```

<span data-ttu-id="96ebb-122">이 명령은 기존 Azure 인증서(지문 E3A38EBA60CAA1C162785A2E1C44A15AD450199C3이 있는 인증서)를 ContosoWebApp이라는 웹앱에 바인딩합니다.</span><span class="sxs-lookup"><span data-stu-id="96ebb-122">This command binds an existing Azure certificate (a certificate with the Thumbprint E3A38EBA60CAA1C162785A2E1C44A15AD450199C3) to the web app named ContosoWebApp.</span></span>

### <span data-ttu-id="96ebb-123">예제 2</span><span class="sxs-lookup"><span data-stu-id="96ebb-123">Example 2</span></span>

<span data-ttu-id="96ebb-124">Azure 웹앱에 대한 SSL 인증서 바인딩을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="96ebb-124">Creates an SSL certificate binding for an Azure Web App.</span></span> <span data-ttu-id="96ebb-125">(자동Generated)</span><span class="sxs-lookup"><span data-stu-id="96ebb-125">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzWebAppSSLBinding -Name 'www.contoso.com' -ResourceGroupName 'ContosoResourceGroup' -SslState Disabled -Thumbprint 'E3A38EBA60CAA1C162785A2E1C44A15AD450199C3' -WebAppName 'ContosoWebApp'
```

## <span data-ttu-id="96ebb-126">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="96ebb-126">PARAMETERS</span></span>

### <span data-ttu-id="96ebb-127">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="96ebb-127">-CertificateFilePath</span></span>
<span data-ttu-id="96ebb-128">업로드할 인증서의 파일 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="96ebb-128">Specifies the file path for the certificate to be uploaded.</span></span>
<span data-ttu-id="96ebb-129">*CertificateFilePath* 매개 변수는 인증서가 아직 Azure에 업로드되지 않은 경우 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="96ebb-129">The *CertificateFilePath* parameter is only required if the certificate has not yet been uploaded to Azure.</span></span>

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

### <span data-ttu-id="96ebb-130">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="96ebb-130">-CertificatePassword</span></span>
<span data-ttu-id="96ebb-131">인증서의 암호 해독 암호를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="96ebb-131">Specifies the decryption password for the certificate.</span></span>

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

### <span data-ttu-id="96ebb-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96ebb-132">-DefaultProfile</span></span>
<span data-ttu-id="96ebb-133">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="96ebb-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="96ebb-134">-Name</span><span class="sxs-lookup"><span data-stu-id="96ebb-134">-Name</span></span>
<span data-ttu-id="96ebb-135">웹앱의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="96ebb-135">Specifies the name of the Web App.</span></span>

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

### <span data-ttu-id="96ebb-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96ebb-136">-ResourceGroupName</span></span>
<span data-ttu-id="96ebb-137">인증서가 할당된 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="96ebb-137">Specifies the name of the resource group that the certificate is assigned to.</span></span>
<span data-ttu-id="96ebb-138">동일한 명령에서 *ResourceGroupName* 매개 변수 및 *WebApp* 매개 변수를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="96ebb-138">You cannot use the *ResourceGroupName* parameter and the *WebApp* parameter in the same command.</span></span>

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

### <span data-ttu-id="96ebb-139">-Slot</span><span class="sxs-lookup"><span data-stu-id="96ebb-139">-Slot</span></span>
<span data-ttu-id="96ebb-140">웹앱 배포 슬롯의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="96ebb-140">Specifies the name of the Web App deployment slot.</span></span>
<span data-ttu-id="96ebb-141">Get-AzWebAppSlot cmdlet을 사용하여 슬롯을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="96ebb-141">You can use the Get-AzWebAppSlot cmdlet to get a slot.</span></span>
<span data-ttu-id="96ebb-142">배포 슬롯은 인터넷을 통해 액세스할 수 없는 웹앱을 준비하고 유효성을 검사할 수 있는 방법을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="96ebb-142">Deployment slots provide a way for you to stage and validate web apps without those apps being accessible over the Internet.</span></span>
<span data-ttu-id="96ebb-143">일반적으로 스테이징 사이트에 변경 내용을 배포하고 해당 변경 내용의 유효성을 검사한 다음 프로덕션(인터넷 액세스 가능) 사이트에 배포합니다.</span><span class="sxs-lookup"><span data-stu-id="96ebb-143">Typically you will deploy your changes to a staging site, validate those changes, and then deploy to the production (Internet-accessible) site.</span></span>

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

### <span data-ttu-id="96ebb-144">-SslState</span><span class="sxs-lookup"><span data-stu-id="96ebb-144">-SslState</span></span>
<span data-ttu-id="96ebb-145">인증서를 사용하도록 설정하는지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="96ebb-145">Specifies whether the certificate is enabled.</span></span>
<span data-ttu-id="96ebb-146">*SSLState* 매개 변수를 1로 설정하여 인증서를 사용하도록 설정하거나 *SSLState를* 0으로 설정하여 인증서를 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="96ebb-146">Set the *SSLState* parameter to 1 to enable the certificate, or set *SSLState* to 0 to disable the certificate.</span></span>

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

### <span data-ttu-id="96ebb-147">-Thumbprint</span><span class="sxs-lookup"><span data-stu-id="96ebb-147">-Thumbprint</span></span>
<span data-ttu-id="96ebb-148">인증서에 대한 고유 식별자를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="96ebb-148">Specifies the unique identifier for the certificate.</span></span>

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

### <span data-ttu-id="96ebb-149">-WebApp</span><span class="sxs-lookup"><span data-stu-id="96ebb-149">-WebApp</span></span>
<span data-ttu-id="96ebb-150">웹앱을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="96ebb-150">Specifies a Web App.</span></span>
<span data-ttu-id="96ebb-151">웹앱을 얻습니다. Get-AzWebApp cmdlet을 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="96ebb-151">To get a Web App, use the Get-AzWebApp cmdlet.</span></span>
<span data-ttu-id="96ebb-152">*ResourceGroupName* 매개 변수 및/또는 *WebAppName과* 동일한 명령에서 *WebApp* 매개 변수를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="96ebb-152">You cannot use the *WebApp* parameter in the same command as the *ResourceGroupName* parameter and/or the *WebAppName*.</span></span>

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

### <span data-ttu-id="96ebb-153">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="96ebb-153">-WebAppName</span></span>
<span data-ttu-id="96ebb-154">새 SSL 바인딩을 만들 웹앱의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="96ebb-154">Specifies the name of the Web App for which the new SSL binding is being created.</span></span>
<span data-ttu-id="96ebb-155">동일한 명령에서 *WebAppName* 매개 변수 및 *WebApp* 매개 변수를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="96ebb-155">You cannot use the *WebAppName* parameter and the *WebApp* parameter in the same command.</span></span>

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

### <span data-ttu-id="96ebb-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96ebb-156">CommonParameters</span></span>
<span data-ttu-id="96ebb-157">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="96ebb-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96ebb-158">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="96ebb-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96ebb-159">입력</span><span class="sxs-lookup"><span data-stu-id="96ebb-159">INPUTS</span></span>

### <span data-ttu-id="96ebb-160">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="96ebb-160">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="96ebb-161">출력</span><span class="sxs-lookup"><span data-stu-id="96ebb-161">OUTPUTS</span></span>

### <span data-ttu-id="96ebb-162">Microsoft.Azure.Management.WebSites.Models.HostNameSslState</span><span class="sxs-lookup"><span data-stu-id="96ebb-162">Microsoft.Azure.Management.WebSites.Models.HostNameSslState</span></span>

## <span data-ttu-id="96ebb-163">참고 사항</span><span class="sxs-lookup"><span data-stu-id="96ebb-163">NOTES</span></span>

## <span data-ttu-id="96ebb-164">관련 링크</span><span class="sxs-lookup"><span data-stu-id="96ebb-164">RELATED LINKS</span></span>

[<span data-ttu-id="96ebb-165">Get-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="96ebb-165">Get-AzWebAppSSLBinding</span></span>](./Get-AzWebAppSSLBinding.md)

[<span data-ttu-id="96ebb-166">Remove-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="96ebb-166">Remove-AzWebAppSSLBinding</span></span>](./Remove-AzWebAppSSLBinding.md)

[<span data-ttu-id="96ebb-167">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="96ebb-167">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="96ebb-168">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="96ebb-168">Get-AzWebApp</span></span>](./Get-AzWebApp.md)


