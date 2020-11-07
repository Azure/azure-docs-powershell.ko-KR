---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: E2A45461-6B41-42FF-A874-A4CEFC867A33
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultsecretattribute
schema: 2.0.0
ms.openlocfilehash: f8463533f8a153b74df1863ba251950f16f9e19a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93880410"
---
# <span data-ttu-id="cd986-101">Set-AzureKeyVaultSecretAttribute</span><span class="sxs-lookup"><span data-stu-id="cd986-101">Set-AzureKeyVaultSecretAttribute</span></span>

## <span data-ttu-id="cd986-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd986-102">SYNOPSIS</span></span>
<span data-ttu-id="cd986-103">키 보관소에서 비밀의 특성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd986-103">Updates attributes of a secret in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cd986-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cd986-104">SYNTAX</span></span>

```
Set-AzureKeyVaultSecretAttribute [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-Enable <Boolean>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd986-105">설명은</span><span class="sxs-lookup"><span data-stu-id="cd986-105">DESCRIPTION</span></span>
<span data-ttu-id="cd986-106">**AzureKeyVaultSecretAttribute** cmdlet은 키 보관소에서 비밀의 편집 가능한 특성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd986-106">The **Set-AzureKeyVaultSecretAttribute** cmdlet updates editable attributes of a secret in a key vault.</span></span>

## <span data-ttu-id="cd986-107">예제의</span><span class="sxs-lookup"><span data-stu-id="cd986-107">EXAMPLES</span></span>

### <span data-ttu-id="cd986-108">예제 1: 비밀의 특성 수정</span><span class="sxs-lookup"><span data-stu-id="cd986-108">Example 1: Modify the attributes of a secret</span></span>
```
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Nbf = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'medium'; 'HR' = null}
PS C:\> $ContentType= 'xml'
PS C:\> Set-AzureKeyVaultSecretAttribute -VaultName 'ContosoVault' -Name 'HR' -Expires $Expires -NotBefore $Nbf -ContentType $ContentType -Enable $True -Tag $Tags -PassThru
```

<span data-ttu-id="cd986-109">처음 네 개의 명령은 만료 날짜, NotBefore 날짜, 태그, 컨텍스트 형식에 대 한 특성을 정의 하 고 변수에 특성을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd986-109">The first four commands define attributes for the expiry date, the NotBefore date, tags, and context type, and store the attributes in variables.</span></span>

<span data-ttu-id="cd986-110">마지막 명령은 저장 된 변수를 사용 하 여 ContosoVault 이라는 키 보관소에서 HR 이라는 비밀에 대 한 특성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd986-110">The final command modifies the attributes for the secret named HR in the key vault named ContosoVault, using the stored variables.</span></span>

### <span data-ttu-id="cd986-111">예제 2: 비밀 태그 및 콘텐츠 형식 삭제</span><span class="sxs-lookup"><span data-stu-id="cd986-111">Example 2: Delete the tags and content type for a secret</span></span>
```
PS C:\>Set-AzureKeyVaultSecretAttribute -VaultName 'ContosoVault' -Name 'HR' -Version '9EEA45C6EE50490B9C3176A80AC1A0DF' -ContentType '' -Tag -@{}
```

<span data-ttu-id="cd986-112">이 명령은 Contoso 라는 키 보관소에 있는 지정 된 버전의 비밀에 대 한 태그와 콘텐츠 유형을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd986-112">This command deletes the tags and the content type for the specified version of the secret named HR in the key vault named Contoso.</span></span>

### <span data-ttu-id="cd986-113">예제 3: 이름이 해당 이름으로 시작 하는 현재 버전의 비밀을 사용 하지 않도록 설정</span><span class="sxs-lookup"><span data-stu-id="cd986-113">Example 3: Disable the current version of secrets whose name begins with IT</span></span>
```
PS C:\> $Vault = 'ContosoVault'
PS C:\> $Prefix = 'IT'
PS C:\> Get-AzureKeyVaultSecret $Vault | Where-Object {$_.Name -like $Prefix + '*'} | Set-AzureKeyVaultSecretAttribute -Enable $False
```

<span data-ttu-id="cd986-114">첫 번째 명령은 Contoso $Vault 변수에 문자열 값을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd986-114">The first command stores the string value Contoso in the $Vault variable.</span></span>

<span data-ttu-id="cd986-115">두 번째 명령은 $Prefix 변수에 문자열 값을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd986-115">The second command stores the string value IT in the $Prefix variable.</span></span>

<span data-ttu-id="cd986-116">세 번째 명령은 Get-AzureKeyVaultSecret cmdlet을 사용 하 여 지정 된 키 보관소의 비밀을 얻은 다음 해당 비밀을 **Where-개체** cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd986-116">The third command uses the Get-AzureKeyVaultSecret cmdlet to get the secrets in the specified key vault, and then passes those secrets to the **Where-Object** cmdlet.</span></span> <span data-ttu-id="cd986-117">**Where 개체** cmdlet은 해당 문자로 시작 하는 이름에 대 한 비밀 정보를 필터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd986-117">The **Where-Object** cmdlet filters the secrets for names that begin with the characters IT.</span></span> <span data-ttu-id="cd986-118">이 명령은 필터와 일치 하는 비밀을 Set-AzureKeyVaultSecretAttribute cmdlet에 연결 하 여 파이프를 비활성화 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd986-118">The command pipes the secrets that match the filter to the Set-AzureKeyVaultSecretAttribute cmdlet, which disables them.</span></span>

### <span data-ttu-id="cd986-119">예제 4: 모든 버전의 비밀에 대 한 ContentType 설정</span><span class="sxs-lookup"><span data-stu-id="cd986-119">Example 4: Set the ContentType for all versions of a secret</span></span>
```
PS C:\>$VaultName = 'ContosoVault'
PS C:\> $Name = 'HR'
PS C:\> $ContentType = 'xml'
PS C:\> Get-AzureKeyVaultKey -VaultName $VaultName -Name $Name -IncludeVersions | Set-AzureKeyVaultSecretAttribute -ContentType $ContentType
```

<span data-ttu-id="cd986-120">처음 세 명령은 *VaultName* , *Name* , *ContentType* 매개 변수에 사용할 문자열 변수를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd986-120">The first three commands define string variables to use for the *VaultName* , *Name* , and *ContentType* parameters.</span></span> <span data-ttu-id="cd986-121">네 번째 명령은 Get-AzureKeyVaultKey cmdlet을 사용 하 여 지정 된 키를 가져오고 Set-AzureKeyVaultSecretAttribute cmdlet에 키를 파이프 하 여 콘텐츠 형식을 XML로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd986-121">The fourth command uses the Get-AzureKeyVaultKey cmdlet to get the specified keys, and pipes the keys to the Set-AzureKeyVaultSecretAttribute cmdlet to set their content type to XML.</span></span>

## <span data-ttu-id="cd986-122">변수</span><span class="sxs-lookup"><span data-stu-id="cd986-122">PARAMETERS</span></span>

### <span data-ttu-id="cd986-123">-ContentType</span><span class="sxs-lookup"><span data-stu-id="cd986-123">-ContentType</span></span>
<span data-ttu-id="cd986-124">비밀의 콘텐츠 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd986-124">Specifies the content type of a secret.</span></span> <span data-ttu-id="cd986-125">이 매개 변수를 지정 하지 않으면 현재 비밀의 콘텐츠 형식이 변경 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cd986-125">If you do not specify this parameter, there is no change to the current secret's content type.</span></span> <span data-ttu-id="cd986-126">기존 콘텐츠 형식을 제거 하려면 빈 문자열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd986-126">To remove the existing content type, specify an empty string.</span></span>

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

### <span data-ttu-id="cd986-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd986-127">-DefaultProfile</span></span>
<span data-ttu-id="cd986-128">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="cd986-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cd986-129">-사용</span><span class="sxs-lookup"><span data-stu-id="cd986-129">-Enable</span></span>
<span data-ttu-id="cd986-130">비밀을 사용할지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="cd986-130">Indicates whether to enable a secret.</span></span> <span data-ttu-id="cd986-131">비밀을 사용 하지 않도록 $False 지정 하거나 비밀을 사용 하도록 $True 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd986-131">Specify $False to disable a secret, or $True to enable a secret.</span></span> <span data-ttu-id="cd986-132">이 매개 변수를 지정 하지 않으면 현재 비밀의 사용 또는 사용 안 함 상태가 변경 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cd986-132">If you do not specify this parameter, there is no change to the current secret's enabled or disabled state.</span></span>

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

### <span data-ttu-id="cd986-133">-만료</span><span class="sxs-lookup"><span data-stu-id="cd986-133">-Expires</span></span>
<span data-ttu-id="cd986-134">비밀을 만료 하는 날짜와 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd986-134">Specifies the date and time that a secret expires.</span></span>

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

### <span data-ttu-id="cd986-135">-이름</span><span class="sxs-lookup"><span data-stu-id="cd986-135">-Name</span></span>
<span data-ttu-id="cd986-136">비밀의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd986-136">Specifies the name of a secret.</span></span> <span data-ttu-id="cd986-137">이 cmdlet은이 매개 변수에서 지정 하는 이름, 키 보관소의 이름 및 현재 환경에 따라 비밀의 FQDN (정규화 된 도메인 이름)을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd986-137">This cmdlet constructs the fully qualified domain name (FQDN) of a secret based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

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

### <span data-ttu-id="cd986-138">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="cd986-138">-NotBefore</span></span>
<span data-ttu-id="cd986-139">비밀을 사용할 수 없는 UTC (협정 세계시)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd986-139">Specifies the Coordinated Universal Time (UTC) before which the secret can't be used.</span></span>
<span data-ttu-id="cd986-140">이 매개 변수를 지정 하지 않으면 현재 비밀의 NotBefore 특성이 변경 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cd986-140">If you do not specify this parameter, there is no change to the current secret's NotBefore attribute.</span></span>

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

### <span data-ttu-id="cd986-141">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cd986-141">-PassThru</span></span>
<span data-ttu-id="cd986-142">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd986-142">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="cd986-143">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cd986-143">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="cd986-144">태그</span><span class="sxs-lookup"><span data-stu-id="cd986-144">-Tag</span></span>
<span data-ttu-id="cd986-145">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="cd986-145">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="cd986-146">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="cd986-146">For example:</span></span>

<span data-ttu-id="cd986-147">@ {key0 = "value0", key1 = $null, key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="cd986-147">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="cd986-148">-VaultName</span><span class="sxs-lookup"><span data-stu-id="cd986-148">-VaultName</span></span>
<span data-ttu-id="cd986-149">수정할 키 보관소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd986-149">Specifies the name of the key vault to modify.</span></span>
<span data-ttu-id="cd986-150">이 cmdlet은이 매개 변수에서 지정 하는 이름 및 현재 선택 된 환경에 따라 키 자격 증명의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd986-150">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies, and your currently selected environment.</span></span>

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

### <span data-ttu-id="cd986-151">-버전</span><span class="sxs-lookup"><span data-stu-id="cd986-151">-Version</span></span>
<span data-ttu-id="cd986-152">비밀의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd986-152">Specifies the version of a secret.</span></span>
<span data-ttu-id="cd986-153">이 cmdlet은 키 보관소 이름, 현재 선택 된 환경, 비밀 이름 및 비밀 버전을 기준으로 비밀의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd986-153">This cmdlet constructs the FQDN of a secret based on the key vault name, your currently selected environment, the secret name, and the secret version.</span></span>

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

### <span data-ttu-id="cd986-154">-확인</span><span class="sxs-lookup"><span data-stu-id="cd986-154">-Confirm</span></span>
<span data-ttu-id="cd986-155">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd986-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd986-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd986-156">-WhatIf</span></span>
<span data-ttu-id="cd986-157">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="cd986-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd986-158">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cd986-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd986-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd986-159">CommonParameters</span></span>
<span data-ttu-id="cd986-160">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd986-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd986-161">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd986-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd986-162">입력</span><span class="sxs-lookup"><span data-stu-id="cd986-162">INPUTS</span></span>

## <span data-ttu-id="cd986-163">출력</span><span class="sxs-lookup"><span data-stu-id="cd986-163">OUTPUTS</span></span>

### <span data-ttu-id="cd986-164">Microsoft. KeyVault. 모델 암호</span><span class="sxs-lookup"><span data-stu-id="cd986-164">Microsoft.Azure.Commands.KeyVault.Models.Secret</span></span>
<span data-ttu-id="cd986-165">PassThru가 지정 된 경우에는 Microsoft Azure. KeyVault를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd986-165">Returns Microsoft.Azure.Commands.KeyVault.Models.Secret object if PassThru is specified.</span></span> <span data-ttu-id="cd986-166">그렇지 않으면 nothing을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd986-166">Otherwise, returns nothing.</span></span>

## <span data-ttu-id="cd986-167">상속자</span><span class="sxs-lookup"><span data-stu-id="cd986-167">NOTES</span></span>

## <span data-ttu-id="cd986-168">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cd986-168">RELATED LINKS</span></span>

[<span data-ttu-id="cd986-169">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="cd986-169">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

[<span data-ttu-id="cd986-170">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="cd986-170">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)

[<span data-ttu-id="cd986-171">제거-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="cd986-171">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)
