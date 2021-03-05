---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/undo-azkeyvaultkeyremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultKeyRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultKeyRemoval.md
ms.openlocfilehash: 9de4cc6572a20dc9ec241c6f93cb035162b914f9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012059"
---
# <span data-ttu-id="27804-101">Undo-AzKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="27804-101">Undo-AzKeyVaultKeyRemoval</span></span>

## <span data-ttu-id="27804-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27804-102">SYNOPSIS</span></span>
<span data-ttu-id="27804-103">키 자격 증명 모음에서 삭제된 키를 활성 상태로 복구합니다.</span><span class="sxs-lookup"><span data-stu-id="27804-103">Recovers a deleted key in a key vault into an active state.</span></span>

## <span data-ttu-id="27804-104">구문</span><span class="sxs-lookup"><span data-stu-id="27804-104">SYNTAX</span></span>

### <span data-ttu-id="27804-105">기본값(기본값)</span><span class="sxs-lookup"><span data-stu-id="27804-105">Default (Default)</span></span>
```
Undo-AzKeyVaultKeyRemoval [-VaultName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27804-106">HsmInteractive</span><span class="sxs-lookup"><span data-stu-id="27804-106">HsmInteractive</span></span>
```
Undo-AzKeyVaultKeyRemoval -HsmName <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27804-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="27804-107">InputObject</span></span>
```
Undo-AzKeyVaultKeyRemoval [-InputObject] <PSDeletedKeyVaultKeyIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27804-108">설명</span><span class="sxs-lookup"><span data-stu-id="27804-108">DESCRIPTION</span></span>
<span data-ttu-id="27804-109">**Undo-AzKeyVaultKeyRemoval** cmdlet은 이전에 삭제된 키를 복구합니다.</span><span class="sxs-lookup"><span data-stu-id="27804-109">The **Undo-AzKeyVaultKeyRemoval** cmdlet will recover a previously deleted key.</span></span>
<span data-ttu-id="27804-110">복구된 키는 활성으로 모든 일반 키 작업에 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="27804-110">The recovered key will be active and can be used for all normal key operations.</span></span>
<span data-ttu-id="27804-111">호출자에 이 작업을 수행하려면 '복구' 권한이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="27804-111">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="27804-112">예제</span><span class="sxs-lookup"><span data-stu-id="27804-112">EXAMPLES</span></span>

### <span data-ttu-id="27804-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="27804-113">Example 1</span></span>
```powershell
PS C:\> Undo-AzKeyVaultKeyRemoval -VaultName 'MyKeyVault' -Name 'MyKey'

Vault Name     : MyKeyVault
Name           : MyKey
Version        : 1af807cc331a49d0b52b7c75e1b2366e
Id             : https://mykeybault.vault.azure.net:443/keys/mykey/1af807cc331a49d0b52b7c75e1b2366e
Enabled        : True
Expires        :
Not Before     :
Created        : 5/24/2018 8:32:27 PM
Updated        : 5/24/2018 8:32:27 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="27804-114">이 명령은 이전에 삭제된 키 'MyKey'를 활성 상태 및 사용 가능한 상태로 복구합니다.</span><span class="sxs-lookup"><span data-stu-id="27804-114">This command will recover the key 'MyKey' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="27804-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="27804-115">PARAMETERS</span></span>

### <span data-ttu-id="27804-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27804-116">-DefaultProfile</span></span>
<span data-ttu-id="27804-117">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="27804-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="27804-118">-HsmName</span><span class="sxs-lookup"><span data-stu-id="27804-118">-HsmName</span></span>
<span data-ttu-id="27804-119">HSM 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="27804-119">HSM name.</span></span> <span data-ttu-id="27804-120">Cmdlet은 이름 및 현재 선택한 환경에 따라 관리되는 HSM의 FQDN을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="27804-120">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: HsmInteractive
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27804-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="27804-121">-InputObject</span></span>
<span data-ttu-id="27804-122">삭제된 키 개체</span><span class="sxs-lookup"><span data-stu-id="27804-122">Deleted key object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="27804-123">-Name</span><span class="sxs-lookup"><span data-stu-id="27804-123">-Name</span></span>
<span data-ttu-id="27804-124">키 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="27804-124">Key name.</span></span>
<span data-ttu-id="27804-125">Cmdlet은 자격 증명 모음 이름, 현재 선택한 환경 및 키 이름의 키의 FQDN을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="27804-125">Cmdlet constructs the FQDN of a key from vault name, currently selected environment and key name.</span></span>

```yaml
Type: System.String
Parameter Sets: Default, HsmInteractive
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27804-126">-VaultName</span><span class="sxs-lookup"><span data-stu-id="27804-126">-VaultName</span></span>
<span data-ttu-id="27804-127">자격 증명 모음 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="27804-127">Vault name.</span></span>
<span data-ttu-id="27804-128">Cmdlet은 이름 및 현재 선택한 환경을 기반으로 자격 증명 모음의 FQDN을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="27804-128">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="27804-129">-확인</span><span class="sxs-lookup"><span data-stu-id="27804-129">-Confirm</span></span>
<span data-ttu-id="27804-130">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="27804-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27804-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27804-131">-WhatIf</span></span>
<span data-ttu-id="27804-132">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="27804-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27804-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="27804-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27804-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27804-134">CommonParameters</span></span>
<span data-ttu-id="27804-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="27804-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27804-136">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="27804-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27804-137">입력</span><span class="sxs-lookup"><span data-stu-id="27804-137">INPUTS</span></span>

### <span data-ttu-id="27804-138">Microsoft.Azure.Commands.KeyVault.Models.PSDKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="27804-138">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="27804-139">출력</span><span class="sxs-lookup"><span data-stu-id="27804-139">OUTPUTS</span></span>

### <span data-ttu-id="27804-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="27804-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="27804-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="27804-141">NOTES</span></span>

## <span data-ttu-id="27804-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="27804-142">RELATED LINKS</span></span>

[<span data-ttu-id="27804-143">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="27804-143">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="27804-144">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="27804-144">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="27804-145">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="27804-145">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

