---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/invoke-azkustodataconnectionvalidation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDataConnectionValidation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDataConnectionValidation.md
ms.openlocfilehash: fa75072cdb29d7aedc7a78ba4e20950b904f1c7f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209277"
---
# <span data-ttu-id="3c89b-101">Invoke-AzKustoDataConnectionValidation</span><span class="sxs-lookup"><span data-stu-id="3c89b-101">Invoke-AzKustoDataConnectionValidation</span></span>

## <span data-ttu-id="3c89b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3c89b-102">SYNOPSIS</span></span>
<span data-ttu-id="3c89b-103">데이터 연결 매개 변수가 유효한지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="3c89b-103">Checks that the data connection parameters are valid.</span></span>

## <span data-ttu-id="3c89b-104">구문</span><span class="sxs-lookup"><span data-stu-id="3c89b-104">SYNTAX</span></span>

### <span data-ttu-id="3c89b-105">DataExpandedEventHub(기본값)</span><span class="sxs-lookup"><span data-stu-id="3c89b-105">DataExpandedEventHub (Default)</span></span>
```
Invoke-AzKustoDataConnectionValidation -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -DataConnectionName <String> -EventHubResourceId <String>
 -Kind <Kind> -Location <String> [-SubscriptionId <String>] [-Compression <Compression>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3c89b-106">DataExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="3c89b-106">DataExpandedEventGrid</span></span>
```
Invoke-AzKustoDataConnectionValidation -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -DataConnectionName <String> -EventHubResourceId <String>
 -Kind <Kind> -Location <String> -StorageAccountResourceId <String> [-SubscriptionId <String>]
 [-DataFormat <EventGridDataFormat>] [-MappingRuleName <String>] [-TableName <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3c89b-107">DataExpandedIotHub</span><span class="sxs-lookup"><span data-stu-id="3c89b-107">DataExpandedIotHub</span></span>
```
Invoke-AzKustoDataConnectionValidation -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -DataConnectionName <String> -IotHubResourceId <String>
 -Kind <Kind> -Location <String> -SharedAccessPolicyName <String> [-SubscriptionId <String>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3c89b-108">DataViaIdentityExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="3c89b-108">DataViaIdentityExpandedEventGrid</span></span>
```
Invoke-AzKustoDataConnectionValidation -InputObject <IKustoIdentity> -ConsumerGroup <String>
 -DataConnectionName <String> -EventHubResourceId <String> -Kind <Kind> -Location <String>
 -StorageAccountResourceId <String> [-DataFormat <EventGridDataFormat>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3c89b-109">DataViaIdentityExpandedEventHub</span><span class="sxs-lookup"><span data-stu-id="3c89b-109">DataViaIdentityExpandedEventHub</span></span>
```
Invoke-AzKustoDataConnectionValidation -InputObject <IKustoIdentity> -ConsumerGroup <String>
 -DataConnectionName <String> -EventHubResourceId <String> -Kind <Kind> -Location <String>
 [-Compression <Compression>] [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>]
 [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="3c89b-110">DataViaIdentityExpandedIotHub</span><span class="sxs-lookup"><span data-stu-id="3c89b-110">DataViaIdentityExpandedIotHub</span></span>
```
Invoke-AzKustoDataConnectionValidation -InputObject <IKustoIdentity> -ConsumerGroup <String>
 -DataConnectionName <String> -IotHubResourceId <String> -Kind <Kind> -Location <String>
 -SharedAccessPolicyName <String> [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>]
 [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="3c89b-111">UpdateExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="3c89b-111">UpdateExpandedEventGrid</span></span>
```
Invoke-AzKustoDataConnectionValidation -ConsumerGroup <String> -DataConnectionName <String> -Kind <Kind>
 -Location <String> [-BlobStorageEventType <BlobStorageEventType>] [-DataFormat <EventGridDataFormat>]
 [-IgnoreFirstRecord] [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3c89b-112">UpdateViaIdentityExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="3c89b-112">UpdateViaIdentityExpandedEventGrid</span></span>
```
Invoke-AzKustoDataConnectionValidation -ConsumerGroup <String> -DataConnectionName <String> -Kind <Kind>
 -Location <String> [-BlobStorageEventType <BlobStorageEventType>] [-DataFormat <EventGridDataFormat>]
 [-IgnoreFirstRecord] [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3c89b-113">설명</span><span class="sxs-lookup"><span data-stu-id="3c89b-113">DESCRIPTION</span></span>
<span data-ttu-id="3c89b-114">데이터 연결 매개 변수가 유효한지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="3c89b-114">Checks that the data connection parameters are valid.</span></span>

## <span data-ttu-id="3c89b-115">예제</span><span class="sxs-lookup"><span data-stu-id="3c89b-115">EXAMPLES</span></span>

### <span data-ttu-id="3c89b-116">예제 1: EventHub 데이터 연결 매개 변수 유효성 검사</span><span class="sxs-lookup"><span data-stu-id="3c89b-116">Example 1: Validate EventHub data connection parameters</span></span>
```powershell
PS C:\> Invoke-AzKustoDataConnectionValidation -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventhubdc" -Location "East US" -Kind "EventHub" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -DataFormat "JSON" -ConsumerGroup '$Default' -Compression "None" -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

<span data-ttu-id="3c89b-117">위의 명령은 "testnewkustocluster" 클러스터의 "mykustodatabase" 데이터베이스에 대해 "myeventhubdc"라는 EventHub 데이터 연결의 유효성을 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="3c89b-117">The above command validates EventHub data connection named "myeventhubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="3c89b-118">예제 2: EventGrid 데이터 연결 매개 변수 유효성 검사</span><span class="sxs-lookup"><span data-stu-id="3c89b-118">Example 2: Validate EventGrid data connection parameters</span></span>
```powershell
PS C:\> Invoke-AzKustoDataConnectionValidation -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventgriddc" -Location "East US" -Kind "EventGrid" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -StorageAccountResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Storage/storageAccounts/mystorage" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

<span data-ttu-id="3c89b-119">위의 명령은 "testnewkustocluster" 클러스터의 "mykustodatabase" 데이터베이스에 대해 "myeventgriddc"라는 EventGrid 데이터 연결의 유효성을 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="3c89b-119">The above command validates EventGrid data connection named "myeventgriddc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="3c89b-120">예제 3: IotHub 데이터 연결 매개 변수 유효성 검사</span><span class="sxs-lookup"><span data-stu-id="3c89b-120">Example 3: Validate IotHub data connection parameters</span></span>
```powershell
PS C:\> Invoke-AzKustoDataConnectionValidation -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myiothubdc" -Location "East US" -Kind "IotHub" -IotHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Devices/IotHubs/myiothub" -SharedAccessPolicyName "myiothubpolicy" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

<span data-ttu-id="3c89b-121">위의 명령은 "testnewkustocluster" 클러스터의 "mykustodatabase" 데이터베이스에 대해 "myiothubdc"라는 IotHub 데이터 연결의 유효성을 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="3c89b-121">The above command validates IotHub data connection named "myiothubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="3c89b-122">예제 4: ID를 통해 EventHub 데이터 연결 매개 변수 유효성 검사</span><span class="sxs-lookup"><span data-stu-id="3c89b-122">Example 4: Validate EventHub data connection parameters via identity</span></span>
```powershell
PS C:\> $database = Get-AzKustoDatabase -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" 
PS C:\> Invoke-AzKustoDataConnectionValidation -InputObject $database -DataConnectionName "myeventhubdc" -Location "East US" -Kind "EventHub" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -DataFormat "JSON" -ConsumerGroup '$Default' -Compression "None" -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

<span data-ttu-id="3c89b-123">위의 명령은 "testnewkustocluster" 클러스터의 "mykustodatabase" 데이터베이스에 대해 "myeventhubdc"라는 EventHub 데이터 연결의 유효성을 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="3c89b-123">The above command validates EventHub data connection named "myeventhubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="3c89b-124">예제 5: ID를 통해 EventGrid 데이터 연결 매개 변수 유효성 검사</span><span class="sxs-lookup"><span data-stu-id="3c89b-124">Example 5: Validate EventGrid data connection parameters via identity</span></span>
```powershell
PS C:\> $database = Get-AzKustoDatabase -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase"
PS C:\> Invoke-AzKustoDataConnectionValidation -InputObject $database -DataConnectionName "myeventgriddc" -Location "East US" -Kind "EventGrid" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -StorageAccountResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Storage/storageAccounts/mystorage" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

<span data-ttu-id="3c89b-125">위의 명령은 "testnewkustocluster" 클러스터의 "mykustodatabase" 데이터베이스에 대해 "myeventgriddc"라는 EventGrid 데이터 연결의 유효성을 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="3c89b-125">The above command validates EventGrid data connection named "myeventgriddc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="3c89b-126">예제 6: ID를 통해 IotHub 데이터 연결 매개 변수 유효성 검사</span><span class="sxs-lookup"><span data-stu-id="3c89b-126">Example 6: Validate IotHub data connection parameters via identity</span></span>
```powershell
PS C:\> $database = Get-AzKustoDatabase -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" 
PS C:\> Invoke-AzKustoDataConnectionValidation -InputObject $database -DataConnectionName "myiothubdc" -Location "East US" -Kind "IotHub" -IotHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Devices/IotHubs/myiothub" -SharedAccessPolicyName "myiothubpolicy" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

<span data-ttu-id="3c89b-127">위의 명령은 "testnewkustocluster" 클러스터의 "mykustodatabase" 데이터베이스에 대해 "myiothubdc"라는 IotHub 데이터 연결의 유효성을 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="3c89b-127">The above command validates IotHub data connection named "myiothubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="3c89b-128">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3c89b-128">PARAMETERS</span></span>

### <span data-ttu-id="3c89b-129">-BlobStorageEventType</span><span class="sxs-lookup"><span data-stu-id="3c89b-129">-BlobStorageEventType</span></span>
<span data-ttu-id="3c89b-130">처리할 Blob Storage 이벤트 유형의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3c89b-130">The name of blob storage event type to process.</span></span>

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

### <span data-ttu-id="3c89b-131">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="3c89b-131">-ClusterName</span></span>
<span data-ttu-id="3c89b-132">Kusto 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3c89b-132">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="3c89b-133">-Compression</span><span class="sxs-lookup"><span data-stu-id="3c89b-133">-Compression</span></span>
<span data-ttu-id="3c89b-134">이벤트 허브 메시지 압축 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="3c89b-134">The event hub messages compression type.</span></span>

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

### <span data-ttu-id="3c89b-135">-ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="3c89b-135">-ConsumerGroup</span></span>
<span data-ttu-id="3c89b-136">이벤트/iot 허브 소비자 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="3c89b-136">The event/iot hub consumer group.</span></span>

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

### <span data-ttu-id="3c89b-137">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3c89b-137">-DatabaseName</span></span>
<span data-ttu-id="3c89b-138">Kusto 클러스터의 데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3c89b-138">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="3c89b-139">-DataConnectionName</span><span class="sxs-lookup"><span data-stu-id="3c89b-139">-DataConnectionName</span></span>
<span data-ttu-id="3c89b-140">데이터 연결의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3c89b-140">The name of the data connection.</span></span>

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

### <span data-ttu-id="3c89b-141">-DataFormat</span><span class="sxs-lookup"><span data-stu-id="3c89b-141">-DataFormat</span></span>
<span data-ttu-id="3c89b-142">메시지의 데이터 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="3c89b-142">The data format of the message.</span></span>
<span data-ttu-id="3c89b-143">선택적으로 각 메시지에 데이터 형식을 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3c89b-143">Optionally the data format can be added to each message.</span></span>

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

### <span data-ttu-id="3c89b-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c89b-144">-DefaultProfile</span></span>
<span data-ttu-id="3c89b-145">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3c89b-145">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c89b-146">-EventHubResourceId</span><span class="sxs-lookup"><span data-stu-id="3c89b-146">-EventHubResourceId</span></span>
<span data-ttu-id="3c89b-147">데이터 연결을 만드는 데 사용할 이벤트 허브의 리소스 ID/Event Grid가 이벤트를 보내도록 구성됩니다.</span><span class="sxs-lookup"><span data-stu-id="3c89b-147">The resource ID of the event hub to be used to create a data connection / event grid is configured to send events.</span></span>

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

### <span data-ttu-id="3c89b-148">-EventSystemProperty</span><span class="sxs-lookup"><span data-stu-id="3c89b-148">-EventSystemProperty</span></span>
<span data-ttu-id="3c89b-149">이벤트/iot 허브의 시스템 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="3c89b-149">System properties of the event/iot hub.</span></span>

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

### <span data-ttu-id="3c89b-150">-IgnoreFirstRecord</span><span class="sxs-lookup"><span data-stu-id="3c89b-150">-IgnoreFirstRecord</span></span>
<span data-ttu-id="3c89b-151">true로 설정하면 모든 파일의 첫 번째 레코드를 무시해야 한다고 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="3c89b-151">If set to true, indicates that ingestion should ignore the first record of every file.</span></span>

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

### <span data-ttu-id="3c89b-152">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3c89b-152">-InputObject</span></span>
<span data-ttu-id="3c89b-153">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="3c89b-153">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="3c89b-154">-IotHubResourceId</span><span class="sxs-lookup"><span data-stu-id="3c89b-154">-IotHubResourceId</span></span>
<span data-ttu-id="3c89b-155">데이터 연결을 만드는 데 사용할 Iot Hub의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="3c89b-155">The resource ID of the Iot hub to be used to create a data connection.</span></span>

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

### <span data-ttu-id="3c89b-156">-Kind</span><span class="sxs-lookup"><span data-stu-id="3c89b-156">-Kind</span></span>
<span data-ttu-id="3c89b-157">데이터 연결에 대한 엔드포인트의 종류</span><span class="sxs-lookup"><span data-stu-id="3c89b-157">Kind of the endpoint for the data connection</span></span>

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

### <span data-ttu-id="3c89b-158">-Location</span><span class="sxs-lookup"><span data-stu-id="3c89b-158">-Location</span></span>
<span data-ttu-id="3c89b-159">리소스 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="3c89b-159">Resource location.</span></span>

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

### <span data-ttu-id="3c89b-160">-MappingRuleName</span><span class="sxs-lookup"><span data-stu-id="3c89b-160">-MappingRuleName</span></span>
<span data-ttu-id="3c89b-161">데이터를 수집하는 데 사용할 매핑 규칙입니다.</span><span class="sxs-lookup"><span data-stu-id="3c89b-161">The mapping rule to be used to ingest the data.</span></span>
<span data-ttu-id="3c89b-162">선택적으로 매핑 정보를 각 메시지에 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3c89b-162">Optionally the mapping information can be added to each message.</span></span>

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

### <span data-ttu-id="3c89b-163">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c89b-163">-ResourceGroupName</span></span>
<span data-ttu-id="3c89b-164">Kusto 클러스터를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3c89b-164">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="3c89b-165">-SharedAccessPolicyName</span><span class="sxs-lookup"><span data-stu-id="3c89b-165">-SharedAccessPolicyName</span></span>
<span data-ttu-id="3c89b-166">공유 액세스 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3c89b-166">The name of the share access policy.</span></span>

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

### <span data-ttu-id="3c89b-167">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="3c89b-167">-StorageAccountResourceId</span></span>
<span data-ttu-id="3c89b-168">데이터가 있는 저장소 계정의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="3c89b-168">The resource ID of the storage account where the data resides.</span></span>

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

### <span data-ttu-id="3c89b-169">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3c89b-169">-SubscriptionId</span></span>
<span data-ttu-id="3c89b-170">Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="3c89b-170">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="3c89b-171">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="3c89b-171">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="3c89b-172">-TableName</span><span class="sxs-lookup"><span data-stu-id="3c89b-172">-TableName</span></span>
<span data-ttu-id="3c89b-173">데이터를 수집해야 하는 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="3c89b-173">The table where the data should be ingested.</span></span>
<span data-ttu-id="3c89b-174">선택적으로 테이블 정보를 각 메시지에 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3c89b-174">Optionally the table information can be added to each message.</span></span>

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

### <span data-ttu-id="3c89b-175">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3c89b-175">-Confirm</span></span>
<span data-ttu-id="3c89b-176">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="3c89b-176">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c89b-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c89b-177">-WhatIf</span></span>
<span data-ttu-id="3c89b-178">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="3c89b-178">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c89b-179">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3c89b-179">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c89b-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c89b-180">CommonParameters</span></span>
<span data-ttu-id="3c89b-181">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3c89b-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c89b-182">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3c89b-182">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c89b-183">입력</span><span class="sxs-lookup"><span data-stu-id="3c89b-183">INPUTS</span></span>

### <span data-ttu-id="3c89b-184">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="3c89b-184">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="3c89b-185">출력</span><span class="sxs-lookup"><span data-stu-id="3c89b-185">OUTPUTS</span></span>

### <span data-ttu-id="3c89b-186">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDataConnectionValidationResult</span><span class="sxs-lookup"><span data-stu-id="3c89b-186">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDataConnectionValidationResult</span></span>

## <span data-ttu-id="3c89b-187">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3c89b-187">NOTES</span></span>

<span data-ttu-id="3c89b-188">별칭</span><span class="sxs-lookup"><span data-stu-id="3c89b-188">ALIASES</span></span>

<span data-ttu-id="3c89b-189">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="3c89b-189">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3c89b-190">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="3c89b-190">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3c89b-191">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3c89b-191">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3c89b-192">INPUTOBJECT: <IKustoIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="3c89b-192">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3c89b-193">`[AttachedDatabaseConfigurationName <String>]`: 연결된 데이터베이스 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3c89b-193">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="3c89b-194">`[ClusterName <String>]`: Kusto 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3c89b-194">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="3c89b-195">`[DataConnectionName <String>]`: 데이터 연결의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3c89b-195">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="3c89b-196">`[DatabaseName <String>]`: Kusto 클러스터의 데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3c89b-196">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="3c89b-197">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="3c89b-197">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3c89b-198">`[Location <String>]`: Azure 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="3c89b-198">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="3c89b-199">`[PrincipalAssignmentName <String>]`: Kusto principalAssignment의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3c89b-199">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="3c89b-200">`[ResourceGroupName <String>]`: Kusto 클러스터를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3c89b-200">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="3c89b-201">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="3c89b-201">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="3c89b-202">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="3c89b-202">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="3c89b-203">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3c89b-203">RELATED LINKS</span></span>
