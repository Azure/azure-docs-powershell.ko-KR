---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 9FC72DE9-46BB-4CB5-9880-F53756DBE012
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultsecret
schema: 2.0.0
ms.openlocfilehash: 0c482d3fd4e2e02221799ea72e61eacc80ff9e2a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882217"
---
# <span data-ttu-id="5aa19-101">Set-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="5aa19-101">Set-AzureKeyVaultSecret</span></span>

## <span data-ttu-id="5aa19-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5aa19-102">SYNOPSIS</span></span>
<span data-ttu-id="5aa19-103">키 자격 증명 모음에서 비밀을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="5aa19-103">Creates or updates a secret in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5aa19-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5aa19-104">SYNTAX</span></span>

```
Set-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [-SecretValue] <SecureString> [-Disable]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5aa19-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5aa19-105">DESCRIPTION</span></span>
<span data-ttu-id="5aa19-106">**AzureKeyVaultSecret** Cmdlet은 Azure key vault의 키 보관소에서 비밀을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="5aa19-106">The **Set-AzureKeyVaultSecret** cmdlet creates or updates a secret in a key vault in Azure Key Vault.</span></span> <span data-ttu-id="5aa19-107">비밀이 존재 하지 않는 경우이 cmdlet이이를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5aa19-107">If the secret does not exist, this cmdlet creates it.</span></span> <span data-ttu-id="5aa19-108">비밀이 이미 있는 경우이 cmdlet은 해당 비밀의 새 버전을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5aa19-108">If the secret already exists, this cmdlet creates a new version of that secret.</span></span>

## <span data-ttu-id="5aa19-109">예제의</span><span class="sxs-lookup"><span data-stu-id="5aa19-109">EXAMPLES</span></span>

### <span data-ttu-id="5aa19-110">예제 1: 기본 특성을 사용 하 여 비밀 값 수정</span><span class="sxs-lookup"><span data-stu-id="5aa19-110">Example 1: Modify the value of a secret using default attributes</span></span>
```
PS C:\> $Secret = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> Set-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -SecretValue $Secret
```

<span data-ttu-id="5aa19-111">첫 번째 명령은 **ConvertTo-SecureString** cmdlet을 사용 하 여 문자열을 보안 문자열로 변환한 다음 해당 문자열을 $Secret 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="5aa19-111">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Secret variable.</span></span> <span data-ttu-id="5aa19-112">자세한 내용은을 입력 `Get-Help
ConvertTo-SecureString` 하세요.</span><span class="sxs-lookup"><span data-stu-id="5aa19-112">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>

<span data-ttu-id="5aa19-113">두 번째 명령은 Contoso 라는 이름의 자격 증명 모음에서 ITSecret 라는 비밀 키의 값을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5aa19-113">The second command modifies value of the secret named ITSecret in the key vault named Contoso.</span></span> <span data-ttu-id="5aa19-114">비밀 값이 $Secret에 저장 된 값이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5aa19-114">The secret value becomes the value stored in $Secret.</span></span>

### <span data-ttu-id="5aa19-115">예제 2: 사용자 지정 특성을 사용 하 여 비밀 값 수정</span><span class="sxs-lookup"><span data-stu-id="5aa19-115">Example 2: Modify the value of a secret using custom attributes</span></span>
```
PS C:\> $Secret = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $NBF =(Get-Date).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'medium'; 'IT' = null }
PS C:\> $ContentType = 'txt'
PS C:\> Set-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -SecretValue $Secret -Expires $Expires -NotBefore $NBF -ContentType $ContentType -Disable $False -Tags $Tags
```

<span data-ttu-id="5aa19-116">첫 번째 명령은 **ConvertTo-SecureString** cmdlet을 사용 하 여 문자열을 보안 문자열로 변환한 다음 해당 문자열을 $Secret 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="5aa19-116">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Secret variable.</span></span> <span data-ttu-id="5aa19-117">자세한 내용은을 입력 `Get-Help
ConvertTo-SecureString` 하세요.</span><span class="sxs-lookup"><span data-stu-id="5aa19-117">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>

<span data-ttu-id="5aa19-118">다음 명령은 만료 날짜, 태그, 컨텍스트 형식에 대 한 사용자 지정 특성을 정의 하 고 변수에 특성을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="5aa19-118">The next commands define custom attributes for the expiry date, tags, and context type, and store the attributes in variables.</span></span>

<span data-ttu-id="5aa19-119">마지막 명령은 이전에 변수로 지정 된 값을 사용 하 여 Contoso 라는 키 보관소에 ITSecret 라는 비밀 값을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5aa19-119">The final command modifies values of the secret named ITSecret in the key vault named Contoso, by using the values specified previously as variables.</span></span>

## <span data-ttu-id="5aa19-120">변수</span><span class="sxs-lookup"><span data-stu-id="5aa19-120">PARAMETERS</span></span>

### <span data-ttu-id="5aa19-121">-ContentType</span><span class="sxs-lookup"><span data-stu-id="5aa19-121">-ContentType</span></span>
<span data-ttu-id="5aa19-122">비밀의 콘텐츠 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5aa19-122">Specifies the content type of a secret.</span></span>
<span data-ttu-id="5aa19-123">기존 콘텐츠 형식을 삭제 하려면 빈 문자열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5aa19-123">To delete the existing content type, specify an empty string.</span></span>

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

### <span data-ttu-id="5aa19-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5aa19-124">-DefaultProfile</span></span>
<span data-ttu-id="5aa19-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="5aa19-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5aa19-126">-Disable</span><span class="sxs-lookup"><span data-stu-id="5aa19-126">-Disable</span></span>
<span data-ttu-id="5aa19-127">이 cmdlet이 비밀을 사용 하지 않도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5aa19-127">Indicates that this cmdlet disables a secret.</span></span>

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

### <span data-ttu-id="5aa19-128">-만료</span><span class="sxs-lookup"><span data-stu-id="5aa19-128">-Expires</span></span>
<span data-ttu-id="5aa19-129">이 cmdlet이 업데이트 하는 비밀에 대 한 만료 시간을 **DateTime** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5aa19-129">Specifies the expiration time, as a **DateTime** object, for the secret that this cmdlet updates.</span></span>
<span data-ttu-id="5aa19-130">이 매개 변수는 UTC (협정 세계시)를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5aa19-130">This parameter uses Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="5aa19-131">**DateTime** 개체를 가져오려면 **날짜 가져오기** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5aa19-131">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="5aa19-132">자세한 내용은을 입력 `Get-Help Get-Date` 하세요.</span><span class="sxs-lookup"><span data-stu-id="5aa19-132">For more information, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="5aa19-133">-이름</span><span class="sxs-lookup"><span data-stu-id="5aa19-133">-Name</span></span>
<span data-ttu-id="5aa19-134">수정할 비밀의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5aa19-134">Specifies the name of a secret to modify.</span></span> <span data-ttu-id="5aa19-135">이 cmdlet은이 매개 변수에서 지정 하는 이름, 키 보관소의 이름 및 현재 환경에 따라 비밀의 FQDN (정규화 된 도메인 이름)을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="5aa19-135">This cmdlet constructs the fully qualified domain name (FQDN) of a secret based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5aa19-136">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="5aa19-136">-NotBefore</span></span>
<span data-ttu-id="5aa19-137">시간을 **DateTime** 개체로 지정 하 고 그 뒤에 비밀을 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="5aa19-137">Specifies the time, as a **DateTime** object, before which the secret cannot be used.</span></span> <span data-ttu-id="5aa19-138">이 매개 변수는 UTC를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5aa19-138">This parameter uses UTC.</span></span> <span data-ttu-id="5aa19-139">**DateTime** 개체를 가져오려면 **날짜 가져오기** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5aa19-139">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>

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

### <span data-ttu-id="5aa19-140">-SecretValue</span><span class="sxs-lookup"><span data-stu-id="5aa19-140">-SecretValue</span></span>
<span data-ttu-id="5aa19-141">암호 값을 **SecureString** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5aa19-141">Specifies the value for the secret as a **SecureString** object.</span></span> <span data-ttu-id="5aa19-142">**Securestring** 개체를 가져오려면 **ConvertTo-SecureString** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5aa19-142">To obtain a **SecureString** object, use the **ConvertTo-SecureString** cmdlet.</span></span> <span data-ttu-id="5aa19-143">자세한 내용은을 입력 `Get-Help
ConvertTo-SecureString` 하세요.</span><span class="sxs-lookup"><span data-stu-id="5aa19-143">For more information, type `Get-Help
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

