---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/remove-azsqlvmgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzSqlVMGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzSqlVMGroup.md
ms.openlocfilehash: fec35992f96940dc69cdb6d1777d43ca151688bc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215642"
---
# <span data-ttu-id="0713a-101">Remove-AzSqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="0713a-101">Remove-AzSqlVMGroup</span></span>

## <span data-ttu-id="0713a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0713a-102">SYNOPSIS</span></span>
<span data-ttu-id="0713a-103">Sql 가상 컴퓨터 그룹을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="0713a-103">Deletes a sql virtual machine group.</span></span>

## <span data-ttu-id="0713a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0713a-104">SYNTAX</span></span>

### <span data-ttu-id="0713a-105">ParamaterList (기본값)</span><span class="sxs-lookup"><span data-stu-id="0713a-105">ParamaterList (Default)</span></span>
```
Remove-AzSqlVMGroup [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0713a-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="0713a-106">InputObject</span></span>
```
Remove-AzSqlVMGroup [-InputObject] <AzureSqlVMGroupModel> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0713a-107">리소스</span><span class="sxs-lookup"><span data-stu-id="0713a-107">ResourceId</span></span>
```
Remove-AzSqlVMGroup [-ResourceId] <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0713a-108">성을</span><span class="sxs-lookup"><span data-stu-id="0713a-108">Name</span></span>
```
Remove-AzSqlVMGroup [-AsJob] [-PassThru] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0713a-109">설명은</span><span class="sxs-lookup"><span data-stu-id="0713a-109">DESCRIPTION</span></span>
<span data-ttu-id="0713a-110">Remove-AzSqlVMGroup cmdlet은 sql 가상 컴퓨터 그룹을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="0713a-110">The Remove-AzSqlVMGroup cmdlet deletes a sql virtual machine group.</span></span>

## <span data-ttu-id="0713a-111">예제의</span><span class="sxs-lookup"><span data-stu-id="0713a-111">EXAMPLES</span></span>

### <span data-ttu-id="0713a-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="0713a-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSqlVMGroup -ResourceGroupName "ResourceGroup01" -Name "test-group"
```

<span data-ttu-id="0713a-113">리소스 그룹 ResourceGroup01에서 Azure SQL 가상 컴퓨터 그룹 "test-group"을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="0713a-113">Deletes the Azure SQL virtual machine group "test-group" in the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="0713a-114">변수</span><span class="sxs-lookup"><span data-stu-id="0713a-114">PARAMETERS</span></span>

### <span data-ttu-id="0713a-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0713a-115">-AsJob</span></span>
<span data-ttu-id="0713a-116">백그라운드에서 cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="0713a-116">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="0713a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0713a-117">-DefaultProfile</span></span>
<span data-ttu-id="0713a-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0713a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0713a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0713a-119">-InputObject</span></span>
<span data-ttu-id="0713a-120">SQL 가상 컴퓨터 개체.</span><span class="sxs-lookup"><span data-stu-id="0713a-120">SQL virtual machine object.</span></span>

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

### <span data-ttu-id="0713a-121">-이름</span><span class="sxs-lookup"><span data-stu-id="0713a-121">-Name</span></span>
<span data-ttu-id="0713a-122">SQL 가상 컴퓨터 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0713a-122">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="0713a-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0713a-123">-PassThru</span></span>
<span data-ttu-id="0713a-124">Cmdlet 실행이 종료 될 때 삭제 된 리소스를 출력할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0713a-124">Specifies whether to output the deleted resource at end of cmdlet execution.</span></span>

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

### <span data-ttu-id="0713a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0713a-125">-ResourceGroupName</span></span>
<span data-ttu-id="0713a-126">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0713a-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="0713a-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0713a-127">-ResourceId</span></span>
<span data-ttu-id="0713a-128">SQL 가상 컴퓨터 그룹 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="0713a-128">SQL virtual machine group resource id.</span></span>

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

### <span data-ttu-id="0713a-129">-확인</span><span class="sxs-lookup"><span data-stu-id="0713a-129">-Confirm</span></span>
<span data-ttu-id="0713a-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0713a-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0713a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0713a-131">-WhatIf</span></span>
<span data-ttu-id="0713a-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0713a-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0713a-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0713a-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0713a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0713a-134">CommonParameters</span></span>
<span data-ttu-id="0713a-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0713a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0713a-136">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="0713a-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0713a-137">입력</span><span class="sxs-lookup"><span data-stu-id="0713a-137">INPUTS</span></span>

### <span data-ttu-id="0713a-138">SqlVirtualMachine를 SqlVirtualMachine 합니다. AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="0713a-138">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

### <span data-ttu-id="0713a-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0713a-139">System.String</span></span>

## <span data-ttu-id="0713a-140">출력</span><span class="sxs-lookup"><span data-stu-id="0713a-140">OUTPUTS</span></span>

### <span data-ttu-id="0713a-141">SqlVirtualMachine를 SqlVirtualMachine 합니다. AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="0713a-141">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="0713a-142">상속자</span><span class="sxs-lookup"><span data-stu-id="0713a-142">NOTES</span></span>

## <span data-ttu-id="0713a-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0713a-143">RELATED LINKS</span></span>
