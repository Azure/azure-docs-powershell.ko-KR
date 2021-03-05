---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/update-azkeyvaultmanagedstorageaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultManagedStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultManagedStorageAccountKey.md
ms.openlocfilehash: 80ff79e71498cc76479592b65207da09fabed6a0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976939"
---
# <span data-ttu-id="78d33-101">Update-AzKeyVaultManagedStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="78d33-101">Update-AzKeyVaultManagedStorageAccountKey</span></span>

## <span data-ttu-id="78d33-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78d33-102">SYNOPSIS</span></span>
<span data-ttu-id="78d33-103">Key Vault 관리 Azure Storage 계정의 지정된 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="78d33-103">Regenerates the specified key of Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="78d33-104">구문</span><span class="sxs-lookup"><span data-stu-id="78d33-104">SYNTAX</span></span>

### <span data-ttu-id="78d33-105">ByDefinitionName(기본값)</span><span class="sxs-lookup"><span data-stu-id="78d33-105">ByDefinitionName (Default)</span></span>
```
Update-AzKeyVaultManagedStorageAccountKey [-VaultName] <String> [-AccountName] <String> [-KeyName] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78d33-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="78d33-106">ByInputObject</span></span>
```
Update-AzKeyVaultManagedStorageAccountKey [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [-KeyName] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="78d33-107">설명</span><span class="sxs-lookup"><span data-stu-id="78d33-107">DESCRIPTION</span></span>
<span data-ttu-id="78d33-108">Key Vault 관리 Azure Storage 계정의 지정된 키를 다시 생성하고 키를 활성 키로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="78d33-108">Regenerates the specified key of Key Vault managed Azure Storage Account and sets the key as the active key.</span></span> <span data-ttu-id="78d33-109">Key Vault는 키를 다시 생성하기 위해 Azure Resource Manager에 대한 호출을 프로시저합니다.</span><span class="sxs-lookup"><span data-stu-id="78d33-109">Key Vault proxies the call to Azure Resource Manager to regenerate the key.</span></span> <span data-ttu-id="78d33-110">호출자는 주어진 Azure Storage 계정에서 키를 다시 생성하는 권한을 포스로 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="78d33-110">The caller must posses permissions to regenerate keys on given Azure Storage Account.</span></span>

## <span data-ttu-id="78d33-111">예제</span><span class="sxs-lookup"><span data-stu-id="78d33-111">EXAMPLES</span></span>

### <span data-ttu-id="78d33-112">예제 1: 키 다시 생성</span><span class="sxs-lookup"><span data-stu-id="78d33-112">Example 1: Regenerate a key</span></span>
```powershell
PS C:\> Update-AzKeyVaultManagedStorageAccountKey -VaultName 'myvault' -AccountName 'mystorageaccount' -KeyName 'key1'

Id                  : https://myvault.vault.azure.net:443/storage/mystorageaccount
Vault Name          : myvault
AccountName         : mystorageaccount
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/mystorageaccount
Active Key Name     : key1
Auto Regenerate Key : True
Regeneration Period : 90.00:00:00
Enabled             : True
Created             : 5/21/2018 11:55:58 PM
Updated             : 5/21/2018 11:55:58 PM
Tags                :
```

<span data-ttu-id="78d33-113">계정 'mystorageaccount'의 'key1'을 다시 생성하고 'key1'을 Key Vault 관리 Azure Storage 계정의 활성으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="78d33-113">Regenerates 'key1' of account 'mystorageaccount' and sets 'key1' as the active of the Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="78d33-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="78d33-114">PARAMETERS</span></span>

### <span data-ttu-id="78d33-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="78d33-115">-AccountName</span></span>
<span data-ttu-id="78d33-116">Key Vault 관리 저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="78d33-116">Key Vault managed storage account name.</span></span> <span data-ttu-id="78d33-117">Cmdlet은 자격 증명 모음 이름, 현재 선택한 환경 및 맹그 저장소 계정 이름에서 관리되는 저장소 계정 이름의 FQDN을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="78d33-117">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefinitionName
Aliases: StorageAccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78d33-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78d33-118">-DefaultProfile</span></span>
<span data-ttu-id="78d33-119">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="78d33-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="78d33-120">-Force</span><span class="sxs-lookup"><span data-stu-id="78d33-120">-Force</span></span>
<span data-ttu-id="78d33-121">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="78d33-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="78d33-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="78d33-122">-InputObject</span></span>
<span data-ttu-id="78d33-123">ManagedStorageAccount 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="78d33-123">ManagedStorageAccount object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="78d33-124">-KeyName</span><span class="sxs-lookup"><span data-stu-id="78d33-124">-KeyName</span></span>
<span data-ttu-id="78d33-125">다시 생성하고 활성화할 저장소 계정 키의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="78d33-125">Name of storage account key to regenerate and make active.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78d33-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="78d33-126">-PassThru</span></span>
<span data-ttu-id="78d33-127">Cmdlet은 기본적으로 개체를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="78d33-127">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="78d33-128">이 스위치가 지정된 경우 cmdlet은 삭제된 관리되는 저장소 계정을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="78d33-128">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

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

### <span data-ttu-id="78d33-129">-VaultName</span><span class="sxs-lookup"><span data-stu-id="78d33-129">-VaultName</span></span>
<span data-ttu-id="78d33-130">자격 증명 모음 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="78d33-130">Vault name.</span></span>
<span data-ttu-id="78d33-131">Cmdlet은 이름 및 현재 선택한 환경을 기반으로 자격 증명 모음의 FQDN을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="78d33-131">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefinitionName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78d33-132">-확인</span><span class="sxs-lookup"><span data-stu-id="78d33-132">-Confirm</span></span>
<span data-ttu-id="78d33-133">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="78d33-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78d33-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78d33-134">-WhatIf</span></span>
<span data-ttu-id="78d33-135">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="78d33-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78d33-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="78d33-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78d33-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78d33-137">CommonParameters</span></span>
<span data-ttu-id="78d33-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="78d33-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78d33-139">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="78d33-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78d33-140">입력</span><span class="sxs-lookup"><span data-stu-id="78d33-140">INPUTS</span></span>

### <span data-ttu-id="78d33-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="78d33-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="78d33-142">출력</span><span class="sxs-lookup"><span data-stu-id="78d33-142">OUTPUTS</span></span>

### <span data-ttu-id="78d33-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="78d33-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="78d33-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="78d33-144">NOTES</span></span>

## <span data-ttu-id="78d33-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="78d33-145">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

