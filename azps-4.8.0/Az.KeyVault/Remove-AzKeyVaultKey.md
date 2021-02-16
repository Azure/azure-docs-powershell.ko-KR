---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 817BF177-519F-47BA-86CF-4591FB402E2Dl
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultKey.md
ms.openlocfilehash: 75d781527a9783c81eba5bd2aacf07d237ef4f8f
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100398362"
---
# <span data-ttu-id="93fcc-101">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="93fcc-101">Remove-AzKeyVaultKey</span></span>

## <span data-ttu-id="93fcc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93fcc-102">SYNOPSIS</span></span>
<span data-ttu-id="93fcc-103">키 자격 증명 모음에서 키를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="93fcc-103">Deletes a key in a key vault.</span></span>

## <span data-ttu-id="93fcc-104">구문</span><span class="sxs-lookup"><span data-stu-id="93fcc-104">SYNTAX</span></span>

### <span data-ttu-id="93fcc-105">ByVaultName(기본값)</span><span class="sxs-lookup"><span data-stu-id="93fcc-105">ByVaultName (Default)</span></span>
```
Remove-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93fcc-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="93fcc-106">ByInputObject</span></span>
```
Remove-AzKeyVaultKey [-InputObject] <PSKeyVaultKeyIdentityItem> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="93fcc-107">설명</span><span class="sxs-lookup"><span data-stu-id="93fcc-107">DESCRIPTION</span></span>
<span data-ttu-id="93fcc-108">Remove-AzKeyVaultKey cmdlet은 키 자격 증명 모음에서 키를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="93fcc-108">The Remove-AzKeyVaultKey cmdlet deletes a key in a key vault.</span></span>
<span data-ttu-id="93fcc-109">키가 실수로 삭제된 경우 특별한 '복구' 권한이 있는 Undo-AzKeyVaultKeyRemoval 키를 사용하여 키를 복구할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="93fcc-109">If the key was accidentally deleted the key can be recovered using Undo-AzKeyVaultKeyRemoval by a user with special 'recover' permissions.</span></span>
<span data-ttu-id="93fcc-110">이 cmdlet은 **ConfirmImpact** 속성의 값이 높습니다.</span><span class="sxs-lookup"><span data-stu-id="93fcc-110">This cmdlet has a value of high for the **ConfirmImpact** property.</span></span>

## <span data-ttu-id="93fcc-111">예제</span><span class="sxs-lookup"><span data-stu-id="93fcc-111">EXAMPLES</span></span>

### <span data-ttu-id="93fcc-112">예제 1: 키 자격 증명 모음에서 키 제거</span><span class="sxs-lookup"><span data-stu-id="93fcc-112">Example 1: Remove a key from a key vault</span></span>
```powershell
PS C:\> Remove-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -PassThru

Vault Name           : contoso
Name                 : key2
Id                   : https://contoso.vault.azure.net:443/keys/itsoftware/fdad15793ba0437e960497908ef9eb32
Deleted Date         : 5/24/2018 11:28:25 PM
Scheduled Purge Date : 8/22/2018 11:28:25 PM
Enabled              : False
Expires              : 10/11/2018 11:32:49 PM
Not Before           : 4/11/2018 11:22:49 PM
Created              : 4/12/2018 10:16:38 PM
Updated              : 4/12/2018 10:16:38 PM
Purge Disabled       : False
Tags                 :
```

<span data-ttu-id="93fcc-113">이 명령은 Contoso라는 키 자격 증명 모음에서 ITSoftware라는 키를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="93fcc-113">This command removes the key named ITSoftware from the key vault named Contoso.</span></span>

### <span data-ttu-id="93fcc-114">예제 2: 사용자 확인 없이 키 제거</span><span class="sxs-lookup"><span data-stu-id="93fcc-114">Example 2: Remove a key without user confirmation</span></span>
```powershell
PS C:\> Remove-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Force
```

<span data-ttu-id="93fcc-115">이 명령은 Contoso라는 키 자격 증명 모음에서 ITSoftware라는 키를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="93fcc-115">This command removes the key named ITSoftware from the key vault named Contoso.</span></span>
<span data-ttu-id="93fcc-116">이 명령은 *Force* 매개 변수를 지정하므로 cmdlet에서 확인 메시지를 표시하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="93fcc-116">The command specifies the *Force* parameter, and, therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="93fcc-117">예제 3: 영구적으로 키 자격 증명 모음에서 삭제된 키 제거</span><span class="sxs-lookup"><span data-stu-id="93fcc-117">Example 3: Purge a deleted key from the key vault permanently</span></span>
```powershell
PS C:\> Remove-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -InRemovedState
```

<span data-ttu-id="93fcc-118">이 명령은 Contoso라는 키 자격 증명 모음에서 ITSoftware라는 키를 영구적으로 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="93fcc-118">This command removes the key named ITSoftware from the key vault named Contoso permanently.</span></span>
<span data-ttu-id="93fcc-119">이 cmdlet을 실행하려면 이전에 이 키 자격 증명 모음에 대해 사용자에게 명시적으로 부여된 '제거' 권한이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="93fcc-119">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user for this key vault.</span></span>

