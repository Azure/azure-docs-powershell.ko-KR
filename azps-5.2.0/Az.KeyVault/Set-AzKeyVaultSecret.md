---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 9FC72DE9-46BB-4CB5-9880-F53756DBE012
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultSecret.md
ms.openlocfilehash: 0733cf722e26cb52abdb84f7917a78d088f49fd4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98347481"
---
# <span data-ttu-id="5a523-101">Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="5a523-101">Set-AzKeyVaultSecret</span></span>

## <span data-ttu-id="5a523-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a523-102">SYNOPSIS</span></span>
<span data-ttu-id="5a523-103">키 자격 증명 모음에서 비밀을 생성하거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="5a523-103">Creates or updates a secret in a key vault.</span></span>

## <span data-ttu-id="5a523-104">구문</span><span class="sxs-lookup"><span data-stu-id="5a523-104">SYNTAX</span></span>

### <span data-ttu-id="5a523-105">기본값(기본값)</span><span class="sxs-lookup"><span data-stu-id="5a523-105">Default (Default)</span></span>
```
Set-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [-SecretValue] <SecureString> [-Disable]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a523-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="5a523-106">InputObject</span></span>
```
Set-AzKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [-SecretValue] <SecureString> [-Disable]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a523-107">설명</span><span class="sxs-lookup"><span data-stu-id="5a523-107">DESCRIPTION</span></span>
<span data-ttu-id="5a523-108">**Set-AzKeyVaultSecret** cmdlet은 Azure Key Vault의 키 자격 증명 모음에 비밀을 만들거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="5a523-108">The **Set-AzKeyVaultSecret** cmdlet creates or updates a secret in a key vault in Azure Key Vault.</span></span> <span data-ttu-id="5a523-109">비밀이 없는 경우 이 cmdlet에서 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5a523-109">If the secret does not exist, this cmdlet creates it.</span></span> <span data-ttu-id="5a523-110">비밀이 이미 있는 경우 이 cmdlet은 해당 비밀의 새 버전을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5a523-110">If the secret already exists, this cmdlet creates a new version of that secret.</span></span>

## <span data-ttu-id="5a523-111">예제</span><span class="sxs-lookup"><span data-stu-id="5a523-111">EXAMPLES</span></span>

### <span data-ttu-id="5a523-112">예제 1: 기본 특성을 사용하여 비밀 값 수정</span><span class="sxs-lookup"><span data-stu-id="5a523-112">Example 1: Modify the value of a secret using default attributes</span></span>
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

<span data-ttu-id="5a523-113">첫 번째 명령은 **ConvertTo-SecureString** cmdlet을 사용하여 문자열을 보안 문자열로 변환한 다음 해당 문자열을 $Secret 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="5a523-113">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Secret variable.</span></span> <span data-ttu-id="5a523-114">자세한 내용은 `Get-Help
ConvertTo-SecureString` .를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="5a523-114">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>
<span data-ttu-id="5a523-115">두 번째 명령은 Contoso라는 키 자격 증명 모음에서 ITSecret이라는 비밀의 값을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="5a523-115">The second command modifies value of the secret named ITSecret in the key vault named Contoso.</span></span> <span data-ttu-id="5a523-116">비밀 값은 다음 위치에 저장된 $Secret.</span><span class="sxs-lookup"><span data-stu-id="5a523-116">The secret value becomes the value stored in $Secret.</span></span>

### <span data-ttu-id="5a523-117">예제 2: 사용자 지정 특성을 사용하여 비밀 값 수정</span><span class="sxs-lookup"><span data-stu-id="5a523-117">Example 2: Modify the value of a secret using custom attributes</span></span>
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

<span data-ttu-id="5a523-118">첫 번째 명령은 **ConvertTo-SecureString** cmdlet을 사용하여 문자열을 보안 문자열로 변환한 다음 해당 문자열을 $Secret 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="5a523-118">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Secret variable.</span></span> <span data-ttu-id="5a523-119">자세한 내용은 `Get-Help
ConvertTo-SecureString` .를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="5a523-119">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>
<span data-ttu-id="5a523-120">다음 명령은 만료 날짜, 태그 및 컨텍스트 형식에 대한 사용자 지정 특성을 정의하고 특성을 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="5a523-120">The next commands define custom attributes for the expiry date, tags, and context type, and store the attributes in variables.</span></span>
<span data-ttu-id="5a523-121">마지막 명령은 이전에 변수로 지정된 값을 사용하여 Contoso라는 키 자격 증명 모음에서 ITSecret이라는 비밀의 값을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="5a523-121">The final command modifies values of the secret named ITSecret in the key vault named Contoso, by using the values specified previously as variables.</span></span>

## <span data-ttu-id="5a523-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5a523-122">PARAMETERS</span></span>

### <span data-ttu-id="5a523-123">-ContentType</span><span class="sxs-lookup"><span data-stu-id="5a523-123">-ContentType</span></span>
<span data-ttu-id="5a523-124">비밀의 콘텐츠 형식을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5a523-124">Specifies the content type of a secret.</span></span>
<span data-ttu-id="5a523-125">기존 콘텐츠 형식을 삭제하려면 빈 문자열을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5a523-125">To delete the existing content type, specify an empty string.</span></span>

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

