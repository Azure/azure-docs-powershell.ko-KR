---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 28BC1B99-946C-4A8D-9581-4D5CC0BCEF8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: eec95cd9c7873d26f88390c5a623a6af40991dfd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93867886"
---
# <span data-ttu-id="ffc02-101">Set-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="ffc02-101">Set-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="ffc02-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ffc02-102">SYNOPSIS</span></span>
<span data-ttu-id="ffc02-103">키 자격 증명 모음에서 인증서에 대 한 정책을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffc02-103">Creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="ffc02-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ffc02-104">SYNTAX</span></span>

### <span data-ttu-id="ffc02-105">ExpandedRenewPercentage (기본값)</span><span class="sxs-lookup"><span data-stu-id="ffc02-105">ExpandedRenewPercentage (Default)</span></span>
```
Set-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String> [-RenewAtPercentageLifetime <Int32>]
 [-SecretContentType <String>] [-ReuseKeyOnRenewal <Boolean>] [-Disabled] [-SubjectName <String>]
 [-DnsName <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] [-IssuerName <String>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeyNotExportable] [-CertificateTransparency <Boolean>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ffc02-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="ffc02-106">ByValue</span></span>
```
Set-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-InputObject] <PSKeyVaultCertificatePolicy> [-EmailAtNumberOfDaysBeforeExpiry <Int32>]
 [-EmailAtPercentageLifetime <Int32>] [-KeyType <String>] [-CertificateTransparency <Boolean>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ffc02-107">ExpandedRenewNumber</span><span class="sxs-lookup"><span data-stu-id="ffc02-107">ExpandedRenewNumber</span></span>
```
Set-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String> -RenewAtNumberOfDaysBeforeExpiry <Int32>
 [-SecretContentType <String>] [-ReuseKeyOnRenewal <Boolean>] [-Disabled] [-SubjectName <String>]
 [-DnsName <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] [-IssuerName <String>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeyNotExportable] [-CertificateTransparency <Boolean>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ffc02-108">설명은</span><span class="sxs-lookup"><span data-stu-id="ffc02-108">DESCRIPTION</span></span>
<span data-ttu-id="ffc02-109">**AzKeyVaultCertificatePolicy** cmdlet은 키 자격 증명 모음에서 인증서에 대 한 정책을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffc02-109">The **Set-AzKeyVaultCertificatePolicy** cmdlet creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="ffc02-110">예제의</span><span class="sxs-lookup"><span data-stu-id="ffc02-110">EXAMPLES</span></span>

### <span data-ttu-id="ffc02-111">예제 1: 인증서 정책 설정</span><span class="sxs-lookup"><span data-stu-id="ffc02-111">Example 1: Set a certificate policy</span></span>
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

<span data-ttu-id="ffc02-112">이 명령은 ContosoKV01 키 자격 증명 모음의 TestCert01 인증서에 대 한 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffc02-112">This command sets the policy for the TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="ffc02-113">변수</span><span class="sxs-lookup"><span data-stu-id="ffc02-113">PARAMETERS</span></span>

### <span data-ttu-id="ffc02-114">-CertificateTransparency</span><span class="sxs-lookup"><span data-stu-id="ffc02-114">-CertificateTransparency</span></span>
<span data-ttu-id="ffc02-115">인증서 투명도가이 인증서/발급자에 대해 사용 되는지 여부를 나타냅니다. 지정 하지 않은 경우 기본값은 ' true '입니다.</span><span class="sxs-lookup"><span data-stu-id="ffc02-115">Indicates whether certificate transparency is enabled for this certificate/issuer; if not specified, the default is 'true'</span></span>

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

### <span data-ttu-id="ffc02-116">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="ffc02-116">-CertificateType</span></span>
<span data-ttu-id="ffc02-117">발급자에 대 한 인증서 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffc02-117">Specifies the type of certificate to the issuer.</span></span>

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

### <span data-ttu-id="ffc02-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffc02-118">-DefaultProfile</span></span>
<span data-ttu-id="ffc02-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="ffc02-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ffc02-120">-사용 안 함</span><span class="sxs-lookup"><span data-stu-id="ffc02-120">-Disabled</span></span>
<span data-ttu-id="ffc02-121">인증서 정책을 사용할 수 없음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ffc02-121">Indicates that the certificate policy is disabled.</span></span>

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

### <span data-ttu-id="ffc02-122">-DnsName</span><span class="sxs-lookup"><span data-stu-id="ffc02-122">-DnsName</span></span>
<span data-ttu-id="ffc02-123">인증서의 주체 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffc02-123">Specifies the subject name of the certificate.</span></span>

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

### <span data-ttu-id="ffc02-124">-Eku</span><span class="sxs-lookup"><span data-stu-id="ffc02-124">-Ekus</span></span>
<span data-ttu-id="ffc02-125">인증서의 Eku (확장 된 키 용도)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffc02-125">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

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

### <span data-ttu-id="ffc02-126">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="ffc02-126">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="ffc02-127">자동 갱신이 시작 될 때까지 만료 되기까지 남은 일 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffc02-127">Specifies the number of days before expiration when automatic renewal should start.</span></span>

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

### <span data-ttu-id="ffc02-128">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="ffc02-128">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="ffc02-129">알림의 자동 프로세스가 시작 되는 수명에 대 한 백분율을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffc02-129">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="ffc02-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ffc02-130">-InputObject</span></span>
<span data-ttu-id="ffc02-131">인증서 정책을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffc02-131">Specifies the certificate policy.</span></span>

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

### <span data-ttu-id="ffc02-132">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="ffc02-132">-IssuerName</span></span>
<span data-ttu-id="ffc02-133">이 인증서에 대 한 발급자의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffc02-133">Specifies the name of the issuer for this certificate.</span></span>

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

### <span data-ttu-id="ffc02-134">-KeyNotExportable 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ffc02-134">-KeyNotExportable</span></span>
<span data-ttu-id="ffc02-135">키를 내보낼 수 없음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ffc02-135">Indicates that the key is not exportable.</span></span>

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

### <span data-ttu-id="ffc02-136">-KeyType</span><span class="sxs-lookup"><span data-stu-id="ffc02-136">-KeyType</span></span>
<span data-ttu-id="ffc02-137">인증서를 지 원하는 키의 키 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffc02-137">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="ffc02-138">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="ffc02-138">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ffc02-139">RSA</span><span class="sxs-lookup"><span data-stu-id="ffc02-139">RSA</span></span>
- <span data-ttu-id="ffc02-140">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="ffc02-140">RSA-HSM</span></span>

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

### <span data-ttu-id="ffc02-141">-KeyUsage</span><span class="sxs-lookup"><span data-stu-id="ffc02-141">-KeyUsage</span></span>
<span data-ttu-id="ffc02-142">인증서의 키 용도를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffc02-142">Specifies the key usages in the certificate.</span></span>

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

### <span data-ttu-id="ffc02-143">-이름</span><span class="sxs-lookup"><span data-stu-id="ffc02-143">-Name</span></span>
<span data-ttu-id="ffc02-144">인증서의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffc02-144">Specifies the name of the certificate.</span></span>

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

### <span data-ttu-id="ffc02-145">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ffc02-145">-PassThru</span></span>
<span data-ttu-id="ffc02-146">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffc02-146">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ffc02-147">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ffc02-147">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ffc02-148">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="ffc02-148">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="ffc02-149">인증서 갱신에 대 한 자동 프로세스가 시작 되는 만료 이전의 일 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffc02-149">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="ffc02-150">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="ffc02-150">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="ffc02-151">인증서 갱신에 대 한 자동 프로세스가 시작 되는 수명의 백분율을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffc02-151">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="ffc02-152">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="ffc02-152">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="ffc02-153">갱신 하는 동안 인증서가 키를 다시 사용 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ffc02-153">Indicates that the certificate reuse the key during renewal.</span></span>

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

### <span data-ttu-id="ffc02-154">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="ffc02-154">-SecretContentType</span></span>
<span data-ttu-id="ffc02-155">새 키 보관소 비밀의 콘텐츠 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffc02-155">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="ffc02-156">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="ffc02-156">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ffc02-157">application/x-pkcs12</span><span class="sxs-lookup"><span data-stu-id="ffc02-157">application/x-pkcs12</span></span>
- <span data-ttu-id="ffc02-158">application/x-pem-파일</span><span class="sxs-lookup"><span data-stu-id="ffc02-158">application/x-pem-file</span></span>

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

### <span data-ttu-id="ffc02-159">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="ffc02-159">-SubjectName</span></span>
<span data-ttu-id="ffc02-160">인증서의 주체 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffc02-160">Specifies the subject name of the certificate.</span></span>

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

### <span data-ttu-id="ffc02-161">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="ffc02-161">-ValidityInMonths</span></span>
<span data-ttu-id="ffc02-162">인증서가 유효한 개월 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffc02-162">Specifies the number of months the certificate is valid.</span></span>

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

### <span data-ttu-id="ffc02-163">-VaultName</span><span class="sxs-lookup"><span data-stu-id="ffc02-163">-VaultName</span></span>
<span data-ttu-id="ffc02-164">키 보관소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffc02-164">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="ffc02-165">-확인</span><span class="sxs-lookup"><span data-stu-id="ffc02-165">-Confirm</span></span>
<span data-ttu-id="ffc02-166">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffc02-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ffc02-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ffc02-167">-WhatIf</span></span>
<span data-ttu-id="ffc02-168">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ffc02-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ffc02-169">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ffc02-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ffc02-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffc02-170">CommonParameters</span></span>
<span data-ttu-id="ffc02-171">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffc02-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffc02-172">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ffc02-172">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffc02-173">입력</span><span class="sxs-lookup"><span data-stu-id="ffc02-173">INPUTS</span></span>

### <span data-ttu-id="ffc02-174">Microsoft. KeyVault. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="ffc02-174">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="ffc02-175">출력</span><span class="sxs-lookup"><span data-stu-id="ffc02-175">OUTPUTS</span></span>

### <span data-ttu-id="ffc02-176">Microsoft. KeyVault. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="ffc02-176">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="ffc02-177">상속자</span><span class="sxs-lookup"><span data-stu-id="ffc02-177">NOTES</span></span>

## <span data-ttu-id="ffc02-178">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ffc02-178">RELATED LINKS</span></span>

[<span data-ttu-id="ffc02-179">Get-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="ffc02-179">Get-AzKeyVaultCertificatePolicy</span></span>](./Get-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="ffc02-180">새로운 AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="ffc02-180">New-AzKeyVaultCertificatePolicy</span></span>](./New-AzKeyVaultCertificatePolicy.md)

