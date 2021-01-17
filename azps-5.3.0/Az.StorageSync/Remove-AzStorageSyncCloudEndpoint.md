---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/remove-Azstoragesynccloudendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncCloudEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncCloudEndpoint.md
ms.openlocfilehash: ae3d75b90e6e095072b8e6e6543e2f122fe4cb50
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491187"
---
# <span data-ttu-id="9092e-101">Remove-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="9092e-101">Remove-AzStorageSyncCloudEndpoint</span></span>

## <span data-ttu-id="9092e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9092e-102">SYNOPSIS</span></span>
<span data-ttu-id="9092e-103">이 명령은 동기화 그룹에서 지정된 클라우드 엔드포인트를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="9092e-103">This command will delete the specified cloud endpoint from a sync group.</span></span> <span data-ttu-id="9092e-104">하나 이상의 클라우드 엔드포인트가 없는 경우 이 동기화 그룹의 다른 서버 엔드포인트는 동기화할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="9092e-104">Without at least one cloud endpoint, no other server endpoints in this sync group can sync.</span></span>

## <span data-ttu-id="9092e-105">구문</span><span class="sxs-lookup"><span data-stu-id="9092e-105">SYNTAX</span></span>

### <span data-ttu-id="9092e-106">StringParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="9092e-106">StringParameterSet (Default)</span></span>
```
Remove-AzStorageSyncCloudEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9092e-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9092e-107">InputObjectParameterSet</span></span>
```
Remove-AzStorageSyncCloudEndpoint [-InputObject] <PSCloudEndpoint> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9092e-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9092e-108">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncCloudEndpoint [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9092e-109">설명</span><span class="sxs-lookup"><span data-stu-id="9092e-109">DESCRIPTION</span></span>
<span data-ttu-id="9092e-110">이 명령은 동기화 그룹에서 지정된 클라우드 엔드포인트를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="9092e-110">This command will delete the specified cloud endpoint from a sync group.</span></span> <span data-ttu-id="9092e-111">Azure 파일 공유 클라우드 엔드포인트 참조는 이 프로세스에 의해 그대로 남아 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9092e-111">The Azure file share the cloud endpoint references remains untouched by this process.</span></span> <span data-ttu-id="9092e-112">이 명령은 해제 전용입니다.</span><span class="sxs-lookup"><span data-stu-id="9092e-112">This command is only intended for decommissioning.</span></span> <span data-ttu-id="9092e-113">클라우드 엔드포인트를 제거하는 것은 파괴적인 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="9092e-113">Removing a cloud endpoint is a destructive operation.</span></span> <span data-ttu-id="9092e-114">하나 이상의 클라우드 엔드포인트가 없는 경우 서버 엔드포인트를 동기화할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="9092e-114">Server endpoints cannot sync without at least one cloud endpoint present.</span></span> <span data-ttu-id="9092e-115">동기화 문제를 해결하기 위해 이 작업을 수행하면 안 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9092e-115">This operation should not be performed to solve sync issues.</span></span> <span data-ttu-id="9092e-116">이 Azure 파일 공유가 클라우드 엔드포인트와 동일한 동기화 그룹에 다시 추가되는 경우 충돌 파일 및 기타 의도하지 않은 결과가 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9092e-116">If this Azure file share is added again to the same sync group, as a cloud endpoint, it can lead to conflict files and other unintended consequences.</span></span>

## <span data-ttu-id="9092e-117">예제</span><span class="sxs-lookup"><span data-stu-id="9092e-117">EXAMPLES</span></span>

### <span data-ttu-id="9092e-118">예제 1</span><span class="sxs-lookup"><span data-stu-id="9092e-118">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncCloudEndpoint -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myCloudEndpointName"
```

<span data-ttu-id="9092e-119">이 명령은 클라우드 엔드포인트를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="9092e-119">This command will remove the cloud endpoint.</span></span>

## <span data-ttu-id="9092e-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9092e-120">PARAMETERS</span></span>

### <span data-ttu-id="9092e-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9092e-121">-AsJob</span></span>
<span data-ttu-id="9092e-122">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="9092e-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9092e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9092e-123">-DefaultProfile</span></span>
<span data-ttu-id="9092e-124">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9092e-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9092e-125">-Force</span><span class="sxs-lookup"><span data-stu-id="9092e-125">-Force</span></span>
<span data-ttu-id="9092e-126">이 명령의 확인을 건너뛰기 위해 -Force를 공급합니다.</span><span class="sxs-lookup"><span data-stu-id="9092e-126">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="9092e-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9092e-127">-InputObject</span></span>
<span data-ttu-id="9092e-128">일반적으로 파이프라인을 통해 전달되는 CloudEndpoint 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="9092e-128">CloudEndpoint Input Object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9092e-129">-Name</span><span class="sxs-lookup"><span data-stu-id="9092e-129">-Name</span></span>
<span data-ttu-id="9092e-130">CloudEndpoint의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9092e-130">Name of the CloudEndpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9092e-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9092e-131">-PassThru</span></span>
<span data-ttu-id="9092e-132">정상적인 실행에서 이 cmdlet은 성공 시 값을 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9092e-132">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="9092e-133">PassThru 매개 변수를 제공하는 경우 cmdlet은 실행에 성공한 후 파이프라인에 값을 쓴다.</span><span class="sxs-lookup"><span data-stu-id="9092e-133">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="9092e-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9092e-134">-ResourceGroupName</span></span>
<span data-ttu-id="9092e-135">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9092e-135">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9092e-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9092e-136">-ResourceId</span></span>
<span data-ttu-id="9092e-137">CloudEndpoint 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="9092e-137">CloudEndpoint Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9092e-138">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="9092e-138">-StorageSyncServiceName</span></span>
<span data-ttu-id="9092e-139">StorageSyncService의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9092e-139">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9092e-140">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="9092e-140">-SyncGroupName</span></span>
<span data-ttu-id="9092e-141">SyncGroup의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9092e-141">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ParentName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9092e-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9092e-142">-Confirm</span></span>
<span data-ttu-id="9092e-143">cmdlet을 실행하기 전에 확인을 요청합니다.</span><span class="sxs-lookup"><span data-stu-id="9092e-143">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9092e-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9092e-144">-WhatIf</span></span>
<span data-ttu-id="9092e-145">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="9092e-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9092e-146">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9092e-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9092e-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9092e-147">CommonParameters</span></span>
<span data-ttu-id="9092e-148">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9092e-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9092e-149">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="9092e-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9092e-150">입력</span><span class="sxs-lookup"><span data-stu-id="9092e-150">INPUTS</span></span>

### <span data-ttu-id="9092e-151">Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="9092e-151">Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint</span></span>

### <span data-ttu-id="9092e-152">System.String</span><span class="sxs-lookup"><span data-stu-id="9092e-152">System.String</span></span>

## <span data-ttu-id="9092e-153">출력</span><span class="sxs-lookup"><span data-stu-id="9092e-153">OUTPUTS</span></span>

### <span data-ttu-id="9092e-154">System.Object</span><span class="sxs-lookup"><span data-stu-id="9092e-154">System.Object</span></span>
## <span data-ttu-id="9092e-155">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9092e-155">NOTES</span></span>

## <span data-ttu-id="9092e-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9092e-156">RELATED LINKS</span></span>
