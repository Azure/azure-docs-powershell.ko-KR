---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: F9703508-DD4D-4D25-A7CA-7E3432B5DCA9
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseSecondary.md
ms.openlocfilehash: d713675e3e73f32a4579d801a4dc1577cebd4cf0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98354741"
---
# <span data-ttu-id="46d9a-101">Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="46d9a-101">Set-AzSqlDatabaseSecondary</span></span>

## <span data-ttu-id="46d9a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46d9a-102">SYNOPSIS</span></span>
<span data-ttu-id="46d9a-103">장애 조치(failover)를 시작하려면 보조 데이터베이스를 주 데이터베이스로 전환합니다.</span><span class="sxs-lookup"><span data-stu-id="46d9a-103">Switches a secondary database to be primary in order to initiate failover.</span></span>

## <span data-ttu-id="46d9a-104">구문</span><span class="sxs-lookup"><span data-stu-id="46d9a-104">SYNTAX</span></span>

### <span data-ttu-id="46d9a-105">NoOptionsSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="46d9a-105">NoOptionsSet (Default)</span></span>
```
Set-AzSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String> [-AsJob]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46d9a-106">ByFailoverParams</span><span class="sxs-lookup"><span data-stu-id="46d9a-106">ByFailoverParams</span></span>
```
Set-AzSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String> [-Failover]
 [-AllowDataLoss] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46d9a-107">설명</span><span class="sxs-lookup"><span data-stu-id="46d9a-107">DESCRIPTION</span></span>
<span data-ttu-id="46d9a-108">**Set-AzSqlDatabaseSecondary** cmdlet은 장애 조치(failover)를 시작하려면 보조 데이터베이스를 주 데이터베이스로 전환합니다.</span><span class="sxs-lookup"><span data-stu-id="46d9a-108">The **Set-AzSqlDatabaseSecondary** cmdlet switches a secondary database to be primary in order to initiate failover.</span></span>
<span data-ttu-id="46d9a-109">이 cmdlet은 일반 구성 명령으로 설계되지만 현재 장애 조치(failover) 시작으로 제한됩니다.</span><span class="sxs-lookup"><span data-stu-id="46d9a-109">This cmdlet is designed as a general configuration command, but is currently limited to initiating failover.</span></span>
<span data-ttu-id="46d9a-110">*AllowDataLoss* 매개 변수를 지정하여 정전 중에 강제 장애 조치(failover)를 시작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="46d9a-110">Specify the *AllowDataLoss* parameter to initiate a force failover during an outage.</span></span>
<span data-ttu-id="46d9a-111">복구 훈련과 같은 계획된 작업을 수행할 때 이 매개 변수를 지정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="46d9a-111">You do not have to specify this parameter when you perform a planned operation, such as recovery drill.</span></span>
<span data-ttu-id="46d9a-112">후자의 경우 보조 데이터베이스는 전환되기 전에 주 데이터베이스와 동기화됩니다.</span><span class="sxs-lookup"><span data-stu-id="46d9a-112">In the latter case, the secondary database is synchronized with the primary before it is switched.</span></span>

## <span data-ttu-id="46d9a-113">예제</span><span class="sxs-lookup"><span data-stu-id="46d9a-113">EXAMPLES</span></span>

### <span data-ttu-id="46d9a-114">예제 1: 계획된 장애 조치 시작</span><span class="sxs-lookup"><span data-stu-id="46d9a-114">Example 1: Initiate a planned failover</span></span>
```powershell
$database = Get-AzSqlDatabase -DatabaseName $databaseName -ResourceGroupName $secondaryResourceGroupName -ServerName $secondaryServerName
$database | Set-AzSqlDatabaseSecondary -PartnerResourceGroupName $primaryResourceGroupName -Failover
```

