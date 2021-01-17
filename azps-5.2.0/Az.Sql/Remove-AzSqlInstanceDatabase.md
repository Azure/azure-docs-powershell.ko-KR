---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlinstancedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabase.md
ms.openlocfilehash: a496bd4ba68d9d62bdfe65dc293c68377b7d3aa6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98369629"
---
# <span data-ttu-id="53eed-101">Remove-AzSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="53eed-101">Remove-AzSqlInstanceDatabase</span></span>

## <span data-ttu-id="53eed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="53eed-102">SYNOPSIS</span></span>
<span data-ttu-id="53eed-103">Azure SQL Managed Instance 데이터베이스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="53eed-103">Removes an Azure SQL Managed Instance database.</span></span>

## <span data-ttu-id="53eed-104">구문</span><span class="sxs-lookup"><span data-stu-id="53eed-104">SYNTAX</span></span>

### <span data-ttu-id="53eed-105">RemoveInstanceDatabaseFromInputParameters(기본값)</span><span class="sxs-lookup"><span data-stu-id="53eed-105">RemoveInstanceDatabaseFromInputParameters (Default)</span></span>
```
Remove-AzSqlInstanceDatabase [-Name] <String> [-InstanceName] <String> [-ResourceGroupName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53eed-106">RemoveInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="53eed-106">RemoveInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Remove-AzSqlInstanceDatabase [-InputObject] <AzureSqlManagedDatabaseModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53eed-107">RemoveInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="53eed-107">RemoveInstanceDatabaseFromAzureResourceId</span></span>
```
Remove-AzSqlInstanceDatabase [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53eed-108">설명</span><span class="sxs-lookup"><span data-stu-id="53eed-108">DESCRIPTION</span></span>
<span data-ttu-id="53eed-109">**Remove-AzSqlInstanceDatabase** cmdlet은 Azure SQL Managed Instance 데이터베이스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="53eed-109">The **Remove-AzSqlInstanceDatabase** cmdlet removes an Azure SQL Managed Instance database.</span></span>

## <span data-ttu-id="53eed-110">예제</span><span class="sxs-lookup"><span data-stu-id="53eed-110">EXAMPLES</span></span>

### <span data-ttu-id="53eed-111">예제 1: 인스턴스에서 데이터베이스 제거</span><span class="sxs-lookup"><span data-stu-id="53eed-111">Example 1: Remove a database from an instance</span></span>
```
PS C:\>Remove-AzSqlInstanceDatabase -Name "Database01" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="53eed-112">이 명령은 managedInstance1 인스턴스에서 Database01이라는 데이터베이스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="53eed-112">This command removes the database named Database01 from instance managedInstance1.</span></span>

## <span data-ttu-id="53eed-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="53eed-113">PARAMETERS</span></span>

### <span data-ttu-id="53eed-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53eed-114">-DefaultProfile</span></span>
<span data-ttu-id="53eed-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="53eed-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53eed-116">-Force</span><span class="sxs-lookup"><span data-stu-id="53eed-116">-Force</span></span>
<span data-ttu-id="53eed-117">작업을 수행하기 위한 확인 메시지 건너뛰기</span><span class="sxs-lookup"><span data-stu-id="53eed-117">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="53eed-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="53eed-118">-InputObject</span></span>
<span data-ttu-id="53eed-119">제거할 인스턴스 데이터베이스 개체</span><span class="sxs-lookup"><span data-stu-id="53eed-119">The Instance Database object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel
Parameter Sets: RemoveInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition
Aliases: InstanceDatabase

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="53eed-120">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="53eed-120">-InstanceName</span></span>
<span data-ttu-id="53eed-121">인스턴스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="53eed-121">The instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53eed-122">-Name</span><span class="sxs-lookup"><span data-stu-id="53eed-122">-Name</span></span>
<span data-ttu-id="53eed-123">제거할 Azure SQL Instance 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="53eed-123">The name of the Azure SQL Instance Database to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveInstanceDatabaseFromInputParameters
Aliases: InstanceDatabaseName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53eed-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53eed-124">-ResourceGroupName</span></span>
<span data-ttu-id="53eed-125">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="53eed-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53eed-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="53eed-126">-ResourceId</span></span>
<span data-ttu-id="53eed-127">제거할 Instance Database 개체의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="53eed-127">The resource id of Instance Database object to remove</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveInstanceDatabaseFromAzureResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53eed-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="53eed-128">-Confirm</span></span>
<span data-ttu-id="53eed-129">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="53eed-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53eed-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53eed-130">-WhatIf</span></span>
<span data-ttu-id="53eed-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="53eed-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53eed-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="53eed-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53eed-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53eed-133">CommonParameters</span></span>
<span data-ttu-id="53eed-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="53eed-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53eed-135">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="53eed-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53eed-136">입력</span><span class="sxs-lookup"><span data-stu-id="53eed-136">INPUTS</span></span>

### <span data-ttu-id="53eed-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="53eed-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

### <span data-ttu-id="53eed-138">System.String</span><span class="sxs-lookup"><span data-stu-id="53eed-138">System.String</span></span>

## <span data-ttu-id="53eed-139">출력</span><span class="sxs-lookup"><span data-stu-id="53eed-139">OUTPUTS</span></span>

### <span data-ttu-id="53eed-140">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="53eed-140">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="53eed-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="53eed-141">NOTES</span></span>

## <span data-ttu-id="53eed-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="53eed-142">RELATED LINKS</span></span>