### <span data-ttu-id="93fcc-120">예제 4: 파이프라인 연산자를 사용하여 키 제거</span><span class="sxs-lookup"><span data-stu-id="93fcc-120">Example 4: Remove keys by using the pipeline operator</span></span>
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'Contoso' | Where-Object {$_.Attributes.Enabled -eq $False} | Remove-AzKeyVaultKey
```

<span data-ttu-id="93fcc-121">이 명령은 Contoso라는 키 자격 증명 모음에 있는 모든 키를 사용하고 파이프라인 연산자를 사용하여 **Where-Object** cmdlet에 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="93fcc-121">This command gets all the keys in the key vault named Contoso, and passes them to the **Where-Object** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="93fcc-122">해당 cmdlet은 **Enabled** 특성에 대한 $False 값이 있는 키를 현재 cmdlet에 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="93fcc-122">That cmdlet passes the keys that have a value of $False for the **Enabled** attribute to the current cmdlet.</span></span>
<span data-ttu-id="93fcc-123">해당 cmdlet은 해당 키를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="93fcc-123">That cmdlet removes those keys.</span></span>

## <span data-ttu-id="93fcc-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="93fcc-124">PARAMETERS</span></span>

### <span data-ttu-id="93fcc-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93fcc-125">-DefaultProfile</span></span>
<span data-ttu-id="93fcc-126">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="93fcc-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="93fcc-127">-Force</span><span class="sxs-lookup"><span data-stu-id="93fcc-127">-Force</span></span>
<span data-ttu-id="93fcc-128">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="93fcc-128">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="93fcc-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="93fcc-129">-InputObject</span></span>
<span data-ttu-id="93fcc-130">KeyBundle 개체</span><span class="sxs-lookup"><span data-stu-id="93fcc-130">KeyBundle Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="93fcc-131">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="93fcc-131">-InRemovedState</span></span>
<span data-ttu-id="93fcc-132">이전에 삭제된 키를 영구적으로 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="93fcc-132">Remove the previously deleted key permanently.</span></span>

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

### <span data-ttu-id="93fcc-133">-Name</span><span class="sxs-lookup"><span data-stu-id="93fcc-133">-Name</span></span>
<span data-ttu-id="93fcc-134">제거할 키의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="93fcc-134">Specifies the name of the key to remove.</span></span>
<span data-ttu-id="93fcc-135">이 cmdlet은 이 매개 변수가 지정하는 이름, 키 자격 증명 모음의 이름 및 현재 환경에 따라 키의 FQDN(정식 도메인 이름)을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="93fcc-135">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93fcc-136">-PassThru</span><span class="sxs-lookup"><span data-stu-id="93fcc-136">-PassThru</span></span>
<span data-ttu-id="93fcc-137">이 cmdlet이 **Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey 개체를 반환합니다.**</span><span class="sxs-lookup"><span data-stu-id="93fcc-137">Indicates that this cmdlet returns a **Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey** object.</span></span>
<span data-ttu-id="93fcc-138">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="93fcc-138">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="93fcc-139">-VaultName</span><span class="sxs-lookup"><span data-stu-id="93fcc-139">-VaultName</span></span>
<span data-ttu-id="93fcc-140">키를 제거할 키 자격 증명 모음의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="93fcc-140">Specifies the name of the key vault from which to remove the key.</span></span>
<span data-ttu-id="93fcc-141">이 cmdlet은 이 매개 변수가 지정하는 이름 및 현재 환경에 따라 키 자격 증명 모음의 FQDN을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="93fcc-141">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="93fcc-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="93fcc-142">-Confirm</span></span>
<span data-ttu-id="93fcc-143">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="93fcc-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93fcc-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93fcc-144">-WhatIf</span></span>
<span data-ttu-id="93fcc-145">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="93fcc-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93fcc-146">cmdlet이 실행되지 않습니다. cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="93fcc-146">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93fcc-147">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="93fcc-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93fcc-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93fcc-148">CommonParameters</span></span>
<span data-ttu-id="93fcc-149">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="93fcc-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93fcc-150">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="93fcc-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93fcc-151">입력</span><span class="sxs-lookup"><span data-stu-id="93fcc-151">INPUTS</span></span>

### <span data-ttu-id="93fcc-152">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="93fcc-152">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="93fcc-153">출력</span><span class="sxs-lookup"><span data-stu-id="93fcc-153">OUTPUTS</span></span>

### <span data-ttu-id="93fcc-154">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="93fcc-154">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span></span>

## <span data-ttu-id="93fcc-155">참고 사항</span><span class="sxs-lookup"><span data-stu-id="93fcc-155">NOTES</span></span>

## <span data-ttu-id="93fcc-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="93fcc-156">RELATED LINKS</span></span>

[<span data-ttu-id="93fcc-157">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="93fcc-157">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="93fcc-158">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="93fcc-158">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)


[<span data-ttu-id="93fcc-159">Undo-AzKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="93fcc-159">Undo-AzKeyVaultKeyRemoval</span></span>](./Undo-AzKeyVaultKeyRemoval.md)

