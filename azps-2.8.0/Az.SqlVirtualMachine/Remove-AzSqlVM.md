---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/remove-azsqlvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzSqlVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzSqlVM.md
ms.openlocfilehash: 5a9d08e007e951700ef6e78fd211303e17d0351c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93874005"
---
# <span data-ttu-id="f3b40-101">Remove-AzSqlVM</span><span class="sxs-lookup"><span data-stu-id="f3b40-101">Remove-AzSqlVM</span></span>

## <span data-ttu-id="f3b40-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3b40-102">SYNOPSIS</span></span>
<span data-ttu-id="f3b40-103">Sql 가상 컴퓨터를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3b40-103">Deletes a sql virtual machine.</span></span>

## <span data-ttu-id="f3b40-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f3b40-104">SYNTAX</span></span>

### <span data-ttu-id="f3b40-105">Name (기본값)</span><span class="sxs-lookup"><span data-stu-id="f3b40-105">Name (Default)</span></span>
```
Remove-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3b40-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="f3b40-106">InputObject</span></span>
```
Remove-AzSqlVM [-InputObject] <AzureSqlVMModel> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3b40-107">리소스</span><span class="sxs-lookup"><span data-stu-id="f3b40-107">ResourceId</span></span>
```
Remove-AzSqlVM [-ResourceId] <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3b40-108">설명은</span><span class="sxs-lookup"><span data-stu-id="f3b40-108">DESCRIPTION</span></span>
<span data-ttu-id="f3b40-109">Remove-AzSqlVM cmdlet은 sql 가상 컴퓨터를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3b40-109">The Remove-AzSqlVM cmdlet deletes a sql virtual machine.</span></span>

## <span data-ttu-id="f3b40-110">예제의</span><span class="sxs-lookup"><span data-stu-id="f3b40-110">EXAMPLES</span></span>

### <span data-ttu-id="f3b40-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="f3b40-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSqlVM -ResourceGroupName "ResourceGroup01" -Name "vm"
```

<span data-ttu-id="f3b40-112">리소스 그룹 ResourceGroup01에서 Azure SQL virtual machine "vm"을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3b40-112">Deletes the Azure SQL virtual machine "vm" in the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="f3b40-113">변수</span><span class="sxs-lookup"><span data-stu-id="f3b40-113">PARAMETERS</span></span>

### <span data-ttu-id="f3b40-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f3b40-114">-AsJob</span></span>
<span data-ttu-id="f3b40-115">백그라운드에서 cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3b40-115">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="f3b40-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3b40-116">-DefaultProfile</span></span>
<span data-ttu-id="f3b40-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f3b40-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3b40-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f3b40-118">-InputObject</span></span>
<span data-ttu-id="f3b40-119">SQL 가상 컴퓨터 개체.</span><span class="sxs-lookup"><span data-stu-id="f3b40-119">SQL virtual machine object.</span></span>

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

### <span data-ttu-id="f3b40-120">-이름</span><span class="sxs-lookup"><span data-stu-id="f3b40-120">-Name</span></span>
<span data-ttu-id="f3b40-121">SQL 가상 컴퓨터 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f3b40-121">SQL virtual machine name.</span></span>

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

### <span data-ttu-id="f3b40-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f3b40-122">-PassThru</span></span>
<span data-ttu-id="f3b40-123">Cmdlet 실행이 종료 될 때 삭제 된 리소스를 출력할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3b40-123">Specifies whether to output the deleted resource at end of cmdlet execution.</span></span>

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

### <span data-ttu-id="f3b40-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3b40-124">-ResourceGroupName</span></span>
<span data-ttu-id="f3b40-125">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f3b40-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="f3b40-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f3b40-126">-ResourceId</span></span>
<span data-ttu-id="f3b40-127">SQL 가상 컴퓨터 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="f3b40-127">SQL virtual machine resource id.</span></span>

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

### <span data-ttu-id="f3b40-128">-확인</span><span class="sxs-lookup"><span data-stu-id="f3b40-128">-Confirm</span></span>
<span data-ttu-id="f3b40-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3b40-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3b40-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3b40-130">-WhatIf</span></span>
<span data-ttu-id="f3b40-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f3b40-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3b40-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f3b40-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3b40-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3b40-133">CommonParameters</span></span>
<span data-ttu-id="f3b40-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3b40-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3b40-135">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f3b40-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3b40-136">입력</span><span class="sxs-lookup"><span data-stu-id="f3b40-136">INPUTS</span></span>

### <span data-ttu-id="f3b40-137">SqlVirtualMachine를 SqlVirtualMachine 합니다. AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="f3b40-137">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="f3b40-138">출력</span><span class="sxs-lookup"><span data-stu-id="f3b40-138">OUTPUTS</span></span>

### <span data-ttu-id="f3b40-139">SqlVirtualMachine를 SqlVirtualMachine 합니다. AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="f3b40-139">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="f3b40-140">상속자</span><span class="sxs-lookup"><span data-stu-id="f3b40-140">NOTES</span></span>

## <span data-ttu-id="f3b40-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f3b40-141">RELATED LINKS</span></span>
