---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzManagedHsm.md
ms.openlocfilehash: 6555299726d8dcf443382f72c2aba6324b6b377d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215294"
---
# <span data-ttu-id="d849b-101">Remove-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="d849b-101">Remove-AzManagedHsm</span></span>

## <span data-ttu-id="d849b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d849b-102">SYNOPSIS</span></span>
<span data-ttu-id="d849b-103">관리 되는 HSM을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="d849b-103">Deletes a managed HSM.</span></span>

## <span data-ttu-id="d849b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d849b-104">SYNTAX</span></span>

### <span data-ttu-id="d849b-105">RemoveManagedHsmByName (기본값)</span><span class="sxs-lookup"><span data-stu-id="d849b-105">RemoveManagedHsmByName (Default)</span></span>
```
Remove-AzManagedHsm [-Name] <String> [[-ResourceGroupName] <String>] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d849b-106">RemoveManagedHsmByInputObject</span><span class="sxs-lookup"><span data-stu-id="d849b-106">RemoveManagedHsmByInputObject</span></span>
```
Remove-AzManagedHsm [-InputObject] <PSManagedHsm> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d849b-107">RemoveManagedHsmByResourceId</span><span class="sxs-lookup"><span data-stu-id="d849b-107">RemoveManagedHsmByResourceId</span></span>
```
Remove-AzManagedHsm [-ResourceId] <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d849b-108">설명은</span><span class="sxs-lookup"><span data-stu-id="d849b-108">DESCRIPTION</span></span>
<span data-ttu-id="d849b-109">**AzManagedHsm** cmdlet은 지정 된 관리 되는 HSM을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="d849b-109">The **Remove-AzManagedHsm** cmdlet deletes the specified managed HSM.</span></span>
<span data-ttu-id="d849b-110">또한 해당 인스턴스에 포함 된 모든 키를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="d849b-110">It also deletes all keys contained in that instance.</span></span>
<span data-ttu-id="d849b-111">이 cmdlet에 대해 리소스 그룹을 지정 하는 것이 선택 사항 이지만 성능이 더 나은 지 확인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d849b-111">Note that although specifying the resource group is optional for this cmdlet, you should so for better performance.</span></span>

## <span data-ttu-id="d849b-112">예제의</span><span class="sxs-lookup"><span data-stu-id="d849b-112">EXAMPLES</span></span>

### <span data-ttu-id="d849b-113">예제 1: 관리 되는 HSM 제거</span><span class="sxs-lookup"><span data-stu-id="d849b-113">Example 1: Remove a managed HSM</span></span>
```powershell
PS C:\> Remove-AzManagedHsm -HsmName 'myhsm' -Force

True
```

<span data-ttu-id="d849b-114">이 명령은 현재 구독에서 myhsm 이라는 관리 되는 hsm을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d849b-114">This command removes the managed hsm named myhsm from your current subscription.</span></span>

### <span data-ttu-id="d849b-115">예제 2: 지정 된 리소스 그룹에서 관리 되는 hsm 제거</span><span class="sxs-lookup"><span data-stu-id="d849b-115">Example 2: Remove a managed hsm from a specified resource group</span></span>
```powershell
PS C:\> Remove-AzManagedHsm -HsmName 'myhsm' -ResourceGroupName "myrg1" -PassThru

