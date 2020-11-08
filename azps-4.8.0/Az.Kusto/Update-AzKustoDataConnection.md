---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/update-azkustodataconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoDataConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoDataConnection.md
ms.openlocfilehash: 70862dee30fd03430d93de88e1e63f0f5acf5e6c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214493"
---
# <span data-ttu-id="5d607-101">Update-AzKustoDataConnection</span><span class="sxs-lookup"><span data-stu-id="5d607-101">Update-AzKustoDataConnection</span></span>

## <span data-ttu-id="5d607-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d607-102">SYNOPSIS</span></span>
<span data-ttu-id="5d607-103">데이터 연결을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d607-103">Updates a data connection.</span></span>

## <span data-ttu-id="5d607-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5d607-104">SYNTAX</span></span>

### <span data-ttu-id="5d607-105">UpdateExpandedEventHub (기본값)</span><span class="sxs-lookup"><span data-stu-id="5d607-105">UpdateExpandedEventHub (Default)</span></span>
```
Update-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -EventHubResourceId <String> -Kind <Kind>
 -Location <String> [-SubscriptionId <String>] [-Compression <Compression>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="5d607-106">UpdateExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="5d607-106">UpdateExpandedEventGrid</span></span>
```
Update-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -EventHubResourceId <String> -Kind <Kind>
 -Location <String> -StorageAccountResourceId <String> [-SubscriptionId <String>]
 [-BlobStorageEventType <BlobStorageEventType>] [-DataFormat <EventGridDataFormat>] [-IgnoreFirstRecord]
 [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5d607-107">UpdateExpandedIotHub</span><span class="sxs-lookup"><span data-stu-id="5d607-107">UpdateExpandedIotHub</span></span>
```
Update-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -IotHubResourceId <String> -Kind <Kind>
 -Location <String> -SharedAccessPolicyName <String> [-SubscriptionId <String>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="5d607-108">UpdateViaIdentityExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="5d607-108">UpdateViaIdentityExpandedEventGrid</span></span>
```
Update-AzKustoDataConnection -InputObject <IKustoIdentity> -ConsumerGroup <String>
 -EventHubResourceId <String> -Kind <Kind> -Location <String> -StorageAccountResourceId <String>
 [-BlobStorageEventType <BlobStorageEventType>] [-DataFormat <EventGridDataFormat>] [-IgnoreFirstRecord]
 [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5d607-109">UpdateViaIdentityExpandedEventHub</span><span class="sxs-lookup"><span data-stu-id="5d607-109">UpdateViaIdentityExpandedEventHub</span></span>
```
Update-AzKustoDataConnection -InputObject <IKustoIdentity> -ConsumerGroup <String>
 -EventHubResourceId <String> -Kind <Kind> -Location <String> [-Compression <Compression>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="5d607-110">UpdateViaIdentityExpandedIotHub</span><span class="sxs-lookup"><span data-stu-id="5d607-110">UpdateViaIdentityExpandedIotHub</span></span>
```
Update-AzKustoDataConnection -InputObject <IKustoIdentity> -ConsumerGroup <String> -IotHubResourceId <String>
 -Kind <Kind> -Location <String> -SharedAccessPolicyName <String> [-DataFormat <EventGridDataFormat>]
 [-EventSystemProperty <String[]>] [-MappingRuleName <String>] [-TableName <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5d607-111">설명은</span><span class="sxs-lookup"><span data-stu-id="5d607-111">DESCRIPTION</span></span>
<span data-ttu-id="5d607-112">데이터 연결을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d607-112">Updates a data connection.</span></span>

## <span data-ttu-id="5d607-113">예제의</span><span class="sxs-lookup"><span data-stu-id="5d607-113">EXAMPLES</span></span>

### <span data-ttu-id="5d607-114">예제 1: 기존 EventHub 데이터 연결 업데이트</span><span class="sxs-lookup"><span data-stu-id="5d607-114">Example 1: Update an existing EventHub data connection</span></span>
```powershell
PS C:\> Update-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventhubdc" -Location="East US" -Kind "EventHub" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -DataFormat "JSON" -ConsumerGroup '$Default' -Compression "None" -TableName "Events" -MappingRuleName "NewEventsMapping"

Kind     Location Name                                             Type
----     -------- ----                                             ----
EventHub East US  testnewkustocluster/mykustodatabase/myeventhubdc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="5d607-115">위의 명령은 "testnewkustocluster" 클러스터의 "mykustodatabase" 데이터베이스에 대해 "myeventhubdc" 이라는 기존 EventHub 데이터 연결을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d607-115">The above command updates the existing EventHub data connection named "myeventhubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="5d607-116">예제 2: 기존 EventGrid 데이터 연결 업데이트</span><span class="sxs-lookup"><span data-stu-id="5d607-116">Example 2: Update an existing EventGrid data connection</span></span>
```powershell
PS C:\> Update-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventgriddc" -Location="East US" -Kind "EventGrid" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -StorageAccountResourceId $storageAccountResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Storage/storageAccounts/mystorage" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

Kind      Location Name                                              Type
----      -------- ----                                              ----
EventGrid East US  testnewkustocluster/mykustodatabase/myeventgriddc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="5d607-117">위의 명령은 "testnewkustocluster" 클러스터의 "mykustodatabase" 데이터베이스에 대 한 "myeventgriddc" 이라는 기존 EventGrid 데이터 연결을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d607-117">The above command updates the existing EventGrid data connection named "myeventgriddc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="5d607-118">예제 3: 기존 IotHub 데이터 연결 업데이트</span><span class="sxs-lookup"><span data-stu-id="5d607-118">Example 3: Update an existing IotHub data connection</span></span>
```powershell
PS C:\> Update-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myiothubdc" -Location="East US" -Kind "IotHub" -IotHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Devices/IotHubs/myiothub" -SharedAccessPolicyName "myiothubpolicy" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

Kind      Location Name                                        Type
----      -------- ----                                        ----
IotHub East US  testnewkustocluster/mykustodatabase/myiothubdc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="5d607-119">위 명령은 "mykustodatabase" 데이터베이스의 "myiothubdc" ("IotHub")를 "testnewkustocluster" 클러스터에 있는 "\*" (으)로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d607-119">The above command updates the existing IotHub data connection named "myiothubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="5d607-120">예제 4: id를 통해 기존 EventHub 데이터 연결 업데이트</span><span class="sxs-lookup"><span data-stu-id="5d607-120">Example 4: Update an existing EventHub data connection via identity</span></span>
```powershell
PS C:\> $dataConnection = Get-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventhubdc" 
PS C:\> Update-AzKustoDataConnection -InputObject $dataConnection -Location="East US" -Kind "EventHub" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -DataFormat "JSON" -ConsumerGroup '$Default' -Compression "None" -TableName "Events" -MappingRuleName "NewEventsMapping"

Kind     Location Name                                             Type
----     -------- ----                                             ----
EventHub East US  testnewkustocluster/mykustodatabase/myeventhubdc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="5d607-121">위의 명령은 "testnewkustocluster" 클러스터의 "mykustodatabase" 데이터베이스에 대해 "myeventhubdc" 이라는 기존 EventHub 데이터 연결을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d607-121">The above command updates the existing EventHub data connection named "myeventhubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="5d607-122">예제 5: id를 통해 기존 EventGrid 데이터 연결 업데이트</span><span class="sxs-lookup"><span data-stu-id="5d607-122">Example 5: Update an existing EventGrid data connection via identity</span></span>
```powershell
PS C:\> $dataConnection = Get-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventgriddc" 
PS C:\> Update-AzKustoDataConnection -InputObject $dataConnection -Location="East US" -Kind "EventGrid" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -StorageAccountResourceId $storageAccountResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Storage/storageAccounts/mystorage" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

Kind      Location Name                                              Type
----      -------- ----                                              ----
EventGrid East US  testnewkustocluster/mykustodatabase/myeventgriddc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="5d607-123">위의 명령은 "testnewkustocluster" 클러스터의 "mykustodatabase" 데이터베이스에 대 한 "myeventgriddc" 이라는 기존 EventGrid 데이터 연결을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d607-123">The above command updates the existing EventGrid data connection named "myeventgriddc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="5d607-124">예제 6: id를 통해 기존 IotHub 데이터 연결 업데이트</span><span class="sxs-lookup"><span data-stu-id="5d607-124">Example 6: Update an existing IotHub data connection via identity</span></span>
```powershell
PS C:\> $dataConnection = Get-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myiothubdc" 
PS C:\> Update-AzKustoDataConnection -InputObject $dataConnection -Location="East US" -Kind "IotHub" -IotHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Devices/IotHubs/myiothub" -SharedAccessPolicyName "myiothubpolicy" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

Kind      Location Name                                        Type
----      -------- ----                                        ----
IotHub East US  testnewkustocluster/mykustodatabase/myiothubdc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="5d607-125">위 명령은 "mykustodatabase" 데이터베이스의 "myiothubdc" ("IotHub")를 "testnewkustocluster" 클러스터에 있는 "\*" (으)로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d607-125">The above command updates the existing IotHub data connection named "myiothubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="5d607-126">변수</span><span class="sxs-lookup"><span data-stu-id="5d607-126">PARAMETERS</span></span>

### <span data-ttu-id="5d607-127">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5d607-127">-AsJob</span></span>
<span data-ttu-id="5d607-128">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="5d607-128">Run the command as a job</span></span>

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

### <span data-ttu-id="5d607-129">-BlobStorageEventType</span><span class="sxs-lookup"><span data-stu-id="5d607-129">-BlobStorageEventType</span></span>
<span data-ttu-id="5d607-130">처리할 blob 저장소 이벤트 유형의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5d607-130">The name of blob storage event type to process.</span></span>

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

### <span data-ttu-id="5d607-131">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="5d607-131">-ClusterName</span></span>
<span data-ttu-id="5d607-132">Kusto의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5d607-132">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="5d607-133">-압축</span><span class="sxs-lookup"><span data-stu-id="5d607-133">-Compression</span></span>
<span data-ttu-id="5d607-134">이벤트 허브 메시지 압축 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="5d607-134">The event hub messages compression type.</span></span>

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

### <span data-ttu-id="5d607-135">-ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="5d607-135">-ConsumerGroup</span></span>
<span data-ttu-id="5d607-136">이벤트/iot hub 소비자 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="5d607-136">The event/iot hub consumer group.</span></span>

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

### <span data-ttu-id="5d607-137">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5d607-137">-DatabaseName</span></span>
<span data-ttu-id="5d607-138">Kusto cluster의 데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5d607-138">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="5d607-139">-DataFormat</span><span class="sxs-lookup"><span data-stu-id="5d607-139">-DataFormat</span></span>
<span data-ttu-id="5d607-140">메시지의 데이터 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="5d607-140">The data format of the message.</span></span>
<span data-ttu-id="5d607-141">필요에 따라 각 메시지에 데이터 형식을 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5d607-141">Optionally the data format can be added to each message.</span></span>

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

### <span data-ttu-id="5d607-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d607-142">-DefaultProfile</span></span>
<span data-ttu-id="5d607-143">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5d607-143">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d607-144">-EventHubResourceId</span><span class="sxs-lookup"><span data-stu-id="5d607-144">-EventHubResourceId</span></span>
<span data-ttu-id="5d607-145">데이터 연결/이벤트 그리드를 만드는 데 사용할 이벤트 허브의 리소스 ID가 이벤트를 보내도록 구성 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5d607-145">The resource ID of the event hub to be used to create a data connection / event grid is configured to send events.</span></span>

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

### <span data-ttu-id="5d607-146">-EventSystemProperty</span><span class="sxs-lookup"><span data-stu-id="5d607-146">-EventSystemProperty</span></span>
<span data-ttu-id="5d607-147">이벤트/iot hub의 시스템 속성</span><span class="sxs-lookup"><span data-stu-id="5d607-147">System properties of the event/iot hub.</span></span>

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

### <span data-ttu-id="5d607-148">-IgnoreFirstRecord</span><span class="sxs-lookup"><span data-stu-id="5d607-148">-IgnoreFirstRecord</span></span>
<span data-ttu-id="5d607-149">True로 설정 되 면 수집에서 모든 파일의 첫 번째 레코드를 무시 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="5d607-149">If set to true, indicates that ingestion should ignore the first record of every file.</span></span>

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

### <span data-ttu-id="5d607-150">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5d607-150">-InputObject</span></span>
<span data-ttu-id="5d607-151">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5d607-151">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="5d607-152">-IotHubResourceId</span><span class="sxs-lookup"><span data-stu-id="5d607-152">-IotHubResourceId</span></span>
<span data-ttu-id="5d607-153">데이터 연결을 만드는 데 사용 되는 Iot hub의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="5d607-153">The resource ID of the Iot hub to be used to create a data connection.</span></span>

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

### <span data-ttu-id="5d607-154">-종류</span><span class="sxs-lookup"><span data-stu-id="5d607-154">-Kind</span></span>
<span data-ttu-id="5d607-155">데이터 연결을 위한 끝점의 종류</span><span class="sxs-lookup"><span data-stu-id="5d607-155">Kind of the endpoint for the data connection</span></span>

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

### <span data-ttu-id="5d607-156">-위치</span><span class="sxs-lookup"><span data-stu-id="5d607-156">-Location</span></span>
<span data-ttu-id="5d607-157">리소스 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="5d607-157">Resource location.</span></span>

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

### <span data-ttu-id="5d607-158">-MappingRuleName</span><span class="sxs-lookup"><span data-stu-id="5d607-158">-MappingRuleName</span></span>
<span data-ttu-id="5d607-159">데이터를 수집 하는 데 사용 되는 매핑 규칙입니다.</span><span class="sxs-lookup"><span data-stu-id="5d607-159">The mapping rule to be used to ingest the data.</span></span>
<span data-ttu-id="5d607-160">필요에 따라 각 메시지에 매핑 정보를 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5d607-160">Optionally the mapping information can be added to each message.</span></span>

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

### <span data-ttu-id="5d607-161">-이름</span><span class="sxs-lookup"><span data-stu-id="5d607-161">-Name</span></span>
<span data-ttu-id="5d607-162">데이터 연결의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5d607-162">The name of the data connection.</span></span>

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

### <span data-ttu-id="5d607-163">-NoWait</span><span class="sxs-lookup"><span data-stu-id="5d607-163">-NoWait</span></span>
<span data-ttu-id="5d607-164">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="5d607-164">Run the command asynchronously</span></span>

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

### <span data-ttu-id="5d607-165">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d607-165">-ResourceGroupName</span></span>
<span data-ttu-id="5d607-166">Kusto cluster를 포함 하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5d607-166">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="5d607-167">-SharedAccessPolicyName</span><span class="sxs-lookup"><span data-stu-id="5d607-167">-SharedAccessPolicyName</span></span>
<span data-ttu-id="5d607-168">공유 액세스 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5d607-168">The name of the share access policy.</span></span>

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

### <span data-ttu-id="5d607-169">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="5d607-169">-StorageAccountResourceId</span></span>
<span data-ttu-id="5d607-170">데이터가 있는 저장소 계정의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="5d607-170">The resource ID of the storage account where the data resides.</span></span>

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

### <span data-ttu-id="5d607-171">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5d607-171">-SubscriptionId</span></span>
<span data-ttu-id="5d607-172">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5d607-172">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="5d607-173">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d607-173">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="5d607-174">-TableName</span><span class="sxs-lookup"><span data-stu-id="5d607-174">-TableName</span></span>
<span data-ttu-id="5d607-175">데이터를 ingested 하는 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="5d607-175">The table where the data should be ingested.</span></span>
<span data-ttu-id="5d607-176">필요에 따라 각 메시지에 테이블 정보를 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5d607-176">Optionally the table information can be added to each message.</span></span>

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

### <span data-ttu-id="5d607-177">-확인</span><span class="sxs-lookup"><span data-stu-id="5d607-177">-Confirm</span></span>
<span data-ttu-id="5d607-178">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d607-178">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d607-179">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d607-179">-WhatIf</span></span>
<span data-ttu-id="5d607-180">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="5d607-180">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d607-181">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5d607-181">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d607-182">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d607-182">CommonParameters</span></span>
<span data-ttu-id="5d607-183">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d607-183">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d607-184">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="5d607-184">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d607-185">입력</span><span class="sxs-lookup"><span data-stu-id="5d607-185">INPUTS</span></span>

### <span data-ttu-id="5d607-186">IKustoIdentity (Microsoft. PowerShell. m a us</span><span class="sxs-lookup"><span data-stu-id="5d607-186">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="5d607-187">출력</span><span class="sxs-lookup"><span data-stu-id="5d607-187">OUTPUTS</span></span>

### <span data-ttu-id="5d607-188">Microsoft. Api20200614. IDataConnection에 대 한.</span><span class="sxs-lookup"><span data-stu-id="5d607-188">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDataConnection</span></span>

## <span data-ttu-id="5d607-189">상속자</span><span class="sxs-lookup"><span data-stu-id="5d607-189">NOTES</span></span>

<span data-ttu-id="5d607-190">별칭과</span><span class="sxs-lookup"><span data-stu-id="5d607-190">ALIASES</span></span>

<span data-ttu-id="5d607-191">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="5d607-191">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5d607-192">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d607-192">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5d607-193">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="5d607-193">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5d607-194">INPUTOBJECT <IKustoIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="5d607-194">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5d607-195">`[AttachedDatabaseConfigurationName <String>]`: 연결 된 데이터베이스 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5d607-195">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="5d607-196">`[ClusterName <String>]`: Kusto의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5d607-196">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="5d607-197">`[DataConnectionName <String>]`: 데이터 연결의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5d607-197">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="5d607-198">`[DatabaseName <String>]`: Kusto cluster의 데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5d607-198">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="5d607-199">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="5d607-199">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5d607-200">`[Location <String>]`: Azure 위치.</span><span class="sxs-lookup"><span data-stu-id="5d607-200">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="5d607-201">`[PrincipalAssignmentName <String>]`:%에 대 한 Kusto principalAssignment의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5d607-201">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="5d607-202">`[ResourceGroupName <String>]`: Kusto cluster를 포함 하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5d607-202">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="5d607-203">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5d607-203">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="5d607-204">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d607-204">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="5d607-205">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5d607-205">RELATED LINKS</span></span>

