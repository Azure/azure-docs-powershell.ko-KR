---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 7A929BA8-02D9-4BBE-AFF3-B8781F8DDAD9
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVault.md
ms.openlocfilehash: 69a1155b99d054699c41cc0b26cd78ef4445f931
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495439"
---
# <span data-ttu-id="a5fec-101">Remove-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="a5fec-101">Remove-AzKeyVault</span></span>

## <span data-ttu-id="a5fec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5fec-102">SYNOPSIS</span></span>
<span data-ttu-id="a5fec-103">키 자격 증명 모음을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fec-103">Deletes a key vault.</span></span>

## <span data-ttu-id="a5fec-104">구문</span><span class="sxs-lookup"><span data-stu-id="a5fec-104">SYNTAX</span></span>

### <span data-ttu-id="a5fec-105">ByAvailableVault(기본값)</span><span class="sxs-lookup"><span data-stu-id="a5fec-105">ByAvailableVault (Default)</span></span>
```
Remove-AzKeyVault [-VaultName] <String> [[-ResourceGroupName] <String>] [[-Location] <String>] [-Force]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5fec-106">ByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="a5fec-106">ByDeletedVault</span></span>
```
Remove-AzKeyVault [-VaultName] <String> [-Location] <String> [-InRemovedState] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5fec-107">InputObjectByAvailableVault</span><span class="sxs-lookup"><span data-stu-id="a5fec-107">InputObjectByAvailableVault</span></span>
```
Remove-AzKeyVault [-InputObject] <PSKeyVault> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5fec-108">InputObjectByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="a5fec-108">InputObjectByDeletedVault</span></span>
```
Remove-AzKeyVault [-InputObject] <PSKeyVault> [-InRemovedState] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5fec-109">ResourceIdByAvailableVault</span><span class="sxs-lookup"><span data-stu-id="a5fec-109">ResourceIdByAvailableVault</span></span>
```
Remove-AzKeyVault [-ResourceId] <String> [[-Location] <String>] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5fec-110">ResourceIdByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="a5fec-110">ResourceIdByDeletedVault</span></span>
```
Remove-AzKeyVault [-ResourceId] <String> [-Location] <String> [-InRemovedState] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5fec-111">설명</span><span class="sxs-lookup"><span data-stu-id="a5fec-111">DESCRIPTION</span></span>
<span data-ttu-id="a5fec-112">**Remove-AzKeyVault** cmdlet은 지정된 키 자격 증명 모음을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fec-112">The **Remove-AzKeyVault** cmdlet deletes the specified key vault.</span></span>
<span data-ttu-id="a5fec-113">또한 해당 인스턴스에 포함된 모든 키와 비밀도 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fec-113">It also deletes all keys and secrets contained in that instance.</span></span>
<span data-ttu-id="a5fec-114">이 cmdlet에 대해 리소스 그룹을 지정하는 것은 선택 사항이지만 성능을 향상하기 위해 이렇게 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fec-114">Note that although specifying the resource group is optional for this cmdlet, you should so for better performance.</span></span>

## <span data-ttu-id="a5fec-115">예제</span><span class="sxs-lookup"><span data-stu-id="a5fec-115">EXAMPLES</span></span>

### <span data-ttu-id="a5fec-116">예제 1: 키 자격 증명 모음 제거</span><span class="sxs-lookup"><span data-stu-id="a5fec-116">Example 1: Remove a key vault</span></span>
```powershell
PS C:\> Remove-AzKeyVault -VaultName "Contoso03Vault" -PassThru

True
```

<span data-ttu-id="a5fec-117">이 명령은 현재 구독에서 Contoso03Vault라는 키 자격 증명 모음을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fec-117">This command removes the key vault named Contoso03Vault from your current subscription.</span></span>

### <span data-ttu-id="a5fec-118">예제 2: 지정된 리소스 그룹에서 키 자격 증명 모음 제거</span><span class="sxs-lookup"><span data-stu-id="a5fec-118">Example 2: Remove a key vault from a specified resource group</span></span>
```powershell
PS C:\> Remove-AzKeyVault -Name "Contoso03Vault" -ResourceGroupName "Group14" -PassThru

True
```

<span data-ttu-id="a5fec-119">이 명령은 명명된 리소스 그룹에서 Contoso03Vault라는 키 자격 증명 모음을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fec-119">This command removes the key vault named Contoso03Vault from the named resource group.</span></span>
<span data-ttu-id="a5fec-120">리소스 그룹 이름을 지정하지 않으면 cmdlet은 현재 구독에서 삭제할 명명된 키 자격 증명 모음을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fec-120">If you do not specify the resource group name, the cmdlet searches for the named key vault to delete in your current subscription.</span></span>

