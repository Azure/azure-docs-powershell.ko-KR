---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azstorageencryptionscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageEncryptionScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageEncryptionScope.md
ms.openlocfilehash: 6c8f07cbdb70b84d235afa7ce953da0bac477f55
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98375950"
---
# <span data-ttu-id="01e7f-101">Update-AzStorageEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="01e7f-101">Update-AzStorageEncryptionScope</span></span>

## <span data-ttu-id="01e7f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01e7f-102">SYNOPSIS</span></span>
<span data-ttu-id="01e7f-103">Storage 계정에 대한 암호화 범위를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="01e7f-103">Modify an encryption scope for a Storage account.</span></span>

## <span data-ttu-id="01e7f-104">구문</span><span class="sxs-lookup"><span data-stu-id="01e7f-104">SYNTAX</span></span>

### <span data-ttu-id="01e7f-105">AccountName(기본값)</span><span class="sxs-lookup"><span data-stu-id="01e7f-105">AccountName (Default)</span></span>
```
Update-AzStorageEncryptionScope [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -EncryptionScopeName <String> [-StorageEncryption] [-State <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01e7f-106">AccountNameKeyVault</span><span class="sxs-lookup"><span data-stu-id="01e7f-106">AccountNameKeyVault</span></span>
```
Update-AzStorageEncryptionScope [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -EncryptionScopeName <String> [-KeyvaultEncryption] -KeyUri <String> [-State <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01e7f-107">AccountObject</span><span class="sxs-lookup"><span data-stu-id="01e7f-107">AccountObject</span></span>
```
Update-AzStorageEncryptionScope -StorageAccount <PSStorageAccount> -EncryptionScopeName <String>
 [-StorageEncryption] [-State <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="01e7f-108">AccountObjectKeyVault</span><span class="sxs-lookup"><span data-stu-id="01e7f-108">AccountObjectKeyVault</span></span>
```
Update-AzStorageEncryptionScope -StorageAccount <PSStorageAccount> -EncryptionScopeName <String>
 [-KeyvaultEncryption] -KeyUri <String> [-State <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01e7f-109">EncryptionScopeObject</span><span class="sxs-lookup"><span data-stu-id="01e7f-109">EncryptionScopeObject</span></span>
```
Update-AzStorageEncryptionScope -InputObject <PSEncryptionScope> [-StorageEncryption] [-State <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01e7f-110">EncryptionScopeObjectKeyVault</span><span class="sxs-lookup"><span data-stu-id="01e7f-110">EncryptionScopeObjectKeyVault</span></span>
```
Update-AzStorageEncryptionScope -InputObject <PSEncryptionScope> [-KeyvaultEncryption] -KeyUri <String>
 [-State <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01e7f-111">설명</span><span class="sxs-lookup"><span data-stu-id="01e7f-111">DESCRIPTION</span></span>
<span data-ttu-id="01e7f-112">**Update-AzStorageEncryptionScope** cmdlet은 Storage 계정에 대한 암호화 범위를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="01e7f-112">The **Update-AzStorageEncryptionScope** cmdlet modifies an encryption scope for a Storage account.</span></span>

## <span data-ttu-id="01e7f-113">예제</span><span class="sxs-lookup"><span data-stu-id="01e7f-113">EXAMPLES</span></span>

### <span data-ttu-id="01e7f-114">예제 1: 암호화 범위 사용 안</span><span class="sxs-lookup"><span data-stu-id="01e7f-114">Example 1: Disable an encryption scope</span></span>
```
PS C:\> Update-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"  -EncryptionScopeName testscope -State Disabled 

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name      State    Source            KeyVaultKeyUri                                                                          
----      -----    ------            --------------                                                                          
testscope Disabled Microsoft.Storage
```

<span data-ttu-id="01e7f-115">이 명령은 암호화 범위를 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="01e7f-115">This command disables an encryption scope.</span></span>

### <span data-ttu-id="01e7f-116">예제 2: 암호화 범위 사용</span><span class="sxs-lookup"><span data-stu-id="01e7f-116">Example 2: Enable an encryption scope</span></span>
```
PS C:\> Update-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"  -EncryptionScopeName testscope -State Enabled 

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name      State    Source            KeyVaultKeyUri                                                                          
----      -----    ------            --------------                                                                          
testscope Enabled  Microsoft.Storage
```

<span data-ttu-id="01e7f-117">이 명령은 암호화 범위를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="01e7f-117">This command enables an encryption scope.</span></span>

### <span data-ttu-id="01e7f-118">예제 3: Storage 암호화를 사용하여 암호화 범위 업데이트</span><span class="sxs-lookup"><span data-stu-id="01e7f-118">Example 3: Update an encryption scope to use Storage Encryption</span></span>
```
PS C:\> Update-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"  -EncryptionScopeName testscope -StorageEncryption

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name      State    Source            KeyVaultKeyUri                                         
----      -----    ------            --------------                                         
testscope Enabled  Microsoft.Storage
```

<span data-ttu-id="01e7f-119">이 명령은 Storage 암호화를 사용하기 위해 암호화 범위를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="01e7f-119">This command updates an encryption scope to use Storage Encryption.</span></span>

### <span data-ttu-id="01e7f-120">예제 4: Keyvault Encryption을 사용하여 암호화 범위 업데이트</span><span class="sxs-lookup"><span data-stu-id="01e7f-120">Example 4: Update an encryption scope to use Keyvault Encryption</span></span>
```
PS C:\> Update-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -EncryptionScopeName testscope -KeyvaultEncryption -KeyUri "https://keyvalutname.vault.azure.net:443/keys/keyname/34a0ba563b4243d9a0ef2b1d3c0c7d57"

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name      State    Source             KeyVaultKeyUri                                         
----      -----    ------             --------------                                         
testscope Enabled  Microsoft.Keyvault https://keyvalutname.vault.azure.net:443/keys/keyname/34a0ba563b4243d9a0ef2b1d3c0c7d57
```

<span data-ttu-id="01e7f-121">이 명령은 Keyvault Encryption을 사용하기 위해 암호화 범위를 updtas합니다.</span><span class="sxs-lookup"><span data-stu-id="01e7f-121">This command updtaes an encryption scope to use Keyvault Encryption.</span></span>
<span data-ttu-id="01e7f-122">Storage 계정 ID에는 keyvault 키에 대한 get,wrapkey, unwrapkey 권한이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="01e7f-122">The Storage account Identity need have get,wrapkey,unwrapkey permissions to the keyvault key.</span></span>

## <span data-ttu-id="01e7f-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="01e7f-123">PARAMETERS</span></span>

### <span data-ttu-id="01e7f-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01e7f-124">-DefaultProfile</span></span>
<span data-ttu-id="01e7f-125">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="01e7f-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01e7f-126">-EncryptionScopeName</span><span class="sxs-lookup"><span data-stu-id="01e7f-126">-EncryptionScopeName</span></span>
<span data-ttu-id="01e7f-127">Azure Storage EncryptionScope 이름</span><span class="sxs-lookup"><span data-stu-id="01e7f-127">Azure Storage EncryptionScope name</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountNameKeyVault, AccountObject, AccountObjectKeyVault
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01e7f-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="01e7f-128">-InputObject</span></span>
<span data-ttu-id="01e7f-129">EncryptionScope 개체</span><span class="sxs-lookup"><span data-stu-id="01e7f-129">EncryptionScope object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSEncryptionScope
Parameter Sets: EncryptionScopeObject, EncryptionScopeObjectKeyVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="01e7f-130">-KeyUri</span><span class="sxs-lookup"><span data-stu-id="01e7f-130">-KeyUri</span></span>
<span data-ttu-id="01e7f-131">키 Uri</span><span class="sxs-lookup"><span data-stu-id="01e7f-131">The key Uri</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameKeyVault, AccountObjectKeyVault, EncryptionScopeObjectKeyVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01e7f-132">-KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="01e7f-132">-KeyvaultEncryption</span></span>
<span data-ttu-id="01e7f-133">keySource를 Microsoft.Keyvault로 사용하여 암호화 범위 만들기</span><span class="sxs-lookup"><span data-stu-id="01e7f-133">Create encryption scope with keySource as Microsoft.Keyvault</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AccountNameKeyVault, AccountObjectKeyVault, EncryptionScopeObjectKeyVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01e7f-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01e7f-134">-ResourceGroupName</span></span>
<span data-ttu-id="01e7f-135">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="01e7f-135">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountNameKeyVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01e7f-136">-State</span><span class="sxs-lookup"><span data-stu-id="01e7f-136">-State</span></span>
<span data-ttu-id="01e7f-137">암호화 범위 상태 업데이트, 가능한 값은 'Enabled', 'Disabled'입니다.</span><span class="sxs-lookup"><span data-stu-id="01e7f-137">Update encryption scope State, Possible values include: 'Enabled', 'Disabled'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01e7f-138">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="01e7f-138">-StorageAccount</span></span>
<span data-ttu-id="01e7f-139">Storage 계정 개체</span><span class="sxs-lookup"><span data-stu-id="01e7f-139">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject, AccountObjectKeyVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="01e7f-140">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="01e7f-140">-StorageAccountName</span></span>
<span data-ttu-id="01e7f-141">저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="01e7f-141">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountNameKeyVault
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01e7f-142">-StorageEncryption</span><span class="sxs-lookup"><span data-stu-id="01e7f-142">-StorageEncryption</span></span>
<span data-ttu-id="01e7f-143">keySource를 Microsoft.Storage로 사용하여 암호화 범위를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="01e7f-143">Create encryption scope with keySource as Microsoft.Storage.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AccountName, AccountObject, EncryptionScopeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01e7f-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="01e7f-144">-Confirm</span></span>
<span data-ttu-id="01e7f-145">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="01e7f-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01e7f-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01e7f-146">-WhatIf</span></span>
<span data-ttu-id="01e7f-147">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="01e7f-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01e7f-148">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="01e7f-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01e7f-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01e7f-149">CommonParameters</span></span>
<span data-ttu-id="01e7f-150">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="01e7f-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01e7f-151">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="01e7f-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01e7f-152">입력</span><span class="sxs-lookup"><span data-stu-id="01e7f-152">INPUTS</span></span>

### <span data-ttu-id="01e7f-153">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="01e7f-153">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="01e7f-154">출력</span><span class="sxs-lookup"><span data-stu-id="01e7f-154">OUTPUTS</span></span>

### <span data-ttu-id="01e7f-155">Microsoft.Azure.Commands.Management.Storage.Models.PSEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="01e7f-155">Microsoft.Azure.Commands.Management.Storage.Models.PSEncryptionScope</span></span>

## <span data-ttu-id="01e7f-156">참고 사항</span><span class="sxs-lookup"><span data-stu-id="01e7f-156">NOTES</span></span>

## <span data-ttu-id="01e7f-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="01e7f-157">RELATED LINKS</span></span>
