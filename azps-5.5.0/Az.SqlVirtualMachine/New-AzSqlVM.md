---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/new-azsqlvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVM.md
ms.openlocfilehash: 764312c64ae9887a6ef4243cc20b04535afcf81f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201393"
---
# <span data-ttu-id="edfb8-101">New-AzSqlVM</span><span class="sxs-lookup"><span data-stu-id="edfb8-101">New-AzSqlVM</span></span>

## <span data-ttu-id="edfb8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="edfb8-102">SYNOPSIS</span></span>
<span data-ttu-id="edfb8-103">새 SQL 가상 머신을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="edfb8-103">Creates a new sql virtual machine.</span></span>

## <span data-ttu-id="edfb8-104">구문</span><span class="sxs-lookup"><span data-stu-id="edfb8-104">SYNTAX</span></span>

### <span data-ttu-id="edfb8-105">NameParamaterList(기본값)</span><span class="sxs-lookup"><span data-stu-id="edfb8-105">NameParamaterList (Default)</span></span>
```
New-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-LicenseType] <String> -Location <String> [-AsJob]
 [-Offer <String>] [-Sku <String>] [-SqlManagementType <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="edfb8-106">NameInputObject</span><span class="sxs-lookup"><span data-stu-id="edfb8-106">NameInputObject</span></span>
```
New-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-SqlVM] <AzureSqlVMModel> -Location <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="edfb8-107">설명</span><span class="sxs-lookup"><span data-stu-id="edfb8-107">DESCRIPTION</span></span>
<span data-ttu-id="edfb8-108">New-AzSqlVM cmdlet은 Azure SQL 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="edfb8-108">The New-AzSqlVM cmdlet creates an Azure SQL virtual machine.</span></span>

## <span data-ttu-id="edfb8-109">예제</span><span class="sxs-lookup"><span data-stu-id="edfb8-109">EXAMPLES</span></span>

### <span data-ttu-id="edfb8-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="edfb8-110">Example 1</span></span>
```powershell
PS C:\> New-AzSqlVM  New-AzSqlVM -ResourceGroupName ResourceGroup01 -Name vm -LicenseType 'PAYG' -Sku Developer
Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="edfb8-111">리소스 그룹 ResourceGroup01에서 이름 vm을 사용하여 새 Azure SQL 가상 머신을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="edfb8-111">Creates a new Azure SQL virtual machine with name vm in the resource group ResourceGroup01</span></span> 

## <span data-ttu-id="edfb8-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="edfb8-112">PARAMETERS</span></span>

### <span data-ttu-id="edfb8-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="edfb8-113">-AsJob</span></span>
<span data-ttu-id="edfb8-114">백그라운드에서 cmdlet을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="edfb8-114">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="edfb8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edfb8-115">-DefaultProfile</span></span>
<span data-ttu-id="edfb8-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="edfb8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="edfb8-117">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="edfb8-117">-LicenseType</span></span>
<span data-ttu-id="edfb8-118">SQL 가상 머신 라이선스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="edfb8-118">SQL virtual machine license type.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParamaterList
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edfb8-119">-Location</span><span class="sxs-lookup"><span data-stu-id="edfb8-119">-Location</span></span>
<span data-ttu-id="edfb8-120">SQL 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="edfb8-120">SQL virtual machine location.</span></span>

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

### <span data-ttu-id="edfb8-121">-Name</span><span class="sxs-lookup"><span data-stu-id="edfb8-121">-Name</span></span>
<span data-ttu-id="edfb8-122">SQL 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="edfb8-122">SQL virtual machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SqlVMName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edfb8-123">-Offer</span><span class="sxs-lookup"><span data-stu-id="edfb8-123">-Offer</span></span>
<span data-ttu-id="edfb8-124">SQL 가상 머신 제품입니다.</span><span class="sxs-lookup"><span data-stu-id="edfb8-124">SQL virtual machine offer.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParamaterList
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edfb8-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="edfb8-125">-ResourceGroupName</span></span>
<span data-ttu-id="edfb8-126">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="edfb8-126">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edfb8-127">-Sku</span><span class="sxs-lookup"><span data-stu-id="edfb8-127">-Sku</span></span>
<span data-ttu-id="edfb8-128">SQL 가상 머신 버전 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="edfb8-128">SQL virtual machine edition type.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParamaterList
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edfb8-129">-SqlManagementType</span><span class="sxs-lookup"><span data-stu-id="edfb8-129">-SqlManagementType</span></span>
<span data-ttu-id="edfb8-130">SQL 가상 머신 관리 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="edfb8-130">SQL virtual machine management type.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParamaterList
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edfb8-131">-SqlVM</span><span class="sxs-lookup"><span data-stu-id="edfb8-131">-SqlVM</span></span>
<span data-ttu-id="edfb8-132">SQL 가상 머신 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="edfb8-132">SQL virtual machine object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel
Parameter Sets: NameInputObject
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="edfb8-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="edfb8-133">-Tag</span></span>
<span data-ttu-id="edfb8-134">가상 머신과 연결하기 위한 SQL.</span><span class="sxs-lookup"><span data-stu-id="edfb8-134">The tags to associate with the SQL virtual machine</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: NameParamaterList
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edfb8-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="edfb8-135">-Confirm</span></span>
<span data-ttu-id="edfb8-136">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="edfb8-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="edfb8-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="edfb8-137">-WhatIf</span></span>
<span data-ttu-id="edfb8-138">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="edfb8-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="edfb8-139">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="edfb8-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="edfb8-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edfb8-140">CommonParameters</span></span>
<span data-ttu-id="edfb8-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="edfb8-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edfb8-142">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="edfb8-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edfb8-143">입력</span><span class="sxs-lookup"><span data-stu-id="edfb8-143">INPUTS</span></span>

### <span data-ttu-id="edfb8-144">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="edfb8-144">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="edfb8-145">출력</span><span class="sxs-lookup"><span data-stu-id="edfb8-145">OUTPUTS</span></span>

### <span data-ttu-id="edfb8-146">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="edfb8-146">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="edfb8-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="edfb8-147">NOTES</span></span>

## <span data-ttu-id="edfb8-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="edfb8-148">RELATED LINKS</span></span>
