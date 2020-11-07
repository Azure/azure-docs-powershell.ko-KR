---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: D4188DC6-A8AB-4B45-9781-94B74C338C63
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/import-azurekeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Import-AzureKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Import-AzureKeyVaultCertificate.md
ms.openlocfilehash: 37befa1434d18241b2f4721523de0ab48bebfd0a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711716"
---
# <span data-ttu-id="1e92e-101">Import-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="1e92e-101">Import-AzureKeyVaultCertificate</span></span>

## <span data-ttu-id="1e92e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e92e-102">SYNOPSIS</span></span>
<span data-ttu-id="1e92e-103">키 자격 증명 모음으로 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1e92e-103">Imports a certificate to a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1e92e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1e92e-104">SYNTAX</span></span>

### <span data-ttu-id="1e92e-105">Importcertificatefile (기본값)</span><span class="sxs-lookup"><span data-stu-id="1e92e-105">ImportCertificateFromFile (Default)</span></span>
```
Import-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> -FilePath <String>
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1e92e-106">ImportWithPrivateKeyFromString</span><span class="sxs-lookup"><span data-stu-id="1e92e-106">ImportWithPrivateKeyFromString</span></span>
```
Import-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> -CertificateString <String>
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1e92e-107">ImportWithPrivateKeyFromCollection</span><span class="sxs-lookup"><span data-stu-id="1e92e-107">ImportWithPrivateKeyFromCollection</span></span>
```
Import-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String>
 [-CertificateCollection] <X509Certificate2Collection> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e92e-108">설명은</span><span class="sxs-lookup"><span data-stu-id="1e92e-108">DESCRIPTION</span></span>
<span data-ttu-id="1e92e-109">**AzureKeyVaultCertificate** cmdlet은 인증서를 키 보관소로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1e92e-109">The **Import-AzureKeyVaultCertificate** cmdlet imports a certificate into a key vault.</span></span>

<span data-ttu-id="1e92e-110">다음 방법 중 하나를 사용 하 여 가져올 인증서를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1e92e-110">You can create the certificate to import by using one of the following methods:</span></span>

- <span data-ttu-id="1e92e-111">New-AzureKeyVaultCertificateSigningRequest cmdlet을 사용 하 여 인증서 서명 요청을 만들어 인증 기관에 제출 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e92e-111">Use the New-AzureKeyVaultCertificateSigningRequest cmdlet to create a certificate signing request and submit it to a certificate authority.</span></span>
- <span data-ttu-id="1e92e-112">.Pfx 또는. p12 파일과 같이 인증서와 개인 키를 모두 포함 하는 기존 인증서 패키지 파일을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e92e-112">Use an existing certificate package file, such as a .pfx or .p12 file, which contains both the certificate and private key.</span></span>

## <span data-ttu-id="1e92e-113">예제의</span><span class="sxs-lookup"><span data-stu-id="1e92e-113">EXAMPLES</span></span>

### <span data-ttu-id="1e92e-114">예제 1: 키 보관소 인증서 가져오기</span><span class="sxs-lookup"><span data-stu-id="1e92e-114">Example 1: Import a key vault certificate</span></span>
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

<span data-ttu-id="1e92e-115">첫 번째 명령은 ConvertTo-SecureString cmdlet을 사용 하 여 보안 암호를 만든 다음 $Password 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e92e-115">The first command uses the ConvertTo-SecureString cmdlet to create a secure password, and then stores it in the $Password variable.</span></span>

<span data-ttu-id="1e92e-116">두 번째 명령은 ImportCert01 이라는 인증서를 CosotosoKV01 키 보관소에 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1e92e-116">The second command imports the certificate named ImportCert01 into the CosotosoKV01 key vault.</span></span>

## <span data-ttu-id="1e92e-117">변수</span><span class="sxs-lookup"><span data-stu-id="1e92e-117">PARAMETERS</span></span>

### <span data-ttu-id="1e92e-118">-CertificateCollection</span><span class="sxs-lookup"><span data-stu-id="1e92e-118">-CertificateCollection</span></span>
<span data-ttu-id="1e92e-119">키 자격 증명 모음에 추가할 인증서 컬렉션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e92e-119">Specifies the certificate collection to add to a key vault.</span></span>

```yaml
Type: X509Certificate2Collection
Parameter Sets: ImportWithPrivateKeyFromCollection
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1e92e-120">-CertificateString</span><span class="sxs-lookup"><span data-stu-id="1e92e-120">-CertificateString</span></span>
<span data-ttu-id="1e92e-121">인증서 문자열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e92e-121">Specifies a certificate string.</span></span>

