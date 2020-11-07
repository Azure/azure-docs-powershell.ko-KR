---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/add-azurermsqldatabasetofailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Add-AzureRmSqlDatabaseToFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Add-AzureRmSqlDatabaseToFailoverGroup.md
ms.openlocfilehash: b8e22e9a62fce4549122351d437916de52ba0ade
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703539"
---
# <span data-ttu-id="aa0b4-101">Add-AzureRmSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="aa0b4-101">Add-AzureRmSqlDatabaseToFailoverGroup</span></span>

## <span data-ttu-id="aa0b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aa0b4-102">SYNOPSIS</span></span>
<span data-ttu-id="aa0b4-103">Azure SQL 데이터베이스 장애 조치 (Failover) 그룹에 데이터베이스를 하나 이상 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa0b4-103">Adds one or more databases to an Azure SQL Database Failover Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aa0b4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="aa0b4-104">SYNTAX</span></span>

```
Add-AzureRmSqlDatabaseToFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String>
 -Database <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel]>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aa0b4-105">설명은</span><span class="sxs-lookup"><span data-stu-id="aa0b4-105">DESCRIPTION</span></span>
<span data-ttu-id="aa0b4-106">Azure SQL 데이터베이스 장애 조치 그룹의 주 서버에 있는 하나 이상의 데이터베이스를 해당 장애 조치 그룹에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa0b4-106">Adds one or more databases on a Azure SQL Database Failover Group's primary server to that Failover Group.</span></span> <span data-ttu-id="aa0b4-107">데이터베이스는 기존 복제 관계의 보조 데이터베이스 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa0b4-107">The databases must not be secondary databases in existing replication relationships.</span></span> <span data-ttu-id="aa0b4-108">이 명령은 추가 된 모든 데이터베이스의 지리적 복제를 장애 조치 그룹의 보조 서버로 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa0b4-108">The command will start geo-replication of any added databases to the Failover Group's secondary server.</span></span>

<span data-ttu-id="aa0b4-109">'-Database ' 매개 변수를 채울 데이터베이스 개체를 가져오려면 Get-AzureRmSqlDatabase cmdlet을 사용 합니다 (예:).</span><span class="sxs-lookup"><span data-stu-id="aa0b4-109">To obtain database objects with which to populate the '-Database' parameter, use (for example) the Get-AzureRmSqlDatabase cmdlet.</span></span>

<span data-ttu-id="aa0b4-110">명령 실행을 위해 장애 조치 그룹의 주 서버를 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa0b4-110">The Failover Group's primary server must be used to execute the command.</span></span>

## <span data-ttu-id="aa0b4-111">예제의</span><span class="sxs-lookup"><span data-stu-id="aa0b4-111">EXAMPLES</span></span>

### <span data-ttu-id="aa0b4-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="aa0b4-112">Example 1</span></span>
```
PS C:\> $failoverGroup = Get-AzureRmSqlDatabase -ResourceGroupName rg -ServerName primaryserver -DatabaseName db1 | Add-AzureRmSqlDatabaseToFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
```

<span data-ttu-id="aa0b4-113">이 명령은 데이터베이스를 파이핑 하 여 장애 조치 (Failover) 그룹에 하나를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa0b4-113">This command adds one database to a Failover Group by piping it in.</span></span>

### <span data-ttu-id="aa0b4-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="aa0b4-114">Example 2</span></span>
```
PS C:\> $primaryServer = Get-AzureRmSqlServer -ResourceGroupName rg -ServerName primaryserver
PS C:\> $failoverGroup = $primaryServer | Add-AzureRmSqlDatabaseToFailoverGroup -FailoverGroupName fg -Database ($primaryServer | Get-AzureRmSqlDatabase)
```

<span data-ttu-id="aa0b4-115">이 명령은 서버의 모든 데이터베이스를 장애 조치 (Failover) 그룹에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa0b4-115">This command adds all databases in a server to a Failover Group.</span></span>

### <span data-ttu-id="aa0b4-116">예제 3</span><span class="sxs-lookup"><span data-stu-id="aa0b4-116">Example 3</span></span>
```
PS C:\> $failoverGroup = Get-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
PS C:\> $databases = Get-AzureRmSqlElasticPoolDatabase -ResourceGroupName rg -ServerName primaryserver -ElasticPoolName pool1
PS C:\> $failoverGroup = $failoverGroup | Add-AzureRmSqlDatabaseToFailoverGroup -Database $databases
```

<span data-ttu-id="aa0b4-117">이 명령은 탄력적 풀의 모든 데이터베이스를 장애 조치 (Failover) 그룹에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa0b4-117">This command adds all databases in an Elastic Pool to a Failover Group.</span></span>

## <span data-ttu-id="aa0b4-118">변수</span><span class="sxs-lookup"><span data-stu-id="aa0b4-118">PARAMETERS</span></span>

### <span data-ttu-id="aa0b4-119">-데이터베이스</span><span class="sxs-lookup"><span data-stu-id="aa0b4-119">-Database</span></span>
<span data-ttu-id="aa0b4-120">장애 조치 그룹에 추가 될 장애 조치 그룹의 주 서버에 있는 하나 이상의 Azure SQL 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="aa0b4-120">One or more Azure SQL Databases on the Failover Group's primary server to be added to the Failover Group.</span></span>

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

### <span data-ttu-id="aa0b4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa0b4-121">-DefaultProfile</span></span>
<span data-ttu-id="aa0b4-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="aa0b4-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa0b4-123">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="aa0b4-123">-FailoverGroupName</span></span>
<span data-ttu-id="aa0b4-124">Azure SQL Database 장애 조치 (Failover) 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aa0b4-124">The name of the Azure SQL Database Failover Group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa0b4-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa0b4-125">-ResourceGroupName</span></span>
<span data-ttu-id="aa0b4-126">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aa0b4-126">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa0b4-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="aa0b4-127">-ServerName</span></span>
<span data-ttu-id="aa0b4-128">장애 조치 (Failover) 그룹의 기본 Azure SQL 데이터베이스 서버 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aa0b4-128">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa0b4-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa0b4-129">CommonParameters</span></span>
<span data-ttu-id="aa0b4-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa0b4-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa0b4-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa0b4-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa0b4-132">입력</span><span class="sxs-lookup"><span data-stu-id="aa0b4-132">INPUTS</span></span>

### <span data-ttu-id="aa0b4-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="aa0b4-133">System.String</span></span>
<span data-ttu-id="aa0b4-134">System.webserver. \` \[ \[ AzureSqlDatabaseModel, 2.5.0.0, Microsoft azure. commands, Version =, Culture = 중립, PublicKeyToken = null 인 경우를 목록으로 표시 합니다.\]\]</span><span class="sxs-lookup"><span data-stu-id="aa0b4-134">System.Collections.Generic.List\`1\[\[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel, Microsoft.Azure.Commands.Sql, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null\]\]</span></span>

## <span data-ttu-id="aa0b4-135">출력</span><span class="sxs-lookup"><span data-stu-id="aa0b4-135">OUTPUTS</span></span>

### <span data-ttu-id="aa0b4-136">System. 개체</span><span class="sxs-lookup"><span data-stu-id="aa0b4-136">System.Object</span></span>

## <span data-ttu-id="aa0b4-137">상속자</span><span class="sxs-lookup"><span data-stu-id="aa0b4-137">NOTES</span></span>

## <span data-ttu-id="aa0b4-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="aa0b4-138">RELATED LINKS</span></span>

[<span data-ttu-id="aa0b4-139">새로운 AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="aa0b4-139">New-AzureRmSqlDatabaseFailoverGroup</span></span>](./New-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="aa0b4-140">Set-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="aa0b4-140">Set-AzureRmSqlDatabaseFailoverGroup</span></span>](./Set-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="aa0b4-141">Get-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="aa0b4-141">Get-AzureRmSqlDatabaseFailoverGroup</span></span>](./Get-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="aa0b4-142">제거-AzureRmSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="aa0b4-142">Remove-AzureRmSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="aa0b4-143">스위치-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="aa0b4-143">Switch-AzureRmSqlDatabaseFailoverGroup</span></span>](./Switch-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="aa0b4-144">제거-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="aa0b4-144">Remove-AzureRmSqlDatabaseFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="aa0b4-145">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="aa0b4-145">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
