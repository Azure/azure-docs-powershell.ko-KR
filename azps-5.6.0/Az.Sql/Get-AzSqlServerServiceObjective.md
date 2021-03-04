---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: AC2D64B9-5BCD-45D3-8650-538633F5BBBC
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlserverserviceobjective
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerServiceObjective.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerServiceObjective.md
ms.openlocfilehash: 031b20aa24c66817d199be5d12049d52222d23b1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101969776"
---
# <span data-ttu-id="f43ea-101">Get-AzSqlServerServiceObjective</span><span class="sxs-lookup"><span data-stu-id="f43ea-101">Get-AzSqlServerServiceObjective</span></span>

## <span data-ttu-id="f43ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f43ea-102">SYNOPSIS</span></span>
<span data-ttu-id="f43ea-103">Azure 데이터베이스 서버의 서비스 SQL 합니다.</span><span class="sxs-lookup"><span data-stu-id="f43ea-103">Gets service objectives for an Azure SQL Database server.</span></span>

## <span data-ttu-id="f43ea-104">구문</span><span class="sxs-lookup"><span data-stu-id="f43ea-104">SYNTAX</span></span>

### <span data-ttu-id="f43ea-105">ByLocation(기본값)</span><span class="sxs-lookup"><span data-stu-id="f43ea-105">ByLocation (Default)</span></span>
```
Get-AzSqlServerServiceObjective [[-ServiceObjectiveName] <String>] -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f43ea-106">ByServer</span><span class="sxs-lookup"><span data-stu-id="f43ea-106">ByServer</span></span>
```
Get-AzSqlServerServiceObjective [[-ServiceObjectiveName] <String>] [-ResourceGroupName] <String>
 [-ServerName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f43ea-107">설명</span><span class="sxs-lookup"><span data-stu-id="f43ea-107">DESCRIPTION</span></span>
<span data-ttu-id="f43ea-108">**Get-AzSqlServerServiceObjective** cmdlet은 Azure SQL 서비스 목표를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f43ea-108">The **Get-AzSqlServerServiceObjective** cmdlet gets the available service objectives for an Azure SQL Database server.</span></span>

## <span data-ttu-id="f43ea-109">예제</span><span class="sxs-lookup"><span data-stu-id="f43ea-109">EXAMPLES</span></span>

### <span data-ttu-id="f43ea-110">예제 1: 서비스 목표 얻기</span><span class="sxs-lookup"><span data-stu-id="f43ea-110">Example 1: Get service objectives</span></span>
```
PS C:\>Get-AzSqlServerServiceObjective -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
serviceObjectiveName SkuName       Edition          Family Capacity CapacityUnit Enabled
-------------------- -------       -------          ------ -------- ------------ -------
System               System        System                  0        DTU          False
Free                 Free          Free                    5        DTU          True
Basic                Basic         Basic                   5        DTU          True
S0                   Standard      Standard                10       DTU          True
S1                   Standard      Standard                20       DTU          True
P1                   Premium       Premium                 125      DTU          True
P2                   Premium       Premium                 250      DTU          True
DW100c               DataWarehouse DataWarehouse           900      DTU          False
GP_Gen4_1            GP_Gen4       GeneralPurpose   Gen4   1        VCores       True
GP_Gen5_2            GP_Gen5       GeneralPurpose   Gen5   2        VCores       True
BC_Gen4_1            BC_Gen4       BusinessCritical Gen4   1        VCores       True
BC_Gen5_4            BC_Gen5       BusinessCritical Gen5   4        VCores       True
```

<span data-ttu-id="f43ea-111">이 명령은 Server01이라는 서버에 대한 서비스 목표를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f43ea-111">This command gets the service objectives for the server named Server01.</span></span>

### <span data-ttu-id="f43ea-112">예제 2: 필터링을 사용하여 서비스 목표 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f43ea-112">Example 2: Get service objectives using filtering</span></span>
```
PS C:\>Get-AzSqlServerServiceObjective -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ServiceObjectiveName "P*"
ServiceObjectiveName SkuName       Edition          Family Capacity CapacityUnit Enabled
-------------------- -------       -------          ------ -------- ------------ -------
P1                   Premium       Premium                 125      DTU          True
P2                   Premium       Premium                 250      DTU          True
```

<span data-ttu-id="f43ea-113">이 명령은 "System"으로 시작하는 Server01이라는 서버에 대한 서비스 목표를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f43ea-113">This command gets the service objectives for the server named Server01 that start with "System".</span></span>

### <span data-ttu-id="f43ea-114">예제 3: 위치에 대한 서비스 목표 얻기</span><span class="sxs-lookup"><span data-stu-id="f43ea-114">Example 3: Get service objectives for a location</span></span>
```
PS C:\>Get-AzSqlServerServiceObjective -Location "west us"
serviceObjectiveName SkuName       Edition          Family Capacity CapacityUnit Enabled
-------------------- -------       -------          ------ -------- ------------ -------
System               System        System                  0        DTU          False
Free                 Free          Free                    5        DTU          True
Basic                Basic         Basic                   5        DTU          True
S0                   Standard      Standard                10       DTU          True
S1                   Standard      Standard                20       DTU          True
P1                   Premium       Premium                 125      DTU          True
P2                   Premium       Premium                 250      DTU          True
DW100c               DataWarehouse DataWarehouse           900      DTU          False
GP_Gen4_1            GP_Gen4       GeneralPurpose   Gen4   1        VCores       True
GP_Gen5_2            GP_Gen5       GeneralPurpose   Gen5   2        VCores       True
BC_Gen4_1            BC_Gen4       BusinessCritical Gen4   1        VCores       True
BC_Gen5_4            BC_Gen5       BusinessCritical Gen5   4        VCores       True
```

<span data-ttu-id="f43ea-115">이 명령은 지정된 Azure 지역에 대한 서비스 목표를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f43ea-115">This command gets the service objectives for a specified Azure region.</span></span>

## <span data-ttu-id="f43ea-116">매개 변수</span><span class="sxs-lookup"><span data-stu-id="f43ea-116">PARAMETERS</span></span>

### <span data-ttu-id="f43ea-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f43ea-117">-DefaultProfile</span></span>
<span data-ttu-id="f43ea-118">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="f43ea-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f43ea-119">-Location</span><span class="sxs-lookup"><span data-stu-id="f43ea-119">-Location</span></span>
<span data-ttu-id="f43ea-120">서비스 목표를 얻을 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f43ea-120">The name of the Location for which to get the service objectives.</span></span>

```yaml
Type: System.String
Parameter Sets: ByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f43ea-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f43ea-121">-ResourceGroupName</span></span>
<span data-ttu-id="f43ea-122">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f43ea-122">Specifies the name of a resource group.</span></span>
<span data-ttu-id="f43ea-123">이 cmdlet은 이 리소스에 할당된 SQL 데이터베이스 서버에 대한 서비스 목표를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="f43ea-123">This cmdlet gets service objectives for a SQL Database server assigned to this resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ByServer
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f43ea-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f43ea-124">-ServerName</span></span>
<span data-ttu-id="f43ea-125">데이터베이스 데이터베이스 서버의 SQL 데이터베이스 SQL 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f43ea-125">Specifies the name of a SQL Database SQL Database server.</span></span>

```yaml
Type: System.String
Parameter Sets: ByServer
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f43ea-126">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="f43ea-126">-ServiceObjectiveName</span></span>
<span data-ttu-id="f43ea-127">Azure 데이터베이스 서버의 서비스 목표의 SQL 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f43ea-127">Specifies the name of a service objective for an Azure SQL Database server.</span></span>
<span data-ttu-id="f43ea-128">이 매개 변수에 대해 허용되는 값은 기본, S0, S1, S2, P1, P2 및 P3입니다.</span><span class="sxs-lookup"><span data-stu-id="f43ea-128">The acceptable values for this parameter are: Basic, S0, S1, S2, P1, P2, and P3.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f43ea-129">-확인</span><span class="sxs-lookup"><span data-stu-id="f43ea-129">-Confirm</span></span>
<span data-ttu-id="f43ea-130">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f43ea-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f43ea-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f43ea-131">-WhatIf</span></span>
<span data-ttu-id="f43ea-132">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="f43ea-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f43ea-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f43ea-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f43ea-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f43ea-134">CommonParameters</span></span>
<span data-ttu-id="f43ea-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f43ea-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f43ea-136">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f43ea-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f43ea-137">입력</span><span class="sxs-lookup"><span data-stu-id="f43ea-137">INPUTS</span></span>

### <span data-ttu-id="f43ea-138">System.String</span><span class="sxs-lookup"><span data-stu-id="f43ea-138">System.String</span></span>

## <span data-ttu-id="f43ea-139">출력</span><span class="sxs-lookup"><span data-stu-id="f43ea-139">OUTPUTS</span></span>

### <span data-ttu-id="f43ea-140">Microsoft.Azure.Commands.Sql.ServiceObjective.Model.AzureSqlServerServiceObjectiveModel</span><span class="sxs-lookup"><span data-stu-id="f43ea-140">Microsoft.Azure.Commands.Sql.ServiceObjective.Model.AzureSqlServerServiceObjectiveModel</span></span>

## <span data-ttu-id="f43ea-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f43ea-141">NOTES</span></span>

## <span data-ttu-id="f43ea-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f43ea-142">RELATED LINKS</span></span>

[<span data-ttu-id="f43ea-143">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="f43ea-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


