---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/az.storagesync/remove-azstoragesyncserverendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncServerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncServerEndpoint.md
ms.openlocfilehash: 9afb334e7c26b49bddcabdbcd1ac4036fc3a77c6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188825"
---
# <span data-ttu-id="0a0ea-101">Remove-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="0a0ea-101">Remove-AzStorageSyncServerEndpoint</span></span>

## <span data-ttu-id="0a0ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a0ea-102">SYNOPSIS</span></span>
<span data-ttu-id="0a0ea-103">이 명령은 지정된 서버 엔드포인트를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="0a0ea-103">This command will delete the specified server endpoint.</span></span> <span data-ttu-id="0a0ea-104">이 위치에 동기화하면 즉시 중지됩니다.</span><span class="sxs-lookup"><span data-stu-id="0a0ea-104">Sync to this location will stop immediately.</span></span>

## <span data-ttu-id="0a0ea-105">구문</span><span class="sxs-lookup"><span data-stu-id="0a0ea-105">SYNTAX</span></span>

### <span data-ttu-id="0a0ea-106">StringParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="0a0ea-106">StringParameterSet (Default)</span></span>
```
Remove-AzStorageSyncServerEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a0ea-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0a0ea-107">InputObjectParameterSet</span></span>
```
Remove-AzStorageSyncServerEndpoint [-InputObject] <PSServerEndpoint> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a0ea-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0a0ea-108">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncServerEndpoint [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a0ea-109">설명</span><span class="sxs-lookup"><span data-stu-id="0a0ea-109">DESCRIPTION</span></span>
<span data-ttu-id="0a0ea-110">서버 엔드포인트를 제거하는 것은 파괴적인 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="0a0ea-110">Removing a server endpoint is a destructive operation.</span></span> <span data-ttu-id="0a0ea-111">이 서버 위치는 동기화를 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="0a0ea-111">This server location will stop syncing.</span></span> <span data-ttu-id="0a0ea-112">동기화 문제를 해결하기 위해 이 작업을 수행하면 안 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0a0ea-112">This operation should not be performed to solve sync issues.</span></span> <span data-ttu-id="0a0ea-113">이 서버 위치(파일 포함)가 서버 엔드포인트와 동일한 동기화 그룹에 다시 추가되는 경우 파일 충돌 및 기타 의도하지 않은 결과가 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0a0ea-113">If this server location (incl. it's files) is added again to the same sync group as a server endpoint, it can lead to conflict files and other unintended consequences.</span></span> <span data-ttu-id="0a0ea-114">이 명령은 해제 전용입니다.</span><span class="sxs-lookup"><span data-stu-id="0a0ea-114">This command is intended for decommissioning only.</span></span>

## <span data-ttu-id="0a0ea-115">예제</span><span class="sxs-lookup"><span data-stu-id="0a0ea-115">EXAMPLES</span></span>

### <span data-ttu-id="0a0ea-116">예제 1</span><span class="sxs-lookup"><span data-stu-id="0a0ea-116">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncServerEndpoint -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myServerEndpointName"
```

<span data-ttu-id="0a0ea-117">이 명령은 서버 엔드포인트를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="0a0ea-117">This command will remove the server endpoint.</span></span>

## <span data-ttu-id="0a0ea-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0a0ea-118">PARAMETERS</span></span>

### <span data-ttu-id="0a0ea-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0a0ea-119">-AsJob</span></span>
<span data-ttu-id="0a0ea-120">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="0a0ea-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0a0ea-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a0ea-121">-DefaultProfile</span></span>
<span data-ttu-id="0a0ea-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0a0ea-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a0ea-123">-Force</span><span class="sxs-lookup"><span data-stu-id="0a0ea-123">-Force</span></span>
<span data-ttu-id="0a0ea-124">이 명령의 확인을 건너뛰기 위해 -Force를 공급합니다.</span><span class="sxs-lookup"><span data-stu-id="0a0ea-124">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="0a0ea-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0a0ea-125">-InputObject</span></span>
<span data-ttu-id="0a0ea-126">일반적으로 파이프라인을 통해 전달되는 ServerEndpoint 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="0a0ea-126">ServerEndpoint Input Object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0a0ea-127">-Name</span><span class="sxs-lookup"><span data-stu-id="0a0ea-127">-Name</span></span>
<span data-ttu-id="0a0ea-128">ServerEndpoint의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0a0ea-128">Name of the ServerEndpoint.</span></span>

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

### <span data-ttu-id="0a0ea-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0a0ea-129">-PassThru</span></span>
<span data-ttu-id="0a0ea-130">정상적인 실행에서 이 cmdlet은 성공 시 값을 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0a0ea-130">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="0a0ea-131">PassThru 매개 변수를 제공하는 경우 cmdlet은 실행에 성공한 후 파이프라인에 값을 쓴다.</span><span class="sxs-lookup"><span data-stu-id="0a0ea-131">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="0a0ea-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a0ea-132">-ResourceGroupName</span></span>
<span data-ttu-id="0a0ea-133">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0a0ea-133">Resource Group Name.</span></span>

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

### <span data-ttu-id="0a0ea-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0a0ea-134">-ResourceId</span></span>
<span data-ttu-id="0a0ea-135">ServerEndpoint 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="0a0ea-135">ServerEndpoint Resource Id</span></span>

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

### <span data-ttu-id="0a0ea-136">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="0a0ea-136">-StorageSyncServiceName</span></span>
<span data-ttu-id="0a0ea-137">StorageSyncService의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0a0ea-137">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="0a0ea-138">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="0a0ea-138">-SyncGroupName</span></span>
<span data-ttu-id="0a0ea-139">SyncGroup의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0a0ea-139">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="0a0ea-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0a0ea-140">-Confirm</span></span>
<span data-ttu-id="0a0ea-141">cmdlet을 실행하기 전에 확인을 요청합니다.</span><span class="sxs-lookup"><span data-stu-id="0a0ea-141">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a0ea-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a0ea-142">-WhatIf</span></span>
<span data-ttu-id="0a0ea-143">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="0a0ea-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0a0ea-144">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0a0ea-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a0ea-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a0ea-145">CommonParameters</span></span>
<span data-ttu-id="0a0ea-146">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0a0ea-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a0ea-147">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="0a0ea-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a0ea-148">입력</span><span class="sxs-lookup"><span data-stu-id="0a0ea-148">INPUTS</span></span>

### <span data-ttu-id="0a0ea-149">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="0a0ea-149">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

### <span data-ttu-id="0a0ea-150">System.String</span><span class="sxs-lookup"><span data-stu-id="0a0ea-150">System.String</span></span>

## <span data-ttu-id="0a0ea-151">출력</span><span class="sxs-lookup"><span data-stu-id="0a0ea-151">OUTPUTS</span></span>

### <span data-ttu-id="0a0ea-152">System.Object</span><span class="sxs-lookup"><span data-stu-id="0a0ea-152">System.Object</span></span>
## <span data-ttu-id="0a0ea-153">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0a0ea-153">NOTES</span></span>

## <span data-ttu-id="0a0ea-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0a0ea-154">RELATED LINKS</span></span>
