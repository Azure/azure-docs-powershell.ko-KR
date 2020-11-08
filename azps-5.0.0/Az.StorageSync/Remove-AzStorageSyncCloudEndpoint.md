---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/remove-Azstoragesynccloudendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncCloudEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncCloudEndpoint.md
ms.openlocfilehash: ae3d75b90e6e095072b8e6e6543e2f122fe4cb50
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216330"
---
# <span data-ttu-id="a5393-101">Remove-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="a5393-101">Remove-AzStorageSyncCloudEndpoint</span></span>

## <span data-ttu-id="a5393-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5393-102">SYNOPSIS</span></span>
<span data-ttu-id="a5393-103">이 명령은 동기화 그룹에서 지정 된 클라우드 끝점을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5393-103">This command will delete the specified cloud endpoint from a sync group.</span></span> <span data-ttu-id="a5393-104">하나 이상의 클라우드 끝점이 없으면이 동기화 그룹의 다른 서버 끝점을 동기화 할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="a5393-104">Without at least one cloud endpoint, no other server endpoints in this sync group can sync.</span></span>

## <span data-ttu-id="a5393-105">구문과</span><span class="sxs-lookup"><span data-stu-id="a5393-105">SYNTAX</span></span>

### <span data-ttu-id="a5393-106">StringParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="a5393-106">StringParameterSet (Default)</span></span>
```
Remove-AzStorageSyncCloudEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5393-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5393-107">InputObjectParameterSet</span></span>
```
Remove-AzStorageSyncCloudEndpoint [-InputObject] <PSCloudEndpoint> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5393-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5393-108">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncCloudEndpoint [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5393-109">설명은</span><span class="sxs-lookup"><span data-stu-id="a5393-109">DESCRIPTION</span></span>
<span data-ttu-id="a5393-110">이 명령은 동기화 그룹에서 지정 된 클라우드 끝점을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5393-110">This command will delete the specified cloud endpoint from a sync group.</span></span> <span data-ttu-id="a5393-111">클라우드 끝점 참조에 대 한 Azure 파일 공유는이 프로세스에 의해 그대로 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a5393-111">The Azure file share the cloud endpoint references remains untouched by this process.</span></span> <span data-ttu-id="a5393-112">이 명령은 서비스를 해제 하기 위한 목적 으로만 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a5393-112">This command is only intended for decommissioning.</span></span> <span data-ttu-id="a5393-113">클라우드 끝점 제거는 소거식 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="a5393-113">Removing a cloud endpoint is a destructive operation.</span></span> <span data-ttu-id="a5393-114">하나 이상의 클라우드 끝점을 포함 하지 않고는 서버 끝점을 동기화 할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="a5393-114">Server endpoints cannot sync without at least one cloud endpoint present.</span></span> <span data-ttu-id="a5393-115">동기화 문제를 해결 하기 위해이 작업을 수행 하면 안 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a5393-115">This operation should not be performed to solve sync issues.</span></span> <span data-ttu-id="a5393-116">이 Azure 파일 공유가 클라우드 끝점으로 동일한 동기화 그룹에 다시 추가 되는 경우 충돌 파일과 기타 의도 하지 않은 결과가 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a5393-116">If this Azure file share is added again to the same sync group, as a cloud endpoint, it can lead to conflict files and other unintended consequences.</span></span>

## <span data-ttu-id="a5393-117">예제의</span><span class="sxs-lookup"><span data-stu-id="a5393-117">EXAMPLES</span></span>

### <span data-ttu-id="a5393-118">예제 1</span><span class="sxs-lookup"><span data-stu-id="a5393-118">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncCloudEndpoint -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myCloudEndpointName"
```

<span data-ttu-id="a5393-119">이 명령은 클라우드 끝점을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5393-119">This command will remove the cloud endpoint.</span></span>

## <span data-ttu-id="a5393-120">변수</span><span class="sxs-lookup"><span data-stu-id="a5393-120">PARAMETERS</span></span>

### <span data-ttu-id="a5393-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a5393-121">-AsJob</span></span>
<span data-ttu-id="a5393-122">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="a5393-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a5393-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5393-123">-DefaultProfile</span></span>
<span data-ttu-id="a5393-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a5393-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5393-125">-Force</span><span class="sxs-lookup"><span data-stu-id="a5393-125">-Force</span></span>
<span data-ttu-id="a5393-126">이 명령에 대 한 확인을 건너뛰기 위해-Force를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5393-126">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="a5393-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a5393-127">-InputObject</span></span>
<span data-ttu-id="a5393-128">일반적으로 파이프라인을 통해 전달 되는 CloudEndpoint 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="a5393-128">CloudEndpoint Input Object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="a5393-129">-이름</span><span class="sxs-lookup"><span data-stu-id="a5393-129">-Name</span></span>
<span data-ttu-id="a5393-130">CloudEndpoint의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a5393-130">Name of the CloudEndpoint.</span></span>

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

### <span data-ttu-id="a5393-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a5393-131">-PassThru</span></span>
<span data-ttu-id="a5393-132">일반 실행에서이 cmdlet은 성공에 대 한 값을 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a5393-132">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="a5393-133">PassThru 매개 변수를 제공 하는 경우 cmdlet은 성공적으로 실행 된 후 파이프라인에 값을 기록 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5393-133">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="a5393-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5393-134">-ResourceGroupName</span></span>
<span data-ttu-id="a5393-135">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a5393-135">Resource Group Name.</span></span>

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

### <span data-ttu-id="a5393-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a5393-136">-ResourceId</span></span>
<span data-ttu-id="a5393-137">CloudEndpoint 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="a5393-137">CloudEndpoint Resource Id</span></span>

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

### <span data-ttu-id="a5393-138">-Storages Cservicename</span><span class="sxs-lookup"><span data-stu-id="a5393-138">-StorageSyncServiceName</span></span>
<span data-ttu-id="a5393-139">Storages<c13> Cservice의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a5393-139">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="a5393-140">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="a5393-140">-SyncGroupName</span></span>
<span data-ttu-id="a5393-141">SyncGroup의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a5393-141">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="a5393-142">-확인</span><span class="sxs-lookup"><span data-stu-id="a5393-142">-Confirm</span></span>
<span data-ttu-id="a5393-143">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5393-143">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5393-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5393-144">-WhatIf</span></span>
<span data-ttu-id="a5393-145">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a5393-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a5393-146">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a5393-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5393-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5393-147">CommonParameters</span></span>
<span data-ttu-id="a5393-148">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5393-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5393-149">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5393-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5393-150">입력</span><span class="sxs-lookup"><span data-stu-id="a5393-150">INPUTS</span></span>

### <span data-ttu-id="a5393-151">StorageSync. c c i. PSCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="a5393-151">Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint</span></span>

### <span data-ttu-id="a5393-152">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a5393-152">System.String</span></span>

## <span data-ttu-id="a5393-153">출력</span><span class="sxs-lookup"><span data-stu-id="a5393-153">OUTPUTS</span></span>

### <span data-ttu-id="a5393-154">System. 개체</span><span class="sxs-lookup"><span data-stu-id="a5393-154">System.Object</span></span>
## <span data-ttu-id="a5393-155">상속자</span><span class="sxs-lookup"><span data-stu-id="a5393-155">NOTES</span></span>

## <span data-ttu-id="a5393-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a5393-156">RELATED LINKS</span></span>
