---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: B7F07494-FBCA-4A77-92BF-E0A2D7ACCD21
online version: ''
schema: 2.0.0
ms.openlocfilehash: 35e29655e8447644b6c5449309424595e45ca187
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100413067"
---
# <span data-ttu-id="66e6e-101">Start-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="66e6e-101">Start-AzureSqlDatabaseCopy</span></span>

## <span data-ttu-id="66e6e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66e6e-102">SYNOPSIS</span></span>
<span data-ttu-id="66e6e-103">Azure SQL 데이터베이스의 복사 작업을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="66e6e-103">Starts a copy operation of an Azure SQL Database.</span></span>

## <span data-ttu-id="66e6e-104">구문</span><span class="sxs-lookup"><span data-stu-id="66e6e-104">SYNTAX</span></span>

### <span data-ttu-id="66e6e-105">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="66e6e-105">ByInputObject</span></span>
```
Start-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> [-PartnerServer <String>]
 -PartnerDatabase <String> [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66e6e-106">ByInputObjectContinuous</span><span class="sxs-lookup"><span data-stu-id="66e6e-106">ByInputObjectContinuous</span></span>
```
Start-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> -PartnerServer <String>
 [-PartnerDatabase <String>] [-ContinuousCopy] [-OfflineSecondary] [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66e6e-107">ByDatabaseName</span><span class="sxs-lookup"><span data-stu-id="66e6e-107">ByDatabaseName</span></span>
```
Start-AzureSqlDatabaseCopy -ServerName <String> -DatabaseName <String> [-PartnerServer <String>]
 -PartnerDatabase <String> [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66e6e-108">ByDatabaseNameContinuous</span><span class="sxs-lookup"><span data-stu-id="66e6e-108">ByDatabaseNameContinuous</span></span>
```
Start-AzureSqlDatabaseCopy -ServerName <String> -DatabaseName <String> -PartnerServer <String>
 [-PartnerDatabase <String>] [-ContinuousCopy] [-OfflineSecondary] [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66e6e-109">설명</span><span class="sxs-lookup"><span data-stu-id="66e6e-109">DESCRIPTION</span></span>
<span data-ttu-id="66e6e-110">**Start-AzureSqlDatabaseCopy** cmdlet은 특정 Azure SQL Database의 일회성 복사 작업 또는 연속 복사 작업을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="66e6e-110">The **Start-AzureSqlDatabaseCopy** cmdlet starts a one-time copy operation or a continuous copy operation of a specific Azure SQL Database.</span></span>
<span data-ttu-id="66e6e-111">이 cmdlet은 트랜잭션이 아니며</span><span class="sxs-lookup"><span data-stu-id="66e6e-111">This cmdlet is not transactional.</span></span>

<span data-ttu-id="66e6e-112">원본 데이터베이스는 원본 데이터베이스입니다.</span><span class="sxs-lookup"><span data-stu-id="66e6e-112">The original database is the source database.</span></span>
<span data-ttu-id="66e6e-113">복사본은 보조 데이터베이스 또는 대상 데이터베이스입니다.</span><span class="sxs-lookup"><span data-stu-id="66e6e-113">The copy is the secondary or target database.</span></span>
<span data-ttu-id="66e6e-114">연속 복사의 경우 원본 및 대상 데이터베이스는 동일한 서버에 있을 수 없습니다. 원본 및 대상 데이터베이스를 호스트하는 서버는 동일한 구독의 일부가 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="66e6e-114">For a continuous copy, the source and target databases cannot reside on the same server, and the servers that host the source and target databases must be part of the same subscription.</span></span>

<span data-ttu-id="66e6e-115">*ContinuousCopy* 매개 변수를 지정하지 않으면 이 cmdlet은 원본 데이터베이스의 일회성 복사본을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="66e6e-115">If you do not specify the *ContinuousCopy* parameter, this cmdlet creates a one-time copy of the source database.</span></span>
<span data-ttu-id="66e6e-116">응답을 수신하면 작업이 계속 진행 중일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="66e6e-116">When the response is received, the operation can still be in progress.</span></span>
<span data-ttu-id="66e6e-117">Get-AzureSqlDatabaseCopy cmdlet을 사용하여 작업을 Get-AzureSqlDatabaseOperation 있습니다.</span><span class="sxs-lookup"><span data-stu-id="66e6e-117">You can monitor the operation by using the Get-AzureSqlDatabaseCopy or Get-AzureSqlDatabaseOperation cmdlet.</span></span>

<span data-ttu-id="66e6e-118">*ContinuousCopy를 지정하는* 경우 이 cmdlet은 원본 데이터베이스의 연속 복사본을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="66e6e-118">If you specify *ContinuousCopy*, this cmdlet creates a continuous copy of the source database.</span></span>
<span data-ttu-id="66e6e-119">응답을 수신하면 작업이 진행 중입니다.</span><span class="sxs-lookup"><span data-stu-id="66e6e-119">When the response is received, the operation will be in progress.</span></span>
<span data-ttu-id="66e6e-120">**Get-AzureSqlDatabaseCopy** 또는 **Get-AzureSqlDatabaseOperation을** 사용하여 작업을 모니터링할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="66e6e-120">You can monitor the operation by using **Get-AzureSqlDatabaseCopy** or **Get-AzureSqlDatabaseOperation**.</span></span>

<span data-ttu-id="66e6e-121">연속 복사본을 온라인 또는 오프라인 데이터베이스로 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="66e6e-121">You can create a continuous copy as an online or offline database.</span></span>
<span data-ttu-id="66e6e-122">온라인 연속 복사는 Azure Geo-Replication Database에 대한 Active SQL 구성하는 데 https://azure.microsoft.com/en-us/documentation/articles/sql-database-geo-replication-overview/ 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="66e6e-122">The online continuous copy is used to configure Active Geo-Replication for Azure SQL Databasehttps://azure.microsoft.com/en-us/documentation/articles/sql-database-geo-replication-overview/.</span></span>
<span data-ttu-id="66e6e-123">오프라인 연속 복사는 Azure SQL Database에 대한 표준 Geo-Replication 구성하는 데 https://azure.microsoft.com/en-us/documentation/articles/sql-database-business-continuity-scenarios/ 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="66e6e-123">The offline continuous copy is used to configure Standard Geo-Replication for Azure SQL Databasehttps://azure.microsoft.com/en-us/documentation/articles/sql-database-business-continuity-scenarios/.</span></span>

## <span data-ttu-id="66e6e-124">예제</span><span class="sxs-lookup"><span data-stu-id="66e6e-124">EXAMPLES</span></span>

### <span data-ttu-id="66e6e-125">예제 1: 연속 데이터베이스 복사 예약</span><span class="sxs-lookup"><span data-stu-id="66e6e-125">Example 1: Schedule a continuous database copy</span></span>
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf65" -ContinuousCopy
```

<span data-ttu-id="66e6e-126">이 명령은 lpqd0zbr8y라는 서버에서 Orders라는 데이터베이스의 연속 복사본을 예약합니다.</span><span class="sxs-lookup"><span data-stu-id="66e6e-126">This command schedules a continuous copy of the database named Orders on the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="66e6e-127">이 명령은 bk0b8kf658이라는 서버에 대상 데이터베이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="66e6e-127">The command creates a target database on the server named bk0b8kf658.</span></span>

### <span data-ttu-id="66e6e-128">예제 2: 동일한 서버에 일회성 복사본 만들기</span><span class="sxs-lookup"><span data-stu-id="66e6e-128">Example 2: Create a one-time copy on the same server</span></span>
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerDatabase "OrdersCopy"
```

<span data-ttu-id="66e6e-129">이 명령은 lpqd0zbr8y라는 서버에 주문이라는 데이터베이스의 일회성 복사본을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="66e6e-129">This command creates a one-time copy of the database named Orders on the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="66e6e-130">이 명령은 동일한 서버에 OrdersCopy라는 복사본을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="66e6e-130">The command creates a copy named OrdersCopy on the same server.</span></span>

### <span data-ttu-id="66e6e-131">예제 3: 연속 오프라인 데이터베이스 복사 예약</span><span class="sxs-lookup"><span data-stu-id="66e6e-131">Example 3: Schedule a continuous offline database copy</span></span>
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf65" -ContinuousCopy -OfflineSecondary
```

<span data-ttu-id="66e6e-132">이 명령은 lpqd0zbr8y라는 서버에서 Orders라는 데이터베이스의 연속 복사본을 예약합니다.</span><span class="sxs-lookup"><span data-stu-id="66e6e-132">This command schedules a continuous copy of the database named Orders on the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="66e6e-133">이 명령은 bk0b8kf658이라는 서버에 오프라인 대상 데이터베이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="66e6e-133">This command creates an offline target database on the server named bk0b8kf658.</span></span>

## <span data-ttu-id="66e6e-134">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="66e6e-134">PARAMETERS</span></span>

### <span data-ttu-id="66e6e-135">-ContinuousCopy</span><span class="sxs-lookup"><span data-stu-id="66e6e-135">-ContinuousCopy</span></span>
<span data-ttu-id="66e6e-136">데이터베이스 복사본이 연속 복사(복제본 데이터베이스)를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="66e6e-136">Indicates that the database copy will be a continuous-copy (a replica database).</span></span>
<span data-ttu-id="66e6e-137">연속 복사는 동일한 서버 내에서 지원되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="66e6e-137">Continuous copy is not supported within the same server.</span></span>
<span data-ttu-id="66e6e-138">이 매개 변수를 지정하지 않으면 일회성 복사본이 수행됩니다.</span><span class="sxs-lookup"><span data-stu-id="66e6e-138">If this parameter is not specified, then a one-time copy is performed.</span></span>
<span data-ttu-id="66e6e-139">일회성 복사본의 경우 원본 및 파트너 데이터베이스가 동일한 서버에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="66e6e-139">For a one-time copy, the source and partner databases must be on the same server.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByInputObjectContinuous, ByDatabaseNameContinuous
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66e6e-140">-Database</span><span class="sxs-lookup"><span data-stu-id="66e6e-140">-Database</span></span>
<span data-ttu-id="66e6e-141">원본 Azure SQL 데이터베이스를 나타내는 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="66e6e-141">Specifies an object that represents the source Azure SQL Database.</span></span>
<span data-ttu-id="66e6e-142">이 매개 변수는 파이프라인 입력을 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="66e6e-142">This parameter accepts pipeline input.</span></span>

```yaml
Type: Database
Parameter Sets: ByInputObject, ByInputObjectContinuous
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="66e6e-143">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="66e6e-143">-DatabaseName</span></span>
<span data-ttu-id="66e6e-144">원본 데이터베이스의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="66e6e-144">Specifies the name of the source database.</span></span>

```yaml
Type: String
Parameter Sets: ByDatabaseName, ByDatabaseNameContinuous
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66e6e-145">-Force</span><span class="sxs-lookup"><span data-stu-id="66e6e-145">-Force</span></span>
<span data-ttu-id="66e6e-146">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="66e6e-146">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66e6e-147">-OfflineSecondary</span><span class="sxs-lookup"><span data-stu-id="66e6e-147">-OfflineSecondary</span></span>
<span data-ttu-id="66e6e-148">연속 복사본이 활성 복사본이 아닌 수동 복사본으로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="66e6e-148">Specifies that a continuous copy is a passive copy rather than an active copy.</span></span>
<span data-ttu-id="66e6e-149">원본 데이터베이스가 Standard Edition 데이터베이스인 경우 이 매개 변수가 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="66e6e-149">If the source database is a Standard edition database, then this parameter is required.</span></span>
<span data-ttu-id="66e6e-150">이 매개 변수를 지정하는 경우 *ContinuousCopy도* 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="66e6e-150">If this parameter is specified then *ContinuousCopy* must also be specified.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByInputObjectContinuous, ByDatabaseNameContinuous
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66e6e-151">-PartnerDatabase</span><span class="sxs-lookup"><span data-stu-id="66e6e-151">-PartnerDatabase</span></span>
<span data-ttu-id="66e6e-152">대상 데이터베이스의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="66e6e-152">Specifies name of the target database.</span></span>
<span data-ttu-id="66e6e-153">*ContinuousCopy* 매개 변수를 지정하는 경우 *PartnerDatabase의* 값은 원본 데이터베이스의 이름과 일치해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="66e6e-153">If you specify the *ContinuousCopy* parameter, the value for *PartnerDatabase* must match the name of the source database.</span></span>
<span data-ttu-id="66e6e-154">*ContinuousCopy를* 지정하지 않으면 원본 데이터베이스 이름과 다를 수 있는 대상 데이터베이스의 이름을 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="66e6e-154">If you do not specify *ContinuousCopy*, you must specify a name for the target database, which can be different from the source database name.</span></span>

```yaml
Type: String
Parameter Sets: ByInputObject, ByDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByInputObjectContinuous, ByDatabaseNameContinuous
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66e6e-155">-PartnerServer</span><span class="sxs-lookup"><span data-stu-id="66e6e-155">-PartnerServer</span></span>
<span data-ttu-id="66e6e-156">대상 데이터베이스를 호스트하는 서버의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="66e6e-156">Specifies the name of the server that hosts the target database.</span></span>
<span data-ttu-id="66e6e-157">이 서버는 원본 데이터베이스 서버와 동일한 Azure 구독에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="66e6e-157">This server must be in the same Azure subscription as the source database server.</span></span>

```yaml
Type: String
Parameter Sets: ByInputObject, ByDatabaseName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByInputObjectContinuous, ByDatabaseNameContinuous
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66e6e-158">-Profile</span><span class="sxs-lookup"><span data-stu-id="66e6e-158">-Profile</span></span>
<span data-ttu-id="66e6e-159">이 cmdlet이 읽을 Azure 프로필을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="66e6e-159">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="66e6e-160">프로필을 지정하지 않으면 이 cmdlet은 로컬 기본 프로필에서 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="66e6e-160">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66e6e-161">-ServerName</span><span class="sxs-lookup"><span data-stu-id="66e6e-161">-ServerName</span></span>
<span data-ttu-id="66e6e-162">원본 데이터베이스가 있는 서버의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="66e6e-162">Specifies the name of the server on which the source database resides.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="66e6e-163">-Confirm</span><span class="sxs-lookup"><span data-stu-id="66e6e-163">-Confirm</span></span>
<span data-ttu-id="66e6e-164">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="66e6e-164">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66e6e-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66e6e-165">-WhatIf</span></span>
<span data-ttu-id="66e6e-166">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="66e6e-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66e6e-167">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="66e6e-167">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66e6e-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66e6e-168">CommonParameters</span></span>
<span data-ttu-id="66e6e-169">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="66e6e-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66e6e-170">자세한 내용은 다음 about_CommonParameters https://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="66e6e-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66e6e-171">입력</span><span class="sxs-lookup"><span data-stu-id="66e6e-171">INPUTS</span></span>

### <span data-ttu-id="66e6e-172">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span><span class="sxs-lookup"><span data-stu-id="66e6e-172">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

## <span data-ttu-id="66e6e-173">출력</span><span class="sxs-lookup"><span data-stu-id="66e6e-173">OUTPUTS</span></span>

### <span data-ttu-id="66e6e-174">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="66e6e-174">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy</span></span>

## <span data-ttu-id="66e6e-175">참고 사항</span><span class="sxs-lookup"><span data-stu-id="66e6e-175">NOTES</span></span>
* <span data-ttu-id="66e6e-176">인증: 이 cmdlet에는 인증서 기반 인증이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="66e6e-176">Authentication: This cmdlet requires certificate-based authentication.</span></span> <span data-ttu-id="66e6e-177">인증서 기반 인증을 사용하여 현재 구독을 설정하는 방법의 예제는 New-AzureSqlDatabaseServerContext 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="66e6e-177">For an example of how to use certificate-based authentication to set the current subscription, see New-AzureSqlDatabaseServerContext cmdlet.</span></span>
* <span data-ttu-id="66e6e-178">모니터링: 서버에서 활성 상태인 하나 이상의 연속 복사 관계의 상태를 확인하기 위해 **Get-AzureSqlDatabaseCopy** cmdlet을 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="66e6e-178">Monitoring: To check for the status of one or more continuous copy relationships that are active on the server, use the **Get-AzureSqlDatabaseCopy** cmdlet.</span></span> <span data-ttu-id="66e6e-179">연속 복사 관계의 원본 및 대상 모두에서 작업의 상태를 확인하기 위해 **Get-AzureSqlDatabaseOperation** cmdlet을 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="66e6e-179">To verify the status of the operations at both the source and target of the continuous copy relationship, use the **Get-AzureSqlDatabaseOperation** cmdlet.</span></span>

## <span data-ttu-id="66e6e-180">관련 링크</span><span class="sxs-lookup"><span data-stu-id="66e6e-180">RELATED LINKS</span></span>

[<span data-ttu-id="66e6e-181">Azure SQL Database</span><span class="sxs-lookup"><span data-stu-id="66e6e-181">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="66e6e-182">Azure SQL 데이터베이스에 대한 작업</span><span class="sxs-lookup"><span data-stu-id="66e6e-182">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="66e6e-183">데이터베이스 복사 시작</span><span class="sxs-lookup"><span data-stu-id="66e6e-183">Start Database Copy</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn509576.aspx)



[<span data-ttu-id="66e6e-184">Get-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="66e6e-184">Get-AzureSqlDatabaseCopy</span></span>](./Get-AzureSqlDatabaseCopy.md)

[<span data-ttu-id="66e6e-185">Stop-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="66e6e-185">Stop-AzureSqlDatabaseCopy</span></span>](./Stop-AzureSqlDatabaseCopy.md)


