---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 28BC1B99-946C-4A8D-9581-4D5CC0BCEF8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: 5a6b88ce85b8b9296d9666955a93d1240b631634
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042542"
---
# <span data-ttu-id="68546-101">Set-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="68546-101">Set-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="68546-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="68546-102">SYNOPSIS</span></span>
<span data-ttu-id="68546-103">키 자격 증명 모음에서 인증서에 대 한 정책을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="68546-103">Creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="68546-104">구문과</span><span class="sxs-lookup"><span data-stu-id="68546-104">SYNTAX</span></span>

### <span data-ttu-id="68546-105">ExpandedRenewPercentage (기본값)</span><span class="sxs-lookup"><span data-stu-id="68546-105">ExpandedRenewPercentage (Default)</span></span>
```
Set-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String> [-RenewAtPercentageLifetime <Int32>]
 [-SecretContentType <String>] [-ReuseKeyOnRenewal <Boolean>] [-Disabled] [-SubjectName <String>]
 [-DnsName <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] [-IssuerName <String>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeySize <Int32>] [-KeyNotExportable] [-CertificateTransparency <Boolean>] [-PassThru]
 [-Curve <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68546-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="68546-106">ByValue</span></span>
```
Set-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-InputObject] <PSKeyVaultCertificatePolicy> [-EmailAtNumberOfDaysBeforeExpiry <Int32>]
 [-EmailAtPercentageLifetime <Int32>] [-KeyType <String>] [-KeySize <Int32>]
 [-CertificateTransparency <Boolean>] [-PassThru] [-Curve <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68546-107">ExpandedRenewNumber</span><span class="sxs-lookup"><span data-stu-id="68546-107">ExpandedRenewNumber</span></span>
```
Set-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String> -RenewAtNumberOfDaysBeforeExpiry <Int32>
 [-SecretContentType <String>] [-ReuseKeyOnRenewal <Boolean>] [-Disabled] [-SubjectName <String>]
 [-DnsName <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] [-IssuerName <String>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeySize <Int32>] [-KeyNotExportable] [-CertificateTransparency <Boolean>] [-PassThru]
 [-Curve <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68546-108">설명은</span><span class="sxs-lookup"><span data-stu-id="68546-108">DESCRIPTION</span></span>
<span data-ttu-id="68546-109">**AzKeyVaultCertificatePolicy** cmdlet은 키 자격 증명 모음에서 인증서에 대 한 정책을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="68546-109">The **Set-AzKeyVaultCertificatePolicy** cmdlet creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="68546-110">예제의</span><span class="sxs-lookup"><span data-stu-id="68546-110">EXAMPLES</span></span>

### <span data-ttu-id="68546-111">예제 1: 인증서 정책 설정</span><span class="sxs-lookup"><span data-stu-id="68546-111">Example 1: Set a certificate policy</span></span>
```powershell
PS C:\> Set-AzKeyVaultCertificatePolicy -VaultName "ContosoKV01" -Name "TestCert01" -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal $True -PassThru

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

<span data-ttu-id="68546-112">이 명령은 ContosoKV01 키 자격 증명 모음의 TestCert01 인증서에 대 한 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="68546-112">This command sets the policy for the TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="68546-113">변수</span><span class="sxs-lookup"><span data-stu-id="68546-113">PARAMETERS</span></span>

### <span data-ttu-id="68546-114">-CertificateTransparency</span><span class="sxs-lookup"><span data-stu-id="68546-114">-CertificateTransparency</span></span>
<span data-ttu-id="68546-115">인증서 투명도가이 인증서/발급자에 대해 사용 되는지 여부를 나타냅니다. 지정 하지 않은 경우 기본값은 ' true '입니다.</span><span class="sxs-lookup"><span data-stu-id="68546-115">Indicates whether certificate transparency is enabled for this certificate/issuer; if not specified, the default is 'true'</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68546-116">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="68546-116">-CertificateType</span></span>
<span data-ttu-id="68546-117">발급자에 대 한 인증서 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="68546-117">Specifies the type of certificate to the issuer.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68546-118">-커브</span><span class="sxs-lookup"><span data-stu-id="68546-118">-Curve</span></span>
<span data-ttu-id="68546-119">인증서 키의 elliptic 곡선 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="68546-119">Specifies the elliptic curve name of the key of the certificate.</span></span>
<span data-ttu-id="68546-120">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="68546-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="68546-121">P-256</span><span class="sxs-lookup"><span data-stu-id="68546-121">P-256</span></span>
- <span data-ttu-id="68546-122">P-384</span><span class="sxs-lookup"><span data-stu-id="68546-122">P-384</span></span>
- <span data-ttu-id="68546-123">P-521</span><span class="sxs-lookup"><span data-stu-id="68546-123">P-521</span></span>
- <span data-ttu-id="68546-124">P-256K</span><span class="sxs-lookup"><span data-stu-id="68546-124">P-256K</span></span>
- <span data-ttu-id="68546-125">SECP256K1</span><span class="sxs-lookup"><span data-stu-id="68546-125">SECP256K1</span></span>

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

### <span data-ttu-id="68546-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68546-126">-DefaultProfile</span></span>
<span data-ttu-id="68546-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="68546-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="68546-128">-사용 안 함</span><span class="sxs-lookup"><span data-stu-id="68546-128">-Disabled</span></span>
<span data-ttu-id="68546-129">인증서 정책을 사용할 수 없음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="68546-129">Indicates that the certificate policy is disabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68546-130">-DnsName</span><span class="sxs-lookup"><span data-stu-id="68546-130">-DnsName</span></span>
<span data-ttu-id="68546-131">인증서의 주체 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="68546-131">Specifies the subject name of the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases: DnsNames

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68546-132">-Eku</span><span class="sxs-lookup"><span data-stu-id="68546-132">-Ekus</span></span>
<span data-ttu-id="68546-133">인증서의 Eku (확장 된 키 용도)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="68546-133">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68546-134">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="68546-134">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="68546-135">자동 갱신이 시작 될 때까지 만료 되기까지 남은 일 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="68546-135">Specifies the number of days before expiration when automatic renewal should start.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68546-136">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="68546-136">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="68546-137">알림의 자동 프로세스가 시작 되는 수명에 대 한 백분율을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="68546-137">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68546-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="68546-138">-InputObject</span></span>
<span data-ttu-id="68546-139">인증서 정책을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="68546-139">Specifies the certificate policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy
Parameter Sets: ByValue
Aliases: CertificatePolicy

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="68546-140">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="68546-140">-IssuerName</span></span>
<span data-ttu-id="68546-141">이 인증서에 대 한 발급자의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="68546-141">Specifies the name of the issuer for this certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68546-142">-KeyNotExportable 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="68546-142">-KeyNotExportable</span></span>
<span data-ttu-id="68546-143">키를 내보낼 수 없음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="68546-143">Indicates that the key is not exportable.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68546-144">-KeySize</span><span class="sxs-lookup"><span data-stu-id="68546-144">-KeySize</span></span>
<span data-ttu-id="68546-145">인증서의 키 크기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="68546-145">Specifies the key size of the certificate.</span></span>
<span data-ttu-id="68546-146">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="68546-146">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="68546-147">2048</span><span class="sxs-lookup"><span data-stu-id="68546-147">2048</span></span>
- <span data-ttu-id="68546-148">3072</span><span class="sxs-lookup"><span data-stu-id="68546-148">3072</span></span>
- <span data-ttu-id="68546-149">4096</span><span class="sxs-lookup"><span data-stu-id="68546-149">4096</span></span>
- <span data-ttu-id="68546-150">256</span><span class="sxs-lookup"><span data-stu-id="68546-150">256</span></span>
- <span data-ttu-id="68546-151">384</span><span class="sxs-lookup"><span data-stu-id="68546-151">384</span></span>
- <span data-ttu-id="68546-152">521</span><span class="sxs-lookup"><span data-stu-id="68546-152">521</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:
Accepted values: 2048, 3072, 4096, 256, 384, 521

Required: False
Position: Named
Default value: 2048
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68546-153">-KeyType</span><span class="sxs-lookup"><span data-stu-id="68546-153">-KeyType</span></span>
<span data-ttu-id="68546-154">인증서를 지 원하는 키의 키 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="68546-154">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="68546-155">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="68546-155">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="68546-156">RSA</span><span class="sxs-lookup"><span data-stu-id="68546-156">RSA</span></span>
- <span data-ttu-id="68546-157">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="68546-157">RSA-HSM</span></span>
- <span data-ttu-id="68546-158">EC</span><span class="sxs-lookup"><span data-stu-id="68546-158">EC</span></span>
- <span data-ttu-id="68546-159">EC-HSM</span><span class="sxs-lookup"><span data-stu-id="68546-159">EC-HSM</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RSA, RSA-HSM, EC, EC-HSM

Required: False
Position: Named
Default value: RSA
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68546-160">-KeyUsage</span><span class="sxs-lookup"><span data-stu-id="68546-160">-KeyUsage</span></span>
<span data-ttu-id="68546-161">인증서의 키 용도를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="68546-161">Specifies the key usages in the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:
Accepted values: None, EncipherOnly, CrlSign, KeyCertSign, KeyAgreement, DataEncipherment, KeyEncipherment, NonRepudiation, DigitalSignature, DecipherOnly

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68546-162">-이름</span><span class="sxs-lookup"><span data-stu-id="68546-162">-Name</span></span>
<span data-ttu-id="68546-163">인증서의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="68546-163">Specifies the name of the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68546-164">-PassThru</span><span class="sxs-lookup"><span data-stu-id="68546-164">-PassThru</span></span>
<span data-ttu-id="68546-165">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="68546-165">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="68546-166">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="68546-166">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="68546-167">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="68546-167">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="68546-168">인증서 갱신에 대 한 자동 프로세스가 시작 되는 만료 이전의 일 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="68546-168">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ExpandedRenewNumber
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68546-169">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="68546-169">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="68546-170">인증서 갱신에 대 한 자동 프로세스가 시작 되는 수명의 백분율을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="68546-170">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ExpandedRenewPercentage
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68546-171">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="68546-171">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="68546-172">갱신 하는 동안 인증서가 키를 다시 사용 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="68546-172">Indicates that the certificate reuse the key during renewal.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68546-173">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="68546-173">-SecretContentType</span></span>
<span data-ttu-id="68546-174">새 키 보관소 비밀의 콘텐츠 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="68546-174">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="68546-175">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="68546-175">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="68546-176">application/x-pkcs12</span><span class="sxs-lookup"><span data-stu-id="68546-176">application/x-pkcs12</span></span>
- <span data-ttu-id="68546-177">application/x-pem-파일</span><span class="sxs-lookup"><span data-stu-id="68546-177">application/x-pem-file</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:
Accepted values: application/x-pkcs12, application/x-pem-file

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68546-178">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="68546-178">-SubjectName</span></span>
<span data-ttu-id="68546-179">인증서의 주체 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="68546-179">Specifies the subject name of the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68546-180">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="68546-180">-ValidityInMonths</span></span>
<span data-ttu-id="68546-181">인증서가 유효한 개월 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="68546-181">Specifies the number of months the certificate is valid.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68546-182">-VaultName</span><span class="sxs-lookup"><span data-stu-id="68546-182">-VaultName</span></span>
<span data-ttu-id="68546-183">키 보관소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="68546-183">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68546-184">-확인</span><span class="sxs-lookup"><span data-stu-id="68546-184">-Confirm</span></span>
<span data-ttu-id="68546-185">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="68546-185">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68546-186">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68546-186">-WhatIf</span></span>
<span data-ttu-id="68546-187">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="68546-187">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68546-188">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="68546-188">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68546-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68546-189">CommonParameters</span></span>
<span data-ttu-id="68546-190">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="68546-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68546-191">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="68546-191">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68546-192">입력</span><span class="sxs-lookup"><span data-stu-id="68546-192">INPUTS</span></span>

### <span data-ttu-id="68546-193">Microsoft. KeyVault. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="68546-193">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="68546-194">출력</span><span class="sxs-lookup"><span data-stu-id="68546-194">OUTPUTS</span></span>

### <span data-ttu-id="68546-195">Microsoft. KeyVault. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="68546-195">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="68546-196">상속자</span><span class="sxs-lookup"><span data-stu-id="68546-196">NOTES</span></span>

## <span data-ttu-id="68546-197">관련 링크</span><span class="sxs-lookup"><span data-stu-id="68546-197">RELATED LINKS</span></span>

[<span data-ttu-id="68546-198">Get-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="68546-198">Get-AzKeyVaultCertificatePolicy</span></span>](./Get-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="68546-199">새로운 AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="68546-199">New-AzKeyVaultCertificatePolicy</span></span>](./New-AzKeyVaultCertificatePolicy.md)

