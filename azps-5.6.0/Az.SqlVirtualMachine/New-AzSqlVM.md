---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/powershell/module/az.sqlvirtualmachine/new-azsqlvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVM.md
ms.openlocfilehash: f7afae369258a30a156ff0439407fb4e4e4ef732
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008315"
---
# <span data-ttu-id="d92e6-101">New-AzSqlVM</span><span class="sxs-lookup"><span data-stu-id="d92e6-101">New-AzSqlVM</span></span>

## <span data-ttu-id="d92e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d92e6-102">SYNOPSIS</span></span>
<span data-ttu-id="d92e6-103">새 SQL 가상 머신을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d92e6-103">Creates a new sql virtual machine.</span></span>

## <span data-ttu-id="d92e6-104">구문</span><span class="sxs-lookup"><span data-stu-id="d92e6-104">SYNTAX</span></span>

### <span data-ttu-id="d92e6-105">NameParamaterList(기본값)</span><span class="sxs-lookup"><span data-stu-id="d92e6-105">NameParamaterList (Default)</span></span>
```
New-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-LicenseType] <String> -Location <String> [-AsJob]
 [-Offer <String>] [-Sku <String>] [-SqlManagementType <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d92e6-106">NameInputObject</span><span class="sxs-lookup"><span data-stu-id="d92e6-106">NameInputObject</span></span>
```
New-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-SqlVM] <AzureSqlVMModel> -Location <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d92e6-107">설명</span><span class="sxs-lookup"><span data-stu-id="d92e6-107">DESCRIPTION</span></span>
<span data-ttu-id="d92e6-108">New-AzSqlVM cmdlet은 Azure SQL 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d92e6-108">The New-AzSqlVM cmdlet creates an Azure SQL virtual machine.</span></span>

## <span data-ttu-id="d92e6-109">예제</span><span class="sxs-lookup"><span data-stu-id="d92e6-109">EXAMPLES</span></span>

### <span data-ttu-id="d92e6-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="d92e6-110">Example 1</span></span>
```powershell
PS C:\> New-AzSqlVM  New-AzSqlVM -ResourceGroupName ResourceGroup01 -Name vm -LicenseType 'PAYG' -Sku Developer
Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="d92e6-111">리소스 그룹 ResourceGroup01에서 이름 vm이 있는 새 Azure SQL 가상 머신을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d92e6-111">Creates a new Azure SQL virtual machine with name vm in the resource group ResourceGroup01</span></span> 

## <span data-ttu-id="d92e6-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="d92e6-112">PARAMETERS</span></span>

### <span data-ttu-id="d92e6-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d92e6-113">-AsJob</span></span>
<span data-ttu-id="d92e6-114">백그라운드에서 cmdlet을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="d92e6-114">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="d92e6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d92e6-115">-DefaultProfile</span></span>
<span data-ttu-id="d92e6-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d92e6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d92e6-117">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="d92e6-117">-LicenseType</span></span>
<span data-ttu-id="d92e6-118">SQL 가상 머신 라이선스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="d92e6-118">SQL virtual machine license type.</span></span>

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

### <span data-ttu-id="d92e6-119">-Location</span><span class="sxs-lookup"><span data-stu-id="d92e6-119">-Location</span></span>
<span data-ttu-id="d92e6-120">SQL 가상 머신 위치를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="d92e6-120">SQL virtual machine location.</span></span>

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

### <span data-ttu-id="d92e6-121">-Name</span><span class="sxs-lookup"><span data-stu-id="d92e6-121">-Name</span></span>
<span data-ttu-id="d92e6-122">SQL 가상 머신 이름을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="d92e6-122">SQL virtual machine name.</span></span>

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

### <span data-ttu-id="d92e6-123">-제품</span><span class="sxs-lookup"><span data-stu-id="d92e6-123">-Offer</span></span>
<span data-ttu-id="d92e6-124">SQL 가상 머신 제품입니다.</span><span class="sxs-lookup"><span data-stu-id="d92e6-124">SQL virtual machine offer.</span></span>

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

### <span data-ttu-id="d92e6-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d92e6-125">-ResourceGroupName</span></span>
<span data-ttu-id="d92e6-126">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d92e6-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="d92e6-127">-Sku</span><span class="sxs-lookup"><span data-stu-id="d92e6-127">-Sku</span></span>
<span data-ttu-id="d92e6-128">SQL 가상 머신 버전 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="d92e6-128">SQL virtual machine edition type.</span></span>

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

### <span data-ttu-id="d92e6-129">-SqlManagementType</span><span class="sxs-lookup"><span data-stu-id="d92e6-129">-SqlManagementType</span></span>
<span data-ttu-id="d92e6-130">SQL 가상 머신 관리 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="d92e6-130">SQL virtual machine management type.</span></span>

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

### <span data-ttu-id="d92e6-131">-SqlVM</span><span class="sxs-lookup"><span data-stu-id="d92e6-131">-SqlVM</span></span>
<span data-ttu-id="d92e6-132">SQL 가상 머신 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="d92e6-132">SQL virtual machine object.</span></span>

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

### <span data-ttu-id="d92e6-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="d92e6-133">-Tag</span></span>
<span data-ttu-id="d92e6-134">가상 머신과 연결되는 SQL 태그</span><span class="sxs-lookup"><span data-stu-id="d92e6-134">The tags to associate with the SQL virtual machine</span></span>

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

### <span data-ttu-id="d92e6-135">-확인</span><span class="sxs-lookup"><span data-stu-id="d92e6-135">-Confirm</span></span>
<span data-ttu-id="d92e6-136">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d92e6-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d92e6-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d92e6-137">-WhatIf</span></span>
<span data-ttu-id="d92e6-138">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="d92e6-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d92e6-139">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d92e6-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d92e6-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d92e6-140">CommonParameters</span></span>
<span data-ttu-id="d92e6-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d92e6-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d92e6-142">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d92e6-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d92e6-143">입력</span><span class="sxs-lookup"><span data-stu-id="d92e6-143">INPUTS</span></span>

### <span data-ttu-id="d92e6-144">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="d92e6-144">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="d92e6-145">출력</span><span class="sxs-lookup"><span data-stu-id="d92e6-145">OUTPUTS</span></span>

### <span data-ttu-id="d92e6-146">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="d92e6-146">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="d92e6-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d92e6-147">NOTES</span></span>

## <span data-ttu-id="d92e6-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d92e6-148">RELATED LINKS</span></span>
