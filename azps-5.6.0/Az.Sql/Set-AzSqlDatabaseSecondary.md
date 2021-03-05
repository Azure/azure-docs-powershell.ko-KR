---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: F9703508-DD4D-4D25-A7CA-7E3432B5DCA9
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseSecondary.md
ms.openlocfilehash: fc0a6bc7fa87a78fedd0416ea1578b9404168dce
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967291"
---
# <span data-ttu-id="d640d-101">Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="d640d-101">Set-AzSqlDatabaseSecondary</span></span>

## <span data-ttu-id="d640d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d640d-102">SYNOPSIS</span></span>
<span data-ttu-id="d640d-103">장애 조치(failover)를 시작하려면 보조 데이터베이스를 기본 데이터베이스로 전환합니다.</span><span class="sxs-lookup"><span data-stu-id="d640d-103">Switches a secondary database to be primary in order to initiate failover.</span></span>

## <span data-ttu-id="d640d-104">구문</span><span class="sxs-lookup"><span data-stu-id="d640d-104">SYNTAX</span></span>

### <span data-ttu-id="d640d-105">NoOptionsSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="d640d-105">NoOptionsSet (Default)</span></span>
```
Set-AzSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String> [-AsJob]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d640d-106">ByFailoverParams</span><span class="sxs-lookup"><span data-stu-id="d640d-106">ByFailoverParams</span></span>
```
Set-AzSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String> [-Failover]
 [-AllowDataLoss] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d640d-107">설명</span><span class="sxs-lookup"><span data-stu-id="d640d-107">DESCRIPTION</span></span>
<span data-ttu-id="d640d-108">**Set-AzSqlDatabaseSecondary** cmdlet은 장애 조치(failover)를 시작하기 위해 보조 데이터베이스를 주 데이터베이스로 전환합니다.</span><span class="sxs-lookup"><span data-stu-id="d640d-108">The **Set-AzSqlDatabaseSecondary** cmdlet switches a secondary database to be primary in order to initiate failover.</span></span>
<span data-ttu-id="d640d-109">이 cmdlet은 일반 구성 명령으로 설계되지만 현재 장애 조치(failover)를 시작하는 것으로 제한됩니다.</span><span class="sxs-lookup"><span data-stu-id="d640d-109">This cmdlet is designed as a general configuration command, but is currently limited to initiating failover.</span></span>
<span data-ttu-id="d640d-110">*AllowDataLoss 매개 변수를* 지정하여 정전 중에 힘 장애 조치(failover)를 시작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d640d-110">Specify the *AllowDataLoss* parameter to initiate a force failover during an outage.</span></span>
<span data-ttu-id="d640d-111">복구 드릴과 같은 계획된 작업을 수행할 때 이 매개 변수를 지정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d640d-111">You do not have to specify this parameter when you perform a planned operation, such as recovery drill.</span></span>
<span data-ttu-id="d640d-112">후자의 경우 보조 데이터베이스가 전환되기 전에 기본 데이터베이스와 동기화됩니다.</span><span class="sxs-lookup"><span data-stu-id="d640d-112">In the latter case, the secondary database is synchronized with the primary before it is switched.</span></span>

## <span data-ttu-id="d640d-113">예제</span><span class="sxs-lookup"><span data-stu-id="d640d-113">EXAMPLES</span></span>

### <span data-ttu-id="d640d-114">예제 1: 계획된 장애 조치(failover) 시작</span><span class="sxs-lookup"><span data-stu-id="d640d-114">Example 1: Initiate a planned failover</span></span>
```powershell
$database = Get-AzSqlDatabase -DatabaseName $databaseName -ResourceGroupName $secondaryResourceGroupName -ServerName $secondaryServerName
$database | Set-AzSqlDatabaseSecondary -PartnerResourceGroupName $primaryResourceGroupName -Failover
```