True
```

<span data-ttu-id="d849b-116">이 명령은 myrg1 이라는 리소스 그룹에서 myhsm 이라는 관리 되는 hsm을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d849b-116">This command removes the managed hsm named myhsm from the resource group named myrg1.</span></span>
<span data-ttu-id="d849b-117">리소스 그룹 이름을 지정 하지 않으면 cmdlet이 현재 구독에서 삭제 하려는 명명 된 관리 되는 HSM을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="d849b-117">If you do not specify the resource group name, the cmdlet searches for the named managed HSM to delete in your current subscription.</span></span>

## <span data-ttu-id="d849b-118">변수</span><span class="sxs-lookup"><span data-stu-id="d849b-118">PARAMETERS</span></span>

### <span data-ttu-id="d849b-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d849b-119">-AsJob</span></span>
<span data-ttu-id="d849b-120">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="d849b-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d849b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d849b-121">-DefaultProfile</span></span>
<span data-ttu-id="d849b-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d849b-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d849b-123">-Force</span><span class="sxs-lookup"><span data-stu-id="d849b-123">-Force</span></span>
<span data-ttu-id="d849b-124">Cmdlet이 확인을 묻는 메시지를 표시 하지 않음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="d849b-124">Indicates that the cmdlet does not prompt you for confirmation.</span></span>
<span data-ttu-id="d849b-125">기본적으로이 cmdlet은 관리 되는 HSM을 삭제할지 확인 하는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d849b-125">By default, this cmdlet prompts you to confirm that you want to delete the managed HSM.</span></span>

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

### <span data-ttu-id="d849b-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d849b-126">-InputObject</span></span>
<span data-ttu-id="d849b-127">삭제할 관리 되는 HSM 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="d849b-127">Managed HSM object to be deleted.</span></span>

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

### <span data-ttu-id="d849b-128">-이름</span><span class="sxs-lookup"><span data-stu-id="d849b-128">-Name</span></span>
<span data-ttu-id="d849b-129">제거할 관리 되는 HSM의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d849b-129">Specifies the name of the managed HSM to remove.</span></span>

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

### <span data-ttu-id="d849b-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d849b-130">-PassThru</span></span>
<span data-ttu-id="d849b-131">이 Cmdlet은 기본적으로 개체를 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d849b-131">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="d849b-132">이 스위치를 지정 하면 성공한 경우 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="d849b-132">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="d849b-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d849b-133">-ResourceGroupName</span></span>
<span data-ttu-id="d849b-134">제거할 Azure 관리 HSM에 대 한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d849b-134">Specifies the name of resource group for Azure managed HSM to remove.</span></span>

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

### <span data-ttu-id="d849b-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d849b-135">-ResourceId</span></span>
<span data-ttu-id="d849b-136">ManagedHsm 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="d849b-136">ManagedHsm Resource Id.</span></span>

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

### <span data-ttu-id="d849b-137">-확인</span><span class="sxs-lookup"><span data-stu-id="d849b-137">-Confirm</span></span>
<span data-ttu-id="d849b-138">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d849b-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d849b-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d849b-139">-WhatIf</span></span>
<span data-ttu-id="d849b-140">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d849b-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d849b-141">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d849b-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d849b-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d849b-142">CommonParameters</span></span>
<span data-ttu-id="d849b-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d849b-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d849b-144">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d849b-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d849b-145">입력</span><span class="sxs-lookup"><span data-stu-id="d849b-145">INPUTS</span></span>

### <span data-ttu-id="d849b-146">Microsoft. KeyVault. 모델. PSManagedHsm</span><span class="sxs-lookup"><span data-stu-id="d849b-146">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

### <span data-ttu-id="d849b-147">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d849b-147">System.String</span></span>

## <span data-ttu-id="d849b-148">출력</span><span class="sxs-lookup"><span data-stu-id="d849b-148">OUTPUTS</span></span>

### <span data-ttu-id="d849b-149">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="d849b-149">System.Boolean</span></span>

## <span data-ttu-id="d849b-150">상속자</span><span class="sxs-lookup"><span data-stu-id="d849b-150">NOTES</span></span>

## <span data-ttu-id="d849b-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d849b-151">RELATED LINKS</span></span>

[<span data-ttu-id="d849b-152">Get-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="d849b-152">Get-AzManagedHsm</span></span>](./Get-AzManagedHsm.md)

[<span data-ttu-id="d849b-153">새로운 AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="d849b-153">New-AzManagedHsm</span></span>](./New-AzManagedHsm.md)

[<span data-ttu-id="d849b-154">업데이트-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="d849b-154">Update-AzManagedHsm</span></span>](./Update-AzManagedHsm.md)