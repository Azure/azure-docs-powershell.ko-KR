---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/az.storagesync/invoke-azstoragesyncchangedetection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncChangeDetection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncChangeDetection.md
ms.openlocfilehash: 41710c328787f542188c828975402696c36f0854
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212041"
---
# <span data-ttu-id="01fc2-101">Invoke-AzStorageSyncChangeDetection</span><span class="sxs-lookup"><span data-stu-id="01fc2-101">Invoke-AzStorageSyncChangeDetection</span></span>

## <span data-ttu-id="01fc2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01fc2-102">SYNOPSIS</span></span>
<span data-ttu-id="01fc2-103">이 명령을 사용 하 여 네임 스페이스 변경 감지를 수동으로 시작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="01fc2-103">This command can be used to manually initiate the detection of namespaces changes.</span></span> <span data-ttu-id="01fc2-104">전체 공유, 하위 폴더 또는 파일 집합을 대상으로 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="01fc2-104">It can be targeted to the entire share, subfolder or set of files.</span></span> <span data-ttu-id="01fc2-105">최대 1만 개의 항목을 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="01fc2-105">A maximum of 10,000 items can be detected.</span></span> <span data-ttu-id="01fc2-106">변경의 범위가 사용자에 게 알려진 경우이 명령의 실행을 네임 스페이스의 부분으로 제한 하 여 변경 내용이 1만 항목 제한 내에서 빠르게 완료 될 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="01fc2-106">If the scope of changes is known to you, limit the execution of this command to parts of the namespace, so change detection can finish quickly and within the 10,000 item limit.</span></span>

