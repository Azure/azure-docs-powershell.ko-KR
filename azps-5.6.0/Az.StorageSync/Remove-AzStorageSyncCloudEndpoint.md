---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/powershell/module/Az.storagesync/remove-Azstoragesynccloudendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncCloudEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncCloudEndpoint.md
ms.openlocfilehash: 451df6b0608ece9888b1525388784dcee1aac334
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974075"
---
# <span data-ttu-id="e348c-101">Remove-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="e348c-101">Remove-AzStorageSyncCloudEndpoint</span></span>

## <span data-ttu-id="e348c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e348c-102">SYNOPSIS</span></span>
<span data-ttu-id="e348c-103">이 명령은 동기화 그룹에서 지정된 클라우드 엔드포인트를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="e348c-103">This command will delete the specified cloud endpoint from a sync group.</span></span> <span data-ttu-id="e348c-104">하나 이상의 클라우드 엔드포인트가 없는 경우 이 동기화 그룹의 다른 서버 엔드포인트는 동기화할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="e348c-104">Without at least one cloud endpoint, no other server endpoints in this sync group can sync.</span></span>

## <span data-ttu-id="e348c-105">구문</span><span class="sxs-lookup"><span data-stu-id="e348c-105">SYNTAX</span></span>

### <span data-ttu-id="e348c-106">StringParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="e348c-106">StringParameterSet (Default)</span></span>
```
Remove-AzStorageSyncCloudEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e348c-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e348c-107">InputObjectParameterSet</span></span>
```
Remove-AzStorageSyncCloudEndpoint [-InputObject] <PSCloudEndpoint> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e348c-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e348c-108">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncCloudEndpoint [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e348c-109">설명</span><span class="sxs-lookup"><span data-stu-id="e348c-109">DESCRIPTION</span></span>
<span data-ttu-id="e348c-110">이 명령은 동기화 그룹에서 지정된 클라우드 엔드포인트를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="e348c-110">This command will delete the specified cloud endpoint from a sync group.</span></span> <span data-ttu-id="e348c-111">클라우드 엔드포인트 참조를 공유하는 Azure 파일에서는 이 프로세스에 의해 그대로 남아 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e348c-111">The Azure file share the cloud endpoint references remains untouched by this process.</span></span> <span data-ttu-id="e348c-112">이 명령은 해제를 위한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="e348c-112">This command is only intended for decommissioning.</span></span> <span data-ttu-id="e348c-113">클라우드 엔드포인트를 제거하는 것은 파괴적인 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="e348c-113">Removing a cloud endpoint is a destructive operation.</span></span> <span data-ttu-id="e348c-114">서버 엔드포인트는 하나 이상의 클라우드 엔드포인트가 없는 경우 동기화할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="e348c-114">Server endpoints cannot sync without at least one cloud endpoint present.</span></span> <span data-ttu-id="e348c-115">동기화 문제를 해결하기 위해 이 작업을 수행하면 안 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e348c-115">This operation should not be performed to solve sync issues.</span></span> <span data-ttu-id="e348c-116">이 Azure 파일 공유가 동일한 동기화 그룹에 다시 추가되는 경우 클라우드 엔드포인트로 충돌 파일 및 기타 의도하지 않은 결과가 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e348c-116">If this Azure file share is added again to the same sync group, as a cloud endpoint, it can lead to conflict files and other unintended consequences.</span></span>

## <span data-ttu-id="e348c-117">예제</span><span class="sxs-lookup"><span data-stu-id="e348c-117">EXAMPLES</span></span>

