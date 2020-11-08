---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 25E0F0E9-BF8C-49DF-87BA-31E2103A29A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: b0d690358fb5598b1a88ecb7fe169c8ef3d2718f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044881"
---
# <span data-ttu-id="b16b4-101">New-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="b16b4-101">New-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="b16b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b16b4-102">SYNOPSIS</span></span>
<span data-ttu-id="b16b4-103">메모리 내 인증서 정책 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b16b4-103">Creates an in-memory certificate policy object.</span></span>

## <span data-ttu-id="b16b4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b16b4-104">SYNTAX</span></span>

### <span data-ttu-id="b16b4-105">SubjectName (기본값)</span><span class="sxs-lookup"><span data-stu-id="b16b4-105">SubjectName (Default)</span></span>
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

### <span data-ttu-id="b16b4-106">DNSNames</span><span class="sxs-lookup"><span data-stu-id="b16b4-106">DNSNames</span></span>
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

## <span data-ttu-id="b16b4-107">설명은</span><span class="sxs-lookup"><span data-stu-id="b16b4-107">DESCRIPTION</span></span>
<span data-ttu-id="b16b4-108">**AzKeyVaultCertificatePolicy** Cmdlet은 Azure 키 자격 증명 모음에 대 한 메모리 내 인증서 정책 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b16b4-108">The **New-AzKeyVaultCertificatePolicy** cmdlet creates an in-memory certificate policy object for Azure Key Vault.</span></span>

## <span data-ttu-id="b16b4-109">예제의</span><span class="sxs-lookup"><span data-stu-id="b16b4-109">EXAMPLES</span></span>

### <span data-ttu-id="b16b4-110">예제 1: 인증서 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="b16b4-110">Example 1: Create a certificate policy</span></span>
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

<span data-ttu-id="b16b4-111">이 명령은 6 개월 동안 유효한 인증서 정책을 만든 다음 키를 다시 사용할 수 있도록 하 여 인증서를 갱신 합니다.</span><span class="sxs-lookup"><span data-stu-id="b16b4-111">This command creates a certificate policy that is valid for six months and reuses the key to renew the certificate.</span></span>

## <span data-ttu-id="b16b4-112">변수</span><span class="sxs-lookup"><span data-stu-id="b16b4-112">PARAMETERS</span></span>

### <span data-ttu-id="b16b4-113">-CertificateTransparency</span><span class="sxs-lookup"><span data-stu-id="b16b4-113">-CertificateTransparency</span></span>
<span data-ttu-id="b16b4-114">인증서 투명도가이 인증서/발급자에 대해 사용 되는지 여부를 나타냅니다. 지정 하지 않은 경우 기본값은 ' true '입니다.</span><span class="sxs-lookup"><span data-stu-id="b16b4-114">Indicates whether certificate transparency is enabled for this certificate/issuer; if not specified, the default is 'true'</span></span>

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

### <span data-ttu-id="b16b4-115">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="b16b4-115">-CertificateType</span></span>
<span data-ttu-id="b16b4-116">발급자에 대 한 인증서 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b16b4-116">Specifies the type of certificate to the issuer.</span></span>

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

### <span data-ttu-id="b16b4-117">-커브</span><span class="sxs-lookup"><span data-stu-id="b16b4-117">-Curve</span></span>
<span data-ttu-id="b16b4-118">인증서 키의 elliptic 곡선 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b16b4-118">Specifies the elliptic curve name of the key of the certificate.</span></span>
<span data-ttu-id="b16b4-119">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="b16b4-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b16b4-120">P-256</span><span class="sxs-lookup"><span data-stu-id="b16b4-120">P-256</span></span>
- <span data-ttu-id="b16b4-121">P-384</span><span class="sxs-lookup"><span data-stu-id="b16b4-121">P-384</span></span>
- <span data-ttu-id="b16b4-122">P-521</span><span class="sxs-lookup"><span data-stu-id="b16b4-122">P-521</span></span>
- <span data-ttu-id="b16b4-123">P-256K</span><span class="sxs-lookup"><span data-stu-id="b16b4-123">P-256K</span></span>
- <span data-ttu-id="b16b4-124">SECP256K1</span><span class="sxs-lookup"><span data-stu-id="b16b4-124">SECP256K1</span></span>

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

