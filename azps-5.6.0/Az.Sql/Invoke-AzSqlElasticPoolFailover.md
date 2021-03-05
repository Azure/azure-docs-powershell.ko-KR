---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/invoke-azsqlelasticpoolfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlElasticPoolFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlElasticPoolFailover.md
ms.openlocfilehash: 0af12c967dbbc65b37619ed837da1b8f778ab1db
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101977739"
---
# <span data-ttu-id="ccf2d-101">Invoke-AzSqlElasticPoolFailover</span><span class="sxs-lookup"><span data-stu-id="ccf2d-101">Invoke-AzSqlElasticPoolFailover</span></span>

## <span data-ttu-id="ccf2d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ccf2d-102">SYNOPSIS</span></span>
<span data-ttu-id="ccf2d-103">탄력적 풀을 장애 조치(failover)합니다.</span><span class="sxs-lookup"><span data-stu-id="ccf2d-103">Failovers an elastic pool.</span></span>

## <span data-ttu-id="ccf2d-104">구문</span><span class="sxs-lookup"><span data-stu-id="ccf2d-104">SYNTAX</span></span>

```
Invoke-AzSqlElasticPoolFailover [-ElasticPoolName] <String> [-AsJob] [-PassThru] [-Force]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ccf2d-105">설명</span><span class="sxs-lookup"><span data-stu-id="ccf2d-105">DESCRIPTION</span></span>
<span data-ttu-id="ccf2d-106">Invoke-AzSqlElasticPoolFailover cmdlet 장애 조치(failover)는 탄력적 풀입니다.</span><span class="sxs-lookup"><span data-stu-id="ccf2d-106">The Invoke-AzSqlElasticPoolFailover cmdlet failovers an elastic pool.</span></span> <span data-ttu-id="ccf2d-107">장애 조치(Failover)는 이 cmdlet을 실행한 후 탄력적 풀의 모든 데이터베이스에 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="ccf2d-107">Failover will occur on all databases in the elastic pool after running this cmdlet.</span></span>

## <span data-ttu-id="ccf2d-108">예제</span><span class="sxs-lookup"><span data-stu-id="ccf2d-108">EXAMPLES</span></span>

### <span data-ttu-id="ccf2d-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="ccf2d-109">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSqlElasticPoolFailover -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="ccf2d-110">이 명령은 "Server01"이라는 서버에서 "ElasticPool01"이라는 탄력적 풀을 장애 조치합니다.</span><span class="sxs-lookup"><span data-stu-id="ccf2d-110">This command will failover the elastic pool named "ElasticPool01" on the server named "Server01".</span></span>  <span data-ttu-id="ccf2d-111">즉, "ElasticPool01"이라는 탄력적 풀의 모든 데이터베이스에 장애 조치(failover)가 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="ccf2d-111">This means failover will occur on all databases in the elastic pool named "ElasticPool01".</span></span>

## <span data-ttu-id="ccf2d-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="ccf2d-112">PARAMETERS</span></span>

### <span data-ttu-id="ccf2d-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ccf2d-113">-AsJob</span></span>
<span data-ttu-id="ccf2d-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="ccf2d-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ccf2d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccf2d-115">-DefaultProfile</span></span>
<span data-ttu-id="ccf2d-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ccf2d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ccf2d-117">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="ccf2d-117">-ElasticPoolName</span></span>
<span data-ttu-id="ccf2d-118">Azure의 이름은 제거할 SQL 탄력적 풀입니다.</span><span class="sxs-lookup"><span data-stu-id="ccf2d-118">The name of the Azure SQL Elastic Pool to remove.</span></span>

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

### <span data-ttu-id="ccf2d-119">-Force</span><span class="sxs-lookup"><span data-stu-id="ccf2d-119">-Force</span></span>
<span data-ttu-id="ccf2d-120">작업을 수행하기 위한 확인 메시지 건너뛰기</span><span class="sxs-lookup"><span data-stu-id="ccf2d-120">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="ccf2d-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ccf2d-121">-PassThru</span></span>
<span data-ttu-id="ccf2d-122">성공적인 실행에서 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="ccf2d-122">On Successful execution, returns true.</span></span>  <span data-ttu-id="ccf2d-123">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ccf2d-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ccf2d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ccf2d-124">-ResourceGroupName</span></span>
<span data-ttu-id="ccf2d-125">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ccf2d-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="ccf2d-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ccf2d-126">-ServerName</span></span>
<span data-ttu-id="ccf2d-127">탄력적 풀에 SQL Server Azure 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ccf2d-127">The name of the Azure SQL Server the Elastic Pool is in.</span></span>

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

### <span data-ttu-id="ccf2d-128">-확인</span><span class="sxs-lookup"><span data-stu-id="ccf2d-128">-Confirm</span></span>
<span data-ttu-id="ccf2d-129">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ccf2d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ccf2d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ccf2d-130">-WhatIf</span></span>
<span data-ttu-id="ccf2d-131">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="ccf2d-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ccf2d-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ccf2d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ccf2d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccf2d-133">CommonParameters</span></span>
<span data-ttu-id="ccf2d-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ccf2d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccf2d-135">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ccf2d-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccf2d-136">입력</span><span class="sxs-lookup"><span data-stu-id="ccf2d-136">INPUTS</span></span>

### <span data-ttu-id="ccf2d-137">System.String</span><span class="sxs-lookup"><span data-stu-id="ccf2d-137">System.String</span></span>

## <span data-ttu-id="ccf2d-138">출력</span><span class="sxs-lookup"><span data-stu-id="ccf2d-138">OUTPUTS</span></span>

## <span data-ttu-id="ccf2d-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ccf2d-139">NOTES</span></span>

## <span data-ttu-id="ccf2d-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ccf2d-140">RELATED LINKS</span></span>

[<span data-ttu-id="ccf2d-141">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="ccf2d-141">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="ccf2d-142">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="ccf2d-142">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="ccf2d-143">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="ccf2d-143">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="ccf2d-144">Invoke-AzSqlDatabaseFailover</span><span class="sxs-lookup"><span data-stu-id="ccf2d-144">Invoke-AzSqlDatabaseFailover</span></span>](./Invoke-AzSqlDatabaseFailover.md)

[<span data-ttu-id="ccf2d-145">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="ccf2d-145">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="ccf2d-146">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="ccf2d-146">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="ccf2d-147">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="ccf2d-147">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)

[<span data-ttu-id="ccf2d-148">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="ccf2d-148">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)