### <span data-ttu-id="5a523-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a523-126">-DefaultProfile</span></span>
<span data-ttu-id="5a523-127">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="5a523-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5a523-128">-Disable</span><span class="sxs-lookup"><span data-stu-id="5a523-128">-Disable</span></span>
<span data-ttu-id="5a523-129">이 cmdlet이 비밀을 사용하지 않도록 설정하는지 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="5a523-129">Indicates that this cmdlet disables a secret.</span></span>

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

### <span data-ttu-id="5a523-130">-Expires</span><span class="sxs-lookup"><span data-stu-id="5a523-130">-Expires</span></span>
<span data-ttu-id="5a523-131">이 cmdlet이 업데이트하는 비밀에 대한 만료 시간을 **DateTime** 개체로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5a523-131">Specifies the expiration time, as a **DateTime** object, for the secret that this cmdlet updates.</span></span>
<span data-ttu-id="5a523-132">이 매개 변수는 협정 세계시(UTC)를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="5a523-132">This parameter uses Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="5a523-133">**DateTime 개체를** 얻습니다. **Get-Date** cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="5a523-133">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="5a523-134">자세한 내용은 `Get-Help Get-Date` .를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="5a523-134">For more information, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="5a523-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5a523-135">-InputObject</span></span>
<span data-ttu-id="5a523-136">비밀 개체</span><span class="sxs-lookup"><span data-stu-id="5a523-136">Secret object</span></span>

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

### <span data-ttu-id="5a523-137">-Name</span><span class="sxs-lookup"><span data-stu-id="5a523-137">-Name</span></span>
<span data-ttu-id="5a523-138">수정할 비밀의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5a523-138">Specifies the name of a secret to modify.</span></span> <span data-ttu-id="5a523-139">이 cmdlet은 이 매개 변수가 지정하는 이름, 키 자격 증명 모음의 이름 및 현재 환경에 따라 비밀의 FQDN(정식 도메인 이름)을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="5a523-139">This cmdlet constructs the fully qualified domain name (FQDN) of a secret based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

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

### <span data-ttu-id="5a523-140">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="5a523-140">-NotBefore</span></span>
<span data-ttu-id="5a523-141">비밀을 사용할 수 없는 **시간(DateTime** 개체)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5a523-141">Specifies the time, as a **DateTime** object, before which the secret cannot be used.</span></span> <span data-ttu-id="5a523-142">이 매개 변수는 UTC를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="5a523-142">This parameter uses UTC.</span></span> <span data-ttu-id="5a523-143">**DateTime 개체를** 얻습니다. **Get-Date** cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="5a523-143">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>

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

### <span data-ttu-id="5a523-144">-SecretValue</span><span class="sxs-lookup"><span data-stu-id="5a523-144">-SecretValue</span></span>
<span data-ttu-id="5a523-145">비밀의 값을 **SecureString** 개체로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5a523-145">Specifies the value for the secret as a **SecureString** object.</span></span> <span data-ttu-id="5a523-146">**SecureString** 개체를 얻습니다. **ConvertTo-SecureString** cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="5a523-146">To obtain a **SecureString** object, use the **ConvertTo-SecureString** cmdlet.</span></span> <span data-ttu-id="5a523-147">자세한 내용은 `Get-Help
ConvertTo-SecureString` .를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="5a523-147">For more information, type `Get-Help
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

### <span data-ttu-id="5a523-148">-Tag</span><span class="sxs-lookup"><span data-stu-id="5a523-148">-Tag</span></span>
<span data-ttu-id="5a523-149">해시 테이블 형식의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="5a523-149">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="5a523-150">예: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="5a523-150">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="5a523-151">-VaultName</span><span class="sxs-lookup"><span data-stu-id="5a523-151">-VaultName</span></span>
<span data-ttu-id="5a523-152">이 비밀이 속한 키 자격 증명 모음의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5a523-152">Specifies the name of the key vault to which this secret belongs.</span></span> <span data-ttu-id="5a523-153">이 cmdlet은 이 매개 변수가 지정하는 이름 및 현재 환경에 따라 키 자격 증명 모음의 FQDN을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="5a523-153">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="5a523-154">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5a523-154">-Confirm</span></span>
<span data-ttu-id="5a523-155">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5a523-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a523-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a523-156">-WhatIf</span></span>
<span data-ttu-id="5a523-157">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="5a523-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a523-158">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5a523-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a523-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a523-159">CommonParameters</span></span>
<span data-ttu-id="5a523-160">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5a523-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a523-161">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5a523-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a523-162">입력</span><span class="sxs-lookup"><span data-stu-id="5a523-162">INPUTS</span></span>

### <span data-ttu-id="5a523-163">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="5a523-163">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span></span>

## <span data-ttu-id="5a523-164">출력</span><span class="sxs-lookup"><span data-stu-id="5a523-164">OUTPUTS</span></span>

### <span data-ttu-id="5a523-165">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="5a523-165">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="5a523-166">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5a523-166">NOTES</span></span>

## <span data-ttu-id="5a523-167">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5a523-167">RELATED LINKS</span></span>

[<span data-ttu-id="5a523-168">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="5a523-168">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)

[<span data-ttu-id="5a523-169">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="5a523-169">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)