### <span data-ttu-id="b16b4-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b16b4-125">-DefaultProfile</span></span>
<span data-ttu-id="b16b4-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="b16b4-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b16b4-127">-사용 안 함</span><span class="sxs-lookup"><span data-stu-id="b16b4-127">-Disabled</span></span>
<span data-ttu-id="b16b4-128">인증서 정책을 사용할 수 없음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="b16b4-128">Indicates that the certificate policy is disabled.</span></span>

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

### <span data-ttu-id="b16b4-129">-DnsName</span><span class="sxs-lookup"><span data-stu-id="b16b4-129">-DnsName</span></span>
<span data-ttu-id="b16b4-130">인증서의 DNS 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b16b4-130">Specifies the DNS names in the certificate.</span></span>

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

### <span data-ttu-id="b16b4-131">-Eku</span><span class="sxs-lookup"><span data-stu-id="b16b4-131">-Ekus</span></span>
<span data-ttu-id="b16b4-132">인증서의 Eku (확장 된 키 용도)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b16b4-132">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

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

### <span data-ttu-id="b16b4-133">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="b16b4-133">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="b16b4-134">만료 되기까지 자동 알림 프로세스가 시작 되는 날짜 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b16b4-134">Specifies how many days before expiry the automatic notification process begins.</span></span>

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

### <span data-ttu-id="b16b4-135">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="b16b4-135">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="b16b4-136">알림의 자동 프로세스가 시작 되는 수명에 대 한 백분율을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b16b4-136">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="b16b4-137">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="b16b4-137">-IssuerName</span></span>
<span data-ttu-id="b16b4-138">인증서 발급자의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b16b4-138">Specifies the name of the issuer for the certificate.</span></span>

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

### <span data-ttu-id="b16b4-139">-KeyNotExportable 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b16b4-139">-KeyNotExportable</span></span>
<span data-ttu-id="b16b4-140">키를 내보낼 수 없음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="b16b4-140">Indicates that the key is not exportable.</span></span>

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

### <span data-ttu-id="b16b4-141">-KeySize</span><span class="sxs-lookup"><span data-stu-id="b16b4-141">-KeySize</span></span>
<span data-ttu-id="b16b4-142">인증서의 키 크기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b16b4-142">Specifies the key size of the certificate.</span></span>
<span data-ttu-id="b16b4-143">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="b16b4-143">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b16b4-144">2048</span><span class="sxs-lookup"><span data-stu-id="b16b4-144">2048</span></span>
- <span data-ttu-id="b16b4-145">3072</span><span class="sxs-lookup"><span data-stu-id="b16b4-145">3072</span></span>
- <span data-ttu-id="b16b4-146">4096</span><span class="sxs-lookup"><span data-stu-id="b16b4-146">4096</span></span>
- <span data-ttu-id="b16b4-147">256</span><span class="sxs-lookup"><span data-stu-id="b16b4-147">256</span></span>
- <span data-ttu-id="b16b4-148">384</span><span class="sxs-lookup"><span data-stu-id="b16b4-148">384</span></span>
- <span data-ttu-id="b16b4-149">521</span><span class="sxs-lookup"><span data-stu-id="b16b4-149">521</span></span>

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

### <span data-ttu-id="b16b4-150">-KeyType</span><span class="sxs-lookup"><span data-stu-id="b16b4-150">-KeyType</span></span>
<span data-ttu-id="b16b4-151">인증서를 지 원하는 키의 키 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b16b4-151">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="b16b4-152">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="b16b4-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b16b4-153">RSA</span><span class="sxs-lookup"><span data-stu-id="b16b4-153">RSA</span></span>
- <span data-ttu-id="b16b4-154">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="b16b4-154">RSA-HSM</span></span>
- <span data-ttu-id="b16b4-155">EC</span><span class="sxs-lookup"><span data-stu-id="b16b4-155">EC</span></span>
- <span data-ttu-id="b16b4-156">EC-HSM</span><span class="sxs-lookup"><span data-stu-id="b16b4-156">EC-HSM</span></span>

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

### <span data-ttu-id="b16b4-157">-KeyUsage</span><span class="sxs-lookup"><span data-stu-id="b16b4-157">-KeyUsage</span></span>
<span data-ttu-id="b16b4-158">인증서의 키 용도를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b16b4-158">Specifies the key usages in the certificate.</span></span>

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

