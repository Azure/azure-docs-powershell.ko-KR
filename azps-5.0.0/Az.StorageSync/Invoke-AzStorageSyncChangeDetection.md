---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/az.storagesync/invoke-azstoragesyncchangedetection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncChangeDetection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncChangeDetection.md
ms.openlocfilehash: f76a399d9d2e592bbea10a9e304d8f6875eea227
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94310502"
---
# <span data-ttu-id="1f378-101">Invoke-AzStorageSyncChangeDetection</span><span class="sxs-lookup"><span data-stu-id="1f378-101">Invoke-AzStorageSyncChangeDetection</span></span>

## <span data-ttu-id="1f378-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f378-102">SYNOPSIS</span></span>
<span data-ttu-id="1f378-103">이 명령을 사용 하 여 네임 스페이스 변경 감지를 수동으로 시작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1f378-103">This command can be used to manually initiate the detection of namespaces changes.</span></span> <span data-ttu-id="1f378-104">전체 공유, 하위 폴더 또는 파일 집합을 대상으로 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1f378-104">It can be targeted to the entire share, subfolder or set of files.</span></span> <span data-ttu-id="1f378-105">최대 1만 개의 항목을 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1f378-105">A maximum of 10,000 items can be detected.</span></span> <span data-ttu-id="1f378-106">변경의 범위가 사용자에 게 알려진 경우이 명령의 실행을 네임 스페이스의 부분으로 제한 하 여 변경 내용이 1만 항목 제한 내에서 빠르게 완료 될 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f378-106">If the scope of changes is known to you, limit the execution of this command to parts of the namespace, so change detection can finish quickly and within the 10,000 item limit.</span></span>

