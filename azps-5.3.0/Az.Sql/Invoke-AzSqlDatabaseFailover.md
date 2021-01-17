---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/invoke-azsqldatabasefailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlDatabaseFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlDatabaseFailover.md
ms.openlocfilehash: e5cd2c2e6e903afd5afeafe2ca5fcdc70551e582
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98374676"
---
# <span data-ttu-id="6deb9-101">Invoke-AzSqlDatabaseFailover</span><span class="sxs-lookup"><span data-stu-id="6deb9-101">Invoke-AzSqlDatabaseFailover</span></span>

## <span data-ttu-id="6deb9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6deb9-102">SYNOPSIS</span></span>
<span data-ttu-id="6deb9-103">데이터베이스를 장애 조치합니다.</span><span class="sxs-lookup"><span data-stu-id="6deb9-103">Failovers a database.</span></span>

## <span data-ttu-id="6deb9-104">구문</span><span class="sxs-lookup"><span data-stu-id="6deb9-104">SYNTAX</span></span>

```
Invoke-AzSqlDatabaseFailover [-DatabaseName] <String> [-ReadableSecondary] [-AsJob] [-PassThru] [-Force]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6deb9-105">설명</span><span class="sxs-lookup"><span data-stu-id="6deb9-105">DESCRIPTION</span></span>
<span data-ttu-id="6deb9-106">Invoke-AzSqlDatabaseFailover cmdlet은 Azure SQL 장애 조치합니다.</span><span class="sxs-lookup"><span data-stu-id="6deb9-106">The Invoke-AzSqlDatabaseFailover cmdlet failovers an Azure SQL database.</span></span> <span data-ttu-id="6deb9-107">데이터베이스가 탄력적 풀에 있는 경우 이 명령은 동일한 탄력적 풀의 다른 데이터베이스에 영향을 주지 않고 주어진 데이터베이스를 장애 조치합니다.</span><span class="sxs-lookup"><span data-stu-id="6deb9-107">If the database is in an elastic pool, this command will failover the given database without affecting the other databases in the same elastic pool.</span></span>

## <span data-ttu-id="6deb9-108">예제</span><span class="sxs-lookup"><span data-stu-id="6deb9-108">EXAMPLES</span></span>

### <span data-ttu-id="6deb9-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="6deb9-109">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSqlDatabaseFailover -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="6deb9-110">이 명령은 "Server01"이라는 서버에서 "Database01"이라는 데이터베이스의 주 복제본을 장애 조치합니다.</span><span class="sxs-lookup"><span data-stu-id="6deb9-110">This command will failover the primary replica of the database named "Database01" on the server named "Server01"</span></span>

### <span data-ttu-id="6deb9-111">예제 2</span><span class="sxs-lookup"><span data-stu-id="6deb9-111">Example 2</span></span>
```powershell
PS C:\> Invoke-AzSqlDatabaseFailover -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -ReadableSecondary
```

<span data-ttu-id="6deb9-112">이 명령은 "Server01"이라는 서버에서 "Database01"이라는 데이터베이스의 읽을 수 있는 보조 복제본을 장애 조치합니다.</span><span class="sxs-lookup"><span data-stu-id="6deb9-112">This command will failover the readable secondary replica of the database named "Database01" on the server named "Server01"</span></span>

## <span data-ttu-id="6deb9-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6deb9-113">PARAMETERS</span></span>

### <span data-ttu-id="6deb9-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6deb9-114">-AsJob</span></span>
<span data-ttu-id="6deb9-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="6deb9-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6deb9-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="6deb9-116">-DatabaseName</span></span>
<span data-ttu-id="6deb9-117">장애 조치할 Azure SQL 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6deb9-117">The name of the Azure SQL Database to failover.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6deb9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6deb9-118">-DefaultProfile</span></span>
<span data-ttu-id="6deb9-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6deb9-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6deb9-120">-Force</span><span class="sxs-lookup"><span data-stu-id="6deb9-120">-Force</span></span>
<span data-ttu-id="6deb9-121">작업을 수행하기 위한 확인 메시지 건너뛰기</span><span class="sxs-lookup"><span data-stu-id="6deb9-121">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="6deb9-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6deb9-122">-PassThru</span></span>
<span data-ttu-id="6deb9-123">성공한 실행 시 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="6deb9-123">On Successful execution, returns true.</span></span>  <span data-ttu-id="6deb9-124">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6deb9-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="6deb9-125">-ReadableSecondary</span><span class="sxs-lookup"><span data-stu-id="6deb9-125">-ReadableSecondary</span></span>
<span data-ttu-id="6deb9-126">기본 주 복제본 대신 읽을 수 있는 보조 복제본 장애 조치(failover)</span><span class="sxs-lookup"><span data-stu-id="6deb9-126">Failover the readable secondary replica instead of the default primary replica</span></span>

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

### <span data-ttu-id="6deb9-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6deb9-127">-ResourceGroupName</span></span>
<span data-ttu-id="6deb9-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6deb9-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="6deb9-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="6deb9-129">-ServerName</span></span>
<span data-ttu-id="6deb9-130">데이터베이스가 있는 Azure SQL 데이터베이스 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6deb9-130">The name of the Azure SQL Database Server the database is in.</span></span>

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

### <span data-ttu-id="6deb9-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6deb9-131">-Confirm</span></span>
<span data-ttu-id="6deb9-132">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="6deb9-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6deb9-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6deb9-133">-WhatIf</span></span>
<span data-ttu-id="6deb9-134">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="6deb9-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6deb9-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6deb9-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6deb9-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6deb9-136">CommonParameters</span></span>
<span data-ttu-id="6deb9-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6deb9-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6deb9-138">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6deb9-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6deb9-139">입력</span><span class="sxs-lookup"><span data-stu-id="6deb9-139">INPUTS</span></span>

### <span data-ttu-id="6deb9-140">System.String</span><span class="sxs-lookup"><span data-stu-id="6deb9-140">System.String</span></span>

## <span data-ttu-id="6deb9-141">출력</span><span class="sxs-lookup"><span data-stu-id="6deb9-141">OUTPUTS</span></span>

## <span data-ttu-id="6deb9-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6deb9-142">NOTES</span></span>

## <span data-ttu-id="6deb9-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6deb9-143">RELATED LINKS</span></span>

[<span data-ttu-id="6deb9-144">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="6deb9-144">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="6deb9-145">Invoke-AzSqlElasticPoolFailover</span><span class="sxs-lookup"><span data-stu-id="6deb9-145">Invoke-AzSqlElasticPoolFailover</span></span>](./Invoke-AzSqlElasticPoolFailover.md)

[<span data-ttu-id="6deb9-146">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="6deb9-146">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="6deb9-147">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="6deb9-147">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="6deb9-148">Resume-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="6deb9-148">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="6deb9-149">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="6deb9-149">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="6deb9-150">Suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="6deb9-150">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="6deb9-151">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="6deb9-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
