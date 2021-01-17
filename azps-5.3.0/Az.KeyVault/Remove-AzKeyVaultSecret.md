---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultSecret.md
ms.openlocfilehash: 71a0dcebdc889eb8116089eb3c5a5b8379c72b20
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98386310"
---
# <span data-ttu-id="7fb15-101">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="7fb15-101">Remove-AzKeyVaultSecret</span></span>

## <span data-ttu-id="7fb15-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7fb15-102">SYNOPSIS</span></span>
<span data-ttu-id="7fb15-103">키 자격 증명 모음에서 비밀을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="7fb15-103">Deletes a secret in a key vault.</span></span>

## <span data-ttu-id="7fb15-104">구문</span><span class="sxs-lookup"><span data-stu-id="7fb15-104">SYNTAX</span></span>

### <span data-ttu-id="7fb15-105">ByVaultName(기본값)</span><span class="sxs-lookup"><span data-stu-id="7fb15-105">ByVaultName (Default)</span></span>
```
Remove-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7fb15-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="7fb15-106">ByInputObject</span></span>
```
Remove-AzKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7fb15-107">설명</span><span class="sxs-lookup"><span data-stu-id="7fb15-107">DESCRIPTION</span></span>
<span data-ttu-id="7fb15-108">이 Remove-AzKeyVaultSecret cmdlet은 키 자격 증명 모음에서 비밀을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="7fb15-108">The Remove-AzKeyVaultSecret cmdlet deletes a secret in a key vault.</span></span>
<span data-ttu-id="7fb15-109">비밀이 실수로 삭제된 경우 특별한 '복구' 권한이 있는 Undo-AzKeyVaultSecretRemoval 사용하여 비밀을 복구할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7fb15-109">If the secret was accidentally deleted the secret can be recovered using Undo-AzKeyVaultSecretRemoval by a user with special 'recover' permissions.</span></span>
<span data-ttu-id="7fb15-110">이 cmdlet은 **ConfirmImpact** 속성의 값이 높습니다.</span><span class="sxs-lookup"><span data-stu-id="7fb15-110">This cmdlet has a value of high for the **ConfirmImpact** property.</span></span>

## <span data-ttu-id="7fb15-111">예제</span><span class="sxs-lookup"><span data-stu-id="7fb15-111">EXAMPLES</span></span>

### <span data-ttu-id="7fb15-112">예제 1: 키 자격 증명 모음에서 비밀 제거</span><span class="sxs-lookup"><span data-stu-id="7fb15-112">Example 1: Remove a secret from a key vault</span></span>
```powershell
PS C:\> Remove-AzKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -PassThru

Vault Name           : Contoso
Name                 : FinanceSecret
Version              : f622abc7b1394092812f1eb0f85dc91c
Id                   : https://contoso.vault.azure.net:443/secrets/financesecret/f622abc7b1394092812f1eb0f85dc91c
Deleted Date         : 5/25/2018 4:45:34 PM
Scheduled Purge Date : 8/23/2018 4:45:34 PM
Enabled              : True
Expires              :
Not Before           :
Created              : 4/19/2018 5:56:02 PM
Updated              : 4/26/2018 7:48:40 PM
Content Type         :
Tags                 :
```

<span data-ttu-id="7fb15-113">이 명령은 Contoso라는 키 자격 증명 모음에서 FinanceSecret이라는 비밀을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7fb15-113">This command removes the secret named FinanceSecret from the key vault named Contoso.'</span></span>

### <span data-ttu-id="7fb15-114">예제 2: 사용자 확인 없이 키 자격 증명 모음에서 비밀 제거</span><span class="sxs-lookup"><span data-stu-id="7fb15-114">Example 2: Remove a secret from a key vault without user confirmation</span></span>
```powershell
PS C:\> Remove-AzKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -PassThru -Force

Vault Name           : Contoso
Name                 : FinanceSecret
Version              : f622abc7b1394092812f1eb0f85dc91c
Id                   : https://contoso.vault.azure.net:443/secrets/financesecret/f622abc7b1394092812f1eb0f85dc91c
Deleted Date         : 5/25/2018 4:45:34 PM
Scheduled Purge Date : 8/23/2018 4:45:34 PM
Enabled              : True
Expires              :
Not Before           :
Created              : 4/19/2018 5:56:02 PM
Updated              : 4/26/2018 7:48:40 PM
Content Type         :
Tags                 :
```

<span data-ttu-id="7fb15-115">이 명령은 Contoso라는 키 자격 증명 모음에서 FinanceSecret이라는 비밀을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7fb15-115">This command removes the secret named FinanceSecret from the key vault named Contoso.</span></span>
<span data-ttu-id="7fb15-116">이 명령은 *Force* 및 *Confirm* 매개 변수를 지정하므로 cmdlet에서 확인 메시지를 표시하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7fb15-116">The command specifies the *Force* and *Confirm* parameters, and, therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="7fb15-117">예제 3: 키 자격 증명 모음에서 삭제된 비밀을 영구적으로 제거</span><span class="sxs-lookup"><span data-stu-id="7fb15-117">Example 3: Purge deleted secret from the key vault permanently</span></span>
```powershell
PS C:\> Remove-AzKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -InRemovedState
```

