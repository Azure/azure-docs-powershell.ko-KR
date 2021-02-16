---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 25E0F0E9-BF8C-49DF-87BA-31E2103A29A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: 370662b1d24f9b5b71653506be7a3add5a3801f8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185561"
---
# <span data-ttu-id="108ad-101">New-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="108ad-101">New-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="108ad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="108ad-102">SYNOPSIS</span></span>
<span data-ttu-id="108ad-103">메모리 내 인증서 정책 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="108ad-103">Creates an in-memory certificate policy object.</span></span>

## <span data-ttu-id="108ad-104">구문</span><span class="sxs-lookup"><span data-stu-id="108ad-104">SYNTAX</span></span>

### <span data-ttu-id="108ad-105">SubjectName(기본값)</span><span class="sxs-lookup"><span data-stu-id="108ad-105">SubjectName (Default)</span></span>
```
New-AzKeyVaultCertificatePolicy [-IssuerName] <String> [-SubjectName] <String>
 [-RenewAtNumberOfDaysBeforeExpiry <Int32>] [-RenewAtPercentageLifetime <Int32>] [-SecretContentType <String>]
 [-ReuseKeyOnRenewal] [-Disabled]
 [-KeyUsage <System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeySize <Int32>] [-KeyNotExportable] [-CertificateTransparency <Boolean>]
 [-Curve <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="108ad-106">DNSNames</span><span class="sxs-lookup"><span data-stu-id="108ad-106">DNSNames</span></span>
```
New-AzKeyVaultCertificatePolicy [-IssuerName] <String> [[-SubjectName] <String>]
 [-DnsName] <System.Collections.Generic.List`1[System.String]> [-RenewAtNumberOfDaysBeforeExpiry <Int32>]
 [-RenewAtPercentageLifetime <Int32>] [-SecretContentType <String>] [-ReuseKeyOnRenewal] [-Disabled]
 [-KeyUsage <System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeySize <Int32>] [-KeyNotExportable] [-CertificateTransparency <Boolean>]
 [-Curve <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="108ad-107">설명</span><span class="sxs-lookup"><span data-stu-id="108ad-107">DESCRIPTION</span></span>
<span data-ttu-id="108ad-108">**New-AzKeyVaultCertificatePolicy** cmdlet은 Azure Key Vault에 대한 메모리 내 인증서 정책 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="108ad-108">The **New-AzKeyVaultCertificatePolicy** cmdlet creates an in-memory certificate policy object for Azure Key Vault.</span></span>

## <span data-ttu-id="108ad-109">예제</span><span class="sxs-lookup"><span data-stu-id="108ad-109">EXAMPLES</span></span>

### <span data-ttu-id="108ad-110">예제 1: 인증서 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="108ad-110">Example 1: Create a certificate policy</span></span>
```powershell
PS C:\> New-AzKeyVaultCertificatePolicy -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal

SecretContentType               : application/x-pkcs12
Kty                             :
KeySize                         : 2048
Curve                           :
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

<span data-ttu-id="108ad-111">이 명령은 6개월 동안 유효한 인증서 정책을 만들고 키를 다시 사용하여 인증서를 갱신합니다.</span><span class="sxs-lookup"><span data-stu-id="108ad-111">This command creates a certificate policy that is valid for six months and reuses the key to renew the certificate.</span></span>

### <span data-ttu-id="108ad-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="108ad-112">Example 2</span></span>

<span data-ttu-id="108ad-113">메모리 내 인증서 정책 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="108ad-113">Creates an in-memory certificate policy object.</span></span> <span data-ttu-id="108ad-114">(자동Generated)</span><span class="sxs-lookup"><span data-stu-id="108ad-114">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzKeyVaultCertificatePolicy -IssuerName 'Self' -KeyType RSA -RenewAtNumberOfDaysBeforeExpiry <Int32> -SecretContentType application/x-pkcs12 -SubjectName 'CN=contoso.com' -ValidityInMonths 6
```

### <span data-ttu-id="108ad-115">예제 3: 주체 대체 이름(또는 SAN) 인증서 만들기</span><span class="sxs-lookup"><span data-stu-id="108ad-115">Example 3: Create a Subject Alternate Name (or SAN) certificate</span></span>

```powershell
PS C:\> New-AzKeyVaultCertificatePolicy -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -DnsName "contoso.com","support.contoso.com","docs.contoso.com" -IssuerName "Self"

