---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/update-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultSecret.md
ms.openlocfilehash: 975395c471a08eac745bd8a9ab07cec826d5c038
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976859"
---
# <span data-ttu-id="36520-101">Update-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="36520-101">Update-AzKeyVaultSecret</span></span>

## <span data-ttu-id="36520-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36520-102">SYNOPSIS</span></span>
<span data-ttu-id="36520-103">키 자격 증명 모음에서 비밀의 특성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="36520-103">Updates attributes of a secret in a key vault.</span></span>

## <span data-ttu-id="36520-104">구문</span><span class="sxs-lookup"><span data-stu-id="36520-104">SYNTAX</span></span>

### <span data-ttu-id="36520-105">기본값(기본값)</span><span class="sxs-lookup"><span data-stu-id="36520-105">Default (Default)</span></span>
```
Update-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36520-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="36520-106">InputObject</span></span>
```
Update-AzKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36520-107">설명</span><span class="sxs-lookup"><span data-stu-id="36520-107">DESCRIPTION</span></span>
<span data-ttu-id="36520-108">**Update-AzKeyVaultSecret cmdlet은** 키 자격 증명 모음에서 비밀의 편집 가능한 특성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="36520-108">The **Update-AzKeyVaultSecret** cmdlet updates editable attributes of a secret in a key vault.</span></span>

## <span data-ttu-id="36520-109">예제</span><span class="sxs-lookup"><span data-stu-id="36520-109">EXAMPLES</span></span>

### <span data-ttu-id="36520-110">예제 1: 비밀의 특성 수정</span><span class="sxs-lookup"><span data-stu-id="36520-110">Example 1: Modify the attributes of a secret</span></span>
```powershell
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Nbf = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'medium'; 'HR' = 'true'}
PS C:\> $ContentType= 'xml'
PS C:\> Update-AzKeyVaultSecret -VaultName 'ContosoVault' -Name 'HR' -Expires $Expires -NotBefore $Nbf -ContentType $ContentType -Enable $True -Tag $Tags -PassThru

Vault Name   : ContosoVault
Name         : HR
Version      : d476edfcd3544017a03bc49c1f3abec0
Id           : https://ContosoVault.vault.azure.net:443/secrets/HR/d476edfcd3544017a03bc49c1f3abec0
Enabled      : True
Expires      : 5/25/2020 8:01:58 PM
Not Before   : 5/25/2018 8:02:02 PM
Created      : 4/11/2018 11:45:06 PM
Updated      : 5/25/2018 8:02:45 PM
Content Type : xml
Tags         : Name      Value
               Severity  medium
               HR        true
```

<span data-ttu-id="36520-111">처음 네 가지 명령은 만료 날짜, NotBefore 날짜, 태그 및 컨텍스트 형식에 대한 특성을 정의하고, 특성을 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="36520-111">The first four commands define attributes for the expiry date, the NotBefore date, tags, and context type, and store the attributes in variables.</span></span>
<span data-ttu-id="36520-112">최종 명령은 저장된 변수를 사용하여 ContosoVault라는 키 자격 증명 모음의 HR이라는 비밀의 특성을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="36520-112">The final command modifies the attributes for the secret named HR in the key vault named ContosoVault, using the stored variables.</span></span>

### <span data-ttu-id="36520-113">예제 2: 비밀에 대한 태그 및 콘텐츠 형식 삭제</span><span class="sxs-lookup"><span data-stu-id="36520-113">Example 2: Delete the tags and content type for a secret</span></span>
```
PS C:\> Update-AzKeyVaultSecret -VaultName 'ContosoVault' -Name 'HR' -Version '9EEA45C6EE50490B9C3176A80AC1A0DF' -ContentType '' -Tag -@{}
```

<span data-ttu-id="36520-114">이 명령은 Contoso라는 키 자격 증명 모음에서 HR이라는 비밀의 지정된 버전에 대한 태그 및 콘텐츠 형식을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="36520-114">This command deletes the tags and the content type for the specified version of the secret named HR in the key vault named Contoso.</span></span>

### <span data-ttu-id="36520-115">예제 3: 이름이 IT로 시작하는 현재 버전의 비밀을 사용하지 않도록 설정</span><span class="sxs-lookup"><span data-stu-id="36520-115">Example 3: Disable the current version of secrets whose name begins with IT</span></span>
```
PS C:\> $Vault = 'ContosoVault'
PS C:\> $Prefix = 'IT'
PS C:\> Get-AzKeyVaultSecret $Vault | Where-Object {$_.Name -like $Prefix + '*'} | Update-AzKeyVaultSecret -Enable $False
```