### <span data-ttu-id="e348c-118">예제 1</span><span class="sxs-lookup"><span data-stu-id="e348c-118">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncCloudEndpoint -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myCloudEndpointName"
```

<span data-ttu-id="e348c-119">이 명령은 클라우드 엔드포인트를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e348c-119">This command will remove the cloud endpoint.</span></span>

## <span data-ttu-id="e348c-120">매개 변수</span><span class="sxs-lookup"><span data-stu-id="e348c-120">PARAMETERS</span></span>

### <span data-ttu-id="e348c-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e348c-121">-AsJob</span></span>
<span data-ttu-id="e348c-122">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="e348c-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e348c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e348c-123">-DefaultProfile</span></span>
<span data-ttu-id="e348c-124">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e348c-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e348c-125">-Force</span><span class="sxs-lookup"><span data-stu-id="e348c-125">-Force</span></span>
<span data-ttu-id="e348c-126">이 명령의 확인을 건너뛰기 위해 -Force를 공급합니다.</span><span class="sxs-lookup"><span data-stu-id="e348c-126">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="e348c-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e348c-127">-InputObject</span></span>
<span data-ttu-id="e348c-128">CloudEndpoint 입력 개체( 일반적으로 파이프라인을 통과합니다.</span><span class="sxs-lookup"><span data-stu-id="e348c-128">CloudEndpoint Input Object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="e348c-129">-Name</span><span class="sxs-lookup"><span data-stu-id="e348c-129">-Name</span></span>
<span data-ttu-id="e348c-130">CloudEndpoint의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e348c-130">Name of the CloudEndpoint.</span></span>

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

### <span data-ttu-id="e348c-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e348c-131">-PassThru</span></span>
<span data-ttu-id="e348c-132">정상적인 실행에서 이 cmdlet은 성공에 대한 값을 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e348c-132">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="e348c-133">PassThru 매개 변수를 제공하는 경우 cmdlet은 성공적으로 실행된 후 파이프라인에 값을 쓴다.</span><span class="sxs-lookup"><span data-stu-id="e348c-133">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="e348c-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e348c-134">-ResourceGroupName</span></span>
<span data-ttu-id="e348c-135">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e348c-135">Resource Group Name.</span></span>

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

### <span data-ttu-id="e348c-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e348c-136">-ResourceId</span></span>
<span data-ttu-id="e348c-137">CloudEndpoint 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="e348c-137">CloudEndpoint Resource Id</span></span>

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

### <span data-ttu-id="e348c-138">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="e348c-138">-StorageSyncServiceName</span></span>
<span data-ttu-id="e348c-139">StorageSyncService의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e348c-139">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="e348c-140">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="e348c-140">-SyncGroupName</span></span>
<span data-ttu-id="e348c-141">SyncGroup의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e348c-141">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="e348c-142">-확인</span><span class="sxs-lookup"><span data-stu-id="e348c-142">-Confirm</span></span>
<span data-ttu-id="e348c-143">cmdlet을 실행하기 전에 확인을 요청합니다.</span><span class="sxs-lookup"><span data-stu-id="e348c-143">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e348c-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e348c-144">-WhatIf</span></span>
<span data-ttu-id="e348c-145">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="e348c-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e348c-146">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e348c-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e348c-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e348c-147">CommonParameters</span></span>
<span data-ttu-id="e348c-148">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e348c-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e348c-149">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e348c-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e348c-150">입력</span><span class="sxs-lookup"><span data-stu-id="e348c-150">INPUTS</span></span>

### <span data-ttu-id="e348c-151">Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="e348c-151">Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint</span></span>

### <span data-ttu-id="e348c-152">System.String</span><span class="sxs-lookup"><span data-stu-id="e348c-152">System.String</span></span>

## <span data-ttu-id="e348c-153">출력</span><span class="sxs-lookup"><span data-stu-id="e348c-153">OUTPUTS</span></span>

### <span data-ttu-id="e348c-154">System.Object</span><span class="sxs-lookup"><span data-stu-id="e348c-154">System.Object</span></span>
## <span data-ttu-id="e348c-155">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e348c-155">NOTES</span></span>

## <span data-ttu-id="e348c-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e348c-156">RELATED LINKS</span></span>
