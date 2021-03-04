---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 817BF177-519F-47BA-86CF-4591FB402E2Dl
online version: https://docs.microsoft.com/powershell/module/az.keyvault/remove-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultKey.md
ms.openlocfilehash: 0d458d6063aa530b1f30f6a79244e7d719080bf6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952523"
---
# <span data-ttu-id="633fb-101">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="633fb-101">Remove-AzKeyVaultKey</span></span>

## <span data-ttu-id="633fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="633fb-102">SYNOPSIS</span></span>
<span data-ttu-id="633fb-103">키 자격 증명 모음의 키를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="633fb-103">Deletes a key in a key vault.</span></span>

## <span data-ttu-id="633fb-104">구문</span><span class="sxs-lookup"><span data-stu-id="633fb-104">SYNTAX</span></span>

### <span data-ttu-id="633fb-105">ByVaultName(기본값)</span><span class="sxs-lookup"><span data-stu-id="633fb-105">ByVaultName (Default)</span></span>
```
Remove-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="633fb-106">HsmByVaultName</span><span class="sxs-lookup"><span data-stu-id="633fb-106">HsmByVaultName</span></span>
```
Remove-AzKeyVaultKey -HsmName <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="633fb-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="633fb-107">ByInputObject</span></span>
```
Remove-AzKeyVaultKey [-InputObject] <PSKeyVaultKeyIdentityItem> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="633fb-108">설명</span><span class="sxs-lookup"><span data-stu-id="633fb-108">DESCRIPTION</span></span>
<span data-ttu-id="633fb-109">Remove-AzKeyVaultKey cmdlet은 키 자격 증명 모음의 키를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="633fb-109">The Remove-AzKeyVaultKey cmdlet deletes a key in a key vault.</span></span>
<span data-ttu-id="633fb-110">키가 실수로 삭제된 경우 특별한 '복구' 권한이 Undo-AzKeyVaultKeyRemoval 사용자가 키를 사용하여 복구할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="633fb-110">If the key was accidentally deleted the key can be recovered using Undo-AzKeyVaultKeyRemoval by a user with special 'recover' permissions.</span></span>
<span data-ttu-id="633fb-111">이 cmdlet에는 **ConfirmImpact** 속성에 대한 값이 높습니다.</span><span class="sxs-lookup"><span data-stu-id="633fb-111">This cmdlet has a value of high for the **ConfirmImpact** property.</span></span>

## <span data-ttu-id="633fb-112">예제</span><span class="sxs-lookup"><span data-stu-id="633fb-112">EXAMPLES</span></span>

### <span data-ttu-id="633fb-113">예제 1: 키 자격 증명 모음에서 키 제거</span><span class="sxs-lookup"><span data-stu-id="633fb-113">Example 1: Remove a key from a key vault</span></span>
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

<span data-ttu-id="633fb-114">이 명령은 Contoso라는 키 자격 증명 모음에서 ITSoftware라는 키를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="633fb-114">This command removes the key named ITSoftware from the key vault named Contoso.</span></span>

### <span data-ttu-id="633fb-115">예제 2: 사용자 확인 없이 키 제거</span><span class="sxs-lookup"><span data-stu-id="633fb-115">Example 2: Remove a key without user confirmation</span></span>
```powershell
PS C:\> Remove-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Force
```

<span data-ttu-id="633fb-116">이 명령은 Contoso라는 키 자격 증명 모음에서 ITSoftware라는 키를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="633fb-116">This command removes the key named ITSoftware from the key vault named Contoso.</span></span>
<span data-ttu-id="633fb-117">명령은 *Force* 매개 변수를 지정하므로 cmdlet에서 확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="633fb-117">The command specifies the *Force* parameter, and, therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="633fb-118">예제 3: 키 자격 증명 모음에서 삭제된 키를 영구적으로 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="633fb-118">Example 3: Purge a deleted key from the key vault permanently</span></span>
```powershell
PS C:\> Remove-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -InRemovedState
```

<span data-ttu-id="633fb-119">이 명령은 Contoso라는 키 자격 증명 모음에서 ITSoftware라는 키를 영구적으로 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="633fb-119">This command removes the key named ITSoftware from the key vault named Contoso permanently.</span></span>
<span data-ttu-id="633fb-120">이 cmdlet을 실행하려면 이 키 자격 증명 모음에 대해 사용자에게 이전에 명시적으로 부여된 '제거' 권한이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="633fb-120">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user for this key vault.</span></span>

### <span data-ttu-id="633fb-121">예제 4: 파이프라인 연산자를 사용하여 키 제거</span><span class="sxs-lookup"><span data-stu-id="633fb-121">Example 4: Remove keys by using the pipeline operator</span></span>
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'Contoso' | Where-Object {$_.Attributes.Enabled -eq $False} | Remove-AzKeyVaultKey
```

