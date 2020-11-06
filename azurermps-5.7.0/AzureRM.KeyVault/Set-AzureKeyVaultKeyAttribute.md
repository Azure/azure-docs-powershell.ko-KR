---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultkeyattribute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultKeyAttribute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultKeyAttribute.md
ms.openlocfilehash: 4b9799a0d2433b513b801a95ffd5c408bf8bdbf2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530497"
---
# <span data-ttu-id="22754-101">Set-AzureKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="22754-101">Set-AzureKeyVaultKeyAttribute</span></span>

## <span data-ttu-id="22754-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22754-102">SYNOPSIS</span></span>
<span data-ttu-id="22754-103">키 자격 증명 모음에서 키의 특성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="22754-103">Updates the attributes of a key in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="22754-104">구문과</span><span class="sxs-lookup"><span data-stu-id="22754-104">SYNTAX</span></span>

### <span data-ttu-id="22754-105">기본값 (기본값)</span><span class="sxs-lookup"><span data-stu-id="22754-105">Default (Default)</span></span>
```
Set-AzureKeyVaultKeyAttribute [-VaultName] <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22754-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="22754-106">InputObject</span></span>
```
Set-AzureKeyVaultKeyAttribute [-InputObject] <PSKeyVaultKeyIdentityItem> [[-Version] <String>]
 [-Enable <Boolean>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22754-107">설명은</span><span class="sxs-lookup"><span data-stu-id="22754-107">DESCRIPTION</span></span>
<span data-ttu-id="22754-108">**AzureKeyVaultKeyAttribute** cmdlet은 키 자격 증명 모음에서 키의 편집 가능한 특성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="22754-108">The **Set-AzureKeyVaultKeyAttribute** cmdlet updates the editable attributes of a key in a key vault.</span></span>

## <span data-ttu-id="22754-109">예제의</span><span class="sxs-lookup"><span data-stu-id="22754-109">EXAMPLES</span></span>

### <span data-ttu-id="22754-110">예제 1: 키를 수정 하 여 사용 하도록 설정 하 고 만료 날짜와 태그를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="22754-110">Example 1: Modify a key to enable it, and set the expiration date and tags</span></span>
```
PS C:\>$Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = null}
PS C:\> Set-AzureKeyVaultKeyAttribute -VaultName 'Contoso' -Name 'ITSoftware' -Expires $Expires -Enable $True -Tag $Tags -PassThru
```

<span data-ttu-id="22754-111">첫 번째 명령은 **데이터 가져오기** cmdlet을 사용 하 여 **DateTime** 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="22754-111">The first command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="22754-112">이 개체는 앞으로 2 년 동안 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="22754-112">That object specifies a time two years in the future.</span></span> <span data-ttu-id="22754-113">이 명령은 $Expires 변수에 해당 날짜를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="22754-113">The command stores that date in the $Expires variable.</span></span>
<span data-ttu-id="22754-114">자세한 내용은을 입력 `Get-Help Get-Date` 하세요.</span><span class="sxs-lookup"><span data-stu-id="22754-114">For more information, type `Get-Help Get-Date`.</span></span>

<span data-ttu-id="22754-115">두 번째 명령은 높은 심각도와 계정의 태그 값을 저장 하는 변수를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="22754-115">The second command creates a variable to store tag values of high severity and Accounting.</span></span>

<span data-ttu-id="22754-116">마지막 명령은 ITSoftware 라는 키를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="22754-116">The final command modifies a key named ITSoftware.</span></span> <span data-ttu-id="22754-117">이 명령은 키를 설정 하 고 만료 시간을 $Expires에 저장 된 시간으로 설정 하 고 $Tags에 저장 된 태그를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="22754-117">The command enables the key, sets its expiration time to the time stored in $Expires, and sets the tags that are stored in $Tags.</span></span>

### <span data-ttu-id="22754-118">예제 2: 모든 태그를 삭제 하는 키 수정</span><span class="sxs-lookup"><span data-stu-id="22754-118">Example 2: Modify a key to delete all tags</span></span>
```
PS C:\>Set-AzureKeyVaultKeyAttribute -VaultName 'Contoso' -Name 'ITSoftware' -Version '7EEA45C6EE50490B9C3176F80AC1A0DG' -Tag @{}
```

<span data-ttu-id="22754-119">이 명령은 ITSoftware 라는 특정 버전의 키에 대 한 태그를 모두 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="22754-119">This commands deletes all tags for a specific version of a key named ITSoftware.</span></span>

## <span data-ttu-id="22754-120">변수</span><span class="sxs-lookup"><span data-stu-id="22754-120">PARAMETERS</span></span>

### <span data-ttu-id="22754-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22754-121">-DefaultProfile</span></span>
<span data-ttu-id="22754-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="22754-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="22754-123">-사용</span><span class="sxs-lookup"><span data-stu-id="22754-123">-Enable</span></span>
<span data-ttu-id="22754-124">키를 사용 하거나 사용 하지 않도록 설정할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="22754-124">Specifies whether to enable or disable a key.</span></span> <span data-ttu-id="22754-125">값 $True는 키를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="22754-125">A value of $True enables the key.</span></span> <span data-ttu-id="22754-126">값이 $False 키를 사용할 수 없게 합니다.</span><span class="sxs-lookup"><span data-stu-id="22754-126">A value of $False disables the key.</span></span> <span data-ttu-id="22754-127">이 매개 변수를 지정 하지 않으면이 cmdlet이 키의 상태를 수정 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="22754-127">If you do not specify this parameter, this cmdlet does not modify the status of the key.</span></span>

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

### <span data-ttu-id="22754-128">-만료</span><span class="sxs-lookup"><span data-stu-id="22754-128">-Expires</span></span>
<span data-ttu-id="22754-129">이 cmdlet이 업데이트 하는 키에 대 한 만료 시간을 **DateTime** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="22754-129">Specifies the expiration time, as a **DateTime** object, for the key that this cmdlet updates.</span></span> <span data-ttu-id="22754-130">이 매개 변수는 UTC (협정 세계시)를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="22754-130">This parameter uses Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="22754-131">**DateTime** 개체를 가져오려면 **날짜 가져오기** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="22754-131">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="22754-132">자세한 내용은을 입력 `Get-Help Get-Date` 하세요.</span><span class="sxs-lookup"><span data-stu-id="22754-132">For more information, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="22754-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="22754-133">-InputObject</span></span>
<span data-ttu-id="22754-134">Key 개체</span><span class="sxs-lookup"><span data-stu-id="22754-134">Key object</span></span>

```yaml
Type: PSKeyVaultKeyIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="22754-135">-KeyOps</span><span class="sxs-lookup"><span data-stu-id="22754-135">-KeyOps</span></span>
<span data-ttu-id="22754-136">이 cmdlet이 추가 하는 키를 사용 하 여 수행할 수 있는 작업 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="22754-136">Specifies an array of operations that can be performed by using the key that this cmdlet adds.</span></span>
<span data-ttu-id="22754-137">이 매개 변수를 지정 하지 않으면 모든 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="22754-137">If you do not specify this parameter, all operations can be performed.</span></span>

<span data-ttu-id="22754-138">이 매개 변수에 허용 되는 값은 JSON 웹 키 사양에 정의 된 키 작업의 쉼표로 구분 된 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="22754-138">The acceptable values for this parameter are a comma-separated list of key operations as defined by the JSON Web Key specification.</span></span> <span data-ttu-id="22754-139">이러한 값 (대/소문자 구분)은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="22754-139">These values (case-sensitive) are:</span></span>

- <span data-ttu-id="22754-140">해독할</span><span class="sxs-lookup"><span data-stu-id="22754-140">encrypt</span></span>
- <span data-ttu-id="22754-141">해독은</span><span class="sxs-lookup"><span data-stu-id="22754-141">decrypt</span></span>
- <span data-ttu-id="22754-142">줄 바꿈</span><span class="sxs-lookup"><span data-stu-id="22754-142">wrap</span></span>
- <span data-ttu-id="22754-143">래핑을</span><span class="sxs-lookup"><span data-stu-id="22754-143">unwrap</span></span>
- <span data-ttu-id="22754-144">등록할</span><span class="sxs-lookup"><span data-stu-id="22754-144">sign</span></span>
- <span data-ttu-id="22754-145">나타나는지</span><span class="sxs-lookup"><span data-stu-id="22754-145">verify</span></span>
- <span data-ttu-id="22754-146">백업할</span><span class="sxs-lookup"><span data-stu-id="22754-146">backup</span></span>
- <span data-ttu-id="22754-147">복원한</span><span class="sxs-lookup"><span data-stu-id="22754-147">restore</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22754-148">-이름</span><span class="sxs-lookup"><span data-stu-id="22754-148">-Name</span></span>
<span data-ttu-id="22754-149">업데이트할 키의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="22754-149">Specifies the name of the key to update.</span></span> <span data-ttu-id="22754-150">이 cmdlet은이 매개 변수에서 지정 하는 이름, 키 보관소의 이름 및 현재 환경에 따라 키의 FQDN (정규화 된 도메인 이름)을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="22754-150">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22754-151">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="22754-151">-NotBefore</span></span>
<span data-ttu-id="22754-152">시간을 **DateTime** 개체로 지정 하 고 그 뒤에 키를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="22754-152">Specifies the time, as a **DateTime** object, before which the key cannot be used.</span></span>
<span data-ttu-id="22754-153">이 매개 변수는 UTC를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="22754-153">This parameter uses UTC.</span></span>
<span data-ttu-id="22754-154">**DateTime** 개체를 가져오려면 **날짜 가져오기** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="22754-154">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>

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

### <span data-ttu-id="22754-155">-PassThru</span><span class="sxs-lookup"><span data-stu-id="22754-155">-PassThru</span></span>
<span data-ttu-id="22754-156">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="22754-156">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="22754-157">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="22754-157">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="22754-158">태그</span><span class="sxs-lookup"><span data-stu-id="22754-158">-Tag</span></span>
<span data-ttu-id="22754-159">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="22754-159">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="22754-160">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="22754-160">For example:</span></span>

<span data-ttu-id="22754-161">@ {key0 = "value0", key1 = $null, key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="22754-161">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="22754-162">-VaultName</span><span class="sxs-lookup"><span data-stu-id="22754-162">-VaultName</span></span>
<span data-ttu-id="22754-163">이 cmdlet이 키를 수정 하는 키 보관소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="22754-163">Specifies the name of the key vault in which this cmdlet modifies the key.</span></span>
<span data-ttu-id="22754-164">이 cmdlet은이 매개 변수에서 지정 하는 이름 및 현재 환경에 따라 키 자격 증명의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="22754-164">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="22754-165">-버전</span><span class="sxs-lookup"><span data-stu-id="22754-165">-Version</span></span>
<span data-ttu-id="22754-166">키 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="22754-166">Specifies the key version.</span></span>
<span data-ttu-id="22754-167">이 cmdlet은 키 자격 증명 이름, 현재 선택 된 환경, 키 이름 및 키 버전을 기준으로 키의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="22754-167">This cmdlet constructs the FQDN of a key based on the key vault name, your currently selected environment, the key name, and the key version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: KeyVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22754-168">-확인</span><span class="sxs-lookup"><span data-stu-id="22754-168">-Confirm</span></span>
<span data-ttu-id="22754-169">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="22754-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22754-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22754-170">-WhatIf</span></span>
<span data-ttu-id="22754-171">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="22754-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22754-172">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="22754-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22754-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22754-173">CommonParameters</span></span>
<span data-ttu-id="22754-174">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="22754-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22754-175">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22754-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22754-176">입력</span><span class="sxs-lookup"><span data-stu-id="22754-176">INPUTS</span></span>

### <span data-ttu-id="22754-177">않아야</span><span class="sxs-lookup"><span data-stu-id="22754-177">None</span></span>
<span data-ttu-id="22754-178">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="22754-178">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="22754-179">출력</span><span class="sxs-lookup"><span data-stu-id="22754-179">OUTPUTS</span></span>

### <span data-ttu-id="22754-180">Microsoft. KeyVault. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="22754-180">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="22754-181">상속자</span><span class="sxs-lookup"><span data-stu-id="22754-181">NOTES</span></span>

## <span data-ttu-id="22754-182">관련 링크</span><span class="sxs-lookup"><span data-stu-id="22754-182">RELATED LINKS</span></span>

[<span data-ttu-id="22754-183">추가-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="22754-183">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="22754-184">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="22754-184">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

[<span data-ttu-id="22754-185">제거-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="22754-185">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)