<span data-ttu-id="7fb15-118">이 명령은 Contoso라는 키 자격 증명 모음에서 FinanceSecret이라는 비밀을 영구적으로 유지합니다.</span><span class="sxs-lookup"><span data-stu-id="7fb15-118">This command premoves the secret named FinanceSecret from the key vault named Contoso permanently.</span></span>
<span data-ttu-id="7fb15-119">이 cmdlet을 실행하려면 이전에 이 키 자격 증명 모음에 대해 사용자에게 명시적으로 부여된 '제거' 권한이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="7fb15-119">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user for this key vault.</span></span>

## <span data-ttu-id="7fb15-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7fb15-120">PARAMETERS</span></span>

### <span data-ttu-id="7fb15-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fb15-121">-DefaultProfile</span></span>
<span data-ttu-id="7fb15-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="7fb15-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7fb15-123">-Force</span><span class="sxs-lookup"><span data-stu-id="7fb15-123">-Force</span></span>
<span data-ttu-id="7fb15-124">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="7fb15-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7fb15-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7fb15-125">-InputObject</span></span>
<span data-ttu-id="7fb15-126">Key Vault 비밀 개체</span><span class="sxs-lookup"><span data-stu-id="7fb15-126">Key Vault Secret Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7fb15-127">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="7fb15-127">-InRemovedState</span></span>
<span data-ttu-id="7fb15-128">있는 경우 이전에 삭제한 비밀을 영구적으로 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7fb15-128">If present, removes the previously deleted secret permanently.</span></span>

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

### <span data-ttu-id="7fb15-129">-Name</span><span class="sxs-lookup"><span data-stu-id="7fb15-129">-Name</span></span>
<span data-ttu-id="7fb15-130">비밀의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7fb15-130">Specifies the name of a secret.</span></span>
<span data-ttu-id="7fb15-131">이 cmdlet은 이 매개 변수가 지정하는 이름, 키 자격 증명 모음의 이름 및 현재 환경에 따라 비밀의 FQDN(정식 도메인 이름)을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="7fb15-131">This cmdlet constructs the fully qualified domain name (FQDN) of a secret based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fb15-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7fb15-132">-PassThru</span></span>
<span data-ttu-id="7fb15-133">이 cmdlet이 **Microsoft.Azure.Commands.KeyVault.Models.Secret 개체를 반환하는지 나타냅니다.**</span><span class="sxs-lookup"><span data-stu-id="7fb15-133">Indicates that this cmdlet returns a **Microsoft.Azure.Commands.KeyVault.Models.Secret** object.</span></span>
<span data-ttu-id="7fb15-134">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7fb15-134">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7fb15-135">-VaultName</span><span class="sxs-lookup"><span data-stu-id="7fb15-135">-VaultName</span></span>
<span data-ttu-id="7fb15-136">비밀이 속한 키 자격 증명 모음의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7fb15-136">Specifies the name of the key vault to which the secret belongs.</span></span>
<span data-ttu-id="7fb15-137">이 cmdlet은 이 매개 변수가 지정하는 이름 및 현재 환경에 따라 키 자격 증명 모음의 FQDN을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="7fb15-137">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fb15-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7fb15-138">-Confirm</span></span>
<span data-ttu-id="7fb15-139">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7fb15-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fb15-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7fb15-140">-WhatIf</span></span>
<span data-ttu-id="7fb15-141">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="7fb15-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7fb15-142">cmdlet이 실행되지 않습니다. cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="7fb15-142">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7fb15-143">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7fb15-143">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fb15-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fb15-144">CommonParameters</span></span>
<span data-ttu-id="7fb15-145">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7fb15-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fb15-146">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7fb15-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fb15-147">입력</span><span class="sxs-lookup"><span data-stu-id="7fb15-147">INPUTS</span></span>

### <span data-ttu-id="7fb15-148">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="7fb15-148">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span></span>

## <span data-ttu-id="7fb15-149">출력</span><span class="sxs-lookup"><span data-stu-id="7fb15-149">OUTPUTS</span></span>

### <span data-ttu-id="7fb15-150">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="7fb15-150">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecret</span></span>

## <span data-ttu-id="7fb15-151">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7fb15-151">NOTES</span></span>

## <span data-ttu-id="7fb15-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7fb15-152">RELATED LINKS</span></span>

[<span data-ttu-id="7fb15-153">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="7fb15-153">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)

[<span data-ttu-id="7fb15-154">Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="7fb15-154">Set-AzKeyVaultSecret</span></span>](./Set-AzKeyVaultSecret.md)

[<span data-ttu-id="7fb15-155">Undo-AzKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="7fb15-155">Undo-AzKeyVaultSecretRemoval</span></span>](./Undo-AzKeyVaultSecretRemoval.md)

