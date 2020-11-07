---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 9FC72DE9-46BB-4CB5-9880-F53756DBE012
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultSecret.md
ms.openlocfilehash: c7968d915ab28dca6bf595e5339d2681962ecdea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711424"
---
# <span data-ttu-id="78517-101">Set-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="78517-101">Set-AzureKeyVaultSecret</span></span>

## <span data-ttu-id="78517-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78517-102">SYNOPSIS</span></span>
<span data-ttu-id="78517-103">키 자격 증명 모음에서 비밀을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="78517-103">Creates or updates a secret in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="78517-104">구문과</span><span class="sxs-lookup"><span data-stu-id="78517-104">SYNTAX</span></span>

### <span data-ttu-id="78517-105">기본값 (기본값)</span><span class="sxs-lookup"><span data-stu-id="78517-105">Default (Default)</span></span>
```
Set-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [-SecretValue] <SecureString> [-Disable]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78517-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="78517-106">InputObject</span></span>
```
Set-AzureKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [-SecretValue] <SecureString> [-Disable]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78517-107">설명은</span><span class="sxs-lookup"><span data-stu-id="78517-107">DESCRIPTION</span></span>
<span data-ttu-id="78517-108">**AzureKeyVaultSecret** Cmdlet은 Azure key vault의 키 보관소에서 비밀을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="78517-108">The **Set-AzureKeyVaultSecret** cmdlet creates or updates a secret in a key vault in Azure Key Vault.</span></span> <span data-ttu-id="78517-109">비밀이 존재 하지 않는 경우이 cmdlet이이를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="78517-109">If the secret does not exist, this cmdlet creates it.</span></span> <span data-ttu-id="78517-110">비밀이 이미 있는 경우이 cmdlet은 해당 비밀의 새 버전을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="78517-110">If the secret already exists, this cmdlet creates a new version of that secret.</span></span>

## <span data-ttu-id="78517-111">예제의</span><span class="sxs-lookup"><span data-stu-id="78517-111">EXAMPLES</span></span>

### <span data-ttu-id="78517-112">예제 1: 기본 특성을 사용 하 여 비밀 값 수정</span><span class="sxs-lookup"><span data-stu-id="78517-112">Example 1: Modify the value of a secret using default attributes</span></span>
```
PS C:\> $Secret = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> Set-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -SecretValue $Secret
```

<span data-ttu-id="78517-113">첫 번째 명령은 **ConvertTo-SecureString** cmdlet을 사용 하 여 문자열을 보안 문자열로 변환한 다음 해당 문자열을 $Secret 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="78517-113">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Secret variable.</span></span> <span data-ttu-id="78517-114">자세한 내용은을 입력 `Get-Help
ConvertTo-SecureString` 하세요.</span><span class="sxs-lookup"><span data-stu-id="78517-114">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>

<span data-ttu-id="78517-115">두 번째 명령은 Contoso 라는 이름의 자격 증명 모음에서 ITSecret 라는 비밀 키의 값을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="78517-115">The second command modifies value of the secret named ITSecret in the key vault named Contoso.</span></span> <span data-ttu-id="78517-116">비밀 값이 $Secret에 저장 된 값이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="78517-116">The secret value becomes the value stored in $Secret.</span></span>

### <span data-ttu-id="78517-117">예제 2: 사용자 지정 특성을 사용 하 여 비밀 값 수정</span><span class="sxs-lookup"><span data-stu-id="78517-117">Example 2: Modify the value of a secret using custom attributes</span></span>
```
PS C:\> $Secret = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $NBF =(Get-Date).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'medium'; 'IT' = null }
PS C:\> $ContentType = 'txt'
PS C:\> Set-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -SecretValue $Secret -Expires $Expires -NotBefore $NBF -ContentType $ContentType -Disable $False -Tags $Tags
```

<span data-ttu-id="78517-118">첫 번째 명령은 **ConvertTo-SecureString** cmdlet을 사용 하 여 문자열을 보안 문자열로 변환한 다음 해당 문자열을 $Secret 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="78517-118">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Secret variable.</span></span> <span data-ttu-id="78517-119">자세한 내용은을 입력 `Get-Help
ConvertTo-SecureString` 하세요.</span><span class="sxs-lookup"><span data-stu-id="78517-119">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>

<span data-ttu-id="78517-120">다음 명령은 만료 날짜, 태그, 컨텍스트 형식에 대 한 사용자 지정 특성을 정의 하 고 변수에 특성을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="78517-120">The next commands define custom attributes for the expiry date, tags, and context type, and store the attributes in variables.</span></span>

<span data-ttu-id="78517-121">마지막 명령은 이전에 변수로 지정 된 값을 사용 하 여 Contoso 라는 키 보관소에 ITSecret 라는 비밀 값을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="78517-121">The final command modifies values of the secret named ITSecret in the key vault named Contoso, by using the values specified previously as variables.</span></span>

## <span data-ttu-id="78517-122">변수</span><span class="sxs-lookup"><span data-stu-id="78517-122">PARAMETERS</span></span>

### <span data-ttu-id="78517-123">-ContentType</span><span class="sxs-lookup"><span data-stu-id="78517-123">-ContentType</span></span>
<span data-ttu-id="78517-124">비밀의 콘텐츠 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="78517-124">Specifies the content type of a secret.</span></span>
<span data-ttu-id="78517-125">기존 콘텐츠 형식을 삭제 하려면 빈 문자열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="78517-125">To delete the existing content type, specify an empty string.</span></span>

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

