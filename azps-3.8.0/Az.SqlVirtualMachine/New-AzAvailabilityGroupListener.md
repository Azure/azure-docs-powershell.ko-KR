---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/new-azavailabilitygrouplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzAvailabilityGroupListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzAvailabilityGroupListener.md
ms.openlocfilehash: af36c7cae36cb3d6bdb9bf2760b9a8299463e877
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93878702"
---
# <span data-ttu-id="40bfd-101">New-AzAvailabilityGroupListener</span><span class="sxs-lookup"><span data-stu-id="40bfd-101">New-AzAvailabilityGroupListener</span></span>

## <span data-ttu-id="40bfd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40bfd-102">SYNOPSIS</span></span>
<span data-ttu-id="40bfd-103">새 가용성 그룹 수신기를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="40bfd-103">Creates a new Availability Group Listener.</span></span>

## <span data-ttu-id="40bfd-104">구문과</span><span class="sxs-lookup"><span data-stu-id="40bfd-104">SYNTAX</span></span>

### <span data-ttu-id="40bfd-105">Name (기본값)</span><span class="sxs-lookup"><span data-stu-id="40bfd-105">Name (Default)</span></span>
```
New-AzAvailabilityGroupListener -AvailabilityGroupName <String> [-Port <Int32>]
 -LoadBalancerResourceId <String> [-IpAddress <String>] [-SubnetId <String>] -ProbePort <Int32>
 [-PublicIpAddressResourceId <String>] [-AsJob] -SqlVirtualMachineId <String[]> [-ResourceGroupName] <String>
 [-SqlVMGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="40bfd-106">SqlVmGroupObject</span><span class="sxs-lookup"><span data-stu-id="40bfd-106">SqlVmGroupObject</span></span>
```
New-AzAvailabilityGroupListener -AvailabilityGroupName <String> [-Port <Int32>]
 -LoadBalancerResourceId <String> [-IpAddress <String>] [-SubnetId <String>] -ProbePort <Int32>
 [-PublicIpAddressResourceId <String>] [-AsJob] -SqlVirtualMachineId <String[]>
 [-SqlVMGroupObject] <AzureSqlVMGroupModel> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40bfd-107">설명은</span><span class="sxs-lookup"><span data-stu-id="40bfd-107">DESCRIPTION</span></span>
<span data-ttu-id="40bfd-108">New-AzAvailabilityGroupListener cmdlet은 새 가용성 그룹 수신기를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="40bfd-108">The New-AzAvailabilityGroupListener cmdlet creates a new Availability Group Listener.</span></span>

## <span data-ttu-id="40bfd-109">예제의</span><span class="sxs-lookup"><span data-stu-id="40bfd-109">EXAMPLES</span></span>

### <span data-ttu-id="40bfd-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="40bfd-110">Example 1</span></span>
```powershell
PS C:\> New-AzAvailabilityGroupListener -AvailabilityGroupName AvailabilityGroup01 -LoadBalancerResourceId $LoadBalanceResourceId -SubnetId $SubnetId -ProbePort 59999 -SqlVirtualMachineId $VmResourceId1,$VmResourceId2 -Name AgListener01  -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01 -IpAddress 10.0.0.3
```

<span data-ttu-id="40bfd-111">Name ResourceGroupName GroupName AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="40bfd-111">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="40bfd-112">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="40bfd-112">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

<span data-ttu-id="40bfd-113">SQL 가상 컴퓨터 그룹 SqlVmGroup01에서 가용성 그룹 AvailabilityGroup01에 대 한 새 가용성 그룹 수신기 AgListener01을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="40bfd-113">Creates a new Availability Group Listener AgListener01 for the Availability Group AvailabilityGroup01 in SQL Virtual Machine Group SqlVmGroup01.</span></span>

## <span data-ttu-id="40bfd-114">변수</span><span class="sxs-lookup"><span data-stu-id="40bfd-114">PARAMETERS</span></span>

### <span data-ttu-id="40bfd-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="40bfd-115">-AsJob</span></span>
<span data-ttu-id="40bfd-116">백그라운드에서 cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="40bfd-116">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="40bfd-117">-AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="40bfd-117">-AvailabilityGroupName</span></span>
<span data-ttu-id="40bfd-118">가용성 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="40bfd-118">Availability Group name.</span></span>

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

### <span data-ttu-id="40bfd-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40bfd-119">-DefaultProfile</span></span>
<span data-ttu-id="40bfd-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="40bfd-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40bfd-121">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="40bfd-121">-IpAddress</span></span>
<span data-ttu-id="40bfd-122">개인 Ip 주소</span><span class="sxs-lookup"><span data-stu-id="40bfd-122">Private Ip Address</span></span>

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

