---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/powershell/module/az.sqlvirtualmachine/remove-azsqlvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzSqlVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzSqlVM.md
ms.openlocfilehash: 741db1ddd4d2cce236d5a1d6787ea25179aa373f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101978000"
---
# <span data-ttu-id="f46ff-101">Remove-AzSqlVM</span><span class="sxs-lookup"><span data-stu-id="f46ff-101">Remove-AzSqlVM</span></span>

## <span data-ttu-id="f46ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f46ff-102">SYNOPSIS</span></span>
<span data-ttu-id="f46ff-103">SQL 가상 머신을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="f46ff-103">Deletes a sql virtual machine.</span></span>

## <span data-ttu-id="f46ff-104">구문</span><span class="sxs-lookup"><span data-stu-id="f46ff-104">SYNTAX</span></span>

### <span data-ttu-id="f46ff-105">이름(기본값)</span><span class="sxs-lookup"><span data-stu-id="f46ff-105">Name (Default)</span></span>
```
Remove-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f46ff-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="f46ff-106">InputObject</span></span>
```
Remove-AzSqlVM [-InputObject] <AzureSqlVMModel> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f46ff-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="f46ff-107">ResourceId</span></span>
```
Remove-AzSqlVM [-ResourceId] <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f46ff-108">설명</span><span class="sxs-lookup"><span data-stu-id="f46ff-108">DESCRIPTION</span></span>
<span data-ttu-id="f46ff-109">Remove-AzSqlVM cmdlet은 SQL 가상 머신을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="f46ff-109">The Remove-AzSqlVM cmdlet deletes a sql virtual machine.</span></span>

## <span data-ttu-id="f46ff-110">예제</span><span class="sxs-lookup"><span data-stu-id="f46ff-110">EXAMPLES</span></span>

### <span data-ttu-id="f46ff-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="f46ff-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSqlVM -ResourceGroupName "ResourceGroup01" -Name "vm"
```

<span data-ttu-id="f46ff-112">리소스 그룹 ResourceGroup01에서 azure SQL "vm"을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="f46ff-112">Deletes the Azure SQL virtual machine "vm" in the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="f46ff-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="f46ff-113">PARAMETERS</span></span>

### <span data-ttu-id="f46ff-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f46ff-114">-AsJob</span></span>
<span data-ttu-id="f46ff-115">백그라운드에서 cmdlet을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="f46ff-115">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="f46ff-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f46ff-116">-DefaultProfile</span></span>
<span data-ttu-id="f46ff-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f46ff-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f46ff-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f46ff-118">-InputObject</span></span>
<span data-ttu-id="f46ff-119">SQL 가상 머신 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="f46ff-119">SQL virtual machine object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel
Parameter Sets: InputObject
Aliases: SqlVM

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f46ff-120">-Name</span><span class="sxs-lookup"><span data-stu-id="f46ff-120">-Name</span></span>
<span data-ttu-id="f46ff-121">SQL 가상 머신 이름을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="f46ff-121">SQL virtual machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: SqlVMName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f46ff-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f46ff-122">-PassThru</span></span>
<span data-ttu-id="f46ff-123">cmdlet 실행이 끝날 때 삭제된 리소스를 출력할지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f46ff-123">Specifies whether to output the deleted resource at end of cmdlet execution.</span></span>

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

### <span data-ttu-id="f46ff-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f46ff-124">-ResourceGroupName</span></span>
<span data-ttu-id="f46ff-125">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f46ff-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="f46ff-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f46ff-126">-ResourceId</span></span>
<span data-ttu-id="f46ff-127">SQL 리소스 ID를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="f46ff-127">SQL virtual machine resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases: SqlVMId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f46ff-128">-확인</span><span class="sxs-lookup"><span data-stu-id="f46ff-128">-Confirm</span></span>
<span data-ttu-id="f46ff-129">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f46ff-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f46ff-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f46ff-130">-WhatIf</span></span>
<span data-ttu-id="f46ff-131">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="f46ff-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f46ff-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f46ff-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f46ff-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f46ff-133">CommonParameters</span></span>
<span data-ttu-id="f46ff-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f46ff-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f46ff-135">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f46ff-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f46ff-136">입력</span><span class="sxs-lookup"><span data-stu-id="f46ff-136">INPUTS</span></span>

### <span data-ttu-id="f46ff-137">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="f46ff-137">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="f46ff-138">출력</span><span class="sxs-lookup"><span data-stu-id="f46ff-138">OUTPUTS</span></span>

### <span data-ttu-id="f46ff-139">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="f46ff-139">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="f46ff-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f46ff-140">NOTES</span></span>

## <span data-ttu-id="f46ff-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f46ff-141">RELATED LINKS</span></span>
