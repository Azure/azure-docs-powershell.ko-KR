---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: D4188DC6-A8AB-4B45-9781-94B74C338C63
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/import-azkeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Import-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Import-AzKeyVaultCertificate.md
ms.openlocfilehash: 6a687f67741a8d4925e3253c9f787532501ad186
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056312"
---
# <span data-ttu-id="8c86d-101">Import-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="8c86d-101">Import-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="8c86d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c86d-102">SYNOPSIS</span></span>
<span data-ttu-id="8c86d-103">키 자격 증명 모음으로 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8c86d-103">Imports a certificate to a key vault.</span></span>

## <span data-ttu-id="8c86d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8c86d-104">SYNTAX</span></span>

### <span data-ttu-id="8c86d-105">Importcertificatefile (기본값)</span><span class="sxs-lookup"><span data-stu-id="8c86d-105">ImportCertificateFromFile (Default)</span></span>
```
Import-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> -FilePath <String>
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8c86d-106">ImportWithPrivateKeyFromString</span><span class="sxs-lookup"><span data-stu-id="8c86d-106">ImportWithPrivateKeyFromString</span></span>
```
Import-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> -CertificateString <String>
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8c86d-107">ImportWithPrivateKeyFromCollection</span><span class="sxs-lookup"><span data-stu-id="8c86d-107">ImportWithPrivateKeyFromCollection</span></span>
```
Import-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String>
 [-CertificateCollection] <X509Certificate2Collection> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c86d-108">설명은</span><span class="sxs-lookup"><span data-stu-id="8c86d-108">DESCRIPTION</span></span>
<span data-ttu-id="8c86d-109">**AzKeyVaultCertificate** cmdlet은 인증서를 키 보관소로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8c86d-109">The **Import-AzKeyVaultCertificate** cmdlet imports a certificate into a key vault.</span></span>
<span data-ttu-id="8c86d-110">다음 방법 중 하나를 사용 하 여 가져올 인증서를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8c86d-110">You can create the certificate to import by using one of the following methods:</span></span>
- <span data-ttu-id="8c86d-111">`Add-AzKeyVaultCertificate`인증서 서명 요청을 만들어 인증 기관에 제출 하는 데 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c86d-111">Use `Add-AzKeyVaultCertificate` to create a certificate signing request and submit it to a certificate authority.</span></span> <span data-ttu-id="8c86d-112">보기 https://docs.microsoft.com/en-us/azure/key-vault/certificates/create-certificate-signing-request</span><span class="sxs-lookup"><span data-stu-id="8c86d-112">See https://docs.microsoft.com/en-us/azure/key-vault/certificates/create-certificate-signing-request</span></span>
- <span data-ttu-id="8c86d-113">.Pfx 또는. p12 파일과 같이 인증서와 개인 키를 모두 포함 하는 기존 인증서 패키지 파일을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c86d-113">Use an existing certificate package file, such as a .pfx or .p12 file, which contains both the certificate and private key.</span></span>

## <span data-ttu-id="8c86d-114">예제의</span><span class="sxs-lookup"><span data-stu-id="8c86d-114">EXAMPLES</span></span>

### <span data-ttu-id="8c86d-115">예제 1: 키 보관소 인증서 가져오기</span><span class="sxs-lookup"><span data-stu-id="8c86d-115">Example 1: Import a key vault certificate</span></span>
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

<span data-ttu-id="8c86d-116">첫 번째 명령은 ConvertTo-SecureString cmdlet을 사용 하 여 보안 암호를 만든 다음 $Password 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c86d-116">The first command uses the ConvertTo-SecureString cmdlet to create a secure password, and then stores it in the $Password variable.</span></span>
<span data-ttu-id="8c86d-117">두 번째 명령은 ImportCert01 이라는 인증서를 CosotosoKV01 키 보관소에 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8c86d-117">The second command imports the certificate named ImportCert01 into the CosotosoKV01 key vault.</span></span>

## <span data-ttu-id="8c86d-118">변수</span><span class="sxs-lookup"><span data-stu-id="8c86d-118">PARAMETERS</span></span>

### <span data-ttu-id="8c86d-119">-CertificateCollection</span><span class="sxs-lookup"><span data-stu-id="8c86d-119">-CertificateCollection</span></span>
<span data-ttu-id="8c86d-120">키 자격 증명 모음에 추가할 인증서 컬렉션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c86d-120">Specifies the certificate collection to add to a key vault.</span></span>

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

### <span data-ttu-id="8c86d-121">-CertificateString</span><span class="sxs-lookup"><span data-stu-id="8c86d-121">-CertificateString</span></span>
<span data-ttu-id="8c86d-122">인증서 문자열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c86d-122">Specifies a certificate string.</span></span>

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

### <span data-ttu-id="8c86d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c86d-123">-DefaultProfile</span></span>
<span data-ttu-id="8c86d-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="8c86d-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8c86d-125">-FilePath</span><span class="sxs-lookup"><span data-stu-id="8c86d-125">-FilePath</span></span>
<span data-ttu-id="8c86d-126">이 cmdlet이 가져오는 인증서 파일의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c86d-126">Specifies the path of the certificate file that this cmdlet imports.</span></span>

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

### <span data-ttu-id="8c86d-127">-이름</span><span class="sxs-lookup"><span data-stu-id="8c86d-127">-Name</span></span>
<span data-ttu-id="8c86d-128">인증서 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c86d-128">Specifies the certificate name.</span></span> <span data-ttu-id="8c86d-129">이 cmdlet은 키 보관소 이름, 현재 선택한 환경, 인증서 이름에서 인증서의 FQDN (정규화 된 도메인 이름)을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c86d-129">This cmdlet constructs the fully qualified domain name (FQDN) of a certificate from key vault name, currently selected environment, and certificate name.</span></span>

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

### <span data-ttu-id="8c86d-130">-암호</span><span class="sxs-lookup"><span data-stu-id="8c86d-130">-Password</span></span>
<span data-ttu-id="8c86d-131">인증서 파일에 대 한 암호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c86d-131">Specifies the password for a certificate file.</span></span>

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

### <span data-ttu-id="8c86d-132">태그</span><span class="sxs-lookup"><span data-stu-id="8c86d-132">-Tag</span></span>
<span data-ttu-id="8c86d-133">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="8c86d-133">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="8c86d-134">예: @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="8c86d-134">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="8c86d-135">-VaultName</span><span class="sxs-lookup"><span data-stu-id="8c86d-135">-VaultName</span></span>
<span data-ttu-id="8c86d-136">이 cmdlet이 인증서를 가져오는 키 보관소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c86d-136">Specifies the key vault name into which this cmdlet imports certificates.</span></span>
<span data-ttu-id="8c86d-137">이 cmdlet은 이름 및 현재 선택 된 환경에 따라 키 보관소의 FQDN (정규화 된 도메인 이름)을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c86d-137">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="8c86d-138">-확인</span><span class="sxs-lookup"><span data-stu-id="8c86d-138">-Confirm</span></span>
<span data-ttu-id="8c86d-139">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c86d-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c86d-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c86d-140">-WhatIf</span></span>
<span data-ttu-id="8c86d-141">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8c86d-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c86d-142">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8c86d-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c86d-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c86d-143">CommonParameters</span></span>
<span data-ttu-id="8c86d-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c86d-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c86d-145">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8c86d-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c86d-146">입력</span><span class="sxs-lookup"><span data-stu-id="8c86d-146">INPUTS</span></span>

### <span data-ttu-id="8c86d-147">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8c86d-147">System.String</span></span>

### <span data-ttu-id="8c86d-148">X509Certificates. X509Certificate2Collection</span><span class="sxs-lookup"><span data-stu-id="8c86d-148">System.Security.Cryptography.X509Certificates.X509Certificate2Collection</span></span>

### <span data-ttu-id="8c86d-149">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="8c86d-149">System.Collections.Hashtable</span></span>

## <span data-ttu-id="8c86d-150">출력</span><span class="sxs-lookup"><span data-stu-id="8c86d-150">OUTPUTS</span></span>

### <span data-ttu-id="8c86d-151">Microsoft. KeyVault. PSKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="8c86d-151">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

## <span data-ttu-id="8c86d-152">상속자</span><span class="sxs-lookup"><span data-stu-id="8c86d-152">NOTES</span></span>

## <span data-ttu-id="8c86d-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8c86d-153">RELATED LINKS</span></span>

[<span data-ttu-id="8c86d-154">제거-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="8c86d-154">Remove-AzKeyVaultCertificate</span></span>](./Remove-AzKeyVaultCertificate.md)

[<span data-ttu-id="8c86d-155">키 자격 증명 모음에서 CSR 만들기 및 병합</span><span class="sxs-lookup"><span data-stu-id="8c86d-155">Creating and merging CSR in Key Vault</span></span>](https://docs.microsoft.com/en-us/azure/key-vault/certificates/create-certificate-signing-request)