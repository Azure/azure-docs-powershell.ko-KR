---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: B7F07494-FBCA-4A77-92BF-E0A2D7ACCD21
online version: ''
schema: 2.0.0
ms.openlocfilehash: fc350cdf117ebbf72b023f64895f4c563e73566b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045845"
---
# <span data-ttu-id="5b02b-101">Start-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="5b02b-101">Start-AzureSqlDatabaseCopy</span></span>

## <span data-ttu-id="5b02b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b02b-102">SYNOPSIS</span></span>
<span data-ttu-id="5b02b-103">Azure SQL 데이터베이스의 복사 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b02b-103">Starts a copy operation of an Azure SQL Database.</span></span>

## <span data-ttu-id="5b02b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5b02b-104">SYNTAX</span></span>

### <span data-ttu-id="5b02b-105">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="5b02b-105">ByInputObject</span></span>
```
Start-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> [-PartnerServer <String>]
 -PartnerDatabase <String> [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b02b-106">ByInputObjectContinuous</span><span class="sxs-lookup"><span data-stu-id="5b02b-106">ByInputObjectContinuous</span></span>
```
Start-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> -PartnerServer <String>
 [-PartnerDatabase <String>] [-ContinuousCopy] [-OfflineSecondary] [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b02b-107">ByDatabaseName</span><span class="sxs-lookup"><span data-stu-id="5b02b-107">ByDatabaseName</span></span>
```
Start-AzureSqlDatabaseCopy -ServerName <String> -DatabaseName <String> [-PartnerServer <String>]
 -PartnerDatabase <String> [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b02b-108">ByDatabaseNameContinuous</span><span class="sxs-lookup"><span data-stu-id="5b02b-108">ByDatabaseNameContinuous</span></span>
```
Start-AzureSqlDatabaseCopy -ServerName <String> -DatabaseName <String> -PartnerServer <String>
 [-PartnerDatabase <String>] [-ContinuousCopy] [-OfflineSecondary] [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5b02b-109">설명은</span><span class="sxs-lookup"><span data-stu-id="5b02b-109">DESCRIPTION</span></span>
<span data-ttu-id="5b02b-110">**AzureSqlDatabaseCopy** cmdlet은 특정 Azure SQL Database에 대 한 일회성 복사 작업 또는 연속 복사 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b02b-110">The **Start-AzureSqlDatabaseCopy** cmdlet starts a one-time copy operation or a continuous copy operation of a specific Azure SQL Database.</span></span>
<span data-ttu-id="5b02b-111">이 cmdlet은 트랜잭션이 아닙니다.</span><span class="sxs-lookup"><span data-stu-id="5b02b-111">This cmdlet is not transactional.</span></span>

<span data-ttu-id="5b02b-112">원래 데이터베이스는 원본 데이터베이스입니다.</span><span class="sxs-lookup"><span data-stu-id="5b02b-112">The original database is the source database.</span></span>
<span data-ttu-id="5b02b-113">사본은 보조 또는 대상 데이터베이스입니다.</span><span class="sxs-lookup"><span data-stu-id="5b02b-113">The copy is the secondary or target database.</span></span>
<span data-ttu-id="5b02b-114">연속 복사본의 경우 원본 및 대상 데이터베이스가 같은 서버에 상주할 수 없으며 원본 및 대상 데이터베이스를 호스트 하는 서버는 동일한 구독의 일부 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b02b-114">For a continuous copy, the source and target databases cannot reside on the same server, and the servers that host the source and target databases must be part of the same subscription.</span></span>

<span data-ttu-id="5b02b-115">*ContinuousCopy* 매개 변수를 지정 하지 않으면이 cmdlet은 원본 데이터베이스의 일회성 복사본을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5b02b-115">If you do not specify the *ContinuousCopy* parameter, this cmdlet creates a one-time copy of the source database.</span></span>
<span data-ttu-id="5b02b-116">응답을 받으면 작업을 계속 진행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5b02b-116">When the response is received, the operation can still be in progress.</span></span>
<span data-ttu-id="5b02b-117">Get-AzureSqlDatabaseCopy 또는 Get-AzureSqlDatabaseOperation cmdlet을 사용 하 여 작업을 모니터링할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5b02b-117">You can monitor the operation by using the Get-AzureSqlDatabaseCopy or Get-AzureSqlDatabaseOperation cmdlet.</span></span>

<span data-ttu-id="5b02b-118">*ContinuousCopy* 를 지정 하는 경우이 cmdlet은 원본 데이터베이스의 연속 복사본을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5b02b-118">If you specify *ContinuousCopy* , this cmdlet creates a continuous copy of the source database.</span></span>
<span data-ttu-id="5b02b-119">응답을 받으면 작업이 진행 되 고 있는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="5b02b-119">When the response is received, the operation will be in progress.</span></span>
<span data-ttu-id="5b02b-120">**Get-AzureSqlDatabaseCopy** 또는 **get-AzureSqlDatabaseOperation** 를 사용 하 여 작업을 모니터링할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5b02b-120">You can monitor the operation by using **Get-AzureSqlDatabaseCopy** or **Get-AzureSqlDatabaseOperation**.</span></span>

<span data-ttu-id="5b02b-121">연속 복사본을 온라인 또는 오프 라인 데이터베이스로 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5b02b-121">You can create a continuous copy as an online or offline database.</span></span>
<span data-ttu-id="5b02b-122">온라인 연속 복사본은 Azure SQL 데이터베이스의 활성 Geo-Replication를 구성 하는 데 사용 됩니다 https://azure.microsoft.com/en-us/documentation/articles/sql-database-geo-replication-overview/ .</span><span class="sxs-lookup"><span data-stu-id="5b02b-122">The online continuous copy is used to configure Active Geo-Replication for Azure SQL Databasehttps://azure.microsoft.com/en-us/documentation/articles/sql-database-geo-replication-overview/.</span></span>
<span data-ttu-id="5b02b-123">오프 라인 연속 복사본은 Azure SQL 데이터베이스에 대 한 표준 Geo-Replication를 구성 하는 데 사용 됩니다 https://azure.microsoft.com/en-us/documentation/articles/sql-database-business-continuity-scenarios/ .</span><span class="sxs-lookup"><span data-stu-id="5b02b-123">The offline continuous copy is used to configure Standard Geo-Replication for Azure SQL Databasehttps://azure.microsoft.com/en-us/documentation/articles/sql-database-business-continuity-scenarios/.</span></span>

## <span data-ttu-id="5b02b-124">예제의</span><span class="sxs-lookup"><span data-stu-id="5b02b-124">EXAMPLES</span></span>

### <span data-ttu-id="5b02b-125">예제 1: 연속 데이터베이스 복사본 예약</span><span class="sxs-lookup"><span data-stu-id="5b02b-125">Example 1: Schedule a continuous database copy</span></span>
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf65" -ContinuousCopy
```

<span data-ttu-id="5b02b-126">이 명령은 lpqd0zbr8y 이라는 서버에서 Order 라는 데이터베이스의 연속 복사본을 예약 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b02b-126">This command schedules a continuous copy of the database named Orders on the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="5b02b-127">명령이 bk0b8kf658 라는 서버에 대상 데이터베이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5b02b-127">The command creates a target database on the server named bk0b8kf658.</span></span>

### <span data-ttu-id="5b02b-128">예제 2: 동일한 서버에서 일회성 복사본 만들기</span><span class="sxs-lookup"><span data-stu-id="5b02b-128">Example 2: Create a one-time copy on the same server</span></span>
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerDatabase "OrdersCopy"
```

<span data-ttu-id="5b02b-129">이 명령은 lpqd0zbr8y 이라는 서버에서 Order 라는 데이터베이스의 일회성 복사본을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5b02b-129">This command creates a one-time copy of the database named Orders on the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="5b02b-130">이 명령은 같은 서버에 OrdersCopy 이라는 복사본을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5b02b-130">The command creates a copy named OrdersCopy on the same server.</span></span>

### <span data-ttu-id="5b02b-131">예제 3: 연속 오프 라인 데이터베이스 복사본 예약</span><span class="sxs-lookup"><span data-stu-id="5b02b-131">Example 3: Schedule a continuous offline database copy</span></span>
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf65" -ContinuousCopy -OfflineSecondary
```

<span data-ttu-id="5b02b-132">이 명령은 lpqd0zbr8y 이라는 서버에서 Order 라는 데이터베이스의 연속 복사본을 예약 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b02b-132">This command schedules a continuous copy of the database named Orders on the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="5b02b-133">이 명령은 bk0b8kf658 이라는 서버에서 오프 라인 대상 데이터베이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5b02b-133">This command creates an offline target database on the server named bk0b8kf658.</span></span>

## <span data-ttu-id="5b02b-134">변수</span><span class="sxs-lookup"><span data-stu-id="5b02b-134">PARAMETERS</span></span>

### <span data-ttu-id="5b02b-135">-ContinuousCopy</span><span class="sxs-lookup"><span data-stu-id="5b02b-135">-ContinuousCopy</span></span>
<span data-ttu-id="5b02b-136">데이터베이스 복사본이 연속 복사본 (복제본 데이터베이스)이 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="5b02b-136">Indicates that the database copy will be a continuous-copy (a replica database).</span></span>
<span data-ttu-id="5b02b-137">동일한 서버 내에서는 연속 복사가 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5b02b-137">Continuous copy is not supported within the same server.</span></span>
<span data-ttu-id="5b02b-138">이 매개 변수를 지정 하지 않으면 일회성 복사가 수행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5b02b-138">If this parameter is not specified, then a one-time copy is performed.</span></span>
<span data-ttu-id="5b02b-139">일회성 복사본의 경우 원본 및 파트너 데이터베이스가 같은 서버에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b02b-139">For a one-time copy, the source and partner databases must be on the same server.</span></span>

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

### <span data-ttu-id="5b02b-140">-데이터베이스</span><span class="sxs-lookup"><span data-stu-id="5b02b-140">-Database</span></span>
<span data-ttu-id="5b02b-141">원본 Azure SQL 데이터베이스를 나타내는 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b02b-141">Specifies an object that represents the source Azure SQL Database.</span></span>
<span data-ttu-id="5b02b-142">이 매개 변수는 파이프라인 입력을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b02b-142">This parameter accepts pipeline input.</span></span>

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

### <span data-ttu-id="5b02b-143">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5b02b-143">-DatabaseName</span></span>
<span data-ttu-id="5b02b-144">원본 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b02b-144">Specifies the name of the source database.</span></span>

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

### <span data-ttu-id="5b02b-145">-Force</span><span class="sxs-lookup"><span data-stu-id="5b02b-145">-Force</span></span>
<span data-ttu-id="5b02b-146">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b02b-146">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5b02b-147">-OfflineSecondary</span><span class="sxs-lookup"><span data-stu-id="5b02b-147">-OfflineSecondary</span></span>
<span data-ttu-id="5b02b-148">연속 복사본이 활성 복사본이 아닌 수동 복사본 임을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b02b-148">Specifies that a continuous copy is a passive copy rather than an active copy.</span></span>
<span data-ttu-id="5b02b-149">원본 데이터베이스가 Standard edition 데이터베이스인 경우이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="5b02b-149">If the source database is a Standard edition database, then this parameter is required.</span></span>
<span data-ttu-id="5b02b-150">이 매개 변수를 지정 하면 *ContinuousCopy* 도 지정 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b02b-150">If this parameter is specified then *ContinuousCopy* must also be specified.</span></span>

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

### <span data-ttu-id="5b02b-151">-데이터 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="5b02b-151">-PartnerDatabase</span></span>
<span data-ttu-id="5b02b-152">대상 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b02b-152">Specifies name of the target database.</span></span>
<span data-ttu-id="5b02b-153">*ContinuousCopy* 매개 변수를 지정 하는 경우 함께 사용할 *데이터베이스* 의 값은 원본 데이터베이스의 이름과 일치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b02b-153">If you specify the *ContinuousCopy* parameter, the value for *PartnerDatabase* must match the name of the source database.</span></span>
<span data-ttu-id="5b02b-154">*ContinuousCopy* 를 지정 하지 않으면 원본 데이터베이스 이름과 다를 수 있는 대상 데이터베이스의 이름을 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b02b-154">If you do not specify *ContinuousCopy* , you must specify a name for the target database, which can be different from the source database name.</span></span>

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

### <span data-ttu-id="5b02b-155">-또는 서버</span><span class="sxs-lookup"><span data-stu-id="5b02b-155">-PartnerServer</span></span>
<span data-ttu-id="5b02b-156">대상 데이터베이스를 호스트 하는 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b02b-156">Specifies the name of the server that hosts the target database.</span></span>
<span data-ttu-id="5b02b-157">이 서버는 원본 데이터베이스 서버와 동일한 Azure 구독에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b02b-157">This server must be in the same Azure subscription as the source database server.</span></span>

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

### <span data-ttu-id="5b02b-158">-프로필</span><span class="sxs-lookup"><span data-stu-id="5b02b-158">-Profile</span></span>
<span data-ttu-id="5b02b-159">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b02b-159">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5b02b-160">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="5b02b-160">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5b02b-161">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5b02b-161">-ServerName</span></span>
<span data-ttu-id="5b02b-162">원본 데이터베이스가 상주 하는 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b02b-162">Specifies the name of the server on which the source database resides.</span></span>

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

### <span data-ttu-id="5b02b-163">-확인</span><span class="sxs-lookup"><span data-stu-id="5b02b-163">-Confirm</span></span>
<span data-ttu-id="5b02b-164">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b02b-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b02b-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b02b-165">-WhatIf</span></span>
<span data-ttu-id="5b02b-166">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="5b02b-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5b02b-167">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5b02b-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b02b-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b02b-168">CommonParameters</span></span>
<span data-ttu-id="5b02b-169">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b02b-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b02b-170">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b02b-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b02b-171">입력</span><span class="sxs-lookup"><span data-stu-id="5b02b-171">INPUTS</span></span>

### <span data-ttu-id="5b02b-172">WindowsAzure. SqlDatabase. \* 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="5b02b-172">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

## <span data-ttu-id="5b02b-173">출력</span><span class="sxs-lookup"><span data-stu-id="5b02b-173">OUTPUTS</span></span>

### <span data-ttu-id="5b02b-174">WindowsAzure. SqlDatabase. DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="5b02b-174">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy</span></span>

## <span data-ttu-id="5b02b-175">상속자</span><span class="sxs-lookup"><span data-stu-id="5b02b-175">NOTES</span></span>
* <span data-ttu-id="5b02b-176">인증:이 cmdlet을 사용 하려면 인증서 기반 인증이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b02b-176">Authentication: This cmdlet requires certificate-based authentication.</span></span> <span data-ttu-id="5b02b-177">인증서 기반 인증을 사용 하 여 현재 구독을 설정 하는 방법의 예는 New-AzureSqlDatabaseServerContext cmdlet을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="5b02b-177">For an example of how to use certificate-based authentication to set the current subscription, see New-AzureSqlDatabaseServerContext cmdlet.</span></span>
* <span data-ttu-id="5b02b-178">모니터링: 서버에서 활성 상태인 하나 이상의 연속 복사본 관계의 상태를 확인 하려면 **AzureSqlDatabaseCopy** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b02b-178">Monitoring: To check for the status of one or more continuous copy relationships that are active on the server, use the **Get-AzureSqlDatabaseCopy** cmdlet.</span></span> <span data-ttu-id="5b02b-179">연속 복사 관계의 원본 및 대상 모두에서 작업의 상태를 확인 하려면 **AzureSqlDatabaseOperation** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b02b-179">To verify the status of the operations at both the source and target of the continuous copy relationship, use the **Get-AzureSqlDatabaseOperation** cmdlet.</span></span>

## <span data-ttu-id="5b02b-180">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5b02b-180">RELATED LINKS</span></span>

[<span data-ttu-id="5b02b-181">Azure SQL 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="5b02b-181">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="5b02b-182">Azure SQL 데이터베이스에 대 한 작업</span><span class="sxs-lookup"><span data-stu-id="5b02b-182">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="5b02b-183">데이터베이스 복사본 시작</span><span class="sxs-lookup"><span data-stu-id="5b02b-183">Start Database Copy</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn509576.aspx)

[<span data-ttu-id="5b02b-184">Azure SQL 데이터베이스 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5b02b-184">Azure SQL Database Cmdlets</span></span>](./Azure.SQLDatabase.md)

[<span data-ttu-id="5b02b-185">Get-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="5b02b-185">Get-AzureSqlDatabaseCopy</span></span>](./Get-AzureSqlDatabaseCopy.md)

[<span data-ttu-id="5b02b-186">중지-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="5b02b-186">Stop-AzureSqlDatabaseCopy</span></span>](./Stop-AzureSqlDatabaseCopy.md)


