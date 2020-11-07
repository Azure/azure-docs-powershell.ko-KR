---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 25E0F0E9-BF8C-49DF-87BA-31E2103A29A9
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/new-AzKeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: 83eea8c8a030c5d22368bc0ede42c71e92df14a2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875827"
---
# <span data-ttu-id="c9465-101">New-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="c9465-101">New-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="c9465-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9465-102">SYNOPSIS</span></span>
<span data-ttu-id="c9465-103">메모리 내 인증서 정책 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c9465-103">Creates an in-memory certificate policy object.</span></span>

## <span data-ttu-id="c9465-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c9465-104">SYNTAX</span></span>

```
New-AzKeyVaultCertificatePolicy [-SecretContentType <String>] [-ReuseKeyOnRenewal] [-Disabled]
 [-SubjectName <String>] [-DnsNames <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.String]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] -IssuerName <String>
 [-CertificateType <String>] [-RenewAtNumberOfDaysBeforeExpiry <Int32>] [-RenewAtPercentageLifetime <Int32>]
 [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>] [-KeyType <String>]
 [-KeyNotExportable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9465-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c9465-105">DESCRIPTION</span></span>
<span data-ttu-id="c9465-106">**AzKeyVaultCertificatePolicy** Cmdlet은 Azure 키 자격 증명 모음에 대 한 메모리 내 인증서 정책 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c9465-106">The **New-AzKeyVaultCertificatePolicy** cmdlet creates an in-memory certificate policy object for Azure Key Vault.</span></span>

## <span data-ttu-id="c9465-107">예제의</span><span class="sxs-lookup"><span data-stu-id="c9465-107">EXAMPLES</span></span>

### <span data-ttu-id="c9465-108">예제 1: 인증서 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="c9465-108">Example 1: Create a certificate policy</span></span>
```
PS C:\>New-AzKeyVaultCertificatePolicy -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal
```

<span data-ttu-id="c9465-109">이 명령은 6 개월 동안 유효한 인증서 정책을 만든 다음 키를 다시 사용할 수 있도록 하 여 인증서를 갱신 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9465-109">This command creates a certificate policy that is valid for six months and reuses the key to renew the certificate.</span></span>

## <span data-ttu-id="c9465-110">변수</span><span class="sxs-lookup"><span data-stu-id="c9465-110">PARAMETERS</span></span>

### <span data-ttu-id="c9465-111">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="c9465-111">-CertificateType</span></span>
<span data-ttu-id="c9465-112">발급자에 대 한 인증서 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9465-112">Specifies the type of certificate to the issuer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9465-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9465-113">-DefaultProfile</span></span>
<span data-ttu-id="c9465-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="c9465-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c9465-115">-사용 안 함</span><span class="sxs-lookup"><span data-stu-id="c9465-115">-Disabled</span></span>
<span data-ttu-id="c9465-116">인증서 정책을 사용할 수 없음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="c9465-116">Indicates that the certificate policy is disabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9465-117">-DnsNames</span><span class="sxs-lookup"><span data-stu-id="c9465-117">-DnsNames</span></span>
<span data-ttu-id="c9465-118">인증서의 DNS 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9465-118">Specifies the DNS names in the certificate.</span></span>

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

### <span data-ttu-id="c9465-119">-Eku</span><span class="sxs-lookup"><span data-stu-id="c9465-119">-Ekus</span></span>
<span data-ttu-id="c9465-120">인증서의 Eku (확장 된 키 용도)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9465-120">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

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

### <span data-ttu-id="c9465-121">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="c9465-121">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="c9465-122">만료 되기까지 자동 알림 프로세스가 시작 되는 날짜 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9465-122">Specifies how many days before expiry the automatic notification process begins.</span></span>

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

### <span data-ttu-id="c9465-123">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="c9465-123">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="c9465-124">알림의 자동 프로세스가 시작 되는 수명에 대 한 백분율을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9465-124">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="c9465-125">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="c9465-125">-IssuerName</span></span>
<span data-ttu-id="c9465-126">인증서 발급자의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9465-126">Specifies the name of the issuer for the certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9465-127">-KeyNotExportable 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c9465-127">-KeyNotExportable</span></span>
<span data-ttu-id="c9465-128">키를 내보낼 수 없음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="c9465-128">Indicates that the key is not exportable.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9465-129">-KeyType</span><span class="sxs-lookup"><span data-stu-id="c9465-129">-KeyType</span></span>
<span data-ttu-id="c9465-130">인증서를 지 원하는 키의 키 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9465-130">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="c9465-131">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="c9465-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c9465-132">RSA</span><span class="sxs-lookup"><span data-stu-id="c9465-132">RSA</span></span>
- <span data-ttu-id="c9465-133">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="c9465-133">RSA-HSM</span></span>

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

### <span data-ttu-id="c9465-134">-KeyUsage</span><span class="sxs-lookup"><span data-stu-id="c9465-134">-KeyUsage</span></span>
<span data-ttu-id="c9465-135">인증서의 키 용도를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9465-135">Specifies the key usages in the certificate.</span></span>

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

### <span data-ttu-id="c9465-136">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="c9465-136">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="c9465-137">인증서 갱신에 대 한 자동 프로세스가 시작 되는 만료 이전의 일 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9465-137">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="c9465-138">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="c9465-138">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="c9465-139">인증서 갱신에 대 한 자동 프로세스가 시작 되는 수명의 백분율을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9465-139">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="c9465-140">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="c9465-140">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="c9465-141">갱신 하는 동안 인증서가 키를 다시 사용 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="c9465-141">Indicates that the certificate reuse the key during renewal.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9465-142">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="c9465-142">-SecretContentType</span></span>
<span data-ttu-id="c9465-143">새 키 보관소 비밀의 콘텐츠 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9465-143">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="c9465-144">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="c9465-144">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c9465-145">application/x-pkcs12</span><span class="sxs-lookup"><span data-stu-id="c9465-145">application/x-pkcs12</span></span>
- <span data-ttu-id="c9465-146">application/x-pem-파일</span><span class="sxs-lookup"><span data-stu-id="c9465-146">application/x-pem-file</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: application/x-pkcs12, application/x-pem-file

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9465-147">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="c9465-147">-SubjectName</span></span>
<span data-ttu-id="c9465-148">인증서의 주체 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9465-148">Specifies the subject name of the certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9465-149">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="c9465-149">-ValidityInMonths</span></span>
<span data-ttu-id="c9465-150">인증서가 유효한 개월 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9465-150">Specifies the number of months the certificate is valid.</span></span>

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

### <span data-ttu-id="c9465-151">-확인</span><span class="sxs-lookup"><span data-stu-id="c9465-151">-Confirm</span></span>
<span data-ttu-id="c9465-152">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9465-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9465-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9465-153">-WhatIf</span></span>
<span data-ttu-id="c9465-154">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c9465-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9465-155">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c9465-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9465-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9465-156">CommonParameters</span></span>
<span data-ttu-id="c9465-157">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9465-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9465-158">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9465-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9465-159">입력</span><span class="sxs-lookup"><span data-stu-id="c9465-159">INPUTS</span></span>

### <span data-ttu-id="c9465-160">않아야</span><span class="sxs-lookup"><span data-stu-id="c9465-160">None</span></span>
<span data-ttu-id="c9465-161">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c9465-161">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c9465-162">출력</span><span class="sxs-lookup"><span data-stu-id="c9465-162">OUTPUTS</span></span>

### <span data-ttu-id="c9465-163">Microsoft. KeyVault. KeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="c9465-163">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="c9465-164">상속자</span><span class="sxs-lookup"><span data-stu-id="c9465-164">NOTES</span></span>

## <span data-ttu-id="c9465-165">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c9465-165">RELATED LINKS</span></span>

[<span data-ttu-id="c9465-166">Get-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="c9465-166">Get-AzKeyVaultCertificatePolicy</span></span>](./Get-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="c9465-167">Set-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="c9465-167">Set-AzKeyVaultCertificatePolicy</span></span>](./Set-AzKeyVaultCertificatePolicy.md)