SecretContentType               : application/x-pkcs12
Kty                             : RSA
KeySize                         : 2048
Curve                           :
Exportable                      :
ReuseKeyOnRenewal               : False
SubjectName                     : CN=contoso.com
DnsNames                        : {contoso.com, support.contoso.com, docs.contoso.com}
KeyUsage                        :
Ekus                            :
ValidityInMonths                :
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

<span data-ttu-id="108ad-116">이 예제에서는 DNS 이름이 3개인 SAN 인증서를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="108ad-116">This example creates a SAN certificate with 3 DNS names.</span></span>

## <span data-ttu-id="108ad-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="108ad-117">PARAMETERS</span></span>

### <span data-ttu-id="108ad-118">-CertificateTransparency</span><span class="sxs-lookup"><span data-stu-id="108ad-118">-CertificateTransparency</span></span>
<span data-ttu-id="108ad-119">이 인증서/발급자에 대해 인증서 투명도를 사용하도록 설정되어 있는지 여부를 나타냅니다. 지정하지 않으면 기본값은 'true'입니다.</span><span class="sxs-lookup"><span data-stu-id="108ad-119">Indicates whether certificate transparency is enabled for this certificate/issuer; if not specified, the default is 'true'</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="108ad-120">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="108ad-120">-CertificateType</span></span>
<span data-ttu-id="108ad-121">발급자에 대한 인증서 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="108ad-121">Specifies the type of certificate to the issuer.</span></span>

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

### <span data-ttu-id="108ad-122">-Curve</span><span class="sxs-lookup"><span data-stu-id="108ad-122">-Curve</span></span>
<span data-ttu-id="108ad-123">인증서 키의 타원 곡선 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="108ad-123">Specifies the elliptic curve name of the key of the certificate.</span></span>
<span data-ttu-id="108ad-124">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="108ad-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="108ad-125">P-256</span><span class="sxs-lookup"><span data-stu-id="108ad-125">P-256</span></span>
- <span data-ttu-id="108ad-126">P-384</span><span class="sxs-lookup"><span data-stu-id="108ad-126">P-384</span></span>
- <span data-ttu-id="108ad-127">P-521</span><span class="sxs-lookup"><span data-stu-id="108ad-127">P-521</span></span>
- <span data-ttu-id="108ad-128">P-256K</span><span class="sxs-lookup"><span data-stu-id="108ad-128">P-256K</span></span>
- <span data-ttu-id="108ad-129">SECP256K1</span><span class="sxs-lookup"><span data-stu-id="108ad-129">SECP256K1</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: P-256, P-384, P-521, P-256K, SECP256K1

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="108ad-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="108ad-130">-DefaultProfile</span></span>
<span data-ttu-id="108ad-131">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="108ad-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="108ad-132">-Disabled</span><span class="sxs-lookup"><span data-stu-id="108ad-132">-Disabled</span></span>
<span data-ttu-id="108ad-133">인증서 정책이 비활성화되어 있는 경우를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="108ad-133">Indicates that the certificate policy is disabled.</span></span>

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

### <span data-ttu-id="108ad-134">-DnsName</span><span class="sxs-lookup"><span data-stu-id="108ad-134">-DnsName</span></span>
<span data-ttu-id="108ad-135">인증서의 DNS 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="108ad-135">Specifies the DNS names in the certificate.</span></span> <span data-ttu-id="108ad-136">주체 대체 이름(SANS)을 DNS 이름으로 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="108ad-136">Subject Alternative Names (SANs) can be specified as DNS names.</span></span>

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

