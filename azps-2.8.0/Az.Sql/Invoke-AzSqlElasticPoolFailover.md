---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/invoke-azsqlelasticpoolfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlElasticPoolFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlElasticPoolFailover.md
ms.openlocfilehash: c07141d8a91974d511653217885b21a50a0b87f1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873623"
---
# <span data-ttu-id="b33c0-101">Invoke-AzSqlElasticPoolFailover</span><span class="sxs-lookup"><span data-stu-id="b33c0-101">Invoke-AzSqlElasticPoolFailover</span></span>

## <span data-ttu-id="b33c0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b33c0-102">SYNOPSIS</span></span>
<span data-ttu-id="b33c0-103">탄력적 풀을 장애 조치 합니다.</span><span class="sxs-lookup"><span data-stu-id="b33c0-103">Failovers an elastic pool.</span></span>

## <span data-ttu-id="b33c0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b33c0-104">SYNTAX</span></span>

```
Invoke-AzSqlElasticPoolFailover [-ElasticPoolName] <String> [-AsJob] [-PassThru] [-Force]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b33c0-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b33c0-105">DESCRIPTION</span></span>
<span data-ttu-id="b33c0-106">Invoke-AzSqlElasticPoolFailover cmdlet이 탄력적 풀을 장애 조치 합니다.</span><span class="sxs-lookup"><span data-stu-id="b33c0-106">The Invoke-AzSqlElasticPoolFailover cmdlet failovers an elastic pool.</span></span> <span data-ttu-id="b33c0-107">이 cmdlet을 실행 한 후 탄력적 풀의 모든 데이터베이스에서 장애 조치 (Failover)가 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="b33c0-107">Failover will occur on all databases in the elastic pool after running this cmdlet.</span></span>

## <span data-ttu-id="b33c0-108">예제의</span><span class="sxs-lookup"><span data-stu-id="b33c0-108">EXAMPLES</span></span>

### <span data-ttu-id="b33c0-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="b33c0-109">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSqlElasticPoolFailover -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="b33c0-110">이 명령은 "Server01" 서버에서 "ElasticPool01" 이라는 탄력적 풀의 장애 조치를 합니다.</span><span class="sxs-lookup"><span data-stu-id="b33c0-110">This command will failover the elastic pool named "ElasticPool01" on the server named "Server01".</span></span>  <span data-ttu-id="b33c0-111">이는 장애 조치가 "ElasticPool01" 이라는 탄력적 풀의 모든 데이터베이스에서 발생 함을 의미 합니다.</span><span class="sxs-lookup"><span data-stu-id="b33c0-111">This means failover will occur on all databases in the elastic pool named "ElasticPool01".</span></span>

## <span data-ttu-id="b33c0-112">변수</span><span class="sxs-lookup"><span data-stu-id="b33c0-112">PARAMETERS</span></span>

### <span data-ttu-id="b33c0-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b33c0-113">-AsJob</span></span>
<span data-ttu-id="b33c0-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="b33c0-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b33c0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b33c0-115">-DefaultProfile</span></span>
<span data-ttu-id="b33c0-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b33c0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b33c0-117">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="b33c0-117">-ElasticPoolName</span></span>
<span data-ttu-id="b33c0-118">제거할 Azure SQL 탄력적 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b33c0-118">The name of the Azure SQL Elastic Pool to remove.</span></span>

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

### <span data-ttu-id="b33c0-119">-Force</span><span class="sxs-lookup"><span data-stu-id="b33c0-119">-Force</span></span>
<span data-ttu-id="b33c0-120">작업 수행을 위한 확인 메시지 건너뛰기</span><span class="sxs-lookup"><span data-stu-id="b33c0-120">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="b33c0-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b33c0-121">-PassThru</span></span>
<span data-ttu-id="b33c0-122">성공적으로 실행 되 면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b33c0-122">On Successful execution, returns true.</span></span>  <span data-ttu-id="b33c0-123">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b33c0-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b33c0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b33c0-124">-ResourceGroupName</span></span>
<span data-ttu-id="b33c0-125">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b33c0-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="b33c0-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b33c0-126">-ServerName</span></span>
<span data-ttu-id="b33c0-127">탄력적인 풀이 있는 Azure SQL Server의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b33c0-127">The name of the Azure SQL Server the Elastic Pool is in.</span></span>

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

### <span data-ttu-id="b33c0-128">-확인</span><span class="sxs-lookup"><span data-stu-id="b33c0-128">-Confirm</span></span>
<span data-ttu-id="b33c0-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b33c0-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b33c0-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b33c0-130">-WhatIf</span></span>
<span data-ttu-id="b33c0-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b33c0-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b33c0-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b33c0-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b33c0-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b33c0-133">CommonParameters</span></span>
<span data-ttu-id="b33c0-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b33c0-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b33c0-135">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b33c0-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b33c0-136">입력</span><span class="sxs-lookup"><span data-stu-id="b33c0-136">INPUTS</span></span>

### <span data-ttu-id="b33c0-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b33c0-137">System.String</span></span>

## <span data-ttu-id="b33c0-138">출력</span><span class="sxs-lookup"><span data-stu-id="b33c0-138">OUTPUTS</span></span>

## <span data-ttu-id="b33c0-139">상속자</span><span class="sxs-lookup"><span data-stu-id="b33c0-139">NOTES</span></span>

## <span data-ttu-id="b33c0-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b33c0-140">RELATED LINKS</span></span>

[<span data-ttu-id="b33c0-141">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="b33c0-141">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="b33c0-142">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="b33c0-142">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="b33c0-143">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="b33c0-143">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="b33c0-144">AzSqlDatabaseFailover-호출</span><span class="sxs-lookup"><span data-stu-id="b33c0-144">Invoke-AzSqlDatabaseFailover</span></span>](./Invoke-AzSqlDatabaseFailover.md)

[<span data-ttu-id="b33c0-145">새로운 AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="b33c0-145">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="b33c0-146">제거-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="b33c0-146">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="b33c0-147">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="b33c0-147">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)

[<span data-ttu-id="b33c0-148">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="b33c0-148">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)