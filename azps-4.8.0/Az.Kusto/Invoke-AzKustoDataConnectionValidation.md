---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/invoke-azkustodataconnectionvalidation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDataConnectionValidation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDataConnectionValidation.md
ms.openlocfilehash: 9eb3ff31873b23fc97f53fffecdbbb38367ac2b5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94211854"
---
# <span data-ttu-id="752b2-101">Invoke-AzKustoDataConnectionValidation</span><span class="sxs-lookup"><span data-stu-id="752b2-101">Invoke-AzKustoDataConnectionValidation</span></span>

## <span data-ttu-id="752b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="752b2-102">SYNOPSIS</span></span>
<span data-ttu-id="752b2-103">데이터 연결 매개 변수가 유효한 지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="752b2-103">Checks that the data connection parameters are valid.</span></span>

## <span data-ttu-id="752b2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="752b2-104">SYNTAX</span></span>

### <span data-ttu-id="752b2-105">DataExpandedEventHub (기본값)</span><span class="sxs-lookup"><span data-stu-id="752b2-105">DataExpandedEventHub (Default)</span></span>
```
Invoke-AzKustoDataConnectionValidation -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -DataConnectionName <String> -EventHubResourceId <String>
 -Kind <Kind> -Location <String> [-SubscriptionId <String>] [-Compression <Compression>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="752b2-106">DataExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="752b2-106">DataExpandedEventGrid</span></span>
```
Invoke-AzKustoDataConnectionValidation -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -DataConnectionName <String> -EventHubResourceId <String>
 -Kind <Kind> -Location <String> -StorageAccountResourceId <String> [-SubscriptionId <String>]
 [-DataFormat <EventGridDataFormat>] [-MappingRuleName <String>] [-TableName <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="752b2-107">DataExpandedIotHub</span><span class="sxs-lookup"><span data-stu-id="752b2-107">DataExpandedIotHub</span></span>
```
Invoke-AzKustoDataConnectionValidation -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -DataConnectionName <String> -IotHubResourceId <String>
 -Kind <Kind> -Location <String> -SharedAccessPolicyName <String> [-SubscriptionId <String>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="752b2-108">DataViaIdentityExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="752b2-108">DataViaIdentityExpandedEventGrid</span></span>
```
Invoke-AzKustoDataConnectionValidation -InputObject <IKustoIdentity> -ConsumerGroup <String>
 -DataConnectionName <String> -EventHubResourceId <String> -Kind <Kind> -Location <String>
 -StorageAccountResourceId <String> [-DataFormat <EventGridDataFormat>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="752b2-109">DataViaIdentityExpandedEventHub</span><span class="sxs-lookup"><span data-stu-id="752b2-109">DataViaIdentityExpandedEventHub</span></span>
```
Invoke-AzKustoDataConnectionValidation -InputObject <IKustoIdentity> -ConsumerGroup <String>
 -DataConnectionName <String> -EventHubResourceId <String> -Kind <Kind> -Location <String>
 [-Compression <Compression>] [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>]
 [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="752b2-110">DataViaIdentityExpandedIotHub</span><span class="sxs-lookup"><span data-stu-id="752b2-110">DataViaIdentityExpandedIotHub</span></span>
```
Invoke-AzKustoDataConnectionValidation -InputObject <IKustoIdentity> -ConsumerGroup <String>
 -DataConnectionName <String> -IotHubResourceId <String> -Kind <Kind> -Location <String>
 -SharedAccessPolicyName <String> [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>]
 [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="752b2-111">UpdateExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="752b2-111">UpdateExpandedEventGrid</span></span>
```
Invoke-AzKustoDataConnectionValidation -ConsumerGroup <String> -DataConnectionName <String> -Kind <Kind>
 -Location <String> [-BlobStorageEventType <BlobStorageEventType>] [-DataFormat <EventGridDataFormat>]
 [-IgnoreFirstRecord] [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="752b2-112">UpdateViaIdentityExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="752b2-112">UpdateViaIdentityExpandedEventGrid</span></span>
```
Invoke-AzKustoDataConnectionValidation -ConsumerGroup <String> -DataConnectionName <String> -Kind <Kind>
 -Location <String> [-BlobStorageEventType <BlobStorageEventType>] [-DataFormat <EventGridDataFormat>]
 [-IgnoreFirstRecord] [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="752b2-113">설명은</span><span class="sxs-lookup"><span data-stu-id="752b2-113">DESCRIPTION</span></span>
<span data-ttu-id="752b2-114">데이터 연결 매개 변수가 유효한 지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="752b2-114">Checks that the data connection parameters are valid.</span></span>

## <span data-ttu-id="752b2-115">예제의</span><span class="sxs-lookup"><span data-stu-id="752b2-115">EXAMPLES</span></span>

### <span data-ttu-id="752b2-116">예제 1: EventHub 데이터 연결 매개 변수 유효성 검사</span><span class="sxs-lookup"><span data-stu-id="752b2-116">Example 1: Validate EventHub data connection parameters</span></span>
```powershell
PS C:\> Invoke-AzKustoDataConnectionValidation -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventhubdc" -Location "East US" -Kind "EventHub" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -DataFormat "JSON" -ConsumerGroup '$Default' -Compression "None" -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

<span data-ttu-id="752b2-117">위의 명령은 "testnewkustocluster" 클러스터의 "mykustodatabase" 데이터베이스에 대 한 "myeventhubdc" 이라는 EventHub 데이터 연결의 유효성을 검사 합니다.</span><span class="sxs-lookup"><span data-stu-id="752b2-117">The above command validates EventHub data connection named "myeventhubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="752b2-118">예제 2: EventGrid 데이터 연결 매개 변수 유효성 검사</span><span class="sxs-lookup"><span data-stu-id="752b2-118">Example 2: Validate EventGrid data connection parameters</span></span>
```powershell
PS C:\> Invoke-AzKustoDataConnectionValidation -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventgriddc" -Location "East US" -Kind "EventGrid" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -StorageAccountResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Storage/storageAccounts/mystorage" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

<span data-ttu-id="752b2-119">위의 명령은 "testnewkustocluster" 클러스터의 "mykustodatabase" 데이터베이스에 대 한 "myeventgriddc" 라는 EventGrid 데이터 연결의 유효성을 검사 합니다.</span><span class="sxs-lookup"><span data-stu-id="752b2-119">The above command validates EventGrid data connection named "myeventgriddc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="752b2-120">예제 3: IotHub data connection 매개 변수 유효성 검사</span><span class="sxs-lookup"><span data-stu-id="752b2-120">Example 3: Validate IotHub data connection parameters</span></span>
```powershell
PS C:\> Invoke-AzKustoDataConnectionValidation -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myiothubdc" -Location "East US" -Kind "IotHub" -IotHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Devices/IotHubs/myiothub" -SharedAccessPolicyName "myiothubpolicy" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

<span data-ttu-id="752b2-121">위의 명령은 "mykustodatabase" 데이터베이스의 "myiothubdc" IotHub 데이터 연결을 "testnewkustocluster" 클러스터의 유효성을 검사 합니다.</span><span class="sxs-lookup"><span data-stu-id="752b2-121">The above command validates IotHub data connection named "myiothubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="752b2-122">예제 4: id를 통해 EventHub 데이터 연결 매개 변수 유효성 검사</span><span class="sxs-lookup"><span data-stu-id="752b2-122">Example 4: Validate EventHub data connection parameters via identity</span></span>
```powershell
PS C:\> $database = Get-AzKustoDatabase -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" 
PS C:\> Invoke-AzKustoDataConnectionValidation -InputObject $database -DataConnectionName "myeventhubdc" -Location "East US" -Kind "EventHub" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -DataFormat "JSON" -ConsumerGroup '$Default' -Compression "None" -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

<span data-ttu-id="752b2-123">위의 명령은 "testnewkustocluster" 클러스터의 "mykustodatabase" 데이터베이스에 대 한 "myeventhubdc" 이라는 EventHub 데이터 연결의 유효성을 검사 합니다.</span><span class="sxs-lookup"><span data-stu-id="752b2-123">The above command validates EventHub data connection named "myeventhubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="752b2-124">예제 5: id를 통해 EventGrid 데이터 연결 매개 변수 유효성 검사</span><span class="sxs-lookup"><span data-stu-id="752b2-124">Example 5: Validate EventGrid data connection parameters via identity</span></span>
```powershell
PS C:\> $database = Get-AzKustoDatabase -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase"
PS C:\> Invoke-AzKustoDataConnectionValidation -InputObject $database -DataConnectionName "myeventgriddc" -Location "East US" -Kind "EventGrid" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -StorageAccountResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Storage/storageAccounts/mystorage" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

<span data-ttu-id="752b2-125">위의 명령은 "testnewkustocluster" 클러스터의 "mykustodatabase" 데이터베이스에 대 한 "myeventgriddc" 라는 EventGrid 데이터 연결의 유효성을 검사 합니다.</span><span class="sxs-lookup"><span data-stu-id="752b2-125">The above command validates EventGrid data connection named "myeventgriddc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="752b2-126">예제 6: id를 통해 IotHub 데이터 연결 매개 변수 유효성 검사</span><span class="sxs-lookup"><span data-stu-id="752b2-126">Example 6: Validate IotHub data connection parameters via identity</span></span>
```powershell
PS C:\> $database = Get-AzKustoDatabase -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" 
PS C:\> Invoke-AzKustoDataConnectionValidation -InputObject $database -DataConnectionName "myiothubdc" -Location "East US" -Kind "IotHub" -IotHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Devices/IotHubs/myiothub" -SharedAccessPolicyName "myiothubpolicy" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

<span data-ttu-id="752b2-127">위의 명령은 "mykustodatabase" 데이터베이스의 "myiothubdc" IotHub 데이터 연결을 "testnewkustocluster" 클러스터의 유효성을 검사 합니다.</span><span class="sxs-lookup"><span data-stu-id="752b2-127">The above command validates IotHub data connection named "myiothubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="752b2-128">변수</span><span class="sxs-lookup"><span data-stu-id="752b2-128">PARAMETERS</span></span>

### <span data-ttu-id="752b2-129">-BlobStorageEventType</span><span class="sxs-lookup"><span data-stu-id="752b2-129">-BlobStorageEventType</span></span>
<span data-ttu-id="752b2-130">처리할 blob 저장소 이벤트 유형의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="752b2-130">The name of blob storage event type to process.</span></span>

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

### <span data-ttu-id="752b2-131">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="752b2-131">-ClusterName</span></span>
<span data-ttu-id="752b2-132">Kusto의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="752b2-132">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: DataExpandedEventGrid, DataExpandedEventHub, DataExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="752b2-133">-압축</span><span class="sxs-lookup"><span data-stu-id="752b2-133">-Compression</span></span>
<span data-ttu-id="752b2-134">이벤트 허브 메시지 압축 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="752b2-134">The event hub messages compression type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.Compression
Parameter Sets: DataExpandedEventHub, DataViaIdentityExpandedEventHub
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="752b2-135">-ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="752b2-135">-ConsumerGroup</span></span>
<span data-ttu-id="752b2-136">이벤트/iot hub 소비자 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="752b2-136">The event/iot hub consumer group.</span></span>

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

### <span data-ttu-id="752b2-137">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="752b2-137">-DatabaseName</span></span>
<span data-ttu-id="752b2-138">Kusto cluster의 데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="752b2-138">The name of the database in the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: DataExpandedEventGrid, DataExpandedEventHub, DataExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="752b2-139">-DataConnectionName</span><span class="sxs-lookup"><span data-stu-id="752b2-139">-DataConnectionName</span></span>
<span data-ttu-id="752b2-140">데이터 연결의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="752b2-140">The name of the data connection.</span></span>

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

### <span data-ttu-id="752b2-141">-DataFormat</span><span class="sxs-lookup"><span data-stu-id="752b2-141">-DataFormat</span></span>
<span data-ttu-id="752b2-142">메시지의 데이터 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="752b2-142">The data format of the message.</span></span>
<span data-ttu-id="752b2-143">필요에 따라 각 메시지에 데이터 형식을 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="752b2-143">Optionally the data format can be added to each message.</span></span>

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

### <span data-ttu-id="752b2-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="752b2-144">-DefaultProfile</span></span>
<span data-ttu-id="752b2-145">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="752b2-145">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="752b2-146">-EventHubResourceId</span><span class="sxs-lookup"><span data-stu-id="752b2-146">-EventHubResourceId</span></span>
<span data-ttu-id="752b2-147">데이터 연결/이벤트 그리드를 만드는 데 사용할 이벤트 허브의 리소스 ID가 이벤트를 보내도록 구성 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="752b2-147">The resource ID of the event hub to be used to create a data connection / event grid is configured to send events.</span></span>

```yaml
Type: System.String
Parameter Sets: DataExpandedEventGrid, DataExpandedEventHub, DataViaIdentityExpandedEventGrid, DataViaIdentityExpandedEventHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="752b2-148">-EventSystemProperty</span><span class="sxs-lookup"><span data-stu-id="752b2-148">-EventSystemProperty</span></span>
<span data-ttu-id="752b2-149">이벤트/iot hub의 시스템 속성</span><span class="sxs-lookup"><span data-stu-id="752b2-149">System properties of the event/iot hub.</span></span>

```yaml
Type: System.String[]
Parameter Sets: DataExpandedEventHub, DataExpandedIotHub, DataViaIdentityExpandedEventHub, DataViaIdentityExpandedIotHub
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="752b2-150">-IgnoreFirstRecord</span><span class="sxs-lookup"><span data-stu-id="752b2-150">-IgnoreFirstRecord</span></span>
<span data-ttu-id="752b2-151">True로 설정 되 면 수집에서 모든 파일의 첫 번째 레코드를 무시 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="752b2-151">If set to true, indicates that ingestion should ignore the first record of every file.</span></span>

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

### <span data-ttu-id="752b2-152">-InputObject</span><span class="sxs-lookup"><span data-stu-id="752b2-152">-InputObject</span></span>
<span data-ttu-id="752b2-153">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="752b2-153">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: DataViaIdentityExpandedEventGrid, DataViaIdentityExpandedEventHub, DataViaIdentityExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="752b2-154">-IotHubResourceId</span><span class="sxs-lookup"><span data-stu-id="752b2-154">-IotHubResourceId</span></span>
<span data-ttu-id="752b2-155">데이터 연결을 만드는 데 사용 되는 Iot hub의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="752b2-155">The resource ID of the Iot hub to be used to create a data connection.</span></span>

```yaml
Type: System.String
Parameter Sets: DataExpandedIotHub, DataViaIdentityExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="752b2-156">-종류</span><span class="sxs-lookup"><span data-stu-id="752b2-156">-Kind</span></span>
<span data-ttu-id="752b2-157">데이터 연결을 위한 끝점의 종류</span><span class="sxs-lookup"><span data-stu-id="752b2-157">Kind of the endpoint for the data connection</span></span>

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

### <span data-ttu-id="752b2-158">-위치</span><span class="sxs-lookup"><span data-stu-id="752b2-158">-Location</span></span>
<span data-ttu-id="752b2-159">리소스 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="752b2-159">Resource location.</span></span>

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

### <span data-ttu-id="752b2-160">-MappingRuleName</span><span class="sxs-lookup"><span data-stu-id="752b2-160">-MappingRuleName</span></span>
<span data-ttu-id="752b2-161">데이터를 수집 하는 데 사용 되는 매핑 규칙입니다.</span><span class="sxs-lookup"><span data-stu-id="752b2-161">The mapping rule to be used to ingest the data.</span></span>
<span data-ttu-id="752b2-162">필요에 따라 각 메시지에 매핑 정보를 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="752b2-162">Optionally the mapping information can be added to each message.</span></span>

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

### <span data-ttu-id="752b2-163">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="752b2-163">-ResourceGroupName</span></span>
<span data-ttu-id="752b2-164">Kusto cluster를 포함 하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="752b2-164">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: DataExpandedEventGrid, DataExpandedEventHub, DataExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="752b2-165">-SharedAccessPolicyName</span><span class="sxs-lookup"><span data-stu-id="752b2-165">-SharedAccessPolicyName</span></span>
<span data-ttu-id="752b2-166">공유 액세스 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="752b2-166">The name of the share access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: DataExpandedIotHub, DataViaIdentityExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="752b2-167">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="752b2-167">-StorageAccountResourceId</span></span>
<span data-ttu-id="752b2-168">데이터가 있는 저장소 계정의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="752b2-168">The resource ID of the storage account where the data resides.</span></span>

```yaml
Type: System.String
Parameter Sets: DataExpandedEventGrid, DataViaIdentityExpandedEventGrid
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="752b2-169">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="752b2-169">-SubscriptionId</span></span>
<span data-ttu-id="752b2-170">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="752b2-170">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="752b2-171">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="752b2-171">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: DataExpandedEventGrid, DataExpandedEventHub, DataExpandedIotHub
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="752b2-172">-TableName</span><span class="sxs-lookup"><span data-stu-id="752b2-172">-TableName</span></span>
<span data-ttu-id="752b2-173">데이터를 ingested 하는 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="752b2-173">The table where the data should be ingested.</span></span>
<span data-ttu-id="752b2-174">필요에 따라 각 메시지에 테이블 정보를 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="752b2-174">Optionally the table information can be added to each message.</span></span>

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

### <span data-ttu-id="752b2-175">-확인</span><span class="sxs-lookup"><span data-stu-id="752b2-175">-Confirm</span></span>
<span data-ttu-id="752b2-176">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="752b2-176">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="752b2-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="752b2-177">-WhatIf</span></span>
<span data-ttu-id="752b2-178">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="752b2-178">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="752b2-179">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="752b2-179">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="752b2-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="752b2-180">CommonParameters</span></span>
<span data-ttu-id="752b2-181">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="752b2-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="752b2-182">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="752b2-182">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="752b2-183">입력</span><span class="sxs-lookup"><span data-stu-id="752b2-183">INPUTS</span></span>

### <span data-ttu-id="752b2-184">IKustoIdentity (Microsoft. PowerShell. m a us</span><span class="sxs-lookup"><span data-stu-id="752b2-184">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="752b2-185">출력</span><span class="sxs-lookup"><span data-stu-id="752b2-185">OUTPUTS</span></span>

### <span data-ttu-id="752b2-186">Microsoft. Api20200614. IDataConnectionValidationResult에 대 한.</span><span class="sxs-lookup"><span data-stu-id="752b2-186">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDataConnectionValidationResult</span></span>

## <span data-ttu-id="752b2-187">상속자</span><span class="sxs-lookup"><span data-stu-id="752b2-187">NOTES</span></span>

<span data-ttu-id="752b2-188">별칭과</span><span class="sxs-lookup"><span data-stu-id="752b2-188">ALIASES</span></span>

<span data-ttu-id="752b2-189">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="752b2-189">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="752b2-190">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="752b2-190">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="752b2-191">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="752b2-191">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="752b2-192">INPUTOBJECT <IKustoIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="752b2-192">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="752b2-193">`[AttachedDatabaseConfigurationName <String>]`: 연결 된 데이터베이스 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="752b2-193">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="752b2-194">`[ClusterName <String>]`: Kusto의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="752b2-194">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="752b2-195">`[DataConnectionName <String>]`: 데이터 연결의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="752b2-195">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="752b2-196">`[DatabaseName <String>]`: Kusto cluster의 데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="752b2-196">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="752b2-197">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="752b2-197">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="752b2-198">`[Location <String>]`: Azure 위치.</span><span class="sxs-lookup"><span data-stu-id="752b2-198">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="752b2-199">`[PrincipalAssignmentName <String>]`:%에 대 한 Kusto principalAssignment의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="752b2-199">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="752b2-200">`[ResourceGroupName <String>]`: Kusto cluster를 포함 하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="752b2-200">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="752b2-201">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="752b2-201">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="752b2-202">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="752b2-202">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="752b2-203">관련 링크</span><span class="sxs-lookup"><span data-stu-id="752b2-203">RELATED LINKS</span></span>

