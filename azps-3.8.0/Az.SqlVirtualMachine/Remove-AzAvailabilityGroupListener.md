---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/remove-azavailabilitygrouplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzAvailabilityGroupListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzAvailabilityGroupListener.md
ms.openlocfilehash: d147fcd53b27031949bf51a33a59a9db86687d57
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93878626"
---
# <span data-ttu-id="35418-101">Remove-AzAvailabilityGroupListener</span><span class="sxs-lookup"><span data-stu-id="35418-101">Remove-AzAvailabilityGroupListener</span></span>

## <span data-ttu-id="35418-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35418-102">SYNOPSIS</span></span>
<span data-ttu-id="35418-103">가용성 그룹 수신기를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="35418-103">Deletes an Availability Group Listener.</span></span>

## <span data-ttu-id="35418-104">구문과</span><span class="sxs-lookup"><span data-stu-id="35418-104">SYNTAX</span></span>

### <span data-ttu-id="35418-105">Name (기본값)</span><span class="sxs-lookup"><span data-stu-id="35418-105">Name (Default)</span></span>
```
Remove-AzAvailabilityGroupListener [-AsJob] [-PassThru] [-ResourceGroupName] <String>
 [-SqlVMGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="35418-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="35418-106">InputObject</span></span>
```
Remove-AzAvailabilityGroupListener [-InputObject] <AzureAvailabilityGroupListenerModel> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35418-107">리소스</span><span class="sxs-lookup"><span data-stu-id="35418-107">ResourceId</span></span>
```
Remove-AzAvailabilityGroupListener [-ResourceId] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35418-108">SqlVmGroupObject</span><span class="sxs-lookup"><span data-stu-id="35418-108">SqlVmGroupObject</span></span>
```
Remove-AzAvailabilityGroupListener [-AsJob] [-PassThru] [-SqlVMGroupObject] <AzureSqlVMGroupModel>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35418-109">설명은</span><span class="sxs-lookup"><span data-stu-id="35418-109">DESCRIPTION</span></span>
<span data-ttu-id="35418-110">Remove-AzAvailabilityGroupListener cmdlet은 가용성 그룹 수신기를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="35418-110">The Remove-AzAvailabilityGroupListener cmdlet deletes an Availability Group Listener.</span></span>

## <span data-ttu-id="35418-111">예제의</span><span class="sxs-lookup"><span data-stu-id="35418-111">EXAMPLES</span></span>

### <span data-ttu-id="35418-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="35418-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzAvailabilityGroupListener -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01 -Name AgListener01
```

<span data-ttu-id="35418-113">Name ResourceGroupName GroupName AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="35418-113">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="35418-114">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="35418-114">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

<span data-ttu-id="35418-115">가용성 그룹 AvailabilityGroup01에서 가용성 그룹 수신기 AgListener01를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="35418-115">Deletes the Availability Group Listener AgListener01 in the Availability Group AvailabilityGroup01.</span></span>

## <span data-ttu-id="35418-116">변수</span><span class="sxs-lookup"><span data-stu-id="35418-116">PARAMETERS</span></span>

### <span data-ttu-id="35418-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="35418-117">-AsJob</span></span>
<span data-ttu-id="35418-118">백그라운드에서 cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="35418-118">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="35418-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35418-119">-DefaultProfile</span></span>
<span data-ttu-id="35418-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="35418-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35418-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="35418-121">-InputObject</span></span>
<span data-ttu-id="35418-122">가용성 그룹 수신기 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="35418-122">Availability Group Listener object.</span></span>

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

### <span data-ttu-id="35418-123">-이름</span><span class="sxs-lookup"><span data-stu-id="35418-123">-Name</span></span>
<span data-ttu-id="35418-124">가용성 그룹 수신기 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="35418-124">Availability Group Listener name.</span></span>

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

### <span data-ttu-id="35418-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="35418-125">-PassThru</span></span>
<span data-ttu-id="35418-126">Cmdlet 실행이 종료 될 때 삭제 된 리소스를 출력할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="35418-126">Specifies whether to output the deleted resource at end of cmdlet execution.</span></span>

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

### <span data-ttu-id="35418-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35418-127">-ResourceGroupName</span></span>
<span data-ttu-id="35418-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="35418-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="35418-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="35418-129">-ResourceId</span></span>
<span data-ttu-id="35418-130">가용성 그룹 수신기 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="35418-130">Availability Group Listener Resource Id</span></span>

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

### <span data-ttu-id="35418-131">-SqlVMGroupName</span><span class="sxs-lookup"><span data-stu-id="35418-131">-SqlVMGroupName</span></span>
<span data-ttu-id="35418-132">SQL 가상 컴퓨터 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="35418-132">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="35418-133">-SqlVMGroupObject</span><span class="sxs-lookup"><span data-stu-id="35418-133">-SqlVMGroupObject</span></span>
<span data-ttu-id="35418-134">SQL 가상 컴퓨터 그룹 개체</span><span class="sxs-lookup"><span data-stu-id="35418-134">SQL virtual machine Group object.</span></span>

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

### <span data-ttu-id="35418-135">-확인</span><span class="sxs-lookup"><span data-stu-id="35418-135">-Confirm</span></span>
<span data-ttu-id="35418-136">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="35418-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35418-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35418-137">-WhatIf</span></span>
<span data-ttu-id="35418-138">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="35418-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35418-139">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="35418-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35418-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35418-140">CommonParameters</span></span>
<span data-ttu-id="35418-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="35418-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35418-142">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="35418-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35418-143">입력</span><span class="sxs-lookup"><span data-stu-id="35418-143">INPUTS</span></span>

### <span data-ttu-id="35418-144">SqlVirtualMachine를 SqlVirtualMachine 합니다. AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="35418-144">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

### <span data-ttu-id="35418-145">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="35418-145">System.String</span></span>

### <span data-ttu-id="35418-146">SqlVirtualMachine를 SqlVirtualMachine 합니다. AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="35418-146">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="35418-147">출력</span><span class="sxs-lookup"><span data-stu-id="35418-147">OUTPUTS</span></span>

### <span data-ttu-id="35418-148">SqlVirtualMachine를 SqlVirtualMachine 합니다. AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="35418-148">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

## <span data-ttu-id="35418-149">상속자</span><span class="sxs-lookup"><span data-stu-id="35418-149">NOTES</span></span>

## <span data-ttu-id="35418-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="35418-150">RELATED LINKS</span></span>
