---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/new-azsqlvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVM.md
ms.openlocfilehash: 764312c64ae9887a6ef4243cc20b04535afcf81f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204747"
---
# <span data-ttu-id="8ee50-101">New-AzSqlVM</span><span class="sxs-lookup"><span data-stu-id="8ee50-101">New-AzSqlVM</span></span>

## <span data-ttu-id="8ee50-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ee50-102">SYNOPSIS</span></span>
<span data-ttu-id="8ee50-103">새 sql 가상 컴퓨터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8ee50-103">Creates a new sql virtual machine.</span></span>

## <span data-ttu-id="8ee50-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8ee50-104">SYNTAX</span></span>

### <span data-ttu-id="8ee50-105">NameParamaterList (기본값)</span><span class="sxs-lookup"><span data-stu-id="8ee50-105">NameParamaterList (Default)</span></span>
```
New-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-LicenseType] <String> -Location <String> [-AsJob]
 [-Offer <String>] [-Sku <String>] [-SqlManagementType <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ee50-106">NameInputObject</span><span class="sxs-lookup"><span data-stu-id="8ee50-106">NameInputObject</span></span>
```
New-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-SqlVM] <AzureSqlVMModel> -Location <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ee50-107">설명은</span><span class="sxs-lookup"><span data-stu-id="8ee50-107">DESCRIPTION</span></span>
<span data-ttu-id="8ee50-108">New-AzSqlVM cmdlet은 Azure SQL 가상 컴퓨터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8ee50-108">The New-AzSqlVM cmdlet creates an Azure SQL virtual machine.</span></span>

## <span data-ttu-id="8ee50-109">예제의</span><span class="sxs-lookup"><span data-stu-id="8ee50-109">EXAMPLES</span></span>

### <span data-ttu-id="8ee50-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="8ee50-110">Example 1</span></span>
```powershell
PS C:\> New-AzSqlVM  New-AzSqlVM -ResourceGroupName ResourceGroup01 -Name vm -LicenseType 'PAYG' -Sku Developer
Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="8ee50-111">리소스 그룹 ResourceGroup01의 이름 vm을 사용 하 여 새 Azure SQL 가상 컴퓨터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8ee50-111">Creates a new Azure SQL virtual machine with name vm in the resource group ResourceGroup01</span></span> 

## <span data-ttu-id="8ee50-112">변수</span><span class="sxs-lookup"><span data-stu-id="8ee50-112">PARAMETERS</span></span>

### <span data-ttu-id="8ee50-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8ee50-113">-AsJob</span></span>
<span data-ttu-id="8ee50-114">백그라운드에서 cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ee50-114">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="8ee50-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ee50-115">-DefaultProfile</span></span>
<span data-ttu-id="8ee50-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8ee50-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ee50-117">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="8ee50-117">-LicenseType</span></span>
<span data-ttu-id="8ee50-118">SQL 가상 컴퓨터 라이선스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="8ee50-118">SQL virtual machine license type.</span></span>

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

### <span data-ttu-id="8ee50-119">-위치</span><span class="sxs-lookup"><span data-stu-id="8ee50-119">-Location</span></span>
<span data-ttu-id="8ee50-120">SQL 가상 컴퓨터 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="8ee50-120">SQL virtual machine location.</span></span>

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

### <span data-ttu-id="8ee50-121">-이름</span><span class="sxs-lookup"><span data-stu-id="8ee50-121">-Name</span></span>
<span data-ttu-id="8ee50-122">SQL 가상 컴퓨터 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8ee50-122">SQL virtual machine name.</span></span>

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

### <span data-ttu-id="8ee50-123">-제공</span><span class="sxs-lookup"><span data-stu-id="8ee50-123">-Offer</span></span>
<span data-ttu-id="8ee50-124">SQL 가상 컴퓨터 제공</span><span class="sxs-lookup"><span data-stu-id="8ee50-124">SQL virtual machine offer.</span></span>

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

### <span data-ttu-id="8ee50-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ee50-125">-ResourceGroupName</span></span>
<span data-ttu-id="8ee50-126">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8ee50-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="8ee50-127">-Sku</span><span class="sxs-lookup"><span data-stu-id="8ee50-127">-Sku</span></span>
<span data-ttu-id="8ee50-128">SQL virtual machine edition 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="8ee50-128">SQL virtual machine edition type.</span></span>

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

### <span data-ttu-id="8ee50-129">-SqlManagementType</span><span class="sxs-lookup"><span data-stu-id="8ee50-129">-SqlManagementType</span></span>
<span data-ttu-id="8ee50-130">SQL 가상 컴퓨터 관리 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="8ee50-130">SQL virtual machine management type.</span></span>

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

### <span data-ttu-id="8ee50-131">-SqlVM</span><span class="sxs-lookup"><span data-stu-id="8ee50-131">-SqlVM</span></span>
<span data-ttu-id="8ee50-132">SQL 가상 컴퓨터 개체.</span><span class="sxs-lookup"><span data-stu-id="8ee50-132">SQL virtual machine object.</span></span>

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

### <span data-ttu-id="8ee50-133">태그</span><span class="sxs-lookup"><span data-stu-id="8ee50-133">-Tag</span></span>
<span data-ttu-id="8ee50-134">SQL 가상 컴퓨터와 연결할 태그</span><span class="sxs-lookup"><span data-stu-id="8ee50-134">The tags to associate with the SQL virtual machine</span></span>

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

### <span data-ttu-id="8ee50-135">-확인</span><span class="sxs-lookup"><span data-stu-id="8ee50-135">-Confirm</span></span>
<span data-ttu-id="8ee50-136">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ee50-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ee50-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ee50-137">-WhatIf</span></span>
<span data-ttu-id="8ee50-138">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8ee50-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ee50-139">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8ee50-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ee50-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ee50-140">CommonParameters</span></span>
<span data-ttu-id="8ee50-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ee50-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ee50-142">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8ee50-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ee50-143">입력</span><span class="sxs-lookup"><span data-stu-id="8ee50-143">INPUTS</span></span>

### <span data-ttu-id="8ee50-144">SqlVirtualMachine를 SqlVirtualMachine 합니다. AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="8ee50-144">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="8ee50-145">출력</span><span class="sxs-lookup"><span data-stu-id="8ee50-145">OUTPUTS</span></span>

### <span data-ttu-id="8ee50-146">SqlVirtualMachine를 SqlVirtualMachine 합니다. AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="8ee50-146">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="8ee50-147">상속자</span><span class="sxs-lookup"><span data-stu-id="8ee50-147">NOTES</span></span>

## <span data-ttu-id="8ee50-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8ee50-148">RELATED LINKS</span></span>
