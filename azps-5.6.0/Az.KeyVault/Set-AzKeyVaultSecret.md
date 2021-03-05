---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 9FC72DE9-46BB-4CB5-9880-F53756DBE012
online version: https://docs.microsoft.com/powershell/module/az.keyvault/set-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultSecret.md
ms.openlocfilehash: a9c104bfc1935f65969e11af8de0abdb4f46c3e7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980400"
---
# <span data-ttu-id="fe8dd-101">Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="fe8dd-101">Set-AzKeyVaultSecret</span></span>

## <span data-ttu-id="fe8dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe8dd-102">SYNOPSIS</span></span>
<span data-ttu-id="fe8dd-103">키 자격 증명 모음에서 비밀을 생성하거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="fe8dd-103">Creates or updates a secret in a key vault.</span></span>

## <span data-ttu-id="fe8dd-104">구문</span><span class="sxs-lookup"><span data-stu-id="fe8dd-104">SYNTAX</span></span>

### <span data-ttu-id="fe8dd-105">기본값(기본값)</span><span class="sxs-lookup"><span data-stu-id="fe8dd-105">Default (Default)</span></span>
```
Set-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [-SecretValue] <SecureString> [-Disable]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe8dd-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="fe8dd-106">InputObject</span></span>
```
Set-AzKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [-SecretValue] <SecureString> [-Disable]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe8dd-107">설명</span><span class="sxs-lookup"><span data-stu-id="fe8dd-107">DESCRIPTION</span></span>
<span data-ttu-id="fe8dd-108">**Set-AzKeyVaultSecret cmdlet은** Azure Key Vault의 키 자격 증명 모음에서 비밀을 만들거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="fe8dd-108">The **Set-AzKeyVaultSecret** cmdlet creates or updates a secret in a key vault in Azure Key Vault.</span></span> <span data-ttu-id="fe8dd-109">비밀이 없는 경우 이 cmdlet이 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fe8dd-109">If the secret does not exist, this cmdlet creates it.</span></span> <span data-ttu-id="fe8dd-110">비밀이 이미 있는 경우 이 cmdlet은 해당 비밀의 새 버전을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fe8dd-110">If the secret already exists, this cmdlet creates a new version of that secret.</span></span>

## <span data-ttu-id="fe8dd-111">예제</span><span class="sxs-lookup"><span data-stu-id="fe8dd-111">EXAMPLES</span></span>

### <span data-ttu-id="fe8dd-112">예제 1: 기본 특성을 사용하여 비밀 값 수정</span><span class="sxs-lookup"><span data-stu-id="fe8dd-112">Example 1: Modify the value of a secret using default attributes</span></span>
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

<span data-ttu-id="fe8dd-113">첫 번째 명령은 **ConvertTo-SecureString** cmdlet을 사용하여 문자열을 보안 문자열로 변환한 다음 해당 문자열을 $Secret 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="fe8dd-113">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Secret variable.</span></span> <span data-ttu-id="fe8dd-114">자세한 내용은 `Get-Help
ConvertTo-SecureString` 를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="fe8dd-114">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>
<span data-ttu-id="fe8dd-115">두 번째 명령은 Contoso라는 키 자격 증명 모음에서 ITSecret이라는 비밀의 값을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="fe8dd-115">The second command modifies value of the secret named ITSecret in the key vault named Contoso.</span></span> <span data-ttu-id="fe8dd-116">비밀 값은 에 저장된 값이 $Secret.</span><span class="sxs-lookup"><span data-stu-id="fe8dd-116">The secret value becomes the value stored in $Secret.</span></span>

### <span data-ttu-id="fe8dd-117">예제 2: 사용자 지정 특성을 사용하여 비밀 값 수정</span><span class="sxs-lookup"><span data-stu-id="fe8dd-117">Example 2: Modify the value of a secret using custom attributes</span></span>
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

<span data-ttu-id="fe8dd-118">첫 번째 명령은 **ConvertTo-SecureString** cmdlet을 사용하여 문자열을 보안 문자열로 변환한 다음 해당 문자열을 $Secret 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="fe8dd-118">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Secret variable.</span></span> <span data-ttu-id="fe8dd-119">자세한 내용은 `Get-Help
ConvertTo-SecureString` 를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="fe8dd-119">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>
<span data-ttu-id="fe8dd-120">다음 명령은 만료 날짜, 태그 및 컨텍스트 형식에 대한 사용자 지정 특성을 정의하고, 특성을 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="fe8dd-120">The next commands define custom attributes for the expiry date, tags, and context type, and store the attributes in variables.</span></span>
<span data-ttu-id="fe8dd-121">최종 명령은 이전에 변수로 지정된 값을 사용하여 Contoso라는 키 자격 증명 모음에서 ITSecret이라는 비밀의 값을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="fe8dd-121">The final command modifies values of the secret named ITSecret in the key vault named Contoso, by using the values specified previously as variables.</span></span>

## <span data-ttu-id="fe8dd-122">매개 변수</span><span class="sxs-lookup"><span data-stu-id="fe8dd-122">PARAMETERS</span></span>

### <span data-ttu-id="fe8dd-123">-ContentType</span><span class="sxs-lookup"><span data-stu-id="fe8dd-123">-ContentType</span></span>
<span data-ttu-id="fe8dd-124">비밀의 콘텐츠 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fe8dd-124">Specifies the content type of a secret.</span></span>
<span data-ttu-id="fe8dd-125">기존 콘텐츠 형식을 삭제하려면 빈 문자열을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fe8dd-125">To delete the existing content type, specify an empty string.</span></span>

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

