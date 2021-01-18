---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/invoke-azsqlelasticpoolfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlElasticPoolFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlElasticPoolFailover.md
ms.openlocfilehash: 631a8edcc3709e80b36a3ff8661b7ea6027b9f78
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494715"
---
# <span data-ttu-id="2f6f3-101">Invoke-AzSqlElasticPoolFailover</span><span class="sxs-lookup"><span data-stu-id="2f6f3-101">Invoke-AzSqlElasticPoolFailover</span></span>

## <span data-ttu-id="2f6f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2f6f3-102">SYNOPSIS</span></span>
<span data-ttu-id="2f6f3-103">탄력적 풀을 장애 조치합니다.</span><span class="sxs-lookup"><span data-stu-id="2f6f3-103">Failovers an elastic pool.</span></span>

## <span data-ttu-id="2f6f3-104">구문</span><span class="sxs-lookup"><span data-stu-id="2f6f3-104">SYNTAX</span></span>

```
Invoke-AzSqlElasticPoolFailover [-ElasticPoolName] <String> [-AsJob] [-PassThru] [-Force]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f6f3-105">설명</span><span class="sxs-lookup"><span data-stu-id="2f6f3-105">DESCRIPTION</span></span>
<span data-ttu-id="2f6f3-106">Invoke-AzSqlElasticPoolFailover cmdlet은 탄력적 풀을 장애 조치합니다.</span><span class="sxs-lookup"><span data-stu-id="2f6f3-106">The Invoke-AzSqlElasticPoolFailover cmdlet failovers an elastic pool.</span></span> <span data-ttu-id="2f6f3-107">장애 조치는 이 cmdlet을 실행한 후 탄력적 풀의 모든 데이터베이스에서 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="2f6f3-107">Failover will occur on all databases in the elastic pool after running this cmdlet.</span></span>

## <span data-ttu-id="2f6f3-108">예제</span><span class="sxs-lookup"><span data-stu-id="2f6f3-108">EXAMPLES</span></span>

### <span data-ttu-id="2f6f3-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="2f6f3-109">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSqlElasticPoolFailover -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="2f6f3-110">이 명령은 "Server01"이라는 서버에서 "ElasticPool01"이라는 탄력적 풀을 장애 조치합니다.</span><span class="sxs-lookup"><span data-stu-id="2f6f3-110">This command will failover the elastic pool named "ElasticPool01" on the server named "Server01".</span></span>  <span data-ttu-id="2f6f3-111">즉, "ElasticPool01"이라는 탄력적 풀의 모든 데이터베이스에서 장애 조치(failover)가 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="2f6f3-111">This means failover will occur on all databases in the elastic pool named "ElasticPool01".</span></span>

## <span data-ttu-id="2f6f3-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2f6f3-112">PARAMETERS</span></span>

### <span data-ttu-id="2f6f3-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2f6f3-113">-AsJob</span></span>
<span data-ttu-id="2f6f3-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="2f6f3-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2f6f3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f6f3-115">-DefaultProfile</span></span>
<span data-ttu-id="2f6f3-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2f6f3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f6f3-117">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="2f6f3-117">-ElasticPoolName</span></span>
<span data-ttu-id="2f6f3-118">제거할 Azure SQL 탄력적 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2f6f3-118">The name of the Azure SQL Elastic Pool to remove.</span></span>

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

### <span data-ttu-id="2f6f3-119">-Force</span><span class="sxs-lookup"><span data-stu-id="2f6f3-119">-Force</span></span>
<span data-ttu-id="2f6f3-120">작업을 수행하기 위한 확인 메시지 건너뛰기</span><span class="sxs-lookup"><span data-stu-id="2f6f3-120">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="2f6f3-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2f6f3-121">-PassThru</span></span>
<span data-ttu-id="2f6f3-122">성공한 실행 시 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="2f6f3-122">On Successful execution, returns true.</span></span>  <span data-ttu-id="2f6f3-123">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2f6f3-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2f6f3-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f6f3-124">-ResourceGroupName</span></span>
<span data-ttu-id="2f6f3-125">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2f6f3-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="2f6f3-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="2f6f3-126">-ServerName</span></span>
<span data-ttu-id="2f6f3-127">탄력적 풀이 SQL Server Azure 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2f6f3-127">The name of the Azure SQL Server the Elastic Pool is in.</span></span>

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

### <span data-ttu-id="2f6f3-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2f6f3-128">-Confirm</span></span>
<span data-ttu-id="2f6f3-129">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="2f6f3-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f6f3-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f6f3-130">-WhatIf</span></span>
<span data-ttu-id="2f6f3-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="2f6f3-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2f6f3-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2f6f3-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f6f3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f6f3-133">CommonParameters</span></span>
<span data-ttu-id="2f6f3-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2f6f3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f6f3-135">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2f6f3-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f6f3-136">입력</span><span class="sxs-lookup"><span data-stu-id="2f6f3-136">INPUTS</span></span>

### <span data-ttu-id="2f6f3-137">System.String</span><span class="sxs-lookup"><span data-stu-id="2f6f3-137">System.String</span></span>

## <span data-ttu-id="2f6f3-138">출력</span><span class="sxs-lookup"><span data-stu-id="2f6f3-138">OUTPUTS</span></span>

## <span data-ttu-id="2f6f3-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2f6f3-139">NOTES</span></span>

## <span data-ttu-id="2f6f3-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2f6f3-140">RELATED LINKS</span></span>

[<span data-ttu-id="2f6f3-141">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="2f6f3-141">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="2f6f3-142">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="2f6f3-142">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="2f6f3-143">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="2f6f3-143">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="2f6f3-144">Invoke-AzSqlDatabaseFailover</span><span class="sxs-lookup"><span data-stu-id="2f6f3-144">Invoke-AzSqlDatabaseFailover</span></span>](./Invoke-AzSqlDatabaseFailover.md)

[<span data-ttu-id="2f6f3-145">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="2f6f3-145">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="2f6f3-146">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="2f6f3-146">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="2f6f3-147">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="2f6f3-147">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)

[<span data-ttu-id="2f6f3-148">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="2f6f3-148">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)