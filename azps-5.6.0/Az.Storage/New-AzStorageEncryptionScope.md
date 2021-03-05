---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstorageencryptionscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageEncryptionScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageEncryptionScope.md
ms.openlocfilehash: ab2750bff8ccc3f53761671455bc50fe3ec154d5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002459"
---
# <span data-ttu-id="1493e-101">New-AzStorageEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="1493e-101">New-AzStorageEncryptionScope</span></span>

## <span data-ttu-id="1493e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1493e-102">SYNOPSIS</span></span>
<span data-ttu-id="1493e-103">Storage 계정에 대한 암호화 범위를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1493e-103">Creates an encryption scope for a Storage account.</span></span>

## <span data-ttu-id="1493e-104">구문</span><span class="sxs-lookup"><span data-stu-id="1493e-104">SYNTAX</span></span>

### <span data-ttu-id="1493e-105">AccountName(기본값)</span><span class="sxs-lookup"><span data-stu-id="1493e-105">AccountName (Default)</span></span>
```
New-AzStorageEncryptionScope [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -EncryptionScopeName <String> [-StorageEncryption] [-RequireInfrastructureEncryption]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1493e-106">AccountNameKeyVault</span><span class="sxs-lookup"><span data-stu-id="1493e-106">AccountNameKeyVault</span></span>
```
New-AzStorageEncryptionScope [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -EncryptionScopeName <String> [-KeyvaultEncryption] -KeyUri <String> [-RequireInfrastructureEncryption]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1493e-107">AccountObject</span><span class="sxs-lookup"><span data-stu-id="1493e-107">AccountObject</span></span>
```
New-AzStorageEncryptionScope -StorageAccount <PSStorageAccount> -EncryptionScopeName <String>
 [-StorageEncryption] [-RequireInfrastructureEncryption] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1493e-108">AccountObjectKeyVault</span><span class="sxs-lookup"><span data-stu-id="1493e-108">AccountObjectKeyVault</span></span>
```
New-AzStorageEncryptionScope -StorageAccount <PSStorageAccount> -EncryptionScopeName <String>
 [-KeyvaultEncryption] -KeyUri <String> [-RequireInfrastructureEncryption]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1493e-109">설명</span><span class="sxs-lookup"><span data-stu-id="1493e-109">DESCRIPTION</span></span>
<span data-ttu-id="1493e-110">**New-AzStorageEncryptionScope** cmdlet은 Storage 계정에 대한 암호화 범위를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1493e-110">The **New-AzStorageEncryptionScope** cmdlet creates an encryption scope for a Storage account.</span></span>

## <span data-ttu-id="1493e-111">예제</span><span class="sxs-lookup"><span data-stu-id="1493e-111">EXAMPLES</span></span>

### <span data-ttu-id="1493e-112">예제 1: Storage 암호화를 사용하여 암호화 범위 만들기</span><span class="sxs-lookup"><span data-stu-id="1493e-112">Example 1: Create an encryption scope with Storage Encryption</span></span>
```
PS C:\> New-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"  -EncryptionScopeName testscope -StorageEncryption

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name      State    Source            KeyVaultKeyUri RequireInfrastructureEncryption                                         
----      -----    ------            -------------- -------------------------------                                         
testscope Enabled  Microsoft.Storage
```

<span data-ttu-id="1493e-113">이 명령은 Storage 암호화를 사용하여 암호화 범위를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1493e-113">This command creates an encryption scope with Storage Encryption.</span></span>

### <span data-ttu-id="1493e-114">예제 2: Keyvault Encryption 및 RequireInfrastructureEncryption을 사용하여 암호화 범위 만들기</span><span class="sxs-lookup"><span data-stu-id="1493e-114">Example 2: Create an encryption scope with Keyvault Encryption, and RequireInfrastructureEncryption</span></span>
```
PS C:\> New-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" `
    -EncryptionScopeName testscope -KeyvaultEncryption -KeyUri "https://keyvalutname.vault.azure.net:443/keys/keyname/34a0ba563b4243d9a0ef2b1d3c0c7d57" `
    -RequireInfrastructureEncryption 

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name         State   Source           KeyVaultKeyUri                                                                          RequireInfrastructureEncryption                                       
----         -----   ------             --------------                                                                        -------------------------------                                     
testscope Enabled  Microsoft.Keyvault https://keyvalutname.vault.azure.net:443/keys/keyname/34a0ba563b4243d9a0ef2b1d3c0c7d57  True 
```

<span data-ttu-id="1493e-115">이 명령은 Keyvault 암호화 및 RequireInfrastructureEncryption을 사용하여 암호화 범위를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1493e-115">This command creates an encryption scope with Keyvault Encryption and RequireInfrastructureEncryption.</span></span>
<span data-ttu-id="1493e-116">Storage 계정 ID에는 keyvault 키에 대한 get,wrapkey, unwrapkey 권한이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="1493e-116">The Storage account Identity need have get,wrapkey,unwrapkey permissions to the keyvault key.</span></span>

## <span data-ttu-id="1493e-117">매개 변수</span><span class="sxs-lookup"><span data-stu-id="1493e-117">PARAMETERS</span></span>

### <span data-ttu-id="1493e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1493e-118">-DefaultProfile</span></span>
<span data-ttu-id="1493e-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1493e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1493e-120">-EncryptionScopeName</span><span class="sxs-lookup"><span data-stu-id="1493e-120">-EncryptionScopeName</span></span>
<span data-ttu-id="1493e-121">Azure Storage EncryptionScope 이름</span><span class="sxs-lookup"><span data-stu-id="1493e-121">Azure Storage EncryptionScope name</span></span>

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

### <span data-ttu-id="1493e-122">-KeyUri</span><span class="sxs-lookup"><span data-stu-id="1493e-122">-KeyUri</span></span>
<span data-ttu-id="1493e-123">키 Uri</span><span class="sxs-lookup"><span data-stu-id="1493e-123">The key Uri</span></span>

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

### <span data-ttu-id="1493e-124">-KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="1493e-124">-KeyvaultEncryption</span></span>
<span data-ttu-id="1493e-125">keySource를 Microsoft.Keyvault로 사용하여 암호화 범위 만들기</span><span class="sxs-lookup"><span data-stu-id="1493e-125">Create encryption scope with keySource as Microsoft.Keyvault</span></span>

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

### <span data-ttu-id="1493e-126">-RequireInfrastructureEncryption</span><span class="sxs-lookup"><span data-stu-id="1493e-126">-RequireInfrastructureEncryption</span></span>
<span data-ttu-id="1493e-127">암호화 범위는 미사용 데이터에 대한 플랫폼 관리 키가 있는 보조 암호화 계층을 적용합니다.</span><span class="sxs-lookup"><span data-stu-id="1493e-127">The encryption scope will apply a secondary layer of encryption with platform managed keys for data at rest.</span></span>

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

### <span data-ttu-id="1493e-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1493e-128">-ResourceGroupName</span></span>
<span data-ttu-id="1493e-129">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1493e-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="1493e-130">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="1493e-130">-StorageAccount</span></span>
<span data-ttu-id="1493e-131">저장소 계정 개체</span><span class="sxs-lookup"><span data-stu-id="1493e-131">Storage account object</span></span>

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

### <span data-ttu-id="1493e-132">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="1493e-132">-StorageAccountName</span></span>
<span data-ttu-id="1493e-133">저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1493e-133">Storage Account Name.</span></span>

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

### <span data-ttu-id="1493e-134">-StorageEncryption</span><span class="sxs-lookup"><span data-stu-id="1493e-134">-StorageEncryption</span></span>
<span data-ttu-id="1493e-135">keySource를 Microsoft.Storage로 사용하여 암호화 범위를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="1493e-135">Create encryption scope with keySource as Microsoft.Storage.</span></span>

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

### <span data-ttu-id="1493e-136">-확인</span><span class="sxs-lookup"><span data-stu-id="1493e-136">-Confirm</span></span>
<span data-ttu-id="1493e-137">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1493e-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1493e-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1493e-138">-WhatIf</span></span>
<span data-ttu-id="1493e-139">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="1493e-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1493e-140">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1493e-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1493e-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1493e-141">CommonParameters</span></span>
<span data-ttu-id="1493e-142">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1493e-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1493e-143">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1493e-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1493e-144">입력</span><span class="sxs-lookup"><span data-stu-id="1493e-144">INPUTS</span></span>

### <span data-ttu-id="1493e-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1493e-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="1493e-146">출력</span><span class="sxs-lookup"><span data-stu-id="1493e-146">OUTPUTS</span></span>

### <span data-ttu-id="1493e-147">Microsoft.Azure.Commands.Management.Storage.Models.PSEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="1493e-147">Microsoft.Azure.Commands.Management.Storage.Models.PSEncryptionScope</span></span>

## <span data-ttu-id="1493e-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1493e-148">NOTES</span></span>

## <span data-ttu-id="1493e-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1493e-149">RELATED LINKS</span></span>
