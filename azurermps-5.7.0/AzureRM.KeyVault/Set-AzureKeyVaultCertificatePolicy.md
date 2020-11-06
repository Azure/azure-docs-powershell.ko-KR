---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 28BC1B99-946C-4A8D-9581-4D5CC0BCEF8B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificatePolicy.md
ms.openlocfilehash: e960aa211b53c79087e67e2bd86504e597a718d5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536779"
---
# <span data-ttu-id="64aef-101">Set-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="64aef-101">Set-AzureKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="64aef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64aef-102">SYNOPSIS</span></span>
<span data-ttu-id="64aef-103">키 자격 증명 모음에서 인증서에 대 한 정책을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="64aef-103">Creates or updates the policy for a certificate in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="64aef-104">구문과</span><span class="sxs-lookup"><span data-stu-id="64aef-104">SYNTAX</span></span>

### <span data-ttu-id="64aef-105">ExpandedRenewPercentage (기본값)</span><span class="sxs-lookup"><span data-stu-id="64aef-105">ExpandedRenewPercentage (Default)</span></span>
```
Set-AzureKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String> [-RenewAtPercentageLifetime <Int32>]
 [-SecretContentType <String>] [-ReuseKeyOnRenewal <Boolean>] [-Disabled] [-SubjectName <String>]
 [-DnsName <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.String]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] [-IssuerName <String>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeyNotExportable] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64aef-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="64aef-106">ByValue</span></span>
```
Set-AzureKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-InputObject] <PSKeyVaultCertificatePolicy> [-EmailAtNumberOfDaysBeforeExpiry <Int32>]
 [-EmailAtPercentageLifetime <Int32>] [-KeyType <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64aef-107">ExpandedRenewNumber</span><span class="sxs-lookup"><span data-stu-id="64aef-107">ExpandedRenewNumber</span></span>
```
Set-AzureKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 -RenewAtNumberOfDaysBeforeExpiry <Int32> [-SecretContentType <String>] [-ReuseKeyOnRenewal <Boolean>]
 [-Disabled] [-SubjectName <String>] [-DnsName <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.String]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] [-IssuerName <String>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeyNotExportable] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64aef-108">설명은</span><span class="sxs-lookup"><span data-stu-id="64aef-108">DESCRIPTION</span></span>
<span data-ttu-id="64aef-109">**AzureKeyVaultCertificatePolicy** cmdlet은 키 자격 증명 모음에서 인증서에 대 한 정책을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="64aef-109">The **Set-AzureKeyVaultCertificatePolicy** cmdlet creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="64aef-110">예제의</span><span class="sxs-lookup"><span data-stu-id="64aef-110">EXAMPLES</span></span>

### <span data-ttu-id="64aef-111">예제 1: 인증서 정책 설정</span><span class="sxs-lookup"><span data-stu-id="64aef-111">Example 1: Set a certificate policy</span></span>
```
PS C:\>Set-AzureKeyVaultCertificatePolicy -VaultName "ContosoKV01" -Name "TestCert01" -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal $True
```

<span data-ttu-id="64aef-112">이 명령은 ContosoKV01 키 자격 증명 모음의 TestCert01 인증서에 대 한 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="64aef-112">This command sets the policy for the TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="64aef-113">변수</span><span class="sxs-lookup"><span data-stu-id="64aef-113">PARAMETERS</span></span>

### <span data-ttu-id="64aef-114">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="64aef-114">-CertificateType</span></span>
<span data-ttu-id="64aef-115">발급자에 대 한 인증서 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="64aef-115">Specifies the type of certificate to the issuer.</span></span>

```yaml
Type: String
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64aef-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64aef-116">-DefaultProfile</span></span>
<span data-ttu-id="64aef-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="64aef-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="64aef-118">-사용 안 함</span><span class="sxs-lookup"><span data-stu-id="64aef-118">-Disabled</span></span>
<span data-ttu-id="64aef-119">인증서 정책을 사용할 수 없음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="64aef-119">Indicates that the certificate policy is disabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64aef-120">-DnsName</span><span class="sxs-lookup"><span data-stu-id="64aef-120">-DnsName</span></span>
<span data-ttu-id="64aef-121">인증서의 주체 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="64aef-121">Specifies the subject name of the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases: DnsNames

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64aef-122">-Eku</span><span class="sxs-lookup"><span data-stu-id="64aef-122">-Ekus</span></span>
<span data-ttu-id="64aef-123">인증서의 Eku (확장 된 키 용도)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="64aef-123">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64aef-124">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="64aef-124">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="64aef-125">자동 갱신이 시작 될 때까지 만료 되기까지 남은 일 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="64aef-125">Specifies the number of days before expiration when automatic renewal should start.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64aef-126">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="64aef-126">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="64aef-127">알림의 자동 프로세스가 시작 되는 수명에 대 한 백분율을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="64aef-127">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64aef-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="64aef-128">-InputObject</span></span>
<span data-ttu-id="64aef-129">인증서 정책을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="64aef-129">Specifies the certificate policy.</span></span>

```yaml
Type: PSKeyVaultCertificatePolicy
Parameter Sets: ByValue
Aliases: CertificatePolicy

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="64aef-130">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="64aef-130">-IssuerName</span></span>
<span data-ttu-id="64aef-131">이 인증서에 대 한 발급자의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="64aef-131">Specifies the name of the issuer for this certificate.</span></span>

```yaml
Type: String
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64aef-132">-KeyNotExportable 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="64aef-132">-KeyNotExportable</span></span>
<span data-ttu-id="64aef-133">키를 내보낼 수 없음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="64aef-133">Indicates that the key is not exportable.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64aef-134">-KeyType</span><span class="sxs-lookup"><span data-stu-id="64aef-134">-KeyType</span></span>
<span data-ttu-id="64aef-135">인증서를 지 원하는 키의 키 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="64aef-135">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="64aef-136">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="64aef-136">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="64aef-137">RSA</span><span class="sxs-lookup"><span data-stu-id="64aef-137">RSA</span></span>
- <span data-ttu-id="64aef-138">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="64aef-138">RSA-HSM</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: RSA, RSA-HSM

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64aef-139">-KeyUsage</span><span class="sxs-lookup"><span data-stu-id="64aef-139">-KeyUsage</span></span>
<span data-ttu-id="64aef-140">인증서의 키 용도를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="64aef-140">Specifies the key usages in the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64aef-141">-이름</span><span class="sxs-lookup"><span data-stu-id="64aef-141">-Name</span></span>
<span data-ttu-id="64aef-142">인증서의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="64aef-142">Specifies the name of the certificate.</span></span>

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

### <span data-ttu-id="64aef-143">-PassThru</span><span class="sxs-lookup"><span data-stu-id="64aef-143">-PassThru</span></span>
<span data-ttu-id="64aef-144">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="64aef-144">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="64aef-145">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="64aef-145">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64aef-146">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="64aef-146">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="64aef-147">인증서 갱신에 대 한 자동 프로세스가 시작 되는 만료 이전의 일 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="64aef-147">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

```yaml
Type: Int32
Parameter Sets: ExpandedRenewNumber
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64aef-148">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="64aef-148">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="64aef-149">인증서 갱신에 대 한 자동 프로세스가 시작 되는 수명의 백분율을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="64aef-149">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

```yaml
Type: Int32
Parameter Sets: ExpandedRenewPercentage
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64aef-150">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="64aef-150">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="64aef-151">갱신 하는 동안 인증서가 키를 다시 사용 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="64aef-151">Indicates that the certificate reuse the key during renewal.</span></span>

```yaml
Type: Boolean
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64aef-152">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="64aef-152">-SecretContentType</span></span>
<span data-ttu-id="64aef-153">새 키 보관소 비밀의 콘텐츠 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="64aef-153">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="64aef-154">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="64aef-154">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="64aef-155">application/x-pkcs12</span><span class="sxs-lookup"><span data-stu-id="64aef-155">application/x-pkcs12</span></span>
- <span data-ttu-id="64aef-156">application/x-pem-파일</span><span class="sxs-lookup"><span data-stu-id="64aef-156">application/x-pem-file</span></span>

```yaml
Type: String
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:
Accepted values: application/x-pkcs12, application/x-pem-file

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64aef-157">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="64aef-157">-SubjectName</span></span>
<span data-ttu-id="64aef-158">인증서의 주체 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="64aef-158">Specifies the subject name of the certificate.</span></span>

```yaml
Type: String
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64aef-159">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="64aef-159">-ValidityInMonths</span></span>
<span data-ttu-id="64aef-160">인증서가 유효한 개월 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="64aef-160">Specifies the number of months the certificate is valid.</span></span>

```yaml
Type: Int32
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64aef-161">-VaultName</span><span class="sxs-lookup"><span data-stu-id="64aef-161">-VaultName</span></span>
<span data-ttu-id="64aef-162">키 보관소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="64aef-162">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="64aef-163">-확인</span><span class="sxs-lookup"><span data-stu-id="64aef-163">-Confirm</span></span>
<span data-ttu-id="64aef-164">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="64aef-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64aef-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64aef-165">-WhatIf</span></span>
<span data-ttu-id="64aef-166">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="64aef-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64aef-167">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="64aef-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64aef-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64aef-168">CommonParameters</span></span>
<span data-ttu-id="64aef-169">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="64aef-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64aef-170">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64aef-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64aef-171">입력</span><span class="sxs-lookup"><span data-stu-id="64aef-171">INPUTS</span></span>

### <span data-ttu-id="64aef-172">않아야</span><span class="sxs-lookup"><span data-stu-id="64aef-172">None</span></span>
<span data-ttu-id="64aef-173">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="64aef-173">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="64aef-174">출력</span><span class="sxs-lookup"><span data-stu-id="64aef-174">OUTPUTS</span></span>

### <span data-ttu-id="64aef-175">Microsoft. KeyVault. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="64aef-175">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="64aef-176">상속자</span><span class="sxs-lookup"><span data-stu-id="64aef-176">NOTES</span></span>

## <span data-ttu-id="64aef-177">관련 링크</span><span class="sxs-lookup"><span data-stu-id="64aef-177">RELATED LINKS</span></span>

[<span data-ttu-id="64aef-178">Get-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="64aef-178">Get-AzureKeyVaultCertificatePolicy</span></span>](./Get-AzureKeyVaultCertificatePolicy.md)

[<span data-ttu-id="64aef-179">새로운 AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="64aef-179">New-AzureKeyVaultCertificatePolicy</span></span>](./New-AzureKeyVaultCertificatePolicy.md)

