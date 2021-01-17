---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/remove-azsqlvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzSqlVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzSqlVM.md
ms.openlocfilehash: 4478ec96cd7354a404a736ddd0f305cba5675b26
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491546"
---
# <span data-ttu-id="7c079-101">Remove-AzSqlVM</span><span class="sxs-lookup"><span data-stu-id="7c079-101">Remove-AzSqlVM</span></span>

## <span data-ttu-id="7c079-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c079-102">SYNOPSIS</span></span>
<span data-ttu-id="7c079-103">SQL 가상 머신을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="7c079-103">Deletes a sql virtual machine.</span></span>

## <span data-ttu-id="7c079-104">구문</span><span class="sxs-lookup"><span data-stu-id="7c079-104">SYNTAX</span></span>

### <span data-ttu-id="7c079-105">이름(기본값)</span><span class="sxs-lookup"><span data-stu-id="7c079-105">Name (Default)</span></span>
```
Remove-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c079-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="7c079-106">InputObject</span></span>
```
Remove-AzSqlVM [-InputObject] <AzureSqlVMModel> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c079-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="7c079-107">ResourceId</span></span>
```
Remove-AzSqlVM [-ResourceId] <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c079-108">설명</span><span class="sxs-lookup"><span data-stu-id="7c079-108">DESCRIPTION</span></span>
<span data-ttu-id="7c079-109">Remove-AzSqlVM cmdlet은 SQL 가상 머신을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="7c079-109">The Remove-AzSqlVM cmdlet deletes a sql virtual machine.</span></span>

## <span data-ttu-id="7c079-110">예제</span><span class="sxs-lookup"><span data-stu-id="7c079-110">EXAMPLES</span></span>

### <span data-ttu-id="7c079-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="7c079-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSqlVM -ResourceGroupName "ResourceGroup01" -Name "vm"
```

<span data-ttu-id="7c079-112">ResourceGroup01에서 Azure SQL "vm"을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="7c079-112">Deletes the Azure SQL virtual machine "vm" in the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="7c079-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7c079-113">PARAMETERS</span></span>

### <span data-ttu-id="7c079-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7c079-114">-AsJob</span></span>
<span data-ttu-id="7c079-115">백그라운드에서 cmdlet을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="7c079-115">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="7c079-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c079-116">-DefaultProfile</span></span>
<span data-ttu-id="7c079-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7c079-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c079-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7c079-118">-InputObject</span></span>
<span data-ttu-id="7c079-119">SQL 가상 머신 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7c079-119">SQL virtual machine object.</span></span>

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

### <span data-ttu-id="7c079-120">-Name</span><span class="sxs-lookup"><span data-stu-id="7c079-120">-Name</span></span>
<span data-ttu-id="7c079-121">SQL 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7c079-121">SQL virtual machine name.</span></span>

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

### <span data-ttu-id="7c079-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7c079-122">-PassThru</span></span>
<span data-ttu-id="7c079-123">cmdlet 실행이 끝나면 삭제된 리소스를 출력할지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7c079-123">Specifies whether to output the deleted resource at end of cmdlet execution.</span></span>

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

### <span data-ttu-id="7c079-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c079-124">-ResourceGroupName</span></span>
<span data-ttu-id="7c079-125">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7c079-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="7c079-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7c079-126">-ResourceId</span></span>
<span data-ttu-id="7c079-127">SQL 리소스 ID를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="7c079-127">SQL virtual machine resource id.</span></span>

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

### <span data-ttu-id="7c079-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7c079-128">-Confirm</span></span>
<span data-ttu-id="7c079-129">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7c079-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c079-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c079-130">-WhatIf</span></span>
<span data-ttu-id="7c079-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="7c079-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c079-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7c079-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c079-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c079-133">CommonParameters</span></span>
<span data-ttu-id="7c079-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7c079-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c079-135">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7c079-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c079-136">입력</span><span class="sxs-lookup"><span data-stu-id="7c079-136">INPUTS</span></span>

### <span data-ttu-id="7c079-137">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="7c079-137">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="7c079-138">출력</span><span class="sxs-lookup"><span data-stu-id="7c079-138">OUTPUTS</span></span>

### <span data-ttu-id="7c079-139">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="7c079-139">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="7c079-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7c079-140">NOTES</span></span>

## <span data-ttu-id="7c079-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7c079-141">RELATED LINKS</span></span>
