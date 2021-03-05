---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/powershell/module/az.sqlvirtualmachine/remove-azavailabilitygrouplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzAvailabilityGroupListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzAvailabilityGroupListener.md
ms.openlocfilehash: 56891d1dae20f89289b9c2f72bf87bfeed7bd347
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101978048"
---
# <span data-ttu-id="f612c-101">Remove-AzAvailabilityGroupListener</span><span class="sxs-lookup"><span data-stu-id="f612c-101">Remove-AzAvailabilityGroupListener</span></span>

## <span data-ttu-id="f612c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f612c-102">SYNOPSIS</span></span>
<span data-ttu-id="f612c-103">가용성 그룹 수신기 를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="f612c-103">Deletes an Availability Group Listener.</span></span>

## <span data-ttu-id="f612c-104">구문</span><span class="sxs-lookup"><span data-stu-id="f612c-104">SYNTAX</span></span>

### <span data-ttu-id="f612c-105">이름(기본값)</span><span class="sxs-lookup"><span data-stu-id="f612c-105">Name (Default)</span></span>
```
Remove-AzAvailabilityGroupListener [-AsJob] [-PassThru] [-ResourceGroupName] <String>
 [-SqlVMGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f612c-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="f612c-106">InputObject</span></span>
```
Remove-AzAvailabilityGroupListener [-InputObject] <AzureAvailabilityGroupListenerModel> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f612c-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="f612c-107">ResourceId</span></span>
```
Remove-AzAvailabilityGroupListener [-ResourceId] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f612c-108">SqlVmGroupObject</span><span class="sxs-lookup"><span data-stu-id="f612c-108">SqlVmGroupObject</span></span>
```
Remove-AzAvailabilityGroupListener [-AsJob] [-PassThru] [-SqlVMGroupObject] <AzureSqlVMGroupModel>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f612c-109">설명</span><span class="sxs-lookup"><span data-stu-id="f612c-109">DESCRIPTION</span></span>
<span data-ttu-id="f612c-110">Remove-AzAvailabilityGroupListener cmdlet은 가용성 그룹 수신기를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="f612c-110">The Remove-AzAvailabilityGroupListener cmdlet deletes an Availability Group Listener.</span></span>

## <span data-ttu-id="f612c-111">예제</span><span class="sxs-lookup"><span data-stu-id="f612c-111">EXAMPLES</span></span>

### <span data-ttu-id="f612c-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="f612c-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzAvailabilityGroupListener -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01 -Name AgListener01
```

<span data-ttu-id="f612c-113">Name ResourceGroupName GroupName AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="f612c-113">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="f612c-114">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="f612c-114">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

<span data-ttu-id="f612c-115">가용성 그룹 가용성 그룹 가용성Group01에서 가용성 그룹 수신기 AgListener01을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="f612c-115">Deletes the Availability Group Listener AgListener01 in the Availability Group AvailabilityGroup01.</span></span>

## <span data-ttu-id="f612c-116">매개 변수</span><span class="sxs-lookup"><span data-stu-id="f612c-116">PARAMETERS</span></span>

### <span data-ttu-id="f612c-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f612c-117">-AsJob</span></span>
<span data-ttu-id="f612c-118">백그라운드에서 cmdlet을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="f612c-118">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="f612c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f612c-119">-DefaultProfile</span></span>
<span data-ttu-id="f612c-120">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f612c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f612c-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f612c-121">-InputObject</span></span>
<span data-ttu-id="f612c-122">가용성 그룹 수신기 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="f612c-122">Availability Group Listener object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f612c-123">-Name</span><span class="sxs-lookup"><span data-stu-id="f612c-123">-Name</span></span>
<span data-ttu-id="f612c-124">가용성 그룹 수신기 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f612c-124">Availability Group Listener name.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, SqlVmGroupObject
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f612c-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f612c-125">-PassThru</span></span>
<span data-ttu-id="f612c-126">cmdlet 실행이 끝날 때 삭제된 리소스를 출력할지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f612c-126">Specifies whether to output the deleted resource at end of cmdlet execution.</span></span>

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

### <span data-ttu-id="f612c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f612c-127">-ResourceGroupName</span></span>
<span data-ttu-id="f612c-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f612c-128">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f612c-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f612c-129">-ResourceId</span></span>
<span data-ttu-id="f612c-130">가용성 그룹 수신기 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="f612c-130">Availability Group Listener Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f612c-131">-SqlVMGroupName</span><span class="sxs-lookup"><span data-stu-id="f612c-131">-SqlVMGroupName</span></span>
<span data-ttu-id="f612c-132">SQL 컴퓨터 그룹 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f612c-132">SQL virtual machine group name.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: GroupName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f612c-133">-SqlVMGroupObject</span><span class="sxs-lookup"><span data-stu-id="f612c-133">-SqlVMGroupObject</span></span>
<span data-ttu-id="f612c-134">SQL 가상 머신 그룹 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="f612c-134">SQL virtual machine Group object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel
Parameter Sets: SqlVmGroupObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f612c-135">-확인</span><span class="sxs-lookup"><span data-stu-id="f612c-135">-Confirm</span></span>
<span data-ttu-id="f612c-136">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f612c-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f612c-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f612c-137">-WhatIf</span></span>
<span data-ttu-id="f612c-138">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="f612c-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f612c-139">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f612c-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f612c-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f612c-140">CommonParameters</span></span>
<span data-ttu-id="f612c-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f612c-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f612c-142">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f612c-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f612c-143">입력</span><span class="sxs-lookup"><span data-stu-id="f612c-143">INPUTS</span></span>

### <span data-ttu-id="f612c-144">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="f612c-144">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

### <span data-ttu-id="f612c-145">System.String</span><span class="sxs-lookup"><span data-stu-id="f612c-145">System.String</span></span>

### <span data-ttu-id="f612c-146">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="f612c-146">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="f612c-147">출력</span><span class="sxs-lookup"><span data-stu-id="f612c-147">OUTPUTS</span></span>

### <span data-ttu-id="f612c-148">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="f612c-148">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

## <span data-ttu-id="f612c-149">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f612c-149">NOTES</span></span>

## <span data-ttu-id="f612c-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f612c-150">RELATED LINKS</span></span>
