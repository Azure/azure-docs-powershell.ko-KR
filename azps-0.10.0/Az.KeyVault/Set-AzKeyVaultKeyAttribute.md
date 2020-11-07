---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/set-AzKeyvaultkeyattribute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Set-AzKeyVaultKeyAttribute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Set-AzKeyVaultKeyAttribute.md
ms.openlocfilehash: df861a5efa87126b5eac1657a2b33b6fbae2110b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876688"
---
# <span data-ttu-id="20ffb-101">Set-AzKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="20ffb-101">Set-AzKeyVaultKeyAttribute</span></span>

## <span data-ttu-id="20ffb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20ffb-102">SYNOPSIS</span></span>
<span data-ttu-id="20ffb-103">키 자격 증명 모음에서 키의 특성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="20ffb-103">Updates the attributes of a key in a key vault.</span></span>

## <span data-ttu-id="20ffb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="20ffb-104">SYNTAX</span></span>

```
Set-AzKeyVaultKeyAttribute [-VaultName] <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20ffb-105">설명은</span><span class="sxs-lookup"><span data-stu-id="20ffb-105">DESCRIPTION</span></span>
<span data-ttu-id="20ffb-106">**AzKeyVaultKeyAttribute** cmdlet은 키 자격 증명 모음에서 키의 편집 가능한 특성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="20ffb-106">The **Set-AzKeyVaultKeyAttribute** cmdlet updates the editable attributes of a key in a key vault.</span></span>

## <span data-ttu-id="20ffb-107">예제의</span><span class="sxs-lookup"><span data-stu-id="20ffb-107">EXAMPLES</span></span>

### <span data-ttu-id="20ffb-108">예제 1: 키를 수정 하 여 사용 하도록 설정 하 고 만료 날짜와 태그를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="20ffb-108">Example 1: Modify a key to enable it, and set the expiration date and tags</span></span>
```
PS C:\>$Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = null}
PS C:\> Set-AzKeyVaultKeyAttribute -VaultName 'Contoso' -Name 'ITSoftware' -Expires $Expires -Enable $True -Tag $Tags -PassThru
```

<span data-ttu-id="20ffb-109">첫 번째 명령은 **데이터 가져오기** cmdlet을 사용 하 여 **DateTime** 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="20ffb-109">The first command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="20ffb-110">이 개체는 앞으로 2 년 동안 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="20ffb-110">That object specifies a time two years in the future.</span></span> <span data-ttu-id="20ffb-111">이 명령은 $Expires 변수에 해당 날짜를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="20ffb-111">The command stores that date in the $Expires variable.</span></span>
<span data-ttu-id="20ffb-112">자세한 내용은을 입력 `Get-Help Get-Date` 하세요.</span><span class="sxs-lookup"><span data-stu-id="20ffb-112">For more information, type `Get-Help Get-Date`.</span></span>

<span data-ttu-id="20ffb-113">두 번째 명령은 높은 심각도와 계정의 태그 값을 저장 하는 변수를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="20ffb-113">The second command creates a variable to store tag values of high severity and Accounting.</span></span>

<span data-ttu-id="20ffb-114">마지막 명령은 ITSoftware 라는 키를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="20ffb-114">The final command modifies a key named ITSoftware.</span></span> <span data-ttu-id="20ffb-115">이 명령은 키를 설정 하 고 만료 시간을 $Expires에 저장 된 시간으로 설정 하 고 $Tags에 저장 된 태그를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="20ffb-115">The command enables the key, sets its expiration time to the time stored in $Expires, and sets the tags that are stored in $Tags.</span></span>

### <span data-ttu-id="20ffb-116">예제 2: 모든 태그를 삭제 하는 키 수정</span><span class="sxs-lookup"><span data-stu-id="20ffb-116">Example 2: Modify a key to delete all tags</span></span>
```
PS C:\>Set-AzKeyVaultKeyAttribute -VaultName 'Contoso' -Name 'ITSoftware' -Version '7EEA45C6EE50490B9C3176F80AC1A0DG' -Tag @{}
```

<span data-ttu-id="20ffb-117">이 명령은 ITSoftware 라는 특정 버전의 키에 대 한 태그를 모두 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="20ffb-117">This commands deletes all tags for a specific version of a key named ITSoftware.</span></span>

## <span data-ttu-id="20ffb-118">변수</span><span class="sxs-lookup"><span data-stu-id="20ffb-118">PARAMETERS</span></span>

### <span data-ttu-id="20ffb-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20ffb-119">-DefaultProfile</span></span>
<span data-ttu-id="20ffb-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="20ffb-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20ffb-121">-사용</span><span class="sxs-lookup"><span data-stu-id="20ffb-121">-Enable</span></span>
<span data-ttu-id="20ffb-122">키를 사용 하거나 사용 하지 않도록 설정할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="20ffb-122">Specifies whether to enable or disable a key.</span></span> <span data-ttu-id="20ffb-123">값 $True는 키를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="20ffb-123">A value of $True enables the key.</span></span> <span data-ttu-id="20ffb-124">값이 $False 키를 사용할 수 없게 합니다.</span><span class="sxs-lookup"><span data-stu-id="20ffb-124">A value of $False disables the key.</span></span> <span data-ttu-id="20ffb-125">이 매개 변수를 지정 하지 않으면이 cmdlet이 키의 상태를 수정 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="20ffb-125">If you do not specify this parameter, this cmdlet does not modify the status of the key.</span></span>

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

### <span data-ttu-id="20ffb-126">-만료</span><span class="sxs-lookup"><span data-stu-id="20ffb-126">-Expires</span></span>
<span data-ttu-id="20ffb-127">이 cmdlet이 업데이트 하는 키에 대 한 만료 시간을 **DateTime** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="20ffb-127">Specifies the expiration time, as a **DateTime** object, for the key that this cmdlet updates.</span></span> <span data-ttu-id="20ffb-128">이 매개 변수는 UTC (협정 세계시)를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="20ffb-128">This parameter uses Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="20ffb-129">**DateTime** 개체를 가져오려면 **날짜 가져오기** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="20ffb-129">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="20ffb-130">자세한 내용은을 입력 `Get-Help Get-Date` 하세요.</span><span class="sxs-lookup"><span data-stu-id="20ffb-130">For more information, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="20ffb-131">-KeyOps</span><span class="sxs-lookup"><span data-stu-id="20ffb-131">-KeyOps</span></span>
<span data-ttu-id="20ffb-132">이 cmdlet이 추가 하는 키를 사용 하 여 수행할 수 있는 작업 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="20ffb-132">Specifies an array of operations that can be performed by using the key that this cmdlet adds.</span></span>
<span data-ttu-id="20ffb-133">이 매개 변수를 지정 하지 않으면 모든 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="20ffb-133">If you do not specify this parameter, all operations can be performed.</span></span>

<span data-ttu-id="20ffb-134">이 매개 변수에 허용 되는 값은 JSON 웹 키 사양에 정의 된 키 작업의 쉼표로 구분 된 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="20ffb-134">The acceptable values for this parameter are a comma-separated list of key operations as defined by the JSON Web Key specification.</span></span> <span data-ttu-id="20ffb-135">이러한 값 (대/소문자 구분)은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="20ffb-135">These values (case-sensitive) are:</span></span>

- <span data-ttu-id="20ffb-136">해독할</span><span class="sxs-lookup"><span data-stu-id="20ffb-136">encrypt</span></span>
- <span data-ttu-id="20ffb-137">해독은</span><span class="sxs-lookup"><span data-stu-id="20ffb-137">decrypt</span></span>
- <span data-ttu-id="20ffb-138">줄 바꿈</span><span class="sxs-lookup"><span data-stu-id="20ffb-138">wrap</span></span>
- <span data-ttu-id="20ffb-139">래핑을</span><span class="sxs-lookup"><span data-stu-id="20ffb-139">unwrap</span></span>
- <span data-ttu-id="20ffb-140">등록할</span><span class="sxs-lookup"><span data-stu-id="20ffb-140">sign</span></span>
- <span data-ttu-id="20ffb-141">나타나는지</span><span class="sxs-lookup"><span data-stu-id="20ffb-141">verify</span></span>
- <span data-ttu-id="20ffb-142">백업할</span><span class="sxs-lookup"><span data-stu-id="20ffb-142">backup</span></span>
- <span data-ttu-id="20ffb-143">복원한</span><span class="sxs-lookup"><span data-stu-id="20ffb-143">restore</span></span>

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

### <span data-ttu-id="20ffb-144">-이름</span><span class="sxs-lookup"><span data-stu-id="20ffb-144">-Name</span></span>
<span data-ttu-id="20ffb-145">업데이트할 키의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="20ffb-145">Specifies the name of the key to update.</span></span> <span data-ttu-id="20ffb-146">이 cmdlet은이 매개 변수에서 지정 하는 이름, 키 보관소의 이름 및 현재 환경에 따라 키의 FQDN (정규화 된 도메인 이름)을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="20ffb-146">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20ffb-147">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="20ffb-147">-NotBefore</span></span>
<span data-ttu-id="20ffb-148">시간을 **DateTime** 개체로 지정 하 고 그 뒤에 키를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="20ffb-148">Specifies the time, as a **DateTime** object, before which the key cannot be used.</span></span>
<span data-ttu-id="20ffb-149">이 매개 변수는 UTC를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="20ffb-149">This parameter uses UTC.</span></span>
<span data-ttu-id="20ffb-150">**DateTime** 개체를 가져오려면 **날짜 가져오기** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="20ffb-150">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>

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

### <span data-ttu-id="20ffb-151">-PassThru</span><span class="sxs-lookup"><span data-stu-id="20ffb-151">-PassThru</span></span>
<span data-ttu-id="20ffb-152">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="20ffb-152">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="20ffb-153">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="20ffb-153">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="20ffb-154">태그</span><span class="sxs-lookup"><span data-stu-id="20ffb-154">-Tag</span></span>
<span data-ttu-id="20ffb-155">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="20ffb-155">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="20ffb-156">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="20ffb-156">For example:</span></span>

<span data-ttu-id="20ffb-157">@ {key0 = "value0", key1 = $null, key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="20ffb-157">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="20ffb-158">-VaultName</span><span class="sxs-lookup"><span data-stu-id="20ffb-158">-VaultName</span></span>
<span data-ttu-id="20ffb-159">이 cmdlet이 키를 수정 하는 키 보관소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="20ffb-159">Specifies the name of the key vault in which this cmdlet modifies the key.</span></span>
<span data-ttu-id="20ffb-160">이 cmdlet은이 매개 변수에서 지정 하는 이름 및 현재 환경에 따라 키 자격 증명의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="20ffb-160">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="20ffb-161">-버전</span><span class="sxs-lookup"><span data-stu-id="20ffb-161">-Version</span></span>
<span data-ttu-id="20ffb-162">키 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="20ffb-162">Specifies the key version.</span></span>
<span data-ttu-id="20ffb-163">이 cmdlet은 키 자격 증명 이름, 현재 선택 된 환경, 키 이름 및 키 버전을 기준으로 키의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="20ffb-163">This cmdlet constructs the FQDN of a key based on the key vault name, your currently selected environment, the key name, and the key version.</span></span>

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

### <span data-ttu-id="20ffb-164">-확인</span><span class="sxs-lookup"><span data-stu-id="20ffb-164">-Confirm</span></span>
<span data-ttu-id="20ffb-165">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="20ffb-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20ffb-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20ffb-166">-WhatIf</span></span>
<span data-ttu-id="20ffb-167">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="20ffb-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20ffb-168">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="20ffb-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20ffb-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20ffb-169">CommonParameters</span></span>
<span data-ttu-id="20ffb-170">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="20ffb-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20ffb-171">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20ffb-171">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20ffb-172">입력</span><span class="sxs-lookup"><span data-stu-id="20ffb-172">INPUTS</span></span>

### <span data-ttu-id="20ffb-173">않아야</span><span class="sxs-lookup"><span data-stu-id="20ffb-173">None</span></span>
<span data-ttu-id="20ffb-174">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="20ffb-174">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="20ffb-175">출력</span><span class="sxs-lookup"><span data-stu-id="20ffb-175">OUTPUTS</span></span>

### <span data-ttu-id="20ffb-176">Microsoft. KeyVault. Keyvault</span><span class="sxs-lookup"><span data-stu-id="20ffb-176">Microsoft.Azure.Commands.KeyVault.Models.KeyBundle</span></span>

## <span data-ttu-id="20ffb-177">상속자</span><span class="sxs-lookup"><span data-stu-id="20ffb-177">NOTES</span></span>

## <span data-ttu-id="20ffb-178">관련 링크</span><span class="sxs-lookup"><span data-stu-id="20ffb-178">RELATED LINKS</span></span>

[<span data-ttu-id="20ffb-179">추가-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="20ffb-179">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="20ffb-180">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="20ffb-180">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

[<span data-ttu-id="20ffb-181">제거-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="20ffb-181">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)
