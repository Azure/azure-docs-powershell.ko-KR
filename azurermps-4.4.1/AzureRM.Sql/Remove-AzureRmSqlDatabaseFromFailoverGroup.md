---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseFromFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseFromFailoverGroup.md
ms.openlocfilehash: b796d1247d1f8a49316431ca944ac6cd1fb77d02
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711768"
---
# <span data-ttu-id="0365d-101">Remove-AzureRmSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="0365d-101">Remove-AzureRmSqlDatabaseFromFailoverGroup</span></span>

## <span data-ttu-id="0365d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0365d-102">SYNOPSIS</span></span>
<span data-ttu-id="0365d-103">Azure SQL 데이터베이스 장애 조치 (Failover) 그룹에서 하나 이상의 데이터베이스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0365d-103">Removes one or more databases from an Azure SQL Database Failover Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0365d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0365d-104">SYNTAX</span></span>

```
Remove-AzureRmSqlDatabaseFromFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String>
 -Database <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel]>
 [-Force] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0365d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0365d-105">DESCRIPTION</span></span>
<span data-ttu-id="0365d-106">지정 된 Azure SQL 데이터베이스 장애 조치 (Failover) 그룹에서 하나 이상의 데이터베이스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0365d-106">Removes one or more databases from the specified Azure SQL Database Failover Group.</span></span> <span data-ttu-id="0365d-107">데이터베이스와 복제 관계는 그대로 유지 되지만 장애 조치 그룹 끝점을 통해 더 이상 액세스할 수 없게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0365d-107">The databases and replication relationships are left intact, but they will no longer be accessible through the Failover Group endpoints.</span></span>

<span data-ttu-id="0365d-108">'-Database ' 매개 변수를 채울 데이터베이스 개체를 가져오려면 Get-AzureRmSqlDatabase cmdlet을 사용 합니다 (예:).</span><span class="sxs-lookup"><span data-stu-id="0365d-108">To obtain database objects with which to populate the '-Database' parameter, use (for example) the Get-AzureRmSqlDatabase cmdlet.</span></span>

<span data-ttu-id="0365d-109">명령 실행을 위해 장애 조치 그룹의 주 서버를 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0365d-109">The Failover Group's primary server must be used to execute the command.</span></span>

## <span data-ttu-id="0365d-110">예제의</span><span class="sxs-lookup"><span data-stu-id="0365d-110">EXAMPLES</span></span>

### <span data-ttu-id="0365d-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="0365d-111">Example 1</span></span>
```
PS C:\> $failoverGroup = Get-AzureRmSqlDatabase -ResourceGroupName rg -ServerName primaryserver -DatabaseName db1 | Remove-AzureRmSqlDatabaseFromFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
```

<span data-ttu-id="0365d-112">이 명령은 한 데이터베이스를 파이핑 하 여 장애 조치 그룹에서 하나를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0365d-112">This command removes one database from a Failover Group by piping it in.</span></span>

### <span data-ttu-id="0365d-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="0365d-113">Example 2</span></span>
```
PS C:\> $primaryServer = Get-AzureRmSqlServer -ResourceGroupName rg -ServerName primaryserver
PS C:\> $failoverGroup = $primaryServer | Remove-AzureRmSqlDatabaseFromFailoverGroup -FailoverGroupName fg -Database ($primaryServer | Get-AzureRmSqlDatabase)
```

<span data-ttu-id="0365d-114">이 명령은 장애 조치 (Failover) 그룹에서 모든 데이터베이스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0365d-114">This command removes all databases from a Failover Group.</span></span>

### <span data-ttu-id="0365d-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="0365d-115">Example 3</span></span>
```
PS C:\> $failoverGroup = Get-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
PS C:\> $databases = Get-AzureRmSqlElasticPoolDatabase -ResourceGroupName rg -ServerName primaryserver -ElasticPoolName pool1
PS C:\> $failoverGroup = $failoverGroup | Remove-AzureRMSqlDatabaseFromFailoverGroup -Database $databases
```

<span data-ttu-id="0365d-116">이 명령은 장애 조치 그룹에서 탄력적 풀의 모든 데이터베이스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0365d-116">This command removes all databases in an Elastic Pool from a Failover Group.</span></span>

## <span data-ttu-id="0365d-117">변수</span><span class="sxs-lookup"><span data-stu-id="0365d-117">PARAMETERS</span></span>

### <span data-ttu-id="0365d-118">-데이터베이스</span><span class="sxs-lookup"><span data-stu-id="0365d-118">-Database</span></span>
<span data-ttu-id="0365d-119">장애 조치 그룹에서 제거할 장애 조치 그룹의 주 서버에 있는 하나 이상의 Azure SQL 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="0365d-119">One or more Azure SQL Databases on the Failover Group's primary server to be removed from the Failover Group.</span></span>

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

### <span data-ttu-id="0365d-120">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="0365d-120">-FailoverGroupName</span></span>
<span data-ttu-id="0365d-121">Azure SQL Database 장애 조치 (Failover) 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0365d-121">The name of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="0365d-122">-Force</span><span class="sxs-lookup"><span data-stu-id="0365d-122">-Force</span></span>
<span data-ttu-id="0365d-123">작업 수행에 대 한 건너뛰기 확인 메시지입니다.</span><span class="sxs-lookup"><span data-stu-id="0365d-123">Skip confirmation message for performing the action.</span></span>

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

### <span data-ttu-id="0365d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0365d-124">-ResourceGroupName</span></span>
<span data-ttu-id="0365d-125">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0365d-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="0365d-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="0365d-126">-ServerName</span></span>
<span data-ttu-id="0365d-127">장애 조치 (Failover) 그룹의 기본 Azure SQL 데이터베이스 서버 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0365d-127">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="0365d-128">-확인</span><span class="sxs-lookup"><span data-stu-id="0365d-128">-Confirm</span></span>
<span data-ttu-id="0365d-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0365d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0365d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0365d-130">-WhatIf</span></span>
<span data-ttu-id="0365d-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0365d-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0365d-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0365d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0365d-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0365d-133">-DefaultProfile</span></span>
<span data-ttu-id="0365d-134">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0365d-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0365d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0365d-135">CommonParameters</span></span>
<span data-ttu-id="0365d-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0365d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0365d-137">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0365d-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0365d-138">입력</span><span class="sxs-lookup"><span data-stu-id="0365d-138">INPUTS</span></span>

### <span data-ttu-id="0365d-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0365d-139">System.String</span></span>
<span data-ttu-id="0365d-140">AzureSqlDatabaseModel, [[Microsoft Azure. 2.5.0.0, Microsoft Azure., Test.sql, Version =, Culture = 중립, PublicKeyToken = null]] 목록의 목록 ' 1 '</span><span class="sxs-lookup"><span data-stu-id="0365d-140">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel, Microsoft.Azure.Commands.Sql, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="0365d-141">출력</span><span class="sxs-lookup"><span data-stu-id="0365d-141">OUTPUTS</span></span>

### <span data-ttu-id="0365d-142">System. 개체</span><span class="sxs-lookup"><span data-stu-id="0365d-142">System.Object</span></span>

## <span data-ttu-id="0365d-143">상속자</span><span class="sxs-lookup"><span data-stu-id="0365d-143">NOTES</span></span>

## <span data-ttu-id="0365d-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0365d-144">RELATED LINKS</span></span>

[<span data-ttu-id="0365d-145">새로운 AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="0365d-145">New-AzureRmSqlDatabaseFailoverGroup</span></span>](./New-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="0365d-146">Set-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="0365d-146">Set-AzureRmSqlDatabaseFailoverGroup</span></span>](./Set-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="0365d-147">Get-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="0365d-147">Get-AzureRmSqlDatabaseFailoverGroup</span></span>](./Get-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="0365d-148">추가-AzureRmSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="0365d-148">Add-AzureRmSqlDatabaseToFailoverGroup</span></span>](./Add-AzureRmSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="0365d-149">스위치-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="0365d-149">Switch-AzureRmSqlDatabaseFailoverGroup</span></span>](./Switch-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="0365d-150">제거-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="0365d-150">Remove-AzureRmSqlDatabaseFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="0365d-151">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="0365d-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
