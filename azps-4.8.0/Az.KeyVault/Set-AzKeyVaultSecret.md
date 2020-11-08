---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 9FC72DE9-46BB-4CB5-9880-F53756DBE012
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultSecret.md
ms.openlocfilehash: 0733cf722e26cb52abdb84f7917a78d088f49fd4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94211885"
---
# <span data-ttu-id="c7087-101">Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="c7087-101">Set-AzKeyVaultSecret</span></span>

## <span data-ttu-id="c7087-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7087-102">SYNOPSIS</span></span>
<span data-ttu-id="c7087-103">키 자격 증명 모음에서 비밀을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7087-103">Creates or updates a secret in a key vault.</span></span>

## <span data-ttu-id="c7087-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c7087-104">SYNTAX</span></span>

### <span data-ttu-id="c7087-105">기본값 (기본값)</span><span class="sxs-lookup"><span data-stu-id="c7087-105">Default (Default)</span></span>
```
Set-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [-SecretValue] <SecureString> [-Disable]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7087-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="c7087-106">InputObject</span></span>
```
Set-AzKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [-SecretValue] <SecureString> [-Disable]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7087-107">설명은</span><span class="sxs-lookup"><span data-stu-id="c7087-107">DESCRIPTION</span></span>
<span data-ttu-id="c7087-108">**AzKeyVaultSecret** Cmdlet은 Azure key vault의 키 보관소에서 비밀을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7087-108">The **Set-AzKeyVaultSecret** cmdlet creates or updates a secret in a key vault in Azure Key Vault.</span></span> <span data-ttu-id="c7087-109">비밀이 존재 하지 않는 경우이 cmdlet이이를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c7087-109">If the secret does not exist, this cmdlet creates it.</span></span> <span data-ttu-id="c7087-110">비밀이 이미 있는 경우이 cmdlet은 해당 비밀의 새 버전을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c7087-110">If the secret already exists, this cmdlet creates a new version of that secret.</span></span>

## <span data-ttu-id="c7087-111">예제의</span><span class="sxs-lookup"><span data-stu-id="c7087-111">EXAMPLES</span></span>

### <span data-ttu-id="c7087-112">예제 1: 기본 특성을 사용 하 여 비밀 값 수정</span><span class="sxs-lookup"><span data-stu-id="c7087-112">Example 1: Modify the value of a secret using default attributes</span></span>
```powershell
PS C:\> $Secret = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> Set-AzKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -SecretValue $Secret

Vault Name   : Contoso
Name         : ITSecret
Version      : 8b5c0cb0326e4350bd78200fac932b51
Id           : https://contoso.vault.azure.net:443/secrets/ITSecret/8b5c0cb0326e4350bd78200fac932b51
Enabled      : True
Expires      :
Not Before   :
Created      : 5/25/2018 6:39:30 PM
Updated      : 5/25/2018 6:39:30 PM
Content Type :
Tags         :
```

<span data-ttu-id="c7087-113">첫 번째 명령은 **ConvertTo-SecureString** cmdlet을 사용 하 여 문자열을 보안 문자열로 변환한 다음 해당 문자열을 $Secret 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7087-113">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Secret variable.</span></span> <span data-ttu-id="c7087-114">자세한 내용은을 입력 `Get-Help
ConvertTo-SecureString` 하세요.</span><span class="sxs-lookup"><span data-stu-id="c7087-114">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>
<span data-ttu-id="c7087-115">두 번째 명령은 Contoso 라는 이름의 자격 증명 모음에서 ITSecret 라는 비밀 키의 값을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7087-115">The second command modifies value of the secret named ITSecret in the key vault named Contoso.</span></span> <span data-ttu-id="c7087-116">비밀 값이 $Secret에 저장 된 값이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c7087-116">The secret value becomes the value stored in $Secret.</span></span>

### <span data-ttu-id="c7087-117">예제 2: 사용자 지정 특성을 사용 하 여 비밀 값 수정</span><span class="sxs-lookup"><span data-stu-id="c7087-117">Example 2: Modify the value of a secret using custom attributes</span></span>
```powershell
PS C:\> $Secret = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $NBF =(Get-Date).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'medium'; 'IT' = 'true'}
PS C:\> $ContentType = 'txt'
PS C:\> Set-AzKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -SecretValue $Secret -Expires $Expires -NotBefore $NBF -ContentType $ContentType -Disable -Tags $Tags

