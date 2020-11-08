---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/invoke-Azstoragesyncfilerecall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncFileRecall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncFileRecall.md
ms.openlocfilehash: fb053da61aabd9328f4ff3d848243ff9b84d6d09
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94043130"
---
# <span data-ttu-id="1744b-101">Invoke-AzStorageSyncFileRecall</span><span class="sxs-lookup"><span data-stu-id="1744b-101">Invoke-AzStorageSyncFileRecall</span></span>

## <span data-ttu-id="1744b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1744b-102">SYNOPSIS</span></span>
<span data-ttu-id="1744b-103">이 명령은 모든 계층화 파일을 다시 로컬 디스크로 회수 합니다.</span><span class="sxs-lookup"><span data-stu-id="1744b-103">This command recalls all tiered files back to local disk.</span></span>

## <span data-ttu-id="1744b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1744b-104">SYNTAX</span></span>

### <span data-ttu-id="1744b-105">StringParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="1744b-105">StringParameterSet (Default)</span></span>
```
Invoke-AzStorageSyncFileRecall [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name] <String> [-Pattern <String>] [-RecallPath <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1744b-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1744b-106">ResourceIdParameterSet</span></span>
```
Invoke-AzStorageSyncFileRecall [-ResourceId] <String> [-Pattern <String>] [-RecallPath <String>] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1744b-107">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1744b-107">ObjectParameterSet</span></span>
```
Invoke-AzStorageSyncFileRecall [-InputObject] <PSServerEndpoint> [-Pattern <String>] [-RecallPath <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1744b-108">설명은</span><span class="sxs-lookup"><span data-stu-id="1744b-108">DESCRIPTION</span></span>
<span data-ttu-id="1744b-109">서버 끝점 (등록 된 서버의 특정 위치)에서 클라우드 계층화를 사용 하는 경우이 명령을 사용 하 여 모든 다층 구성 파일을 로컬 디스크에 회수할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1744b-109">When cloud tiering is enabled on a server endpoint (a specific location on a registered server) then this command can be used to recall all tiered files to local disk.</span></span> <span data-ttu-id="1744b-110">회수를 시작 하기 전에이 서버 끝점에서 클라우드 tiering을 사용 하지 않도록 설정 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="1744b-110">It is highly recommended to disable cloud tiering on this server endpoint before starting recall.</span></span> <span data-ttu-id="1744b-111">Tiering이 켜져 있는 경우 회수는 다른 파일이 계층을 가져와 로컬 디스크에 있는 모든 콘텐츠의 원하는 목표를 달성 하지 못할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1744b-111">If tiering is still on, recall might lead to other files getting tiered which misses to achieve the desired goal of all content residing on local disk.</span></span>

## <span data-ttu-id="1744b-112">예제의</span><span class="sxs-lookup"><span data-stu-id="1744b-112">EXAMPLES</span></span>

### <span data-ttu-id="1744b-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="1744b-113">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncFileRecall -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -ServerEndpointName "myServerEndpointName"
```

<span data-ttu-id="1744b-114">이 명령은 지정 된 서버 끝점의 루트 경로 아래에 있는 모든 계층 파일을 재귀적으로 회수 합니다.</span><span class="sxs-lookup"><span data-stu-id="1744b-114">This command recursively recalls all tiered files located under the root path of the specified server endpoint.</span></span>

## <span data-ttu-id="1744b-115">변수</span><span class="sxs-lookup"><span data-stu-id="1744b-115">PARAMETERS</span></span>

### <span data-ttu-id="1744b-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1744b-116">-AsJob</span></span>
<span data-ttu-id="1744b-117">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="1744b-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1744b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1744b-118">-DefaultProfile</span></span>
<span data-ttu-id="1744b-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1744b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1744b-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1744b-120">-InputObject</span></span>
<span data-ttu-id="1744b-121">일반적으로 매개 변수를 통해 전달 되는 SyncGroup 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="1744b-121">SyncGroup Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="1744b-122">-이름</span><span class="sxs-lookup"><span data-stu-id="1744b-122">-Name</span></span>
<span data-ttu-id="1744b-123">ServerEndpoint의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1744b-123">Name of the ServerEndpoint.</span></span>

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

### <span data-ttu-id="1744b-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1744b-124">-PassThru</span></span>
<span data-ttu-id="1744b-125">일반 실행에서이 cmdlet은 성공에 대 한 값을 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1744b-125">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="1744b-126">PassThru 매개 변수를 제공 하는 경우 cmdlet은 성공적으로 실행 된 후 파이프라인에 값을 기록 합니다.</span><span class="sxs-lookup"><span data-stu-id="1744b-126">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="1744b-127">-패턴</span><span class="sxs-lookup"><span data-stu-id="1744b-127">-Pattern</span></span>
<span data-ttu-id="1744b-128">파일 이름 패턴</span><span class="sxs-lookup"><span data-stu-id="1744b-128">Pattern of the file name</span></span>

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

### <span data-ttu-id="1744b-129">-없음 Allpath</span><span class="sxs-lookup"><span data-stu-id="1744b-129">-RecallPath</span></span>
<span data-ttu-id="1744b-130">리콜 경로가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="1744b-130">Recall path which need to be recalled.</span></span>

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

### <span data-ttu-id="1744b-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1744b-131">-ResourceGroupName</span></span>
<span data-ttu-id="1744b-132">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1744b-132">Resource Group Name.</span></span>

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

### <span data-ttu-id="1744b-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1744b-133">-ResourceId</span></span>
<span data-ttu-id="1744b-134">ServerEndpoint 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="1744b-134">ServerEndpoint Resource Id</span></span>

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

### <span data-ttu-id="1744b-135">-Storages<c13> Cservicename</span><span class="sxs-lookup"><span data-stu-id="1744b-135">-StorageSyncServiceName</span></span>
<span data-ttu-id="1744b-136">Storages<c13> Cservice의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1744b-136">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="1744b-137">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="1744b-137">-SyncGroupName</span></span>
<span data-ttu-id="1744b-138">SyncGroup의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1744b-138">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="1744b-139">-확인</span><span class="sxs-lookup"><span data-stu-id="1744b-139">-Confirm</span></span>
<span data-ttu-id="1744b-140">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1744b-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1744b-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1744b-141">-WhatIf</span></span>
<span data-ttu-id="1744b-142">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1744b-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1744b-143">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1744b-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1744b-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1744b-144">CommonParameters</span></span>
<span data-ttu-id="1744b-145">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1744b-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1744b-146">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1744b-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1744b-147">입력</span><span class="sxs-lookup"><span data-stu-id="1744b-147">INPUTS</span></span>

### <span data-ttu-id="1744b-148">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="1744b-148">System.String</span></span>

### <span data-ttu-id="1744b-149">StorageSync. a m a. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="1744b-149">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="1744b-150">출력</span><span class="sxs-lookup"><span data-stu-id="1744b-150">OUTPUTS</span></span>

### <span data-ttu-id="1744b-151">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="1744b-151">System.Boolean</span></span>

## <span data-ttu-id="1744b-152">상속자</span><span class="sxs-lookup"><span data-stu-id="1744b-152">NOTES</span></span>

## <span data-ttu-id="1744b-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1744b-153">RELATED LINKS</span></span>
