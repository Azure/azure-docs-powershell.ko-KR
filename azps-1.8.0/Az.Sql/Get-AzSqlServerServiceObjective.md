---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: AC2D64B9-5BCD-45D3-8650-538633F5BBBC
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverserviceobjective
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerServiceObjective.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerServiceObjective.md
ms.openlocfilehash: 5b9bd64eb4d83af9ca150e5eb9ac04479c7fdf5c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698938"
---
# <span data-ttu-id="6b970-101">Get-AzSqlServerServiceObjective</span><span class="sxs-lookup"><span data-stu-id="6b970-101">Get-AzSqlServerServiceObjective</span></span>

## <span data-ttu-id="6b970-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b970-102">SYNOPSIS</span></span>
<span data-ttu-id="6b970-103">Azure SQL 데이터베이스 서버의 서비스 목표를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6b970-103">Gets service objectives for an Azure SQL Database server.</span></span>

## <span data-ttu-id="6b970-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6b970-104">SYNTAX</span></span>

### <span data-ttu-id="6b970-105">ByLocation (기본값)</span><span class="sxs-lookup"><span data-stu-id="6b970-105">ByLocation (Default)</span></span>
```
Get-AzSqlServerServiceObjective [[-ServiceObjectiveName] <String>] -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b970-106">ByServer</span><span class="sxs-lookup"><span data-stu-id="6b970-106">ByServer</span></span>
```
Get-AzSqlServerServiceObjective [[-ServiceObjectiveName] <String>] [-ResourceGroupName] <String>
 [-ServerName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b970-107">설명은</span><span class="sxs-lookup"><span data-stu-id="6b970-107">DESCRIPTION</span></span>
<span data-ttu-id="6b970-108">**AzSqlServerServiceObjective** Cmdlet은 Azure SQL 데이터베이스 서버에 대해 사용 가능한 서비스 목표를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6b970-108">The **Get-AzSqlServerServiceObjective** cmdlet gets the available service objectives for an Azure SQL Database server.</span></span>

## <span data-ttu-id="6b970-109">예제의</span><span class="sxs-lookup"><span data-stu-id="6b970-109">EXAMPLES</span></span>

### <span data-ttu-id="6b970-110">예제 1: 서비스 목표 가져오기</span><span class="sxs-lookup"><span data-stu-id="6b970-110">Example 1: Get service objectives</span></span>
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

<span data-ttu-id="6b970-111">이 명령은 Server01 이라는 서버에 대 한 서비스 목표를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6b970-111">This command gets the service objectives for the server named Server01.</span></span>

### <span data-ttu-id="6b970-112">예제 2: 필터링을 사용 하 여 서비스 목표 구하기</span><span class="sxs-lookup"><span data-stu-id="6b970-112">Example 2: Get service objectives using filtering</span></span>
```
PS C:\>Get-AzSqlServerServiceObjective -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ServiceObjectiveName "P*"
ServiceObjectiveName SkuName       Edition          Family Capacity CapacityUnit Enabled
-------------------- -------       -------          ------ -------- ------------ -------
P1                   Premium       Premium                 125      DTU          True
P2                   Premium       Premium                 250      DTU          True
```

<span data-ttu-id="6b970-113">이 명령은 "System"으로 시작 하는 Server01 이라는 서버의 서비스 목표를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6b970-113">This command gets the service objectives for the server named Server01 that start with "System".</span></span>

### <span data-ttu-id="6b970-114">예제 3: 위치에 대 한 서비스 목표 가져오기</span><span class="sxs-lookup"><span data-stu-id="6b970-114">Example 3: Get service objectives for a location</span></span>
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

<span data-ttu-id="6b970-115">이 명령은 지정 된 Azure 지역에 대 한 서비스 목표를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6b970-115">This command gets the service objectives for a specified Azure region.</span></span>

## <span data-ttu-id="6b970-116">변수</span><span class="sxs-lookup"><span data-stu-id="6b970-116">PARAMETERS</span></span>

### <span data-ttu-id="6b970-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b970-117">-DefaultProfile</span></span>
<span data-ttu-id="6b970-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="6b970-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6b970-119">-위치</span><span class="sxs-lookup"><span data-stu-id="6b970-119">-Location</span></span>
<span data-ttu-id="6b970-120">서비스 목표를 가져올 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6b970-120">The name of the Location for which to get the service objectives.</span></span>

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

### <span data-ttu-id="6b970-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b970-121">-ResourceGroupName</span></span>
<span data-ttu-id="6b970-122">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b970-122">Specifies the name of a resource group.</span></span>
<span data-ttu-id="6b970-123">이 cmdlet은이 리소스에 할당 된 SQL 데이터베이스 서버의 서비스 목표를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6b970-123">This cmdlet gets service objectives for a SQL Database server assigned to this resource.</span></span>

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

### <span data-ttu-id="6b970-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="6b970-124">-ServerName</span></span>
<span data-ttu-id="6b970-125">SQL 데이터베이스 SQL 데이터베이스 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b970-125">Specifies the name of a SQL Database SQL Database server.</span></span>

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

### <span data-ttu-id="6b970-126">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="6b970-126">-ServiceObjectiveName</span></span>
<span data-ttu-id="6b970-127">Azure SQL 데이터베이스 서버에 대 한 서비스 목표의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b970-127">Specifies the name of a service objective for an Azure SQL Database server.</span></span>
<span data-ttu-id="6b970-128">이 매개 변수에 허용 되는 값은 Basic, S0, S1, S2, P1, P2, P3입니다.</span><span class="sxs-lookup"><span data-stu-id="6b970-128">The acceptable values for this parameter are: Basic, S0, S1, S2, P1, P2, and P3.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="6b970-129">-확인</span><span class="sxs-lookup"><span data-stu-id="6b970-129">-Confirm</span></span>
<span data-ttu-id="6b970-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b970-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b970-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b970-131">-WhatIf</span></span>
<span data-ttu-id="6b970-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6b970-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b970-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6b970-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b970-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b970-134">CommonParameters</span></span>
<span data-ttu-id="6b970-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b970-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b970-136">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6b970-136">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b970-137">입력</span><span class="sxs-lookup"><span data-stu-id="6b970-137">INPUTS</span></span>

### <span data-ttu-id="6b970-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="6b970-138">System.String</span></span>

## <span data-ttu-id="6b970-139">출력</span><span class="sxs-lookup"><span data-stu-id="6b970-139">OUTPUTS</span></span>

### <span data-ttu-id="6b970-140">AzureSqlServerServiceObjectiveModel (\*). w i m.</span><span class="sxs-lookup"><span data-stu-id="6b970-140">Microsoft.Azure.Commands.Sql.ServiceObjective.Model.AzureSqlServerServiceObjectiveModel</span></span>

## <span data-ttu-id="6b970-141">상속자</span><span class="sxs-lookup"><span data-stu-id="6b970-141">NOTES</span></span>

## <span data-ttu-id="6b970-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6b970-142">RELATED LINKS</span></span>

[<span data-ttu-id="6b970-143">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="6b970-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


