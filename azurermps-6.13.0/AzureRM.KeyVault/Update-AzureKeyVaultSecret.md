---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/update-azurekeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureKeyVaultSecret.md
ms.openlocfilehash: d895485354c33daa4eac57b699358ee0335905be
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711366"
---
# <span data-ttu-id="78210-101">Update-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="78210-101">Update-AzureKeyVaultSecret</span></span>

## <span data-ttu-id="78210-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78210-102">SYNOPSIS</span></span>
<span data-ttu-id="78210-103">키 보관소에서 비밀의 특성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="78210-103">Updates attributes of a secret in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="78210-104">구문과</span><span class="sxs-lookup"><span data-stu-id="78210-104">SYNTAX</span></span>

### <span data-ttu-id="78210-105">기본값 (기본값)</span><span class="sxs-lookup"><span data-stu-id="78210-105">Default (Default)</span></span>
```
Update-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78210-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="78210-106">InputObject</span></span>
```
Update-AzureKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [[-Version] <String>]
 [-Enable <Boolean>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78210-107">설명은</span><span class="sxs-lookup"><span data-stu-id="78210-107">DESCRIPTION</span></span>
<span data-ttu-id="78210-108">**AzureKeyVaultSecret** cmdlet은 키 보관소에서 비밀의 편집 가능한 특성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="78210-108">The **Update-AzureKeyVaultSecret** cmdlet updates editable attributes of a secret in a key vault.</span></span>

## <span data-ttu-id="78210-109">예제의</span><span class="sxs-lookup"><span data-stu-id="78210-109">EXAMPLES</span></span>

### <span data-ttu-id="78210-110">예제 1: 비밀의 특성 수정</span><span class="sxs-lookup"><span data-stu-id="78210-110">Example 1: Modify the attributes of a secret</span></span>
```powershell
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Nbf = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'medium'; 'HR' = 'true'}
PS C:\> $ContentType= 'xml'
PS C:\> Update-AzureKeyVaultSecret -VaultName 'ContosoVault' -Name 'HR' -Expires $Expires -NotBefore $Nbf -ContentType $ContentType -Enable $True -Tag $Tags -PassThru

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

<span data-ttu-id="78210-111">처음 네 개의 명령은 만료 날짜, NotBefore 날짜, 태그, 컨텍스트 형식에 대 한 특성을 정의 하 고 변수에 특성을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="78210-111">The first four commands define attributes for the expiry date, the NotBefore date, tags, and context type, and store the attributes in variables.</span></span>
<span data-ttu-id="78210-112">마지막 명령은 저장 된 변수를 사용 하 여 ContosoVault 이라는 키 보관소에서 HR 이라는 비밀에 대 한 특성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="78210-112">The final command modifies the attributes for the secret named HR in the key vault named ContosoVault, using the stored variables.</span></span>

### <span data-ttu-id="78210-113">예제 2: 비밀 태그 및 콘텐츠 형식 삭제</span><span class="sxs-lookup"><span data-stu-id="78210-113">Example 2: Delete the tags and content type for a secret</span></span>
```
PS C:\> Update-AzureKeyVaultSecret -VaultName 'ContosoVault' -Name 'HR' -Version '9EEA45C6EE50490B9C3176A80AC1A0DF' -ContentType '' -Tag -@{}
```

<span data-ttu-id="78210-114">이 명령은 Contoso 라는 키 보관소에 있는 지정 된 버전의 비밀에 대 한 태그와 콘텐츠 유형을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="78210-114">This command deletes the tags and the content type for the specified version of the secret named HR in the key vault named Contoso.</span></span>

### <span data-ttu-id="78210-115">예제 3: 이름이 해당 이름으로 시작 하는 현재 버전의 비밀을 사용 하지 않도록 설정</span><span class="sxs-lookup"><span data-stu-id="78210-115">Example 3: Disable the current version of secrets whose name begins with IT</span></span>
```
PS C:\> $Vault = 'ContosoVault'
PS C:\> $Prefix = 'IT'
PS C:\> Get-AzureKeyVaultSecret $Vault | Where-Object {$_.Name -like $Prefix + '*'} | Update-AzureKeyVaultSecret -Enable $False
```

<span data-ttu-id="78210-116">첫 번째 명령은 Contoso $Vault 변수에 문자열 값을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="78210-116">The first command stores the string value Contoso in the $Vault variable.</span></span>
<span data-ttu-id="78210-117">두 번째 명령은 $Prefix 변수에 문자열 값을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="78210-117">The second command stores the string value IT in the $Prefix variable.</span></span>
<span data-ttu-id="78210-118">세 번째 명령은 Get-AzureKeyVaultSecret cmdlet을 사용 하 여 지정 된 키 보관소의 비밀을 얻은 다음 해당 비밀을 **Where-개체** cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="78210-118">The third command uses the Get-AzureKeyVaultSecret cmdlet to get the secrets in the specified key vault, and then passes those secrets to the **Where-Object** cmdlet.</span></span> <span data-ttu-id="78210-119">**Where 개체** cmdlet은 해당 문자로 시작 하는 이름에 대 한 비밀 정보를 필터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="78210-119">The **Where-Object** cmdlet filters the secrets for names that begin with the characters IT.</span></span> <span data-ttu-id="78210-120">이 명령은 필터와 일치 하는 비밀을 Update-AzureKeyVaultSecret cmdlet에 연결 하 여 파이프를 비활성화 합니다.</span><span class="sxs-lookup"><span data-stu-id="78210-120">The command pipes the secrets that match the filter to the Update-AzureKeyVaultSecret cmdlet, which disables them.</span></span>

### <span data-ttu-id="78210-121">예제 4: 모든 버전의 비밀에 대 한 ContentType 설정</span><span class="sxs-lookup"><span data-stu-id="78210-121">Example 4: Set the ContentType for all versions of a secret</span></span>
```
PS C:\> $VaultName = 'ContosoVault'
PS C:\> $Name = 'HR'
PS C:\> $ContentType = 'xml'
PS C:\> Get-AzureKeyVaultKey -VaultName $VaultName -Name $Name -IncludeVersions | Update-AzureKeyVaultSecret -ContentType $ContentType
```

<span data-ttu-id="78210-122">처음 세 명령은 *VaultName* , *Name* , *ContentType* 매개 변수에 사용할 문자열 변수를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="78210-122">The first three commands define string variables to use for the *VaultName* , *Name* , and *ContentType* parameters.</span></span> <span data-ttu-id="78210-123">네 번째 명령은 Get-AzureKeyVaultKey cmdlet을 사용 하 여 지정 된 키를 가져오고 Update-AzureKeyVaultSecret cmdlet에 키를 파이프 하 여 콘텐츠 형식을 XML로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="78210-123">The fourth command uses the Get-AzureKeyVaultKey cmdlet to get the specified keys, and pipes the keys to the Update-AzureKeyVaultSecret cmdlet to set their content type to XML.</span></span>

## <span data-ttu-id="78210-124">변수</span><span class="sxs-lookup"><span data-stu-id="78210-124">PARAMETERS</span></span>

### <span data-ttu-id="78210-125">-ContentType</span><span class="sxs-lookup"><span data-stu-id="78210-125">-ContentType</span></span>
<span data-ttu-id="78210-126">비밀의 콘텐츠 형식.</span><span class="sxs-lookup"><span data-stu-id="78210-126">Secret's content type.</span></span>
<span data-ttu-id="78210-127">지정 하지 않으면 비밀의 기존 값이 변경 되지 않고 그대로 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="78210-127">If not specified, the existing value of the secret's content type remains unchanged.</span></span>
<span data-ttu-id="78210-128">빈 문자열을 지정 하 여 기존 콘텐츠 형식 값을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="78210-128">Remove the existing content type value by specifying an empty string.</span></span>

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

### <span data-ttu-id="78210-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78210-129">-DefaultProfile</span></span>
<span data-ttu-id="78210-130">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="78210-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78210-131">-사용</span><span class="sxs-lookup"><span data-stu-id="78210-131">-Enable</span></span>
<span data-ttu-id="78210-132">있는 경우 값이 true 이면 secret를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="78210-132">If present, enable a secret if value is true.</span></span>
<span data-ttu-id="78210-133">값이 false 인 경우 비밀을 비활성화 합니다.</span><span class="sxs-lookup"><span data-stu-id="78210-133">Disable a secret if value is false.</span></span>
<span data-ttu-id="78210-134">지정 하지 않으면 비밀의 사용/사용 안 함 상태에 대 한 기존 값이 변경 되지 않고 그대로 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="78210-134">If not specified, the existing value of the secret's enabled/disabled state remains unchanged.</span></span>

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

### <span data-ttu-id="78210-135">-만료</span><span class="sxs-lookup"><span data-stu-id="78210-135">-Expires</span></span>
<span data-ttu-id="78210-136">UTC 시간에 비밀을 만료 하는 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="78210-136">The expiration time of a secret in UTC time.</span></span>
<span data-ttu-id="78210-137">지정 하지 않으면 비밀의 기존 값이 변경 되지 않고 그대로 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="78210-137">If not specified, the existing value of the secret's expiration time remains unchanged.</span></span>

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

### <span data-ttu-id="78210-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="78210-138">-InputObject</span></span>
<span data-ttu-id="78210-139">비밀 개체</span><span class="sxs-lookup"><span data-stu-id="78210-139">Secret object</span></span>

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

### <span data-ttu-id="78210-140">-이름</span><span class="sxs-lookup"><span data-stu-id="78210-140">-Name</span></span>
<span data-ttu-id="78210-141">비밀 이름.</span><span class="sxs-lookup"><span data-stu-id="78210-141">Secret name.</span></span>
<span data-ttu-id="78210-142">Cmdlet은 자격 증명 정보, 현재 선택 된 환경 및 비밀 이름 으로부터 비밀의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="78210-142">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

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

### <span data-ttu-id="78210-143">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="78210-143">-NotBefore</span></span>
<span data-ttu-id="78210-144">이전에 비밀을 사용할 수 없는 UTC 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="78210-144">The UTC time before which secret can't be used.</span></span>
<span data-ttu-id="78210-145">지정 하지 않으면 비밀의 NotBefore 특성에 대 한 기존 값이 변경 되지 않은 상태로 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="78210-145">If not specified, the existing value of the secret's NotBefore attribute remains unchanged.</span></span>

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

### <span data-ttu-id="78210-146">-PassThru</span><span class="sxs-lookup"><span data-stu-id="78210-146">-PassThru</span></span>
<span data-ttu-id="78210-147">Cmdlet은 기본적으로 개체를 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="78210-147">Cmdlet does not return object by default.</span></span>
<span data-ttu-id="78210-148">이 스위치가 지정 된 경우 비밀 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="78210-148">If this switch is specified, return Secret object.</span></span>

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

### <span data-ttu-id="78210-149">태그</span><span class="sxs-lookup"><span data-stu-id="78210-149">-Tag</span></span>
<span data-ttu-id="78210-150">비밀 태그를 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="78210-150">A hashtable representing secret tags.</span></span>
<span data-ttu-id="78210-151">지정 하지 않으면 비밀의 기존 태그가 변경 되지 않은 상태로 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="78210-151">If not specified, the existing tags of the secret remain unchanged.</span></span>
<span data-ttu-id="78210-152">빈 Hashtable을 지정 하 여 태그를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="78210-152">Remove a tag by specifying an empty Hashtable.</span></span>

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

### <span data-ttu-id="78210-153">-VaultName</span><span class="sxs-lookup"><span data-stu-id="78210-153">-VaultName</span></span>
<span data-ttu-id="78210-154">자격 증명 모음 이름</span><span class="sxs-lookup"><span data-stu-id="78210-154">Vault name.</span></span>
<span data-ttu-id="78210-155">Cmdlet은 이름 및 현재 선택 된 환경을 기준으로 자격 증명 모음의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="78210-155">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="78210-156">-버전</span><span class="sxs-lookup"><span data-stu-id="78210-156">-Version</span></span>
<span data-ttu-id="78210-157">비밀 버전.</span><span class="sxs-lookup"><span data-stu-id="78210-157">Secret version.</span></span>
<span data-ttu-id="78210-158">Cmdlet은 자격 증명 정보, 현재 선택 된 환경, 비밀 이름 및 비밀 버전의 비밀에 대 한 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="78210-158">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment, secret name and secret version.</span></span>

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

### <span data-ttu-id="78210-159">-확인</span><span class="sxs-lookup"><span data-stu-id="78210-159">-Confirm</span></span>
<span data-ttu-id="78210-160">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="78210-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78210-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78210-161">-WhatIf</span></span>
<span data-ttu-id="78210-162">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="78210-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78210-163">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="78210-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78210-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78210-164">CommonParameters</span></span>
<span data-ttu-id="78210-165">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="78210-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78210-166">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78210-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78210-167">입력</span><span class="sxs-lookup"><span data-stu-id="78210-167">INPUTS</span></span>

### <span data-ttu-id="78210-168">Microsoft. KeyVault. PSKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="78210-168">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span></span>
<span data-ttu-id="78210-169">매개 변수: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="78210-169">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="78210-170">출력</span><span class="sxs-lookup"><span data-stu-id="78210-170">OUTPUTS</span></span>

### <span data-ttu-id="78210-171">Microsoft. KeyVault. PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="78210-171">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="78210-172">상속자</span><span class="sxs-lookup"><span data-stu-id="78210-172">NOTES</span></span>

## <span data-ttu-id="78210-173">관련 링크</span><span class="sxs-lookup"><span data-stu-id="78210-173">RELATED LINKS</span></span>
