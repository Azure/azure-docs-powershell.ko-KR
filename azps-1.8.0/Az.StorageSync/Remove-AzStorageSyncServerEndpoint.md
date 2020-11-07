---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/az.storagesync/remove-azstoragesyncserverendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncServerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncServerEndpoint.md
ms.openlocfilehash: 328fd4c798380202b355974cc8d9150e1d138da5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698483"
---
# <span data-ttu-id="ad2e9-101">Remove-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="ad2e9-101">Remove-AzStorageSyncServerEndpoint</span></span>

## <span data-ttu-id="ad2e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad2e9-102">SYNOPSIS</span></span>
<span data-ttu-id="ad2e9-103">이 명령은 지정 된 서버 종점을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad2e9-103">This command will delete the specified server endpoint.</span></span> <span data-ttu-id="ad2e9-104">이 위치와 동기화가 즉시 중지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ad2e9-104">Sync to this location will stop immediately.</span></span>

## <span data-ttu-id="ad2e9-105">구문과</span><span class="sxs-lookup"><span data-stu-id="ad2e9-105">SYNTAX</span></span>

### <span data-ttu-id="ad2e9-106">StringParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="ad2e9-106">StringParameterSet (Default)</span></span>
```
Remove-AzStorageSyncServerEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad2e9-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ad2e9-107">InputObjectParameterSet</span></span>
```
Remove-AzStorageSyncServerEndpoint [-InputObject] <PSServerEndpoint> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad2e9-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ad2e9-108">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncServerEndpoint [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad2e9-109">설명은</span><span class="sxs-lookup"><span data-stu-id="ad2e9-109">DESCRIPTION</span></span>
<span data-ttu-id="ad2e9-110">서버 끝점 제거는 소거식 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="ad2e9-110">Removing a server endpoint is a destructive operation.</span></span> <span data-ttu-id="ad2e9-111">이 서버 위치는 동기화를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad2e9-111">This server location will stop syncing.</span></span> <span data-ttu-id="ad2e9-112">동기화 문제를 해결 하기 위해이 작업을 수행 하면 안 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ad2e9-112">This operation should not be performed to solve sync issues.</span></span> <span data-ttu-id="ad2e9-113">이 서버 위치 (포함)가 서버 끝점과 동일한 동기화 그룹에 다시 추가 되 면 충돌 파일과 기타 의도 하지 않은 결과가 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ad2e9-113">If this server location (incl. it's files) is added again to the same sync group as a server endpoint, it can lead to conflict files and other unintended consequences.</span></span> <span data-ttu-id="ad2e9-114">이 명령은 폐기 목적 으로만 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ad2e9-114">This command is intended for decommissioning only.</span></span>

## <span data-ttu-id="ad2e9-115">예제의</span><span class="sxs-lookup"><span data-stu-id="ad2e9-115">EXAMPLES</span></span>

### <span data-ttu-id="ad2e9-116">예제 1</span><span class="sxs-lookup"><span data-stu-id="ad2e9-116">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncServerEndpoint -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myServerEndpointName"
```

<span data-ttu-id="ad2e9-117">이 명령은 서버 끝점을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad2e9-117">This command will remove the server endpoint.</span></span>

## <span data-ttu-id="ad2e9-118">변수</span><span class="sxs-lookup"><span data-stu-id="ad2e9-118">PARAMETERS</span></span>

### <span data-ttu-id="ad2e9-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ad2e9-119">-AsJob</span></span>
<span data-ttu-id="ad2e9-120">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="ad2e9-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ad2e9-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad2e9-121">-DefaultProfile</span></span>
<span data-ttu-id="ad2e9-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ad2e9-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad2e9-123">-Force</span><span class="sxs-lookup"><span data-stu-id="ad2e9-123">-Force</span></span>
<span data-ttu-id="ad2e9-124">이 명령에 대 한 확인을 건너뛰기 위해-Force를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad2e9-124">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="ad2e9-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ad2e9-125">-InputObject</span></span>
<span data-ttu-id="ad2e9-126">일반적으로 파이프라인을 통해 전달 되는 ServerEndpoint 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="ad2e9-126">ServerEndpoint Input Object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="ad2e9-127">-이름</span><span class="sxs-lookup"><span data-stu-id="ad2e9-127">-Name</span></span>
<span data-ttu-id="ad2e9-128">ServerEndpoint의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ad2e9-128">Name of the ServerEndpoint.</span></span>

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

### <span data-ttu-id="ad2e9-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ad2e9-129">-PassThru</span></span>
<span data-ttu-id="ad2e9-130">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="ad2e9-130">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="ad2e9-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad2e9-131">-ResourceGroupName</span></span>
<span data-ttu-id="ad2e9-132">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ad2e9-132">Resource Group Name.</span></span>

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

### <span data-ttu-id="ad2e9-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ad2e9-133">-ResourceId</span></span>
<span data-ttu-id="ad2e9-134">ServerEndpoint 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="ad2e9-134">ServerEndpoint Resource Id</span></span>

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

### <span data-ttu-id="ad2e9-135">-Storages<c13> Cservicename</span><span class="sxs-lookup"><span data-stu-id="ad2e9-135">-StorageSyncServiceName</span></span>
<span data-ttu-id="ad2e9-136">Storages Cservice의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ad2e9-136">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="ad2e9-137">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="ad2e9-137">-SyncGroupName</span></span>
<span data-ttu-id="ad2e9-138">SyncGroup의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ad2e9-138">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="ad2e9-139">-확인</span><span class="sxs-lookup"><span data-stu-id="ad2e9-139">-Confirm</span></span>
<span data-ttu-id="ad2e9-140">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad2e9-140">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad2e9-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad2e9-141">-WhatIf</span></span>
<span data-ttu-id="ad2e9-142">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ad2e9-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ad2e9-143">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ad2e9-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad2e9-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad2e9-144">CommonParameters</span></span>
<span data-ttu-id="ad2e9-145">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad2e9-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad2e9-146">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad2e9-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad2e9-147">입력</span><span class="sxs-lookup"><span data-stu-id="ad2e9-147">INPUTS</span></span>

### <span data-ttu-id="ad2e9-148">StorageSync. a m a. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="ad2e9-148">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

### <span data-ttu-id="ad2e9-149">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ad2e9-149">System.String</span></span>

## <span data-ttu-id="ad2e9-150">출력</span><span class="sxs-lookup"><span data-stu-id="ad2e9-150">OUTPUTS</span></span>

### <span data-ttu-id="ad2e9-151">System. 개체</span><span class="sxs-lookup"><span data-stu-id="ad2e9-151">System.Object</span></span>
## <span data-ttu-id="ad2e9-152">상속자</span><span class="sxs-lookup"><span data-stu-id="ad2e9-152">NOTES</span></span>

## <span data-ttu-id="ad2e9-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ad2e9-153">RELATED LINKS</span></span>