### <span data-ttu-id="d640d-115">예제 2: 강제 장애 조치(데이터 손실 가능성이 있는) 시작</span><span class="sxs-lookup"><span data-stu-id="d640d-115">Example 2: Initiate a forced failover (with potential data loss)</span></span>
```powershell
$database = Get-AzSqlDatabase -DatabaseName $databaseName -ResourceGroupName $secondaryResourceGroupName -ServerName $secondaryServerName
$database | Set-AzSqlDatabaseSecondary -PartnerResourceGroupName $primaryResourceGroupName -Failover -AllowDataLoss
```

## <span data-ttu-id="d640d-116">매개 변수</span><span class="sxs-lookup"><span data-stu-id="d640d-116">PARAMETERS</span></span>

### <span data-ttu-id="d640d-117">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="d640d-117">-AllowDataLoss</span></span>
<span data-ttu-id="d640d-118">이 장애 조치(failover) 작업이 데이터 손실을 허용하는지 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="d640d-118">Indicates that this failover operation permits data loss.</span></span>

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

### <span data-ttu-id="d640d-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d640d-119">-AsJob</span></span>
<span data-ttu-id="d640d-120">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="d640d-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d640d-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d640d-121">-DatabaseName</span></span>
<span data-ttu-id="d640d-122">Azure 데이터베이스 보조 데이터베이스의 이름을 SQL 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d640d-122">Specifies the name of the Azure SQL Database Secondary.</span></span>

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

### <span data-ttu-id="d640d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d640d-123">-DefaultProfile</span></span>
<span data-ttu-id="d640d-124">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="d640d-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d640d-125">-Failover</span><span class="sxs-lookup"><span data-stu-id="d640d-125">-Failover</span></span>
<span data-ttu-id="d640d-126">이 작업은 장애 조치(failover)를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="d640d-126">Indicates that this operation is a failover.</span></span>

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

### <span data-ttu-id="d640d-127">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d640d-127">-PartnerResourceGroupName</span></span>
<span data-ttu-id="d640d-128">파트너 Azure 데이터베이스가 할당된 리소스 그룹의 SQL 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d640d-128">Specifies the name of the resource group to which the partner Azure SQL Database is assigned.</span></span>

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

### <span data-ttu-id="d640d-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d640d-129">-ResourceGroupName</span></span>
<span data-ttu-id="d640d-130">Azure 데이터베이스 보조 데이터베이스가 할당된 리소스 그룹의 SQL 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d640d-130">Specifies the name of the resource group to which the Azure SQL Database Secondary is assigned.</span></span>

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

### <span data-ttu-id="d640d-131">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d640d-131">-ServerName</span></span>
<span data-ttu-id="d640d-132">Azure SQL Server 데이터베이스 보조를 호스트하는 SQL 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d640d-132">Specifies the name of the SQL Server that hosts the Azure SQL Database Secondary.</span></span>

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

### <span data-ttu-id="d640d-133">-확인</span><span class="sxs-lookup"><span data-stu-id="d640d-133">-Confirm</span></span>
<span data-ttu-id="d640d-134">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d640d-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d640d-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d640d-135">-WhatIf</span></span>
<span data-ttu-id="d640d-136">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="d640d-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d640d-137">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d640d-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d640d-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d640d-138">CommonParameters</span></span>
<span data-ttu-id="d640d-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d640d-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d640d-140">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d640d-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d640d-141">입력</span><span class="sxs-lookup"><span data-stu-id="d640d-141">INPUTS</span></span>

### <span data-ttu-id="d640d-142">System.String</span><span class="sxs-lookup"><span data-stu-id="d640d-142">System.String</span></span>

## <span data-ttu-id="d640d-143">출력</span><span class="sxs-lookup"><span data-stu-id="d640d-143">OUTPUTS</span></span>

### <span data-ttu-id="d640d-144">Microsoft.Azure.Commands.Sql.복제.Model.AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="d640d-144">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="d640d-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d640d-145">NOTES</span></span>

## <span data-ttu-id="d640d-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d640d-146">RELATED LINKS</span></span>

[<span data-ttu-id="d640d-147">New-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="d640d-147">New-AzSqlDatabaseSecondary</span></span>](./New-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="d640d-148">Remove-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="d640d-148">Remove-AzSqlDatabaseSecondary</span></span>](./Remove-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="d640d-149">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="d640d-149">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
