---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 28BC1B99-946C-4A8D-9581-4D5CC0BCEF8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: 963a7005e95941a644b35a57f80b558f02e2d6a0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94211887"
---
# <span data-ttu-id="f9ac8-101">Set-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="f9ac8-101">Set-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="f9ac8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f9ac8-102">SYNOPSIS</span></span>
<span data-ttu-id="f9ac8-103">키 자격 증명 모음에서 인증서에 대 한 정책을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9ac8-103">Creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="f9ac8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f9ac8-104">SYNTAX</span></span>

### <span data-ttu-id="f9ac8-105">ExpandedRenewPercentage (기본값)</span><span class="sxs-lookup"><span data-stu-id="f9ac8-105">ExpandedRenewPercentage (Default)</span></span>
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

### <span data-ttu-id="f9ac8-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="f9ac8-106">ByValue</span></span>
```
Set-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-InputObject] <PSKeyVaultCertificatePolicy> [-EmailAtNumberOfDaysBeforeExpiry <Int32>]
 [-EmailAtPercentageLifetime <Int32>] [-KeyType <String>] [-KeySize <Int32>]
 [-CertificateTransparency <Boolean>] [-PassThru] [-Curve <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9ac8-107">ExpandedRenewNumber</span><span class="sxs-lookup"><span data-stu-id="f9ac8-107">ExpandedRenewNumber</span></span>
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

## <span data-ttu-id="f9ac8-108">설명은</span><span class="sxs-lookup"><span data-stu-id="f9ac8-108">DESCRIPTION</span></span>
<span data-ttu-id="f9ac8-109">**AzKeyVaultCertificatePolicy** cmdlet은 키 자격 증명 모음에서 인증서에 대 한 정책을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9ac8-109">The **Set-AzKeyVaultCertificatePolicy** cmdlet creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="f9ac8-110">예제의</span><span class="sxs-lookup"><span data-stu-id="f9ac8-110">EXAMPLES</span></span>

### <span data-ttu-id="f9ac8-111">예제 1: 인증서 정책 설정</span><span class="sxs-lookup"><span data-stu-id="f9ac8-111">Example 1: Set a certificate policy</span></span>
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

<span data-ttu-id="f9ac8-112">이 명령은 ContosoKV01 키 자격 증명 모음의 TestCert01 인증서에 대 한 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9ac8-112">This command sets the policy for the TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="f9ac8-113">변수</span><span class="sxs-lookup"><span data-stu-id="f9ac8-113">PARAMETERS</span></span>

### <span data-ttu-id="f9ac8-114">-CertificateTransparency</span><span class="sxs-lookup"><span data-stu-id="f9ac8-114">-CertificateTransparency</span></span>
<span data-ttu-id="f9ac8-115">인증서 투명도가이 인증서/발급자에 대해 사용 되는지 여부를 나타냅니다. 지정 하지 않은 경우 기본값은 ' true '입니다.</span><span class="sxs-lookup"><span data-stu-id="f9ac8-115">Indicates whether certificate transparency is enabled for this certificate/issuer; if not specified, the default is 'true'.</span></span>
<span data-ttu-id="f9ac8-116">`-IssuerName` 이 속성을 설정할 때 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9ac8-116">`-IssuerName` needs to be specified when setting this property.</span></span>

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

### <span data-ttu-id="f9ac8-117">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="f9ac8-117">-CertificateType</span></span>
<span data-ttu-id="f9ac8-118">발급자에 대 한 인증서 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9ac8-118">Specifies the type of certificate to the issuer.</span></span>

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

### <span data-ttu-id="f9ac8-119">-커브</span><span class="sxs-lookup"><span data-stu-id="f9ac8-119">-Curve</span></span>
<span data-ttu-id="f9ac8-120">인증서 키의 elliptic 곡선 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9ac8-120">Specifies the elliptic curve name of the key of the certificate.</span></span>
<span data-ttu-id="f9ac8-121">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="f9ac8-121">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f9ac8-122">P-256</span><span class="sxs-lookup"><span data-stu-id="f9ac8-122">P-256</span></span>
- <span data-ttu-id="f9ac8-123">P-384</span><span class="sxs-lookup"><span data-stu-id="f9ac8-123">P-384</span></span>
- <span data-ttu-id="f9ac8-124">P-521</span><span class="sxs-lookup"><span data-stu-id="f9ac8-124">P-521</span></span>
- <span data-ttu-id="f9ac8-125">P-256K</span><span class="sxs-lookup"><span data-stu-id="f9ac8-125">P-256K</span></span>
- <span data-ttu-id="f9ac8-126">SECP256K1</span><span class="sxs-lookup"><span data-stu-id="f9ac8-126">SECP256K1</span></span>

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

### <span data-ttu-id="f9ac8-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9ac8-127">-DefaultProfile</span></span>
<span data-ttu-id="f9ac8-128">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="f9ac8-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f9ac8-129">-사용 안 함</span><span class="sxs-lookup"><span data-stu-id="f9ac8-129">-Disabled</span></span>
<span data-ttu-id="f9ac8-130">인증서 정책을 사용할 수 없음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f9ac8-130">Indicates that the certificate policy is disabled.</span></span>

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

### <span data-ttu-id="f9ac8-131">-DnsName</span><span class="sxs-lookup"><span data-stu-id="f9ac8-131">-DnsName</span></span>
<span data-ttu-id="f9ac8-132">인증서의 주체 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9ac8-132">Specifies the subject name of the certificate.</span></span>

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

### <span data-ttu-id="f9ac8-133">-Eku</span><span class="sxs-lookup"><span data-stu-id="f9ac8-133">-Ekus</span></span>
<span data-ttu-id="f9ac8-134">인증서의 Eku (확장 된 키 용도)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9ac8-134">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

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

### <span data-ttu-id="f9ac8-135">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="f9ac8-135">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="f9ac8-136">자동 갱신이 시작 될 때까지 만료 되기까지 남은 일 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9ac8-136">Specifies the number of days before expiration when automatic renewal should start.</span></span>

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

### <span data-ttu-id="f9ac8-137">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="f9ac8-137">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="f9ac8-138">알림의 자동 프로세스가 시작 되는 수명에 대 한 백분율을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9ac8-138">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="f9ac8-139">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f9ac8-139">-InputObject</span></span>
<span data-ttu-id="f9ac8-140">인증서 정책을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9ac8-140">Specifies the certificate policy.</span></span>

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

### <span data-ttu-id="f9ac8-141">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="f9ac8-141">-IssuerName</span></span>
<span data-ttu-id="f9ac8-142">이 인증서에 대 한 발급자의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9ac8-142">Specifies the name of the issuer for this certificate.</span></span>

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

### <span data-ttu-id="f9ac8-143">-KeyNotExportable 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f9ac8-143">-KeyNotExportable</span></span>
<span data-ttu-id="f9ac8-144">키를 내보낼 수 없음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f9ac8-144">Indicates that the key is not exportable.</span></span>

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

### <span data-ttu-id="f9ac8-145">-KeySize</span><span class="sxs-lookup"><span data-stu-id="f9ac8-145">-KeySize</span></span>
<span data-ttu-id="f9ac8-146">인증서의 키 크기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9ac8-146">Specifies the key size of the certificate.</span></span>
<span data-ttu-id="f9ac8-147">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="f9ac8-147">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f9ac8-148">2048</span><span class="sxs-lookup"><span data-stu-id="f9ac8-148">2048</span></span>
- <span data-ttu-id="f9ac8-149">3072</span><span class="sxs-lookup"><span data-stu-id="f9ac8-149">3072</span></span>
- <span data-ttu-id="f9ac8-150">4096</span><span class="sxs-lookup"><span data-stu-id="f9ac8-150">4096</span></span>
- <span data-ttu-id="f9ac8-151">256</span><span class="sxs-lookup"><span data-stu-id="f9ac8-151">256</span></span>
- <span data-ttu-id="f9ac8-152">384</span><span class="sxs-lookup"><span data-stu-id="f9ac8-152">384</span></span>
- <span data-ttu-id="f9ac8-153">521</span><span class="sxs-lookup"><span data-stu-id="f9ac8-153">521</span></span>

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

### <span data-ttu-id="f9ac8-154">-KeyType</span><span class="sxs-lookup"><span data-stu-id="f9ac8-154">-KeyType</span></span>
<span data-ttu-id="f9ac8-155">인증서를 지 원하는 키의 키 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9ac8-155">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="f9ac8-156">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="f9ac8-156">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f9ac8-157">RSA</span><span class="sxs-lookup"><span data-stu-id="f9ac8-157">RSA</span></span>
- <span data-ttu-id="f9ac8-158">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="f9ac8-158">RSA-HSM</span></span>
- <span data-ttu-id="f9ac8-159">EC</span><span class="sxs-lookup"><span data-stu-id="f9ac8-159">EC</span></span>
- <span data-ttu-id="f9ac8-160">EC-HSM</span><span class="sxs-lookup"><span data-stu-id="f9ac8-160">EC-HSM</span></span>

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

### <span data-ttu-id="f9ac8-161">-KeyUsage</span><span class="sxs-lookup"><span data-stu-id="f9ac8-161">-KeyUsage</span></span>
<span data-ttu-id="f9ac8-162">인증서의 키 용도를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9ac8-162">Specifies the key usages in the certificate.</span></span>

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

### <span data-ttu-id="f9ac8-163">-이름</span><span class="sxs-lookup"><span data-stu-id="f9ac8-163">-Name</span></span>
<span data-ttu-id="f9ac8-164">인증서의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9ac8-164">Specifies the name of the certificate.</span></span>

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

### <span data-ttu-id="f9ac8-165">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f9ac8-165">-PassThru</span></span>
<span data-ttu-id="f9ac8-166">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9ac8-166">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f9ac8-167">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f9ac8-167">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f9ac8-168">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="f9ac8-168">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="f9ac8-169">인증서 갱신에 대 한 자동 프로세스가 시작 되는 만료 이전의 일 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9ac8-169">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="f9ac8-170">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="f9ac8-170">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="f9ac8-171">인증서 갱신에 대 한 자동 프로세스가 시작 되는 수명의 백분율을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9ac8-171">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="f9ac8-172">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="f9ac8-172">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="f9ac8-173">갱신 하는 동안 인증서가 키를 다시 사용 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f9ac8-173">Indicates that the certificate reuse the key during renewal.</span></span>

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

### <span data-ttu-id="f9ac8-174">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="f9ac8-174">-SecretContentType</span></span>
<span data-ttu-id="f9ac8-175">새 키 보관소 비밀의 콘텐츠 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9ac8-175">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="f9ac8-176">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="f9ac8-176">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f9ac8-177">application/x-pkcs12</span><span class="sxs-lookup"><span data-stu-id="f9ac8-177">application/x-pkcs12</span></span>
- <span data-ttu-id="f9ac8-178">application/x-pem-파일</span><span class="sxs-lookup"><span data-stu-id="f9ac8-178">application/x-pem-file</span></span>

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

### <span data-ttu-id="f9ac8-179">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="f9ac8-179">-SubjectName</span></span>
<span data-ttu-id="f9ac8-180">인증서의 주체 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9ac8-180">Specifies the subject name of the certificate.</span></span>

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

### <span data-ttu-id="f9ac8-181">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="f9ac8-181">-ValidityInMonths</span></span>
<span data-ttu-id="f9ac8-182">인증서가 유효한 개월 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9ac8-182">Specifies the number of months the certificate is valid.</span></span>

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

### <span data-ttu-id="f9ac8-183">-VaultName</span><span class="sxs-lookup"><span data-stu-id="f9ac8-183">-VaultName</span></span>
<span data-ttu-id="f9ac8-184">키 보관소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9ac8-184">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="f9ac8-185">-확인</span><span class="sxs-lookup"><span data-stu-id="f9ac8-185">-Confirm</span></span>
<span data-ttu-id="f9ac8-186">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9ac8-186">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9ac8-187">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9ac8-187">-WhatIf</span></span>
<span data-ttu-id="f9ac8-188">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f9ac8-188">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9ac8-189">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f9ac8-189">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9ac8-190">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9ac8-190">CommonParameters</span></span>
<span data-ttu-id="f9ac8-191">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9ac8-191">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9ac8-192">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f9ac8-192">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9ac8-193">입력</span><span class="sxs-lookup"><span data-stu-id="f9ac8-193">INPUTS</span></span>

### <span data-ttu-id="f9ac8-194">Microsoft. KeyVault. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="f9ac8-194">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="f9ac8-195">출력</span><span class="sxs-lookup"><span data-stu-id="f9ac8-195">OUTPUTS</span></span>

### <span data-ttu-id="f9ac8-196">Microsoft. KeyVault. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="f9ac8-196">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="f9ac8-197">상속자</span><span class="sxs-lookup"><span data-stu-id="f9ac8-197">NOTES</span></span>

## <span data-ttu-id="f9ac8-198">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f9ac8-198">RELATED LINKS</span></span>

[<span data-ttu-id="f9ac8-199">Get-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="f9ac8-199">Get-AzKeyVaultCertificatePolicy</span></span>](./Get-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="f9ac8-200">새로운 AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="f9ac8-200">New-AzKeyVaultCertificatePolicy</span></span>](./New-AzKeyVaultCertificatePolicy.md)