### <span data-ttu-id="78517-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78517-126">-DefaultProfile</span></span>
<span data-ttu-id="78517-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="78517-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="78517-128">-Disable</span><span class="sxs-lookup"><span data-stu-id="78517-128">-Disable</span></span>
<span data-ttu-id="78517-129">이 cmdlet이 비밀을 사용 하지 않도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="78517-129">Indicates that this cmdlet disables a secret.</span></span>

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

### <span data-ttu-id="78517-130">-만료</span><span class="sxs-lookup"><span data-stu-id="78517-130">-Expires</span></span>
<span data-ttu-id="78517-131">이 cmdlet이 업데이트 하는 비밀에 대 한 만료 시간을 **DateTime** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="78517-131">Specifies the expiration time, as a **DateTime** object, for the secret that this cmdlet updates.</span></span>
<span data-ttu-id="78517-132">이 매개 변수는 UTC (협정 세계시)를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="78517-132">This parameter uses Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="78517-133">**DateTime** 개체를 가져오려면 **날짜 가져오기** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="78517-133">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="78517-134">자세한 내용은을 입력 `Get-Help Get-Date` 하세요.</span><span class="sxs-lookup"><span data-stu-id="78517-134">For more information, type `Get-Help Get-Date`.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78517-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="78517-135">-InputObject</span></span>
<span data-ttu-id="78517-136">비밀 개체</span><span class="sxs-lookup"><span data-stu-id="78517-136">Secret object</span></span>

```yaml
Type: PSKeyVaultSecretIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="78517-137">-이름</span><span class="sxs-lookup"><span data-stu-id="78517-137">-Name</span></span>
<span data-ttu-id="78517-138">수정할 비밀의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="78517-138">Specifies the name of a secret to modify.</span></span> <span data-ttu-id="78517-139">이 cmdlet은이 매개 변수에서 지정 하는 이름, 키 보관소의 이름 및 현재 환경에 따라 비밀의 FQDN (정규화 된 도메인 이름)을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="78517-139">This cmdlet constructs the fully qualified domain name (FQDN) of a secret based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78517-140">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="78517-140">-NotBefore</span></span>
<span data-ttu-id="78517-141">시간을 **DateTime** 개체로 지정 하 고 그 뒤에 비밀을 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="78517-141">Specifies the time, as a **DateTime** object, before which the secret cannot be used.</span></span> <span data-ttu-id="78517-142">이 매개 변수는 UTC를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="78517-142">This parameter uses UTC.</span></span> <span data-ttu-id="78517-143">**DateTime** 개체를 가져오려면 **날짜 가져오기** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="78517-143">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78517-144">-SecretValue</span><span class="sxs-lookup"><span data-stu-id="78517-144">-SecretValue</span></span>
<span data-ttu-id="78517-145">암호 값을 **SecureString** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="78517-145">Specifies the value for the secret as a **SecureString** object.</span></span> <span data-ttu-id="78517-146">**Securestring** 개체를 가져오려면 **ConvertTo-SecureString** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="78517-146">To obtain a **SecureString** object, use the **ConvertTo-SecureString** cmdlet.</span></span> <span data-ttu-id="78517-147">자세한 내용은을 입력 `Get-Help
ConvertTo-SecureString` 하세요.</span><span class="sxs-lookup"><span data-stu-id="78517-147">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78517-148">태그</span><span class="sxs-lookup"><span data-stu-id="78517-148">-Tag</span></span>
<span data-ttu-id="78517-149">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="78517-149">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="78517-150">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="78517-150">For example:</span></span>

<span data-ttu-id="78517-151">@ {key0 = "value0", key1 = $null, key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="78517-151">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78517-152">-VaultName</span><span class="sxs-lookup"><span data-stu-id="78517-152">-VaultName</span></span>
<span data-ttu-id="78517-153">이 비밀이 속한 키 보관소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="78517-153">Specifies the name of the key vault to which this secret belongs.</span></span> <span data-ttu-id="78517-154">이 cmdlet은이 매개 변수에서 지정 하는 이름 및 현재 환경에 따라 키 자격 증명의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="78517-154">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78517-155">-확인</span><span class="sxs-lookup"><span data-stu-id="78517-155">-Confirm</span></span>
<span data-ttu-id="78517-156">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="78517-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78517-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78517-157">-WhatIf</span></span>
<span data-ttu-id="78517-158">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="78517-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78517-159">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="78517-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78517-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78517-160">CommonParameters</span></span>
<span data-ttu-id="78517-161">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="78517-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78517-162">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78517-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78517-163">입력</span><span class="sxs-lookup"><span data-stu-id="78517-163">INPUTS</span></span>

### <span data-ttu-id="78517-164">않아야</span><span class="sxs-lookup"><span data-stu-id="78517-164">None</span></span>
<span data-ttu-id="78517-165">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="78517-165">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="78517-166">출력</span><span class="sxs-lookup"><span data-stu-id="78517-166">OUTPUTS</span></span>

### <span data-ttu-id="78517-167">Microsoft. KeyVault. PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="78517-167">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="78517-168">상속자</span><span class="sxs-lookup"><span data-stu-id="78517-168">NOTES</span></span>

## <span data-ttu-id="78517-169">관련 링크</span><span class="sxs-lookup"><span data-stu-id="78517-169">RELATED LINKS</span></span>

[<span data-ttu-id="78517-170">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="78517-170">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)

[<span data-ttu-id="78517-171">제거-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="78517-171">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)
