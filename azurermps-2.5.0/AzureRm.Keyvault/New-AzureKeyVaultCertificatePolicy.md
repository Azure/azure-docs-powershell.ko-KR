---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 25E0F0E9-BF8C-49DF-87BA-31E2103A29A9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/new-azurekeyvaultcertificatepolicy
schema: 2.0.0
ms.openlocfilehash: b10dd0e034db53af35c930ce1c4588dee2576c75
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93881078"
---
# <span data-ttu-id="67578-101">New-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="67578-101">New-AzureKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="67578-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67578-102">SYNOPSIS</span></span>
<span data-ttu-id="67578-103">메모리 내 인증서 정책 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="67578-103">Creates an in-memory certificate policy object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="67578-104">구문과</span><span class="sxs-lookup"><span data-stu-id="67578-104">SYNTAX</span></span>

```
New-AzureKeyVaultCertificatePolicy [-SecretContentType <String>] [-ReuseKeyOnRenewal] [-Disabled]
 [-SubjectName <String>] [-DnsNames <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.String]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] -IssuerName <String>
 [-CertificateType <String>] [-RenewAtNumberOfDaysBeforeExpiry <Int32>] [-RenewAtPercentageLifetime <Int32>]
 [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>] [-KeyType <String>]
 [-KeyNotExportable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67578-105">설명은</span><span class="sxs-lookup"><span data-stu-id="67578-105">DESCRIPTION</span></span>
<span data-ttu-id="67578-106">**AzureKeyVaultCertificatePolicy** Cmdlet은 Azure 키 자격 증명 모음에 대 한 메모리 내 인증서 정책 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="67578-106">The **New-AzureKeyVaultCertificatePolicy** cmdlet creates an in-memory certificate policy object for Azure Key Vault.</span></span>

## <span data-ttu-id="67578-107">예제의</span><span class="sxs-lookup"><span data-stu-id="67578-107">EXAMPLES</span></span>

### <span data-ttu-id="67578-108">예제 1: 인증서 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="67578-108">Example 1: Create a certificate policy</span></span>
```
PS C:\>New-AzureKeyVaultCertificatePolicy -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal
```

<span data-ttu-id="67578-109">이 명령은 6 개월 동안 유효한 인증서 정책을 만든 다음 키를 다시 사용할 수 있도록 하 여 인증서를 갱신 합니다.</span><span class="sxs-lookup"><span data-stu-id="67578-109">This command creates a certificate policy that is valid for six months and reuses the key to renew the certificate.</span></span>

## <span data-ttu-id="67578-110">변수</span><span class="sxs-lookup"><span data-stu-id="67578-110">PARAMETERS</span></span>

### <span data-ttu-id="67578-111">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="67578-111">-CertificateType</span></span>
<span data-ttu-id="67578-112">발급자에 대 한 인증서 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="67578-112">Specifies the type of certificate to the issuer.</span></span>

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

### <span data-ttu-id="67578-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67578-113">-DefaultProfile</span></span>
<span data-ttu-id="67578-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="67578-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="67578-115">-사용 안 함</span><span class="sxs-lookup"><span data-stu-id="67578-115">-Disabled</span></span>
<span data-ttu-id="67578-116">인증서 정책을 사용할 수 없음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="67578-116">Indicates that the certificate policy is disabled.</span></span>

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

### <span data-ttu-id="67578-117">-DnsNames</span><span class="sxs-lookup"><span data-stu-id="67578-117">-DnsNames</span></span>
<span data-ttu-id="67578-118">인증서의 DNS 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="67578-118">Specifies the DNS names in the certificate.</span></span>

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

### <span data-ttu-id="67578-119">-Eku</span><span class="sxs-lookup"><span data-stu-id="67578-119">-Ekus</span></span>
<span data-ttu-id="67578-120">인증서의 Eku (확장 된 키 용도)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="67578-120">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

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

### <span data-ttu-id="67578-121">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="67578-121">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="67578-122">만료 되기까지 자동 알림 프로세스가 시작 되는 날짜 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="67578-122">Specifies how many days before expiry the automatic notification process begins.</span></span>

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

### <span data-ttu-id="67578-123">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="67578-123">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="67578-124">알림의 자동 프로세스가 시작 되는 수명에 대 한 백분율을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="67578-124">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="67578-125">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="67578-125">-IssuerName</span></span>
<span data-ttu-id="67578-126">인증서 발급자의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="67578-126">Specifies the name of the issuer for the certificate.</span></span>

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

### <span data-ttu-id="67578-127">-KeyNotExportable 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="67578-127">-KeyNotExportable</span></span>
<span data-ttu-id="67578-128">키를 내보낼 수 없음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="67578-128">Indicates that the key is not exportable.</span></span>

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

### <span data-ttu-id="67578-129">-KeyType</span><span class="sxs-lookup"><span data-stu-id="67578-129">-KeyType</span></span>
<span data-ttu-id="67578-130">인증서를 지 원하는 키의 키 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="67578-130">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="67578-131">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="67578-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="67578-132">RSA</span><span class="sxs-lookup"><span data-stu-id="67578-132">RSA</span></span>
- <span data-ttu-id="67578-133">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="67578-133">RSA-HSM</span></span>

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

### <span data-ttu-id="67578-134">-KeyUsage</span><span class="sxs-lookup"><span data-stu-id="67578-134">-KeyUsage</span></span>
<span data-ttu-id="67578-135">인증서의 키 용도를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="67578-135">Specifies the key usages in the certificate.</span></span>

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

### <span data-ttu-id="67578-136">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="67578-136">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="67578-137">인증서 갱신에 대 한 자동 프로세스가 시작 되는 만료 이전의 일 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="67578-137">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="67578-138">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="67578-138">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="67578-139">인증서 갱신에 대 한 자동 프로세스가 시작 되는 수명의 백분율을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="67578-139">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="67578-140">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="67578-140">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="67578-141">갱신 하는 동안 인증서가 키를 다시 사용 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="67578-141">Indicates that the certificate reuse the key during renewal.</span></span>

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

### <span data-ttu-id="67578-142">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="67578-142">-SecretContentType</span></span>
<span data-ttu-id="67578-143">새 키 보관소 비밀의 콘텐츠 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="67578-143">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="67578-144">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="67578-144">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="67578-145">application/x-pkcs12</span><span class="sxs-lookup"><span data-stu-id="67578-145">application/x-pkcs12</span></span>
- <span data-ttu-id="67578-146">application/x-pem-파일</span><span class="sxs-lookup"><span data-stu-id="67578-146">application/x-pem-file</span></span>

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

### <span data-ttu-id="67578-147">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="67578-147">-SubjectName</span></span>
<span data-ttu-id="67578-148">인증서의 주체 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="67578-148">Specifies the subject name of the certificate.</span></span>

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

### <span data-ttu-id="67578-149">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="67578-149">-ValidityInMonths</span></span>
<span data-ttu-id="67578-150">인증서가 유효한 개월 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="67578-150">Specifies the number of months the certificate is valid.</span></span>

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

### <span data-ttu-id="67578-151">-확인</span><span class="sxs-lookup"><span data-stu-id="67578-151">-Confirm</span></span>
<span data-ttu-id="67578-152">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="67578-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67578-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67578-153">-WhatIf</span></span>
<span data-ttu-id="67578-154">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="67578-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67578-155">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="67578-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67578-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67578-156">CommonParameters</span></span>
<span data-ttu-id="67578-157">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="67578-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67578-158">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67578-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67578-159">입력</span><span class="sxs-lookup"><span data-stu-id="67578-159">INPUTS</span></span>

## <span data-ttu-id="67578-160">출력</span><span class="sxs-lookup"><span data-stu-id="67578-160">OUTPUTS</span></span>

### <span data-ttu-id="67578-161">Microsoft. KeyVault. KeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="67578-161">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="67578-162">상속자</span><span class="sxs-lookup"><span data-stu-id="67578-162">NOTES</span></span>

## <span data-ttu-id="67578-163">관련 링크</span><span class="sxs-lookup"><span data-stu-id="67578-163">RELATED LINKS</span></span>

[<span data-ttu-id="67578-164">Get-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="67578-164">Get-AzureKeyVaultCertificatePolicy</span></span>](./Get-AzureKeyVaultCertificatePolicy.md)

[<span data-ttu-id="67578-165">Set-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="67578-165">Set-AzureKeyVaultCertificatePolicy</span></span>](./Set-AzureKeyVaultCertificatePolicy.md)

