---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 910239BE-9E48-4DC5-85EA-CC6D466FE62F
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppSSLBinding.md
ms.openlocfilehash: 2fff18033febbab23083127628959d2fca9305a3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213122"
---
# <span data-ttu-id="c991d-101">New-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="c991d-101">New-AzWebAppSSLBinding</span></span>

## <span data-ttu-id="c991d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c991d-102">SYNOPSIS</span></span>
<span data-ttu-id="c991d-103">Azure Web App에 대 한 SSL 인증서 바인딩을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c991d-103">Creates an SSL certificate binding for an Azure Web App.</span></span>

## <span data-ttu-id="c991d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c991d-104">SYNTAX</span></span>

### <span data-ttu-id="c991d-105">S1</span><span class="sxs-lookup"><span data-stu-id="c991d-105">S1</span></span>
```
New-AzWebAppSSLBinding [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>] [-Name] <String>
 [[-SslState] <SslState>] [-CertificateFilePath] <String> [-CertificatePassword] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c991d-106">구성원과</span><span class="sxs-lookup"><span data-stu-id="c991d-106">S2</span></span>
```
New-AzWebAppSSLBinding [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>] [-Name] <String>
 [[-SslState] <SslState>] [-Thumbprint] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c991d-107">시스템이</span><span class="sxs-lookup"><span data-stu-id="c991d-107">S3</span></span>
```
New-AzWebAppSSLBinding [-WebApp] <PSSite> [-Name] <String> [[-SslState] <SslState>]
 [-CertificateFilePath] <String> [-CertificatePassword] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c991d-108">S4</span><span class="sxs-lookup"><span data-stu-id="c991d-108">S4</span></span>
```
New-AzWebAppSSLBinding [-WebApp] <PSSite> [-Name] <String> [[-SslState] <SslState>] [-Thumbprint] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c991d-109">설명은</span><span class="sxs-lookup"><span data-stu-id="c991d-109">DESCRIPTION</span></span>
<span data-ttu-id="c991d-110">**AzWebAppSSLBinding** Cmdlet은 Azure Web App에 대 한 SSL (Secure Socket Layer) 인증서 바인딩을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c991d-110">The **New-AzWebAppSSLBinding** cmdlet creates a Secure Socket Layer (SSL) certificate binding for an Azure Web App.</span></span>
<span data-ttu-id="c991d-111">Cmdlet은 다음과 같은 두 가지 방법으로 SSL 바인딩을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c991d-111">The cmdlet creates an SSL binding in two ways:</span></span> 
- <span data-ttu-id="c991d-112">웹 앱을 기존 인증서에 바인딩할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c991d-112">You can bind a Web App to an existing certificate.</span></span>
- <span data-ttu-id="c991d-113">새 인증서를 업로드 한 다음 웹 앱을 새 인증서에 바인딩할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c991d-113">You can upload a new certificate and then bind the Web App to this new certificate.</span></span>
<span data-ttu-id="c991d-114">사용 하는 방법에 관계 없이 인증서와 웹 앱은 동일한 Azure 리소스 그룹과 연결 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c991d-114">Regardless of which approach you use, the certificate and the Web App must be associated with the same Azure resource group.</span></span>
<span data-ttu-id="c991d-115">리소스 그룹 A에 웹 앱이 있고 리소스 그룹 B의 인증서에 웹 앱을 바인딩하는 경우 유일한 방법은 리소스 그룹 A에 인증서 복사본을 업로드 하는 것입니다. 새 인증서를 업로드 하는 경우 Azure SSL 인증서에 대 한 다음 요구 사항을 염두에 두어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c991d-115">If you have a Web App in Resource Group A and you want to bind that Web App to a certificate in Resource Group B, the only way to do that is to upload a copy of the certificate to Resource Group A. If you upload a new certificate, keep in mind the following requirements for an Azure SSL certificate:</span></span> 
- <span data-ttu-id="c991d-116">인증서에는 개인 키가 포함 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c991d-116">The certificate must contain a private key.</span></span> 
- <span data-ttu-id="c991d-117">인증서는 PFX (개인 정보 교환) 형식을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c991d-117">The certificate must use the Personal Information Exchange (PFX) format.</span></span> 
- <span data-ttu-id="c991d-118">인증서의 주체 이름은 웹 앱에 액세스 하는 데 사용 되는 도메인과 일치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c991d-118">The certificate's subject name must match the domain used to access the Web App.</span></span> 
- <span data-ttu-id="c991d-119">인증서는 최소 2048 비트 암호화를 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c991d-119">The certificate must use a minimum of 2048-bit encryption.</span></span>

