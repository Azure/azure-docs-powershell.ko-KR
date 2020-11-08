---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/add-azsqldatabasetofailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlDatabaseToFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlDatabaseToFailoverGroup.md
ms.openlocfilehash: 7577809134987bd1a0092e28170d5bf25ccac04e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034739"
---
# <span data-ttu-id="9e833-101">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="9e833-101">Add-AzSqlDatabaseToFailoverGroup</span></span>

## <span data-ttu-id="9e833-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e833-102">SYNOPSIS</span></span>
<span data-ttu-id="9e833-103">Azure SQL 데이터베이스 장애 조치 (Failover) 그룹에 데이터베이스를 하나 이상 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e833-103">Adds one or more databases to an Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="9e833-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9e833-104">SYNTAX</span></span>

```
Add-AzSqlDatabaseToFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String>
 -Database <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel]>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9e833-105">설명은</span><span class="sxs-lookup"><span data-stu-id="9e833-105">DESCRIPTION</span></span>
<span data-ttu-id="9e833-106">Azure SQL 데이터베이스 장애 조치 그룹의 주 서버에 있는 하나 이상의 데이터베이스를 해당 장애 조치 그룹에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e833-106">Adds one or more databases on a Azure SQL Database Failover Group's primary server to that Failover Group.</span></span> <span data-ttu-id="9e833-107">데이터베이스는 기존 복제 관계의 보조 데이터베이스 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e833-107">The databases must not be secondary databases in existing replication relationships.</span></span> <span data-ttu-id="9e833-108">이 명령은 추가 된 모든 데이터베이스의 지리적 복제를 장애 조치 그룹의 보조 서버로 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e833-108">The command will start geo-replication of any added databases to the Failover Group's secondary server.</span></span>
<span data-ttu-id="9e833-109">'-Database ' 매개 변수를 채울 데이터베이스 개체를 가져오려면 Get-AzSqlDatabase cmdlet을 사용 합니다 (예:).</span><span class="sxs-lookup"><span data-stu-id="9e833-109">To obtain database objects with which to populate the '-Database' parameter, use (for example) the Get-AzSqlDatabase cmdlet.</span></span>
<span data-ttu-id="9e833-110">명령 실행을 위해 장애 조치 그룹의 주 서버를 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e833-110">The Failover Group's primary server must be used to execute the command.</span></span>

## <span data-ttu-id="9e833-111">예제의</span><span class="sxs-lookup"><span data-stu-id="9e833-111">EXAMPLES</span></span>

### <span data-ttu-id="9e833-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="9e833-112">Example 1</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabase -ResourceGroupName rg -ServerName primaryserver -DatabaseName db1 | Add-AzSqlDatabaseToFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
```

<span data-ttu-id="9e833-113">이 명령은 데이터베이스를 파이핑 하 여 장애 조치 (Failover) 그룹에 하나를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e833-113">This command adds one database to a Failover Group by piping it in.</span></span>

### <span data-ttu-id="9e833-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="9e833-114">Example 2</span></span>
```
PS C:\> $primaryServer = Get-AzSqlServer -ResourceGroupName rg -ServerName primaryserver
PS C:\> $failoverGroup = $primaryServer | Add-AzSqlDatabaseToFailoverGroup -FailoverGroupName fg -Database ($primaryServer | Get-AzSqlDatabase)
```

<span data-ttu-id="9e833-115">이 명령은 서버의 모든 데이터베이스를 장애 조치 (Failover) 그룹에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e833-115">This command adds all databases in a server to a Failover Group.</span></span>

### <span data-ttu-id="9e833-116">예제 3</span><span class="sxs-lookup"><span data-stu-id="9e833-116">Example 3</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
PS C:\> $databases = Get-AzSqlElasticPoolDatabase -ResourceGroupName rg -ServerName primaryserver -ElasticPoolName pool1
PS C:\> $failoverGroup = $failoverGroup | Add-AzSqlDatabaseToFailoverGroup -Database $databases
```

<span data-ttu-id="9e833-117">이 명령은 탄력적 풀의 모든 데이터베이스를 장애 조치 (Failover) 그룹에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e833-117">This command adds all databases in an Elastic Pool to a Failover Group.</span></span>

## <span data-ttu-id="9e833-118">변수</span><span class="sxs-lookup"><span data-stu-id="9e833-118">PARAMETERS</span></span>

### <span data-ttu-id="9e833-119">-데이터베이스</span><span class="sxs-lookup"><span data-stu-id="9e833-119">-Database</span></span>
<span data-ttu-id="9e833-120">장애 조치 그룹에 추가 될 장애 조치 그룹의 주 서버에 있는 하나 이상의 Azure SQL 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="9e833-120">One or more Azure SQL Databases on the Failover Group's primary server to be added to the Failover Group.</span></span>

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

### <span data-ttu-id="9e833-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e833-121">-DefaultProfile</span></span>
<span data-ttu-id="9e833-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="9e833-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9e833-123">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="9e833-123">-FailoverGroupName</span></span>
<span data-ttu-id="9e833-124">Azure SQL Database 장애 조치 (Failover) 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9e833-124">The name of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="9e833-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e833-125">-ResourceGroupName</span></span>
<span data-ttu-id="9e833-126">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9e833-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="9e833-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="9e833-127">-ServerName</span></span>
<span data-ttu-id="9e833-128">장애 조치 (Failover) 그룹의 기본 Azure SQL 데이터베이스 서버 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9e833-128">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="9e833-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e833-129">CommonParameters</span></span>
<span data-ttu-id="9e833-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e833-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e833-131">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9e833-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e833-132">입력</span><span class="sxs-lookup"><span data-stu-id="9e833-132">INPUTS</span></span>

### <span data-ttu-id="9e833-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9e833-133">System.String</span></span>

### <span data-ttu-id="9e833-134">AzureSqlDatabaseModel, [[Microsoft Azure. 1.3.0.0, Microsoft Azure. PowerShell., Culture = 중립, PublicKeyToken = null]] 목록에 List ' 1 '이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9e833-134">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel, Microsoft.Azure.PowerShell.Cmdlets.Sql, Version=1.3.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="9e833-135">출력</span><span class="sxs-lookup"><span data-stu-id="9e833-135">OUTPUTS</span></span>

### <span data-ttu-id="9e833-136">AzureSqlFailoverGroupModel (\*. \*.)</span><span class="sxs-lookup"><span data-stu-id="9e833-136">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="9e833-137">상속자</span><span class="sxs-lookup"><span data-stu-id="9e833-137">NOTES</span></span>

## <span data-ttu-id="9e833-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9e833-138">RELATED LINKS</span></span>

[<span data-ttu-id="9e833-139">새로운 AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="9e833-139">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="9e833-140">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="9e833-140">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="9e833-141">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="9e833-141">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="9e833-142">제거-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="9e833-142">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="9e833-143">스위치-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="9e833-143">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="9e833-144">제거-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="9e833-144">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="9e833-145">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="9e833-145">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
