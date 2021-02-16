---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustodataconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDataConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDataConnection.md
ms.openlocfilehash: ab58d679e9fc3ad62baeded8622b81a0cb8b2f95
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203801"
---
# <span data-ttu-id="c0816-101">New-AzKustoDataConnection</span><span class="sxs-lookup"><span data-stu-id="c0816-101">New-AzKustoDataConnection</span></span>

## <span data-ttu-id="c0816-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0816-102">SYNOPSIS</span></span>
<span data-ttu-id="c0816-103">데이터 연결을 생성하거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="c0816-103">Creates or updates a data connection.</span></span>

## <span data-ttu-id="c0816-104">구문</span><span class="sxs-lookup"><span data-stu-id="c0816-104">SYNTAX</span></span>

### <span data-ttu-id="c0816-105">CreateExpandedEventHub(기본값)</span><span class="sxs-lookup"><span data-stu-id="c0816-105">CreateExpandedEventHub (Default)</span></span>
```
New-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -EventHubResourceId <String> -Kind <Kind>
 -Location <String> [-SubscriptionId <String>] [-Compression <Compression>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="c0816-106">CreateExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="c0816-106">CreateExpandedEventGrid</span></span>
```
New-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -EventHubResourceId <String> -Kind <Kind>
 -Location <String> -StorageAccountResourceId <String> [-SubscriptionId <String>]
 [-DataFormat <EventGridDataFormat>] [-MappingRuleName <String>] [-TableName <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c0816-107">CreateExpandedIotHub</span><span class="sxs-lookup"><span data-stu-id="c0816-107">CreateExpandedIotHub</span></span>
```
New-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -IotHubResourceId <String> -Kind <Kind>
 -Location <String> -SharedAccessPolicyName <String> [-SubscriptionId <String>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="c0816-108">UpdateExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="c0816-108">UpdateExpandedEventGrid</span></span>
```
New-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -Kind <Kind> -Location <String>
 [-SubscriptionId <String>] [-BlobStorageEventType <BlobStorageEventType>] [-DataFormat <EventGridDataFormat>]
 [-IgnoreFirstRecord] [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c0816-109">UpdateViaIdentityExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="c0816-109">UpdateViaIdentityExpandedEventGrid</span></span>
```
New-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -Kind <Kind> -Location <String>
 [-SubscriptionId <String>] [-BlobStorageEventType <BlobStorageEventType>] [-DataFormat <EventGridDataFormat>]
 [-IgnoreFirstRecord] [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c0816-110">설명</span><span class="sxs-lookup"><span data-stu-id="c0816-110">DESCRIPTION</span></span>
<span data-ttu-id="c0816-111">데이터 연결을 생성하거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="c0816-111">Creates or updates a data connection.</span></span>

## <span data-ttu-id="c0816-112">예제</span><span class="sxs-lookup"><span data-stu-id="c0816-112">EXAMPLES</span></span>

### <span data-ttu-id="c0816-113">예제 1: 새 EventHub 데이터 연결 만들기</span><span class="sxs-lookup"><span data-stu-id="c0816-113">Example 1: Create a new EventHub data connection</span></span>
```powershell
PS C:\> New-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventhubdc" -Location="East US" -Kind "EventHub" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -DataFormat "JSON" -ConsumerGroup '$Default' -Compression "None" -TableName "Events" -MappingRuleName "EventsMapping"

Kind     Location Name                                             Type
----     -------- ----                                             ----
EventHub East US  testnewkustocluster/mykustodatabase/myeventhubdc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="c0816-114">위의 명령은 "testnewkustocluster" 클러스터의 "mykustodatabase" 데이터베이스에 대해 "myeventhubdc"라는 새 EventHub 데이터 연결을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c0816-114">The above command creates a new EventHub data connection named "myeventhubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="c0816-115">예제 2: 새 EventGrid 데이터 연결 만들기</span><span class="sxs-lookup"><span data-stu-id="c0816-115">Example 2: Create a new EventGrid data connection</span></span>
```powershell
PS C:\> New-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventgriddc" -Location="East US" -Kind "EventGrid" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -StorageAccountResourceId $storageAccountResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Storage/storageAccounts/mystorage" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "EventsMapping" -IgnoreFirstRecord "false" -BlobStorageEventType "Microsoft.Storage.BlobRenamed"

Kind      Location Name                                              Type
----      -------- ----                                              ----
EventGrid East US  testnewkustocluster/mykustodatabase/myeventgriddc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="c0816-116">위의 명령은 "testnewkustocluster" 클러스터의 데이터베이스 "mykustodatabase"에 대해 "myeventgriddc"라는 새 EventGrid 데이터 연결을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c0816-116">The above command creates a new EventGrid data connection named "myeventgriddc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="c0816-117">예제 3: 새 IotHub 데이터 연결 만들기</span><span class="sxs-lookup"><span data-stu-id="c0816-117">Example 3: Create a new IotHub data connection</span></span>
```powershell
PS C:\> New-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myiothubdc" -Location="East US" -Kind "IotHub" -IotHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Devices/IotHubs/myiothub" -SharedAccessPolicyName "myiothubpolicy" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "EventsMapping"

Kind      Location Name                                        Type
----      -------- ----                                        ----
IotHub East US  testnewkustocluster/mykustodatabase/myiothubdc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="c0816-118">위의 명령은 "testnewkustocluster" 클러스터의 "mykustodatabase" 데이터베이스에 대해 "myiothubdc"라는 새 IotHub 데이터 연결을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c0816-118">The above command creates a new IotHub data connection named "myiothubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="c0816-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c0816-119">PARAMETERS</span></span>

### <span data-ttu-id="c0816-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c0816-120">-AsJob</span></span>
<span data-ttu-id="c0816-121">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="c0816-121">Run the command as a job</span></span>

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

### <span data-ttu-id="c0816-122">-BlobStorageEventType</span><span class="sxs-lookup"><span data-stu-id="c0816-122">-BlobStorageEventType</span></span>
<span data-ttu-id="c0816-123">처리할 Blob Storage 이벤트 유형의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c0816-123">The name of blob storage event type to process.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.BlobStorageEventType
Parameter Sets: UpdateExpandedEventGrid, UpdateViaIdentityExpandedEventGrid
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0816-124">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="c0816-124">-ClusterName</span></span>
<span data-ttu-id="c0816-125">Kusto 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c0816-125">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0816-126">-Compression</span><span class="sxs-lookup"><span data-stu-id="c0816-126">-Compression</span></span>
<span data-ttu-id="c0816-127">이벤트 허브 메시지 압축 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="c0816-127">The event hub messages compression type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.Compression
Parameter Sets: CreateExpandedEventHub
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0816-128">-ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="c0816-128">-ConsumerGroup</span></span>
<span data-ttu-id="c0816-129">이벤트/iot 허브 소비자 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="c0816-129">The event/iot hub consumer group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0816-130">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c0816-130">-DatabaseName</span></span>
<span data-ttu-id="c0816-131">Kusto 클러스터의 데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c0816-131">The name of the database in the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0816-132">-DataFormat</span><span class="sxs-lookup"><span data-stu-id="c0816-132">-DataFormat</span></span>
<span data-ttu-id="c0816-133">메시지의 데이터 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="c0816-133">The data format of the message.</span></span>
<span data-ttu-id="c0816-134">선택적으로 각 메시지에 데이터 형식을 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c0816-134">Optionally the data format can be added to each message.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.EventGridDataFormat
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0816-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0816-135">-DefaultProfile</span></span>
<span data-ttu-id="c0816-136">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c0816-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0816-137">-EventHubResourceId</span><span class="sxs-lookup"><span data-stu-id="c0816-137">-EventHubResourceId</span></span>
<span data-ttu-id="c0816-138">데이터 연결을 만드는 데 사용할 이벤트 허브의 리소스 ID/Event Grid가 이벤트를 보내도록 구성됩니다.</span><span class="sxs-lookup"><span data-stu-id="c0816-138">The resource ID of the event hub to be used to create a data connection / event grid is configured to send events.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpandedEventGrid, CreateExpandedEventHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0816-139">-EventSystemProperty</span><span class="sxs-lookup"><span data-stu-id="c0816-139">-EventSystemProperty</span></span>
<span data-ttu-id="c0816-140">이벤트/iot 허브의 시스템 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="c0816-140">System properties of the event/iot hub.</span></span>

```yaml
Type: System.String[]
Parameter Sets: CreateExpandedEventHub, CreateExpandedIotHub
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0816-141">-IgnoreFirstRecord</span><span class="sxs-lookup"><span data-stu-id="c0816-141">-IgnoreFirstRecord</span></span>
<span data-ttu-id="c0816-142">true로 설정하면 모든 파일의 첫 번째 레코드를 무시해야 한다고 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="c0816-142">If set to true, indicates that ingestion should ignore the first record of every file.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UpdateExpandedEventGrid, UpdateViaIdentityExpandedEventGrid
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0816-143">-IotHubResourceId</span><span class="sxs-lookup"><span data-stu-id="c0816-143">-IotHubResourceId</span></span>
<span data-ttu-id="c0816-144">데이터 연결을 만드는 데 사용할 Iot Hub의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c0816-144">The resource ID of the Iot hub to be used to create a data connection.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0816-145">-Kind</span><span class="sxs-lookup"><span data-stu-id="c0816-145">-Kind</span></span>
<span data-ttu-id="c0816-146">데이터 연결에 대한 엔드포인트의 종류</span><span class="sxs-lookup"><span data-stu-id="c0816-146">Kind of the endpoint for the data connection</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.Kind
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0816-147">-Location</span><span class="sxs-lookup"><span data-stu-id="c0816-147">-Location</span></span>
<span data-ttu-id="c0816-148">리소스 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="c0816-148">Resource location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0816-149">-MappingRuleName</span><span class="sxs-lookup"><span data-stu-id="c0816-149">-MappingRuleName</span></span>
<span data-ttu-id="c0816-150">데이터를 수집하는 데 사용할 매핑 규칙입니다.</span><span class="sxs-lookup"><span data-stu-id="c0816-150">The mapping rule to be used to ingest the data.</span></span>
<span data-ttu-id="c0816-151">선택적으로 매핑 정보를 각 메시지에 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c0816-151">Optionally the mapping information can be added to each message.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0816-152">-Name</span><span class="sxs-lookup"><span data-stu-id="c0816-152">-Name</span></span>
<span data-ttu-id="c0816-153">데이터 연결의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c0816-153">The name of the data connection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DataConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0816-154">-NoWait</span><span class="sxs-lookup"><span data-stu-id="c0816-154">-NoWait</span></span>
<span data-ttu-id="c0816-155">명령을 비동기적으로 실행</span><span class="sxs-lookup"><span data-stu-id="c0816-155">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c0816-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0816-156">-ResourceGroupName</span></span>
<span data-ttu-id="c0816-157">Kusto 클러스터를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c0816-157">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0816-158">-SharedAccessPolicyName</span><span class="sxs-lookup"><span data-stu-id="c0816-158">-SharedAccessPolicyName</span></span>
<span data-ttu-id="c0816-159">공유 액세스 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c0816-159">The name of the share access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0816-160">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="c0816-160">-StorageAccountResourceId</span></span>
<span data-ttu-id="c0816-161">데이터가 있는 저장소 계정의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c0816-161">The resource ID of the storage account where the data resides.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpandedEventGrid
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0816-162">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c0816-162">-SubscriptionId</span></span>
<span data-ttu-id="c0816-163">Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c0816-163">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="c0816-164">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="c0816-164">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0816-165">-TableName</span><span class="sxs-lookup"><span data-stu-id="c0816-165">-TableName</span></span>
<span data-ttu-id="c0816-166">데이터를 수집해야 하는 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="c0816-166">The table where the data should be ingested.</span></span>
<span data-ttu-id="c0816-167">선택적으로 테이블 정보를 각 메시지에 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c0816-167">Optionally the table information can be added to each message.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0816-168">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c0816-168">-Confirm</span></span>
<span data-ttu-id="c0816-169">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c0816-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0816-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0816-170">-WhatIf</span></span>
<span data-ttu-id="c0816-171">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="c0816-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0816-172">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c0816-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0816-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0816-173">CommonParameters</span></span>
<span data-ttu-id="c0816-174">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c0816-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0816-175">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c0816-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0816-176">입력</span><span class="sxs-lookup"><span data-stu-id="c0816-176">INPUTS</span></span>

## <span data-ttu-id="c0816-177">출력</span><span class="sxs-lookup"><span data-stu-id="c0816-177">OUTPUTS</span></span>

### <span data-ttu-id="c0816-178">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDataConnection</span><span class="sxs-lookup"><span data-stu-id="c0816-178">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDataConnection</span></span>

## <span data-ttu-id="c0816-179">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c0816-179">NOTES</span></span>

<span data-ttu-id="c0816-180">별칭</span><span class="sxs-lookup"><span data-stu-id="c0816-180">ALIASES</span></span>

## <span data-ttu-id="c0816-181">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c0816-181">RELATED LINKS</span></span>

