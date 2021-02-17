---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/invoke-Azstoragesyncfilerecall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncFileRecall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncFileRecall.md
ms.openlocfilehash: fb053da61aabd9328f4ff3d848243ff9b84d6d09
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195668"
---
# <span data-ttu-id="4282f-101">Invoke-AzStorageSyncFileRecall</span><span class="sxs-lookup"><span data-stu-id="4282f-101">Invoke-AzStorageSyncFileRecall</span></span>

## <span data-ttu-id="4282f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4282f-102">SYNOPSIS</span></span>
<span data-ttu-id="4282f-103">이 명령은 모든 계층화 파일을 로컬 디스크로 회수합니다.</span><span class="sxs-lookup"><span data-stu-id="4282f-103">This command recalls all tiered files back to local disk.</span></span>

## <span data-ttu-id="4282f-104">구문</span><span class="sxs-lookup"><span data-stu-id="4282f-104">SYNTAX</span></span>

### <span data-ttu-id="4282f-105">StringParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="4282f-105">StringParameterSet (Default)</span></span>
```
Invoke-AzStorageSyncFileRecall [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name] <String> [-Pattern <String>] [-RecallPath <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4282f-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4282f-106">ResourceIdParameterSet</span></span>
```
Invoke-AzStorageSyncFileRecall [-ResourceId] <String> [-Pattern <String>] [-RecallPath <String>] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4282f-107">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4282f-107">ObjectParameterSet</span></span>
```
Invoke-AzStorageSyncFileRecall [-InputObject] <PSServerEndpoint> [-Pattern <String>] [-RecallPath <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4282f-108">설명</span><span class="sxs-lookup"><span data-stu-id="4282f-108">DESCRIPTION</span></span>
<span data-ttu-id="4282f-109">클라우드 계층화가 서버 엔드포인트(등록된 서버의 특정 위치)에서 사용하도록 설정되면 이 명령을 사용하여 모든 계층화 파일을 로컬 디스크로 회수할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4282f-109">When cloud tiering is enabled on a server endpoint (a specific location on a registered server) then this command can be used to recall all tiered files to local disk.</span></span> <span data-ttu-id="4282f-110">회수를 시작하기 전에 이 서버 엔드포인트에서 클라우드 계층을 사용하지 않도록 설정하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="4282f-110">It is highly recommended to disable cloud tiering on this server endpoint before starting recall.</span></span> <span data-ttu-id="4282f-111">계층화가 계속 진행 중이면 회수를 통해 다른 파일이 계층화될 수 있습니다. 이 경우 로컬 디스크에 있는 모든 콘텐츠의 원하는 목표를 달성하기 위해 누락된 파일이 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4282f-111">If tiering is still on, recall might lead to other files getting tiered which misses to achieve the desired goal of all content residing on local disk.</span></span>

## <span data-ttu-id="4282f-112">예제</span><span class="sxs-lookup"><span data-stu-id="4282f-112">EXAMPLES</span></span>

### <span data-ttu-id="4282f-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="4282f-113">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncFileRecall -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -ServerEndpointName "myServerEndpointName"
```

<span data-ttu-id="4282f-114">이 명령은 지정된 서버 엔드포인트의 루트 경로 아래에 있는 모든 계층화 파일을 재발적으로 회수합니다.</span><span class="sxs-lookup"><span data-stu-id="4282f-114">This command recursively recalls all tiered files located under the root path of the specified server endpoint.</span></span>

## <span data-ttu-id="4282f-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4282f-115">PARAMETERS</span></span>

### <span data-ttu-id="4282f-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4282f-116">-AsJob</span></span>
<span data-ttu-id="4282f-117">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="4282f-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4282f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4282f-118">-DefaultProfile</span></span>
<span data-ttu-id="4282f-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4282f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4282f-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4282f-120">-InputObject</span></span>
<span data-ttu-id="4282f-121">일반적으로 매개 변수를 통해 전달되는 SyncGroup 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="4282f-121">SyncGroup Object, normally passed through the parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint
Parameter Sets: ObjectParameterSet
Aliases: RegisteredServer, ServerEndpoint

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4282f-122">-Name</span><span class="sxs-lookup"><span data-stu-id="4282f-122">-Name</span></span>
<span data-ttu-id="4282f-123">ServerEndpoint의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4282f-123">Name of the ServerEndpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ServerEndpointName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4282f-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4282f-124">-PassThru</span></span>
<span data-ttu-id="4282f-125">정상적인 실행에서 이 cmdlet은 성공 시 값을 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4282f-125">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="4282f-126">PassThru 매개 변수를 제공하는 경우 cmdlet은 실행에 성공한 후 파이프라인에 값을 쓴다.</span><span class="sxs-lookup"><span data-stu-id="4282f-126">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="4282f-127">-Pattern</span><span class="sxs-lookup"><span data-stu-id="4282f-127">-Pattern</span></span>
<span data-ttu-id="4282f-128">파일 이름 패턴</span><span class="sxs-lookup"><span data-stu-id="4282f-128">Pattern of the file name</span></span>

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

### <span data-ttu-id="4282f-129">-RecallPath</span><span class="sxs-lookup"><span data-stu-id="4282f-129">-RecallPath</span></span>
<span data-ttu-id="4282f-130">회수해야 하는 회수 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="4282f-130">Recall path which need to be recalled.</span></span>

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

### <span data-ttu-id="4282f-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4282f-131">-ResourceGroupName</span></span>
<span data-ttu-id="4282f-132">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4282f-132">Resource Group Name.</span></span>

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

### <span data-ttu-id="4282f-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4282f-133">-ResourceId</span></span>
<span data-ttu-id="4282f-134">ServerEndpoint 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="4282f-134">ServerEndpoint Resource Id</span></span>

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

### <span data-ttu-id="4282f-135">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="4282f-135">-StorageSyncServiceName</span></span>
<span data-ttu-id="4282f-136">StorageSyncService의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4282f-136">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ParentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4282f-137">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="4282f-137">-SyncGroupName</span></span>
<span data-ttu-id="4282f-138">SyncGroup의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4282f-138">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4282f-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4282f-139">-Confirm</span></span>
<span data-ttu-id="4282f-140">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4282f-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4282f-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4282f-141">-WhatIf</span></span>
<span data-ttu-id="4282f-142">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="4282f-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4282f-143">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4282f-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4282f-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4282f-144">CommonParameters</span></span>
<span data-ttu-id="4282f-145">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4282f-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4282f-146">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="4282f-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4282f-147">입력</span><span class="sxs-lookup"><span data-stu-id="4282f-147">INPUTS</span></span>

### <span data-ttu-id="4282f-148">System.String</span><span class="sxs-lookup"><span data-stu-id="4282f-148">System.String</span></span>

### <span data-ttu-id="4282f-149">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="4282f-149">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="4282f-150">출력</span><span class="sxs-lookup"><span data-stu-id="4282f-150">OUTPUTS</span></span>

### <span data-ttu-id="4282f-151">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4282f-151">System.Boolean</span></span>

## <span data-ttu-id="4282f-152">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4282f-152">NOTES</span></span>

## <span data-ttu-id="4282f-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4282f-153">RELATED LINKS</span></span>