<span data-ttu-id="36520-116">첫 번째 명령은 문자열 값을 Contoso 변수에 $Vault 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="36520-116">The first command stores the string value Contoso in the $Vault variable.</span></span>
<span data-ttu-id="36520-117">두 번째 명령은 문자열 값 IT를 $Prefix 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="36520-117">The second command stores the string value IT in the $Prefix variable.</span></span>
<span data-ttu-id="36520-118">세 번째 명령은 Get-AzKeyVaultSecret cmdlet을 사용하여 지정된 키 자격 증명 모음에서 비밀을 얻은 다음 해당 비밀을 **Where-Object** cmdlet에 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="36520-118">The third command uses the Get-AzKeyVaultSecret cmdlet to get the secrets in the specified key vault, and then passes those secrets to the **Where-Object** cmdlet.</span></span> <span data-ttu-id="36520-119">**Where-Object** cmdlet은 IT 문자로 시작하는 이름에 대한 비밀을 필터합니다.</span><span class="sxs-lookup"><span data-stu-id="36520-119">The **Where-Object** cmdlet filters the secrets for names that begin with the characters IT.</span></span> <span data-ttu-id="36520-120">명령은 필터와 일치하는 비밀을 Update-AzKeyVaultSecret cmdlet에 파이프합니다.</span><span class="sxs-lookup"><span data-stu-id="36520-120">The command pipes the secrets that match the filter to the Update-AzKeyVaultSecret cmdlet, which disables them.</span></span>

### <span data-ttu-id="36520-121">예제 4: 모든 버전의 비밀에 ContentType 설정</span><span class="sxs-lookup"><span data-stu-id="36520-121">Example 4: Set the ContentType for all versions of a secret</span></span>
```
PS C:\> $VaultName = 'ContosoVault'
PS C:\> $Name = 'HR'
PS C:\> $ContentType = 'xml'
PS C:\> Get-AzKeyVaultKey -VaultName $VaultName -Name $Name -IncludeVersions | Update-AzKeyVaultSecret -ContentType $ContentType
```

<span data-ttu-id="36520-122">처음 세 명령은 *VaultName,* *Name* 및 ContentType 매개 변수에 사용할 문자열 *변수를 정의합니다.*</span><span class="sxs-lookup"><span data-stu-id="36520-122">The first three commands define string variables to use for the *VaultName*, *Name*, and *ContentType* parameters.</span></span> <span data-ttu-id="36520-123">네 번째 명령은 Get-AzKeyVaultKey cmdlet을 사용하여 지정된 키를 얻게 하여 해당 Update-AzKeyVaultSecret cmdlet에 키를 파이프하여 해당 콘텐츠 형식을 XML로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="36520-123">The fourth command uses the Get-AzKeyVaultKey cmdlet to get the specified keys, and pipes the keys to the Update-AzKeyVaultSecret cmdlet to set their content type to XML.</span></span>

## <span data-ttu-id="36520-124">매개 변수</span><span class="sxs-lookup"><span data-stu-id="36520-124">PARAMETERS</span></span>

### <span data-ttu-id="36520-125">-ContentType</span><span class="sxs-lookup"><span data-stu-id="36520-125">-ContentType</span></span>
<span data-ttu-id="36520-126">비밀의 콘텐츠 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="36520-126">Secret's content type.</span></span>
<span data-ttu-id="36520-127">지정하지 않으면 비밀의 콘텐츠 형식의 기존 값은 변경되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="36520-127">If not specified, the existing value of the secret's content type remains unchanged.</span></span>
<span data-ttu-id="36520-128">빈 문자열을 지정하여 기존 콘텐츠 형식 값을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="36520-128">Remove the existing content type value by specifying an empty string.</span></span>

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

### <span data-ttu-id="36520-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36520-129">-DefaultProfile</span></span>
<span data-ttu-id="36520-130">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="36520-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36520-131">-사용하도록 설정</span><span class="sxs-lookup"><span data-stu-id="36520-131">-Enable</span></span>
<span data-ttu-id="36520-132">있는 경우 값이 true이면 비밀을 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="36520-132">If present, enable a secret if value is true.</span></span>
<span data-ttu-id="36520-133">값이 false이면 비밀을 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="36520-133">Disable a secret if value is false.</span></span>
<span data-ttu-id="36520-134">지정하지 않으면 비밀의 사용 가능/사용 안 함 상태의 기존 값은 변경되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="36520-134">If not specified, the existing value of the secret's enabled/disabled state remains unchanged.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36520-135">-만료</span><span class="sxs-lookup"><span data-stu-id="36520-135">-Expires</span></span>
<span data-ttu-id="36520-136">UTC 시간의 비밀의 만료 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="36520-136">The expiration time of a secret in UTC time.</span></span>
<span data-ttu-id="36520-137">지정하지 않으면 비밀의 만료 시간의 기존 값은 변경되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="36520-137">If not specified, the existing value of the secret's expiration time remains unchanged.</span></span>

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