> [!Note]  
> <span data-ttu-id="1f378-107">Invoke-AzStorageSyncChangeDetection cmdlet은 Azure 파일 공유에서 다음과 같은 변경 내용을 검색 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1f378-107">The Invoke-AzStorageSyncChangeDetection cmdlet will not detect the following changes in the Azure file share:</span></span>
> - <span data-ttu-id="1f378-108">삭제 되는 파일</span><span class="sxs-lookup"><span data-stu-id="1f378-108">Files that are deleted.</span></span> 
> - <span data-ttu-id="1f378-109">공유에서 옮겨진 파일</span><span class="sxs-lookup"><span data-stu-id="1f378-109">Files that are moved out of the share.</span></span>
> - <span data-ttu-id="1f378-110">같은 이름으로 삭제 하 고 만든 파일</span><span class="sxs-lookup"><span data-stu-id="1f378-110">Files that are deleted and created with the same name.</span></span>  
> 
>  <span data-ttu-id="1f378-111">이러한 변경 내용은 [변경 내용 검색 작업이](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#afs->change-detection) 실행 될 때 검색 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1f378-111">These changes will be detected when the [change detection job](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#afs->change-detection) runs.</span></span>

## <span data-ttu-id="1f378-112">구문과</span><span class="sxs-lookup"><span data-stu-id="1f378-112">SYNTAX</span></span>

### <span data-ttu-id="1f378-113">StringAndDirectoryParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="1f378-113">StringAndDirectoryParameterSet (Default)</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -DirectoryPath <String> [-Recursive] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f378-114">StringAndPathParameterSet</span><span class="sxs-lookup"><span data-stu-id="1f378-114">StringAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f378-115">ResourceIdAndDirectoryParameterSet</span><span class="sxs-lookup"><span data-stu-id="1f378-115">ResourceIdAndDirectoryParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceId] <String> -DirectoryPath <String> [-Recursive] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f378-116">ResourceIdAndPathParameterSet</span><span class="sxs-lookup"><span data-stu-id="1f378-116">ResourceIdAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceId] <String> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f378-117">ObjectAndDirectoryParameterSet</span><span class="sxs-lookup"><span data-stu-id="1f378-117">ObjectAndDirectoryParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-InputObject] <PSCloudEndpoint> -DirectoryPath <String> [-Recursive]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f378-118">ObjectAndPathParameterSet</span><span class="sxs-lookup"><span data-stu-id="1f378-118">ObjectAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-InputObject] <PSCloudEndpoint> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f378-119">설명은</span><span class="sxs-lookup"><span data-stu-id="1f378-119">DESCRIPTION</span></span>
<span data-ttu-id="1f378-120">정기적으로 Azure 파일 동기화는 동기화 하는 것 보다 다른 수단으로 파일 공유에 제공 된 변경 내용에 대 한 Azure 파일 공유 내의 네임 스페이스를 검사 합니다. 목표는 이러한 변경을 식별 하 고 궁극적으로 연결 된 서버와 동기화 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="1f378-120">Periodically, Azure File Sync checks the namespace inside a syncing Azure file share for changes that came into the file share by other means than sync. The goal is to identify these changes and ultimately sync them to connected servers.</span></span> <span data-ttu-id="1f378-121">이 명령을 사용 하 여 네임 스페이스 변경 감지를 수동으로 시작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1f378-121">This command can be used to manually initiate the detection of namespaces changes.</span></span> <span data-ttu-id="1f378-122">전체 공유, 하위 폴더 또는 파일 집합을 대상으로 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1f378-122">It can be targeted to the entire share, subfolder or set of files.</span></span> <span data-ttu-id="1f378-123">변경의 범위가 사용자에 게 알려진 경우,이 명령의 실행을 네임 스페이스의 부분으로 제한 하 여 1만 항목 제한 내에서 변경 내용을 빠르게 완료할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1f378-123">If the scope of changes is known to you, limit the execution of this command to parts of the namespace, so change detection can finish quickly and within the 10,000 items limit.</span></span>

## <span data-ttu-id="1f378-124">예제의</span><span class="sxs-lookup"><span data-stu-id="1f378-124">EXAMPLES</span></span>

### <span data-ttu-id="1f378-125">예제 1</span><span class="sxs-lookup"><span data-stu-id="1f378-125">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "b38fc242-8100-4807-89d0-399cef5863bf" -Path "Data","Reporting\Templates"
```

<span data-ttu-id="1f378-126">이 예제에서는 동기화 Azure 파일 공유의 "Data" 및 "Reporting\Templates" 디렉터리에서 변경 감지를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f378-126">In this example, change detection is run in the "Data" and "Reporting\Templates" directories of a syncing Azure file share.</span></span> <span data-ttu-id="1f378-127">모든 경로는 Azure 파일 공유 네임 스페이스의 루트를 기준으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f378-127">All paths are relative to the root of the Azure file share namespace.</span></span>

### <span data-ttu-id="1f378-128">예제 2</span><span class="sxs-lookup"><span data-stu-id="1f378-128">Example 2</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "b38fc242-8100-4807-89d0-399cef5863bf" -Path "Data\results.xslx","Reporting\Templates\generated.pptx"
```

<span data-ttu-id="1f378-129">이 예제에서는 변경 내용 검색이 명령 호출자가 변경 하는 것으로 알려진 파일 집합에 대해 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1f378-129">In this example, change detection is run for a set of files that are known to the command caller to have changed.</span></span> <span data-ttu-id="1f378-130">목표는 Azure 파일 동기화를 통해 이러한 변경 내용을 검색 하 고 동기화 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="1f378-130">The goal is to have Azure file sync detect and sync these changes as well.</span></span>

### <span data-ttu-id="1f378-131">예제 3</span><span class="sxs-lookup"><span data-stu-id="1f378-131">Example 3</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "b38fc242-8100-4807-89d0-399cef5863bf" -DirectoryPath "Examples" -Recursive
```

<span data-ttu-id="1f378-132">이 예제에서는 "예제" 디렉터리에 대 한 변경 감지를 실행 하 고 하위 디렉터리의 변경 내용을 재귀적으로 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f378-132">In this example, change detection is run for the "Examples" directory and will recursively detect changes in subdirectories.</span></span> <span data-ttu-id="1f378-133">경로에 1만 항목이 여러 개 포함 되어 있으면 cmdlet이 실패 하는 것에 유의 하세요.</span><span class="sxs-lookup"><span data-stu-id="1f378-133">Keep in mind the cmdlet will fail if the path contains more than 10,000 items.</span></span> <span data-ttu-id="1f378-134">경로에 1만 개 이상의 항목이 포함 된 경우 네임 스페이스의 하위 부분에 대 한 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f378-134">If the path contains more than 10,000 items, run the command on sub-parts of the namespace.</span></span>

## <span data-ttu-id="1f378-135">변수</span><span class="sxs-lookup"><span data-stu-id="1f378-135">PARAMETERS</span></span>

### <span data-ttu-id="1f378-136">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1f378-136">-AsJob</span></span>
<span data-ttu-id="1f378-137">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="1f378-137">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1f378-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f378-138">-DefaultProfile</span></span>
<span data-ttu-id="1f378-139">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1f378-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f378-140">-DirectoryPath</span><span class="sxs-lookup"><span data-stu-id="1f378-140">-DirectoryPath</span></span>
<span data-ttu-id="1f378-141">변경 내용 검색이 수행 되는 디렉터리입니다.</span><span class="sxs-lookup"><span data-stu-id="1f378-141">Directory where change detection will be performed.</span></span>

```yaml
Type: System.String
Parameter Sets: StringAndDirectoryParameterSet, ResourceIdAndDirectoryParameterSet, ObjectAndDirectoryParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f378-142">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1f378-142">-InputObject</span></span>
<span data-ttu-id="1f378-143">일반적으로 매개 변수를 통해 전달 되는 CloudEndpoint 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="1f378-143">CloudEndpoint Object, normally passed through the parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint
Parameter Sets: ObjectAndDirectoryParameterSet, ObjectAndPathParameterSet
Aliases: CloudEndpoint

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1f378-144">-이름</span><span class="sxs-lookup"><span data-stu-id="1f378-144">-Name</span></span>
<span data-ttu-id="1f378-145">CloudEndpoint의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1f378-145">Name of the CloudEndpoint.</span></span> <span data-ttu-id="1f378-146">이름은 포털에 표시 되는 친근 한 이름이 아니라 GUID입니다.</span><span class="sxs-lookup"><span data-stu-id="1f378-146">The name is a GUID, not the friendly name that's displayed in the portal.</span></span> <span data-ttu-id="1f378-147">CloudEndpointName를 가져오려면 Get-AzStorageSyncCloudEndpoint cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f378-147">To get the CloudEndpointName, use the Get-AzStorageSyncCloudEndpoint cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: StringAndDirectoryParameterSet, StringAndPathParameterSet
Aliases: CloudEndpointName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f378-148">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1f378-148">-PassThru</span></span>
<span data-ttu-id="1f378-149">일반 실행에서이 cmdlet은 성공에 대 한 값을 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1f378-149">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="1f378-150">PassThru 매개 변수를 제공 하는 경우 cmdlet은 성공적으로 실행 된 후 파이프라인에 값을 기록 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f378-150">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="1f378-151">-Path</span><span class="sxs-lookup"><span data-stu-id="1f378-151">-Path</span></span>
<span data-ttu-id="1f378-152">변경 내용 검색이 수행 되는 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="1f378-152">Path where change detection will be performed.</span></span>

```yaml
Type: System.String[]
Parameter Sets: StringAndPathParameterSet, ResourceIdAndPathParameterSet, ObjectAndPathParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f378-153">-Recursive</span><span class="sxs-lookup"><span data-stu-id="1f378-153">-Recursive</span></span>
<span data-ttu-id="1f378-154">디렉터리 변경 내용 검색이 재귀적 인지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="1f378-154">Indication whether directory change detection is recursive.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: StringAndDirectoryParameterSet, ResourceIdAndDirectoryParameterSet, ObjectAndDirectoryParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f378-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f378-155">-ResourceGroupName</span></span>
<span data-ttu-id="1f378-156">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1f378-156">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: StringAndDirectoryParameterSet, StringAndPathParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f378-157">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1f378-157">-ResourceId</span></span>
<span data-ttu-id="1f378-158">CloudEndpoint 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="1f378-158">CloudEndpoint Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdAndDirectoryParameterSet, ResourceIdAndPathParameterSet
Aliases: CloudEndpointId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f378-159">-Storages Cservicename</span><span class="sxs-lookup"><span data-stu-id="1f378-159">-StorageSyncServiceName</span></span>
<span data-ttu-id="1f378-160">Storages<c13> Cservice의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1f378-160">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringAndDirectoryParameterSet, StringAndPathParameterSet
Aliases: ParentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f378-161">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="1f378-161">-SyncGroupName</span></span>
<span data-ttu-id="1f378-162">SyncGroup의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1f378-162">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: StringAndDirectoryParameterSet, StringAndPathParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f378-163">-확인</span><span class="sxs-lookup"><span data-stu-id="1f378-163">-Confirm</span></span>
<span data-ttu-id="1f378-164">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f378-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f378-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f378-165">-WhatIf</span></span>
<span data-ttu-id="1f378-166">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1f378-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f378-167">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1f378-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f378-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f378-168">CommonParameters</span></span>
<span data-ttu-id="1f378-169">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f378-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f378-170">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f378-170">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f378-171">입력</span><span class="sxs-lookup"><span data-stu-id="1f378-171">INPUTS</span></span>

### <span data-ttu-id="1f378-172">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="1f378-172">System.String</span></span>

### <span data-ttu-id="1f378-173">StorageSync. a m a. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="1f378-173">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="1f378-174">출력</span><span class="sxs-lookup"><span data-stu-id="1f378-174">OUTPUTS</span></span>

### <span data-ttu-id="1f378-175">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="1f378-175">System.Void</span></span>

## <span data-ttu-id="1f378-176">상속자</span><span class="sxs-lookup"><span data-stu-id="1f378-176">NOTES</span></span>

## <span data-ttu-id="1f378-177">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1f378-177">RELATED LINKS</span></span>
