---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageencryptionscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageEncryptionScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageEncryptionScope.md
ms.openlocfilehash: 011bdd96d69ae73ca62145b85f6e636751f8eb9f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491336"
---
# <span data-ttu-id="3a3a8-101">New-AzStorageEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="3a3a8-101">New-AzStorageEncryptionScope</span></span>

## <span data-ttu-id="3a3a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a3a8-102">SYNOPSIS</span></span>
<span data-ttu-id="3a3a8-103">Storage 계정에 대한 암호화 범위를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3a3a8-103">Creates an encryption scope for a Storage account.</span></span>

## <span data-ttu-id="3a3a8-104">구문</span><span class="sxs-lookup"><span data-stu-id="3a3a8-104">SYNTAX</span></span>

### <span data-ttu-id="3a3a8-105">AccountName(기본값)</span><span class="sxs-lookup"><span data-stu-id="3a3a8-105">AccountName (Default)</span></span>
```
New-AzStorageEncryptionScope [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -EncryptionScopeName <String> [-StorageEncryption] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a3a8-106">AccountNameKeyVault</span><span class="sxs-lookup"><span data-stu-id="3a3a8-106">AccountNameKeyVault</span></span>
```
New-AzStorageEncryptionScope [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -EncryptionScopeName <String> [-KeyvaultEncryption] -KeyUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a3a8-107">AccountObject</span><span class="sxs-lookup"><span data-stu-id="3a3a8-107">AccountObject</span></span>
```
New-AzStorageEncryptionScope -StorageAccount <PSStorageAccount> -EncryptionScopeName <String>
 [-StorageEncryption] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a3a8-108">AccountObjectKeyVault</span><span class="sxs-lookup"><span data-stu-id="3a3a8-108">AccountObjectKeyVault</span></span>
```
New-AzStorageEncryptionScope -StorageAccount <PSStorageAccount> -EncryptionScopeName <String>
 [-KeyvaultEncryption] -KeyUri <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3a3a8-109">설명</span><span class="sxs-lookup"><span data-stu-id="3a3a8-109">DESCRIPTION</span></span>
<span data-ttu-id="3a3a8-110">**New-AzStorageEncryptionScope** cmdlet은 Storage 계정에 대한 암호화 범위를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3a3a8-110">The **New-AzStorageEncryptionScope** cmdlet creates an encryption scope for a Storage account.</span></span>

## <span data-ttu-id="3a3a8-111">예제</span><span class="sxs-lookup"><span data-stu-id="3a3a8-111">EXAMPLES</span></span>

### <span data-ttu-id="3a3a8-112">예제 1: Storage 암호화를 사용하여 암호화 범위 만들기</span><span class="sxs-lookup"><span data-stu-id="3a3a8-112">Example 1: Create an encryption scope with Storage Encryption</span></span>
```
PS C:\> New-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"  -EncryptionScopeName testscope -StorageEncryption

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name      State    Source            KeyVaultKeyUri                                         
----      -----    ------            --------------                                         
testscope Enabled  Microsoft.Storage
```

<span data-ttu-id="3a3a8-113">이 명령은 Storage 암호화를 사용하여 암호화 범위를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3a3a8-113">This command creates an encryption scope with Storage Encryption.</span></span>

### <span data-ttu-id="3a3a8-114">예제 2: Keyvault Encryption을 사용하여 암호화 범위 만들기</span><span class="sxs-lookup"><span data-stu-id="3a3a8-114">Example 2: Create an encryption scope with Keyvault Encryption</span></span>
```
PS C:\> New-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -EncryptionScopeName testscope -KeyvaultEncryption -KeyUri "https://keyvalutname.vault.azure.net:443/keys/keyname/34a0ba563b4243d9a0ef2b1d3c0c7d57"

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name      State    Source             KeyVaultKeyUri                                         
----      -----    ------             --------------                                         
testscope Enabled  Microsoft.Keyvault https://keyvalutname.vault.azure.net:443/keys/keyname/34a0ba563b4243d9a0ef2b1d3c0c7d57
```

<span data-ttu-id="3a3a8-115">이 명령은 Keyvault Encryption을 사용하여 암호화 범위를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3a3a8-115">This command creates an encryption scope with Keyvault Encryption.</span></span>
<span data-ttu-id="3a3a8-116">Storage 계정 ID에는 keyvault 키에 대한 get,wrapkey, unwrapkey 권한이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="3a3a8-116">The Storage account Identity need have get,wrapkey,unwrapkey permissions to the keyvault key.</span></span>

## <span data-ttu-id="3a3a8-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3a3a8-117">PARAMETERS</span></span>

### <span data-ttu-id="3a3a8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a3a8-118">-DefaultProfile</span></span>
<span data-ttu-id="3a3a8-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3a3a8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a3a8-120">-EncryptionScopeName</span><span class="sxs-lookup"><span data-stu-id="3a3a8-120">-EncryptionScopeName</span></span>
<span data-ttu-id="3a3a8-121">Azure Storage EncryptionScope 이름</span><span class="sxs-lookup"><span data-stu-id="3a3a8-121">Azure Storage EncryptionScope name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a3a8-122">-KeyUri</span><span class="sxs-lookup"><span data-stu-id="3a3a8-122">-KeyUri</span></span>
<span data-ttu-id="3a3a8-123">키 Uri</span><span class="sxs-lookup"><span data-stu-id="3a3a8-123">The key Uri</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameKeyVault, AccountObjectKeyVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a3a8-124">-KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="3a3a8-124">-KeyvaultEncryption</span></span>
<span data-ttu-id="3a3a8-125">keySource를 Microsoft.Keyvault로 사용하여 암호화 범위 만들기</span><span class="sxs-lookup"><span data-stu-id="3a3a8-125">Create encryption scope with keySource as Microsoft.Keyvault</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AccountNameKeyVault, AccountObjectKeyVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a3a8-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a3a8-126">-ResourceGroupName</span></span>
<span data-ttu-id="3a3a8-127">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3a3a8-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="3a3a8-128">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="3a3a8-128">-StorageAccount</span></span>
<span data-ttu-id="3a3a8-129">Storage 계정 개체</span><span class="sxs-lookup"><span data-stu-id="3a3a8-129">Storage account object</span></span>

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

### <span data-ttu-id="3a3a8-130">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="3a3a8-130">-StorageAccountName</span></span>
<span data-ttu-id="3a3a8-131">저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3a3a8-131">Storage Account Name.</span></span>

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

### <span data-ttu-id="3a3a8-132">-StorageEncryption</span><span class="sxs-lookup"><span data-stu-id="3a3a8-132">-StorageEncryption</span></span>
<span data-ttu-id="3a3a8-133">keySource를 Microsoft.Storage로 사용하여 암호화 범위를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3a3a8-133">Create encryption scope with keySource as Microsoft.Storage.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AccountName, AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a3a8-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3a3a8-134">-Confirm</span></span>
<span data-ttu-id="3a3a8-135">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="3a3a8-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a3a8-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a3a8-136">-WhatIf</span></span>
<span data-ttu-id="3a3a8-137">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="3a3a8-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a3a8-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3a3a8-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a3a8-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a3a8-139">CommonParameters</span></span>
<span data-ttu-id="3a3a8-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3a3a8-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a3a8-141">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="3a3a8-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a3a8-142">입력</span><span class="sxs-lookup"><span data-stu-id="3a3a8-142">INPUTS</span></span>

### <span data-ttu-id="3a3a8-143">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3a3a8-143">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="3a3a8-144">출력</span><span class="sxs-lookup"><span data-stu-id="3a3a8-144">OUTPUTS</span></span>

### <span data-ttu-id="3a3a8-145">Microsoft.Azure.Commands.Management.Storage.Models.PSEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="3a3a8-145">Microsoft.Azure.Commands.Management.Storage.Models.PSEncryptionScope</span></span>

## <span data-ttu-id="3a3a8-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3a3a8-146">NOTES</span></span>

## <span data-ttu-id="3a3a8-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3a3a8-147">RELATED LINKS</span></span>
