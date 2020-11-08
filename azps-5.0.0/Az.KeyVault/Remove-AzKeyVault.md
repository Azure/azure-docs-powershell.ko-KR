---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 7A929BA8-02D9-4BBE-AFF3-B8781F8DDAD9
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVault.md
ms.openlocfilehash: 69a1155b99d054699c41cc0b26cd78ef4445f931
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215302"
---
# <span data-ttu-id="622ff-101">Remove-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="622ff-101">Remove-AzKeyVault</span></span>

## <span data-ttu-id="622ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="622ff-102">SYNOPSIS</span></span>
<span data-ttu-id="622ff-103">키 자격 증명 모음을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="622ff-103">Deletes a key vault.</span></span>

## <span data-ttu-id="622ff-104">구문과</span><span class="sxs-lookup"><span data-stu-id="622ff-104">SYNTAX</span></span>

### <span data-ttu-id="622ff-105">ByAvailableVault (기본값)</span><span class="sxs-lookup"><span data-stu-id="622ff-105">ByAvailableVault (Default)</span></span>
```
Remove-AzKeyVault [-VaultName] <String> [[-ResourceGroupName] <String>] [[-Location] <String>] [-Force]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="622ff-106">ByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="622ff-106">ByDeletedVault</span></span>
```
Remove-AzKeyVault [-VaultName] <String> [-Location] <String> [-InRemovedState] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="622ff-107">InputObjectByAvailableVault</span><span class="sxs-lookup"><span data-stu-id="622ff-107">InputObjectByAvailableVault</span></span>
```
Remove-AzKeyVault [-InputObject] <PSKeyVault> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="622ff-108">InputObjectByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="622ff-108">InputObjectByDeletedVault</span></span>
```
Remove-AzKeyVault [-InputObject] <PSKeyVault> [-InRemovedState] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="622ff-109">ResourceIdByAvailableVault</span><span class="sxs-lookup"><span data-stu-id="622ff-109">ResourceIdByAvailableVault</span></span>
```
Remove-AzKeyVault [-ResourceId] <String> [[-Location] <String>] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="622ff-110">ResourceIdByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="622ff-110">ResourceIdByDeletedVault</span></span>
```
Remove-AzKeyVault [-ResourceId] <String> [-Location] <String> [-InRemovedState] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="622ff-111">설명은</span><span class="sxs-lookup"><span data-stu-id="622ff-111">DESCRIPTION</span></span>
<span data-ttu-id="622ff-112">**AzKeyVault** cmdlet은 지정 된 키 자격 증명 모음을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="622ff-112">The **Remove-AzKeyVault** cmdlet deletes the specified key vault.</span></span>
<span data-ttu-id="622ff-113">또한 해당 인스턴스에 포함 된 모든 키와 비밀이 삭제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="622ff-113">It also deletes all keys and secrets contained in that instance.</span></span>
<span data-ttu-id="622ff-114">이 cmdlet에 대해 리소스 그룹을 지정 하는 것이 선택 사항 이지만 성능이 더 나은 지 확인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="622ff-114">Note that although specifying the resource group is optional for this cmdlet, you should so for better performance.</span></span>

## <span data-ttu-id="622ff-115">예제의</span><span class="sxs-lookup"><span data-stu-id="622ff-115">EXAMPLES</span></span>

### <span data-ttu-id="622ff-116">예제 1: 키 자격 증명 모음 제거</span><span class="sxs-lookup"><span data-stu-id="622ff-116">Example 1: Remove a key vault</span></span>
```powershell
PS C:\> Remove-AzKeyVault -VaultName "Contoso03Vault" -PassThru

True
```

<span data-ttu-id="622ff-117">이 명령은 현재 구독에서 Contoso03Vault 이라는 키 자격 증명 모음을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="622ff-117">This command removes the key vault named Contoso03Vault from your current subscription.</span></span>

### <span data-ttu-id="622ff-118">예제 2: 지정 된 리소스 그룹에서 키 보관소 제거</span><span class="sxs-lookup"><span data-stu-id="622ff-118">Example 2: Remove a key vault from a specified resource group</span></span>
```powershell
PS C:\> Remove-AzKeyVault -Name "Contoso03Vault" -ResourceGroupName "Group14" -PassThru

True
```

<span data-ttu-id="622ff-119">이 명령은 이름이 지정 된 리소스 그룹에서 Contoso03Vault 이라는 키 자격 증명 모음을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="622ff-119">This command removes the key vault named Contoso03Vault from the named resource group.</span></span>
<span data-ttu-id="622ff-120">리소스 그룹 이름을 지정 하지 않으면 cmdlet이 지정 된 키 보관소를 검색 하 여 현재 구독에서 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="622ff-120">If you do not specify the resource group name, the cmdlet searches for the named key vault to delete in your current subscription.</span></span>

