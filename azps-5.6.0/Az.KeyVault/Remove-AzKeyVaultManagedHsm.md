---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/remove-azkeyvaultmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedHsm.md
ms.openlocfilehash: ac778148f90d90caf52fdb3c029376daf4470069
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991116"
---
# <span data-ttu-id="04401-101">Remove-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="04401-101">Remove-AzKeyVaultManagedHsm</span></span>

## <span data-ttu-id="04401-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04401-102">SYNOPSIS</span></span>
<span data-ttu-id="04401-103">관리되는 HSM을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="04401-103">Deletes a managed HSM.</span></span>

## <span data-ttu-id="04401-104">구문</span><span class="sxs-lookup"><span data-stu-id="04401-104">SYNTAX</span></span>

### <span data-ttu-id="04401-105">RemoveManagedHsmByName(기본값)</span><span class="sxs-lookup"><span data-stu-id="04401-105">RemoveManagedHsmByName (Default)</span></span>
```
Remove-AzKeyVaultManagedHsm [-Name] <String> [[-ResourceGroupName] <String>] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04401-106">RemoveManagedHsmByInputObject</span><span class="sxs-lookup"><span data-stu-id="04401-106">RemoveManagedHsmByInputObject</span></span>
```
Remove-AzKeyVaultManagedHsm [-InputObject] <PSManagedHsm> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04401-107">RemoveManagedHsmByResourceId</span><span class="sxs-lookup"><span data-stu-id="04401-107">RemoveManagedHsmByResourceId</span></span>
```
Remove-AzKeyVaultManagedHsm [-ResourceId] <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04401-108">설명</span><span class="sxs-lookup"><span data-stu-id="04401-108">DESCRIPTION</span></span>
<span data-ttu-id="04401-109">**Remove-AzKeyVaultManagedHsm** cmdlet은 지정된 관리되는 HSM을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="04401-109">The **Remove-AzKeyVaultManagedHsm** cmdlet deletes the specified managed HSM.</span></span>
<span data-ttu-id="04401-110">또한 해당 인스턴스에 포함된 모든 키를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="04401-110">It also deletes all keys contained in that instance.</span></span>
<span data-ttu-id="04401-111">리소스 그룹을 지정하는 것은 이 cmdlet에 대한 선택 사항이지만 성능을 향상하기 위해 그렇게 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="04401-111">Note that although specifying the resource group is optional for this cmdlet, you should so for better performance.</span></span>

## <span data-ttu-id="04401-112">예제</span><span class="sxs-lookup"><span data-stu-id="04401-112">EXAMPLES</span></span>

### <span data-ttu-id="04401-113">예제 1: 관리되는 HSM 제거</span><span class="sxs-lookup"><span data-stu-id="04401-113">Example 1: Remove a managed HSM</span></span>
```powershell
PS C:\> Remove-AzKeyVaultManagedHsm -HsmName 'myhsm' -Force

True
```

<span data-ttu-id="04401-114">이 명령은 현재 구독에서 myhsm이라는 관리되는 hsm을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="04401-114">This command removes the managed hsm named myhsm from your current subscription.</span></span>

### <span data-ttu-id="04401-115">예제 2: 지정된 리소스 그룹에서 관리되는 hsm 제거</span><span class="sxs-lookup"><span data-stu-id="04401-115">Example 2: Remove a managed hsm from a specified resource group</span></span>
```powershell
PS C:\> Remove-AzKeyVaultManagedHsm -HsmName 'myhsm' -ResourceGroupName "myrg1" -PassThru