### <span data-ttu-id="108ad-137">-Ekus</span><span class="sxs-lookup"><span data-stu-id="108ad-137">-Ekus</span></span>
<span data-ttu-id="108ad-138">인증서에서 EKUS(향상된 키 사용)를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="108ad-138">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

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

### <span data-ttu-id="108ad-139">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="108ad-139">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="108ad-140">자동 알림 프로세스가 만료되기 전의 일 수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="108ad-140">Specifies how many days before expiry the automatic notification process begins.</span></span>

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

### <span data-ttu-id="108ad-141">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="108ad-141">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="108ad-142">알림에 대한 자동 프로세스가 시작된 후 수명의 백분율을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="108ad-142">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="108ad-143">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="108ad-143">-IssuerName</span></span>
<span data-ttu-id="108ad-144">인증서에 대한 발급자 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="108ad-144">Specifies the name of the issuer for the certificate.</span></span>

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

### <span data-ttu-id="108ad-145">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="108ad-145">-KeyNotExportable</span></span>
<span data-ttu-id="108ad-146">키를 내보낼 수 없다고 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="108ad-146">Indicates that the key is not exportable.</span></span>

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

### <span data-ttu-id="108ad-147">-KeySize</span><span class="sxs-lookup"><span data-stu-id="108ad-147">-KeySize</span></span>
<span data-ttu-id="108ad-148">인증서의 키 크기를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="108ad-148">Specifies the key size of the certificate.</span></span>
<span data-ttu-id="108ad-149">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="108ad-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="108ad-150">2048</span><span class="sxs-lookup"><span data-stu-id="108ad-150">2048</span></span>
- <span data-ttu-id="108ad-151">3072</span><span class="sxs-lookup"><span data-stu-id="108ad-151">3072</span></span>
- <span data-ttu-id="108ad-152">4096</span><span class="sxs-lookup"><span data-stu-id="108ad-152">4096</span></span>
- <span data-ttu-id="108ad-153">256</span><span class="sxs-lookup"><span data-stu-id="108ad-153">256</span></span>
- <span data-ttu-id="108ad-154">384</span><span class="sxs-lookup"><span data-stu-id="108ad-154">384</span></span>
- <span data-ttu-id="108ad-155">521</span><span class="sxs-lookup"><span data-stu-id="108ad-155">521</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:
Accepted values: 2048, 3072, 4096, 256, 384, 521

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="108ad-156">-KeyType</span><span class="sxs-lookup"><span data-stu-id="108ad-156">-KeyType</span></span>
<span data-ttu-id="108ad-157">인증서를 백업하는 키의 키 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="108ad-157">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="108ad-158">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="108ad-158">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="108ad-159">RSA</span><span class="sxs-lookup"><span data-stu-id="108ad-159">RSA</span></span>
- <span data-ttu-id="108ad-160">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="108ad-160">RSA-HSM</span></span>
- <span data-ttu-id="108ad-161">EC</span><span class="sxs-lookup"><span data-stu-id="108ad-161">EC</span></span>
- <span data-ttu-id="108ad-162">EC-HSM</span><span class="sxs-lookup"><span data-stu-id="108ad-162">EC-HSM</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RSA, RSA-HSM, EC, EC-HSM

Required: False
Position: Named
Default value: RSA
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="108ad-163">-KeyUsage</span><span class="sxs-lookup"><span data-stu-id="108ad-163">-KeyUsage</span></span>
<span data-ttu-id="108ad-164">인증서의 키 사용량을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="108ad-164">Specifies the key usages in the certificate.</span></span>

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

### <span data-ttu-id="108ad-165">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="108ad-165">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="108ad-166">인증서 갱신에 대한 자동 프로세스가 시작되는 만료 전 일 수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="108ad-166">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="108ad-167">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="108ad-167">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="108ad-168">인증서 갱신에 대한 자동 프로세스가 시작되는 수명의 백분율을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="108ad-168">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="108ad-169">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="108ad-169">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="108ad-170">인증서가 갱신하는 동안 키를 다시 사용하게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="108ad-170">Indicates that the certificate reuse the key during renewal.</span></span>

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