Vault Name   : Contoso
Name         : ITSecret
Version      : a2c150be3ea24dd6b8286986e6364851
Id           : https://contoso.vault.azure.net:443/secrets/ITSecret/a2c150be3ea24dd6b8286986e6364851
Enabled      : False
Expires      : 5/25/2020 6:40:00 PM
Not Before   : 5/25/2018 6:40:05 PM
Created      : 5/25/2018 6:41:22 PM
Updated      : 5/25/2018 6:41:22 PM
Content Type : txt
Tags         : Name      Value
               Severity  medium
               IT        true
```

<span data-ttu-id="c7087-118">첫 번째 명령은 **ConvertTo-SecureString** cmdlet을 사용 하 여 문자열을 보안 문자열로 변환한 다음 해당 문자열을 $Secret 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7087-118">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Secret variable.</span></span> <span data-ttu-id="c7087-119">자세한 내용은을 입력 `Get-Help
ConvertTo-SecureString` 하세요.</span><span class="sxs-lookup"><span data-stu-id="c7087-119">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>
<span data-ttu-id="c7087-120">다음 명령은 만료 날짜, 태그, 컨텍스트 형식에 대 한 사용자 지정 특성을 정의 하 고 변수에 특성을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7087-120">The next commands define custom attributes for the expiry date, tags, and context type, and store the attributes in variables.</span></span>
<span data-ttu-id="c7087-121">마지막 명령은 이전에 변수로 지정 된 값을 사용 하 여 Contoso 라는 키 보관소에 ITSecret 라는 비밀 값을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7087-121">The final command modifies values of the secret named ITSecret in the key vault named Contoso, by using the values specified previously as variables.</span></span>

## <span data-ttu-id="c7087-122">변수</span><span class="sxs-lookup"><span data-stu-id="c7087-122">PARAMETERS</span></span>

### <span data-ttu-id="c7087-123">-ContentType</span><span class="sxs-lookup"><span data-stu-id="c7087-123">-ContentType</span></span>
<span data-ttu-id="c7087-124">비밀의 콘텐츠 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7087-124">Specifies the content type of a secret.</span></span>
<span data-ttu-id="c7087-125">기존 콘텐츠 형식을 삭제 하려면 빈 문자열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7087-125">To delete the existing content type, specify an empty string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7087-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7087-126">-DefaultProfile</span></span>
<span data-ttu-id="c7087-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="c7087-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c7087-128">-Disable</span><span class="sxs-lookup"><span data-stu-id="c7087-128">-Disable</span></span>
<span data-ttu-id="c7087-129">이 cmdlet이 비밀을 사용 하지 않도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7087-129">Indicates that this cmdlet disables a secret.</span></span>

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

### <span data-ttu-id="c7087-130">-만료</span><span class="sxs-lookup"><span data-stu-id="c7087-130">-Expires</span></span>
<span data-ttu-id="c7087-131">이 cmdlet이 업데이트 하는 비밀에 대 한 만료 시간을 **DateTime** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7087-131">Specifies the expiration time, as a **DateTime** object, for the secret that this cmdlet updates.</span></span>
<span data-ttu-id="c7087-132">이 매개 변수는 UTC (협정 세계시)를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7087-132">This parameter uses Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="c7087-133">**DateTime** 개체를 가져오려면 **날짜 가져오기** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7087-133">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="c7087-134">자세한 내용은을 입력 `Get-Help Get-Date` 하세요.</span><span class="sxs-lookup"><span data-stu-id="c7087-134">For more information, type `Get-Help Get-Date`.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7087-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c7087-135">-InputObject</span></span>
<span data-ttu-id="c7087-136">비밀 개체</span><span class="sxs-lookup"><span data-stu-id="c7087-136">Secret object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c7087-137">-이름</span><span class="sxs-lookup"><span data-stu-id="c7087-137">-Name</span></span>
<span data-ttu-id="c7087-138">수정할 비밀의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7087-138">Specifies the name of a secret to modify.</span></span> <span data-ttu-id="c7087-139">이 cmdlet은이 매개 변수에서 지정 하는 이름, 키 보관소의 이름 및 현재 환경에 따라 비밀의 FQDN (정규화 된 도메인 이름)을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7087-139">This cmdlet constructs the fully qualified domain name (FQDN) of a secret based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7087-140">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="c7087-140">-NotBefore</span></span>
<span data-ttu-id="c7087-141">시간을 **DateTime** 개체로 지정 하 고 그 뒤에 비밀을 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="c7087-141">Specifies the time, as a **DateTime** object, before which the secret cannot be used.</span></span> <span data-ttu-id="c7087-142">이 매개 변수는 UTC를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7087-142">This parameter uses UTC.</span></span> <span data-ttu-id="c7087-143">**DateTime** 개체를 가져오려면 **날짜 가져오기** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7087-143">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7087-144">-SecretValue</span><span class="sxs-lookup"><span data-stu-id="c7087-144">-SecretValue</span></span>
<span data-ttu-id="c7087-145">암호 값을 **SecureString** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7087-145">Specifies the value for the secret as a **SecureString** object.</span></span> <span data-ttu-id="c7087-146">**Securestring** 개체를 가져오려면 **ConvertTo-SecureString** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7087-146">To obtain a **SecureString** object, use the **ConvertTo-SecureString** cmdlet.</span></span> <span data-ttu-id="c7087-147">자세한 내용은을 입력 `Get-Help
ConvertTo-SecureString` 하세요.</span><span class="sxs-lookup"><span data-stu-id="c7087-147">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7087-148">태그</span><span class="sxs-lookup"><span data-stu-id="c7087-148">-Tag</span></span>
<span data-ttu-id="c7087-149">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="c7087-149">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="c7087-150">예: @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="c7087-150">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7087-151">-VaultName</span><span class="sxs-lookup"><span data-stu-id="c7087-151">-VaultName</span></span>
<span data-ttu-id="c7087-152">이 비밀이 속한 키 보관소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7087-152">Specifies the name of the key vault to which this secret belongs.</span></span> <span data-ttu-id="c7087-153">이 cmdlet은이 매개 변수에서 지정 하는 이름 및 현재 환경에 따라 키 자격 증명의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7087-153">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7087-154">-확인</span><span class="sxs-lookup"><span data-stu-id="c7087-154">-Confirm</span></span>
<span data-ttu-id="c7087-155">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7087-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7087-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7087-156">-WhatIf</span></span>
<span data-ttu-id="c7087-157">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c7087-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7087-158">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c7087-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7087-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7087-159">CommonParameters</span></span>
<span data-ttu-id="c7087-160">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7087-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7087-161">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c7087-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7087-162">입력</span><span class="sxs-lookup"><span data-stu-id="c7087-162">INPUTS</span></span>

### <span data-ttu-id="c7087-163">Microsoft. KeyVault. PSKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="c7087-163">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span></span>

## <span data-ttu-id="c7087-164">출력</span><span class="sxs-lookup"><span data-stu-id="c7087-164">OUTPUTS</span></span>

### <span data-ttu-id="c7087-165">Microsoft. KeyVault. PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="c7087-165">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="c7087-166">상속자</span><span class="sxs-lookup"><span data-stu-id="c7087-166">NOTES</span></span>

## <span data-ttu-id="c7087-167">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c7087-167">RELATED LINKS</span></span>

[<span data-ttu-id="c7087-168">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="c7087-168">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)

[<span data-ttu-id="c7087-169">제거-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="c7087-169">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)