<span data-ttu-id="633fb-122">이 명령은 Contoso라는 키 자격 증명 모음의 모든 키를 얻게 하여 파이프라인 연산자를 사용하여 **Where-Object** cmdlet에 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="633fb-122">This command gets all the keys in the key vault named Contoso, and passes them to the **Where-Object** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="633fb-123">해당 cmdlet은 현재 cmdlet에 $False 값의  키를 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="633fb-123">That cmdlet passes the keys that have a value of $False for the **Enabled** attribute to the current cmdlet.</span></span>
<span data-ttu-id="633fb-124">해당 cmdlet은 해당 키를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="633fb-124">That cmdlet removes those keys.</span></span>

## <span data-ttu-id="633fb-125">매개 변수</span><span class="sxs-lookup"><span data-stu-id="633fb-125">PARAMETERS</span></span>

### <span data-ttu-id="633fb-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="633fb-126">-DefaultProfile</span></span>
<span data-ttu-id="633fb-127">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="633fb-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="633fb-128">-Force</span><span class="sxs-lookup"><span data-stu-id="633fb-128">-Force</span></span>
<span data-ttu-id="633fb-129">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="633fb-129">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="633fb-130">-HsmName</span><span class="sxs-lookup"><span data-stu-id="633fb-130">-HsmName</span></span>
<span data-ttu-id="633fb-131">HSM 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="633fb-131">HSM name.</span></span> <span data-ttu-id="633fb-132">Cmdlet은 이름 및 현재 선택한 환경에 따라 관리되는 HSM의 FQDN을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="633fb-132">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: HsmByVaultName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="633fb-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="633fb-133">-InputObject</span></span>
<span data-ttu-id="633fb-134">KeyBundle 개체</span><span class="sxs-lookup"><span data-stu-id="633fb-134">KeyBundle Object</span></span>

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

### <span data-ttu-id="633fb-135">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="633fb-135">-InRemovedState</span></span>
<span data-ttu-id="633fb-136">이전에 삭제한 키를 영구적으로 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="633fb-136">Remove the previously deleted key permanently.</span></span>

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

### <span data-ttu-id="633fb-137">-Name</span><span class="sxs-lookup"><span data-stu-id="633fb-137">-Name</span></span>
<span data-ttu-id="633fb-138">제거할 키의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="633fb-138">Specifies the name of the key to remove.</span></span>
<span data-ttu-id="633fb-139">이 cmdlet은 이 매개 변수가 지정하는 이름, 키 자격 증명 모음의 이름 및 현재 환경에 따라 키의 완전히 자격을 갖춘 도메인 이름(FQDN)을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="633fb-139">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName, HsmByVaultName
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="633fb-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="633fb-140">-PassThru</span></span>
<span data-ttu-id="633fb-141">이 cmdlet은 **Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey 개체를 반환합니다.**</span><span class="sxs-lookup"><span data-stu-id="633fb-141">Indicates that this cmdlet returns a **Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey** object.</span></span>
<span data-ttu-id="633fb-142">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="633fb-142">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="633fb-143">-VaultName</span><span class="sxs-lookup"><span data-stu-id="633fb-143">-VaultName</span></span>
<span data-ttu-id="633fb-144">키를 제거할 키 자격 증명 모음의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="633fb-144">Specifies the name of the key vault from which to remove the key.</span></span>
<span data-ttu-id="633fb-145">이 cmdlet은 이 매개 변수가 지정하는 이름과 현재 환경을 기반으로 키 자격 증명 모음의 FQDN을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="633fb-145">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="633fb-146">-확인</span><span class="sxs-lookup"><span data-stu-id="633fb-146">-Confirm</span></span>
<span data-ttu-id="633fb-147">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="633fb-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="633fb-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="633fb-148">-WhatIf</span></span>
<span data-ttu-id="633fb-149">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="633fb-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="633fb-150">cmdlet이 실행되지 않습니다. cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="633fb-150">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="633fb-151">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="633fb-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="633fb-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="633fb-152">CommonParameters</span></span>
<span data-ttu-id="633fb-153">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="633fb-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="633fb-154">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="633fb-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="633fb-155">입력</span><span class="sxs-lookup"><span data-stu-id="633fb-155">INPUTS</span></span>

### <span data-ttu-id="633fb-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="633fb-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="633fb-157">출력</span><span class="sxs-lookup"><span data-stu-id="633fb-157">OUTPUTS</span></span>

### <span data-ttu-id="633fb-158">Microsoft.Azure.Commands.KeyVault.Models.PSDKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="633fb-158">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span></span>

## <span data-ttu-id="633fb-159">참고 사항</span><span class="sxs-lookup"><span data-stu-id="633fb-159">NOTES</span></span>

## <span data-ttu-id="633fb-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="633fb-160">RELATED LINKS</span></span>

[<span data-ttu-id="633fb-161">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="633fb-161">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="633fb-162">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="633fb-162">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

[<span data-ttu-id="633fb-163">Set-AzKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="633fb-163">Set-AzKeyVaultKeyAttribute</span></span>](./Set-AzKeyVaultKeyAttribute.md)

[<span data-ttu-id="633fb-164">Undo-AzKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="633fb-164">Undo-AzKeyVaultKeyRemoval</span></span>](./Undo-AzKeyVaultKeyRemoval.md)

