---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlinstancedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabase.md
ms.openlocfilehash: 342944fbd933f135f3643d4022f965405de2f1df
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698844"
---
# <span data-ttu-id="49e4d-101">Remove-AzSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="49e4d-101">Remove-AzSqlInstanceDatabase</span></span>

## <span data-ttu-id="49e4d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49e4d-102">SYNOPSIS</span></span>
<span data-ttu-id="49e4d-103">Azure SQL 관리 인스턴스 데이터베이스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="49e4d-103">Removes an Azure SQL Managed Instance database.</span></span>

## <span data-ttu-id="49e4d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="49e4d-104">SYNTAX</span></span>

### <span data-ttu-id="49e4d-105">Removeinstancedatabase찡그린 Minputparameters (기본값)</span><span class="sxs-lookup"><span data-stu-id="49e4d-105">RemoveInstanceDatabaseFromInputParameters (Default)</span></span>
```
Remove-AzSqlInstanceDatabase [-Name] <String> [-InstanceName] <String> [-ResourceGroupName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49e4d-106">RemoveInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="49e4d-106">RemoveInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Remove-AzSqlInstanceDatabase [-InputObject] <AzureSqlManagedDatabaseModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49e4d-107">RemoveInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="49e4d-107">RemoveInstanceDatabaseFromAzureResourceId</span></span>
```
Remove-AzSqlInstanceDatabase [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49e4d-108">설명은</span><span class="sxs-lookup"><span data-stu-id="49e4d-108">DESCRIPTION</span></span>
<span data-ttu-id="49e4d-109">**AzSqlInstanceDatabase** Cmdlet은 Azure SQL 관리 인스턴스 데이터베이스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="49e4d-109">The **Remove-AzSqlInstanceDatabase** cmdlet removes an Azure SQL Managed Instance database.</span></span>

## <span data-ttu-id="49e4d-110">예제의</span><span class="sxs-lookup"><span data-stu-id="49e4d-110">EXAMPLES</span></span>

### <span data-ttu-id="49e4d-111">예제 1: 인스턴스에서 데이터베이스 제거</span><span class="sxs-lookup"><span data-stu-id="49e4d-111">Example 1: Remove a database from an instance</span></span>
```
PS C:\>Remove-AzSqlInstanceDatabase -Name "Database01" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="49e4d-112">이 명령은 instance managedInstance1에서 Database01 이라는 데이터베이스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="49e4d-112">This command removes the database named Database01 from instance managedInstance1.</span></span>

## <span data-ttu-id="49e4d-113">변수</span><span class="sxs-lookup"><span data-stu-id="49e4d-113">PARAMETERS</span></span>

### <span data-ttu-id="49e4d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49e4d-114">-DefaultProfile</span></span>
<span data-ttu-id="49e4d-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="49e4d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49e4d-116">-Force</span><span class="sxs-lookup"><span data-stu-id="49e4d-116">-Force</span></span>
<span data-ttu-id="49e4d-117">작업 수행을 위한 확인 메시지 건너뛰기</span><span class="sxs-lookup"><span data-stu-id="49e4d-117">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="49e4d-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="49e4d-118">-InputObject</span></span>
<span data-ttu-id="49e4d-119">제거할 인스턴스 데이터베이스 개체</span><span class="sxs-lookup"><span data-stu-id="49e4d-119">The Instance Database object to remove</span></span>

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

### <span data-ttu-id="49e4d-120">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="49e4d-120">-InstanceName</span></span>
<span data-ttu-id="49e4d-121">인스턴스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="49e4d-121">The instance name.</span></span>

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

### <span data-ttu-id="49e4d-122">-이름</span><span class="sxs-lookup"><span data-stu-id="49e4d-122">-Name</span></span>
<span data-ttu-id="49e4d-123">제거할 Azure SQL Instance 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="49e4d-123">The name of the Azure SQL Instance Database to remove.</span></span>

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

### <span data-ttu-id="49e4d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49e4d-124">-ResourceGroupName</span></span>
<span data-ttu-id="49e4d-125">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="49e4d-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="49e4d-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="49e4d-126">-ResourceId</span></span>
<span data-ttu-id="49e4d-127">제거할 인스턴스 데이터베이스 개체의 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="49e4d-127">The resource id of Instance Database object to remove</span></span>

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

### <span data-ttu-id="49e4d-128">-확인</span><span class="sxs-lookup"><span data-stu-id="49e4d-128">-Confirm</span></span>
<span data-ttu-id="49e4d-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="49e4d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49e4d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49e4d-130">-WhatIf</span></span>
<span data-ttu-id="49e4d-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="49e4d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49e4d-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="49e4d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49e4d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49e4d-133">CommonParameters</span></span>
<span data-ttu-id="49e4d-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="49e4d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49e4d-135">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="49e4d-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49e4d-136">입력</span><span class="sxs-lookup"><span data-stu-id="49e4d-136">INPUTS</span></span>

### <span data-ttu-id="49e4d-137">AzureSqlManagedDatabaseModel (. \*. \*)</span><span class="sxs-lookup"><span data-stu-id="49e4d-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

### <span data-ttu-id="49e4d-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="49e4d-138">System.String</span></span>

## <span data-ttu-id="49e4d-139">출력</span><span class="sxs-lookup"><span data-stu-id="49e4d-139">OUTPUTS</span></span>

### <span data-ttu-id="49e4d-140">AzureSqlManagedDatabaseModel (. \*. \*)</span><span class="sxs-lookup"><span data-stu-id="49e4d-140">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="49e4d-141">상속자</span><span class="sxs-lookup"><span data-stu-id="49e4d-141">NOTES</span></span>

## <span data-ttu-id="49e4d-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="49e4d-142">RELATED LINKS</span></span>
