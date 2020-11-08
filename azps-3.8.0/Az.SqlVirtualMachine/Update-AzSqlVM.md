---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/update-azsqlvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzSqlVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzSqlVM.md
ms.openlocfilehash: ce700b90194e1cd0fcdf05162696ae980d24ad01
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044187"
---
# <span data-ttu-id="e66d6-101">Update-AzSqlVM</span><span class="sxs-lookup"><span data-stu-id="e66d6-101">Update-AzSqlVM</span></span>

## <span data-ttu-id="e66d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e66d6-102">SYNOPSIS</span></span>
<span data-ttu-id="e66d6-103">Sql 가상 컴퓨터를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="e66d6-103">Updates a sql virtual machine.</span></span>

## <span data-ttu-id="e66d6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e66d6-104">SYNTAX</span></span>

### <span data-ttu-id="e66d6-105">NameParamaterList (기본값)</span><span class="sxs-lookup"><span data-stu-id="e66d6-105">NameParamaterList (Default)</span></span>
```
Update-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-LicenseType <String>] [-Offer <String>]
 [-Sku <String>] [-SqlManagementType <String>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e66d6-106">NameInputObject</span><span class="sxs-lookup"><span data-stu-id="e66d6-106">NameInputObject</span></span>
```
Update-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-InputObject] <AzureSqlVMModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e66d6-107">ResourceIdParamaterList</span><span class="sxs-lookup"><span data-stu-id="e66d6-107">ResourceIdParamaterList</span></span>
```
Update-AzSqlVM [-LicenseType <String>] [-Offer <String>] [-Sku <String>] [-SqlManagementType <String>]
 [-Tag <Hashtable>] [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e66d6-108">ResourceIdInputObject</span><span class="sxs-lookup"><span data-stu-id="e66d6-108">ResourceIdInputObject</span></span>
```
Update-AzSqlVM [-InputObject] <AzureSqlVMModel> [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e66d6-109">설명은</span><span class="sxs-lookup"><span data-stu-id="e66d6-109">DESCRIPTION</span></span>
<span data-ttu-id="e66d6-110">Update-AzSqlVM cmdlet은 sql 가상 컴퓨터를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="e66d6-110">The Update-AzSqlVM cmdlet updates a sql virtual machine.</span></span>

## <span data-ttu-id="e66d6-111">예제의</span><span class="sxs-lookup"><span data-stu-id="e66d6-111">EXAMPLES</span></span>

### <span data-ttu-id="e66d6-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="e66d6-112">Example 1</span></span>
```powershell
PS C:\> $tags = @{'key'='value'}
PS C:\> $vm = Update-AzSqlVM -InputObject $vm -Tags $tags
PS C:\> $group.Tags
Name                           Value
----                           -----
key                            value
```

<span data-ttu-id="e66d6-113">Sql 가상 컴퓨터의 태그를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="e66d6-113">Updates the tags of a sql virtual machine.</span></span>

## <span data-ttu-id="e66d6-114">변수</span><span class="sxs-lookup"><span data-stu-id="e66d6-114">PARAMETERS</span></span>

### <span data-ttu-id="e66d6-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e66d6-115">-AsJob</span></span>
<span data-ttu-id="e66d6-116">백그라운드에서 cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="e66d6-116">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="e66d6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e66d6-117">-DefaultProfile</span></span>
<span data-ttu-id="e66d6-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e66d6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e66d6-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e66d6-119">-InputObject</span></span>
<span data-ttu-id="e66d6-120">SQL 가상 컴퓨터 개체.</span><span class="sxs-lookup"><span data-stu-id="e66d6-120">SQL virtual machine object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel
Parameter Sets: NameInputObject, ResourceIdInputObject
Aliases: SqlVM

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e66d6-121">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="e66d6-121">-LicenseType</span></span>
<span data-ttu-id="e66d6-122">SQL 가상 컴퓨터 라이선스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="e66d6-122">SQL virtual machine license type.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParamaterList, ResourceIdParamaterList
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e66d6-123">-이름</span><span class="sxs-lookup"><span data-stu-id="e66d6-123">-Name</span></span>
<span data-ttu-id="e66d6-124">SQL 가상 컴퓨터 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e66d6-124">SQL virtual machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParamaterList, NameInputObject
Aliases: SqlVMName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e66d6-125">-제공</span><span class="sxs-lookup"><span data-stu-id="e66d6-125">-Offer</span></span>
<span data-ttu-id="e66d6-126">SQL 가상 컴퓨터 제공</span><span class="sxs-lookup"><span data-stu-id="e66d6-126">SQL virtual machine offer.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParamaterList, ResourceIdParamaterList
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e66d6-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e66d6-127">-ResourceGroupName</span></span>
<span data-ttu-id="e66d6-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e66d6-128">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParamaterList, NameInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e66d6-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e66d6-129">-ResourceId</span></span>
<span data-ttu-id="e66d6-130">SQL 가상 컴퓨터 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="e66d6-130">SQL virtual machine resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParamaterList, ResourceIdInputObject
Aliases: SqlVMId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e66d6-131">-Sku</span><span class="sxs-lookup"><span data-stu-id="e66d6-131">-Sku</span></span>
<span data-ttu-id="e66d6-132">SQL virtual machine edition 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="e66d6-132">SQL virtual machine edition type.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParamaterList, ResourceIdParamaterList
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e66d6-133">-SqlManagementType</span><span class="sxs-lookup"><span data-stu-id="e66d6-133">-SqlManagementType</span></span>
<span data-ttu-id="e66d6-134">SQL 가상 컴퓨터 관리 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="e66d6-134">SQL virtual machine management type.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParamaterList, ResourceIdParamaterList
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e66d6-135">태그</span><span class="sxs-lookup"><span data-stu-id="e66d6-135">-Tag</span></span>
<span data-ttu-id="e66d6-136">SQL 가상 컴퓨터와 연결할 태그</span><span class="sxs-lookup"><span data-stu-id="e66d6-136">The tags to associate with the SQL virtual machine</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: NameParamaterList, ResourceIdParamaterList
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e66d6-137">-확인</span><span class="sxs-lookup"><span data-stu-id="e66d6-137">-Confirm</span></span>
<span data-ttu-id="e66d6-138">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e66d6-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e66d6-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e66d6-139">-WhatIf</span></span>
<span data-ttu-id="e66d6-140">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e66d6-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e66d6-141">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e66d6-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e66d6-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e66d6-142">CommonParameters</span></span>
<span data-ttu-id="e66d6-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e66d6-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e66d6-144">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e66d6-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e66d6-145">입력</span><span class="sxs-lookup"><span data-stu-id="e66d6-145">INPUTS</span></span>

### <span data-ttu-id="e66d6-146">SqlVirtualMachine를 SqlVirtualMachine 합니다. AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="e66d6-146">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="e66d6-147">출력</span><span class="sxs-lookup"><span data-stu-id="e66d6-147">OUTPUTS</span></span>

### <span data-ttu-id="e66d6-148">SqlVirtualMachine를 SqlVirtualMachine 합니다. AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="e66d6-148">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="e66d6-149">상속자</span><span class="sxs-lookup"><span data-stu-id="e66d6-149">NOTES</span></span>

## <span data-ttu-id="e66d6-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e66d6-150">RELATED LINKS</span></span>
