---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/register-Azstoragesyncserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Register-AzStorageSyncServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Register-AzStorageSyncServer.md
ms.openlocfilehash: bb1ce6f9ff7e846c2f485665cafad700fa4c825b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98366605"
---
# <span data-ttu-id="5bc09-101">Register-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="5bc09-101">Register-AzStorageSyncServer</span></span>

## <span data-ttu-id="5bc09-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5bc09-102">SYNOPSIS</span></span>
<span data-ttu-id="5bc09-103">이 명령은 신뢰 관계를 만드는 저장소 동기화 서비스에 서버를 등록합니다.</span><span class="sxs-lookup"><span data-stu-id="5bc09-103">This command registers a server to a storage sync service which creates a trust relationship.</span></span> <span data-ttu-id="5bc09-104">그런 다음 PowerShell 또는 Azure Portal을 사용하여 이 서버에서 동기화를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5bc09-104">PowerShell or the Azure portal can then be used to configure sync on this server.</span></span>

## <span data-ttu-id="5bc09-105">구문</span><span class="sxs-lookup"><span data-stu-id="5bc09-105">SYNTAX</span></span>

### <span data-ttu-id="5bc09-106">StringParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="5bc09-106">StringParameterSet (Default)</span></span>
```
Register-AzStorageSyncServer [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5bc09-107">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5bc09-107">ObjectParameterSet</span></span>
```
Register-AzStorageSyncServer [-ParentObject] <PSStorageSyncService> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5bc09-108">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="5bc09-108">ParentStringParameterSet</span></span>
```
Register-AzStorageSyncServer [-ParentResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5bc09-109">설명</span><span class="sxs-lookup"><span data-stu-id="5bc09-109">DESCRIPTION</span></span>
<span data-ttu-id="5bc09-110">이 명령은 Azure 파일 동기화에 대한 최상위 리소스인 저장소 동기화 서비스에 서버를 등록합니다. 보안 데이터 전송 및 관리 채널을 보장하는 서버와 저장소 동기화 서비스 간의 트러스트 관계가 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="5bc09-110">This command registers a server to a storage sync service, the top-level resource for Azure File Sync. A trust relationship between server and storage sync service is created that ensures secure data transfer and management channels.</span></span> <span data-ttu-id="5bc09-111">그런 다음 PowerShell 또는 Azure Portal을 사용하여 이 서버에서 동기화되는 것을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5bc09-111">PowerShell or the Azure portal can then be used to configure what syncs on this server.</span></span> <span data-ttu-id="5bc09-112">서버는 단일 저장소 동기화 서비스에만 등록할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5bc09-112">A server can only be registered to a single storage sync service.</span></span> <span data-ttu-id="5bc09-113">서버가 동일한 파일 집합 동기화에 참여해야 하는 경우 동일한 저장소 동기화 서비스에 등록합니다.</span><span class="sxs-lookup"><span data-stu-id="5bc09-113">If servers ever need to participate in syncing the same set of files, register them to the same storage sync service.</span></span>
<span data-ttu-id="5bc09-114">명령은 직접 실행되거나 원격 PowerShell 세션을 통해 등록할 서버에서 로컬로 실행되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5bc09-114">The command must be run locally on the server that is to be registered - either executed directly or via a remote PowerShell session.</span></span> <span data-ttu-id="5bc09-115">원격 컴퓨터 개체를 수락할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="5bc09-115">A remote computer object cannot be accepted.</span></span>

## <span data-ttu-id="5bc09-116">예제</span><span class="sxs-lookup"><span data-stu-id="5bc09-116">EXAMPLES</span></span>

### <span data-ttu-id="5bc09-117">예제 1</span><span class="sxs-lookup"><span data-stu-id="5bc09-117">Example 1</span></span>
```powershell
PS C:\> Register-AzStorageSyncServer -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
```

<span data-ttu-id="5bc09-118">이 명령은 이 명령이 실행되는 로컬 서버를 등록합니다.</span><span class="sxs-lookup"><span data-stu-id="5bc09-118">This command will register the local server this command is run on.</span></span>

## <span data-ttu-id="5bc09-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5bc09-119">PARAMETERS</span></span>

### <span data-ttu-id="5bc09-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5bc09-120">-AsJob</span></span>
<span data-ttu-id="5bc09-121">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="5bc09-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5bc09-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bc09-122">-DefaultProfile</span></span>
<span data-ttu-id="5bc09-123">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5bc09-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5bc09-124">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="5bc09-124">-ParentObject</span></span>
<span data-ttu-id="5bc09-125">StorageSyncService 개체입니다. 일반적으로 매개 변수를 통해 전달됩니다.</span><span class="sxs-lookup"><span data-stu-id="5bc09-125">StorageSyncService Object, normally passed through the parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService
Parameter Sets: ObjectParameterSet
Aliases: StorageSyncService

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5bc09-126">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="5bc09-126">-ParentResourceId</span></span>
<span data-ttu-id="5bc09-127">StorageSyncService 부모 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="5bc09-127">StorageSyncService Parent Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ParentStringParameterSet
Aliases: StorageSyncServiceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5bc09-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5bc09-128">-ResourceGroupName</span></span>
<span data-ttu-id="5bc09-129">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5bc09-129">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5bc09-130">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="5bc09-130">-StorageSyncServiceName</span></span>
<span data-ttu-id="5bc09-131">StorageSyncService의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5bc09-131">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ParentName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5bc09-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5bc09-132">-Confirm</span></span>
<span data-ttu-id="5bc09-133">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5bc09-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5bc09-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5bc09-134">-WhatIf</span></span>
<span data-ttu-id="5bc09-135">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="5bc09-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5bc09-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5bc09-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5bc09-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bc09-137">CommonParameters</span></span>
<span data-ttu-id="5bc09-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5bc09-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bc09-139">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5bc09-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bc09-140">입력</span><span class="sxs-lookup"><span data-stu-id="5bc09-140">INPUTS</span></span>

### <span data-ttu-id="5bc09-141">System.String</span><span class="sxs-lookup"><span data-stu-id="5bc09-141">System.String</span></span>

### <span data-ttu-id="5bc09-142">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="5bc09-142">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="5bc09-143">출력</span><span class="sxs-lookup"><span data-stu-id="5bc09-143">OUTPUTS</span></span>

### <span data-ttu-id="5bc09-144">Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer</span><span class="sxs-lookup"><span data-stu-id="5bc09-144">Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer</span></span>

## <span data-ttu-id="5bc09-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5bc09-145">NOTES</span></span>

## <span data-ttu-id="5bc09-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5bc09-146">RELATED LINKS</span></span>