### <span data-ttu-id="36520-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="36520-138">-InputObject</span></span>
<span data-ttu-id="36520-139">비밀 개체</span><span class="sxs-lookup"><span data-stu-id="36520-139">Secret object</span></span>

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

### <span data-ttu-id="36520-140">-Name</span><span class="sxs-lookup"><span data-stu-id="36520-140">-Name</span></span>
<span data-ttu-id="36520-141">비밀 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="36520-141">Secret name.</span></span>
<span data-ttu-id="36520-142">Cmdlet은 자격 증명 모음 이름, 현재 선택한 환경 및 비밀 이름의 비밀의 FQDN을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="36520-142">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

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

### <span data-ttu-id="36520-143">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="36520-143">-NotBefore</span></span>
<span data-ttu-id="36520-144">비밀을 사용할 수 없는 UTC 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="36520-144">The UTC time before which secret can't be used.</span></span>
<span data-ttu-id="36520-145">지정하지 않으면 비밀의 NotBefore 특성의 기존 값은 변경되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="36520-145">If not specified, the existing value of the secret's NotBefore attribute remains unchanged.</span></span>

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

### <span data-ttu-id="36520-146">-PassThru</span><span class="sxs-lookup"><span data-stu-id="36520-146">-PassThru</span></span>
<span data-ttu-id="36520-147">Cmdlet은 기본적으로 개체를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="36520-147">Cmdlet does not return object by default.</span></span>
<span data-ttu-id="36520-148">이 스위치가 지정되어 있는 경우 비밀 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="36520-148">If this switch is specified, return Secret object.</span></span>

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

### <span data-ttu-id="36520-149">-Tag</span><span class="sxs-lookup"><span data-stu-id="36520-149">-Tag</span></span>
<span data-ttu-id="36520-150">비밀 태그를 나타내는 해시테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="36520-150">A hashtable representing secret tags.</span></span>
<span data-ttu-id="36520-151">지정하지 않으면 비밀의 기존 태그는 변경되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="36520-151">If not specified, the existing tags of the secret remain unchanged.</span></span>
<span data-ttu-id="36520-152">빈 해시테이블을 지정하여 태그를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="36520-152">Remove a tag by specifying an empty Hashtable.</span></span>

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

### <span data-ttu-id="36520-153">-VaultName</span><span class="sxs-lookup"><span data-stu-id="36520-153">-VaultName</span></span>
<span data-ttu-id="36520-154">자격 증명 모음 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="36520-154">Vault name.</span></span>
<span data-ttu-id="36520-155">Cmdlet은 이름 및 현재 선택한 환경을 기반으로 자격 증명 모음의 FQDN을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="36520-155">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="36520-156">-Version</span><span class="sxs-lookup"><span data-stu-id="36520-156">-Version</span></span>
<span data-ttu-id="36520-157">비밀 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="36520-157">Secret version.</span></span>
<span data-ttu-id="36520-158">Cmdlet은 자격 증명 모음 이름, 현재 선택한 환경, 비밀 이름 및 비밀 버전에서 비밀의 FQDN을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="36520-158">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment, secret name and secret version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SecretVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36520-159">-확인</span><span class="sxs-lookup"><span data-stu-id="36520-159">-Confirm</span></span>
<span data-ttu-id="36520-160">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="36520-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36520-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36520-161">-WhatIf</span></span>
<span data-ttu-id="36520-162">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="36520-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36520-163">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="36520-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36520-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36520-164">CommonParameters</span></span>
<span data-ttu-id="36520-165">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="36520-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36520-166">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="36520-166">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36520-167">입력</span><span class="sxs-lookup"><span data-stu-id="36520-167">INPUTS</span></span>

### <span data-ttu-id="36520-168">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="36520-168">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span></span>

## <span data-ttu-id="36520-169">출력</span><span class="sxs-lookup"><span data-stu-id="36520-169">OUTPUTS</span></span>

### <span data-ttu-id="36520-170">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="36520-170">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="36520-171">참고 사항</span><span class="sxs-lookup"><span data-stu-id="36520-171">NOTES</span></span>

## <span data-ttu-id="36520-172">관련 링크</span><span class="sxs-lookup"><span data-stu-id="36520-172">RELATED LINKS</span></span>
