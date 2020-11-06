---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 25E0F0E9-BF8C-49DF-87BA-31E2103A29A9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureKeyVaultCertificatePolicy.md
ms.openlocfilehash: 381ce302a8404c0bb643db0fc82e392fe53d956a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527528"
---
# <span data-ttu-id="c3054-101">New-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="c3054-101">New-AzureKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="c3054-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3054-102">SYNOPSIS</span></span>
<span data-ttu-id="c3054-103">메모리 내 인증서 정책 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c3054-103">Creates an in-memory certificate policy object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c3054-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c3054-104">SYNTAX</span></span>

```
New-AzureKeyVaultCertificatePolicy [-SecretContentType <String>] [-ReuseKeyOnRenewal] [-Disabled]
 [-SubjectName <String>] [-DnsNames <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.String]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] -IssuerName <String>
 [-CertificateType <String>] [-RenewAtNumberOfDaysBeforeExpiry <Int32>] [-RenewAtPercentageLifetime <Int32>]
 [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>] [-KeyType <String>]
 [-KeyNotExportable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3054-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c3054-105">DESCRIPTION</span></span>
<span data-ttu-id="c3054-106">**AzureKeyVaultCertificatePolicy** Cmdlet은 Azure 키 자격 증명 모음에 대 한 메모리 내 인증서 정책 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c3054-106">The **New-AzureKeyVaultCertificatePolicy** cmdlet creates an in-memory certificate policy object for Azure Key Vault.</span></span>

## <span data-ttu-id="c3054-107">예제의</span><span class="sxs-lookup"><span data-stu-id="c3054-107">EXAMPLES</span></span>

### <span data-ttu-id="c3054-108">예제 1: 인증서 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="c3054-108">Example 1: Create a certificate policy</span></span>
```
PS C:\>New-AzureKeyVaultCertificatePolicy -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal
```

<span data-ttu-id="c3054-109">이 명령은 6 개월 동안 유효한 인증서 정책을 만든 다음 키를 다시 사용할 수 있도록 하 여 인증서를 갱신 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3054-109">This command creates a certificate policy that is valid for six months and reuses the key to renew the certificate.</span></span>

## <span data-ttu-id="c3054-110">변수</span><span class="sxs-lookup"><span data-stu-id="c3054-110">PARAMETERS</span></span>

### <span data-ttu-id="c3054-111">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="c3054-111">-CertificateType</span></span>
<span data-ttu-id="c3054-112">발급자에 대 한 인증서 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3054-112">Specifies the type of certificate to the issuer.</span></span>

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

### <span data-ttu-id="c3054-113">-사용 안 함</span><span class="sxs-lookup"><span data-stu-id="c3054-113">-Disabled</span></span>
<span data-ttu-id="c3054-114">인증서 정책을 사용할 수 없음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="c3054-114">Indicates that the certificate policy is disabled.</span></span>

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

### <span data-ttu-id="c3054-115">-DnsNames</span><span class="sxs-lookup"><span data-stu-id="c3054-115">-DnsNames</span></span>
<span data-ttu-id="c3054-116">인증서의 DNS 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3054-116">Specifies the DNS names in the certificate.</span></span>

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

### <span data-ttu-id="c3054-117">-Eku</span><span class="sxs-lookup"><span data-stu-id="c3054-117">-Ekus</span></span>
<span data-ttu-id="c3054-118">인증서의 Eku (확장 된 키 용도)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3054-118">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

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

### <span data-ttu-id="c3054-119">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="c3054-119">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="c3054-120">만료 되기까지 자동 알림 프로세스가 시작 되는 날짜 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3054-120">Specifies how many days before expiry the automatic notification process begins.</span></span>

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

### <span data-ttu-id="c3054-121">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="c3054-121">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="c3054-122">알림의 자동 프로세스가 시작 되는 수명에 대 한 백분율을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3054-122">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="c3054-123">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="c3054-123">-IssuerName</span></span>
<span data-ttu-id="c3054-124">인증서 발급자의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3054-124">Specifies the name of the issuer for the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3054-125">-KeyNotExportable 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c3054-125">-KeyNotExportable</span></span>
<span data-ttu-id="c3054-126">키를 내보낼 수 없음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="c3054-126">Indicates that the key is not exportable.</span></span>

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

### <span data-ttu-id="c3054-127">-KeyType</span><span class="sxs-lookup"><span data-stu-id="c3054-127">-KeyType</span></span>
<span data-ttu-id="c3054-128">인증서를 지 원하는 키의 키 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3054-128">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="c3054-129">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="c3054-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c3054-130">RSA</span><span class="sxs-lookup"><span data-stu-id="c3054-130">RSA</span></span>
- <span data-ttu-id="c3054-131">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="c3054-131">RSA-HSM</span></span>

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

### <span data-ttu-id="c3054-132">-KeyUsage</span><span class="sxs-lookup"><span data-stu-id="c3054-132">-KeyUsage</span></span>
<span data-ttu-id="c3054-133">인증서의 키 용도를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3054-133">Specifies the key usages in the certificate.</span></span>

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

### <span data-ttu-id="c3054-134">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="c3054-134">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="c3054-135">인증서 갱신에 대 한 자동 프로세스가 시작 되는 만료 이전의 일 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3054-135">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="c3054-136">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="c3054-136">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="c3054-137">인증서 갱신에 대 한 자동 프로세스가 시작 되는 수명의 백분율을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3054-137">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="c3054-138">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="c3054-138">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="c3054-139">갱신 하는 동안 인증서가 키를 다시 사용 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="c3054-139">Indicates that the certificate reuse the key during renewal.</span></span>

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

### <span data-ttu-id="c3054-140">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="c3054-140">-SecretContentType</span></span>
<span data-ttu-id="c3054-141">새 키 보관소 비밀의 콘텐츠 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3054-141">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="c3054-142">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="c3054-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c3054-143">application/x-pkcs12</span><span class="sxs-lookup"><span data-stu-id="c3054-143">application/x-pkcs12</span></span>
- <span data-ttu-id="c3054-144">application/x-pem-파일</span><span class="sxs-lookup"><span data-stu-id="c3054-144">application/x-pem-file</span></span>

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

### <span data-ttu-id="c3054-145">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="c3054-145">-SubjectName</span></span>
<span data-ttu-id="c3054-146">인증서의 주체 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3054-146">Specifies the subject name of the certificate.</span></span>

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

### <span data-ttu-id="c3054-147">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="c3054-147">-ValidityInMonths</span></span>
<span data-ttu-id="c3054-148">인증서가 유효한 개월 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3054-148">Specifies the number of months the certificate is valid.</span></span>

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

### <span data-ttu-id="c3054-149">-확인</span><span class="sxs-lookup"><span data-stu-id="c3054-149">-Confirm</span></span>
<span data-ttu-id="c3054-150">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3054-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3054-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3054-151">-WhatIf</span></span>
<span data-ttu-id="c3054-152">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c3054-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3054-153">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c3054-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3054-154">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3054-154">-DefaultProfile</span></span>
<span data-ttu-id="c3054-155">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c3054-155">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c3054-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3054-156">CommonParameters</span></span>
<span data-ttu-id="c3054-157">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3054-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3054-158">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3054-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3054-159">입력</span><span class="sxs-lookup"><span data-stu-id="c3054-159">INPUTS</span></span>

## <span data-ttu-id="c3054-160">출력</span><span class="sxs-lookup"><span data-stu-id="c3054-160">OUTPUTS</span></span>

### <span data-ttu-id="c3054-161">Microsoft. KeyVault. KeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="c3054-161">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="c3054-162">상속자</span><span class="sxs-lookup"><span data-stu-id="c3054-162">NOTES</span></span>

## <span data-ttu-id="c3054-163">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c3054-163">RELATED LINKS</span></span>

[<span data-ttu-id="c3054-164">Get-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="c3054-164">Get-AzureKeyVaultCertificatePolicy</span></span>](./Get-AzureKeyVaultCertificatePolicy.md)

[<span data-ttu-id="c3054-165">Set-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="c3054-165">Set-AzureKeyVaultCertificatePolicy</span></span>](./Set-AzureKeyVaultCertificatePolicy.md)

