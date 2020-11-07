---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementcustomhostnameconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementCustomHostnameConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementCustomHostnameConfiguration.md
ms.openlocfilehash: 2f929fc2968935284024e1112e62b395aa0d545e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703515"
---
# <span data-ttu-id="c239b-101">New-AzureRmApiManagementCustomHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="c239b-101">New-AzureRmApiManagementCustomHostnameConfiguration</span></span>

## <span data-ttu-id="c239b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c239b-102">SYNOPSIS</span></span>
<span data-ttu-id="c239b-103">의 인스턴스를 만듭니다 `PsApiManagementCustomHostNameConfiguration` .</span><span class="sxs-lookup"><span data-stu-id="c239b-103">Creates an instance of `PsApiManagementCustomHostNameConfiguration`.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c239b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c239b-104">SYNTAX</span></span>

### <span data-ttu-id="c239b-105">NoChangeCertificate (기본값)</span><span class="sxs-lookup"><span data-stu-id="c239b-105">NoChangeCertificate (Default)</span></span>
```
New-AzureRmApiManagementCustomHostnameConfiguration -Hostname <String>
 -HostnameType <PsApiManagementHostnameType>
 -HostNameCertificateInformation <PsApiManagementCertificateInformation> [-DefaultSslBinding]
 [-NegotiateClientCertificate] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c239b-106">SslCertificateFromFile</span><span class="sxs-lookup"><span data-stu-id="c239b-106">SslCertificateFromFile</span></span>
```
New-AzureRmApiManagementCustomHostnameConfiguration -Hostname <String>
 -HostnameType <PsApiManagementHostnameType> -PfxPath <String> [-PfxPassword <SecureString>]
 [-DefaultSslBinding] [-NegotiateClientCertificate] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c239b-107">SslCertificateFromKeyVault</span><span class="sxs-lookup"><span data-stu-id="c239b-107">SslCertificateFromKeyVault</span></span>
```
New-AzureRmApiManagementCustomHostnameConfiguration -Hostname <String>
 -HostnameType <PsApiManagementHostnameType> -KeyVaultId <String> [-DefaultSslBinding]
 [-NegotiateClientCertificate] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c239b-108">설명은</span><span class="sxs-lookup"><span data-stu-id="c239b-108">DESCRIPTION</span></span>
<span data-ttu-id="c239b-109">**AzureRmApiManagementCustomHostnameConfiguration** Cmdlet은 **PsApiManagementCustomHostNameConfiguration** 의 인스턴스를 만드는 도우미 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="c239b-109">The **New-AzureRmApiManagementCustomHostnameConfiguration** cmdlet is a helper command that creates an instance of **PsApiManagementCustomHostNameConfiguration**.</span></span>
<span data-ttu-id="c239b-110">이 명령은 New-AzureRmApiManagement 및 Set-AzureRmApiManagement cmdlet에 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c239b-110">This command is used with the New-AzureRmApiManagement and Set-AzureRmApiManagement cmdlet.</span></span>

## <span data-ttu-id="c239b-111">예제의</span><span class="sxs-lookup"><span data-stu-id="c239b-111">EXAMPLES</span></span>

### <span data-ttu-id="c239b-112">예제 1: 파일의 Ssl 인증서를 사용 하 여 PsApiManagementCustomHostNameConfiguration의 인스턴스 만들기 및 초기화</span><span class="sxs-lookup"><span data-stu-id="c239b-112">Example 1: Create and initialize an instance of PsApiManagementCustomHostNameConfiguration using an Ssl Certificate from file</span></span>
```powershell
PS C:\>$portal = New-AzureRmApiManagementCustomHostnameConfiguration -Hostname "portal.contoso.com" -HostnameType Portal -PfxPath "C:\contoso\certificates\apimanagement.pfx" -PfxPassword "1111" -DefaultSslBinding
PS C:\>$customConfig = @($portal)
PS C:\>New-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -CustomHostnameConfiguration $customConfig
```

<span data-ttu-id="c239b-113">이 명령은 포털에 대 한 **PsApiManagementCustomHostNameConfiguration** 의 인스턴스를 만들고 초기화 합니다.</span><span class="sxs-lookup"><span data-stu-id="c239b-113">This command creates and initializes an instance of **PsApiManagementCustomHostNameConfiguration** for Portal.</span></span> <span data-ttu-id="c239b-114">그런 다음 사용자 지정 호스트 이름 구성을 사용 하 여 새 ApiManagement 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c239b-114">Then it creates a new ApiManagement service with custom hostname configuration.</span></span>

### <span data-ttu-id="c239b-115">예제 2: KeyVault 리소스의 비밀을 사용 하 여 PsApiManagementCustomHostNameConfiguration 인스턴스 만들기 및 초기화</span><span class="sxs-lookup"><span data-stu-id="c239b-115">Example 2: Create and initialize an instance of PsApiManagementCustomHostNameConfiguration using an Secret from KeyVault Resource</span></span>
```powershell
PS C:\>$portal = New-AzureRmApiManagementCustomHostnameConfiguration -Hostname "portal.contoso.com" -HostnameType Portal -KeyVaultId "https://apim-test-keyvault.vault.azure.net/secrets/api-portal-custom-ssl.pfx"

