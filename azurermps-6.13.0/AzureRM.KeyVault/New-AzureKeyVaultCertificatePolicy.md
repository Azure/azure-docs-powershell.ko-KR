---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 25E0F0E9-BF8C-49DF-87BA-31E2103A29A9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/new-azurekeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureKeyVaultCertificatePolicy.md
ms.openlocfilehash: a77cd700064777c769d5499cb099cfa3f9a53ec0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702477"
---
# <span data-ttu-id="9c7ee-101">New-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="9c7ee-101">New-AzureKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="9c7ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9c7ee-102">SYNOPSIS</span></span>
<span data-ttu-id="9c7ee-103">메모리 내 인증서 정책 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9c7ee-103">Creates an in-memory certificate policy object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9c7ee-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9c7ee-104">SYNTAX</span></span>

### <span data-ttu-id="9c7ee-105">SubjectName (기본값)</span><span class="sxs-lookup"><span data-stu-id="9c7ee-105">SubjectName (Default)</span></span>
```
New-AzureKeyVaultCertificatePolicy [-IssuerName] <String> [-SubjectName] <String>
 [-RenewAtNumberOfDaysBeforeExpiry <Int32>] [-RenewAtPercentageLifetime <Int32>] [-SecretContentType <String>]
 [-ReuseKeyOnRenewal] [-Disabled]
 [-KeyUsage <System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeyNotExportable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9c7ee-106">DNSNames</span><span class="sxs-lookup"><span data-stu-id="9c7ee-106">DNSNames</span></span>
```
New-AzureKeyVaultCertificatePolicy [-IssuerName] <String> [[-SubjectName] <String>]
 [-DnsName] <System.Collections.Generic.List`1[System.String]> [-RenewAtNumberOfDaysBeforeExpiry <Int32>]
 [-RenewAtPercentageLifetime <Int32>] [-SecretContentType <String>] [-ReuseKeyOnRenewal] [-Disabled]
 [-KeyUsage <System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeyNotExportable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9c7ee-107">설명은</span><span class="sxs-lookup"><span data-stu-id="9c7ee-107">DESCRIPTION</span></span>
<span data-ttu-id="9c7ee-108">**AzureKeyVaultCertificatePolicy** Cmdlet은 Azure 키 자격 증명 모음에 대 한 메모리 내 인증서 정책 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9c7ee-108">The **New-AzureKeyVaultCertificatePolicy** cmdlet creates an in-memory certificate policy object for Azure Key Vault.</span></span>

## <span data-ttu-id="9c7ee-109">예제의</span><span class="sxs-lookup"><span data-stu-id="9c7ee-109">EXAMPLES</span></span>

### <span data-ttu-id="9c7ee-110">예제 1: 인증서 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="9c7ee-110">Example 1: Create a certificate policy</span></span>
```powershell
PS C:\> New-AzureKeyVaultCertificatePolicy -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal

