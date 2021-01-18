---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: D4188DC6-A8AB-4B45-9781-94B74C338C63
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/import-azkeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Import-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Import-AzKeyVaultCertificate.md
ms.openlocfilehash: 6a687f67741a8d4925e3253c9f787532501ad186
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495327"
---
# <span data-ttu-id="317e2-101">Import-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="317e2-101">Import-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="317e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="317e2-102">SYNOPSIS</span></span>
<span data-ttu-id="317e2-103">인증서를 키 자격 증명 모음으로 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="317e2-103">Imports a certificate to a key vault.</span></span>

## <span data-ttu-id="317e2-104">구문</span><span class="sxs-lookup"><span data-stu-id="317e2-104">SYNTAX</span></span>

### <span data-ttu-id="317e2-105">ImportCertificateFromFile(기본값)</span><span class="sxs-lookup"><span data-stu-id="317e2-105">ImportCertificateFromFile (Default)</span></span>
```
Import-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> -FilePath <String>
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="317e2-106">ImportWithPrivateKeyFromString</span><span class="sxs-lookup"><span data-stu-id="317e2-106">ImportWithPrivateKeyFromString</span></span>
```
Import-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> -CertificateString <String>
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="317e2-107">ImportWithPrivateKeyFromCollection</span><span class="sxs-lookup"><span data-stu-id="317e2-107">ImportWithPrivateKeyFromCollection</span></span>
```
Import-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String>
 [-CertificateCollection] <X509Certificate2Collection> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="317e2-108">설명</span><span class="sxs-lookup"><span data-stu-id="317e2-108">DESCRIPTION</span></span>
<span data-ttu-id="317e2-109">**Import-AzKeyVaultCertificate** cmdlet은 인증서를 키 자격 증명 모음으로 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="317e2-109">The **Import-AzKeyVaultCertificate** cmdlet imports a certificate into a key vault.</span></span>
<span data-ttu-id="317e2-110">다음 방법 중 하나를 사용하여 가져올 인증서를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="317e2-110">You can create the certificate to import by using one of the following methods:</span></span>
- <span data-ttu-id="317e2-111">인증서 서명 요청을 만들고 인증 기관에 `Add-AzKeyVaultCertificate` 제출하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="317e2-111">Use `Add-AzKeyVaultCertificate` to create a certificate signing request and submit it to a certificate authority.</span></span> <span data-ttu-id="317e2-112">참조 https://docs.microsoft.com/en-us/azure/key-vault/certificates/create-certificate-signing-request</span><span class="sxs-lookup"><span data-stu-id="317e2-112">See https://docs.microsoft.com/en-us/azure/key-vault/certificates/create-certificate-signing-request</span></span>
- <span data-ttu-id="317e2-113">인증서와 개인 키를 모두 포함하는 .pfx 또는 .p12 파일과 같은 기존 인증서 패키지 파일을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="317e2-113">Use an existing certificate package file, such as a .pfx or .p12 file, which contains both the certificate and private key.</span></span>

## <span data-ttu-id="317e2-114">예제</span><span class="sxs-lookup"><span data-stu-id="317e2-114">EXAMPLES</span></span>

### <span data-ttu-id="317e2-115">예제 1: 키 자격 증명 모음 인증서 가져오기</span><span class="sxs-lookup"><span data-stu-id="317e2-115">Example 1: Import a key vault certificate</span></span>
```powershell
PS C:\> $Password = ConvertTo-SecureString -String "123" -AsPlainText -Force
PS C:\> Import-AzKeyVaultCertificate -VaultName "ContosoKV01" -Name "ImportCert01" -FilePath "C:\Users\contosoUser\Desktop\import.pfx" -Password $Password

Name        : importCert01
Certificate : [Subject]
                CN=contoso.com

              [Issuer]
                CN=contoso.com

              [Serial Number]
                XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

              [Not Before]
                2/8/2016 3:11:45 PM

              [Not After]
                8/8/2016 4:21:45 PM

              [Thumbprint]
                XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

Thumbprint  : XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
Tags        :
Enabled     : True
Created     : 2/8/2016 11:50:43 PM
Updated     : 2/8/2016 11:50:43 PM
```

<span data-ttu-id="317e2-116">첫 번째 명령은 ConvertTo-SecureString cmdlet을 사용하여 보안 암호를 만든 다음 $Password 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="317e2-116">The first command uses the ConvertTo-SecureString cmdlet to create a secure password, and then stores it in the $Password variable.</span></span>
<span data-ttu-id="317e2-117">두 번째 명령은 ImportCert01이라는 인증서를 CosotosoKV01 키 자격 증명 모음으로 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="317e2-117">The second command imports the certificate named ImportCert01 into the CosotosoKV01 key vault.</span></span>

## <span data-ttu-id="317e2-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="317e2-118">PARAMETERS</span></span>

### <span data-ttu-id="317e2-119">-CertificateCollection</span><span class="sxs-lookup"><span data-stu-id="317e2-119">-CertificateCollection</span></span>
<span data-ttu-id="317e2-120">키 자격 증명 모음에 추가할 인증서 컬렉션을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="317e2-120">Specifies the certificate collection to add to a key vault.</span></span>

```yaml
Type: System.Security.Cryptography.X509Certificates.X509Certificate2Collection
Parameter Sets: ImportWithPrivateKeyFromCollection
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="317e2-121">-CertificateString</span><span class="sxs-lookup"><span data-stu-id="317e2-121">-CertificateString</span></span>
<span data-ttu-id="317e2-122">인증서 문자열을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="317e2-122">Specifies a certificate string.</span></span>

