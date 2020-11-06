---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: D4188DC6-A8AB-4B45-9781-94B74C338C63
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Import-AzureKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Import-AzureKeyVaultCertificate.md
ms.openlocfilehash: b97dc509ad6508c2cbec79d6ba1db27508f94c34
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527544"
---
# <span data-ttu-id="56915-101">Import-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="56915-101">Import-AzureKeyVaultCertificate</span></span>

## <span data-ttu-id="56915-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56915-102">SYNOPSIS</span></span>
<span data-ttu-id="56915-103">키 자격 증명 모음으로 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="56915-103">Imports a certificate to a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="56915-104">구문과</span><span class="sxs-lookup"><span data-stu-id="56915-104">SYNTAX</span></span>

### <span data-ttu-id="56915-105">Importcertificatefile (기본값)</span><span class="sxs-lookup"><span data-stu-id="56915-105">ImportCertificateFromFile (Default)</span></span>
```
Import-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> -FilePath <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56915-106">ImportWithPrivateKeyFromFile</span><span class="sxs-lookup"><span data-stu-id="56915-106">ImportWithPrivateKeyFromFile</span></span>
```
Import-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> -FilePath <String>
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="56915-107">ImportWithPrivateKeyFromString</span><span class="sxs-lookup"><span data-stu-id="56915-107">ImportWithPrivateKeyFromString</span></span>
```
Import-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> -CertificateString <String>
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="56915-108">ImportWithPrivateKeyFromCollection</span><span class="sxs-lookup"><span data-stu-id="56915-108">ImportWithPrivateKeyFromCollection</span></span>
```
Import-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String>
 -CertificateCollection <X509Certificate2Collection> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56915-109">설명은</span><span class="sxs-lookup"><span data-stu-id="56915-109">DESCRIPTION</span></span>
<span data-ttu-id="56915-110">**AzureKeyVaultCertificate** cmdlet은 인증서를 키 보관소로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="56915-110">The **Import-AzureKeyVaultCertificate** cmdlet imports a certificate into a key vault.</span></span>

<span data-ttu-id="56915-111">다음 방법 중 하나를 사용 하 여 가져올 인증서를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="56915-111">You can create the certificate to import by using one of the following methods:</span></span>

- <span data-ttu-id="56915-112">New-AzureKeyVaultCertificateSigningRequest cmdlet을 사용 하 여 인증서 서명 요청을 만들어 인증 기관에 제출 합니다.</span><span class="sxs-lookup"><span data-stu-id="56915-112">Use the New-AzureKeyVaultCertificateSigningRequest cmdlet to create a certificate signing request and submit it to a certificate authority.</span></span>
- <span data-ttu-id="56915-113">.Pfx 또는. p12 파일과 같이 인증서와 개인 키를 모두 포함 하는 기존 인증서 패키지 파일을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="56915-113">Use an existing certificate package file, such as a .pfx or .p12 file, which contains both the certificate and private key.</span></span>

## <span data-ttu-id="56915-114">예제의</span><span class="sxs-lookup"><span data-stu-id="56915-114">EXAMPLES</span></span>

### <span data-ttu-id="56915-115">예제 1: 키 보관소 인증서 가져오기</span><span class="sxs-lookup"><span data-stu-id="56915-115">Example 1: Import a key vault certificate</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String "123" -AsPlainText -Force
PS C:\> Import-AzureKeyVaultCertificate -VaultName "ContosoKV01" -Name "ImportCert01" -FilePath "C:\Users\contosoUser\Desktop\import.pfx" -Password $Password
Name        : importCert01
Certificate : [Subject]
                CN=contoso.com

              [Issuer]
                CN=contoso.com

              [Serial Number]
                05979C5A2F0741D5A3B6F97673E8A118

              [Not Before]
                2/8/2016 3:11:45 PM

              [Not After]
                8/8/2016 4:21:45 PM

              [Thumbprint]
                3E9B6848AD1834284157D68B060F748037F663C8