### <span data-ttu-id="5aa19-144">태그</span><span class="sxs-lookup"><span data-stu-id="5aa19-144">-Tag</span></span>
<span data-ttu-id="5aa19-145">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="5aa19-145">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="5aa19-146">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="5aa19-146">For example:</span></span>

<span data-ttu-id="5aa19-147">@ {key0 = "value0", key1 = $null, key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="5aa19-147">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="5aa19-148">-VaultName</span><span class="sxs-lookup"><span data-stu-id="5aa19-148">-VaultName</span></span>
<span data-ttu-id="5aa19-149">이 비밀이 속한 키 보관소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5aa19-149">Specifies the name of the key vault to which this secret belongs.</span></span> <span data-ttu-id="5aa19-150">이 cmdlet은이 매개 변수에서 지정 하는 이름 및 현재 환경에 따라 키 자격 증명의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="5aa19-150">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="5aa19-151">-확인</span><span class="sxs-lookup"><span data-stu-id="5aa19-151">-Confirm</span></span>
<span data-ttu-id="5aa19-152">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="5aa19-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5aa19-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5aa19-153">-WhatIf</span></span>
<span data-ttu-id="5aa19-154">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="5aa19-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5aa19-155">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5aa19-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5aa19-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5aa19-156">CommonParameters</span></span>
<span data-ttu-id="5aa19-157">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5aa19-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5aa19-158">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5aa19-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5aa19-159">입력</span><span class="sxs-lookup"><span data-stu-id="5aa19-159">INPUTS</span></span>

## <span data-ttu-id="5aa19-160">출력</span><span class="sxs-lookup"><span data-stu-id="5aa19-160">OUTPUTS</span></span>

### <span data-ttu-id="5aa19-161">Microsoft. KeyVault. 모델 암호</span><span class="sxs-lookup"><span data-stu-id="5aa19-161">Microsoft.Azure.Commands.KeyVault.Models.Secret</span></span>

## <span data-ttu-id="5aa19-162">상속자</span><span class="sxs-lookup"><span data-stu-id="5aa19-162">NOTES</span></span>

## <span data-ttu-id="5aa19-163">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5aa19-163">RELATED LINKS</span></span>

[<span data-ttu-id="5aa19-164">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="5aa19-164">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)

[<span data-ttu-id="5aa19-165">제거-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="5aa19-165">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)