## <span data-ttu-id="c991d-120">예제의</span><span class="sxs-lookup"><span data-stu-id="c991d-120">EXAMPLES</span></span>

### <span data-ttu-id="c991d-121">예제 1: 웹 앱에 인증서 바인딩</span><span class="sxs-lookup"><span data-stu-id="c991d-121">Example 1: Bind a certificate to a Web App</span></span>
```powershell
PS C:\>New-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3" -Name "www.contoso.com"
```

<span data-ttu-id="c991d-122">이 명령은 기존 Azure 인증서 (지문이 E3A38EBA60CAA1C162785A2E1C44A15AD450199C3 인 인증서)를 ContosoWebApp 이라는 웹 앱에 바인딩합니다.</span><span class="sxs-lookup"><span data-stu-id="c991d-122">This command binds an existing Azure certificate (a certificate with the Thumbprint E3A38EBA60CAA1C162785A2E1C44A15AD450199C3) to the web app named ContosoWebApp.</span></span>

### <span data-ttu-id="c991d-123">예제 2</span><span class="sxs-lookup"><span data-stu-id="c991d-123">Example 2</span></span>

<span data-ttu-id="c991d-124">Azure Web App에 대 한 SSL 인증서 바인딩을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c991d-124">Creates an SSL certificate binding for an Azure Web App.</span></span> <span data-ttu-id="c991d-125">생성</span><span class="sxs-lookup"><span data-stu-id="c991d-125">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzWebAppSSLBinding -Name 'www.contoso.com' -ResourceGroupName 'ContosoResourceGroup' -SslState Disabled -Thumbprint 'E3A38EBA60CAA1C162785A2E1C44A15AD450199C3' -WebAppName 'ContosoWebApp'
```

## <span data-ttu-id="c991d-126">변수</span><span class="sxs-lookup"><span data-stu-id="c991d-126">PARAMETERS</span></span>

### <span data-ttu-id="c991d-127">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="c991d-127">-CertificateFilePath</span></span>
<span data-ttu-id="c991d-128">업로드할 인증서의 파일 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c991d-128">Specifies the file path for the certificate to be uploaded.</span></span>
<span data-ttu-id="c991d-129">*Certificatefilepath* 매개 변수는 인증서가 아직 Azure에 업로드 되지 않은 경우에만 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="c991d-129">The *CertificateFilePath* parameter is only required if the certificate has not yet been uploaded to Azure.</span></span>

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

### <span data-ttu-id="c991d-130">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="c991d-130">-CertificatePassword</span></span>
<span data-ttu-id="c991d-131">인증서 암호를 해독 합니다.</span><span class="sxs-lookup"><span data-stu-id="c991d-131">Specifies the decryption password for the certificate.</span></span>

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

### <span data-ttu-id="c991d-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c991d-132">-DefaultProfile</span></span>
<span data-ttu-id="c991d-133">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c991d-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c991d-134">-이름</span><span class="sxs-lookup"><span data-stu-id="c991d-134">-Name</span></span>
<span data-ttu-id="c991d-135">웹 앱의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c991d-135">Specifies the name of the Web App.</span></span>

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

### <span data-ttu-id="c991d-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c991d-136">-ResourceGroupName</span></span>
<span data-ttu-id="c991d-137">인증서가 할당 되는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c991d-137">Specifies the name of the resource group that the certificate is assigned to.</span></span>
<span data-ttu-id="c991d-138">동일한 명령에서 *ResourceGroupName* 매개 변수와 *web app* 매개 변수를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="c991d-138">You cannot use the *ResourceGroupName* parameter and the *WebApp* parameter in the same command.</span></span>

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

### <span data-ttu-id="c991d-139">-슬롯</span><span class="sxs-lookup"><span data-stu-id="c991d-139">-Slot</span></span>
<span data-ttu-id="c991d-140">웹 앱 배포 슬롯의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c991d-140">Specifies the name of the Web App deployment slot.</span></span>
<span data-ttu-id="c991d-141">Get-AzWebAppSlot cmdlet을 사용 하 여 슬롯을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c991d-141">You can use the Get-AzWebAppSlot cmdlet to get a slot.</span></span>
<span data-ttu-id="c991d-142">배포 슬롯은 인터넷을 통해 해당 앱에 액세스할 수 없는 웹 앱을 준비 하 고 유효성을 검사할 수 있는 방법을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="c991d-142">Deployment slots provide a way for you to stage and validate web apps without those apps being accessible over the Internet.</span></span>
<span data-ttu-id="c991d-143">일반적으로 변경 내용을 준비 사이트에 배포 하 고 해당 변경의 유효성을 검사 한 다음 프로덕션 (인터넷 액세스 가능) 사이트에 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="c991d-143">Typically you will deploy your changes to a staging site, validate those changes, and then deploy to the production (Internet-accessible) site.</span></span>

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

### <span data-ttu-id="c991d-144">-SslState</span><span class="sxs-lookup"><span data-stu-id="c991d-144">-SslState</span></span>
<span data-ttu-id="c991d-145">인증서를 사용할 수 있는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c991d-145">Specifies whether the certificate is enabled.</span></span>
<span data-ttu-id="c991d-146">*Sslstate* 매개 변수를 1로 설정 하 여 인증서를 활성화 하거나, *sslstate* 를 0으로 설정 하 여 인증서를 비활성화 합니다.</span><span class="sxs-lookup"><span data-stu-id="c991d-146">Set the *SSLState* parameter to 1 to enable the certificate, or set *SSLState* to 0 to disable the certificate.</span></span>

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

### <span data-ttu-id="c991d-147">-지문</span><span class="sxs-lookup"><span data-stu-id="c991d-147">-Thumbprint</span></span>
<span data-ttu-id="c991d-148">인증서에 대 한 고유 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c991d-148">Specifies the unique identifier for the certificate.</span></span>

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

### <span data-ttu-id="c991d-149">-Web app</span><span class="sxs-lookup"><span data-stu-id="c991d-149">-WebApp</span></span>
<span data-ttu-id="c991d-150">웹 앱을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c991d-150">Specifies a Web App.</span></span>
<span data-ttu-id="c991d-151">웹 앱을 가져오려면 Get-AzWebApp cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c991d-151">To get a Web App, use the Get-AzWebApp cmdlet.</span></span>
<span data-ttu-id="c991d-152">*ResourceGroupName* 매개 변수 및/또는 *webappname* 과 동일한 명령에서 *web app* 매개 변수를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="c991d-152">You cannot use the *WebApp* parameter in the same command as the *ResourceGroupName* parameter and/or the *WebAppName*.</span></span>

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

### <span data-ttu-id="c991d-153">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="c991d-153">-WebAppName</span></span>
<span data-ttu-id="c991d-154">새 SSL 바인딩이 생성 되는 웹 앱의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c991d-154">Specifies the name of the Web App for which the new SSL binding is being created.</span></span>
<span data-ttu-id="c991d-155">동일한 명령에서 *Webappname* 매개 변수와 *web app* 매개 변수를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="c991d-155">You cannot use the *WebAppName* parameter and the *WebApp* parameter in the same command.</span></span>

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

### <span data-ttu-id="c991d-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c991d-156">CommonParameters</span></span>
<span data-ttu-id="c991d-157">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c991d-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c991d-158">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c991d-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c991d-159">입력</span><span class="sxs-lookup"><span data-stu-id="c991d-159">INPUTS</span></span>

### <span data-ttu-id="c991d-160">Microsoft Azure. \*. m a i m Apps.</span><span class="sxs-lookup"><span data-stu-id="c991d-160">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="c991d-161">출력</span><span class="sxs-lookup"><span data-stu-id="c991d-161">OUTPUTS</span></span>

### <span data-ttu-id="c991d-162">Microsoft. Azure. 관리. i m m 네임 스페이스. i m m Namesslstate</span><span class="sxs-lookup"><span data-stu-id="c991d-162">Microsoft.Azure.Management.WebSites.Models.HostNameSslState</span></span>

## <span data-ttu-id="c991d-163">상속자</span><span class="sxs-lookup"><span data-stu-id="c991d-163">NOTES</span></span>

## <span data-ttu-id="c991d-164">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c991d-164">RELATED LINKS</span></span>

[<span data-ttu-id="c991d-165">Get-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="c991d-165">Get-AzWebAppSSLBinding</span></span>](./Get-AzWebAppSSLBinding.md)

[<span data-ttu-id="c991d-166">제거-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="c991d-166">Remove-AzWebAppSSLBinding</span></span>](./Remove-AzWebAppSSLBinding.md)

[<span data-ttu-id="c991d-167">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c991d-167">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="c991d-168">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="c991d-168">Get-AzWebApp</span></span>](./Get-AzWebApp.md)