PS C:\>$customConfig = @($portal)
PS C:\>New-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -CustomHostnameConfiguration $customConfig -AssignIdentity
```

<span data-ttu-id="c239b-116">이 명령은 **PsApiManagementCustomHostNameConfiguration** 의 인스턴스를 만들고 초기화 합니다.</span><span class="sxs-lookup"><span data-stu-id="c239b-116">This command creates and initializes an instance of **PsApiManagementCustomHostNameConfiguration**.</span></span>

## <span data-ttu-id="c239b-117">변수</span><span class="sxs-lookup"><span data-stu-id="c239b-117">PARAMETERS</span></span>

### <span data-ttu-id="c239b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c239b-118">-DefaultProfile</span></span>
<span data-ttu-id="c239b-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c239b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c239b-120">-DefaultSslBinding</span><span class="sxs-lookup"><span data-stu-id="c239b-120">-DefaultSslBinding</span></span>
<span data-ttu-id="c239b-121">값이 비밀이 고 암호화 해야 하는지 여부를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="c239b-121">Determines whether the value is a secret and should be encrypted or not.</span></span>
<span data-ttu-id="c239b-122">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="c239b-122">This parameter is optional.</span></span>
<span data-ttu-id="c239b-123">기본값은 false입니다.</span><span class="sxs-lookup"><span data-stu-id="c239b-123">Default Value is false.</span></span>

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

### <span data-ttu-id="c239b-124">-Hostname</span><span class="sxs-lookup"><span data-stu-id="c239b-124">-Hostname</span></span>
<span data-ttu-id="c239b-125">사용자 지정 호스트 이름</span><span class="sxs-lookup"><span data-stu-id="c239b-125">Custom Hostname</span></span>

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

### <span data-ttu-id="c239b-126">-HostNameCertificateInformation</span><span class="sxs-lookup"><span data-stu-id="c239b-126">-HostNameCertificateInformation</span></span>
<span data-ttu-id="c239b-127">기존 인증서 구성.</span><span class="sxs-lookup"><span data-stu-id="c239b-127">Existing Certificate Configuration.</span></span>

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

### <span data-ttu-id="c239b-128">-HostnameType</span><span class="sxs-lookup"><span data-stu-id="c239b-128">-HostnameType</span></span>
<span data-ttu-id="c239b-129">호스트 이름 유형</span><span class="sxs-lookup"><span data-stu-id="c239b-129">Hostname Type</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementHostnameType
Parameter Sets: (All)
Aliases:
Accepted values: Proxy, Portal, Management, Scm

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c239b-130">-KeyVaultId</span><span class="sxs-lookup"><span data-stu-id="c239b-130">-KeyVaultId</span></span>
<span data-ttu-id="c239b-131">사용자 지정 SSL 인증서를 저장 하는 비밀으로 KeyVaultId.</span><span class="sxs-lookup"><span data-stu-id="c239b-131">KeyVaultId to the secret storing the Custom SSL Certificate.</span></span>

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

### <span data-ttu-id="c239b-132">-NegotiateClientCertificate</span><span class="sxs-lookup"><span data-stu-id="c239b-132">-NegotiateClientCertificate</span></span>
<span data-ttu-id="c239b-133">값이 비밀이 고 암호화 해야 하는지 여부를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="c239b-133">Determines whether the value is a secret and should be encrypted or not.</span></span>
<span data-ttu-id="c239b-134">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="c239b-134">This parameter is optional.</span></span>
<span data-ttu-id="c239b-135">기본값은 false입니다.</span><span class="sxs-lookup"><span data-stu-id="c239b-135">Default Value is false.</span></span>

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

### <span data-ttu-id="c239b-136">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="c239b-136">-PfxPassword</span></span>
<span data-ttu-id="c239b-137">.Pfx 인증서 파일의 암호입니다.</span><span class="sxs-lookup"><span data-stu-id="c239b-137">Password for the .pfx certificate file.</span></span>

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

### <span data-ttu-id="c239b-138">-PfxPath</span><span class="sxs-lookup"><span data-stu-id="c239b-138">-PfxPath</span></span>
<span data-ttu-id="c239b-139">.Pfx 인증서 파일의 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="c239b-139">Path to a .pfx certificate file.</span></span>

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

### <span data-ttu-id="c239b-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c239b-140">CommonParameters</span></span>
<span data-ttu-id="c239b-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c239b-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c239b-142">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c239b-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c239b-143">입력</span><span class="sxs-lookup"><span data-stu-id="c239b-143">INPUTS</span></span>

### <span data-ttu-id="c239b-144">ApiManagement. PsApiManagementCertificateInformation/.</span><span class="sxs-lookup"><span data-stu-id="c239b-144">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCertificateInformation</span></span>

## <span data-ttu-id="c239b-145">출력</span><span class="sxs-lookup"><span data-stu-id="c239b-145">OUTPUTS</span></span>

### <span data-ttu-id="c239b-146">ApiManagement. PsApiManagementCustomHostNameConfiguration/.</span><span class="sxs-lookup"><span data-stu-id="c239b-146">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCustomHostNameConfiguration</span></span>

## <span data-ttu-id="c239b-147">상속자</span><span class="sxs-lookup"><span data-stu-id="c239b-147">NOTES</span></span>

## <span data-ttu-id="c239b-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c239b-148">RELATED LINKS</span></span>

[<span data-ttu-id="c239b-149">새로운 AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="c239b-149">New-AzureRmApiManagement</span></span>](./New-AzureRmApiManagement.md)

[<span data-ttu-id="c239b-150">Set-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="c239b-150">Set-AzureRmApiManagement</span></span>](./Set-AzureRmApiManagement.md)
