---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/add-azsqldatabasetofailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlDatabaseToFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlDatabaseToFailoverGroup.md
ms.openlocfilehash: 7577809134987bd1a0092e28170d5bf25ccac04e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98375607"
---
# <span data-ttu-id="9e451-101">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="9e451-101">Add-AzSqlDatabaseToFailoverGroup</span></span>

## <span data-ttu-id="9e451-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e451-102">SYNOPSIS</span></span>
<span data-ttu-id="9e451-103">하나 이상의 데이터베이스를 Azure SQL 장애 조치(failover) 그룹에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="9e451-103">Adds one or more databases to an Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="9e451-104">구문</span><span class="sxs-lookup"><span data-stu-id="9e451-104">SYNTAX</span></span>

```
Add-AzSqlDatabaseToFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String>
 -Database <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel]>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9e451-105">설명</span><span class="sxs-lookup"><span data-stu-id="9e451-105">DESCRIPTION</span></span>
<span data-ttu-id="9e451-106">Azure SQL 데이터베이스 장애 조치(failover) 그룹의 주 서버에 하나 이상의 데이터베이스를 해당 장애 조치(failover) 그룹에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="9e451-106">Adds one or more databases on a Azure SQL Database Failover Group's primary server to that Failover Group.</span></span> <span data-ttu-id="9e451-107">데이터베이스는 기존 복제 관계의 보조 데이터베이스가 아니어도 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9e451-107">The databases must not be secondary databases in existing replication relationships.</span></span> <span data-ttu-id="9e451-108">이 명령은 장애 조치(Failover) 그룹의 보조 서버에 추가된 데이터베이스의 지역 복제를 시작하게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9e451-108">The command will start geo-replication of any added databases to the Failover Group's secondary server.</span></span>
<span data-ttu-id="9e451-109">'-Database' 매개 변수를 채울 데이터베이스 개체를 얻습니다. 예를 들어 Get-AzSqlDatabase cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="9e451-109">To obtain database objects with which to populate the '-Database' parameter, use (for example) the Get-AzSqlDatabase cmdlet.</span></span>
<span data-ttu-id="9e451-110">장애 조치 그룹의 주 서버를 사용하여 명령을 실행해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e451-110">The Failover Group's primary server must be used to execute the command.</span></span>

## <span data-ttu-id="9e451-111">예제</span><span class="sxs-lookup"><span data-stu-id="9e451-111">EXAMPLES</span></span>

### <span data-ttu-id="9e451-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="9e451-112">Example 1</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabase -ResourceGroupName rg -ServerName primaryserver -DatabaseName db1 | Add-AzSqlDatabaseToFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
```

<span data-ttu-id="9e451-113">이 명령은 데이터베이스를 파이핑하여 장애 조치(failover) 그룹에 하나의 데이터베이스를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="9e451-113">This command adds one database to a Failover Group by piping it in.</span></span>

### <span data-ttu-id="9e451-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="9e451-114">Example 2</span></span>
```
PS C:\> $primaryServer = Get-AzSqlServer -ResourceGroupName rg -ServerName primaryserver
PS C:\> $failoverGroup = $primaryServer | Add-AzSqlDatabaseToFailoverGroup -FailoverGroupName fg -Database ($primaryServer | Get-AzSqlDatabase)
```

<span data-ttu-id="9e451-115">이 명령은 서버의 모든 데이터베이스를 장애 조치(failover) 그룹에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="9e451-115">This command adds all databases in a server to a Failover Group.</span></span>

### <span data-ttu-id="9e451-116">예제 3</span><span class="sxs-lookup"><span data-stu-id="9e451-116">Example 3</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
PS C:\> $databases = Get-AzSqlElasticPoolDatabase -ResourceGroupName rg -ServerName primaryserver -ElasticPoolName pool1
PS C:\> $failoverGroup = $failoverGroup | Add-AzSqlDatabaseToFailoverGroup -Database $databases
```

<span data-ttu-id="9e451-117">이 명령은 탄력적 풀의 모든 데이터베이스를 장애 조치(failover) 그룹에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="9e451-117">This command adds all databases in an Elastic Pool to a Failover Group.</span></span>

## <span data-ttu-id="9e451-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9e451-118">PARAMETERS</span></span>

### <span data-ttu-id="9e451-119">-Database</span><span class="sxs-lookup"><span data-stu-id="9e451-119">-Database</span></span>
<span data-ttu-id="9e451-120">장애 조치(failover) SQL 주 서버에 있는 하나 이상의 Azure 데이터베이스를 장애 조치(failover) 그룹에 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9e451-120">One or more Azure SQL Databases on the Failover Group's primary server to be added to the Failover Group.</span></span>

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

### <span data-ttu-id="9e451-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e451-121">-DefaultProfile</span></span>
<span data-ttu-id="9e451-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="9e451-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9e451-123">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="9e451-123">-FailoverGroupName</span></span>
<span data-ttu-id="9e451-124">Azure SQL 데이터베이스 장애 조치(failover) 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9e451-124">The name of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="9e451-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e451-125">-ResourceGroupName</span></span>
<span data-ttu-id="9e451-126">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9e451-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="9e451-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="9e451-127">-ServerName</span></span>
<span data-ttu-id="9e451-128">장애 조치 그룹의 기본 Azure SQL 데이터베이스 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9e451-128">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="9e451-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e451-129">CommonParameters</span></span>
<span data-ttu-id="9e451-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9e451-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e451-131">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9e451-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e451-132">입력</span><span class="sxs-lookup"><span data-stu-id="9e451-132">INPUTS</span></span>

### <span data-ttu-id="9e451-133">System.String</span><span class="sxs-lookup"><span data-stu-id="9e451-133">System.String</span></span>

### <span data-ttu-id="9e451-134">System.Collections.Generic.List'1[[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel, Microsoft.Azure.PowerShell.Cmdlets.Sql, Version=1.3.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="9e451-134">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel, Microsoft.Azure.PowerShell.Cmdlets.Sql, Version=1.3.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="9e451-135">출력</span><span class="sxs-lookup"><span data-stu-id="9e451-135">OUTPUTS</span></span>

### <span data-ttu-id="9e451-136">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="9e451-136">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="9e451-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9e451-137">NOTES</span></span>

## <span data-ttu-id="9e451-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9e451-138">RELATED LINKS</span></span>

[<span data-ttu-id="9e451-139">New-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="9e451-139">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="9e451-140">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="9e451-140">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="9e451-141">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="9e451-141">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="9e451-142">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="9e451-142">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="9e451-143">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="9e451-143">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="9e451-144">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="9e451-144">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="9e451-145">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="9e451-145">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
