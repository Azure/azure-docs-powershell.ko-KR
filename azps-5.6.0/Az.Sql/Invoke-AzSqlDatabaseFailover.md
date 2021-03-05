---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/invoke-azsqldatabasefailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlDatabaseFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlDatabaseFailover.md
ms.openlocfilehash: 23df8f00c91cfabf4ad01b5dd641069f159eb064
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987541"
---
# <span data-ttu-id="f1ba1-101">Invoke-AzSqlDatabaseFailover</span><span class="sxs-lookup"><span data-stu-id="f1ba1-101">Invoke-AzSqlDatabaseFailover</span></span>

## <span data-ttu-id="f1ba1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1ba1-102">SYNOPSIS</span></span>
<span data-ttu-id="f1ba1-103">데이터베이스를 장애 조치(Failover)합니다.</span><span class="sxs-lookup"><span data-stu-id="f1ba1-103">Failovers a database.</span></span>

## <span data-ttu-id="f1ba1-104">구문</span><span class="sxs-lookup"><span data-stu-id="f1ba1-104">SYNTAX</span></span>

```
Invoke-AzSqlDatabaseFailover [-DatabaseName] <String> [-ReadableSecondary] [-AsJob] [-PassThru] [-Force]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1ba1-105">설명</span><span class="sxs-lookup"><span data-stu-id="f1ba1-105">DESCRIPTION</span></span>
<span data-ttu-id="f1ba1-106">Invoke-AzSqlDatabaseFailover cmdlet은 Azure SQL 장애 조치(failover)합니다.</span><span class="sxs-lookup"><span data-stu-id="f1ba1-106">The Invoke-AzSqlDatabaseFailover cmdlet failovers an Azure SQL database.</span></span> <span data-ttu-id="f1ba1-107">데이터베이스가 탄력적 풀에 있는 경우 이 명령은 동일한 탄력적 풀의 다른 데이터베이스에 영향을 주지 않고 주어진 데이터베이스를 장애 조치(failover)합니다.</span><span class="sxs-lookup"><span data-stu-id="f1ba1-107">If the database is in an elastic pool, this command will failover the given database without affecting the other databases in the same elastic pool.</span></span>

## <span data-ttu-id="f1ba1-108">예제</span><span class="sxs-lookup"><span data-stu-id="f1ba1-108">EXAMPLES</span></span>

### <span data-ttu-id="f1ba1-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="f1ba1-109">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSqlDatabaseFailover -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="f1ba1-110">이 명령은 "Server01"이라는 서버에서 "Database01"이라는 데이터베이스의 기본 복제본을 장애 조치합니다.</span><span class="sxs-lookup"><span data-stu-id="f1ba1-110">This command will failover the primary replica of the database named "Database01" on the server named "Server01"</span></span>

### <span data-ttu-id="f1ba1-111">예제 2</span><span class="sxs-lookup"><span data-stu-id="f1ba1-111">Example 2</span></span>
```powershell
PS C:\> Invoke-AzSqlDatabaseFailover -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -ReadableSecondary
```

<span data-ttu-id="f1ba1-112">이 명령은 "Server01"이라는 서버에서 "Database01"이라는 데이터베이스의 읽을 수 있는 보조 복제본을 장애 조치합니다.</span><span class="sxs-lookup"><span data-stu-id="f1ba1-112">This command will failover the readable secondary replica of the database named "Database01" on the server named "Server01"</span></span>

## <span data-ttu-id="f1ba1-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="f1ba1-113">PARAMETERS</span></span>

### <span data-ttu-id="f1ba1-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f1ba1-114">-AsJob</span></span>
<span data-ttu-id="f1ba1-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="f1ba1-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f1ba1-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f1ba1-116">-DatabaseName</span></span>
<span data-ttu-id="f1ba1-117">Azure 데이터베이스의 SQL 장애 조치(failover)를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f1ba1-117">The name of the Azure SQL Database to failover.</span></span>

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

### <span data-ttu-id="f1ba1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1ba1-118">-DefaultProfile</span></span>
<span data-ttu-id="f1ba1-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f1ba1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1ba1-120">-Force</span><span class="sxs-lookup"><span data-stu-id="f1ba1-120">-Force</span></span>
<span data-ttu-id="f1ba1-121">작업을 수행하기 위한 확인 메시지 건너뛰기</span><span class="sxs-lookup"><span data-stu-id="f1ba1-121">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="f1ba1-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f1ba1-122">-PassThru</span></span>
<span data-ttu-id="f1ba1-123">성공적인 실행에서 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="f1ba1-123">On Successful execution, returns true.</span></span>  <span data-ttu-id="f1ba1-124">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f1ba1-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f1ba1-125">-ReadableSecondary</span><span class="sxs-lookup"><span data-stu-id="f1ba1-125">-ReadableSecondary</span></span>
<span data-ttu-id="f1ba1-126">기본 주 복제본 대신 읽을 수 있는 보조 복제본 장애 조치(Failover)</span><span class="sxs-lookup"><span data-stu-id="f1ba1-126">Failover the readable secondary replica instead of the default primary replica</span></span>

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

### <span data-ttu-id="f1ba1-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1ba1-127">-ResourceGroupName</span></span>
<span data-ttu-id="f1ba1-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f1ba1-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="f1ba1-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f1ba1-129">-ServerName</span></span>
<span data-ttu-id="f1ba1-130">데이터베이스가 있는 Azure SQL 데이터베이스 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f1ba1-130">The name of the Azure SQL Database Server the database is in.</span></span>

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

### <span data-ttu-id="f1ba1-131">-확인</span><span class="sxs-lookup"><span data-stu-id="f1ba1-131">-Confirm</span></span>
<span data-ttu-id="f1ba1-132">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f1ba1-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1ba1-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1ba1-133">-WhatIf</span></span>
<span data-ttu-id="f1ba1-134">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="f1ba1-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f1ba1-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f1ba1-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1ba1-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1ba1-136">CommonParameters</span></span>
<span data-ttu-id="f1ba1-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f1ba1-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1ba1-138">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f1ba1-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1ba1-139">입력</span><span class="sxs-lookup"><span data-stu-id="f1ba1-139">INPUTS</span></span>

### <span data-ttu-id="f1ba1-140">System.String</span><span class="sxs-lookup"><span data-stu-id="f1ba1-140">System.String</span></span>

## <span data-ttu-id="f1ba1-141">출력</span><span class="sxs-lookup"><span data-stu-id="f1ba1-141">OUTPUTS</span></span>

## <span data-ttu-id="f1ba1-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f1ba1-142">NOTES</span></span>

## <span data-ttu-id="f1ba1-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f1ba1-143">RELATED LINKS</span></span>

[<span data-ttu-id="f1ba1-144">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f1ba1-144">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="f1ba1-145">Invoke-AzSqlElasticPoolFailover</span><span class="sxs-lookup"><span data-stu-id="f1ba1-145">Invoke-AzSqlElasticPoolFailover</span></span>](./Invoke-AzSqlElasticPoolFailover.md)

[<span data-ttu-id="f1ba1-146">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f1ba1-146">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="f1ba1-147">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f1ba1-147">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="f1ba1-148">Resume-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f1ba1-148">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="f1ba1-149">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f1ba1-149">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="f1ba1-150">suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f1ba1-150">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="f1ba1-151">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="f1ba1-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
