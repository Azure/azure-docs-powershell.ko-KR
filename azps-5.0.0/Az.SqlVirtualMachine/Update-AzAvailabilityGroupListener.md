---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/update-azavailabilitygrouplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzAvailabilityGroupListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzAvailabilityGroupListener.md
ms.openlocfilehash: 6c44a2fc7193acaadcf24ac311b5eb4b4a00b7d0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216519"
---
# <span data-ttu-id="09db5-101">Update-AzAvailabilityGroupListener</span><span class="sxs-lookup"><span data-stu-id="09db5-101">Update-AzAvailabilityGroupListener</span></span>

## <span data-ttu-id="09db5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="09db5-102">SYNOPSIS</span></span>
<span data-ttu-id="09db5-103">가용성 그룹 수신기를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="09db5-103">Updates the Availability Group Listener.</span></span>

## <span data-ttu-id="09db5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="09db5-104">SYNTAX</span></span>

### <span data-ttu-id="09db5-105">Name (기본값)</span><span class="sxs-lookup"><span data-stu-id="09db5-105">Name (Default)</span></span>
```
Update-AzAvailabilityGroupListener [-SqlVirtualMachineId <String[]>] [-AsJob] [-ResourceGroupName] <String>
 [-SqlVMGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="09db5-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="09db5-106">InputObject</span></span>
```
Update-AzAvailabilityGroupListener [-InputObject] <AzureAvailabilityGroupListenerModel>
 [-SqlVirtualMachineId <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="09db5-107">리소스</span><span class="sxs-lookup"><span data-stu-id="09db5-107">ResourceId</span></span>
```
Update-AzAvailabilityGroupListener [-ResourceId] <String> [-SqlVirtualMachineId <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09db5-108">SqlVmGroupObject</span><span class="sxs-lookup"><span data-stu-id="09db5-108">SqlVmGroupObject</span></span>
```
Update-AzAvailabilityGroupListener [-SqlVirtualMachineId <String[]>] [-AsJob]
 [-SqlVMGroupObject] <AzureSqlVMGroupModel> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09db5-109">설명은</span><span class="sxs-lookup"><span data-stu-id="09db5-109">DESCRIPTION</span></span>
<span data-ttu-id="09db5-110">Update-AzAvailabilityGroupListener cmdlet은 가용성 그룹 수신기를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="09db5-110">The Update-AzAvailabilityGroupListener cmdlet updates an Availability Group Listener.</span></span>

## <span data-ttu-id="09db5-111">예제의</span><span class="sxs-lookup"><span data-stu-id="09db5-111">EXAMPLES</span></span>

### <span data-ttu-id="09db5-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="09db5-112">Example 1</span></span>
```powershell
PS C:\> Update-AzAvailabilityGroupListener -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01 -Name AgListener01 -SqlVirtualMachineId $VmResourceId01,$VmResourceId02
```

<span data-ttu-id="09db5-113">Name ResourceGroupName GroupName AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="09db5-113">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="09db5-114">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="09db5-114">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

<span data-ttu-id="09db5-115">가용성 그룹 수신기에 대 한 SQL 가상 컴퓨터 목록을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="09db5-115">Updates the list SQL Virtual Machines for the Availability Group Listener.</span></span>

## <span data-ttu-id="09db5-116">변수</span><span class="sxs-lookup"><span data-stu-id="09db5-116">PARAMETERS</span></span>

### <span data-ttu-id="09db5-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="09db5-117">-AsJob</span></span>
<span data-ttu-id="09db5-118">백그라운드에서 cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="09db5-118">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="09db5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09db5-119">-DefaultProfile</span></span>
<span data-ttu-id="09db5-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="09db5-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09db5-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="09db5-121">-InputObject</span></span>
<span data-ttu-id="09db5-122">가용성 그룹 수신기 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="09db5-122">Availability Group Listener object.</span></span>

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

### <span data-ttu-id="09db5-123">-이름</span><span class="sxs-lookup"><span data-stu-id="09db5-123">-Name</span></span>
<span data-ttu-id="09db5-124">가용성 그룹 수신기 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="09db5-124">Availability Group Listener name.</span></span>

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

### <span data-ttu-id="09db5-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09db5-125">-ResourceGroupName</span></span>
<span data-ttu-id="09db5-126">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="09db5-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="09db5-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="09db5-127">-ResourceId</span></span>
<span data-ttu-id="09db5-128">가용성 그룹 수신기 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="09db5-128">Availability Group Listener Resource Id</span></span>

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

### <span data-ttu-id="09db5-129">-SqlVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="09db5-129">-SqlVirtualMachineId</span></span>
<span data-ttu-id="09db5-130">Sql VM 리소스 Id 목록</span><span class="sxs-lookup"><span data-stu-id="09db5-130">List of Sql VM Resource IDs</span></span>

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

### <span data-ttu-id="09db5-131">-SqlVMGroupName</span><span class="sxs-lookup"><span data-stu-id="09db5-131">-SqlVMGroupName</span></span>
<span data-ttu-id="09db5-132">SQL 가상 컴퓨터 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="09db5-132">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="09db5-133">-SqlVMGroupObject</span><span class="sxs-lookup"><span data-stu-id="09db5-133">-SqlVMGroupObject</span></span>
<span data-ttu-id="09db5-134">SQL 가상 컴퓨터 그룹 개체</span><span class="sxs-lookup"><span data-stu-id="09db5-134">SQL virtual machine Group object.</span></span>

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

### <span data-ttu-id="09db5-135">-확인</span><span class="sxs-lookup"><span data-stu-id="09db5-135">-Confirm</span></span>
<span data-ttu-id="09db5-136">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="09db5-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09db5-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09db5-137">-WhatIf</span></span>
<span data-ttu-id="09db5-138">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="09db5-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09db5-139">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="09db5-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09db5-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09db5-140">CommonParameters</span></span>
<span data-ttu-id="09db5-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="09db5-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09db5-142">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="09db5-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09db5-143">입력</span><span class="sxs-lookup"><span data-stu-id="09db5-143">INPUTS</span></span>

### <span data-ttu-id="09db5-144">SqlVirtualMachine를 SqlVirtualMachine 합니다. AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="09db5-144">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

### <span data-ttu-id="09db5-145">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="09db5-145">System.String</span></span>

### <span data-ttu-id="09db5-146">SqlVirtualMachine를 SqlVirtualMachine 합니다. AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="09db5-146">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="09db5-147">출력</span><span class="sxs-lookup"><span data-stu-id="09db5-147">OUTPUTS</span></span>

### <span data-ttu-id="09db5-148">SqlVirtualMachine를 SqlVirtualMachine 합니다. AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="09db5-148">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

## <span data-ttu-id="09db5-149">상속자</span><span class="sxs-lookup"><span data-stu-id="09db5-149">NOTES</span></span>

## <span data-ttu-id="09db5-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="09db5-150">RELATED LINKS</span></span>
