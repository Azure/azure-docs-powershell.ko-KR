---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azmanagedhsmkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzManagedHsmKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzManagedHsmKey.md
ms.openlocfilehash: 15a9466dd0caac6ebe7497942de36e832b89ee55
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215289"
---
# <span data-ttu-id="a0159-101">Remove-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="a0159-101">Remove-AzManagedHsmKey</span></span>

## <span data-ttu-id="a0159-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0159-102">SYNOPSIS</span></span>
<span data-ttu-id="a0159-103">관리 되는 HSM에서 키를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0159-103">Deletes a key in a managed HSM.</span></span>

## <span data-ttu-id="a0159-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a0159-104">SYNTAX</span></span>

### <span data-ttu-id="a0159-105">RemoveByKeyNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="a0159-105">RemoveByKeyNameParameterSet (Default)</span></span>
```
Remove-AzManagedHsmKey [-HsmName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0159-106">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0159-106">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzManagedHsmKey [-InputObject] <PSKeyVaultKeyIdentityItem> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0159-107">설명은</span><span class="sxs-lookup"><span data-stu-id="a0159-107">DESCRIPTION</span></span>
<span data-ttu-id="a0159-108">Remove-AzManagedHsmKey cmdlet은 관리 되는 HSM에서 키를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0159-108">The Remove-AzManagedHsmKey cmdlet deletes a key in a managed HSM.</span></span>
<span data-ttu-id="a0159-109">키를 실수로 삭제 한 경우 특정 ' 복구 ' 권한이 있는 사용자가 Undo-AzManagedHsmKeyRemoval를 사용 하 여 키를 복구할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a0159-109">If the key was accidentally deleted the key can be recovered using Undo-AzManagedHsmKeyRemoval by a user with special 'recover' permissions.</span></span>
<span data-ttu-id="a0159-110">이 cmdlet의 값은 ' a/or **영향** ' 속성에 대해 high입니다.</span><span class="sxs-lookup"><span data-stu-id="a0159-110">This cmdlet has a value of high for the **ConfirmImpact** property.</span></span>

## <span data-ttu-id="a0159-111">예제의</span><span class="sxs-lookup"><span data-stu-id="a0159-111">EXAMPLES</span></span>

### <span data-ttu-id="a0159-112">예제 1: 관리 되는 HSM에서 키 제거</span><span class="sxs-lookup"><span data-stu-id="a0159-112">Example 1: Remove a key from a managed HSM</span></span>
```powershell
PS C:\> Remove-AzManagedHsmKey -HsmName testmhsm -Name testkey -PassThru

