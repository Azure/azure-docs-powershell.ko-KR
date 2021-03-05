---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/powershell/module/az.sqlvirtualmachine/update-azavailabilitygrouplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzAvailabilityGroupListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzAvailabilityGroupListener.md
ms.openlocfilehash: c94f1e842697a64dd95f7d5ccb90e389484a61e0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967248"
---
# <span data-ttu-id="ca223-101">Update-AzAvailabilityGroupListener</span><span class="sxs-lookup"><span data-stu-id="ca223-101">Update-AzAvailabilityGroupListener</span></span>

## <span data-ttu-id="ca223-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca223-102">SYNOPSIS</span></span>
<span data-ttu-id="ca223-103">가용성 그룹 수신기 업데이트.</span><span class="sxs-lookup"><span data-stu-id="ca223-103">Updates the Availability Group Listener.</span></span>

## <span data-ttu-id="ca223-104">구문</span><span class="sxs-lookup"><span data-stu-id="ca223-104">SYNTAX</span></span>

### <span data-ttu-id="ca223-105">이름(기본값)</span><span class="sxs-lookup"><span data-stu-id="ca223-105">Name (Default)</span></span>
```
Update-AzAvailabilityGroupListener [-SqlVirtualMachineId <String[]>] [-AsJob] [-ResourceGroupName] <String>
 [-SqlVMGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ca223-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="ca223-106">InputObject</span></span>
```
Update-AzAvailabilityGroupListener [-InputObject] <AzureAvailabilityGroupListenerModel>
 [-SqlVirtualMachineId <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ca223-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="ca223-107">ResourceId</span></span>
```
Update-AzAvailabilityGroupListener [-ResourceId] <String> [-SqlVirtualMachineId <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca223-108">SqlVmGroupObject</span><span class="sxs-lookup"><span data-stu-id="ca223-108">SqlVmGroupObject</span></span>
```
Update-AzAvailabilityGroupListener [-SqlVirtualMachineId <String[]>] [-AsJob]
 [-SqlVMGroupObject] <AzureSqlVMGroupModel> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca223-109">설명</span><span class="sxs-lookup"><span data-stu-id="ca223-109">DESCRIPTION</span></span>
<span data-ttu-id="ca223-110">Update-AzAvailabilityGroupListener cmdlet은 가용성 그룹 수신기를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="ca223-110">The Update-AzAvailabilityGroupListener cmdlet updates an Availability Group Listener.</span></span>

## <span data-ttu-id="ca223-111">예제</span><span class="sxs-lookup"><span data-stu-id="ca223-111">EXAMPLES</span></span>

### <span data-ttu-id="ca223-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="ca223-112">Example 1</span></span>
```powershell
PS C:\> Update-AzAvailabilityGroupListener -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01 -Name AgListener01 -SqlVirtualMachineId $VmResourceId01,$VmResourceId02
```

<span data-ttu-id="ca223-113">Name ResourceGroupName GroupName AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="ca223-113">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="ca223-114">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="ca223-114">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

<span data-ttu-id="ca223-115">가용성 그룹 수신기에 SQL Virtual Machines에서 목록을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="ca223-115">Updates the list SQL Virtual Machines for the Availability Group Listener.</span></span>

## <span data-ttu-id="ca223-116">매개 변수</span><span class="sxs-lookup"><span data-stu-id="ca223-116">PARAMETERS</span></span>

### <span data-ttu-id="ca223-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ca223-117">-AsJob</span></span>
<span data-ttu-id="ca223-118">백그라운드에서 cmdlet을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="ca223-118">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="ca223-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca223-119">-DefaultProfile</span></span>
<span data-ttu-id="ca223-120">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ca223-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca223-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ca223-121">-InputObject</span></span>
<span data-ttu-id="ca223-122">가용성 그룹 수신기 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="ca223-122">Availability Group Listener object.</span></span>

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

### <span data-ttu-id="ca223-123">-Name</span><span class="sxs-lookup"><span data-stu-id="ca223-123">-Name</span></span>
<span data-ttu-id="ca223-124">가용성 그룹 수신기 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ca223-124">Availability Group Listener name.</span></span>

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

### <span data-ttu-id="ca223-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca223-125">-ResourceGroupName</span></span>
<span data-ttu-id="ca223-126">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ca223-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="ca223-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ca223-127">-ResourceId</span></span>
<span data-ttu-id="ca223-128">가용성 그룹 수신기 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="ca223-128">Availability Group Listener Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases: AvailabilityGroupListenerId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca223-129">-SqlVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="ca223-129">-SqlVirtualMachineId</span></span>
<span data-ttu-id="ca223-130">Sql VM 리소스 아이디 목록</span><span class="sxs-lookup"><span data-stu-id="ca223-130">List of Sql VM Resource IDs</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca223-131">-SqlVMGroupName</span><span class="sxs-lookup"><span data-stu-id="ca223-131">-SqlVMGroupName</span></span>
<span data-ttu-id="ca223-132">SQL 컴퓨터 그룹 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ca223-132">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="ca223-133">-SqlVMGroupObject</span><span class="sxs-lookup"><span data-stu-id="ca223-133">-SqlVMGroupObject</span></span>
<span data-ttu-id="ca223-134">SQL 가상 머신 그룹 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="ca223-134">SQL virtual machine Group object.</span></span>

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

### <span data-ttu-id="ca223-135">-확인</span><span class="sxs-lookup"><span data-stu-id="ca223-135">-Confirm</span></span>
<span data-ttu-id="ca223-136">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ca223-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca223-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca223-137">-WhatIf</span></span>
<span data-ttu-id="ca223-138">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="ca223-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca223-139">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ca223-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca223-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca223-140">CommonParameters</span></span>
<span data-ttu-id="ca223-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ca223-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca223-142">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ca223-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca223-143">입력</span><span class="sxs-lookup"><span data-stu-id="ca223-143">INPUTS</span></span>

### <span data-ttu-id="ca223-144">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="ca223-144">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

### <span data-ttu-id="ca223-145">System.String</span><span class="sxs-lookup"><span data-stu-id="ca223-145">System.String</span></span>

### <span data-ttu-id="ca223-146">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="ca223-146">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="ca223-147">출력</span><span class="sxs-lookup"><span data-stu-id="ca223-147">OUTPUTS</span></span>

### <span data-ttu-id="ca223-148">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="ca223-148">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

## <span data-ttu-id="ca223-149">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ca223-149">NOTES</span></span>

## <span data-ttu-id="ca223-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ca223-150">RELATED LINKS</span></span>