### <span data-ttu-id="108ad-171">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="108ad-171">-SecretContentType</span></span>
<span data-ttu-id="108ad-172">새 Key Vault 비밀의 콘텐츠 형식을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="108ad-172">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="108ad-173">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="108ad-173">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="108ad-174">application/x-pkcs12</span><span class="sxs-lookup"><span data-stu-id="108ad-174">application/x-pkcs12</span></span>
- <span data-ttu-id="108ad-175">application/x-pem-file</span><span class="sxs-lookup"><span data-stu-id="108ad-175">application/x-pem-file</span></span>

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

### <span data-ttu-id="108ad-176">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="108ad-176">-SubjectName</span></span>
<span data-ttu-id="108ad-177">인증서의 주체 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="108ad-177">Specifies the subject name of the certificate.</span></span> 

> [!NOTE]
> <span data-ttu-id="108ad-178">매개 변수의 속성 내에 콤마(,) 또는 마침표(.)를 사용하려면 속성 필드를 인용 부호로 `SubjectName` 묶아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="108ad-178">If you must use a comma (,) or a period (.) within a property in the `SubjectName` parameter, you must enclose the property field in quotation marks.</span></span> <span data-ttu-id="108ad-179">예를 들어 O="Contoso, Ltd"를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="108ad-179">For example, you may use O="Contoso, Ltd."</span></span> <span data-ttu-id="108ad-180">를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="108ad-180">in the Organization Name field.</span></span>

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

### <span data-ttu-id="108ad-181">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="108ad-181">-ValidityInMonths</span></span>
<span data-ttu-id="108ad-182">인증서가 유효한 개월 수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="108ad-182">Specifies the number of months the certificate is valid.</span></span>

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

### <span data-ttu-id="108ad-183">-Confirm</span><span class="sxs-lookup"><span data-stu-id="108ad-183">-Confirm</span></span>
<span data-ttu-id="108ad-184">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="108ad-184">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="108ad-185">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="108ad-185">-WhatIf</span></span>
<span data-ttu-id="108ad-186">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="108ad-186">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="108ad-187">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="108ad-187">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="108ad-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="108ad-188">CommonParameters</span></span>
<span data-ttu-id="108ad-189">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="108ad-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="108ad-190">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="108ad-190">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="108ad-191">입력</span><span class="sxs-lookup"><span data-stu-id="108ad-191">INPUTS</span></span>

### <span data-ttu-id="108ad-192">System.String</span><span class="sxs-lookup"><span data-stu-id="108ad-192">System.String</span></span>

### <span data-ttu-id="108ad-193">System.Collections.Generic.List'1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="108ad-193">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="108ad-194">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="108ad-194">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="108ad-195">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="108ad-195">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="108ad-196">System.Collections.Generic.List'1[[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags, System.Security.Cryptography.X509Certificates, Version=4.2.1.0, Culture=neutral, PublicKeyToken=b03f5f7f11d50a3a]]</span><span class="sxs-lookup"><span data-stu-id="108ad-196">System.Collections.Generic.List\`1[[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags, System.Security.Cryptography.X509Certificates, Version=4.2.1.0, Culture=neutral, PublicKeyToken=b03f5f7f11d50a3a]]</span></span>

## <span data-ttu-id="108ad-197">출력</span><span class="sxs-lookup"><span data-stu-id="108ad-197">OUTPUTS</span></span>

### <span data-ttu-id="108ad-198">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="108ad-198">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="108ad-199">참고 사항</span><span class="sxs-lookup"><span data-stu-id="108ad-199">NOTES</span></span>

## <span data-ttu-id="108ad-200">관련 링크</span><span class="sxs-lookup"><span data-stu-id="108ad-200">RELATED LINKS</span></span>

[<span data-ttu-id="108ad-201">Get-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="108ad-201">Get-AzKeyVaultCertificatePolicy</span></span>](./Get-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="108ad-202">Set-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="108ad-202">Set-AzKeyVaultCertificatePolicy</span></span>](./Set-AzKeyVaultCertificatePolicy.md)