Vault/HSM Name       : testmhsm
Name                 : testkey
Id                   : https://testmhsm.managedhsm.azure.net:443/keys/testkey/9a9de2bcec540c3b160cd54cbae71339
Deleted Date         : 10/14/2020 9:35:06 AM
Scheduled Purge Date : 1/12/2021 9:35:06 AM
Enabled              : False
Expires              : 10/14/2022 8:13:29 AM
Not Before           : 10/14/2020 8:13:33 AM
Created              : 10/14/2020 8:14:01 AM
Updated              : 10/14/2020 8:14:01 AM
Recovery Level       : Recoverable+Purgeable
Tags                 :
```

<span data-ttu-id="a0159-113">이 명령은 testmhsm 이라는 관리 되는 HSM에서 testkey 라는 키를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0159-113">This command removes the key named testkey from the managed HSM named testmhsm.</span></span>

### <span data-ttu-id="a0159-114">예제 2: 사용자 확인 없이 키 제거</span><span class="sxs-lookup"><span data-stu-id="a0159-114">Example 2: Remove a key without user confirmation</span></span>
```powershell
PS C:\> Remove-AzManagedHsmKey -HsmName testmhsm -Name testkey -Force
```

<span data-ttu-id="a0159-115">이 명령은 testmhsm 이라는 관리 되는 HSM에서 testkey 라는 키를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0159-115">This command removes the key named testkey from the managed HSM named testmhsm.</span></span>
<span data-ttu-id="a0159-116">명령에서 *Force* 매개 변수를 지정 하므로 cmdlet이 확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a0159-116">The command specifies the *Force* parameter, and, therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="a0159-117">예제 3: 관리 되는 HSM에서 삭제 된 키 지우기 영구 제거</span><span class="sxs-lookup"><span data-stu-id="a0159-117">Example 3: Purge a deleted key from the managed HSM permanently</span></span>
```powershell
PS C:\> Remove-AzManagedHsmKey -HsmName testmhsm -Name testkey -InRemovedState
```

<span data-ttu-id="a0159-118">이 명령은 testmhsm 이라는 관리 되는 HSM에서 testkey 라는 키를 영구적으로 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0159-118">This command removes the key named testkey from the managed HSM named testmhsm permanently.</span></span>
<span data-ttu-id="a0159-119">이 cmdlet을 실행 하려면이 관리 되는 HSM에 대해 사용자에 게 명시적으로 부여 된 ' 제거 ' 권한이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0159-119">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user for this managed HSM.</span></span>

### <span data-ttu-id="a0159-120">예제 4: 파이프라인 연산자를 사용 하 여 키 제거</span><span class="sxs-lookup"><span data-stu-id="a0159-120">Example 4: Remove keys by using the pipeline operator</span></span>
```powershell
PS C:\> Get-AzManagedHsmKey -HsmName testmhsm | Where-Object {$_.Attributes.Enabled -eq $False} | Remove-AzManagedHsmKey
```

<span data-ttu-id="a0159-121">이 명령은 관리 되는 HSM의 모든 키를 testmhsm 이라고 하 고 파이프라인 연산자를 사용 하 여 **Where-개체** cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0159-121">This command gets all the keys in the managed HSM named testmhsm and passes them to the **Where-Object** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="a0159-122">해당 cmdlet은 **Enabled** 특성에 대 한 $False 값을 갖는 키를 현재 cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0159-122">That cmdlet passes the keys that have a value of $False for the **Enabled** attribute to the current cmdlet.</span></span>
<span data-ttu-id="a0159-123">해당 cmdlet은 해당 키를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0159-123">That cmdlet removes those keys.</span></span>

## <span data-ttu-id="a0159-124">변수</span><span class="sxs-lookup"><span data-stu-id="a0159-124">PARAMETERS</span></span>

### <span data-ttu-id="a0159-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0159-125">-DefaultProfile</span></span>
<span data-ttu-id="a0159-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a0159-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0159-127">-Force</span><span class="sxs-lookup"><span data-stu-id="a0159-127">-Force</span></span>
<span data-ttu-id="a0159-128">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a0159-128">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="a0159-129">-HsmName</span><span class="sxs-lookup"><span data-stu-id="a0159-129">-HsmName</span></span>
<span data-ttu-id="a0159-130">HSM 이름.</span><span class="sxs-lookup"><span data-stu-id="a0159-130">HSM name.</span></span> <span data-ttu-id="a0159-131">Cmdlet은 이름 및 현재 선택 된 환경에 따라 관리 되는 HSM의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0159-131">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByKeyNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0159-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a0159-132">-InputObject</span></span>
<span data-ttu-id="a0159-133">Key 개체</span><span class="sxs-lookup"><span data-stu-id="a0159-133">Key Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem
Parameter Sets: RemoveByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a0159-134">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="a0159-134">-InRemovedState</span></span>
<span data-ttu-id="a0159-135">이전에 삭제 된 키를 영구적으로 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0159-135">Remove the previously deleted key permanently.</span></span>

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

### <span data-ttu-id="a0159-136">-이름</span><span class="sxs-lookup"><span data-stu-id="a0159-136">-Name</span></span>
<span data-ttu-id="a0159-137">키 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a0159-137">Key name.</span></span>
<span data-ttu-id="a0159-138">Cmdlet은 관리 되는 HSM 이름, 현재 선택 된 환경 및 키 이름에서 키의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0159-138">Cmdlet constructs the FQDN of a key from managed HSM name, currently selected environment and key name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByKeyNameParameterSet
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0159-139">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a0159-139">-PassThru</span></span>
<span data-ttu-id="a0159-140">Cmdlet은 기본적으로 개체를 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a0159-140">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="a0159-141">이 스위치가 지정 된 경우 cmdlet은 삭제 된 키 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0159-141">If this switch is specified, the cmdlet returns the key object that was deleted.</span></span>

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

### <span data-ttu-id="a0159-142">-확인</span><span class="sxs-lookup"><span data-stu-id="a0159-142">-Confirm</span></span>
<span data-ttu-id="a0159-143">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0159-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0159-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0159-144">-WhatIf</span></span>
<span data-ttu-id="a0159-145">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a0159-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0159-146">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a0159-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0159-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0159-147">CommonParameters</span></span>
<span data-ttu-id="a0159-148">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0159-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0159-149">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a0159-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0159-150">입력</span><span class="sxs-lookup"><span data-stu-id="a0159-150">INPUTS</span></span>

### <span data-ttu-id="a0159-151">Microsoft. KeyVault. PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="a0159-151">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="a0159-152">출력</span><span class="sxs-lookup"><span data-stu-id="a0159-152">OUTPUTS</span></span>

### <span data-ttu-id="a0159-153">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="a0159-153">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span></span>

## <span data-ttu-id="a0159-154">상속자</span><span class="sxs-lookup"><span data-stu-id="a0159-154">NOTES</span></span>

## <span data-ttu-id="a0159-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a0159-155">RELATED LINKS</span></span>

[<span data-ttu-id="a0159-156">추가-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="a0159-156">Add-AzManagedHsmKey</span></span>](./Add-AzManagedHsmKey.md)

[<span data-ttu-id="a0159-157">백업-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="a0159-157">Backup-AzManagedHsmKey</span></span>](./Backup-AzManagedHsmKey.md)

[<span data-ttu-id="a0159-158">Get-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="a0159-158">Get-AzManagedHsmKey</span></span>](./Get-AzManagedHsmKey.md)

[<span data-ttu-id="a0159-159">실행 취소-AzManagedHsmKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="a0159-159">Undo-AzManagedHsmKeyRemoval</span></span>](./Undo-AzManagedHsmKeyRemoval.md)

[<span data-ttu-id="a0159-160">업데이트-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="a0159-160">Update-AzManagedHsmKey</span></span>](./Update-AzManagedHsmKey.md)

[<span data-ttu-id="a0159-161">Restore-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="a0159-161">Restore-AzManagedHsmKey</span></span>](./Restore-AzManagedHsmKey.md)