---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/update-azkustodataconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoDataConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoDataConnection.md
ms.openlocfilehash: 94a0764b61b32ce55ff4d9aca06a22d67b1edc96
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008987"
---
# <span data-ttu-id="2aa0b-101">Update-AzKustoDataConnection</span><span class="sxs-lookup"><span data-stu-id="2aa0b-101">Update-AzKustoDataConnection</span></span>

## <span data-ttu-id="2aa0b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2aa0b-102">SYNOPSIS</span></span>
<span data-ttu-id="2aa0b-103">데이터 연결을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="2aa0b-103">Updates a data connection.</span></span>

## <span data-ttu-id="2aa0b-104">구문</span><span class="sxs-lookup"><span data-stu-id="2aa0b-104">SYNTAX</span></span>

### <span data-ttu-id="2aa0b-105">UpdateExpandedEventHub(기본값)</span><span class="sxs-lookup"><span data-stu-id="2aa0b-105">UpdateExpandedEventHub (Default)</span></span>
```
Update-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -EventHubResourceId <String> -Kind <Kind>
 -Location <String> [-SubscriptionId <String>] [-Compression <Compression>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="2aa0b-106">UpdateExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="2aa0b-106">UpdateExpandedEventGrid</span></span>
```
Update-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -EventHubResourceId <String> -Kind <Kind>
 -Location <String> -StorageAccountResourceId <String> [-SubscriptionId <String>]
 [-BlobStorageEventType <BlobStorageEventType>] [-DataFormat <EventGridDataFormat>] [-IgnoreFirstRecord]
 [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="2aa0b-107">UpdateExpandedIotHub</span><span class="sxs-lookup"><span data-stu-id="2aa0b-107">UpdateExpandedIotHub</span></span>
```
Update-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -IotHubResourceId <String> -Kind <Kind>
 -Location <String> -SharedAccessPolicyName <String> [-SubscriptionId <String>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="2aa0b-108">UpdateViaIdentityExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="2aa0b-108">UpdateViaIdentityExpandedEventGrid</span></span>
```
Update-AzKustoDataConnection -InputObject <IKustoIdentity> -ConsumerGroup <String>
 -EventHubResourceId <String> -Kind <Kind> -Location <String> -StorageAccountResourceId <String>
 [-BlobStorageEventType <BlobStorageEventType>] [-DataFormat <EventGridDataFormat>] [-IgnoreFirstRecord]
 [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="2aa0b-109">UpdateViaIdentityExpandedEventHub</span><span class="sxs-lookup"><span data-stu-id="2aa0b-109">UpdateViaIdentityExpandedEventHub</span></span>
```
Update-AzKustoDataConnection -InputObject <IKustoIdentity> -ConsumerGroup <String>
 -EventHubResourceId <String> -Kind <Kind> -Location <String> [-Compression <Compression>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="2aa0b-110">UpdateViaIdentityExpandedIotHub</span><span class="sxs-lookup"><span data-stu-id="2aa0b-110">UpdateViaIdentityExpandedIotHub</span></span>
```
Update-AzKustoDataConnection -InputObject <IKustoIdentity> -ConsumerGroup <String> -IotHubResourceId <String>
 -Kind <Kind> -Location <String> -SharedAccessPolicyName <String> [-DataFormat <EventGridDataFormat>]
 [-EventSystemProperty <String[]>] [-MappingRuleName <String>] [-TableName <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2aa0b-111">설명</span><span class="sxs-lookup"><span data-stu-id="2aa0b-111">DESCRIPTION</span></span>
<span data-ttu-id="2aa0b-112">데이터 연결을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="2aa0b-112">Updates a data connection.</span></span>

## <span data-ttu-id="2aa0b-113">예제</span><span class="sxs-lookup"><span data-stu-id="2aa0b-113">EXAMPLES</span></span>

### <span data-ttu-id="2aa0b-114">예제 1: 기존 EventHub 데이터 연결 업데이트</span><span class="sxs-lookup"><span data-stu-id="2aa0b-114">Example 1: Update an existing EventHub data connection</span></span>
```powershell
PS C:\> Update-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventhubdc" -Location="East US" -Kind "EventHub" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -DataFormat "JSON" -ConsumerGroup '$Default' -Compression "None" -TableName "Events" -MappingRuleName "NewEventsMapping"

Kind     Location Name                                             Type
----     -------- ----                                             ----
EventHub East US  testnewkustocluster/mykustodatabase/myeventhubdc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="2aa0b-115">위의 명령은 "testnewkustocluster"의 데이터베이스 "mykustodatabase"에 대해 "myeventhubdc"라는 기존 EventHub 데이터 연결을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="2aa0b-115">The above command updates the existing EventHub data connection named "myeventhubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="2aa0b-116">예제 2: 기존 EventGrid 데이터 연결 업데이트</span><span class="sxs-lookup"><span data-stu-id="2aa0b-116">Example 2: Update an existing EventGrid data connection</span></span>
```powershell
PS C:\> Update-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventgriddc" -Location="East US" -Kind "EventGrid" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -StorageAccountResourceId $storageAccountResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Storage/storageAccounts/mystorage" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

Kind      Location Name                                              Type
----      -------- ----                                              ----
EventGrid East US  testnewkustocluster/mykustodatabase/myeventgriddc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="2aa0b-117">위의 명령은 클러스터 "testnewkustocluster"의 데이터베이스 "mykustodatabase"에 대해 "myeventgriddc"라는 기존 EventGrid 데이터 연결을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="2aa0b-117">The above command updates the existing EventGrid data connection named "myeventgriddc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="2aa0b-118">예제 3: 기존 IotHub 데이터 연결 업데이트</span><span class="sxs-lookup"><span data-stu-id="2aa0b-118">Example 3: Update an existing IotHub data connection</span></span>
```powershell
PS C:\> Update-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myiothubdc" -Location="East US" -Kind "IotHub" -IotHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Devices/IotHubs/myiothub" -SharedAccessPolicyName "myiothubpolicy" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

Kind      Location Name                                        Type
----      -------- ----                                        ----
IotHub East US  testnewkustocluster/mykustodatabase/myiothubdc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="2aa0b-119">위의 명령은 "testnewkustocluster"의 데이터베이스 "mykustodatabase"에 대해 "myiothubdc"라는 기존 IotHub 데이터 연결을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="2aa0b-119">The above command updates the existing IotHub data connection named "myiothubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="2aa0b-120">예제 4: ID를 통해 기존 EventHub 데이터 연결 업데이트</span><span class="sxs-lookup"><span data-stu-id="2aa0b-120">Example 4: Update an existing EventHub data connection via identity</span></span>
```powershell
PS C:\> $dataConnection = Get-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventhubdc" 
PS C:\> Update-AzKustoDataConnection -InputObject $dataConnection -Location="East US" -Kind "EventHub" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -DataFormat "JSON" -ConsumerGroup '$Default' -Compression "None" -TableName "Events" -MappingRuleName "NewEventsMapping"

Kind     Location Name                                             Type
----     -------- ----                                             ----
EventHub East US  testnewkustocluster/mykustodatabase/myeventhubdc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="2aa0b-121">위의 명령은 "testnewkustocluster"의 데이터베이스 "mykustodatabase"에 대해 "myeventhubdc"라는 기존 EventHub 데이터 연결을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="2aa0b-121">The above command updates the existing EventHub data connection named "myeventhubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="2aa0b-122">예제 5: ID를 통해 기존 EventGrid 데이터 연결 업데이트</span><span class="sxs-lookup"><span data-stu-id="2aa0b-122">Example 5: Update an existing EventGrid data connection via identity</span></span>
```powershell
PS C:\> $dataConnection = Get-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventgriddc" 
PS C:\> Update-AzKustoDataConnection -InputObject $dataConnection -Location="East US" -Kind "EventGrid" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -StorageAccountResourceId $storageAccountResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Storage/storageAccounts/mystorage" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

Kind      Location Name                                              Type
----      -------- ----                                              ----
EventGrid East US  testnewkustocluster/mykustodatabase/myeventgriddc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="2aa0b-123">위의 명령은 클러스터 "testnewkustocluster"의 데이터베이스 "mykustodatabase"에 대해 "myeventgriddc"라는 기존 EventGrid 데이터 연결을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="2aa0b-123">The above command updates the existing EventGrid data connection named "myeventgriddc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="2aa0b-124">예제 6: ID를 통해 기존 IotHub 데이터 연결 업데이트</span><span class="sxs-lookup"><span data-stu-id="2aa0b-124">Example 6: Update an existing IotHub data connection via identity</span></span>
```powershell
PS C:\> $dataConnection = Get-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myiothubdc" 
PS C:\> Update-AzKustoDataConnection -InputObject $dataConnection -Location="East US" -Kind "IotHub" -IotHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Devices/IotHubs/myiothub" -SharedAccessPolicyName "myiothubpolicy" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

Kind      Location Name                                        Type
----      -------- ----                                        ----
IotHub East US  testnewkustocluster/mykustodatabase/myiothubdc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="2aa0b-125">위의 명령은 "testnewkustocluster"의 데이터베이스 "mykustodatabase"에 대해 "myiothubdc"라는 기존 IotHub 데이터 연결을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="2aa0b-125">The above command updates the existing IotHub data connection named "myiothubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="2aa0b-126">매개 변수</span><span class="sxs-lookup"><span data-stu-id="2aa0b-126">PARAMETERS</span></span>

### <span data-ttu-id="2aa0b-127">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2aa0b-127">-AsJob</span></span>
<span data-ttu-id="2aa0b-128">작업으로 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="2aa0b-128">Run the command as a job</span></span>

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

### <span data-ttu-id="2aa0b-129">-BlobStorageEventType</span><span class="sxs-lookup"><span data-stu-id="2aa0b-129">-BlobStorageEventType</span></span>
<span data-ttu-id="2aa0b-130">처리할 Blob Storage 이벤트 형식의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2aa0b-130">The name of blob storage event type to process.</span></span>

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

### <span data-ttu-id="2aa0b-131">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="2aa0b-131">-ClusterName</span></span>
<span data-ttu-id="2aa0b-132">Kusto 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2aa0b-132">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpandedEventGrid, UpdateExpandedEventHub, UpdateExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2aa0b-133">-압축</span><span class="sxs-lookup"><span data-stu-id="2aa0b-133">-Compression</span></span>
<span data-ttu-id="2aa0b-134">이벤트 허브 메시지 압축 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="2aa0b-134">The event hub messages compression type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.Compression
Parameter Sets: UpdateExpandedEventHub, UpdateViaIdentityExpandedEventHub
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2aa0b-135">-ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="2aa0b-135">-ConsumerGroup</span></span>
<span data-ttu-id="2aa0b-136">이벤트/iot Hub 소비자 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="2aa0b-136">The event/iot hub consumer group.</span></span>

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

### <span data-ttu-id="2aa0b-137">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2aa0b-137">-DatabaseName</span></span>
<span data-ttu-id="2aa0b-138">Kusto 클러스터의 데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2aa0b-138">The name of the database in the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpandedEventGrid, UpdateExpandedEventHub, UpdateExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2aa0b-139">-DataFormat</span><span class="sxs-lookup"><span data-stu-id="2aa0b-139">-DataFormat</span></span>
<span data-ttu-id="2aa0b-140">메시지의 데이터 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="2aa0b-140">The data format of the message.</span></span>
<span data-ttu-id="2aa0b-141">선택적으로 데이터 형식을 각 메시지에 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2aa0b-141">Optionally the data format can be added to each message.</span></span>

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

### <span data-ttu-id="2aa0b-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2aa0b-142">-DefaultProfile</span></span>
<span data-ttu-id="2aa0b-143">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2aa0b-143">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2aa0b-144">-EventHubResourceId</span><span class="sxs-lookup"><span data-stu-id="2aa0b-144">-EventHubResourceId</span></span>
<span data-ttu-id="2aa0b-145">데이터 연결/이벤트 그리드를 만드는 데 사용할 이벤트 허브의 리소스 ID는 이벤트를 보내도록 구성됩니다.</span><span class="sxs-lookup"><span data-stu-id="2aa0b-145">The resource ID of the event hub to be used to create a data connection / event grid is configured to send events.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpandedEventGrid, UpdateExpandedEventHub, UpdateViaIdentityExpandedEventGrid, UpdateViaIdentityExpandedEventHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2aa0b-146">-EventSystemProperty</span><span class="sxs-lookup"><span data-stu-id="2aa0b-146">-EventSystemProperty</span></span>
<span data-ttu-id="2aa0b-147">이벤트/iot 허브의 시스템 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="2aa0b-147">System properties of the event/iot hub.</span></span>

```yaml
Type: System.String[]
Parameter Sets: UpdateExpandedEventHub, UpdateExpandedIotHub, UpdateViaIdentityExpandedEventHub, UpdateViaIdentityExpandedIotHub
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2aa0b-148">-IgnoreFirstRecord</span><span class="sxs-lookup"><span data-stu-id="2aa0b-148">-IgnoreFirstRecord</span></span>
<span data-ttu-id="2aa0b-149">true로 설정하면 모든 파일의 첫 번째 레코드를 무시해야 한다고 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="2aa0b-149">If set to true, indicates that ingestion should ignore the first record of every file.</span></span>

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

### <span data-ttu-id="2aa0b-150">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2aa0b-150">-InputObject</span></span>
<span data-ttu-id="2aa0b-151">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="2aa0b-151">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: UpdateViaIdentityExpandedEventGrid, UpdateViaIdentityExpandedEventHub, UpdateViaIdentityExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2aa0b-152">-IotHubResourceId</span><span class="sxs-lookup"><span data-stu-id="2aa0b-152">-IotHubResourceId</span></span>
<span data-ttu-id="2aa0b-153">데이터 연결을 만드는 데 사용할 Iot Hub의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="2aa0b-153">The resource ID of the Iot hub to be used to create a data connection.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpandedIotHub, UpdateViaIdentityExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2aa0b-154">-Kind</span><span class="sxs-lookup"><span data-stu-id="2aa0b-154">-Kind</span></span>
<span data-ttu-id="2aa0b-155">데이터 연결에 대한 엔드포인트의 종류</span><span class="sxs-lookup"><span data-stu-id="2aa0b-155">Kind of the endpoint for the data connection</span></span>

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

### <span data-ttu-id="2aa0b-156">-Location</span><span class="sxs-lookup"><span data-stu-id="2aa0b-156">-Location</span></span>
<span data-ttu-id="2aa0b-157">리소스 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="2aa0b-157">Resource location.</span></span>

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

### <span data-ttu-id="2aa0b-158">-MappingRuleName</span><span class="sxs-lookup"><span data-stu-id="2aa0b-158">-MappingRuleName</span></span>
<span data-ttu-id="2aa0b-159">데이터를 수집하는 데 사용할 매핑 규칙입니다.</span><span class="sxs-lookup"><span data-stu-id="2aa0b-159">The mapping rule to be used to ingest the data.</span></span>
<span data-ttu-id="2aa0b-160">선택적으로 매핑 정보를 각 메시지에 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2aa0b-160">Optionally the mapping information can be added to each message.</span></span>

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

### <span data-ttu-id="2aa0b-161">-Name</span><span class="sxs-lookup"><span data-stu-id="2aa0b-161">-Name</span></span>
<span data-ttu-id="2aa0b-162">데이터 연결의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2aa0b-162">The name of the data connection.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpandedEventGrid, UpdateExpandedEventHub, UpdateExpandedIotHub
Aliases: DataConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2aa0b-163">-NoWait</span><span class="sxs-lookup"><span data-stu-id="2aa0b-163">-NoWait</span></span>
<span data-ttu-id="2aa0b-164">명령 비동기 실행</span><span class="sxs-lookup"><span data-stu-id="2aa0b-164">Run the command asynchronously</span></span>

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

### <span data-ttu-id="2aa0b-165">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2aa0b-165">-ResourceGroupName</span></span>
<span data-ttu-id="2aa0b-166">Kusto 클러스터를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2aa0b-166">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpandedEventGrid, UpdateExpandedEventHub, UpdateExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2aa0b-167">-SharedAccessPolicyName</span><span class="sxs-lookup"><span data-stu-id="2aa0b-167">-SharedAccessPolicyName</span></span>
<span data-ttu-id="2aa0b-168">공유 액세스 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2aa0b-168">The name of the share access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpandedIotHub, UpdateViaIdentityExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2aa0b-169">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="2aa0b-169">-StorageAccountResourceId</span></span>
<span data-ttu-id="2aa0b-170">데이터가 있는 저장소 계정의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="2aa0b-170">The resource ID of the storage account where the data resides.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpandedEventGrid, UpdateViaIdentityExpandedEventGrid
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2aa0b-171">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2aa0b-171">-SubscriptionId</span></span>
<span data-ttu-id="2aa0b-172">Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="2aa0b-172">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="2aa0b-173">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="2aa0b-173">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpandedEventGrid, UpdateExpandedEventHub, UpdateExpandedIotHub
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2aa0b-174">-TableName</span><span class="sxs-lookup"><span data-stu-id="2aa0b-174">-TableName</span></span>
<span data-ttu-id="2aa0b-175">데이터를 수집해야 하는 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="2aa0b-175">The table where the data should be ingested.</span></span>
<span data-ttu-id="2aa0b-176">선택적으로 표 정보를 각 메시지에 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2aa0b-176">Optionally the table information can be added to each message.</span></span>

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

### <span data-ttu-id="2aa0b-177">-확인</span><span class="sxs-lookup"><span data-stu-id="2aa0b-177">-Confirm</span></span>
<span data-ttu-id="2aa0b-178">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="2aa0b-178">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2aa0b-179">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2aa0b-179">-WhatIf</span></span>
<span data-ttu-id="2aa0b-180">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="2aa0b-180">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2aa0b-181">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2aa0b-181">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2aa0b-182">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2aa0b-182">CommonParameters</span></span>
<span data-ttu-id="2aa0b-183">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2aa0b-183">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2aa0b-184">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2aa0b-184">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2aa0b-185">입력</span><span class="sxs-lookup"><span data-stu-id="2aa0b-185">INPUTS</span></span>

### <span data-ttu-id="2aa0b-186">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="2aa0b-186">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="2aa0b-187">출력</span><span class="sxs-lookup"><span data-stu-id="2aa0b-187">OUTPUTS</span></span>

### <span data-ttu-id="2aa0b-188">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDataConnection</span><span class="sxs-lookup"><span data-stu-id="2aa0b-188">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDataConnection</span></span>

## <span data-ttu-id="2aa0b-189">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2aa0b-189">NOTES</span></span>

<span data-ttu-id="2aa0b-190">별칭</span><span class="sxs-lookup"><span data-stu-id="2aa0b-190">ALIASES</span></span>

<span data-ttu-id="2aa0b-191">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="2aa0b-191">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2aa0b-192">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="2aa0b-192">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2aa0b-193">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2aa0b-193">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2aa0b-194">INPUTOBJECT <IKustoIdentity> : ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="2aa0b-194">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2aa0b-195">`[AttachedDatabaseConfigurationName <String>]`: 연결된 데이터베이스 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2aa0b-195">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="2aa0b-196">`[ClusterName <String>]`: Kusto 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2aa0b-196">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="2aa0b-197">`[DataConnectionName <String>]`: 데이터 연결의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2aa0b-197">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="2aa0b-198">`[DatabaseName <String>]`: Kusto 클러스터의 데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2aa0b-198">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="2aa0b-199">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="2aa0b-199">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2aa0b-200">`[Location <String>]`: Azure 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="2aa0b-200">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="2aa0b-201">`[PrincipalAssignmentName <String>]`: Kusto principalAssignment의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2aa0b-201">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="2aa0b-202">`[ResourceGroupName <String>]`: Kusto 클러스터를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2aa0b-202">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="2aa0b-203">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="2aa0b-203">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="2aa0b-204">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="2aa0b-204">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="2aa0b-205">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2aa0b-205">RELATED LINKS</span></span>