> [!Note]  
> <span data-ttu-id="01fc2-107">Invoke-AzStorageSyncChangeDetection cmdlet은 Azure 파일 공유에서 삭제 된 파일을 검색 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="01fc2-107">The Invoke-AzStorageSyncChangeDetection cmdlet will not detect files that are deleted in the Azure file share.</span></span> <span data-ttu-id="01fc2-108">Azure 파일 공유에서 파일을 삭제 하면 [변경 내용 검색 작업이](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#afs-change-detection) 실행 될 때 검색 됩니다.</span><span class="sxs-lookup"><span data-stu-id="01fc2-108">If files are deleted in the Azure file share, they will be detected when the [change detection job](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#afs-change-detection) runs.</span></span>

## <span data-ttu-id="01fc2-109">구문과</span><span class="sxs-lookup"><span data-stu-id="01fc2-109">SYNTAX</span></span>

### <span data-ttu-id="01fc2-110">StringAndDirectoryParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="01fc2-110">StringAndDirectoryParameterSet (Default)</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -DirectoryPath <String> [-Recursive] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01fc2-111">StringAndPathParameterSet</span><span class="sxs-lookup"><span data-stu-id="01fc2-111">StringAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01fc2-112">ResourceIdAndDirectoryParameterSet</span><span class="sxs-lookup"><span data-stu-id="01fc2-112">ResourceIdAndDirectoryParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceId] <String> -DirectoryPath <String> [-Recursive] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01fc2-113">ResourceIdAndPathParameterSet</span><span class="sxs-lookup"><span data-stu-id="01fc2-113">ResourceIdAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceId] <String> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01fc2-114">ObjectAndDirectoryParameterSet</span><span class="sxs-lookup"><span data-stu-id="01fc2-114">ObjectAndDirectoryParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-InputObject] <PSCloudEndpoint> -DirectoryPath <String> [-Recursive]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01fc2-115">ObjectAndPathParameterSet</span><span class="sxs-lookup"><span data-stu-id="01fc2-115">ObjectAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-InputObject] <PSCloudEndpoint> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01fc2-116">설명은</span><span class="sxs-lookup"><span data-stu-id="01fc2-116">DESCRIPTION</span></span>
<span data-ttu-id="01fc2-117">정기적으로 Azure 파일 동기화는 동기화 하는 것 보다 다른 수단으로 파일 공유에 제공 된 변경 내용에 대 한 Azure 파일 공유 내의 네임 스페이스를 검사 합니다. 목표는 이러한 변경을 식별 하 고 궁극적으로 연결 된 서버와 동기화 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="01fc2-117">Periodically, Azure File Sync checks the namespace inside a syncing Azure file share for changes that came into the file share by other means than sync. The goal is to identify these changes and ultimately sync them to connected servers.</span></span> <span data-ttu-id="01fc2-118">이 명령을 사용 하 여 네임 스페이스 변경 감지를 수동으로 시작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="01fc2-118">This command can be used to manually initiate the detection of namespaces changes.</span></span> <span data-ttu-id="01fc2-119">전체 공유, 하위 폴더 또는 파일 집합을 대상으로 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="01fc2-119">It can be targeted to the entire share, subfolder or set of files.</span></span> <span data-ttu-id="01fc2-120">변경의 범위가 사용자에 게 알려진 경우이 명령의 실행을 네임 스페이스의 부분으로 제한 하 여 변경 내용이 1만 변경 제한 내에서 신속 하 게 완료 될 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="01fc2-120">If the scope of changes is known to you, limit the execution of this command to parts of the namespace, so change detection can finish quickly and within a 10,000 changes limit.</span></span>

## <span data-ttu-id="01fc2-121">예제의</span><span class="sxs-lookup"><span data-stu-id="01fc2-121">EXAMPLES</span></span>

### <span data-ttu-id="01fc2-122">예제 1</span><span class="sxs-lookup"><span data-stu-id="01fc2-122">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "myCloudEndpointName" -Path "Data","Reporting\Templates"
```

<span data-ttu-id="01fc2-123">이 예제에서는 동기화 Azure 파일 공유의 "Data" 및 "Reporting\Templates" 디렉터리에서 변경 감지를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="01fc2-123">In this example, change detection is run in the "Data" and "Reporting\Templates" directories of a syncing Azure file share.</span></span> <span data-ttu-id="01fc2-124">모든 경로는 Azure 파일 공유 네임 스페이스의 루트를 기준으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="01fc2-124">All paths are relative to the root of the Azure file share namespace.</span></span>

### <span data-ttu-id="01fc2-125">예제 2</span><span class="sxs-lookup"><span data-stu-id="01fc2-125">Example 2</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "myCloudEndpointName" -Path "Data\results.xslx","Reporting\Templates\generated.pptx"
```

<span data-ttu-id="01fc2-126">이 예제에서는 변경 내용 검색이 명령 호출자가 변경 하는 것으로 알려진 파일 집합에 대해 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="01fc2-126">In this example, change detection is run for a set of files that are known to the command caller to have changed.</span></span> <span data-ttu-id="01fc2-127">목표는 Azure 파일 동기화를 통해 이러한 변경 내용을 검색 하 고 동기화 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="01fc2-127">The goal is to have Azure file sync detect and sync these changes as well.</span></span>

### <span data-ttu-id="01fc2-128">예제 3</span><span class="sxs-lookup"><span data-stu-id="01fc2-128">Example 3</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "myCloudEndpointName" -DirectoryPath "Examples" -Recursive
```

<span data-ttu-id="01fc2-129">이 예제에서는 "예제" 디렉터리에 대 한 변경 감지를 실행 하 고 하위 디렉터리의 변경 내용을 재귀적으로 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="01fc2-129">In this example, change detection is run for the "Examples" directory and will recursively detect changes in subdirectories.</span></span> <span data-ttu-id="01fc2-130">이 명령은 자동으로 중단 되기 전에 1만 변경 내용을 검색할 수 있다는 점에 유의 하세요.</span><span class="sxs-lookup"><span data-stu-id="01fc2-130">Keep in mind that this command can detect up to 10,000 changes before it is automatically aborted.</span></span> <span data-ttu-id="01fc2-131">1만 변경 내용이 발생 한 것으로 의심 되는 경우 네임 스페이스의 하위 부분에 대 한 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="01fc2-131">If you suspect more than 10,000 changes to have occurred, run the command on sub-parts of the namespace.</span></span>

## <span data-ttu-id="01fc2-132">변수</span><span class="sxs-lookup"><span data-stu-id="01fc2-132">PARAMETERS</span></span>

### <span data-ttu-id="01fc2-133">-AsJob</span><span class="sxs-lookup"><span data-stu-id="01fc2-133">-AsJob</span></span>
<span data-ttu-id="01fc2-134">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="01fc2-134">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="01fc2-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01fc2-135">-DefaultProfile</span></span>
<span data-ttu-id="01fc2-136">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="01fc2-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01fc2-137">-DirectoryPath</span><span class="sxs-lookup"><span data-stu-id="01fc2-137">-DirectoryPath</span></span>
<span data-ttu-id="01fc2-138">변경 내용 검색이 수행 되는 디렉터리입니다.</span><span class="sxs-lookup"><span data-stu-id="01fc2-138">Directory where change detection will be performed.</span></span>

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

### <span data-ttu-id="01fc2-139">-InputObject</span><span class="sxs-lookup"><span data-stu-id="01fc2-139">-InputObject</span></span>
<span data-ttu-id="01fc2-140">일반적으로 매개 변수를 통해 전달 되는 CloudEndpoint 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="01fc2-140">CloudEndpoint Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="01fc2-141">-이름</span><span class="sxs-lookup"><span data-stu-id="01fc2-141">-Name</span></span>
<span data-ttu-id="01fc2-142">CloudEndpoint의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="01fc2-142">Name of the CloudEndpoint.</span></span>

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

### <span data-ttu-id="01fc2-143">-PassThru</span><span class="sxs-lookup"><span data-stu-id="01fc2-143">-PassThru</span></span>
<span data-ttu-id="01fc2-144">일반 실행에서이 cmdlet은 성공에 대 한 값을 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="01fc2-144">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="01fc2-145">PassThru 매개 변수를 제공 하는 경우 cmdlet은 성공적으로 실행 된 후 파이프라인에 값을 기록 합니다.</span><span class="sxs-lookup"><span data-stu-id="01fc2-145">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="01fc2-146">-Path</span><span class="sxs-lookup"><span data-stu-id="01fc2-146">-Path</span></span>
<span data-ttu-id="01fc2-147">변경 내용 검색이 수행 되는 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="01fc2-147">Path where change detection will be performed.</span></span>

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

### <span data-ttu-id="01fc2-148">-Recursive</span><span class="sxs-lookup"><span data-stu-id="01fc2-148">-Recursive</span></span>
<span data-ttu-id="01fc2-149">디렉터리 변경 내용 검색이 재귀적 인지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="01fc2-149">Indication whether directory change detection is recursive.</span></span>

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

### <span data-ttu-id="01fc2-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01fc2-150">-ResourceGroupName</span></span>
<span data-ttu-id="01fc2-151">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="01fc2-151">Resource Group Name.</span></span>

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

### <span data-ttu-id="01fc2-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="01fc2-152">-ResourceId</span></span>
<span data-ttu-id="01fc2-153">CloudEndpoint 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="01fc2-153">CloudEndpoint Resource Id</span></span>

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

### <span data-ttu-id="01fc2-154">-Storages<c13> Cservicename</span><span class="sxs-lookup"><span data-stu-id="01fc2-154">-StorageSyncServiceName</span></span>
<span data-ttu-id="01fc2-155">Storages Cservice의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="01fc2-155">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="01fc2-156">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="01fc2-156">-SyncGroupName</span></span>
<span data-ttu-id="01fc2-157">SyncGroup의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="01fc2-157">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="01fc2-158">-확인</span><span class="sxs-lookup"><span data-stu-id="01fc2-158">-Confirm</span></span>
<span data-ttu-id="01fc2-159">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="01fc2-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01fc2-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01fc2-160">-WhatIf</span></span>
<span data-ttu-id="01fc2-161">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="01fc2-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01fc2-162">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="01fc2-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01fc2-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01fc2-163">CommonParameters</span></span>
<span data-ttu-id="01fc2-164">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="01fc2-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01fc2-165">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01fc2-165">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01fc2-166">입력</span><span class="sxs-lookup"><span data-stu-id="01fc2-166">INPUTS</span></span>

### <span data-ttu-id="01fc2-167">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="01fc2-167">System.String</span></span>

### <span data-ttu-id="01fc2-168">StorageSync. a m a. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="01fc2-168">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="01fc2-169">출력</span><span class="sxs-lookup"><span data-stu-id="01fc2-169">OUTPUTS</span></span>

### <span data-ttu-id="01fc2-170">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="01fc2-170">System.Void</span></span>

## <span data-ttu-id="01fc2-171">상속자</span><span class="sxs-lookup"><span data-stu-id="01fc2-171">NOTES</span></span>

## <span data-ttu-id="01fc2-172">관련 링크</span><span class="sxs-lookup"><span data-stu-id="01fc2-172">RELATED LINKS</span></span>
