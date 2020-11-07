---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/az.storagesync/invoke-azstoragesyncchangedetection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncChangeDetection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncChangeDetection.md
ms.openlocfilehash: c266b6623463165f14e01e55f0fec4d2d59a581f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93874339"
---
# <span data-ttu-id="c44b2-101">Invoke-AzStorageSyncChangeDetection</span><span class="sxs-lookup"><span data-stu-id="c44b2-101">Invoke-AzStorageSyncChangeDetection</span></span>

## <span data-ttu-id="c44b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c44b2-102">SYNOPSIS</span></span>
<span data-ttu-id="c44b2-103">이 명령을 사용 하 여 네임 스페이스 변경 감지를 수동으로 시작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c44b2-103">This command can be used to manually initiate the detection of namespaces changes.</span></span> <span data-ttu-id="c44b2-104">전체 공유, 하위 폴더 또는 파일 집합을 대상으로 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c44b2-104">It can be targeted to the entire share, subfolder or set of files.</span></span> <span data-ttu-id="c44b2-105">최대 1만 개의 변경 내용을 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c44b2-105">A maximum of 10,000 changes can be detected.</span></span> <span data-ttu-id="c44b2-106">변경의 범위가 사용자에 게 알려진 경우이 명령의 실행을 네임 스페이스의 부분으로 제한 하 여 변경 내용이 1만 변경 제한 내에서 신속 하 게 완료 될 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="c44b2-106">If the scope of changes is known to you, limit the execution of this command to parts of the namespace, so change detection can finish quickly and within a 10,000 changes limit.</span></span>

## <span data-ttu-id="c44b2-107">구문과</span><span class="sxs-lookup"><span data-stu-id="c44b2-107">SYNTAX</span></span>

### <span data-ttu-id="c44b2-108">StringAndDirectoryParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="c44b2-108">StringAndDirectoryParameterSet (Default)</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -DirectoryPath <String> [-Recursive] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c44b2-109">StringAndPathParameterSet</span><span class="sxs-lookup"><span data-stu-id="c44b2-109">StringAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c44b2-110">ResourceIdAndDirectoryParameterSet</span><span class="sxs-lookup"><span data-stu-id="c44b2-110">ResourceIdAndDirectoryParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceId] <String> -DirectoryPath <String> [-Recursive] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c44b2-111">ResourceIdAndPathParameterSet</span><span class="sxs-lookup"><span data-stu-id="c44b2-111">ResourceIdAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceId] <String> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c44b2-112">ObjectAndDirectoryParameterSet</span><span class="sxs-lookup"><span data-stu-id="c44b2-112">ObjectAndDirectoryParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-InputObject] <PSCloudEndpoint> -DirectoryPath <String> [-Recursive]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c44b2-113">ObjectAndPathParameterSet</span><span class="sxs-lookup"><span data-stu-id="c44b2-113">ObjectAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-InputObject] <PSCloudEndpoint> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c44b2-114">설명은</span><span class="sxs-lookup"><span data-stu-id="c44b2-114">DESCRIPTION</span></span>
<span data-ttu-id="c44b2-115">정기적으로 Azure 파일 동기화는 동기화 하는 것 보다 다른 수단으로 파일 공유에 제공 된 변경 내용에 대 한 Azure 파일 공유 내의 네임 스페이스를 검사 합니다. 목표는 이러한 변경을 식별 하 고 궁극적으로 연결 된 서버와 동기화 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="c44b2-115">Periodically, Azure File Sync checks the namespace inside a syncing Azure file share for changes that came into the file share by other means than sync. The goal is to identify these changes and ultimately sync them to connected servers.</span></span> <span data-ttu-id="c44b2-116">이 명령을 사용 하 여 네임 스페이스 변경 감지를 수동으로 시작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c44b2-116">This command can be used to manually initiate the detection of namespaces changes.</span></span> <span data-ttu-id="c44b2-117">전체 공유, 하위 폴더 또는 파일 집합을 대상으로 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c44b2-117">It can be targeted to the entire share, subfolder or set of files.</span></span> <span data-ttu-id="c44b2-118">변경의 범위가 사용자에 게 알려진 경우이 명령의 실행을 네임 스페이스의 부분으로 제한 하 여 변경 내용이 1만 변경 제한 내에서 신속 하 게 완료 될 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="c44b2-118">If the scope of changes is known to you, limit the execution of this command to parts of the namespace, so change detection can finish quickly and within a 10,000 changes limit.</span></span>

