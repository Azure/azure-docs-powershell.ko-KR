---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/undo-azkeyvaultsecretremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultSecretRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultSecretRemoval.md
ms.openlocfilehash: 9513cba1532ec70acb77cdf97d19de25db36434f
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100416144"
---
# <span data-ttu-id="467ba-101">Undo-AzKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="467ba-101">Undo-AzKeyVaultSecretRemoval</span></span>

## <span data-ttu-id="467ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="467ba-102">SYNOPSIS</span></span>
<span data-ttu-id="467ba-103">키 자격 증명 모음에서 삭제된 비밀을 활성 상태로 복구합니다.</span><span class="sxs-lookup"><span data-stu-id="467ba-103">Recovers a deleted secret in a key vault into an active state.</span></span>

## <span data-ttu-id="467ba-104">구문</span><span class="sxs-lookup"><span data-stu-id="467ba-104">SYNTAX</span></span>

### <span data-ttu-id="467ba-105">기본값(기본값)</span><span class="sxs-lookup"><span data-stu-id="467ba-105">Default (Default)</span></span>
```
Undo-AzKeyVaultSecretRemoval [-VaultName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="467ba-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="467ba-106">InputObject</span></span>
```
Undo-AzKeyVaultSecretRemoval [-InputObject] <PSDeletedKeyVaultSecretIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="467ba-107">설명</span><span class="sxs-lookup"><span data-stu-id="467ba-107">DESCRIPTION</span></span>
<span data-ttu-id="467ba-108">**Undo-AzKeyVaultSecretRemoval** cmdlet은 이전에 삭제된 비밀을 복구합니다.</span><span class="sxs-lookup"><span data-stu-id="467ba-108">The **Undo-AzKeyVaultSecretRemoval** cmdlet will recover a previously deleted secret.</span></span>
<span data-ttu-id="467ba-109">복구된 비밀은 활성화됩니다. 모든 일반 비밀 작업에 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="467ba-109">The recovered secret will be active and can be used for all normal secret operations.</span></span>
<span data-ttu-id="467ba-110">이 작업을 수행하려면 호출자에 '복구' 권한이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="467ba-110">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="467ba-111">예제</span><span class="sxs-lookup"><span data-stu-id="467ba-111">EXAMPLES</span></span>

### <span data-ttu-id="467ba-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="467ba-112">Example 1</span></span>
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

<span data-ttu-id="467ba-113">이 명령은 이전에 삭제된 'MySecret' 비밀을 활성 및 사용 가능한 상태로 복구합니다.</span><span class="sxs-lookup"><span data-stu-id="467ba-113">This command will recover the secret 'MySecret' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="467ba-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="467ba-114">PARAMETERS</span></span>

### <span data-ttu-id="467ba-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="467ba-115">-DefaultProfile</span></span>
<span data-ttu-id="467ba-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="467ba-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="467ba-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="467ba-117">-InputObject</span></span>
<span data-ttu-id="467ba-118">비밀 개체 삭제</span><span class="sxs-lookup"><span data-stu-id="467ba-118">Deleted secret object</span></span>

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

### <span data-ttu-id="467ba-119">-Name</span><span class="sxs-lookup"><span data-stu-id="467ba-119">-Name</span></span>
<span data-ttu-id="467ba-120">비밀 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="467ba-120">Secret name.</span></span>
<span data-ttu-id="467ba-121">Cmdlet은 자격 증명 모음 이름, 현재 선택한 환경 및 비밀 이름에서 비밀의 FQDN을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="467ba-121">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

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

### <span data-ttu-id="467ba-122">-VaultName</span><span class="sxs-lookup"><span data-stu-id="467ba-122">-VaultName</span></span>
<span data-ttu-id="467ba-123">자격 증명 모음 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="467ba-123">Vault name.</span></span>
<span data-ttu-id="467ba-124">Cmdlet은 이름 및 현재 선택한 환경을 기반으로 자격 증명 모음의 FQDN을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="467ba-124">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="467ba-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="467ba-125">-Confirm</span></span>
<span data-ttu-id="467ba-126">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="467ba-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="467ba-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="467ba-127">-WhatIf</span></span>
<span data-ttu-id="467ba-128">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="467ba-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="467ba-129">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="467ba-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="467ba-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="467ba-130">CommonParameters</span></span>
<span data-ttu-id="467ba-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="467ba-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="467ba-132">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="467ba-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="467ba-133">입력</span><span class="sxs-lookup"><span data-stu-id="467ba-133">INPUTS</span></span>

### <span data-ttu-id="467ba-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="467ba-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem</span></span>

## <span data-ttu-id="467ba-135">출력</span><span class="sxs-lookup"><span data-stu-id="467ba-135">OUTPUTS</span></span>

### <span data-ttu-id="467ba-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="467ba-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="467ba-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="467ba-137">NOTES</span></span>

## <span data-ttu-id="467ba-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="467ba-138">RELATED LINKS</span></span>

[<span data-ttu-id="467ba-139">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="467ba-139">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)


[<span data-ttu-id="467ba-140">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="467ba-140">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)