### <span data-ttu-id="622ff-121">예제 3: 관리 되는 hsm 제거</span><span class="sxs-lookup"><span data-stu-id="622ff-121">Example 3: Remove a managed hsm</span></span>
```powershell
PS C:\>  Remove-AzKeyVault -Name "testManagedHsm" -Hsm -PassThru

True
```

<span data-ttu-id="622ff-122">이 명령은 현재 구독에서 testManagedHsm 이라는 관리 되는 hsm을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="622ff-122">This command removes the managed hsm named testManagedHsm from your current subscription.</span></span>

## <span data-ttu-id="622ff-123">변수</span><span class="sxs-lookup"><span data-stu-id="622ff-123">PARAMETERS</span></span>

### <span data-ttu-id="622ff-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="622ff-124">-AsJob</span></span>
<span data-ttu-id="622ff-125">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="622ff-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="622ff-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="622ff-126">-DefaultProfile</span></span>
<span data-ttu-id="622ff-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="622ff-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="622ff-128">-Force</span><span class="sxs-lookup"><span data-stu-id="622ff-128">-Force</span></span>
<span data-ttu-id="622ff-129">Cmdlet이 확인을 묻는 메시지를 표시 하지 않음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="622ff-129">Indicates that the cmdlet does not prompt you for confirmation.</span></span>
<span data-ttu-id="622ff-130">기본적으로이 cmdlet은 키 자격 증명을 삭제할 것인지 확인 하는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="622ff-130">By default, this cmdlet prompts you to confirm that you want to delete the key vault.</span></span>

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

### <span data-ttu-id="622ff-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="622ff-131">-InputObject</span></span>
<span data-ttu-id="622ff-132">삭제할 키 자격 증명 모음 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="622ff-132">Key Vault object to be deleted.</span></span>

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

### <span data-ttu-id="622ff-133">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="622ff-133">-InRemovedState</span></span>
<span data-ttu-id="622ff-134">이전에 삭제 된 자격 증명을 영구적으로 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="622ff-134">Remove the previously deleted vault permanently.</span></span>

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

### <span data-ttu-id="622ff-135">-위치</span><span class="sxs-lookup"><span data-stu-id="622ff-135">-Location</span></span>
<span data-ttu-id="622ff-136">삭제 된 자격 증명 모음의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="622ff-136">The location of the deleted vault.</span></span>

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

### <span data-ttu-id="622ff-137">-PassThru</span><span class="sxs-lookup"><span data-stu-id="622ff-137">-PassThru</span></span>
<span data-ttu-id="622ff-138">이 Cmdlet은 기본적으로 개체를 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="622ff-138">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="622ff-139">이 스위치를 지정 하면 성공한 경우 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="622ff-139">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="622ff-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="622ff-140">-ResourceGroupName</span></span>
<span data-ttu-id="622ff-141">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="622ff-141">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="622ff-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="622ff-142">-ResourceId</span></span>
<span data-ttu-id="622ff-143">KeyVault 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="622ff-143">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="622ff-144">-VaultName</span><span class="sxs-lookup"><span data-stu-id="622ff-144">-VaultName</span></span>
<span data-ttu-id="622ff-145">제거할 키 보관소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="622ff-145">Specifies the name of the key vault to remove.</span></span>

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

### <span data-ttu-id="622ff-146">-확인</span><span class="sxs-lookup"><span data-stu-id="622ff-146">-Confirm</span></span>
<span data-ttu-id="622ff-147">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="622ff-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="622ff-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="622ff-148">-WhatIf</span></span>
<span data-ttu-id="622ff-149">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="622ff-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="622ff-150">Cmdlet이 실행 되지 않습니다. Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="622ff-150">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="622ff-151">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="622ff-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="622ff-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="622ff-152">CommonParameters</span></span>
<span data-ttu-id="622ff-153">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="622ff-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="622ff-154">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="622ff-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="622ff-155">입력</span><span class="sxs-lookup"><span data-stu-id="622ff-155">INPUTS</span></span>

### <span data-ttu-id="622ff-156">Microsoft. KeyVault. 모델. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="622ff-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="622ff-157">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="622ff-157">System.String</span></span>

## <span data-ttu-id="622ff-158">출력</span><span class="sxs-lookup"><span data-stu-id="622ff-158">OUTPUTS</span></span>

### <span data-ttu-id="622ff-159">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="622ff-159">System.Boolean</span></span>

## <span data-ttu-id="622ff-160">상속자</span><span class="sxs-lookup"><span data-stu-id="622ff-160">NOTES</span></span>

## <span data-ttu-id="622ff-161">관련 링크</span><span class="sxs-lookup"><span data-stu-id="622ff-161">RELATED LINKS</span></span>

[<span data-ttu-id="622ff-162">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="622ff-162">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)

[<span data-ttu-id="622ff-163">새로운 AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="622ff-163">New-AzKeyVault</span></span>](./New-AzKeyVault.md)