### <span data-ttu-id="46d9a-115">예제 2: 강제 장애 조치(failover) 시작(데이터 손실 가능성이 있는 경우)</span><span class="sxs-lookup"><span data-stu-id="46d9a-115">Example 2: Initiate a forced failover (with potential data loss)</span></span>
```powershell
$database = Get-AzSqlDatabase -DatabaseName $databaseName -ResourceGroupName $secondaryResourceGroupName -ServerName $secondaryServerName
$database | Set-AzSqlDatabaseSecondary -PartnerResourceGroupName $primaryResourceGroupName -Failover -AllowDataLoss
```

## <span data-ttu-id="46d9a-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="46d9a-116">PARAMETERS</span></span>

### <span data-ttu-id="46d9a-117">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="46d9a-117">-AllowDataLoss</span></span>
<span data-ttu-id="46d9a-118">이 장애 조치(failover) 작업이 데이터 손실을 허용하는지 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="46d9a-118">Indicates that this failover operation permits data loss.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByFailoverParams
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46d9a-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="46d9a-119">-AsJob</span></span>
<span data-ttu-id="46d9a-120">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="46d9a-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="46d9a-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="46d9a-121">-DatabaseName</span></span>
<span data-ttu-id="46d9a-122">Azure SQL Database Secondary의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="46d9a-122">Specifies the name of the Azure SQL Database Secondary.</span></span>

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

### <span data-ttu-id="46d9a-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46d9a-123">-DefaultProfile</span></span>
<span data-ttu-id="46d9a-124">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="46d9a-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="46d9a-125">-장애 조치(failover)</span><span class="sxs-lookup"><span data-stu-id="46d9a-125">-Failover</span></span>
<span data-ttu-id="46d9a-126">이 작업이 장애 조치(failover)를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="46d9a-126">Indicates that this operation is a failover.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByFailoverParams
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46d9a-127">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46d9a-127">-PartnerResourceGroupName</span></span>
<span data-ttu-id="46d9a-128">파트너 Azure SQL Database가 할당된 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="46d9a-128">Specifies the name of the resource group to which the partner Azure SQL Database is assigned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46d9a-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46d9a-129">-ResourceGroupName</span></span>
<span data-ttu-id="46d9a-130">Azure SQL Database Secondary가 할당된 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="46d9a-130">Specifies the name of the resource group to which the Azure SQL Database Secondary is assigned.</span></span>

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

### <span data-ttu-id="46d9a-131">-ServerName</span><span class="sxs-lookup"><span data-stu-id="46d9a-131">-ServerName</span></span>
<span data-ttu-id="46d9a-132">Azure SQL Server Database Secondary를 호스트하는 SQL 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="46d9a-132">Specifies the name of the SQL Server that hosts the Azure SQL Database Secondary.</span></span>

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

### <span data-ttu-id="46d9a-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="46d9a-133">-Confirm</span></span>
<span data-ttu-id="46d9a-134">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="46d9a-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46d9a-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46d9a-135">-WhatIf</span></span>
<span data-ttu-id="46d9a-136">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="46d9a-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46d9a-137">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="46d9a-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46d9a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46d9a-138">CommonParameters</span></span>
<span data-ttu-id="46d9a-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="46d9a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46d9a-140">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="46d9a-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46d9a-141">입력</span><span class="sxs-lookup"><span data-stu-id="46d9a-141">INPUTS</span></span>

### <span data-ttu-id="46d9a-142">System.String</span><span class="sxs-lookup"><span data-stu-id="46d9a-142">System.String</span></span>

## <span data-ttu-id="46d9a-143">출력</span><span class="sxs-lookup"><span data-stu-id="46d9a-143">OUTPUTS</span></span>

### <span data-ttu-id="46d9a-144">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="46d9a-144">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="46d9a-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="46d9a-145">NOTES</span></span>

## <span data-ttu-id="46d9a-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="46d9a-146">RELATED LINKS</span></span>

[<span data-ttu-id="46d9a-147">New-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="46d9a-147">New-AzSqlDatabaseSecondary</span></span>](./New-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="46d9a-148">Remove-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="46d9a-148">Remove-AzSqlDatabaseSecondary</span></span>](./Remove-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="46d9a-149">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="46d9a-149">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
