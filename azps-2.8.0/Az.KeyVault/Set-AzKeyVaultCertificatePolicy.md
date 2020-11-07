---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 28BC1B99-946C-4A8D-9581-4D5CC0BCEF8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: e6ae1be8599869631698ddd886fa09184abfb867
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93689610"
---
# <span data-ttu-id="132c9-101">Set-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="132c9-101">Set-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="132c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="132c9-102">SYNOPSIS</span></span>
<span data-ttu-id="132c9-103">키 자격 증명 모음에서 인증서에 대 한 정책을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="132c9-103">Creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="132c9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="132c9-104">SYNTAX</span></span>

### <span data-ttu-id="132c9-105">ExpandedRenewPercentage (기본값)</span><span class="sxs-lookup"><span data-stu-id="132c9-105">ExpandedRenewPercentage (Default)</span></span>
```
Set-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String> [-RenewAtPercentageLifetime <Int32>]
 [-SecretContentType <String>] [-ReuseKeyOnRenewal <Boolean>] [-Disabled] [-SubjectName <String>]
 [-DnsName <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] [-IssuerName <String>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeySize <Int32>] [-KeyType <String>] [-KeyNotExportable] [-CertificateTransparency <Boolean>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="132c9-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="132c9-106">ByValue</span></span>
```
Set-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-InputObject] <PSKeyVaultCertificatePolicy> [-EmailAtNumberOfDaysBeforeExpiry <Int32>]
 [-EmailAtPercentageLifetime <Int32>] [-KeySize <Int32>] [-KeyType <String>] [-CertificateTransparency <Boolean>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="132c9-107">ExpandedRenewNumber</span><span class="sxs-lookup"><span data-stu-id="132c9-107">ExpandedRenewNumber</span></span>
```
Set-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String> -RenewAtNumberOfDaysBeforeExpiry <Int32>
 [-SecretContentType <String>] [-ReuseKeyOnRenewal <Boolean>] [-Disabled] [-SubjectName <String>]
 [-DnsName <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] [-IssuerName <String>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeySize <Int32>] [-KeyType <String>] [-KeyNotExportable] [-CertificateTransparency <Boolean>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="132c9-108">설명은</span><span class="sxs-lookup"><span data-stu-id="132c9-108">DESCRIPTION</span></span>
<span data-ttu-id="132c9-109">**AzKeyVaultCertificatePolicy** cmdlet은 키 자격 증명 모음에서 인증서에 대 한 정책을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="132c9-109">The **Set-AzKeyVaultCertificatePolicy** cmdlet creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="132c9-110">예제의</span><span class="sxs-lookup"><span data-stu-id="132c9-110">EXAMPLES</span></span>

### <span data-ttu-id="132c9-111">예제 1: 인증서 정책 설정</span><span class="sxs-lookup"><span data-stu-id="132c9-111">Example 1: Set a certificate policy</span></span>
```powershell
PS C:\> Set-AzKeyVaultCertificatePolicy -VaultName "ContosoKV01" -Name "TestCert01" -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal $True -PassThru

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

<span data-ttu-id="132c9-112">이 명령은 ContosoKV01 키 자격 증명 모음의 TestCert01 인증서에 대 한 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="132c9-112">This command sets the policy for the TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="132c9-113">변수</span><span class="sxs-lookup"><span data-stu-id="132c9-113">PARAMETERS</span></span>

### <span data-ttu-id="132c9-114">-CertificateTransparency</span><span class="sxs-lookup"><span data-stu-id="132c9-114">-CertificateTransparency</span></span>
<span data-ttu-id="132c9-115">인증서 투명도가이 인증서/발급자에 대해 사용 되는지 여부를 나타냅니다. 지정 하지 않은 경우 기본값은 ' true '입니다.</span><span class="sxs-lookup"><span data-stu-id="132c9-115">Indicates whether certificate transparency is enabled for this certificate/issuer; if not specified, the default is 'true'</span></span>

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

### <span data-ttu-id="132c9-116">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="132c9-116">-CertificateType</span></span>
<span data-ttu-id="132c9-117">발급자에 대 한 인증서 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="132c9-117">Specifies the type of certificate to the issuer.</span></span>

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

### <span data-ttu-id="132c9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="132c9-118">-DefaultProfile</span></span>
<span data-ttu-id="132c9-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="132c9-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="132c9-120">-사용 안 함</span><span class="sxs-lookup"><span data-stu-id="132c9-120">-Disabled</span></span>
<span data-ttu-id="132c9-121">인증서 정책을 사용할 수 없음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="132c9-121">Indicates that the certificate policy is disabled.</span></span>

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

### <span data-ttu-id="132c9-122">-DnsName</span><span class="sxs-lookup"><span data-stu-id="132c9-122">-DnsName</span></span>
<span data-ttu-id="132c9-123">인증서의 주체 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="132c9-123">Specifies the subject name of the certificate.</span></span>

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

### <span data-ttu-id="132c9-124">-Eku</span><span class="sxs-lookup"><span data-stu-id="132c9-124">-Ekus</span></span>
<span data-ttu-id="132c9-125">인증서의 Eku (확장 된 키 용도)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="132c9-125">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

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

### <span data-ttu-id="132c9-126">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="132c9-126">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="132c9-127">자동 갱신이 시작 될 때까지 만료 되기까지 남은 일 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="132c9-127">Specifies the number of days before expiration when automatic renewal should start.</span></span>

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

### <span data-ttu-id="132c9-128">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="132c9-128">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="132c9-129">알림의 자동 프로세스가 시작 되는 수명에 대 한 백분율을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="132c9-129">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="132c9-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="132c9-130">-InputObject</span></span>
<span data-ttu-id="132c9-131">인증서 정책을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="132c9-131">Specifies the certificate policy.</span></span>

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

### <span data-ttu-id="132c9-132">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="132c9-132">-IssuerName</span></span>
<span data-ttu-id="132c9-133">이 인증서에 대 한 발급자의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="132c9-133">Specifies the name of the issuer for this certificate.</span></span>

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

### <span data-ttu-id="132c9-134">-KeyNotExportable 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="132c9-134">-KeyNotExportable</span></span>
<span data-ttu-id="132c9-135">키를 내보낼 수 없음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="132c9-135">Indicates that the key is not exportable.</span></span>

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

### <span data-ttu-id="132c9-136">-KeySize</span><span class="sxs-lookup"><span data-stu-id="132c9-136">-KeySize</span></span>
<span data-ttu-id="132c9-137">인증서의 키 크기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="132c9-137">Specifies the key size of the certificate.</span></span>
<span data-ttu-id="132c9-138">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="132c9-138">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="132c9-139">2048</span><span class="sxs-lookup"><span data-stu-id="132c9-139">2048</span></span>
- <span data-ttu-id="132c9-140">3072</span><span class="sxs-lookup"><span data-stu-id="132c9-140">3072</span></span>
- <span data-ttu-id="132c9-141">4096</span><span class="sxs-lookup"><span data-stu-id="132c9-141">4096</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:
Accepted values: 2048, 3072, 4096

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="132c9-142">-KeyType</span><span class="sxs-lookup"><span data-stu-id="132c9-142">-KeyType</span></span>
<span data-ttu-id="132c9-143">인증서를 지 원하는 키의 키 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="132c9-143">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="132c9-144">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="132c9-144">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="132c9-145">RSA</span><span class="sxs-lookup"><span data-stu-id="132c9-145">RSA</span></span>
- <span data-ttu-id="132c9-146">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="132c9-146">RSA-HSM</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RSA, RSA-HSM

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="132c9-147">-KeyUsage</span><span class="sxs-lookup"><span data-stu-id="132c9-147">-KeyUsage</span></span>
<span data-ttu-id="132c9-148">인증서의 키 용도를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="132c9-148">Specifies the key usages in the certificate.</span></span>

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

### <span data-ttu-id="132c9-149">-이름</span><span class="sxs-lookup"><span data-stu-id="132c9-149">-Name</span></span>
<span data-ttu-id="132c9-150">인증서의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="132c9-150">Specifies the name of the certificate.</span></span>

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

### <span data-ttu-id="132c9-151">-PassThru</span><span class="sxs-lookup"><span data-stu-id="132c9-151">-PassThru</span></span>
<span data-ttu-id="132c9-152">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="132c9-152">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="132c9-153">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="132c9-153">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="132c9-154">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="132c9-154">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="132c9-155">인증서 갱신에 대 한 자동 프로세스가 시작 되는 만료 이전의 일 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="132c9-155">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="132c9-156">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="132c9-156">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="132c9-157">인증서 갱신에 대 한 자동 프로세스가 시작 되는 수명의 백분율을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="132c9-157">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="132c9-158">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="132c9-158">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="132c9-159">갱신 하는 동안 인증서가 키를 다시 사용 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="132c9-159">Indicates that the certificate reuse the key during renewal.</span></span>

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

### <span data-ttu-id="132c9-160">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="132c9-160">-SecretContentType</span></span>
<span data-ttu-id="132c9-161">새 키 보관소 비밀의 콘텐츠 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="132c9-161">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="132c9-162">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="132c9-162">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="132c9-163">application/x-pkcs12</span><span class="sxs-lookup"><span data-stu-id="132c9-163">application/x-pkcs12</span></span>
- <span data-ttu-id="132c9-164">application/x-pem-파일</span><span class="sxs-lookup"><span data-stu-id="132c9-164">application/x-pem-file</span></span>

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

### <span data-ttu-id="132c9-165">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="132c9-165">-SubjectName</span></span>
<span data-ttu-id="132c9-166">인증서의 주체 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="132c9-166">Specifies the subject name of the certificate.</span></span>

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

### <span data-ttu-id="132c9-167">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="132c9-167">-ValidityInMonths</span></span>
<span data-ttu-id="132c9-168">인증서가 유효한 개월 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="132c9-168">Specifies the number of months the certificate is valid.</span></span>

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

### <span data-ttu-id="132c9-169">-VaultName</span><span class="sxs-lookup"><span data-stu-id="132c9-169">-VaultName</span></span>
<span data-ttu-id="132c9-170">키 보관소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="132c9-170">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="132c9-171">-확인</span><span class="sxs-lookup"><span data-stu-id="132c9-171">-Confirm</span></span>
<span data-ttu-id="132c9-172">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="132c9-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="132c9-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="132c9-173">-WhatIf</span></span>
<span data-ttu-id="132c9-174">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="132c9-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="132c9-175">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="132c9-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="132c9-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="132c9-176">CommonParameters</span></span>
<span data-ttu-id="132c9-177">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="132c9-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="132c9-178">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="132c9-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="132c9-179">입력</span><span class="sxs-lookup"><span data-stu-id="132c9-179">INPUTS</span></span>

### <span data-ttu-id="132c9-180">Microsoft. KeyVault. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="132c9-180">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="132c9-181">출력</span><span class="sxs-lookup"><span data-stu-id="132c9-181">OUTPUTS</span></span>

### <span data-ttu-id="132c9-182">Microsoft. KeyVault. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="132c9-182">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="132c9-183">상속자</span><span class="sxs-lookup"><span data-stu-id="132c9-183">NOTES</span></span>

## <span data-ttu-id="132c9-184">관련 링크</span><span class="sxs-lookup"><span data-stu-id="132c9-184">RELATED LINKS</span></span>

[<span data-ttu-id="132c9-185">Get-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="132c9-185">Get-AzKeyVaultCertificatePolicy</span></span>](./Get-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="132c9-186">새로운 AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="132c9-186">New-AzKeyVaultCertificatePolicy</span></span>](./New-AzKeyVaultCertificatePolicy.md)