## <span data-ttu-id="c44b2-119">예제의</span><span class="sxs-lookup"><span data-stu-id="c44b2-119">EXAMPLES</span></span>

### <span data-ttu-id="c44b2-120">예제 1</span><span class="sxs-lookup"><span data-stu-id="c44b2-120">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "myCloudEndpointName" -Path "Data","Reporting\Templates"
```

<span data-ttu-id="c44b2-121">이 예제에서는 동기화 Azure 파일 공유의 "Data" 및 "Reporting\Templates" 디렉터리에서 변경 감지를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="c44b2-121">In this example, change detection is run in the "Data" and "Reporting\Templates" directories of a syncing Azure file share.</span></span> <span data-ttu-id="c44b2-122">모든 경로는 Azure 파일 공유 네임 스페이스의 루트를 기준으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="c44b2-122">All paths are relative to the root of the Azure file share namespace.</span></span>

### <span data-ttu-id="c44b2-123">예제 2</span><span class="sxs-lookup"><span data-stu-id="c44b2-123">Example 2</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "myCloudEndpointName" -Path "Data\results.xslx","Reporting\Templates\generated.pptx"
```

<span data-ttu-id="c44b2-124">이 예제에서는 변경 내용 검색이 명령 호출자가 변경 하는 것으로 알려진 파일 집합에 대해 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c44b2-124">In this example, change detection is run for a set of files that are known to the command caller to have changed.</span></span> <span data-ttu-id="c44b2-125">목표는 Azure 파일 동기화를 통해 이러한 변경 내용을 검색 하 고 동기화 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="c44b2-125">The goal is to have Azure file sync detect and sync these changes as well.</span></span>

