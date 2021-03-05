---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/powershell/module/az.sqlvirtualmachine/new-azavailabilitygrouplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzAvailabilityGroupListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzAvailabilityGroupListener.md
ms.openlocfilehash: f187a2704ed1f23d6cc5ac7dded1c8d9cd8ae954
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008331"
---
# <span data-ttu-id="278bd-101">New-AzAvailabilityGroupListener</span><span class="sxs-lookup"><span data-stu-id="278bd-101">New-AzAvailabilityGroupListener</span></span>

## <span data-ttu-id="278bd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="278bd-102">SYNOPSIS</span></span>
<span data-ttu-id="278bd-103">새 가용성 그룹 수신기를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="278bd-103">Creates a new Availability Group Listener.</span></span>

## <span data-ttu-id="278bd-104">구문</span><span class="sxs-lookup"><span data-stu-id="278bd-104">SYNTAX</span></span>

### <span data-ttu-id="278bd-105">이름(기본값)</span><span class="sxs-lookup"><span data-stu-id="278bd-105">Name (Default)</span></span>
```
New-AzAvailabilityGroupListener -AvailabilityGroupName <String> [-Port <Int32>]
 -LoadBalancerResourceId <String> [-IpAddress <String>] [-SubnetId <String>] -ProbePort <Int32>
 [-PublicIpAddressResourceId <String>] [-AsJob] -SqlVirtualMachineId <String[]> [-ResourceGroupName] <String>
 [-SqlVMGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="278bd-106">SqlVmGroupObject</span><span class="sxs-lookup"><span data-stu-id="278bd-106">SqlVmGroupObject</span></span>
```
New-AzAvailabilityGroupListener -AvailabilityGroupName <String> [-Port <Int32>]
 -LoadBalancerResourceId <String> [-IpAddress <String>] [-SubnetId <String>] -ProbePort <Int32>
 [-PublicIpAddressResourceId <String>] [-AsJob] -SqlVirtualMachineId <String[]>
 [-SqlVMGroupObject] <AzureSqlVMGroupModel> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="278bd-107">설명</span><span class="sxs-lookup"><span data-stu-id="278bd-107">DESCRIPTION</span></span>
<span data-ttu-id="278bd-108">New-AzAvailabilityGroupListener cmdlet은 새 가용성 그룹 수신기를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="278bd-108">The New-AzAvailabilityGroupListener cmdlet creates a new Availability Group Listener.</span></span>

## <span data-ttu-id="278bd-109">예제</span><span class="sxs-lookup"><span data-stu-id="278bd-109">EXAMPLES</span></span>

### <span data-ttu-id="278bd-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="278bd-110">Example 1</span></span>
```powershell
PS C:\> New-AzAvailabilityGroupListener -AvailabilityGroupName AvailabilityGroup01 -LoadBalancerResourceId $LoadBalanceResourceId -SubnetId $SubnetId -ProbePort 59999 -SqlVirtualMachineId $VmResourceId1,$VmResourceId2 -Name AgListener01  -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01 -IpAddress 10.0.0.3
```

<span data-ttu-id="278bd-111">Name ResourceGroupName GroupName AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="278bd-111">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="278bd-112">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="278bd-112">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

<span data-ttu-id="278bd-113">Virtual Machine Group SqlVmGroup01에서 가용성 그룹 가용성Group01에 대한 새 가용성 그룹 수신기 AgListener01을 SQL 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="278bd-113">Creates a new Availability Group Listener AgListener01 for the Availability Group AvailabilityGroup01 in SQL Virtual Machine Group SqlVmGroup01.</span></span>

## <span data-ttu-id="278bd-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="278bd-114">PARAMETERS</span></span>