Thumbprint  : 3E9B6848AD1834284157D68B060F748037F663C8
Tags        :
Enabled     : True
Created     : 2/8/2016 11:50:43 PM
Updated     : 2/8/2016 11:50:43 PM
```

<span data-ttu-id="56915-116">첫 번째 명령은 ConvertTo-SecureString cmdlet을 사용 하 여 보안 암호를 만든 다음 $Password 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="56915-116">The first command uses the ConvertTo-SecureString cmdlet to create a secure password, and then stores it in the $Password variable.</span></span>

<span data-ttu-id="56915-117">두 번째 명령은 ImportCert01 이라는 인증서를 CosotosoKV01 키 보관소에 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="56915-117">The second command imports the certificate named ImportCert01 into the CosotosoKV01 key vault.</span></span>

## <span data-ttu-id="56915-118">변수</span><span class="sxs-lookup"><span data-stu-id="56915-118">PARAMETERS</span></span>

### <span data-ttu-id="56915-119">-CertificateCollection</span><span class="sxs-lookup"><span data-stu-id="56915-119">-CertificateCollection</span></span>
<span data-ttu-id="56915-120">키 자격 증명 모음에 추가할 인증서 컬렉션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56915-120">Specifies the certificate collection to add to a key vault.</span></span>

```yaml
Type: System.Security.Cryptography.X509Certificates.X509Certificate2Collection
Parameter Sets: ImportWithPrivateKeyFromCollection
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56915-121">-CertificateString</span><span class="sxs-lookup"><span data-stu-id="56915-121">-CertificateString</span></span>
<span data-ttu-id="56915-122">인증서 문자열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56915-122">Specifies a certificate string.</span></span>

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

### <span data-ttu-id="56915-123">-확인</span><span class="sxs-lookup"><span data-stu-id="56915-123">-Confirm</span></span>
<span data-ttu-id="56915-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="56915-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56915-125">-FilePath</span><span class="sxs-lookup"><span data-stu-id="56915-125">-FilePath</span></span>
<span data-ttu-id="56915-126">이 cmdlet이 가져오는 인증서 파일의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56915-126">Specifies the path of the certificate file that this cmdlet imports.</span></span>

```yaml
Type: System.String
Parameter Sets: ImportCertificateFromFile, ImportWithPrivateKeyFromFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56915-127">-이름</span><span class="sxs-lookup"><span data-stu-id="56915-127">-Name</span></span>
<span data-ttu-id="56915-128">인증서 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56915-128">Specifies the certificate name.</span></span> <span data-ttu-id="56915-129">이 cmdlet은 키 보관소 이름, 현재 선택한 환경, 인증서 이름에서 인증서의 FQDN (정규화 된 도메인 이름)을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="56915-129">This cmdlet constructs the fully qualified domain name (FQDN) of a certificate from key vault name, currently selected environment, and certificate name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56915-130">-암호</span><span class="sxs-lookup"><span data-stu-id="56915-130">-Password</span></span>
<span data-ttu-id="56915-131">인증서 파일에 대 한 암호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56915-131">Specifies the password for a certificate file.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ImportWithPrivateKeyFromFile, ImportWithPrivateKeyFromString
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56915-132">태그</span><span class="sxs-lookup"><span data-stu-id="56915-132">-Tag</span></span>
<span data-ttu-id="56915-133">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="56915-133">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="56915-134">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="56915-134">For example:</span></span>

<span data-ttu-id="56915-135">@ {key0 = "value0", key1 = $null, key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="56915-135">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="56915-136">-VaultName</span><span class="sxs-lookup"><span data-stu-id="56915-136">-VaultName</span></span>
<span data-ttu-id="56915-137">이 cmdlet이 인증서를 가져오는 키 보관소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56915-137">Specifies the key vault name into which this cmdlet imports certificates.</span></span>
<span data-ttu-id="56915-138">이 cmdlet은 이름 및 현재 선택 된 환경에 따라 키 보관소의 FQDN (정규화 된 도메인 이름)을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="56915-138">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56915-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56915-139">-WhatIf</span></span>
<span data-ttu-id="56915-140">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="56915-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56915-141">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="56915-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56915-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56915-142">-DefaultProfile</span></span>
<span data-ttu-id="56915-143">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="56915-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="56915-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56915-144">CommonParameters</span></span>
<span data-ttu-id="56915-145">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="56915-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56915-146">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56915-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56915-147">입력</span><span class="sxs-lookup"><span data-stu-id="56915-147">INPUTS</span></span>

## <span data-ttu-id="56915-148">출력</span><span class="sxs-lookup"><span data-stu-id="56915-148">OUTPUTS</span></span>

### <span data-ttu-id="56915-149">Microsoft. KeyVault.-모델-CertificateBundle</span><span class="sxs-lookup"><span data-stu-id="56915-149">Microsoft.Azure.Commands.KeyVault.Models.CertificateBundle</span></span>

## <span data-ttu-id="56915-150">상속자</span><span class="sxs-lookup"><span data-stu-id="56915-150">NOTES</span></span>

## <span data-ttu-id="56915-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="56915-151">RELATED LINKS</span></span>

[<span data-ttu-id="56915-152">제거-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="56915-152">Remove-AzureKeyVaultCertificate</span></span>](./Remove-AzureKeyVaultCertificate.md)