### <span data-ttu-id="fe8dd-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe8dd-126">-DefaultProfile</span></span>
<span data-ttu-id="fe8dd-127">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="fe8dd-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fe8dd-128">-사용 안</span><span class="sxs-lookup"><span data-stu-id="fe8dd-128">-Disable</span></span>
<span data-ttu-id="fe8dd-129">이 cmdlet이 비밀을 사용하지 않도록 설정되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fe8dd-129">Indicates that this cmdlet disables a secret.</span></span>

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

### <span data-ttu-id="fe8dd-130">-만료</span><span class="sxs-lookup"><span data-stu-id="fe8dd-130">-Expires</span></span>
<span data-ttu-id="fe8dd-131">이 cmdlet이 업데이트하는 비밀에 대한 만료 시간을 **DateTime** 개체로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fe8dd-131">Specifies the expiration time, as a **DateTime** object, for the secret that this cmdlet updates.</span></span>
<span data-ttu-id="fe8dd-132">이 매개 변수는 UTC(조정된 유니버설 시간)를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="fe8dd-132">This parameter uses Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="fe8dd-133">DateTime 개체를 **얻은** 경우 **Get-Date** cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="fe8dd-133">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="fe8dd-134">자세한 내용은 `Get-Help Get-Date` 를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="fe8dd-134">For more information, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="fe8dd-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fe8dd-135">-InputObject</span></span>
<span data-ttu-id="fe8dd-136">비밀 개체</span><span class="sxs-lookup"><span data-stu-id="fe8dd-136">Secret object</span></span>

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

### <span data-ttu-id="fe8dd-137">-Name</span><span class="sxs-lookup"><span data-stu-id="fe8dd-137">-Name</span></span>
<span data-ttu-id="fe8dd-138">수정할 비밀의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fe8dd-138">Specifies the name of a secret to modify.</span></span> <span data-ttu-id="fe8dd-139">이 cmdlet은 이 매개 변수가 지정하는 이름, 키 자격 증명 모음의 이름 및 현재 환경에 따라 비밀의 완전히 자격을 갖춘 도메인 이름(FQDN)을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="fe8dd-139">This cmdlet constructs the fully qualified domain name (FQDN) of a secret based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

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

### <span data-ttu-id="fe8dd-140">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="fe8dd-140">-NotBefore</span></span>
<span data-ttu-id="fe8dd-141">비밀을 사용할 수 없는 **시간을 DateTime** 개체로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fe8dd-141">Specifies the time, as a **DateTime** object, before which the secret cannot be used.</span></span> <span data-ttu-id="fe8dd-142">이 매개 변수는 UTC를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="fe8dd-142">This parameter uses UTC.</span></span> <span data-ttu-id="fe8dd-143">DateTime 개체를 **얻은** 경우 **Get-Date** cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="fe8dd-143">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>

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

### <span data-ttu-id="fe8dd-144">-SecretValue</span><span class="sxs-lookup"><span data-stu-id="fe8dd-144">-SecretValue</span></span>
<span data-ttu-id="fe8dd-145">비밀에 대한 값을 **SecureString 개체로 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="fe8dd-145">Specifies the value for the secret as a **SecureString** object.</span></span> <span data-ttu-id="fe8dd-146">**SecureString** 개체를 얻은 경우 **ConvertTo-SecureString** cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="fe8dd-146">To obtain a **SecureString** object, use the **ConvertTo-SecureString** cmdlet.</span></span> <span data-ttu-id="fe8dd-147">자세한 내용은 `Get-Help
ConvertTo-SecureString` 를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="fe8dd-147">For more information, type `Get-Help
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

### <span data-ttu-id="fe8dd-148">-Tag</span><span class="sxs-lookup"><span data-stu-id="fe8dd-148">-Tag</span></span>
<span data-ttu-id="fe8dd-149">해시 테이블의 형태로 키 값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="fe8dd-149">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="fe8dd-150">예: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="fe8dd-150">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="fe8dd-151">-VaultName</span><span class="sxs-lookup"><span data-stu-id="fe8dd-151">-VaultName</span></span>
<span data-ttu-id="fe8dd-152">이 비밀이 속한 키 자격 증명 모음의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fe8dd-152">Specifies the name of the key vault to which this secret belongs.</span></span> <span data-ttu-id="fe8dd-153">이 cmdlet은 이 매개 변수가 지정하는 이름과 현재 환경을 기반으로 키 자격 증명 모음의 FQDN을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="fe8dd-153">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="fe8dd-154">-확인</span><span class="sxs-lookup"><span data-stu-id="fe8dd-154">-Confirm</span></span>
<span data-ttu-id="fe8dd-155">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="fe8dd-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe8dd-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe8dd-156">-WhatIf</span></span>
<span data-ttu-id="fe8dd-157">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="fe8dd-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe8dd-158">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fe8dd-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe8dd-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe8dd-159">CommonParameters</span></span>
<span data-ttu-id="fe8dd-160">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="fe8dd-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe8dd-161">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fe8dd-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe8dd-162">입력</span><span class="sxs-lookup"><span data-stu-id="fe8dd-162">INPUTS</span></span>

### <span data-ttu-id="fe8dd-163">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="fe8dd-163">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span></span>

## <span data-ttu-id="fe8dd-164">출력</span><span class="sxs-lookup"><span data-stu-id="fe8dd-164">OUTPUTS</span></span>

### <span data-ttu-id="fe8dd-165">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="fe8dd-165">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="fe8dd-166">참고 사항</span><span class="sxs-lookup"><span data-stu-id="fe8dd-166">NOTES</span></span>

## <span data-ttu-id="fe8dd-167">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fe8dd-167">RELATED LINKS</span></span>

[<span data-ttu-id="fe8dd-168">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="fe8dd-168">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)

[<span data-ttu-id="fe8dd-169">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="fe8dd-169">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)
