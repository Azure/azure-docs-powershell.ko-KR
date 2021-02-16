---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementcustomhostnameconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementCustomHostnameConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementCustomHostnameConfiguration.md
ms.openlocfilehash: a5c619a88f9366699f37124eab5afb2302717762
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176500"
---
# <span data-ttu-id="da3cb-101">New-AzApiManagementCustomHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="da3cb-101">New-AzApiManagementCustomHostnameConfiguration</span></span>

## <span data-ttu-id="da3cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da3cb-102">SYNOPSIS</span></span>
<span data-ttu-id="da3cb-103">.의 `PsApiManagementCustomHostNameConfiguration` 인스턴스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="da3cb-103">Creates an instance of `PsApiManagementCustomHostNameConfiguration`.</span></span>

## <span data-ttu-id="da3cb-104">구문</span><span class="sxs-lookup"><span data-stu-id="da3cb-104">SYNTAX</span></span>

### <span data-ttu-id="da3cb-105">NoChangeCertificate(기본값)</span><span class="sxs-lookup"><span data-stu-id="da3cb-105">NoChangeCertificate (Default)</span></span>
```
New-AzApiManagementCustomHostnameConfiguration -Hostname <String> -HostnameType <PsApiManagementHostnameType>
 -HostNameCertificateInformation <PsApiManagementCertificateInformation> [-DefaultSslBinding]
 [-NegotiateClientCertificate] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da3cb-106">SslCertificateFromFile</span><span class="sxs-lookup"><span data-stu-id="da3cb-106">SslCertificateFromFile</span></span>
```
New-AzApiManagementCustomHostnameConfiguration -Hostname <String> -HostnameType <PsApiManagementHostnameType>
 -PfxPath <String> [-PfxPassword <SecureString>] [-DefaultSslBinding] [-NegotiateClientCertificate]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da3cb-107">SslCertificateFromKeyVault</span><span class="sxs-lookup"><span data-stu-id="da3cb-107">SslCertificateFromKeyVault</span></span>
```
New-AzApiManagementCustomHostnameConfiguration -Hostname <String> -HostnameType <PsApiManagementHostnameType>
 -KeyVaultId <String> [-DefaultSslBinding] [-NegotiateClientCertificate]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="da3cb-108">설명</span><span class="sxs-lookup"><span data-stu-id="da3cb-108">DESCRIPTION</span></span>
<span data-ttu-id="da3cb-109">**New-AzApiManagementCustomHostnameConfiguration** cmdlet은 **PsApiManagementCustomHostNameConfiguration의** 인스턴스를 만드는 도우미 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="da3cb-109">The **New-AzApiManagementCustomHostnameConfiguration** cmdlet is a helper command that creates an instance of **PsApiManagementCustomHostNameConfiguration**.</span></span>
<span data-ttu-id="da3cb-110">이 명령은 New-AzApiManagement cmdlet과 Set-AzApiManagement 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="da3cb-110">This command is used with the New-AzApiManagement and Set-AzApiManagement cmdlet.</span></span>

## <span data-ttu-id="da3cb-111">예제</span><span class="sxs-lookup"><span data-stu-id="da3cb-111">EXAMPLES</span></span>

### <span data-ttu-id="da3cb-112">예제 1: 파일에서 Ssl 인증서를 사용하여 PsApiManagementCustomHostNameConfiguration 인스턴스 만들기 및 초기화</span><span class="sxs-lookup"><span data-stu-id="da3cb-112">Example 1: Create and initialize an instance of PsApiManagementCustomHostNameConfiguration using an Ssl Certificate from file</span></span>
```powershell
PS C:\>$portal = New-AzApiManagementCustomHostnameConfiguration -Hostname "portal.contoso.com" -HostnameType Portal -PfxPath "C:\contoso\certificates\apimanagement.pfx" -PfxPassword "1111" -DefaultSslBinding
PS C:\>$customConfig = @($portal)
PS C:\>New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -CustomHostnameConfiguration $customConfig
```

<span data-ttu-id="da3cb-113">이 명령은 **포털용 PsApiManagementCustomHostNameConfiguration의** 인스턴스를 만들고 초기화합니다.</span><span class="sxs-lookup"><span data-stu-id="da3cb-113">This command creates and initializes an instance of **PsApiManagementCustomHostNameConfiguration** for Portal.</span></span> <span data-ttu-id="da3cb-114">그런 다음 사용자 지정 호스트 이름 구성을 사용하여 새 ApiManagement 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="da3cb-114">Then it creates a new ApiManagement service with custom hostname configuration.</span></span>

### <span data-ttu-id="da3cb-115">예제 2: KeyVault 리소스의 비밀을 사용하여 PsApiManagementCustomHostNameConfiguration 인스턴스 만들기 및 초기화</span><span class="sxs-lookup"><span data-stu-id="da3cb-115">Example 2: Create and initialize an instance of PsApiManagementCustomHostNameConfiguration using an Secret from KeyVault Resource</span></span>
```powershell
PS C:\>$portal = New-AzApiManagementCustomHostnameConfiguration -Hostname "portal.contoso.com" -HostnameType Portal -KeyVaultId "https://apim-test-keyvault.vault.azure.net/secrets/api-portal-custom-ssl.pfx"