### <span data-ttu-id="a5fec-121">예제 3: 관리되는 hsm 제거</span><span class="sxs-lookup"><span data-stu-id="a5fec-121">Example 3: Remove a managed hsm</span></span>
```powershell
PS C:\>  Remove-AzKeyVault -Name "testManagedHsm" -Hsm -PassThru

True
```

<span data-ttu-id="a5fec-122">이 명령은 현재 구독에서 testManagedHsm이라는 관리되는 hsm을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fec-122">This command removes the managed hsm named testManagedHsm from your current subscription.</span></span>

## <span data-ttu-id="a5fec-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a5fec-123">PARAMETERS</span></span>

### <span data-ttu-id="a5fec-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a5fec-124">-AsJob</span></span>
<span data-ttu-id="a5fec-125">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="a5fec-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a5fec-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5fec-126">-DefaultProfile</span></span>
<span data-ttu-id="a5fec-127">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="a5fec-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a5fec-128">-Force</span><span class="sxs-lookup"><span data-stu-id="a5fec-128">-Force</span></span>
<span data-ttu-id="a5fec-129">cmdlet이 확인 메시지를 표시하지 않는다는 의미입니다.</span><span class="sxs-lookup"><span data-stu-id="a5fec-129">Indicates that the cmdlet does not prompt you for confirmation.</span></span>
<span data-ttu-id="a5fec-130">기본적으로 이 cmdlet은 키 자격 증명 모음을 삭제할지 묻는 메시지를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fec-130">By default, this cmdlet prompts you to confirm that you want to delete the key vault.</span></span>

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

### <span data-ttu-id="a5fec-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a5fec-131">-InputObject</span></span>
<span data-ttu-id="a5fec-132">삭제할 Key Vault 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="a5fec-132">Key Vault object to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: InputObjectByAvailableVault, InputObjectByDeletedVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a5fec-133">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="a5fec-133">-InRemovedState</span></span>
<span data-ttu-id="a5fec-134">이전에 삭제된 자격 증명 모음을 영구적으로 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fec-134">Remove the previously deleted vault permanently.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByDeletedVault, InputObjectByDeletedVault, ResourceIdByDeletedVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5fec-135">-Location</span><span class="sxs-lookup"><span data-stu-id="a5fec-135">-Location</span></span>
<span data-ttu-id="a5fec-136">삭제된 자격 증명 모음의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="a5fec-136">The location of the deleted vault.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAvailableVault, ResourceIdByAvailableVault
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByDeletedVault, ResourceIdByDeletedVault
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5fec-137">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a5fec-137">-PassThru</span></span>
<span data-ttu-id="a5fec-138">이 Cmdlet은 기본적으로 개체를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a5fec-138">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="a5fec-139">이 스위치를 지정하면 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fec-139">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="a5fec-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5fec-140">-ResourceGroupName</span></span>
<span data-ttu-id="a5fec-141">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fec-141">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAvailableVault
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5fec-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a5fec-142">-ResourceId</span></span>
<span data-ttu-id="a5fec-143">KeyVault 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="a5fec-143">KeyVault Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdByAvailableVault, ResourceIdByDeletedVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5fec-144">-VaultName</span><span class="sxs-lookup"><span data-stu-id="a5fec-144">-VaultName</span></span>
<span data-ttu-id="a5fec-145">제거할 키 자격 증명 모음의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fec-145">Specifies the name of the key vault to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAvailableVault, ByDeletedVault
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5fec-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a5fec-146">-Confirm</span></span>
<span data-ttu-id="a5fec-147">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a5fec-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5fec-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5fec-148">-WhatIf</span></span>
<span data-ttu-id="a5fec-149">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="a5fec-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5fec-150">cmdlet이 실행되지 않습니다. cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="a5fec-150">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5fec-151">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a5fec-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5fec-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5fec-152">CommonParameters</span></span>
<span data-ttu-id="a5fec-153">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fec-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5fec-154">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a5fec-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5fec-155">입력</span><span class="sxs-lookup"><span data-stu-id="a5fec-155">INPUTS</span></span>

### <span data-ttu-id="a5fec-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="a5fec-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="a5fec-157">System.String</span><span class="sxs-lookup"><span data-stu-id="a5fec-157">System.String</span></span>

## <span data-ttu-id="a5fec-158">출력</span><span class="sxs-lookup"><span data-stu-id="a5fec-158">OUTPUTS</span></span>

### <span data-ttu-id="a5fec-159">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a5fec-159">System.Boolean</span></span>

## <span data-ttu-id="a5fec-160">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a5fec-160">NOTES</span></span>

## <span data-ttu-id="a5fec-161">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a5fec-161">RELATED LINKS</span></span>

[<span data-ttu-id="a5fec-162">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="a5fec-162">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)

[<span data-ttu-id="a5fec-163">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="a5fec-163">New-AzKeyVault</span></span>](./New-AzKeyVault.md)