### <span data-ttu-id="b16b4-159">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="b16b4-159">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="b16b4-160">인증서 갱신에 대 한 자동 프로세스가 시작 되는 만료 이전의 일 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b16b4-160">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="b16b4-161">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="b16b4-161">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="b16b4-162">인증서 갱신에 대 한 자동 프로세스가 시작 되는 수명의 백분율을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b16b4-162">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="b16b4-163">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="b16b4-163">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="b16b4-164">갱신 하는 동안 인증서가 키를 다시 사용 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="b16b4-164">Indicates that the certificate reuse the key during renewal.</span></span>

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

### <span data-ttu-id="b16b4-165">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="b16b4-165">-SecretContentType</span></span>
<span data-ttu-id="b16b4-166">새 키 보관소 비밀의 콘텐츠 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b16b4-166">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="b16b4-167">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="b16b4-167">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b16b4-168">application/x-pkcs12</span><span class="sxs-lookup"><span data-stu-id="b16b4-168">application/x-pkcs12</span></span>
- <span data-ttu-id="b16b4-169">application/x-pem-파일</span><span class="sxs-lookup"><span data-stu-id="b16b4-169">application/x-pem-file</span></span>

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

### <span data-ttu-id="b16b4-170">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="b16b4-170">-SubjectName</span></span>
<span data-ttu-id="b16b4-171">인증서의 주체 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b16b4-171">Specifies the subject name of the certificate.</span></span>

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

### <span data-ttu-id="b16b4-172">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="b16b4-172">-ValidityInMonths</span></span>
<span data-ttu-id="b16b4-173">인증서가 유효한 개월 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b16b4-173">Specifies the number of months the certificate is valid.</span></span>

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

### <span data-ttu-id="b16b4-174">-확인</span><span class="sxs-lookup"><span data-stu-id="b16b4-174">-Confirm</span></span>
<span data-ttu-id="b16b4-175">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b16b4-175">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b16b4-176">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b16b4-176">-WhatIf</span></span>
<span data-ttu-id="b16b4-177">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b16b4-177">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b16b4-178">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b16b4-178">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b16b4-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b16b4-179">CommonParameters</span></span>
<span data-ttu-id="b16b4-180">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b16b4-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b16b4-181">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b16b4-181">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b16b4-182">입력</span><span class="sxs-lookup"><span data-stu-id="b16b4-182">INPUTS</span></span>

### <span data-ttu-id="b16b4-183">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b16b4-183">System.String</span></span>

### <span data-ttu-id="b16b4-184">System.webserver. List ' 1 [[System.webserver], CoreLib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="b16b4-184">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="b16b4-185">시스템 Null 허용 ' 1 [[4.0.0.0, System.webserver, Version =, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e])</span><span class="sxs-lookup"><span data-stu-id="b16b4-185">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="b16b4-186">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="b16b4-186">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="b16b4-187">System.webserver. List ' 1 [[X509Certificates. X509KeyUsageFlags, X509Certificates, Version = 4.2.1.0, Culture = 중립, PublicKeyToken = b03f5f7f11d50a3a]])</span><span class="sxs-lookup"><span data-stu-id="b16b4-187">System.Collections.Generic.List\`1[[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags, System.Security.Cryptography.X509Certificates, Version=4.2.1.0, Culture=neutral, PublicKeyToken=b03f5f7f11d50a3a]]</span></span>

## <span data-ttu-id="b16b4-188">출력</span><span class="sxs-lookup"><span data-stu-id="b16b4-188">OUTPUTS</span></span>

### <span data-ttu-id="b16b4-189">Microsoft. KeyVault. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="b16b4-189">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="b16b4-190">상속자</span><span class="sxs-lookup"><span data-stu-id="b16b4-190">NOTES</span></span>

## <span data-ttu-id="b16b4-191">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b16b4-191">RELATED LINKS</span></span>

[<span data-ttu-id="b16b4-192">Get-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="b16b4-192">Get-AzKeyVaultCertificatePolicy</span></span>](./Get-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="b16b4-193">Set-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="b16b4-193">Set-AzKeyVaultCertificatePolicy</span></span>](./Set-AzKeyVaultCertificatePolicy.md)

