---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/az.storagesync/invoke-azstoragesyncchangedetection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncChangeDetection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncChangeDetection.md
ms.openlocfilehash: 9b7c539074f38b730a8ab5cd767a62fb44216ef6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195684"
---
# <span data-ttu-id="c7486-101">Invoke-AzStorageSyncChangeDetection</span><span class="sxs-lookup"><span data-stu-id="c7486-101">Invoke-AzStorageSyncChangeDetection</span></span>

## <span data-ttu-id="c7486-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7486-102">SYNOPSIS</span></span>
<span data-ttu-id="c7486-103">이 명령을 사용하여 네임스페이스 변경 내용의 검색을 수동으로 시작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c7486-103">This command can be used to manually initiate the detection of namespaces changes.</span></span> <span data-ttu-id="c7486-104">전체 공유, 하위 폴더 또는 파일 집합을 대상으로 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c7486-104">It can be targeted to the entire share, subfolder or set of files.</span></span> <span data-ttu-id="c7486-105">최대 10,000개 항목을 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c7486-105">A maximum of 10,000 items can be detected.</span></span> <span data-ttu-id="c7486-106">변경 범위가 알려진 경우 이 명령의 실행을 네임스페이스의 일부로 제한하면 변경 검색이 10,000개 항목 제한 내에서 빠르게 완료될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c7486-106">If the scope of changes is known to you, limit the execution of this command to parts of the namespace, so change detection can finish quickly and within the 10,000 item limit.</span></span>

