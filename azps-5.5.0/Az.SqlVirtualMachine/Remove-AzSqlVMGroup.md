---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/remove-azsqlvmgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzSqlVMGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzSqlVMGroup.md
ms.openlocfilehash: fec35992f96940dc69cdb6d1777d43ca151688bc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178284"
---
# <span data-ttu-id="b6e54-101">Remove-AzSqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="b6e54-101">Remove-AzSqlVMGroup</span></span>

## <span data-ttu-id="b6e54-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6e54-102">SYNOPSIS</span></span>
<span data-ttu-id="b6e54-103">SQL 가상 머신 그룹을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="b6e54-103">Deletes a sql virtual machine group.</span></span>

## <span data-ttu-id="b6e54-104">구문</span><span class="sxs-lookup"><span data-stu-id="b6e54-104">SYNTAX</span></span>

### <span data-ttu-id="b6e54-105">ParamaterList(기본값)</span><span class="sxs-lookup"><span data-stu-id="b6e54-105">ParamaterList (Default)</span></span>
```
Remove-AzSqlVMGroup [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b6e54-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="b6e54-106">InputObject</span></span>
```
Remove-AzSqlVMGroup [-InputObject] <AzureSqlVMGroupModel> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6e54-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="b6e54-107">ResourceId</span></span>
```
Remove-AzSqlVMGroup [-ResourceId] <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6e54-108">이름</span><span class="sxs-lookup"><span data-stu-id="b6e54-108">Name</span></span>
```
Remove-AzSqlVMGroup [-AsJob] [-PassThru] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6e54-109">설명</span><span class="sxs-lookup"><span data-stu-id="b6e54-109">DESCRIPTION</span></span>
<span data-ttu-id="b6e54-110">Remove-AzSqlVMGroup cmdlet은 SQL 가상 머신 그룹을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="b6e54-110">The Remove-AzSqlVMGroup cmdlet deletes a sql virtual machine group.</span></span>

## <span data-ttu-id="b6e54-111">예제</span><span class="sxs-lookup"><span data-stu-id="b6e54-111">EXAMPLES</span></span>

### <span data-ttu-id="b6e54-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="b6e54-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSqlVMGroup -ResourceGroupName "ResourceGroup01" -Name "test-group"
```

<span data-ttu-id="b6e54-113">ResourceGroup01에서 Azure SQL 가상 머신 그룹 "test-group"을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="b6e54-113">Deletes the Azure SQL virtual machine group "test-group" in the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="b6e54-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b6e54-114">PARAMETERS</span></span>

### <span data-ttu-id="b6e54-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b6e54-115">-AsJob</span></span>
<span data-ttu-id="b6e54-116">백그라운드에서 cmdlet을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="b6e54-116">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="b6e54-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6e54-117">-DefaultProfile</span></span>
<span data-ttu-id="b6e54-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b6e54-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6e54-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b6e54-119">-InputObject</span></span>
<span data-ttu-id="b6e54-120">SQL 가상 머신 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b6e54-120">SQL virtual machine object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel
Parameter Sets: InputObject
Aliases: SqlVMGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b6e54-121">-Name</span><span class="sxs-lookup"><span data-stu-id="b6e54-121">-Name</span></span>
<span data-ttu-id="b6e54-122">SQL 컴퓨터 그룹 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b6e54-122">SQL virtual machine group name.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: SqlVMGroupName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6e54-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b6e54-123">-PassThru</span></span>
<span data-ttu-id="b6e54-124">cmdlet 실행이 끝나면 삭제된 리소스를 출력할지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b6e54-124">Specifies whether to output the deleted resource at end of cmdlet execution.</span></span>

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

### <span data-ttu-id="b6e54-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6e54-125">-ResourceGroupName</span></span>
<span data-ttu-id="b6e54-126">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b6e54-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="b6e54-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b6e54-127">-ResourceId</span></span>
<span data-ttu-id="b6e54-128">SQL 컴퓨터 그룹 리소스 ID를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="b6e54-128">SQL virtual machine group resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases: SqlVMGroupId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6e54-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b6e54-129">-Confirm</span></span>
<span data-ttu-id="b6e54-130">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b6e54-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6e54-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6e54-131">-WhatIf</span></span>
<span data-ttu-id="b6e54-132">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="b6e54-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6e54-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b6e54-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6e54-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6e54-134">CommonParameters</span></span>
<span data-ttu-id="b6e54-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b6e54-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6e54-136">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b6e54-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6e54-137">입력</span><span class="sxs-lookup"><span data-stu-id="b6e54-137">INPUTS</span></span>

### <span data-ttu-id="b6e54-138">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="b6e54-138">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

### <span data-ttu-id="b6e54-139">System.String</span><span class="sxs-lookup"><span data-stu-id="b6e54-139">System.String</span></span>

## <span data-ttu-id="b6e54-140">출력</span><span class="sxs-lookup"><span data-stu-id="b6e54-140">OUTPUTS</span></span>

### <span data-ttu-id="b6e54-141">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="b6e54-141">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="b6e54-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b6e54-142">NOTES</span></span>

## <span data-ttu-id="b6e54-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b6e54-143">RELATED LINKS</span></span>