PS C:\>$customConfig = @($portal)
PS C:\>New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -CustomHostnameConfiguration $customConfig -SystemAssignedIdentity
```

<span data-ttu-id="da3cb-116">이 명령은 **PsApiManagementCustomHostNameConfiguration의** 인스턴스를 만들고 초기화합니다.</span><span class="sxs-lookup"><span data-stu-id="da3cb-116">This command creates and initializes an instance of **PsApiManagementCustomHostNameConfiguration**.</span></span>

## <span data-ttu-id="da3cb-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="da3cb-117">PARAMETERS</span></span>

### <span data-ttu-id="da3cb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da3cb-118">-DefaultProfile</span></span>
<span data-ttu-id="da3cb-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="da3cb-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da3cb-120">-DefaultSslBinding</span><span class="sxs-lookup"><span data-stu-id="da3cb-120">-DefaultSslBinding</span></span>
<span data-ttu-id="da3cb-121">값이 비밀인지, 암호화해야 하는지 여부를 판단합니다.</span><span class="sxs-lookup"><span data-stu-id="da3cb-121">Determines whether the value is a secret and should be encrypted or not.</span></span>
<span data-ttu-id="da3cb-122">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="da3cb-122">This parameter is optional.</span></span>
<span data-ttu-id="da3cb-123">기본값은 false입니다.</span><span class="sxs-lookup"><span data-stu-id="da3cb-123">Default Value is false.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da3cb-124">-Hostname</span><span class="sxs-lookup"><span data-stu-id="da3cb-124">-Hostname</span></span>
<span data-ttu-id="da3cb-125">사용자 지정 호스트 이름</span><span class="sxs-lookup"><span data-stu-id="da3cb-125">Custom Hostname</span></span>

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

### <span data-ttu-id="da3cb-126">-HostNameCertificateInformation</span><span class="sxs-lookup"><span data-stu-id="da3cb-126">-HostNameCertificateInformation</span></span>
<span data-ttu-id="da3cb-127">기존 인증서 구성.</span><span class="sxs-lookup"><span data-stu-id="da3cb-127">Existing Certificate Configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCertificateInformation
Parameter Sets: NoChangeCertificate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da3cb-128">-HostnameType</span><span class="sxs-lookup"><span data-stu-id="da3cb-128">-HostnameType</span></span>
<span data-ttu-id="da3cb-129">호스트 이름 형식</span><span class="sxs-lookup"><span data-stu-id="da3cb-129">Hostname Type</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementHostnameType
Parameter Sets: (All)
Aliases:
Accepted values: Proxy, Portal, Management, Scm, DeveloperPortal

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da3cb-130">-KeyVaultId</span><span class="sxs-lookup"><span data-stu-id="da3cb-130">-KeyVaultId</span></span>
<span data-ttu-id="da3cb-131">사용자 지정 SSL 인증서를 저장하는 비밀에 대한 KeyVaultId입니다.</span><span class="sxs-lookup"><span data-stu-id="da3cb-131">KeyVaultId to the secret storing the Custom SSL Certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: SslCertificateFromKeyVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da3cb-132">-NegotiateClientCertificate</span><span class="sxs-lookup"><span data-stu-id="da3cb-132">-NegotiateClientCertificate</span></span>
<span data-ttu-id="da3cb-133">값이 비밀인지, 암호화해야 하는지 여부를 판단합니다.</span><span class="sxs-lookup"><span data-stu-id="da3cb-133">Determines whether the value is a secret and should be encrypted or not.</span></span>
<span data-ttu-id="da3cb-134">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="da3cb-134">This parameter is optional.</span></span>
<span data-ttu-id="da3cb-135">기본값은 false입니다.</span><span class="sxs-lookup"><span data-stu-id="da3cb-135">Default Value is false.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da3cb-136">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="da3cb-136">-PfxPassword</span></span>
<span data-ttu-id="da3cb-137">.pfx 인증서 파일의 암호입니다.</span><span class="sxs-lookup"><span data-stu-id="da3cb-137">Password for the .pfx certificate file.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: SslCertificateFromFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da3cb-138">-PfxPath</span><span class="sxs-lookup"><span data-stu-id="da3cb-138">-PfxPath</span></span>
<span data-ttu-id="da3cb-139">.pfx 인증서 파일의 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="da3cb-139">Path to a .pfx certificate file.</span></span>

```yaml
Type: System.String
Parameter Sets: SslCertificateFromFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da3cb-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da3cb-140">CommonParameters</span></span>
<span data-ttu-id="da3cb-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="da3cb-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da3cb-142">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="da3cb-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da3cb-143">입력</span><span class="sxs-lookup"><span data-stu-id="da3cb-143">INPUTS</span></span>

### <span data-ttu-id="da3cb-144">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCertificateInformation</span><span class="sxs-lookup"><span data-stu-id="da3cb-144">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCertificateInformation</span></span>

## <span data-ttu-id="da3cb-145">출력</span><span class="sxs-lookup"><span data-stu-id="da3cb-145">OUTPUTS</span></span>

### <span data-ttu-id="da3cb-146">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCustomHostNameConfiguration</span><span class="sxs-lookup"><span data-stu-id="da3cb-146">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCustomHostNameConfiguration</span></span>

## <span data-ttu-id="da3cb-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="da3cb-147">NOTES</span></span>

## <span data-ttu-id="da3cb-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="da3cb-148">RELATED LINKS</span></span>

[<span data-ttu-id="da3cb-149">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="da3cb-149">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="da3cb-150">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="da3cb-150">Set-AzApiManagement</span></span>](./Set-AzApiManagement.md)