### <span data-ttu-id="278bd-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="278bd-115">-AsJob</span></span>
<span data-ttu-id="278bd-116">백그라운드에서 cmdlet을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="278bd-116">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="278bd-117">-AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="278bd-117">-AvailabilityGroupName</span></span>
<span data-ttu-id="278bd-118">가용성 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="278bd-118">Availability Group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="278bd-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="278bd-119">-DefaultProfile</span></span>
<span data-ttu-id="278bd-120">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="278bd-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="278bd-121">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="278bd-121">-IpAddress</span></span>
<span data-ttu-id="278bd-122">개인 IP 주소</span><span class="sxs-lookup"><span data-stu-id="278bd-122">Private Ip Address</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="278bd-123">-LoadBalancerResourceId</span><span class="sxs-lookup"><span data-stu-id="278bd-123">-LoadBalancerResourceId</span></span>
<span data-ttu-id="278bd-124">Load Balancer Id</span><span class="sxs-lookup"><span data-stu-id="278bd-124">Load Balancer Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="278bd-125">-Name</span><span class="sxs-lookup"><span data-stu-id="278bd-125">-Name</span></span>
<span data-ttu-id="278bd-126">가용성 그룹 수신기 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="278bd-126">Availability Group Listener name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="278bd-127">-Port</span><span class="sxs-lookup"><span data-stu-id="278bd-127">-Port</span></span>
<span data-ttu-id="278bd-128">AG 수신기의 포트 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="278bd-128">Port number of AG Listener.</span></span> <span data-ttu-id="278bd-129">기본값은 1433입니다.</span><span class="sxs-lookup"><span data-stu-id="278bd-129">Default Value is 1433.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="278bd-130">-ProbePort</span><span class="sxs-lookup"><span data-stu-id="278bd-130">-ProbePort</span></span>
<span data-ttu-id="278bd-131">프로브 포트</span><span class="sxs-lookup"><span data-stu-id="278bd-131">Probe Port</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="278bd-132">-PublicIpAddressResourceId</span><span class="sxs-lookup"><span data-stu-id="278bd-132">-PublicIpAddressResourceId</span></span>
<span data-ttu-id="278bd-133">공용 IP 주소 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="278bd-133">Public Ip Address Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="278bd-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="278bd-134">-ResourceGroupName</span></span>
<span data-ttu-id="278bd-135">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="278bd-135">The name of the resource group.</span></span>

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

### <span data-ttu-id="278bd-136">-SqlVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="278bd-136">-SqlVirtualMachineId</span></span>
<span data-ttu-id="278bd-137">Sql VM 리소스 아이디 목록</span><span class="sxs-lookup"><span data-stu-id="278bd-137">List of Sql VM Resource IDs</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="278bd-138">-SqlVMGroupName</span><span class="sxs-lookup"><span data-stu-id="278bd-138">-SqlVMGroupName</span></span>
<span data-ttu-id="278bd-139">SQL 컴퓨터 그룹 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="278bd-139">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="278bd-140">-SqlVMGroupObject</span><span class="sxs-lookup"><span data-stu-id="278bd-140">-SqlVMGroupObject</span></span>
<span data-ttu-id="278bd-141">SQL 가상 머신 그룹 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="278bd-141">SQL virtual machine Group object.</span></span>

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

### <span data-ttu-id="278bd-142">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="278bd-142">-SubnetId</span></span>
<span data-ttu-id="278bd-143">서브넷 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="278bd-143">Subnet Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="278bd-144">-확인</span><span class="sxs-lookup"><span data-stu-id="278bd-144">-Confirm</span></span>
<span data-ttu-id="278bd-145">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="278bd-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="278bd-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="278bd-146">-WhatIf</span></span>
<span data-ttu-id="278bd-147">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="278bd-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="278bd-148">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="278bd-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="278bd-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="278bd-149">CommonParameters</span></span>
<span data-ttu-id="278bd-150">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="278bd-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="278bd-151">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="278bd-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="278bd-152">입력</span><span class="sxs-lookup"><span data-stu-id="278bd-152">INPUTS</span></span>

### <span data-ttu-id="278bd-153">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="278bd-153">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="278bd-154">출력</span><span class="sxs-lookup"><span data-stu-id="278bd-154">OUTPUTS</span></span>

### <span data-ttu-id="278bd-155">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="278bd-155">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

## <span data-ttu-id="278bd-156">참고 사항</span><span class="sxs-lookup"><span data-stu-id="278bd-156">NOTES</span></span>

## <span data-ttu-id="278bd-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="278bd-157">RELATED LINKS</span></span>