```yaml
Type: System.String
Parameter Sets: ImportWithPrivateKeyFromString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="317e2-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="317e2-123">-DefaultProfile</span></span>
<span data-ttu-id="317e2-124">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="317e2-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="317e2-125">-FilePath</span><span class="sxs-lookup"><span data-stu-id="317e2-125">-FilePath</span></span>
<span data-ttu-id="317e2-126">이 cmdlet에서 가져오는 인증서 파일의 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="317e2-126">Specifies the path of the certificate file that this cmdlet imports.</span></span>

```yaml
Type: System.String
Parameter Sets: ImportCertificateFromFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="317e2-127">-Name</span><span class="sxs-lookup"><span data-stu-id="317e2-127">-Name</span></span>
<span data-ttu-id="317e2-128">인증서 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="317e2-128">Specifies the certificate name.</span></span> <span data-ttu-id="317e2-129">이 cmdlet은 키 자격 증명 모음 이름, 현재 선택한 환경 및 인증서 이름에서 인증서의 FQDN(정식 도메인 이름)을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="317e2-129">This cmdlet constructs the fully qualified domain name (FQDN) of a certificate from key vault name, currently selected environment, and certificate name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="317e2-130">-Password</span><span class="sxs-lookup"><span data-stu-id="317e2-130">-Password</span></span>
<span data-ttu-id="317e2-131">인증서 파일의 암호를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="317e2-131">Specifies the password for a certificate file.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ImportCertificateFromFile, ImportWithPrivateKeyFromString
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="317e2-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="317e2-132">-Tag</span></span>
<span data-ttu-id="317e2-133">해시 테이블 형식의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="317e2-133">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="317e2-134">예: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="317e2-134">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="317e2-135">-VaultName</span><span class="sxs-lookup"><span data-stu-id="317e2-135">-VaultName</span></span>
<span data-ttu-id="317e2-136">이 cmdlet이 인증서를 가져올 키 자격 증명 모음 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="317e2-136">Specifies the key vault name into which this cmdlet imports certificates.</span></span>
<span data-ttu-id="317e2-137">이 cmdlet은 이름 및 현재 선택한 환경에 따라 키 자격 증명 모음의 FQDN(정식 도메인 이름)을 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="317e2-137">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="317e2-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="317e2-138">-Confirm</span></span>
<span data-ttu-id="317e2-139">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="317e2-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="317e2-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="317e2-140">-WhatIf</span></span>
<span data-ttu-id="317e2-141">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="317e2-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="317e2-142">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="317e2-142">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="317e2-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="317e2-143">CommonParameters</span></span>
<span data-ttu-id="317e2-144">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="317e2-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="317e2-145">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="317e2-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="317e2-146">입력</span><span class="sxs-lookup"><span data-stu-id="317e2-146">INPUTS</span></span>

### <span data-ttu-id="317e2-147">System.String</span><span class="sxs-lookup"><span data-stu-id="317e2-147">System.String</span></span>

### <span data-ttu-id="317e2-148">System.Security.Cryptography.X509Certificates.X509Certificate2Collection</span><span class="sxs-lookup"><span data-stu-id="317e2-148">System.Security.Cryptography.X509Certificates.X509Certificate2Collection</span></span>

### <span data-ttu-id="317e2-149">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="317e2-149">System.Collections.Hashtable</span></span>

## <span data-ttu-id="317e2-150">출력</span><span class="sxs-lookup"><span data-stu-id="317e2-150">OUTPUTS</span></span>

### <span data-ttu-id="317e2-151">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="317e2-151">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

## <span data-ttu-id="317e2-152">참고 사항</span><span class="sxs-lookup"><span data-stu-id="317e2-152">NOTES</span></span>

## <span data-ttu-id="317e2-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="317e2-153">RELATED LINKS</span></span>

[<span data-ttu-id="317e2-154">Remove-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="317e2-154">Remove-AzKeyVaultCertificate</span></span>](./Remove-AzKeyVaultCertificate.md)

[<span data-ttu-id="317e2-155">Key Vault에서 CSR 만들기 및 Merging</span><span class="sxs-lookup"><span data-stu-id="317e2-155">Creating and merging CSR in Key Vault</span></span>](https://docs.microsoft.com/en-us/azure/key-vault/certificates/create-certificate-signing-request)