SecretContentType               : application/x-pkcs12
Kty                             :
KeySize                         : 2048
Exportable                      :
ReuseKeyOnRenewal               : True
SubjectName                     : CN=contoso.com
DnsNames                        :
KeyUsage                        :
Ekus                            :
ValidityInMonths                : 6
IssuerName                      : Self
CertificateType                 :
RenewAtNumberOfDaysBeforeExpiry :
RenewAtPercentageLifetime       :
EmailAtNumberOfDaysBeforeExpiry :
EmailAtPercentageLifetime       :
CertificateTransparency         :
Enabled                         : True
Created                         :
Updated                         :
```

<span data-ttu-id="9c7ee-111">이 명령은 6 개월 동안 유효한 인증서 정책을 만든 다음 키를 다시 사용할 수 있도록 하 여 인증서를 갱신 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c7ee-111">This command creates a certificate policy that is valid for six months and reuses the key to renew the certificate.</span></span>

## <span data-ttu-id="9c7ee-112">변수</span><span class="sxs-lookup"><span data-stu-id="9c7ee-112">PARAMETERS</span></span>

### <span data-ttu-id="9c7ee-113">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="9c7ee-113">-CertificateType</span></span>
<span data-ttu-id="9c7ee-114">발급자에 대 한 인증서 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c7ee-114">Specifies the type of certificate to the issuer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c7ee-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c7ee-115">-DefaultProfile</span></span>
<span data-ttu-id="9c7ee-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="9c7ee-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9c7ee-117">-사용 안 함</span><span class="sxs-lookup"><span data-stu-id="9c7ee-117">-Disabled</span></span>
<span data-ttu-id="9c7ee-118">인증서 정책을 사용할 수 없음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="9c7ee-118">Indicates that the certificate policy is disabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c7ee-119">-DnsName</span><span class="sxs-lookup"><span data-stu-id="9c7ee-119">-DnsName</span></span>
<span data-ttu-id="9c7ee-120">인증서의 DNS 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c7ee-120">Specifies the DNS names in the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: DNSNames
Aliases: DnsNames

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c7ee-121">-Eku</span><span class="sxs-lookup"><span data-stu-id="9c7ee-121">-Ekus</span></span>
<span data-ttu-id="9c7ee-122">인증서의 Eku (확장 된 키 용도)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c7ee-122">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c7ee-123">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="9c7ee-123">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="9c7ee-124">만료 되기까지 자동 알림 프로세스가 시작 되는 날짜 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c7ee-124">Specifies how many days before expiry the automatic notification process begins.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c7ee-125">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="9c7ee-125">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="9c7ee-126">알림의 자동 프로세스가 시작 되는 수명에 대 한 백분율을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c7ee-126">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c7ee-127">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="9c7ee-127">-IssuerName</span></span>
<span data-ttu-id="9c7ee-128">인증서 발급자의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c7ee-128">Specifies the name of the issuer for the certificate.</span></span>

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

### <span data-ttu-id="9c7ee-129">-KeyNotExportable 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9c7ee-129">-KeyNotExportable</span></span>
<span data-ttu-id="9c7ee-130">키를 내보낼 수 없음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="9c7ee-130">Indicates that the key is not exportable.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c7ee-131">-KeyType</span><span class="sxs-lookup"><span data-stu-id="9c7ee-131">-KeyType</span></span>
<span data-ttu-id="9c7ee-132">인증서를 지 원하는 키의 키 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c7ee-132">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="9c7ee-133">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="9c7ee-133">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9c7ee-134">RSA</span><span class="sxs-lookup"><span data-stu-id="9c7ee-134">RSA</span></span>
- <span data-ttu-id="9c7ee-135">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="9c7ee-135">RSA-HSM</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RSA, RSA-HSM

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c7ee-136">-KeyUsage</span><span class="sxs-lookup"><span data-stu-id="9c7ee-136">-KeyUsage</span></span>
<span data-ttu-id="9c7ee-137">인증서의 키 용도를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c7ee-137">Specifies the key usages in the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]
Parameter Sets: (All)
Aliases:
Accepted values: None, EncipherOnly, CrlSign, KeyCertSign, KeyAgreement, DataEncipherment, KeyEncipherment, NonRepudiation, DigitalSignature, DecipherOnly

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c7ee-138">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="9c7ee-138">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="9c7ee-139">인증서 갱신에 대 한 자동 프로세스가 시작 되는 만료 이전의 일 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c7ee-139">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c7ee-140">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="9c7ee-140">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="9c7ee-141">인증서 갱신에 대 한 자동 프로세스가 시작 되는 수명의 백분율을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c7ee-141">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c7ee-142">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="9c7ee-142">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="9c7ee-143">갱신 하는 동안 인증서가 키를 다시 사용 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="9c7ee-143">Indicates that the certificate reuse the key during renewal.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c7ee-144">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="9c7ee-144">-SecretContentType</span></span>
<span data-ttu-id="9c7ee-145">새 키 보관소 비밀의 콘텐츠 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c7ee-145">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="9c7ee-146">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="9c7ee-146">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9c7ee-147">application/x-pkcs12</span><span class="sxs-lookup"><span data-stu-id="9c7ee-147">application/x-pkcs12</span></span>
- <span data-ttu-id="9c7ee-148">application/x-pem-파일</span><span class="sxs-lookup"><span data-stu-id="9c7ee-148">application/x-pem-file</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: application/x-pkcs12, application/x-pem-file

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c7ee-149">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="9c7ee-149">-SubjectName</span></span>
<span data-ttu-id="9c7ee-150">인증서의 주체 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c7ee-150">Specifies the subject name of the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: SubjectName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: DNSNames
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c7ee-151">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="9c7ee-151">-ValidityInMonths</span></span>
<span data-ttu-id="9c7ee-152">인증서가 유효한 개월 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c7ee-152">Specifies the number of months the certificate is valid.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c7ee-153">-확인</span><span class="sxs-lookup"><span data-stu-id="9c7ee-153">-Confirm</span></span>
<span data-ttu-id="9c7ee-154">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c7ee-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c7ee-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c7ee-155">-WhatIf</span></span>
<span data-ttu-id="9c7ee-156">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9c7ee-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c7ee-157">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9c7ee-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c7ee-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c7ee-158">CommonParameters</span></span>
<span data-ttu-id="9c7ee-159">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c7ee-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c7ee-160">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c7ee-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c7ee-161">입력</span><span class="sxs-lookup"><span data-stu-id="9c7ee-161">INPUTS</span></span>

### <span data-ttu-id="9c7ee-162">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9c7ee-162">System.String</span></span>

### <span data-ttu-id="9c7ee-163">System.webserver. List ' 1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="9c7ee-163">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="9c7ee-164">시스템 Null 허용 ' 1 [[b77a5c561934e089, mscorlib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken =]]</span><span class="sxs-lookup"><span data-stu-id="9c7ee-164">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="9c7ee-165">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="9c7ee-165">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="9c7ee-166">System.webserver. List ' 1 [[X509Certificates. X509KeyUsageFlags, System, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="9c7ee-166">System.Collections.Generic.List\`1[[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags, System, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="9c7ee-167">출력</span><span class="sxs-lookup"><span data-stu-id="9c7ee-167">OUTPUTS</span></span>

### <span data-ttu-id="9c7ee-168">Microsoft. KeyVault. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="9c7ee-168">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="9c7ee-169">상속자</span><span class="sxs-lookup"><span data-stu-id="9c7ee-169">NOTES</span></span>

## <span data-ttu-id="9c7ee-170">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9c7ee-170">RELATED LINKS</span></span>

[<span data-ttu-id="9c7ee-171">Get-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="9c7ee-171">Get-AzureKeyVaultCertificatePolicy</span></span>](./Get-AzureKeyVaultCertificatePolicy.md)

[<span data-ttu-id="9c7ee-172">Set-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="9c7ee-172">Set-AzureKeyVaultCertificatePolicy</span></span>](./Set-AzureKeyVaultCertificatePolicy.md)

