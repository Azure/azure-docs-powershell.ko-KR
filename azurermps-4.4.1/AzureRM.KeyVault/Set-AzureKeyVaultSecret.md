---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 9FC72DE9-46BB-4CB5-9880-F53756DBE012
online version: https://go.microsoft.com/fwlink/?LinkId=690303
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultSecret.md
ms.openlocfilehash: 737a99fa59530ca37d32e2ca1c2c7d7e609ed225
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711270"
---
# <span data-ttu-id="a7a4d-101">Set-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="a7a4d-101">Set-AzureKeyVaultSecret</span></span>

## <span data-ttu-id="a7a4d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7a4d-102">SYNOPSIS</span></span>
<span data-ttu-id="a7a4d-103">키 자격 증명 모음에서 비밀을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7a4d-103">Creates or updates a secret in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a7a4d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a7a4d-104">SYNTAX</span></span>

```
Set-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [-SecretValue] <SecureString> [-Disable]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a7a4d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a7a4d-105">DESCRIPTION</span></span>
<span data-ttu-id="a7a4d-106">**AzureKeyVaultSecret** Cmdlet은 Azure key vault의 키 보관소에서 비밀을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7a4d-106">The **Set-AzureKeyVaultSecret** cmdlet creates or updates a secret in a key vault in Azure Key Vault.</span></span> <span data-ttu-id="a7a4d-107">비밀이 존재 하지 않는 경우이 cmdlet이이를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a7a4d-107">If the secret does not exist, this cmdlet creates it.</span></span> <span data-ttu-id="a7a4d-108">비밀이 이미 있는 경우이 cmdlet은 해당 비밀의 새 버전을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a7a4d-108">If the secret already exists, this cmdlet creates a new version of that secret.</span></span>

## <span data-ttu-id="a7a4d-109">예제의</span><span class="sxs-lookup"><span data-stu-id="a7a4d-109">EXAMPLES</span></span>

### <span data-ttu-id="a7a4d-110">예제 1: 기본 특성을 사용 하 여 비밀 값 수정</span><span class="sxs-lookup"><span data-stu-id="a7a4d-110">Example 1: Modify the value of a secret using default attributes</span></span>
```
PS C:\> $Secret = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> Set-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -SecretValue $Secret
```

<span data-ttu-id="a7a4d-111">첫 번째 명령은 **ConvertTo-SecureString** cmdlet을 사용 하 여 문자열을 보안 문자열로 변환한 다음 해당 문자열을 $Secret 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7a4d-111">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Secret variable.</span></span> <span data-ttu-id="a7a4d-112">자세한 내용은을 입력 `Get-Help
ConvertTo-SecureString` 하세요.</span><span class="sxs-lookup"><span data-stu-id="a7a4d-112">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>

<span data-ttu-id="a7a4d-113">두 번째 명령은 Contoso 라는 이름의 자격 증명 모음에서 ITSecret 라는 비밀 키의 값을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7a4d-113">The second command modifies value of the secret named ITSecret in the key vault named Contoso.</span></span> <span data-ttu-id="a7a4d-114">비밀 값이 $Secret에 저장 된 값이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a7a4d-114">The secret value becomes the value stored in $Secret.</span></span>

### <span data-ttu-id="a7a4d-115">예제 2: 사용자 지정 특성을 사용 하 여 비밀 값 수정</span><span class="sxs-lookup"><span data-stu-id="a7a4d-115">Example 2: Modify the value of a secret using custom attributes</span></span>
```
PS C:\> $Secret = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $NBF =(Get-Date).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'medium'; 'IT' = null }
PS C:\> $ContentType = 'txt'
PS C:\> Set-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -SecretValue $Secret -Expires $Expires -NotBefore $NBF -ContentType $ContentType -Disable $False -Tags $Tags
```

<span data-ttu-id="a7a4d-116">첫 번째 명령은 **ConvertTo-SecureString** cmdlet을 사용 하 여 문자열을 보안 문자열로 변환한 다음 해당 문자열을 $Secret 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7a4d-116">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Secret variable.</span></span> <span data-ttu-id="a7a4d-117">자세한 내용은을 입력 `Get-Help
ConvertTo-SecureString` 하세요.</span><span class="sxs-lookup"><span data-stu-id="a7a4d-117">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>

<span data-ttu-id="a7a4d-118">다음 명령은 만료 날짜, 태그, 컨텍스트 형식에 대 한 사용자 지정 특성을 정의 하 고 변수에 특성을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7a4d-118">The next commands define custom attributes for the expiry date, tags, and context type, and store the attributes in variables.</span></span>

<span data-ttu-id="a7a4d-119">마지막 명령은 이전에 변수로 지정 된 값을 사용 하 여 Contoso 라는 키 보관소에 ITSecret 라는 비밀 값을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7a4d-119">The final command modifies values of the secret named ITSecret in the key vault named Contoso, by using the values specified previously as variables.</span></span>

## <span data-ttu-id="a7a4d-120">변수</span><span class="sxs-lookup"><span data-stu-id="a7a4d-120">PARAMETERS</span></span>

### <span data-ttu-id="a7a4d-121">-확인</span><span class="sxs-lookup"><span data-stu-id="a7a4d-121">-Confirm</span></span>
<span data-ttu-id="a7a4d-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7a4d-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7a4d-123">-ContentType</span><span class="sxs-lookup"><span data-stu-id="a7a4d-123">-ContentType</span></span>
<span data-ttu-id="a7a4d-124">비밀의 콘텐츠 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7a4d-124">Specifies the content type of a secret.</span></span>
<span data-ttu-id="a7a4d-125">기존 콘텐츠 형식을 삭제 하려면 빈 문자열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7a4d-125">To delete the existing content type, specify an empty string.</span></span>

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

### <span data-ttu-id="a7a4d-126">-Disable</span><span class="sxs-lookup"><span data-stu-id="a7a4d-126">-Disable</span></span>
<span data-ttu-id="a7a4d-127">이 cmdlet이 비밀을 사용 하지 않도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7a4d-127">Indicates that this cmdlet disables a secret.</span></span>

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

### <span data-ttu-id="a7a4d-128">-만료</span><span class="sxs-lookup"><span data-stu-id="a7a4d-128">-Expires</span></span>
<span data-ttu-id="a7a4d-129">이 cmdlet이 업데이트 하는 비밀에 대 한 만료 시간을 **DateTime** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7a4d-129">Specifies the expiration time, as a **DateTime** object, for the secret that this cmdlet updates.</span></span>
<span data-ttu-id="a7a4d-130">이 매개 변수는 UTC (협정 세계시)를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7a4d-130">This parameter uses Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="a7a4d-131">**DateTime** 개체를 가져오려면 **날짜 가져오기** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7a4d-131">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="a7a4d-132">자세한 내용은을 입력 `Get-Help Get-Date` 하세요.</span><span class="sxs-lookup"><span data-stu-id="a7a4d-132">For more information, type `Get-Help Get-Date`.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7a4d-133">-이름</span><span class="sxs-lookup"><span data-stu-id="a7a4d-133">-Name</span></span>
<span data-ttu-id="a7a4d-134">수정할 비밀의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7a4d-134">Specifies the name of a secret to modify.</span></span> <span data-ttu-id="a7a4d-135">이 cmdlet은이 매개 변수에서 지정 하는 이름, 키 보관소의 이름 및 현재 환경에 따라 비밀의 FQDN (정규화 된 도메인 이름)을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7a4d-135">This cmdlet constructs the fully qualified domain name (FQDN) of a secret based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SecretName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7a4d-136">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="a7a4d-136">-NotBefore</span></span>
<span data-ttu-id="a7a4d-137">시간을 **DateTime** 개체로 지정 하 고 그 뒤에 비밀을 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="a7a4d-137">Specifies the time, as a **DateTime** object, before which the secret cannot be used.</span></span> <span data-ttu-id="a7a4d-138">이 매개 변수는 UTC를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7a4d-138">This parameter uses UTC.</span></span> <span data-ttu-id="a7a4d-139">**DateTime** 개체를 가져오려면 **날짜 가져오기** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7a4d-139">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7a4d-140">-SecretValue</span><span class="sxs-lookup"><span data-stu-id="a7a4d-140">-SecretValue</span></span>
<span data-ttu-id="a7a4d-141">암호 값을 **SecureString** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7a4d-141">Specifies the value for the secret as a **SecureString** object.</span></span> <span data-ttu-id="a7a4d-142">**Securestring** 개체를 가져오려면 **ConvertTo-SecureString** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7a4d-142">To obtain a **SecureString** object, use the **ConvertTo-SecureString** cmdlet.</span></span> <span data-ttu-id="a7a4d-143">자세한 내용은을 입력 `Get-Help
ConvertTo-SecureString` 하세요.</span><span class="sxs-lookup"><span data-stu-id="a7a4d-143">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7a4d-144">태그</span><span class="sxs-lookup"><span data-stu-id="a7a4d-144">-Tag</span></span>
<span data-ttu-id="a7a4d-145">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="a7a4d-145">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="a7a4d-146">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="a7a4d-146">For example:</span></span>

<span data-ttu-id="a7a4d-147">@ {key0 = "value0", key1 = $null, key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="a7a4d-147">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7a4d-148">-VaultName</span><span class="sxs-lookup"><span data-stu-id="a7a4d-148">-VaultName</span></span>
<span data-ttu-id="a7a4d-149">이 비밀이 속한 키 보관소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7a4d-149">Specifies the name of the key vault to which this secret belongs.</span></span> <span data-ttu-id="a7a4d-150">이 cmdlet은이 매개 변수에서 지정 하는 이름 및 현재 환경에 따라 키 자격 증명의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7a4d-150">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7a4d-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7a4d-151">-WhatIf</span></span>
<span data-ttu-id="a7a4d-152">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a7a4d-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7a4d-153">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a7a4d-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7a4d-154">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7a4d-154">-DefaultProfile</span></span>
<span data-ttu-id="a7a4d-155">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a7a4d-155">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a7a4d-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7a4d-156">CommonParameters</span></span>
<span data-ttu-id="a7a4d-157">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7a4d-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7a4d-158">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7a4d-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7a4d-159">입력</span><span class="sxs-lookup"><span data-stu-id="a7a4d-159">INPUTS</span></span>

## <span data-ttu-id="a7a4d-160">출력</span><span class="sxs-lookup"><span data-stu-id="a7a4d-160">OUTPUTS</span></span>

### <span data-ttu-id="a7a4d-161">Microsoft. KeyVault. 모델 암호</span><span class="sxs-lookup"><span data-stu-id="a7a4d-161">Microsoft.Azure.Commands.KeyVault.Models.Secret</span></span>

## <span data-ttu-id="a7a4d-162">상속자</span><span class="sxs-lookup"><span data-stu-id="a7a4d-162">NOTES</span></span>

## <span data-ttu-id="a7a4d-163">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a7a4d-163">RELATED LINKS</span></span>

[<span data-ttu-id="a7a4d-164">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="a7a4d-164">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)

[<span data-ttu-id="a7a4d-165">제거-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="a7a4d-165">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)
