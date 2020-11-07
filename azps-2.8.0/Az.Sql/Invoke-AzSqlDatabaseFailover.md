---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/invoke-azsqldatabasefailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlDatabaseFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlDatabaseFailover.md
ms.openlocfilehash: 5832b263f87ee0122dbc49c6dc765e7e54287311
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873895"
---
# <span data-ttu-id="863fc-101">Invoke-AzSqlDatabaseFailover</span><span class="sxs-lookup"><span data-stu-id="863fc-101">Invoke-AzSqlDatabaseFailover</span></span>

## <span data-ttu-id="863fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="863fc-102">SYNOPSIS</span></span>
<span data-ttu-id="863fc-103">데이터베이스를 장애 조치 합니다.</span><span class="sxs-lookup"><span data-stu-id="863fc-103">Failovers a database.</span></span>

## <span data-ttu-id="863fc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="863fc-104">SYNTAX</span></span>

```
Invoke-AzSqlDatabaseFailover [-DatabaseName] <String> [-AsJob] [-PassThru] [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="863fc-105">설명은</span><span class="sxs-lookup"><span data-stu-id="863fc-105">DESCRIPTION</span></span>
<span data-ttu-id="863fc-106">Invoke-AzSqlDatabaseFailover cmdlet은 Azure SQL 데이터베이스를 장애 조치 합니다.</span><span class="sxs-lookup"><span data-stu-id="863fc-106">The Invoke-AzSqlDatabaseFailover cmdlet failovers an Azure SQL database.</span></span> <span data-ttu-id="863fc-107">데이터베이스가 탄력적 풀에 있는 경우이 명령을 사용 하면 동일한 탄력적 풀의 다른 데이터베이스에 영향을 주지 않고 지정 된 데이터베이스를 장애 조치 (failover) 합니다.</span><span class="sxs-lookup"><span data-stu-id="863fc-107">If the database is in an elastic pool, this command will failover the given database without affecting the other databases in the same elastic pool.</span></span>

## <span data-ttu-id="863fc-108">예제의</span><span class="sxs-lookup"><span data-stu-id="863fc-108">EXAMPLES</span></span>

### <span data-ttu-id="863fc-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="863fc-109">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSqlDatabaseFailover -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="863fc-110">이 명령은 이름이 "Server01" 인 서버에서 "Database01" 데이터베이스의 장애 조치를 합니다.</span><span class="sxs-lookup"><span data-stu-id="863fc-110">This command will failover the database named "Database01" on the server named "Server01"</span></span>

## <span data-ttu-id="863fc-111">변수</span><span class="sxs-lookup"><span data-stu-id="863fc-111">PARAMETERS</span></span>

### <span data-ttu-id="863fc-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="863fc-112">-AsJob</span></span>
<span data-ttu-id="863fc-113">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="863fc-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="863fc-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="863fc-114">-DatabaseName</span></span>
<span data-ttu-id="863fc-115">장애 조치 (failover) 할 Azure SQL 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="863fc-115">The name of the Azure SQL Database to failover.</span></span>

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

### <span data-ttu-id="863fc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="863fc-116">-DefaultProfile</span></span>
<span data-ttu-id="863fc-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="863fc-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="863fc-118">-Force</span><span class="sxs-lookup"><span data-stu-id="863fc-118">-Force</span></span>
<span data-ttu-id="863fc-119">작업 수행을 위한 확인 메시지 건너뛰기</span><span class="sxs-lookup"><span data-stu-id="863fc-119">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="863fc-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="863fc-120">-PassThru</span></span>
<span data-ttu-id="863fc-121">성공적으로 실행 되 면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="863fc-121">On Successful execution, returns true.</span></span>  <span data-ttu-id="863fc-122">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="863fc-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="863fc-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="863fc-123">-ResourceGroupName</span></span>
<span data-ttu-id="863fc-124">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="863fc-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="863fc-125">-ServerName</span><span class="sxs-lookup"><span data-stu-id="863fc-125">-ServerName</span></span>
<span data-ttu-id="863fc-126">데이터베이스가 있는 Azure SQL 데이터베이스 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="863fc-126">The name of the Azure SQL Database Server the database is in.</span></span>

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

### <span data-ttu-id="863fc-127">-확인</span><span class="sxs-lookup"><span data-stu-id="863fc-127">-Confirm</span></span>
<span data-ttu-id="863fc-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="863fc-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="863fc-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="863fc-129">-WhatIf</span></span>
<span data-ttu-id="863fc-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="863fc-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="863fc-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="863fc-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="863fc-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="863fc-132">CommonParameters</span></span>
<span data-ttu-id="863fc-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="863fc-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="863fc-134">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="863fc-134">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="863fc-135">입력</span><span class="sxs-lookup"><span data-stu-id="863fc-135">INPUTS</span></span>

### <span data-ttu-id="863fc-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="863fc-136">System.String</span></span>

## <span data-ttu-id="863fc-137">출력</span><span class="sxs-lookup"><span data-stu-id="863fc-137">OUTPUTS</span></span>

## <span data-ttu-id="863fc-138">상속자</span><span class="sxs-lookup"><span data-stu-id="863fc-138">NOTES</span></span>

## <span data-ttu-id="863fc-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="863fc-139">RELATED LINKS</span></span>

[<span data-ttu-id="863fc-140">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="863fc-140">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="863fc-141">AzSqlElasticPoolFailover-호출</span><span class="sxs-lookup"><span data-stu-id="863fc-141">Invoke-AzSqlElasticPoolFailover</span></span>](./Invoke-AzSqlElasticPoolFailover.md)

[<span data-ttu-id="863fc-142">새로운 AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="863fc-142">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="863fc-143">제거-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="863fc-143">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="863fc-144">이력서-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="863fc-144">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="863fc-145">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="863fc-145">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="863fc-146">일시 중단-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="863fc-146">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="863fc-147">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="863fc-147">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