### <span data-ttu-id="40bfd-123">-LoadBalancerResourceId</span><span class="sxs-lookup"><span data-stu-id="40bfd-123">-LoadBalancerResourceId</span></span>
<span data-ttu-id="40bfd-124">부하 분산 장치 Id</span><span class="sxs-lookup"><span data-stu-id="40bfd-124">Load Balancer Id</span></span>

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

### <span data-ttu-id="40bfd-125">-이름</span><span class="sxs-lookup"><span data-stu-id="40bfd-125">-Name</span></span>
<span data-ttu-id="40bfd-126">가용성 그룹 수신기 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="40bfd-126">Availability Group Listener name.</span></span>

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

### <span data-ttu-id="40bfd-127">-포트</span><span class="sxs-lookup"><span data-stu-id="40bfd-127">-Port</span></span>
<span data-ttu-id="40bfd-128">AG 수신기의 포트 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="40bfd-128">Port number of AG Listener.</span></span> <span data-ttu-id="40bfd-129">기본값은 1433입니다.</span><span class="sxs-lookup"><span data-stu-id="40bfd-129">Default Value is 1433.</span></span>

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

### <span data-ttu-id="40bfd-130">-ProbePort</span><span class="sxs-lookup"><span data-stu-id="40bfd-130">-ProbePort</span></span>
<span data-ttu-id="40bfd-131">프로브 포트</span><span class="sxs-lookup"><span data-stu-id="40bfd-131">Probe Port</span></span>

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

### <span data-ttu-id="40bfd-132">-PublicIpAddressResourceId</span><span class="sxs-lookup"><span data-stu-id="40bfd-132">-PublicIpAddressResourceId</span></span>
<span data-ttu-id="40bfd-133">공용 Ip 주소 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="40bfd-133">Public Ip Address Resource Id</span></span>

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

### <span data-ttu-id="40bfd-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40bfd-134">-ResourceGroupName</span></span>
<span data-ttu-id="40bfd-135">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="40bfd-135">The name of the resource group.</span></span>

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

### <span data-ttu-id="40bfd-136">-SqlVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="40bfd-136">-SqlVirtualMachineId</span></span>
<span data-ttu-id="40bfd-137">Sql VM 리소스 Id 목록</span><span class="sxs-lookup"><span data-stu-id="40bfd-137">List of Sql VM Resource IDs</span></span>

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

### <span data-ttu-id="40bfd-138">-SqlVMGroupName</span><span class="sxs-lookup"><span data-stu-id="40bfd-138">-SqlVMGroupName</span></span>
<span data-ttu-id="40bfd-139">SQL 가상 컴퓨터 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="40bfd-139">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="40bfd-140">-SqlVMGroupObject</span><span class="sxs-lookup"><span data-stu-id="40bfd-140">-SqlVMGroupObject</span></span>
<span data-ttu-id="40bfd-141">SQL 가상 컴퓨터 그룹 개체</span><span class="sxs-lookup"><span data-stu-id="40bfd-141">SQL virtual machine Group object.</span></span>

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

### <span data-ttu-id="40bfd-142">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="40bfd-142">-SubnetId</span></span>
<span data-ttu-id="40bfd-143">서브넷 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="40bfd-143">Subnet Resource Id</span></span>

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

### <span data-ttu-id="40bfd-144">-확인</span><span class="sxs-lookup"><span data-stu-id="40bfd-144">-Confirm</span></span>
<span data-ttu-id="40bfd-145">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="40bfd-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40bfd-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40bfd-146">-WhatIf</span></span>
<span data-ttu-id="40bfd-147">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="40bfd-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40bfd-148">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="40bfd-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40bfd-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40bfd-149">CommonParameters</span></span>
<span data-ttu-id="40bfd-150">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="40bfd-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40bfd-151">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="40bfd-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40bfd-152">입력</span><span class="sxs-lookup"><span data-stu-id="40bfd-152">INPUTS</span></span>

### <span data-ttu-id="40bfd-153">SqlVirtualMachine를 SqlVirtualMachine 합니다. AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="40bfd-153">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="40bfd-154">출력</span><span class="sxs-lookup"><span data-stu-id="40bfd-154">OUTPUTS</span></span>

### <span data-ttu-id="40bfd-155">SqlVirtualMachine를 SqlVirtualMachine 합니다. AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="40bfd-155">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

## <span data-ttu-id="40bfd-156">상속자</span><span class="sxs-lookup"><span data-stu-id="40bfd-156">NOTES</span></span>

## <span data-ttu-id="40bfd-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="40bfd-157">RELATED LINKS</span></span>
