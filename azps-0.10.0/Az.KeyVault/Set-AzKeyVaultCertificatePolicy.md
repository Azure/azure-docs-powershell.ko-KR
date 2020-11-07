---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 28BC1B99-946C-4A8D-9581-4D5CC0BCEF8B
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/set-AzKeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: 160c98b141dbde36786404b58c694772dc86d323
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876693"
---
# <span data-ttu-id="3ce0f-101">Set-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="3ce0f-101">Set-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="3ce0f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ce0f-102">SYNOPSIS</span></span>
<span data-ttu-id="3ce0f-103">키 자격 증명 모음에서 인증서에 대 한 정책을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ce0f-103">Creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="3ce0f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3ce0f-104">SYNTAX</span></span>

### <span data-ttu-id="3ce0f-105">확장 됨 (기본값)</span><span class="sxs-lookup"><span data-stu-id="3ce0f-105">Expanded (Default)</span></span>
```
Set-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String> [-SecretContentType <String>]
 [-ReuseKeyOnRenewal <Boolean>] [-Disabled] [-SubjectName <String>]
 [-DnsNames <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.String]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] [-IssuerName <String>]
 [-CertificateType <String>] [-RenewAtNumberOfDaysBeforeExpiry <Int32>] [-RenewAtPercentageLifetime <Int32>]
 [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>] [-KeyType <String>]
 [-KeyNotExportable] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3ce0f-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="3ce0f-106">ByValue</span></span>
```
Set-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>] [-KeyType <String>]
 [[-CertificatePolicy] <KeyVaultCertificatePolicy>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ce0f-107">설명은</span><span class="sxs-lookup"><span data-stu-id="3ce0f-107">DESCRIPTION</span></span>
<span data-ttu-id="3ce0f-108">**AzKeyVaultCertificatePolicy** cmdlet은 키 자격 증명 모음에서 인증서에 대 한 정책을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ce0f-108">The **Set-AzKeyVaultCertificatePolicy** cmdlet creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="3ce0f-109">예제의</span><span class="sxs-lookup"><span data-stu-id="3ce0f-109">EXAMPLES</span></span>

### <span data-ttu-id="3ce0f-110">예제 1: 인증서 정책 설정</span><span class="sxs-lookup"><span data-stu-id="3ce0f-110">Example 1: Set a certificate policy</span></span>
```
PS C:\>Set-AzKeyVaultCertificatePolicy -VaultName "ContosoKV01" -Name "TestCert01" -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal $True
```

<span data-ttu-id="3ce0f-111">이 명령은 ContosoKV01 키 자격 증명 모음의 TestCert01 인증서에 대 한 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ce0f-111">This command sets the policy for the TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="3ce0f-112">변수</span><span class="sxs-lookup"><span data-stu-id="3ce0f-112">PARAMETERS</span></span>

### <span data-ttu-id="3ce0f-113">-CertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="3ce0f-113">-CertificatePolicy</span></span>
<span data-ttu-id="3ce0f-114">인증서 정책을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ce0f-114">Specifies the certificate policy.</span></span>

```yaml
Type: KeyVaultCertificatePolicy
Parameter Sets: ByValue
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ce0f-115">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="3ce0f-115">-CertificateType</span></span>
<span data-ttu-id="3ce0f-116">발급자에 대 한 인증서 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ce0f-116">Specifies the type of certificate to the issuer.</span></span>

```yaml
Type: String
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ce0f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ce0f-117">-DefaultProfile</span></span>
<span data-ttu-id="3ce0f-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="3ce0f-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ce0f-119">-사용 안 함</span><span class="sxs-lookup"><span data-stu-id="3ce0f-119">-Disabled</span></span>
<span data-ttu-id="3ce0f-120">인증서 정책을 사용할 수 없음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="3ce0f-120">Indicates that the certificate policy is disabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ce0f-121">-DnsNames</span><span class="sxs-lookup"><span data-stu-id="3ce0f-121">-DnsNames</span></span>
<span data-ttu-id="3ce0f-122">인증서의 DNS 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ce0f-122">Specifies the DNS names in the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ce0f-123">-Eku</span><span class="sxs-lookup"><span data-stu-id="3ce0f-123">-Ekus</span></span>
<span data-ttu-id="3ce0f-124">인증서의 Eku (확장 된 키 용도)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ce0f-124">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ce0f-125">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="3ce0f-125">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="3ce0f-126">만료 되기까지 자동 알림 프로세스가 시작 되는 날짜 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ce0f-126">Specifies how many days before expiry the automatic notification process begins.</span></span>

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

### <span data-ttu-id="3ce0f-127">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="3ce0f-127">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="3ce0f-128">알림의 자동 프로세스가 시작 되는 수명에 대 한 백분율을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ce0f-128">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="3ce0f-129">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="3ce0f-129">-IssuerName</span></span>
<span data-ttu-id="3ce0f-130">이 인증서에 대 한 발급자의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ce0f-130">Specifies the name of the issuer for this certificate.</span></span>

```yaml
Type: String
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ce0f-131">-KeyNotExportable 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3ce0f-131">-KeyNotExportable</span></span>
<span data-ttu-id="3ce0f-132">키를 내보낼 수 없음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="3ce0f-132">Indicates that the key is not exportable.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ce0f-133">-KeyType</span><span class="sxs-lookup"><span data-stu-id="3ce0f-133">-KeyType</span></span>
<span data-ttu-id="3ce0f-134">인증서를 지 원하는 키의 키 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ce0f-134">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="3ce0f-135">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="3ce0f-135">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3ce0f-136">RSA</span><span class="sxs-lookup"><span data-stu-id="3ce0f-136">RSA</span></span>
- <span data-ttu-id="3ce0f-137">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="3ce0f-137">RSA-HSM</span></span>

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

### <span data-ttu-id="3ce0f-138">-KeyUsage</span><span class="sxs-lookup"><span data-stu-id="3ce0f-138">-KeyUsage</span></span>
<span data-ttu-id="3ce0f-139">인증서의 키 용도를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ce0f-139">Specifies the key usages in the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ce0f-140">-이름</span><span class="sxs-lookup"><span data-stu-id="3ce0f-140">-Name</span></span>
<span data-ttu-id="3ce0f-141">인증서의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ce0f-141">Specifies the name of the certificate.</span></span>

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

### <span data-ttu-id="3ce0f-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3ce0f-142">-PassThru</span></span>
<span data-ttu-id="3ce0f-143">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ce0f-143">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="3ce0f-144">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3ce0f-144">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3ce0f-145">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="3ce0f-145">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="3ce0f-146">인증서 갱신에 대 한 자동 프로세스가 시작 되는 만료 이전의 일 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ce0f-146">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

```yaml
Type: Int32
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ce0f-147">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="3ce0f-147">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="3ce0f-148">인증서 갱신에 대 한 자동 프로세스가 시작 되는 수명의 백분율을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ce0f-148">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

```yaml
Type: Int32
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ce0f-149">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="3ce0f-149">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="3ce0f-150">갱신 하는 동안 인증서가 키를 다시 사용 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="3ce0f-150">Indicates that the certificate reuse the key during renewal.</span></span>

```yaml
Type: Boolean
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ce0f-151">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="3ce0f-151">-SecretContentType</span></span>
<span data-ttu-id="3ce0f-152">새 키 보관소 비밀의 콘텐츠 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ce0f-152">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="3ce0f-153">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="3ce0f-153">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3ce0f-154">application/x-pkcs12</span><span class="sxs-lookup"><span data-stu-id="3ce0f-154">application/x-pkcs12</span></span>
- <span data-ttu-id="3ce0f-155">application/x-pem-파일</span><span class="sxs-lookup"><span data-stu-id="3ce0f-155">application/x-pem-file</span></span>

```yaml
Type: String
Parameter Sets: Expanded
Aliases: 
Accepted values: application/x-pkcs12, application/x-pem-file

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ce0f-156">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="3ce0f-156">-SubjectName</span></span>
<span data-ttu-id="3ce0f-157">인증서의 주체 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ce0f-157">Specifies the subject name of the certificate.</span></span>

```yaml
Type: String
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ce0f-158">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="3ce0f-158">-ValidityInMonths</span></span>
<span data-ttu-id="3ce0f-159">인증서가 유효한 개월 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ce0f-159">Specifies the number of months the certificate is valid.</span></span>

```yaml
Type: Int32
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ce0f-160">-VaultName</span><span class="sxs-lookup"><span data-stu-id="3ce0f-160">-VaultName</span></span>
<span data-ttu-id="3ce0f-161">키 보관소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ce0f-161">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="3ce0f-162">-확인</span><span class="sxs-lookup"><span data-stu-id="3ce0f-162">-Confirm</span></span>
<span data-ttu-id="3ce0f-163">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ce0f-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ce0f-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ce0f-164">-WhatIf</span></span>
<span data-ttu-id="3ce0f-165">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="3ce0f-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ce0f-166">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3ce0f-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ce0f-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ce0f-167">CommonParameters</span></span>
<span data-ttu-id="3ce0f-168">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ce0f-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ce0f-169">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ce0f-169">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ce0f-170">입력</span><span class="sxs-lookup"><span data-stu-id="3ce0f-170">INPUTS</span></span>

### <span data-ttu-id="3ce0f-171">않아야</span><span class="sxs-lookup"><span data-stu-id="3ce0f-171">None</span></span>
<span data-ttu-id="3ce0f-172">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3ce0f-172">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3ce0f-173">출력</span><span class="sxs-lookup"><span data-stu-id="3ce0f-173">OUTPUTS</span></span>

### <span data-ttu-id="3ce0f-174">Microsoft. KeyVault. KeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="3ce0f-174">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="3ce0f-175">상속자</span><span class="sxs-lookup"><span data-stu-id="3ce0f-175">NOTES</span></span>

## <span data-ttu-id="3ce0f-176">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3ce0f-176">RELATED LINKS</span></span>

[<span data-ttu-id="3ce0f-177">Get-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="3ce0f-177">Get-AzKeyVaultCertificatePolicy</span></span>](./Get-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="3ce0f-178">새로운 AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="3ce0f-178">New-AzKeyVaultCertificatePolicy</span></span>](./New-AzKeyVaultCertificatePolicy.md)