### <span data-ttu-id="c44b2-126">예제 3</span><span class="sxs-lookup"><span data-stu-id="c44b2-126">Example 3</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "myCloudEndpointName" -DirectoryPath "Examples" -Recursive
```

<span data-ttu-id="c44b2-127">이 예제에서는 "예제" 디렉터리에 대 한 변경 감지를 실행 하 고 하위 디렉터리의 변경 내용을 재귀적으로 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="c44b2-127">In this example, change detection is run for the "Examples" directory and will recursively detect changes in subdirectories.</span></span> <span data-ttu-id="c44b2-128">이 명령은 자동으로 중단 되기 전에 1만 변경 내용을 검색할 수 있다는 점에 유의 하세요.</span><span class="sxs-lookup"><span data-stu-id="c44b2-128">Keep in mind that this command can detect up to 10,000 changes before it is automatically aborted.</span></span> <span data-ttu-id="c44b2-129">1만 변경 내용이 발생 한 것으로 의심 되는 경우 네임 스페이스의 하위 부분에 대 한 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="c44b2-129">If you suspect more than 10,000 changes to have occurred, run the command on sub-parts of the namespace.</span></span>

## <span data-ttu-id="c44b2-130">변수</span><span class="sxs-lookup"><span data-stu-id="c44b2-130">PARAMETERS</span></span>

### <span data-ttu-id="c44b2-131">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c44b2-131">-AsJob</span></span>
<span data-ttu-id="c44b2-132">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="c44b2-132">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c44b2-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c44b2-133">-DefaultProfile</span></span>
<span data-ttu-id="c44b2-134">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c44b2-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c44b2-135">-DirectoryPath</span><span class="sxs-lookup"><span data-stu-id="c44b2-135">-DirectoryPath</span></span>
<span data-ttu-id="c44b2-136">변경 내용 검색이 수행 되는 디렉터리입니다.</span><span class="sxs-lookup"><span data-stu-id="c44b2-136">Directory where change detection will be performed.</span></span>

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

### <span data-ttu-id="c44b2-137">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c44b2-137">-InputObject</span></span>
<span data-ttu-id="c44b2-138">일반적으로 매개 변수를 통해 전달 되는 CloudEndpoint 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="c44b2-138">CloudEndpoint Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="c44b2-139">-이름</span><span class="sxs-lookup"><span data-stu-id="c44b2-139">-Name</span></span>
<span data-ttu-id="c44b2-140">CloudEndpoint의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c44b2-140">Name of the CloudEndpoint.</span></span>

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

### <span data-ttu-id="c44b2-141">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c44b2-141">-PassThru</span></span>
<span data-ttu-id="c44b2-142">일반 실행에서이 cmdlet은 성공에 대 한 값을 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c44b2-142">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="c44b2-143">PassThru 매개 변수를 제공 하는 경우 cmdlet은 성공적으로 실행 된 후 파이프라인에 값을 기록 합니다.</span><span class="sxs-lookup"><span data-stu-id="c44b2-143">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="c44b2-144">-Path</span><span class="sxs-lookup"><span data-stu-id="c44b2-144">-Path</span></span>
<span data-ttu-id="c44b2-145">변경 내용 검색이 수행 되는 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="c44b2-145">Path where change detection will be performed.</span></span>

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

### <span data-ttu-id="c44b2-146">-Recursive</span><span class="sxs-lookup"><span data-stu-id="c44b2-146">-Recursive</span></span>
<span data-ttu-id="c44b2-147">디렉터리 변경 내용 검색이 재귀적 인지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="c44b2-147">Indication whether directory change detection is recursive.</span></span>

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

### <span data-ttu-id="c44b2-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c44b2-148">-ResourceGroupName</span></span>
<span data-ttu-id="c44b2-149">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c44b2-149">Resource Group Name.</span></span>

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

### <span data-ttu-id="c44b2-150">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c44b2-150">-ResourceId</span></span>
<span data-ttu-id="c44b2-151">CloudEndpoint 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="c44b2-151">CloudEndpoint Resource Id</span></span>

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

### <span data-ttu-id="c44b2-152">-Storages<c13> Cservicename</span><span class="sxs-lookup"><span data-stu-id="c44b2-152">-StorageSyncServiceName</span></span>
<span data-ttu-id="c44b2-153">Storages<c13> Cservice의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c44b2-153">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="c44b2-154">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="c44b2-154">-SyncGroupName</span></span>
<span data-ttu-id="c44b2-155">SyncGroup의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c44b2-155">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="c44b2-156">-확인</span><span class="sxs-lookup"><span data-stu-id="c44b2-156">-Confirm</span></span>
<span data-ttu-id="c44b2-157">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c44b2-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c44b2-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c44b2-158">-WhatIf</span></span>
<span data-ttu-id="c44b2-159">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c44b2-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c44b2-160">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c44b2-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c44b2-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c44b2-161">CommonParameters</span></span>
<span data-ttu-id="c44b2-162">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c44b2-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c44b2-163">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c44b2-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c44b2-164">입력</span><span class="sxs-lookup"><span data-stu-id="c44b2-164">INPUTS</span></span>

### <span data-ttu-id="c44b2-165">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c44b2-165">System.String</span></span>

### <span data-ttu-id="c44b2-166">StorageSync. a m a. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="c44b2-166">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="c44b2-167">출력</span><span class="sxs-lookup"><span data-stu-id="c44b2-167">OUTPUTS</span></span>

### <span data-ttu-id="c44b2-168">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="c44b2-168">System.Void</span></span>

## <span data-ttu-id="c44b2-169">상속자</span><span class="sxs-lookup"><span data-stu-id="c44b2-169">NOTES</span></span>

## <span data-ttu-id="c44b2-170">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c44b2-170">RELATED LINKS</span></span>
