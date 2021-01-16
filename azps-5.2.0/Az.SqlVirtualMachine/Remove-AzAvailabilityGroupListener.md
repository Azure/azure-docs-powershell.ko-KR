---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/remove-azavailabilitygrouplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzAvailabilityGroupListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzAvailabilityGroupListener.md
ms.openlocfilehash: d147fcd53b27031949bf51a33a59a9db86687d57
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98334425"
---
# <span data-ttu-id="7dbee-101">Remove-AzAvailabilityGroupListener</span><span class="sxs-lookup"><span data-stu-id="7dbee-101">Remove-AzAvailabilityGroupListener</span></span>

## <span data-ttu-id="7dbee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7dbee-102">SYNOPSIS</span></span>
<span data-ttu-id="7dbee-103">가용성 그룹 수신기 삭제</span><span class="sxs-lookup"><span data-stu-id="7dbee-103">Deletes an Availability Group Listener.</span></span>

## <span data-ttu-id="7dbee-104">구문</span><span class="sxs-lookup"><span data-stu-id="7dbee-104">SYNTAX</span></span>

### <span data-ttu-id="7dbee-105">이름(기본값)</span><span class="sxs-lookup"><span data-stu-id="7dbee-105">Name (Default)</span></span>
```
Remove-AzAvailabilityGroupListener [-AsJob] [-PassThru] [-ResourceGroupName] <String>
 [-SqlVMGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7dbee-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="7dbee-106">InputObject</span></span>
```
Remove-AzAvailabilityGroupListener [-InputObject] <AzureAvailabilityGroupListenerModel> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7dbee-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="7dbee-107">ResourceId</span></span>
```
Remove-AzAvailabilityGroupListener [-ResourceId] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7dbee-108">SqlVmGroupObject</span><span class="sxs-lookup"><span data-stu-id="7dbee-108">SqlVmGroupObject</span></span>
```
Remove-AzAvailabilityGroupListener [-AsJob] [-PassThru] [-SqlVMGroupObject] <AzureSqlVMGroupModel>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7dbee-109">설명</span><span class="sxs-lookup"><span data-stu-id="7dbee-109">DESCRIPTION</span></span>
<span data-ttu-id="7dbee-110">Remove-AzAvailabilityGroupListener cmdlet은 가용성 그룹 수신기 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="7dbee-110">The Remove-AzAvailabilityGroupListener cmdlet deletes an Availability Group Listener.</span></span>

## <span data-ttu-id="7dbee-111">예제</span><span class="sxs-lookup"><span data-stu-id="7dbee-111">EXAMPLES</span></span>

### <span data-ttu-id="7dbee-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="7dbee-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzAvailabilityGroupListener -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01 -Name AgListener01
```

<span data-ttu-id="7dbee-113">ResourceGroupName GroupName AvailabilityGroupName 이름 지정</span><span class="sxs-lookup"><span data-stu-id="7dbee-113">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="7dbee-114">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="7dbee-114">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

<span data-ttu-id="7dbee-115">가용성 그룹 AvailabilityGroup01에서 가용성 그룹 수신기 AgListener01을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="7dbee-115">Deletes the Availability Group Listener AgListener01 in the Availability Group AvailabilityGroup01.</span></span>

## <span data-ttu-id="7dbee-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7dbee-116">PARAMETERS</span></span>

### <span data-ttu-id="7dbee-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7dbee-117">-AsJob</span></span>
<span data-ttu-id="7dbee-118">백그라운드에서 cmdlet을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="7dbee-118">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="7dbee-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7dbee-119">-DefaultProfile</span></span>
<span data-ttu-id="7dbee-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7dbee-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7dbee-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7dbee-121">-InputObject</span></span>
<span data-ttu-id="7dbee-122">가용성 그룹 수신기 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="7dbee-122">Availability Group Listener object.</span></span>

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

### <span data-ttu-id="7dbee-123">-Name</span><span class="sxs-lookup"><span data-stu-id="7dbee-123">-Name</span></span>
<span data-ttu-id="7dbee-124">가용성 그룹 수신기 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7dbee-124">Availability Group Listener name.</span></span>

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

### <span data-ttu-id="7dbee-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7dbee-125">-PassThru</span></span>
<span data-ttu-id="7dbee-126">cmdlet 실행이 끝나면 삭제된 리소스를 출력할지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7dbee-126">Specifies whether to output the deleted resource at end of cmdlet execution.</span></span>

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

### <span data-ttu-id="7dbee-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7dbee-127">-ResourceGroupName</span></span>
<span data-ttu-id="7dbee-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7dbee-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="7dbee-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7dbee-129">-ResourceId</span></span>
<span data-ttu-id="7dbee-130">가용성 그룹 수신기 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="7dbee-130">Availability Group Listener Resource Id</span></span>

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

### <span data-ttu-id="7dbee-131">-SqlVMGroupName</span><span class="sxs-lookup"><span data-stu-id="7dbee-131">-SqlVMGroupName</span></span>
<span data-ttu-id="7dbee-132">SQL 컴퓨터 그룹 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7dbee-132">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="7dbee-133">-SqlVMGroupObject</span><span class="sxs-lookup"><span data-stu-id="7dbee-133">-SqlVMGroupObject</span></span>
<span data-ttu-id="7dbee-134">SQL 그룹 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="7dbee-134">SQL virtual machine Group object.</span></span>

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

### <span data-ttu-id="7dbee-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7dbee-135">-Confirm</span></span>
<span data-ttu-id="7dbee-136">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7dbee-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7dbee-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7dbee-137">-WhatIf</span></span>
<span data-ttu-id="7dbee-138">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="7dbee-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7dbee-139">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7dbee-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7dbee-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7dbee-140">CommonParameters</span></span>
<span data-ttu-id="7dbee-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7dbee-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7dbee-142">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7dbee-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7dbee-143">입력</span><span class="sxs-lookup"><span data-stu-id="7dbee-143">INPUTS</span></span>

### <span data-ttu-id="7dbee-144">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="7dbee-144">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

### <span data-ttu-id="7dbee-145">System.String</span><span class="sxs-lookup"><span data-stu-id="7dbee-145">System.String</span></span>

### <span data-ttu-id="7dbee-146">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="7dbee-146">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="7dbee-147">출력</span><span class="sxs-lookup"><span data-stu-id="7dbee-147">OUTPUTS</span></span>

### <span data-ttu-id="7dbee-148">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="7dbee-148">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

## <span data-ttu-id="7dbee-149">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7dbee-149">NOTES</span></span>

## <span data-ttu-id="7dbee-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7dbee-150">RELATED LINKS</span></span>