True
```

<span data-ttu-id="04401-116">이 명령은 myrg1이라는 리소스 그룹에서 myhsm이라는 관리되는 hsm을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="04401-116">This command removes the managed hsm named myhsm from the resource group named myrg1.</span></span>
<span data-ttu-id="04401-117">리소스 그룹 이름을 지정하지 않으면 cmdlet은 현재 구독에서 삭제하기 위해 명명된 관리되는 HSM을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="04401-117">If you do not specify the resource group name, the cmdlet searches for the named managed HSM to delete in your current subscription.</span></span>

## <span data-ttu-id="04401-118">매개 변수</span><span class="sxs-lookup"><span data-stu-id="04401-118">PARAMETERS</span></span>

### <span data-ttu-id="04401-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="04401-119">-AsJob</span></span>
<span data-ttu-id="04401-120">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="04401-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="04401-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04401-121">-DefaultProfile</span></span>
<span data-ttu-id="04401-122">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="04401-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04401-123">-Force</span><span class="sxs-lookup"><span data-stu-id="04401-123">-Force</span></span>
<span data-ttu-id="04401-124">cmdlet에서 확인을 묻는 메시지가 표시되지 않는다는 의미입니다.</span><span class="sxs-lookup"><span data-stu-id="04401-124">Indicates that the cmdlet does not prompt you for confirmation.</span></span>
<span data-ttu-id="04401-125">기본적으로 이 cmdlet은 관리되는 HSM을 삭제하려는지 확인하라는 메시지를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="04401-125">By default, this cmdlet prompts you to confirm that you want to delete the managed HSM.</span></span>

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

### <span data-ttu-id="04401-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="04401-126">-InputObject</span></span>
<span data-ttu-id="04401-127">삭제할 관리되는 HSM 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="04401-127">Managed HSM object to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: RemoveManagedHsmByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="04401-128">-Name</span><span class="sxs-lookup"><span data-stu-id="04401-128">-Name</span></span>
<span data-ttu-id="04401-129">제거할 관리되는 HSM의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="04401-129">Specifies the name of the managed HSM to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveManagedHsmByName
Aliases: HsmName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04401-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="04401-130">-PassThru</span></span>
<span data-ttu-id="04401-131">이 Cmdlet은 기본적으로 개체를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="04401-131">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="04401-132">이 스위치가 지정되어 있는 경우 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="04401-132">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="04401-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04401-133">-ResourceGroupName</span></span>
<span data-ttu-id="04401-134">제거할 Azure 관리 HSM에 대한 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="04401-134">Specifies the name of resource group for Azure managed HSM to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveManagedHsmByName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04401-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="04401-135">-ResourceId</span></span>
<span data-ttu-id="04401-136">ManagedHsm 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="04401-136">ManagedHsm Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveManagedHsmByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04401-137">-확인</span><span class="sxs-lookup"><span data-stu-id="04401-137">-Confirm</span></span>
<span data-ttu-id="04401-138">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="04401-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04401-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04401-139">-WhatIf</span></span>
<span data-ttu-id="04401-140">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="04401-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04401-141">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="04401-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04401-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04401-142">CommonParameters</span></span>
<span data-ttu-id="04401-143">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="04401-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04401-144">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="04401-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04401-145">입력</span><span class="sxs-lookup"><span data-stu-id="04401-145">INPUTS</span></span>

### <span data-ttu-id="04401-146">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span><span class="sxs-lookup"><span data-stu-id="04401-146">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

### <span data-ttu-id="04401-147">System.String</span><span class="sxs-lookup"><span data-stu-id="04401-147">System.String</span></span>

## <span data-ttu-id="04401-148">출력</span><span class="sxs-lookup"><span data-stu-id="04401-148">OUTPUTS</span></span>

### <span data-ttu-id="04401-149">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="04401-149">System.Boolean</span></span>

## <span data-ttu-id="04401-150">참고 사항</span><span class="sxs-lookup"><span data-stu-id="04401-150">NOTES</span></span>

## <span data-ttu-id="04401-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="04401-151">RELATED LINKS</span></span>

[<span data-ttu-id="04401-152">Get-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="04401-152">Get-AzKeyVaultManagedHsm</span></span>](./Get-AzKeyVaultManagedHsm.md)

[<span data-ttu-id="04401-153">New-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="04401-153">New-AzKeyVaultManagedHsm</span></span>](./New-AzKeyVaultManagedHsm.md)

[<span data-ttu-id="04401-154">Update-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="04401-154">Update-AzKeyVaultManagedHsm</span></span>](./Update-AzKeyVaultManagedHsm.md)