---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/invoke-Azstoragesyncfilerecall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncFileRecall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncFileRecall.md
ms.openlocfilehash: 5463c20274f60c2d6fb6c4807bf2c4d27da76808
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698493"
---
# <span data-ttu-id="a8574-101">Invoke-AzStorageSyncFileRecall</span><span class="sxs-lookup"><span data-stu-id="a8574-101">Invoke-AzStorageSyncFileRecall</span></span>

## <span data-ttu-id="a8574-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a8574-102">SYNOPSIS</span></span>
<span data-ttu-id="a8574-103">이 명령은 모든 계층화 파일을 다시 로컬 디스크로 회수 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8574-103">This command recalls all tiered files back to local disk.</span></span>

## <span data-ttu-id="a8574-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a8574-104">SYNTAX</span></span>

### <span data-ttu-id="a8574-105">ObjectParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="a8574-105">ObjectParameterSet (Default)</span></span>
```
Invoke-AzStorageSyncFileRecall [-InputObject] <PSServerEndpoint> [-Pattern <String>] [-RecallPath <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a8574-106">StringParameterSet</span><span class="sxs-lookup"><span data-stu-id="a8574-106">StringParameterSet</span></span>
```
Invoke-AzStorageSyncFileRecall [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name] <String> [-Pattern <String>] [-RecallPath <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a8574-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a8574-107">ResourceIdParameterSet</span></span>
```
Invoke-AzStorageSyncFileRecall [-ResourceId] <String> [-Pattern <String>] [-RecallPath <String>] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a8574-108">설명은</span><span class="sxs-lookup"><span data-stu-id="a8574-108">DESCRIPTION</span></span>
<span data-ttu-id="a8574-109">서버 끝점 (등록 된 서버의 특정 위치)에서 클라우드 계층화를 사용 하는 경우이 명령을 사용 하 여 모든 다층 구성 파일을 로컬 디스크에 회수할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a8574-109">When cloud tiering is enabled on a server endpoint (a specific location on a registered server) then this command can be used to recall all tiered files to local disk.</span></span> <span data-ttu-id="a8574-110">회수를 시작 하기 전에이 서버 끝점에서 클라우드 tiering을 사용 하지 않도록 설정 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="a8574-110">It is highly recommended to disable cloud tiering on this server endpoint before starting recall.</span></span> <span data-ttu-id="a8574-111">Tiering이 켜져 있는 경우 회수는 다른 파일이 계층을 가져와 로컬 디스크에 있는 모든 콘텐츠의 원하는 목표를 달성 하지 못할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a8574-111">If tiering is still on, recall might lead to other files getting tiered which misses to achieve the desired goal of all content residing on local disk.</span></span>

## <span data-ttu-id="a8574-112">예제의</span><span class="sxs-lookup"><span data-stu-id="a8574-112">EXAMPLES</span></span>

### <span data-ttu-id="a8574-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="a8574-113">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncFileRecall -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -ServerEndpointName "myServerEndpointName"
```

<span data-ttu-id="a8574-114">이 명령은 지정 된 서버 끝점의 루트 경로 아래에 있는 모든 계층 파일을 재귀적으로 회수 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8574-114">This command recursively recalls all tiered files located under the root path of the specified server endpoint.</span></span>

## <span data-ttu-id="a8574-115">변수</span><span class="sxs-lookup"><span data-stu-id="a8574-115">PARAMETERS</span></span>

### <span data-ttu-id="a8574-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a8574-116">-AsJob</span></span>
<span data-ttu-id="a8574-117">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="a8574-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a8574-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8574-118">-DefaultProfile</span></span>
<span data-ttu-id="a8574-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a8574-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a8574-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a8574-120">-InputObject</span></span>
<span data-ttu-id="a8574-121">일반적으로 매개 변수를 통해 전달 되는 SyncGroup 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="a8574-121">SyncGroup Object, normally passed through the parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint
Parameter Sets: ObjectParameterSet
Aliases: RegisteredServer

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a8574-122">-이름</span><span class="sxs-lookup"><span data-stu-id="a8574-122">-Name</span></span>
<span data-ttu-id="a8574-123">ServerEndpoint의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a8574-123">Name of the ServerEndpoint.</span></span>

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

### <span data-ttu-id="a8574-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a8574-124">-PassThru</span></span>
<span data-ttu-id="a8574-125">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="a8574-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="a8574-126">-패턴</span><span class="sxs-lookup"><span data-stu-id="a8574-126">-Pattern</span></span>
<span data-ttu-id="a8574-127">파일 이름 패턴</span><span class="sxs-lookup"><span data-stu-id="a8574-127">Pattern of the file name</span></span>

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

### <span data-ttu-id="a8574-128">-없음 Allpath</span><span class="sxs-lookup"><span data-stu-id="a8574-128">-RecallPath</span></span>
<span data-ttu-id="a8574-129">리콜 경로가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8574-129">Recall path which need to be recalled.</span></span>

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

### <span data-ttu-id="a8574-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8574-130">-ResourceGroupName</span></span>
<span data-ttu-id="a8574-131">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a8574-131">Resource Group Name.</span></span>

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

### <span data-ttu-id="a8574-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a8574-132">-ResourceId</span></span>
<span data-ttu-id="a8574-133">ServerEndpoint 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="a8574-133">ServerEndpoint Resource Id</span></span>

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

### <span data-ttu-id="a8574-134">-Storages Cservicename</span><span class="sxs-lookup"><span data-stu-id="a8574-134">-StorageSyncServiceName</span></span>
<span data-ttu-id="a8574-135">Storages Cservice의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a8574-135">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="a8574-136">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="a8574-136">-SyncGroupName</span></span>
<span data-ttu-id="a8574-137">SyncGroup의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a8574-137">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="a8574-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8574-138">CommonParameters</span></span>
<span data-ttu-id="a8574-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8574-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8574-140">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8574-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8574-141">입력</span><span class="sxs-lookup"><span data-stu-id="a8574-141">INPUTS</span></span>

### <span data-ttu-id="a8574-142">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a8574-142">System.String</span></span>

### <span data-ttu-id="a8574-143">StorageSync. a m a. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="a8574-143">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="a8574-144">출력</span><span class="sxs-lookup"><span data-stu-id="a8574-144">OUTPUTS</span></span>

### <span data-ttu-id="a8574-145">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="a8574-145">System.Boolean</span></span>

## <span data-ttu-id="a8574-146">상속자</span><span class="sxs-lookup"><span data-stu-id="a8574-146">NOTES</span></span>

## <span data-ttu-id="a8574-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a8574-147">RELATED LINKS</span></span>
