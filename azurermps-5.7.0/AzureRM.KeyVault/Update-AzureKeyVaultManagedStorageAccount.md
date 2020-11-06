---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/update-azurekeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureKeyVaultManagedStorageAccount.md
ms.openlocfilehash: b16ceeb2409c2709286b970f857fcb9079bf067a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528935"
---
# <span data-ttu-id="3823c-101">Update-AzureKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3823c-101">Update-AzureKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="3823c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3823c-102">SYNOPSIS</span></span>
<span data-ttu-id="3823c-103">키 자격 증명 모음 관리 Azure 저장소 계정의 편집 가능한 특성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="3823c-103">Update editable attributes of a Key Vault managed Azure Storage Account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3823c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3823c-104">SYNTAX</span></span>

```
Update-AzureKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String>
 [-ActiveKeyName <String>] [-AutoRegenerateKey <Boolean>] [-RegenerationPeriod <TimeSpan>] [-Enable <Boolean>]
 [-Tag <Hashtable>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3823c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="3823c-105">DESCRIPTION</span></span>
<span data-ttu-id="3823c-106">키 보관소 관리 Azure Storage 계정의 편집 가능한 특성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="3823c-106">Update the editable attributes of a Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="3823c-107">예제의</span><span class="sxs-lookup"><span data-stu-id="3823c-107">EXAMPLES</span></span>

### <span data-ttu-id="3823c-108">예제 1: 키 보관소 관리 Azure 저장소 계정에서 활성 키를 ' key2 '로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="3823c-108">Example 1:Update the active key to 'key2' on a Key Vault managed Azure Storage Account.</span></span>
```
PS C:\> Update-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -ActiveKeyName 'key2'
```

<span data-ttu-id="3823c-109">키 자격 증명 모음에서 Azure Storage 계정 활성 키를 ' a m m '으로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="3823c-109">Updates the Key Vault managed Azure Storage Account active key to 'key2'.</span></span> <span data-ttu-id="3823c-110">이 업데이트 후에 ' key2 '가 SAS 토큰을 생성 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3823c-110">'key2' will be used to generate SAS tokens after this update.</span></span>

## <span data-ttu-id="3823c-111">변수</span><span class="sxs-lookup"><span data-stu-id="3823c-111">PARAMETERS</span></span>

### <span data-ttu-id="3823c-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="3823c-112">-AccountName</span></span>
<span data-ttu-id="3823c-113">키 자격 증명 모음 관리 저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3823c-113">Key Vault managed storage account name.</span></span> <span data-ttu-id="3823c-114">Cmdlet은 자격 증명 모음 이름, 현재 선택한 환경 및 manged 저장소 계정 이름에서 관리 되는 저장소 계정 이름의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="3823c-114">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3823c-115">-ActiveKeyName</span><span class="sxs-lookup"><span data-stu-id="3823c-115">-ActiveKeyName</span></span>
<span data-ttu-id="3823c-116">활성 키 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3823c-116">Active key name.</span></span>
<span data-ttu-id="3823c-117">지정 하지 않으면 관리 저장소 계정의 활성 키 이름에 대 한 기존 값이 변경 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3823c-117">If not specified, the existing value of managed storage account's active key name remains unchanged</span></span>

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

### <span data-ttu-id="3823c-118">-AutoRegenerateKey</span><span class="sxs-lookup"><span data-stu-id="3823c-118">-AutoRegenerateKey</span></span>
<span data-ttu-id="3823c-119">자동으로 키를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="3823c-119">Auto regenerate key.</span></span>
<span data-ttu-id="3823c-120">지정 하지 않으면 관리 되는 저장소 계정의 기존 자동 재생성 키 값은 변경 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3823c-120">If not specified, the existing value of auto regenerate key of managed storage account remains unchanged</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3823c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3823c-121">-DefaultProfile</span></span>
<span data-ttu-id="3823c-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="3823c-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3823c-123">-사용</span><span class="sxs-lookup"><span data-stu-id="3823c-123">-Enable</span></span>
<span data-ttu-id="3823c-124">있으면 value가 true 인 경우 sas 토큰 생성에 대해 관리 되는 저장소 계정 키를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3823c-124">If present, enables a use of a managed storage account key for sas token generation if value is true.</span></span> <span data-ttu-id="3823c-125">값이 false 인 경우 sas 토큰 생성에 대해 관리 되는 저장소 계정 키를 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3823c-125">Disables use of a managed storage account key for sas token generation if value is false.</span></span> <span data-ttu-id="3823c-126">지정 하지 않으면 저장소 계정의 사용/사용 안 함 상태에 대 한 기존 값이 변경 되지 않고 그대로 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3823c-126">If not specified, the existing value of the storage account's enabled/disabled state remains unchanged.</span></span>

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

### <span data-ttu-id="3823c-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3823c-127">-PassThru</span></span>
<span data-ttu-id="3823c-128">Cmdlet은 기본적으로 개체를 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3823c-128">Cmdlet does not return object by default.</span></span> <span data-ttu-id="3823c-129">이 스위치가 지정 된 경우 관리 되는 저장소 계정 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="3823c-129">If this switch is specified, return managed storage account object.</span></span>

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

### <span data-ttu-id="3823c-130">-RegenerationPeriod</span><span class="sxs-lookup"><span data-stu-id="3823c-130">-RegenerationPeriod</span></span>
<span data-ttu-id="3823c-131">재생성 기간.</span><span class="sxs-lookup"><span data-stu-id="3823c-131">Regeneration period.</span></span> <span data-ttu-id="3823c-132">자동 다시 생성 키를 사용 하는 경우이 값은 관리 저장소 계정의 비활성 keygets 재생성 되 고 활성 키가 되는 timespan을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3823c-132">If auto regenerate key is enabled, this value specifies the timespan after which managed storage account's inactive keygets auto regenerated and becomes the active key.</span></span> <span data-ttu-id="3823c-133">지정 하지 않은 경우 관리 되는 저장소 계정의 기존 다시 생성 기간 값은 변경 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3823c-133">If not specified, the existing value of regeneration period of keys of managed storage account remains unchanged</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3823c-134">태그</span><span class="sxs-lookup"><span data-stu-id="3823c-134">-Tag</span></span>
<span data-ttu-id="3823c-135">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="3823c-135">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="3823c-136">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="3823c-136">For example:</span></span>

<span data-ttu-id="3823c-137">@ {key0 = "value0", key1 = $null, key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="3823c-137">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="3823c-138">-VaultName</span><span class="sxs-lookup"><span data-stu-id="3823c-138">-VaultName</span></span>
<span data-ttu-id="3823c-139">자격 증명 모음 이름</span><span class="sxs-lookup"><span data-stu-id="3823c-139">Vault name.</span></span>
<span data-ttu-id="3823c-140">Cmdlet은 이름 및 현재 선택 된 환경을 기준으로 자격 증명 모음의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="3823c-140">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="3823c-141">-확인</span><span class="sxs-lookup"><span data-stu-id="3823c-141">-Confirm</span></span>
<span data-ttu-id="3823c-142">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3823c-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3823c-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3823c-143">-WhatIf</span></span>
<span data-ttu-id="3823c-144">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="3823c-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3823c-145">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3823c-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3823c-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3823c-146">CommonParameters</span></span>
<span data-ttu-id="3823c-147">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3823c-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3823c-148">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3823c-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3823c-149">입력</span><span class="sxs-lookup"><span data-stu-id="3823c-149">INPUTS</span></span>

### <span data-ttu-id="3823c-150">않아야</span><span class="sxs-lookup"><span data-stu-id="3823c-150">None</span></span>
<span data-ttu-id="3823c-151">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3823c-151">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3823c-152">출력</span><span class="sxs-lookup"><span data-stu-id="3823c-152">OUTPUTS</span></span>

### <span data-ttu-id="3823c-153">Microsoft. KeyVault. \* ManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3823c-153">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageAccount</span></span>

## <span data-ttu-id="3823c-154">상속자</span><span class="sxs-lookup"><span data-stu-id="3823c-154">NOTES</span></span>

## <span data-ttu-id="3823c-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3823c-155">RELATED LINKS</span></span>

[<span data-ttu-id="3823c-156">AzureRM 볼트</span><span class="sxs-lookup"><span data-stu-id="3823c-156">AzureRM.KeyVault</span></span>](/powershell/module/azurerm.keyvault)