```yaml
Type: String
Parameter Sets: ImportWithPrivateKeyFromString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e92e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e92e-122">-DefaultProfile</span></span>
<span data-ttu-id="1e92e-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="1e92e-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e92e-124">-FilePath</span><span class="sxs-lookup"><span data-stu-id="1e92e-124">-FilePath</span></span>
<span data-ttu-id="1e92e-125">이 cmdlet이 가져오는 인증서 파일의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e92e-125">Specifies the path of the certificate file that this cmdlet imports.</span></span>

```yaml
Type: String
Parameter Sets: ImportCertificateFromFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e92e-126">-이름</span><span class="sxs-lookup"><span data-stu-id="1e92e-126">-Name</span></span>
<span data-ttu-id="1e92e-127">인증서 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e92e-127">Specifies the certificate name.</span></span> <span data-ttu-id="1e92e-128">이 cmdlet은 키 보관소 이름, 현재 선택한 환경, 인증서 이름에서 인증서의 FQDN (정규화 된 도메인 이름)을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e92e-128">This cmdlet constructs the fully qualified domain name (FQDN) of a certificate from key vault name, currently selected environment, and certificate name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e92e-129">-암호</span><span class="sxs-lookup"><span data-stu-id="1e92e-129">-Password</span></span>
<span data-ttu-id="1e92e-130">인증서 파일에 대 한 암호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e92e-130">Specifies the password for a certificate file.</span></span>

```yaml
Type: SecureString
Parameter Sets: ImportCertificateFromFile, ImportWithPrivateKeyFromString
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e92e-131">태그</span><span class="sxs-lookup"><span data-stu-id="1e92e-131">-Tag</span></span>
<span data-ttu-id="1e92e-132">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="1e92e-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="1e92e-133">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="1e92e-133">For example:</span></span>

<span data-ttu-id="1e92e-134">@ {key0 = "value0", key1 = $null, key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="1e92e-134">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e92e-135">-VaultName</span><span class="sxs-lookup"><span data-stu-id="1e92e-135">-VaultName</span></span>
<span data-ttu-id="1e92e-136">이 cmdlet이 인증서를 가져오는 키 보관소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e92e-136">Specifies the key vault name into which this cmdlet imports certificates.</span></span>
<span data-ttu-id="1e92e-137">이 cmdlet은 이름 및 현재 선택 된 환경에 따라 키 보관소의 FQDN (정규화 된 도메인 이름)을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e92e-137">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name and currently selected environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e92e-138">-확인</span><span class="sxs-lookup"><span data-stu-id="1e92e-138">-Confirm</span></span>
<span data-ttu-id="1e92e-139">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e92e-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e92e-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e92e-140">-WhatIf</span></span>
<span data-ttu-id="1e92e-141">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1e92e-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e92e-142">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1e92e-142">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e92e-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e92e-143">CommonParameters</span></span>
<span data-ttu-id="1e92e-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e92e-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e92e-145">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e92e-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e92e-146">입력</span><span class="sxs-lookup"><span data-stu-id="1e92e-146">INPUTS</span></span>

### <span data-ttu-id="1e92e-147">않아야</span><span class="sxs-lookup"><span data-stu-id="1e92e-147">None</span></span>
<span data-ttu-id="1e92e-148">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1e92e-148">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1e92e-149">출력</span><span class="sxs-lookup"><span data-stu-id="1e92e-149">OUTPUTS</span></span>

### <span data-ttu-id="1e92e-150">Microsoft. KeyVault. PSKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="1e92e-150">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

## <span data-ttu-id="1e92e-151">상속자</span><span class="sxs-lookup"><span data-stu-id="1e92e-151">NOTES</span></span>

## <span data-ttu-id="1e92e-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1e92e-152">RELATED LINKS</span></span>

[<span data-ttu-id="1e92e-153">제거-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="1e92e-153">Remove-AzureKeyVaultCertificate</span></span>](./Remove-AzureKeyVaultCertificate.md)
