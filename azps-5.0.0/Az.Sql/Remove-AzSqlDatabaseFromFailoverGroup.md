---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabasefromfailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseFromFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseFromFailoverGroup.md
ms.openlocfilehash: 7fa7c09d5c6c992dfa3eab7a6f81b70e820a9ee4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216637"
---
# <span data-ttu-id="6774d-101">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="6774d-101">Remove-AzSqlDatabaseFromFailoverGroup</span></span>

## <span data-ttu-id="6774d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6774d-102">SYNOPSIS</span></span>
<span data-ttu-id="6774d-103">Azure SQL 데이터베이스 장애 조치 (Failover) 그룹에서 하나 이상의 데이터베이스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="6774d-103">Removes one or more databases from an Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="6774d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6774d-104">SYNTAX</span></span>

```
Remove-AzSqlDatabaseFromFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String>
 -Database <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel]>
 [-Force] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6774d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="6774d-105">DESCRIPTION</span></span>
<span data-ttu-id="6774d-106">지정 된 Azure SQL 데이터베이스 장애 조치 (Failover) 그룹에서 하나 이상의 데이터베이스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="6774d-106">Removes one or more databases from the specified Azure SQL Database Failover Group.</span></span> <span data-ttu-id="6774d-107">데이터베이스와 복제 관계는 그대로 유지 되지만 장애 조치 그룹 끝점을 통해 더 이상 액세스할 수 없게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6774d-107">The databases and replication relationships are left intact, but they will no longer be accessible through the Failover Group endpoints.</span></span>
<span data-ttu-id="6774d-108">'-Database ' 매개 변수를 채울 데이터베이스 개체를 가져오려면 Get-AzSqlDatabase cmdlet을 사용 합니다 (예:).</span><span class="sxs-lookup"><span data-stu-id="6774d-108">To obtain database objects with which to populate the '-Database' parameter, use (for example) the Get-AzSqlDatabase cmdlet.</span></span>
<span data-ttu-id="6774d-109">명령 실행을 위해 장애 조치 그룹의 주 서버를 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6774d-109">The Failover Group's primary server must be used to execute the command.</span></span>

## <span data-ttu-id="6774d-110">예제의</span><span class="sxs-lookup"><span data-stu-id="6774d-110">EXAMPLES</span></span>

### <span data-ttu-id="6774d-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="6774d-111">Example 1</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabase -ResourceGroupName rg -ServerName primaryserver -DatabaseName db1 | Remove-AzSqlDatabaseFromFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
```

<span data-ttu-id="6774d-112">이 명령은 한 데이터베이스를 파이핑 하 여 장애 조치 그룹에서 하나를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="6774d-112">This command removes one database from a Failover Group by piping it in.</span></span>

### <span data-ttu-id="6774d-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="6774d-113">Example 2</span></span>
```
PS C:\> $primaryServer = Get-AzSqlServer -ResourceGroupName rg -ServerName primaryserver
PS C:\> $failoverGroup = $primaryServer | Remove-AzSqlDatabaseFromFailoverGroup -FailoverGroupName fg -Database ($primaryServer | Get-AzSqlDatabase)
```

<span data-ttu-id="6774d-114">이 명령은 장애 조치 (Failover) 그룹에서 모든 데이터베이스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="6774d-114">This command removes all databases from a Failover Group.</span></span>

### <span data-ttu-id="6774d-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="6774d-115">Example 3</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
PS C:\> $databases = Get-AzSqlElasticPoolDatabase -ResourceGroupName rg -ServerName primaryserver -ElasticPoolName pool1
PS C:\> $failoverGroup = $failoverGroup | Remove-AzSqlDatabaseFromFailoverGroup -Database $databases
```

<span data-ttu-id="6774d-116">이 명령은 장애 조치 그룹에서 탄력적 풀의 모든 데이터베이스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="6774d-116">This command removes all databases in an Elastic Pool from a Failover Group.</span></span>

## <span data-ttu-id="6774d-117">변수</span><span class="sxs-lookup"><span data-stu-id="6774d-117">PARAMETERS</span></span>

### <span data-ttu-id="6774d-118">-데이터베이스</span><span class="sxs-lookup"><span data-stu-id="6774d-118">-Database</span></span>
<span data-ttu-id="6774d-119">장애 조치 그룹에서 제거할 장애 조치 그룹의 주 서버에 있는 하나 이상의 Azure SQL 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="6774d-119">One or more Azure SQL Databases on the Failover Group's primary server to be removed from the Failover Group.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6774d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6774d-120">-DefaultProfile</span></span>
<span data-ttu-id="6774d-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="6774d-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6774d-122">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="6774d-122">-FailoverGroupName</span></span>
<span data-ttu-id="6774d-123">Azure SQL Database 장애 조치 (Failover) 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6774d-123">The name of the Azure SQL Database Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6774d-124">-Force</span><span class="sxs-lookup"><span data-stu-id="6774d-124">-Force</span></span>
<span data-ttu-id="6774d-125">작업 수행에 대 한 건너뛰기 확인 메시지입니다.</span><span class="sxs-lookup"><span data-stu-id="6774d-125">Skip confirmation message for performing the action.</span></span>

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

### <span data-ttu-id="6774d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6774d-126">-ResourceGroupName</span></span>
<span data-ttu-id="6774d-127">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6774d-127">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6774d-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="6774d-128">-ServerName</span></span>
<span data-ttu-id="6774d-129">장애 조치 (Failover) 그룹의 기본 Azure SQL 데이터베이스 서버 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6774d-129">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6774d-130">-확인</span><span class="sxs-lookup"><span data-stu-id="6774d-130">-Confirm</span></span>
<span data-ttu-id="6774d-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6774d-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6774d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6774d-132">-WhatIf</span></span>
<span data-ttu-id="6774d-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6774d-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6774d-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6774d-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6774d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6774d-135">CommonParameters</span></span>
<span data-ttu-id="6774d-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6774d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6774d-137">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6774d-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6774d-138">입력</span><span class="sxs-lookup"><span data-stu-id="6774d-138">INPUTS</span></span>

### <span data-ttu-id="6774d-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="6774d-139">System.String</span></span>

### <span data-ttu-id="6774d-140">AzureSqlDatabaseModel, [[Microsoft Azure. 1.3.0.0, Microsoft Azure. PowerShell., Culture = 중립, PublicKeyToken = null]] 목록에 List ' 1 '이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6774d-140">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel, Microsoft.Azure.PowerShell.Cmdlets.Sql, Version=1.3.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="6774d-141">출력</span><span class="sxs-lookup"><span data-stu-id="6774d-141">OUTPUTS</span></span>

### <span data-ttu-id="6774d-142">AzureSqlFailoverGroupModel (\*. \*.)</span><span class="sxs-lookup"><span data-stu-id="6774d-142">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="6774d-143">상속자</span><span class="sxs-lookup"><span data-stu-id="6774d-143">NOTES</span></span>

## <span data-ttu-id="6774d-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6774d-144">RELATED LINKS</span></span>

[<span data-ttu-id="6774d-145">새로운 AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="6774d-145">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="6774d-146">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="6774d-146">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="6774d-147">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="6774d-147">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="6774d-148">추가-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="6774d-148">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="6774d-149">스위치-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="6774d-149">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="6774d-150">제거-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="6774d-150">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="6774d-151">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="6774d-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
