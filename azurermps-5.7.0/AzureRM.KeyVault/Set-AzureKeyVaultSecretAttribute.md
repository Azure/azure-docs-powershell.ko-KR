---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: E2A45461-6B41-42FF-A874-A4CEFC867A33
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultsecretattribute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultSecretAttribute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultSecretAttribute.md
ms.openlocfilehash: edb4c166fbacbf0ee394b10ff475fe90dc00a67d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711423"
---
# <span data-ttu-id="1c636-101">Set-AzureKeyVaultSecretAttribute</span><span class="sxs-lookup"><span data-stu-id="1c636-101">Set-AzureKeyVaultSecretAttribute</span></span>

## <span data-ttu-id="1c636-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c636-102">SYNOPSIS</span></span>
<span data-ttu-id="1c636-103">키 보관소에서 비밀의 특성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c636-103">Updates attributes of a secret in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1c636-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1c636-104">SYNTAX</span></span>

### <span data-ttu-id="1c636-105">기본값</span><span class="sxs-lookup"><span data-stu-id="1c636-105">Default</span></span>
```
Set-AzureKeyVaultSecretAttribute [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-Enable <Boolean>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c636-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="1c636-106">InputObject</span></span>
```
Set-AzureKeyVaultSecretAttribute [-InputObject] <PSKeyVaultSecretIdentityItem> [[-Version] <String>]
 [-Enable <Boolean>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c636-107">설명은</span><span class="sxs-lookup"><span data-stu-id="1c636-107">DESCRIPTION</span></span>
<span data-ttu-id="1c636-108">**AzureKeyVaultSecretAttribute** cmdlet은 키 보관소에서 비밀의 편집 가능한 특성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c636-108">The **Set-AzureKeyVaultSecretAttribute** cmdlet updates editable attributes of a secret in a key vault.</span></span>

## <span data-ttu-id="1c636-109">예제의</span><span class="sxs-lookup"><span data-stu-id="1c636-109">EXAMPLES</span></span>

### <span data-ttu-id="1c636-110">예제 1: 비밀의 특성 수정</span><span class="sxs-lookup"><span data-stu-id="1c636-110">Example 1: Modify the attributes of a secret</span></span>
```
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Nbf = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'medium'; 'HR' = null}
PS C:\> $ContentType= 'xml'
PS C:\> Set-AzureKeyVaultSecretAttribute -VaultName 'ContosoVault' -Name 'HR' -Expires $Expires -NotBefore $Nbf -ContentType $ContentType -Enable $True -Tag $Tags -PassThru
```

<span data-ttu-id="1c636-111">처음 네 개의 명령은 만료 날짜, NotBefore 날짜, 태그, 컨텍스트 형식에 대 한 특성을 정의 하 고 변수에 특성을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c636-111">The first four commands define attributes for the expiry date, the NotBefore date, tags, and context type, and store the attributes in variables.</span></span>

<span data-ttu-id="1c636-112">마지막 명령은 저장 된 변수를 사용 하 여 ContosoVault 이라는 키 보관소에서 HR 이라는 비밀에 대 한 특성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c636-112">The final command modifies the attributes for the secret named HR in the key vault named ContosoVault, using the stored variables.</span></span>

### <span data-ttu-id="1c636-113">예제 2: 비밀 태그 및 콘텐츠 형식 삭제</span><span class="sxs-lookup"><span data-stu-id="1c636-113">Example 2: Delete the tags and content type for a secret</span></span>
```
PS C:\>Set-AzureKeyVaultSecretAttribute -VaultName 'ContosoVault' -Name 'HR' -Version '9EEA45C6EE50490B9C3176A80AC1A0DF' -ContentType '' -Tag -@{}
```

<span data-ttu-id="1c636-114">이 명령은 Contoso 라는 키 보관소에 있는 지정 된 버전의 비밀에 대 한 태그와 콘텐츠 유형을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c636-114">This command deletes the tags and the content type for the specified version of the secret named HR in the key vault named Contoso.</span></span>

### <span data-ttu-id="1c636-115">예제 3: 이름이 해당 이름으로 시작 하는 현재 버전의 비밀을 사용 하지 않도록 설정</span><span class="sxs-lookup"><span data-stu-id="1c636-115">Example 3: Disable the current version of secrets whose name begins with IT</span></span>
```
PS C:\> $Vault = 'ContosoVault'
PS C:\> $Prefix = 'IT'
PS C:\> Get-AzureKeyVaultSecret $Vault | Where-Object {$_.Name -like $Prefix + '*'} | Set-AzureKeyVaultSecretAttribute -Enable $False
```

<span data-ttu-id="1c636-116">첫 번째 명령은 Contoso $Vault 변수에 문자열 값을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c636-116">The first command stores the string value Contoso in the $Vault variable.</span></span>

<span data-ttu-id="1c636-117">두 번째 명령은 $Prefix 변수에 문자열 값을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c636-117">The second command stores the string value IT in the $Prefix variable.</span></span>

<span data-ttu-id="1c636-118">세 번째 명령은 Get-AzureKeyVaultSecret cmdlet을 사용 하 여 지정 된 키 보관소의 비밀을 얻은 다음 해당 비밀을 **Where-개체** cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c636-118">The third command uses the Get-AzureKeyVaultSecret cmdlet to get the secrets in the specified key vault, and then passes those secrets to the **Where-Object** cmdlet.</span></span> <span data-ttu-id="1c636-119">**Where 개체** cmdlet은 해당 문자로 시작 하는 이름에 대 한 비밀 정보를 필터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c636-119">The **Where-Object** cmdlet filters the secrets for names that begin with the characters IT.</span></span> <span data-ttu-id="1c636-120">이 명령은 필터와 일치 하는 비밀을 Set-AzureKeyVaultSecretAttribute cmdlet에 연결 하 여 파이프를 비활성화 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c636-120">The command pipes the secrets that match the filter to the Set-AzureKeyVaultSecretAttribute cmdlet, which disables them.</span></span>

### <span data-ttu-id="1c636-121">예제 4: 모든 버전의 비밀에 대 한 ContentType 설정</span><span class="sxs-lookup"><span data-stu-id="1c636-121">Example 4: Set the ContentType for all versions of a secret</span></span>
```
PS C:\>$VaultName = 'ContosoVault'
PS C:\> $Name = 'HR'
PS C:\> $ContentType = 'xml'
PS C:\> Get-AzureKeyVaultKey -VaultName $VaultName -Name $Name -IncludeVersions | Set-AzureKeyVaultSecretAttribute -ContentType $ContentType
```

<span data-ttu-id="1c636-122">처음 세 명령은 *VaultName* , *Name* , *ContentType* 매개 변수에 사용할 문자열 변수를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c636-122">The first three commands define string variables to use for the *VaultName* , *Name* , and *ContentType* parameters.</span></span> <span data-ttu-id="1c636-123">네 번째 명령은 Get-AzureKeyVaultKey cmdlet을 사용 하 여 지정 된 키를 가져오고 Set-AzureKeyVaultSecretAttribute cmdlet에 키를 파이프 하 여 콘텐츠 형식을 XML로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c636-123">The fourth command uses the Get-AzureKeyVaultKey cmdlet to get the specified keys, and pipes the keys to the Set-AzureKeyVaultSecretAttribute cmdlet to set their content type to XML.</span></span>

## <span data-ttu-id="1c636-124">변수</span><span class="sxs-lookup"><span data-stu-id="1c636-124">PARAMETERS</span></span>

### <span data-ttu-id="1c636-125">-ContentType</span><span class="sxs-lookup"><span data-stu-id="1c636-125">-ContentType</span></span>
<span data-ttu-id="1c636-126">비밀의 콘텐츠 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c636-126">Specifies the content type of a secret.</span></span> <span data-ttu-id="1c636-127">이 매개 변수를 지정 하지 않으면 현재 비밀의 콘텐츠 형식이 변경 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1c636-127">If you do not specify this parameter, there is no change to the current secret's content type.</span></span> <span data-ttu-id="1c636-128">기존 콘텐츠 형식을 제거 하려면 빈 문자열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c636-128">To remove the existing content type, specify an empty string.</span></span>

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

### <span data-ttu-id="1c636-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c636-129">-DefaultProfile</span></span>
<span data-ttu-id="1c636-130">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="1c636-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1c636-131">-사용</span><span class="sxs-lookup"><span data-stu-id="1c636-131">-Enable</span></span>
<span data-ttu-id="1c636-132">비밀을 사용할지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="1c636-132">Indicates whether to enable a secret.</span></span> <span data-ttu-id="1c636-133">비밀을 사용 하지 않도록 $False 지정 하거나 비밀을 사용 하도록 $True 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c636-133">Specify $False to disable a secret, or $True to enable a secret.</span></span> <span data-ttu-id="1c636-134">이 매개 변수를 지정 하지 않으면 현재 비밀의 사용 또는 사용 안 함 상태가 변경 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1c636-134">If you do not specify this parameter, there is no change to the current secret's enabled or disabled state.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c636-135">-만료</span><span class="sxs-lookup"><span data-stu-id="1c636-135">-Expires</span></span>
<span data-ttu-id="1c636-136">비밀을 만료 하는 날짜와 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c636-136">Specifies the date and time that a secret expires.</span></span>

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

### <span data-ttu-id="1c636-137">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1c636-137">-InputObject</span></span>
<span data-ttu-id="1c636-138">비밀 개체</span><span class="sxs-lookup"><span data-stu-id="1c636-138">Secret object</span></span>

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

### <span data-ttu-id="1c636-139">-이름</span><span class="sxs-lookup"><span data-stu-id="1c636-139">-Name</span></span>
<span data-ttu-id="1c636-140">비밀의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c636-140">Specifies the name of a secret.</span></span> <span data-ttu-id="1c636-141">이 cmdlet은이 매개 변수에서 지정 하는 이름, 키 보관소의 이름 및 현재 환경에 따라 비밀의 FQDN (정규화 된 도메인 이름)을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c636-141">This cmdlet constructs the fully qualified domain name (FQDN) of a secret based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

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

### <span data-ttu-id="1c636-142">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="1c636-142">-NotBefore</span></span>
<span data-ttu-id="1c636-143">비밀을 사용할 수 없는 UTC (협정 세계시)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c636-143">Specifies the Coordinated Universal Time (UTC) before which the secret can't be used.</span></span>
<span data-ttu-id="1c636-144">이 매개 변수를 지정 하지 않으면 현재 비밀의 NotBefore 특성이 변경 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1c636-144">If you do not specify this parameter, there is no change to the current secret's NotBefore attribute.</span></span>

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

### <span data-ttu-id="1c636-145">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1c636-145">-PassThru</span></span>
<span data-ttu-id="1c636-146">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c636-146">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="1c636-147">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1c636-147">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="1c636-148">태그</span><span class="sxs-lookup"><span data-stu-id="1c636-148">-Tag</span></span>
<span data-ttu-id="1c636-149">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="1c636-149">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="1c636-150">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="1c636-150">For example:</span></span>

<span data-ttu-id="1c636-151">@ {key0 = "value0", key1 = $null, key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="1c636-151">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="1c636-152">-VaultName</span><span class="sxs-lookup"><span data-stu-id="1c636-152">-VaultName</span></span>
<span data-ttu-id="1c636-153">수정할 키 보관소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c636-153">Specifies the name of the key vault to modify.</span></span>
<span data-ttu-id="1c636-154">이 cmdlet은이 매개 변수에서 지정 하는 이름 및 현재 선택 된 환경에 따라 키 자격 증명의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c636-154">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies, and your currently selected environment.</span></span>

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

### <span data-ttu-id="1c636-155">-버전</span><span class="sxs-lookup"><span data-stu-id="1c636-155">-Version</span></span>
<span data-ttu-id="1c636-156">비밀의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c636-156">Specifies the version of a secret.</span></span>
<span data-ttu-id="1c636-157">이 cmdlet은 키 보관소 이름, 현재 선택 된 환경, 비밀 이름 및 비밀 버전을 기준으로 비밀의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c636-157">This cmdlet constructs the FQDN of a secret based on the key vault name, your currently selected environment, the secret name, and the secret version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SecretVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c636-158">-확인</span><span class="sxs-lookup"><span data-stu-id="1c636-158">-Confirm</span></span>
<span data-ttu-id="1c636-159">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c636-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c636-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c636-160">-WhatIf</span></span>
<span data-ttu-id="1c636-161">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1c636-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c636-162">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1c636-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c636-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c636-163">CommonParameters</span></span>
<span data-ttu-id="1c636-164">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c636-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c636-165">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c636-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c636-166">입력</span><span class="sxs-lookup"><span data-stu-id="1c636-166">INPUTS</span></span>

### <span data-ttu-id="1c636-167">않아야</span><span class="sxs-lookup"><span data-stu-id="1c636-167">None</span></span>
<span data-ttu-id="1c636-168">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1c636-168">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1c636-169">출력</span><span class="sxs-lookup"><span data-stu-id="1c636-169">OUTPUTS</span></span>

### <span data-ttu-id="1c636-170">Microsoft. KeyVault. PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="1c636-170">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>
<span data-ttu-id="1c636-171">PassThru가 지정 된 경우에는 Microsoft Azure. KeyVault를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c636-171">Returns Microsoft.Azure.Commands.KeyVault.Models.Secret object if PassThru is specified.</span></span> <span data-ttu-id="1c636-172">그렇지 않으면 nothing을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c636-172">Otherwise, returns nothing.</span></span>

## <span data-ttu-id="1c636-173">상속자</span><span class="sxs-lookup"><span data-stu-id="1c636-173">NOTES</span></span>

## <span data-ttu-id="1c636-174">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1c636-174">RELATED LINKS</span></span>

[<span data-ttu-id="1c636-175">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="1c636-175">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

[<span data-ttu-id="1c636-176">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="1c636-176">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)

[<span data-ttu-id="1c636-177">제거-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="1c636-177">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)