> [!Note]  
> <span data-ttu-id="c7486-107">Invoke-AzStorageSyncChangeDetection cmdlet은 Azure 파일 공유에서 다음과 같은 변경 내용을 검색하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c7486-107">The Invoke-AzStorageSyncChangeDetection cmdlet will not detect the following changes in the Azure file share:</span></span>
> - <span data-ttu-id="c7486-108">삭제된 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="c7486-108">Files that are deleted.</span></span> 
> - <span data-ttu-id="c7486-109">공유에서 이동된 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="c7486-109">Files that are moved out of the share.</span></span>
> - <span data-ttu-id="c7486-110">동일한 이름으로 삭제되고 만들어진 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="c7486-110">Files that are deleted and created with the same name.</span></span>  
> 
>  <span data-ttu-id="c7486-111">이러한 변경 내용은 변경 검색 작업이 [실행될 때 검색됩니다.](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#afs-change-detection)</span><span class="sxs-lookup"><span data-stu-id="c7486-111">These changes will be detected when the [change detection job](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#afs-change-detection) runs.</span></span>

## <span data-ttu-id="c7486-112">구문</span><span class="sxs-lookup"><span data-stu-id="c7486-112">SYNTAX</span></span>

### <span data-ttu-id="c7486-113">StringAndDirectoryParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="c7486-113">StringAndDirectoryParameterSet (Default)</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -DirectoryPath <String> [-Recursive] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7486-114">StringAndPathParameterSet</span><span class="sxs-lookup"><span data-stu-id="c7486-114">StringAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7486-115">ResourceIdAndDirectoryParameterSet</span><span class="sxs-lookup"><span data-stu-id="c7486-115">ResourceIdAndDirectoryParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceId] <String> -DirectoryPath <String> [-Recursive] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7486-116">ResourceIdAndPathParameterSet</span><span class="sxs-lookup"><span data-stu-id="c7486-116">ResourceIdAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceId] <String> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7486-117">ObjectAndDirectoryParameterSet</span><span class="sxs-lookup"><span data-stu-id="c7486-117">ObjectAndDirectoryParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-InputObject] <PSCloudEndpoint> -DirectoryPath <String> [-Recursive]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7486-118">ObjectAndPathParameterSet</span><span class="sxs-lookup"><span data-stu-id="c7486-118">ObjectAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-InputObject] <PSCloudEndpoint> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7486-119">설명</span><span class="sxs-lookup"><span data-stu-id="c7486-119">DESCRIPTION</span></span>
<span data-ttu-id="c7486-120">Azure 파일 동기화는 주기적으로 동기화된 Azure 파일 공유 내부의 네임스페이스에서 동기화가 다른 수단으로 파일 공유에 들어온 변경 내용을 검사합니다. 목표는 이러한 변경 내용을 식별하고 궁극적으로 연결된 서버에 동기화하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="c7486-120">Periodically, Azure File Sync checks the namespace inside a syncing Azure file share for changes that came into the file share by other means than sync. The goal is to identify these changes and ultimately sync them to connected servers.</span></span> <span data-ttu-id="c7486-121">이 명령을 사용하여 네임스페이스 변경 내용의 검색을 수동으로 시작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c7486-121">This command can be used to manually initiate the detection of namespaces changes.</span></span> <span data-ttu-id="c7486-122">전체 공유, 하위 폴더 또는 파일 집합을 대상으로 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c7486-122">It can be targeted to the entire share, subfolder or set of files.</span></span> <span data-ttu-id="c7486-123">변경 범위가 알려진 경우 이 명령의 실행을 네임스페이스의 일부로 제한하여 10,000개 항목 제한 내에서 변경 검색을 신속하게 완료할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c7486-123">If the scope of changes is known to you, limit the execution of this command to parts of the namespace, so change detection can finish quickly and within the 10,000 items limit.</span></span>

## <span data-ttu-id="c7486-124">예제</span><span class="sxs-lookup"><span data-stu-id="c7486-124">EXAMPLES</span></span>

### <span data-ttu-id="c7486-125">예제 1</span><span class="sxs-lookup"><span data-stu-id="c7486-125">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "b38fc242-8100-4807-89d0-399cef5863bf" -Path "Data","Reporting\Templates"
```

<span data-ttu-id="c7486-126">이 예제에서는 변경 검색이 동기화된 Azure 파일 공유의 "데이터" 및 "Reporting\Templates" 원장에서 실행됩니다.</span><span class="sxs-lookup"><span data-stu-id="c7486-126">In this example, change detection is run in the "Data" and "Reporting\Templates" directories of a syncing Azure file share.</span></span> <span data-ttu-id="c7486-127">모든 경로는 Azure 파일 공유 네임스페이스의 루트에 상대적입니다.</span><span class="sxs-lookup"><span data-stu-id="c7486-127">All paths are relative to the root of the Azure file share namespace.</span></span>

### <span data-ttu-id="c7486-128">예제 2</span><span class="sxs-lookup"><span data-stu-id="c7486-128">Example 2</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "b38fc242-8100-4807-89d0-399cef5863bf" -Path "Data\results.xslx","Reporting\Templates\generated.pptx"
```

<span data-ttu-id="c7486-129">이 예제에서는 명령 호출자에 변경된 것으로 알려진 파일 집합에 대해 변경 검색이 실행됩니다.</span><span class="sxs-lookup"><span data-stu-id="c7486-129">In this example, change detection is run for a set of files that are known to the command caller to have changed.</span></span> <span data-ttu-id="c7486-130">목표는 Azure 파일 동기화가 이러한 변경 내용도 검색하고 동기화하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="c7486-130">The goal is to have Azure file sync detect and sync these changes as well.</span></span>

### <span data-ttu-id="c7486-131">예제 3</span><span class="sxs-lookup"><span data-stu-id="c7486-131">Example 3</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "b38fc242-8100-4807-89d0-399cef5863bf" -DirectoryPath "Examples" -Recursive
```

<span data-ttu-id="c7486-132">이 예제에서 변경 내용 검색은 "Examples" 디렉터리에 대해 실행되고 하위 디렉터리의 변경 내용을 재발적으로 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="c7486-132">In this example, change detection is run for the "Examples" directory and will recursively detect changes in subdirectories.</span></span> <span data-ttu-id="c7486-133">경로에 10,000개 이상의 항목이 포함된 경우 cmdlet이 실패합니다.</span><span class="sxs-lookup"><span data-stu-id="c7486-133">Keep in mind the cmdlet will fail if the path contains more than 10,000 items.</span></span> <span data-ttu-id="c7486-134">경로에 10,000개가 넘는 항목이 포함된 경우 네임스페이스의 하위 부분에서 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="c7486-134">If the path contains more than 10,000 items, run the command on sub-parts of the namespace.</span></span>

## <span data-ttu-id="c7486-135">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c7486-135">PARAMETERS</span></span>

### <span data-ttu-id="c7486-136">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c7486-136">-AsJob</span></span>
<span data-ttu-id="c7486-137">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="c7486-137">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c7486-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7486-138">-DefaultProfile</span></span>
<span data-ttu-id="c7486-139">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c7486-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c7486-140">-DirectoryPath</span><span class="sxs-lookup"><span data-stu-id="c7486-140">-DirectoryPath</span></span>
<span data-ttu-id="c7486-141">변경 검색을 수행할 디렉터리입니다.</span><span class="sxs-lookup"><span data-stu-id="c7486-141">Directory where change detection will be performed.</span></span>

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

### <span data-ttu-id="c7486-142">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c7486-142">-InputObject</span></span>
<span data-ttu-id="c7486-143">일반적으로 매개 변수를 통해 전달되는 CloudEndpoint 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="c7486-143">CloudEndpoint Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="c7486-144">-Name</span><span class="sxs-lookup"><span data-stu-id="c7486-144">-Name</span></span>
<span data-ttu-id="c7486-145">CloudEndpoint의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c7486-145">Name of the CloudEndpoint.</span></span> <span data-ttu-id="c7486-146">이름은 포털에 표시되는 이름이 아닌 GUID입니다.</span><span class="sxs-lookup"><span data-stu-id="c7486-146">The name is a GUID, not the friendly name that's displayed in the portal.</span></span> <span data-ttu-id="c7486-147">CloudEndpointName을 얻습니다. Get-AzStorageSyncCloudEndpoint cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7486-147">To get the CloudEndpointName, use the Get-AzStorageSyncCloudEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="c7486-148">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c7486-148">-PassThru</span></span>
<span data-ttu-id="c7486-149">정상적인 실행에서 이 cmdlet은 성공 시 값을 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c7486-149">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="c7486-150">PassThru 매개 변수를 제공하는 경우 cmdlet은 실행에 성공한 후 파이프라인에 값을 쓴다.</span><span class="sxs-lookup"><span data-stu-id="c7486-150">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="c7486-151">-Path</span><span class="sxs-lookup"><span data-stu-id="c7486-151">-Path</span></span>
<span data-ttu-id="c7486-152">변경 검색을 수행할 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="c7486-152">Path where change detection will be performed.</span></span>

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

### <span data-ttu-id="c7486-153">-Recursive</span><span class="sxs-lookup"><span data-stu-id="c7486-153">-Recursive</span></span>
<span data-ttu-id="c7486-154">디렉터리 변경 검색이 재발하는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="c7486-154">Indication whether directory change detection is recursive.</span></span>

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

### <span data-ttu-id="c7486-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7486-155">-ResourceGroupName</span></span>
<span data-ttu-id="c7486-156">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c7486-156">Resource Group Name.</span></span>

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

### <span data-ttu-id="c7486-157">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c7486-157">-ResourceId</span></span>
<span data-ttu-id="c7486-158">CloudEndpoint 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="c7486-158">CloudEndpoint Resource Id</span></span>

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

### <span data-ttu-id="c7486-159">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="c7486-159">-StorageSyncServiceName</span></span>
<span data-ttu-id="c7486-160">StorageSyncService의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c7486-160">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="c7486-161">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="c7486-161">-SyncGroupName</span></span>
<span data-ttu-id="c7486-162">SyncGroup의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c7486-162">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="c7486-163">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c7486-163">-Confirm</span></span>
<span data-ttu-id="c7486-164">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c7486-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7486-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7486-165">-WhatIf</span></span>
<span data-ttu-id="c7486-166">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="c7486-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7486-167">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c7486-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7486-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7486-168">CommonParameters</span></span>
<span data-ttu-id="c7486-169">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c7486-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7486-170">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c7486-170">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7486-171">입력</span><span class="sxs-lookup"><span data-stu-id="c7486-171">INPUTS</span></span>

### <span data-ttu-id="c7486-172">System.String</span><span class="sxs-lookup"><span data-stu-id="c7486-172">System.String</span></span>

### <span data-ttu-id="c7486-173">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="c7486-173">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="c7486-174">출력</span><span class="sxs-lookup"><span data-stu-id="c7486-174">OUTPUTS</span></span>

### <span data-ttu-id="c7486-175">System.Void</span><span class="sxs-lookup"><span data-stu-id="c7486-175">System.Void</span></span>

## <span data-ttu-id="c7486-176">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c7486-176">NOTES</span></span>

## <span data-ttu-id="c7486-177">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c7486-177">RELATED LINKS</span></span>
