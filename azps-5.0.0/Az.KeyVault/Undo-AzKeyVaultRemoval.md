---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/undo-azkeyvaultremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultRemoval.md
ms.openlocfilehash: 98a3a023564c2c61f1398856e8a089276aeae7bc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94219040"
---
# <span data-ttu-id="49b86-101">Undo-AzKeyVaultRemoval</span><span class="sxs-lookup"><span data-stu-id="49b86-101">Undo-AzKeyVaultRemoval</span></span>

## <span data-ttu-id="49b86-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49b86-102">SYNOPSIS</span></span>
<span data-ttu-id="49b86-103">삭제 된 키 자격 증명 모음을 활성 상태로 복구 합니다.</span><span class="sxs-lookup"><span data-stu-id="49b86-103">Recovers a deleted key vault into an active state.</span></span>

## <span data-ttu-id="49b86-104">구문과</span><span class="sxs-lookup"><span data-stu-id="49b86-104">SYNTAX</span></span>

### <span data-ttu-id="49b86-105">기본값 (기본값)</span><span class="sxs-lookup"><span data-stu-id="49b86-105">Default (Default)</span></span>
```
Undo-AzKeyVaultRemoval [-VaultName] <String> [-ResourceGroupName] <String> [-Location] <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49b86-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="49b86-106">InputObject</span></span>
```
Undo-AzKeyVaultRemoval [-InputObject] <PSDeletedKeyVault> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49b86-107">설명은</span><span class="sxs-lookup"><span data-stu-id="49b86-107">DESCRIPTION</span></span>
<span data-ttu-id="49b86-108">**AzKeyVaultRemoval** cmdlet은 이전에 삭제 된 키 자격 증명 모음을 복구 합니다.</span><span class="sxs-lookup"><span data-stu-id="49b86-108">The **Undo-AzKeyVaultRemoval** cmdlet will recover a previously deleted key vault.</span></span> <span data-ttu-id="49b86-109">복구 후 복구 된 자격 증명 모음이 활성 상태가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="49b86-109">The recovered vault will be active after recovery</span></span>

## <span data-ttu-id="49b86-110">예제의</span><span class="sxs-lookup"><span data-stu-id="49b86-110">EXAMPLES</span></span>

### <span data-ttu-id="49b86-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="49b86-111">Example 1</span></span>
```powershell
PS C:\> Undo-AzKeyVaultRemoval -VaultName 'MyKeyVault' -ResourceGroupName 'MyResourceGroup' -Location 'eastus2' -Tag @{"x"= "y"}

Vault Name                       : MyKeyVault
Resource Group Name              : MyResourceGroup
Location                         : eastus2
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers
                                   /Microsoft.KeyVault/vaults/mykeyvault
Vault URI                        : https://mykeyvault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Standard
Enabled For Deployment?          : True
Enabled For Template Deployment? : True
Enabled For Disk Encryption?     : True
Soft Delete Enabled?             : True
Access Policies                  :
                                   Tenant ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Object ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Application ID                             :
                                   Display Name                               : User Name (username@microsoft.com)
                                   Permissions to Keys                        : get, create, delete, list, update,
                                   import, backup, restore, recover
                                   Permissions to Secrets                     : get, list, set, delete, backup,
                                   restore, recover
                                   Permissions to Certificates                : get, delete, list, create, import,
                                   update, deleteissuers, getissuers, listissuers, managecontacts, manageissuers,
                                   setissuers, recover
                                   Permissions to (Key Vault Managed) Storage : delete, deletesas, get, getsas, list,
                                   listsas, regeneratekey, set, setsas, update

Tags                             :
                                   Name  Value
                                   ====  =====
                                   x     y
```

<span data-ttu-id="49b86-112">이 명령은 eastus2 지역 및 ' MyResourceGroup ' 리소스 그룹에서 이전에 삭제 된 키 자격 증명 모음 ' MyKeyVault '을 활성 및 사용 가능한 상태로 복구 합니다.</span><span class="sxs-lookup"><span data-stu-id="49b86-112">This command will recover the key vault 'MyKeyVault' that was previously deleted from eastus2 region and 'MyResourceGroup' resource group, into an active and usable state.</span></span> <span data-ttu-id="49b86-113">또한 태그를 새 태그로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="49b86-113">It also replaces the tags with new tag.</span></span>

## <span data-ttu-id="49b86-114">변수</span><span class="sxs-lookup"><span data-stu-id="49b86-114">PARAMETERS</span></span>

### <span data-ttu-id="49b86-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49b86-115">-DefaultProfile</span></span>
<span data-ttu-id="49b86-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="49b86-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="49b86-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="49b86-117">-InputObject</span></span>
<span data-ttu-id="49b86-118">삭제 된 자격 증명 모음 개체</span><span class="sxs-lookup"><span data-stu-id="49b86-118">Deleted vault object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="49b86-119">-위치</span><span class="sxs-lookup"><span data-stu-id="49b86-119">-Location</span></span>
<span data-ttu-id="49b86-120">삭제 된 자격 증명 모음 원본 Azure 지역을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="49b86-120">Specifies the deleted vault original Azure region.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49b86-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49b86-121">-ResourceGroupName</span></span>
<span data-ttu-id="49b86-122">키 자격 증명 모음을 만들 기존 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="49b86-122">Specifies the name of an existing resource group in which to create the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49b86-123">태그</span><span class="sxs-lookup"><span data-stu-id="49b86-123">-Tag</span></span>
<span data-ttu-id="49b86-124">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="49b86-124">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="49b86-125">예: @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="49b86-125">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49b86-126">-VaultName</span><span class="sxs-lookup"><span data-stu-id="49b86-126">-VaultName</span></span>
<span data-ttu-id="49b86-127">자격 증명 모음 이름</span><span class="sxs-lookup"><span data-stu-id="49b86-127">Vault name.</span></span>
<span data-ttu-id="49b86-128">Cmdlet은 이름 및 현재 선택 된 환경을 기준으로 자격 증명 모음의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="49b86-128">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="49b86-129">-확인</span><span class="sxs-lookup"><span data-stu-id="49b86-129">-Confirm</span></span>
<span data-ttu-id="49b86-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="49b86-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49b86-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49b86-131">-WhatIf</span></span>
<span data-ttu-id="49b86-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="49b86-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="49b86-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="49b86-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49b86-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49b86-134">CommonParameters</span></span>
<span data-ttu-id="49b86-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="49b86-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49b86-136">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="49b86-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49b86-137">입력</span><span class="sxs-lookup"><span data-stu-id="49b86-137">INPUTS</span></span>

### <span data-ttu-id="49b86-138">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault</span><span class="sxs-lookup"><span data-stu-id="49b86-138">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault</span></span>

## <span data-ttu-id="49b86-139">출력</span><span class="sxs-lookup"><span data-stu-id="49b86-139">OUTPUTS</span></span>

### <span data-ttu-id="49b86-140">Microsoft. KeyVault. 모델. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="49b86-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="49b86-141">상속자</span><span class="sxs-lookup"><span data-stu-id="49b86-141">NOTES</span></span>

## <span data-ttu-id="49b86-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="49b86-142">RELATED LINKS</span></span>

[<span data-ttu-id="49b86-143">제거-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="49b86-143">Remove-AzKeyVault</span></span>](./Remove-AzKeyVault.md)

[<span data-ttu-id="49b86-144">새로운 AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="49b86-144">New-AzKeyVault</span></span>](./New-AzKeyVault.md)

[<span data-ttu-id="49b86-145">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="49b86-145">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)
