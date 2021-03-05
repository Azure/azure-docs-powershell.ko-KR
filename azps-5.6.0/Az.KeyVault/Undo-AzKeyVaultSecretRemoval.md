---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/undo-azkeyvaultsecretremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultSecretRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultSecretRemoval.md
ms.openlocfilehash: dc4c8925d4ddf00cc2e2739d3aa06285f628e423
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976992"
---
# <span data-ttu-id="81b34-101">Undo-AzKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="81b34-101">Undo-AzKeyVaultSecretRemoval</span></span>

## <span data-ttu-id="81b34-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="81b34-102">SYNOPSIS</span></span>
<span data-ttu-id="81b34-103">키 자격 증명 모음에서 삭제된 비밀을 활성 상태로 복구합니다.</span><span class="sxs-lookup"><span data-stu-id="81b34-103">Recovers a deleted secret in a key vault into an active state.</span></span>

## <span data-ttu-id="81b34-104">구문</span><span class="sxs-lookup"><span data-stu-id="81b34-104">SYNTAX</span></span>

### <span data-ttu-id="81b34-105">기본값(기본값)</span><span class="sxs-lookup"><span data-stu-id="81b34-105">Default (Default)</span></span>
```
Undo-AzKeyVaultSecretRemoval [-VaultName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81b34-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="81b34-106">InputObject</span></span>
```
Undo-AzKeyVaultSecretRemoval [-InputObject] <PSDeletedKeyVaultSecretIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81b34-107">설명</span><span class="sxs-lookup"><span data-stu-id="81b34-107">DESCRIPTION</span></span>
<span data-ttu-id="81b34-108">**Undo-AzKeyVaultSecretRemoval** cmdlet은 이전에 삭제된 비밀을 복구합니다.</span><span class="sxs-lookup"><span data-stu-id="81b34-108">The **Undo-AzKeyVaultSecretRemoval** cmdlet will recover a previously deleted secret.</span></span>
<span data-ttu-id="81b34-109">복구된 비밀은 활성 상태며 모든 일반 비밀 작업에 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="81b34-109">The recovered secret will be active and can be used for all normal secret operations.</span></span>
<span data-ttu-id="81b34-110">호출자에 이 작업을 수행하려면 '복구' 권한이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="81b34-110">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="81b34-111">예제</span><span class="sxs-lookup"><span data-stu-id="81b34-111">EXAMPLES</span></span>

### <span data-ttu-id="81b34-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="81b34-112">Example 1</span></span>
```powershell
PS C:\> Undo-AzKeyVaultSecretRemoval -VaultName 'MyKeyVault' -Name 'MySecret'

Vault Name   : MyKeyVault
Name         : MySecret
Version      : f622abc7b1394092812f1eb0f85dc91c
Id           : https://mykeyvault.vault.azure.net:443/secrets/mysecret/f622abc7b1394092812f1eb0f85dc91c
Enabled      : True
Expires      :
Not Before   :
Created      : 4/19/2018 5:56:02 PM
Updated      : 4/26/2018 7:48:40 PM
Content Type :
Tags         :
```

<span data-ttu-id="81b34-113">이 명령은 이전에 삭제된 비밀 'MySecret'을 활성 상태 및 사용 가능한 상태로 복구합니다.</span><span class="sxs-lookup"><span data-stu-id="81b34-113">This command will recover the secret 'MySecret' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="81b34-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="81b34-114">PARAMETERS</span></span>

### <span data-ttu-id="81b34-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81b34-115">-DefaultProfile</span></span>
<span data-ttu-id="81b34-116">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="81b34-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="81b34-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="81b34-117">-InputObject</span></span>
<span data-ttu-id="81b34-118">삭제된 비밀 개체</span><span class="sxs-lookup"><span data-stu-id="81b34-118">Deleted secret object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="81b34-119">-Name</span><span class="sxs-lookup"><span data-stu-id="81b34-119">-Name</span></span>
<span data-ttu-id="81b34-120">비밀 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="81b34-120">Secret name.</span></span>
<span data-ttu-id="81b34-121">Cmdlet은 자격 증명 모음 이름, 현재 선택한 환경 및 비밀 이름의 비밀의 FQDN을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="81b34-121">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81b34-122">-VaultName</span><span class="sxs-lookup"><span data-stu-id="81b34-122">-VaultName</span></span>
<span data-ttu-id="81b34-123">자격 증명 모음 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="81b34-123">Vault name.</span></span>
<span data-ttu-id="81b34-124">Cmdlet은 이름 및 현재 선택한 환경을 기반으로 자격 증명 모음의 FQDN을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="81b34-124">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="81b34-125">-확인</span><span class="sxs-lookup"><span data-stu-id="81b34-125">-Confirm</span></span>
<span data-ttu-id="81b34-126">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="81b34-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81b34-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81b34-127">-WhatIf</span></span>
<span data-ttu-id="81b34-128">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="81b34-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81b34-129">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="81b34-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81b34-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81b34-130">CommonParameters</span></span>
<span data-ttu-id="81b34-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="81b34-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81b34-132">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="81b34-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81b34-133">입력</span><span class="sxs-lookup"><span data-stu-id="81b34-133">INPUTS</span></span>

### <span data-ttu-id="81b34-134">Microsoft.Azure.Commands.KeyVault.Models.PSDKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="81b34-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem</span></span>

## <span data-ttu-id="81b34-135">출력</span><span class="sxs-lookup"><span data-stu-id="81b34-135">OUTPUTS</span></span>

### <span data-ttu-id="81b34-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="81b34-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="81b34-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="81b34-137">NOTES</span></span>

## <span data-ttu-id="81b34-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="81b34-138">RELATED LINKS</span></span>

[<span data-ttu-id="81b34-139">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="81b34-139">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)

[<span data-ttu-id="81b34-140">Add-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="81b34-140">Add-AzKeyVaultSecret</span></span>](./Add-AzKeyVaultSecret.md)

[<span data-ttu-id="81b34-141">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="81b34-141">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)
