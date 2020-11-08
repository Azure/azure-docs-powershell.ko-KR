---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/register-Azstoragesyncserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Register-AzStorageSyncServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Register-AzStorageSyncServer.md
ms.openlocfilehash: bb1ce6f9ff7e846c2f485665cafad700fa4c825b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94043121"
---
# <span data-ttu-id="c6954-101">Register-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="c6954-101">Register-AzStorageSyncServer</span></span>

## <span data-ttu-id="c6954-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6954-102">SYNOPSIS</span></span>
<span data-ttu-id="c6954-103">이 명령은 신뢰 관계를 만드는 저장소 동기화 서비스에 서버를 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6954-103">This command registers a server to a storage sync service which creates a trust relationship.</span></span> <span data-ttu-id="c6954-104">그러면 PowerShell 또는 Azure 포털을 사용 하 여이 서버에서 동기화를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c6954-104">PowerShell or the Azure portal can then be used to configure sync on this server.</span></span>

## <span data-ttu-id="c6954-105">구문과</span><span class="sxs-lookup"><span data-stu-id="c6954-105">SYNTAX</span></span>

### <span data-ttu-id="c6954-106">StringParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="c6954-106">StringParameterSet (Default)</span></span>
```
Register-AzStorageSyncServer [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6954-107">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c6954-107">ObjectParameterSet</span></span>
```
Register-AzStorageSyncServer [-ParentObject] <PSStorageSyncService> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6954-108">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="c6954-108">ParentStringParameterSet</span></span>
```
Register-AzStorageSyncServer [-ParentResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6954-109">설명은</span><span class="sxs-lookup"><span data-stu-id="c6954-109">DESCRIPTION</span></span>
<span data-ttu-id="c6954-110">이 명령은 Azure 파일 동기화에 대 한 최상위 리소스인 저장소 동기화 서비스에 서버를 등록 합니다. 서버와 저장소 동기화 서비스 간의 신뢰 관계를 만들어 보안 데이터 전송 및 관리 채널을 보장 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6954-110">This command registers a server to a storage sync service, the top-level resource for Azure File Sync. A trust relationship between server and storage sync service is created that ensures secure data transfer and management channels.</span></span> <span data-ttu-id="c6954-111">그러면 PowerShell 또는 Azure 포털을 사용 하 여이 서버에서 동기화 할 항목을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c6954-111">PowerShell or the Azure portal can then be used to configure what syncs on this server.</span></span> <span data-ttu-id="c6954-112">서버는 단일 저장소 동기화 서비스에만 등록할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c6954-112">A server can only be registered to a single storage sync service.</span></span> <span data-ttu-id="c6954-113">동일한 파일 집합을 동기화 하는 데 서버가 참가 해야 하는 경우 동일한 저장소 동기화 서비스에이를 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6954-113">If servers ever need to participate in syncing the same set of files, register them to the same storage sync service.</span></span>
<span data-ttu-id="c6954-114">이 명령은 직접 실행 되거나 원격 PowerShell 세션을 통해 등록 되는 서버에서 로컬로 실행 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6954-114">The command must be run locally on the server that is to be registered - either executed directly or via a remote PowerShell session.</span></span> <span data-ttu-id="c6954-115">원격 컴퓨터 개체를 수락할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="c6954-115">A remote computer object cannot be accepted.</span></span>

## <span data-ttu-id="c6954-116">예제의</span><span class="sxs-lookup"><span data-stu-id="c6954-116">EXAMPLES</span></span>

### <span data-ttu-id="c6954-117">예제 1</span><span class="sxs-lookup"><span data-stu-id="c6954-117">Example 1</span></span>
```powershell
PS C:\> Register-AzStorageSyncServer -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
```

<span data-ttu-id="c6954-118">이 명령은이 명령이 실행 되는 로컬 서버를 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6954-118">This command will register the local server this command is run on.</span></span>

## <span data-ttu-id="c6954-119">변수</span><span class="sxs-lookup"><span data-stu-id="c6954-119">PARAMETERS</span></span>

### <span data-ttu-id="c6954-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c6954-120">-AsJob</span></span>
<span data-ttu-id="c6954-121">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="c6954-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c6954-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6954-122">-DefaultProfile</span></span>
<span data-ttu-id="c6954-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c6954-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6954-124">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="c6954-124">-ParentObject</span></span>
<span data-ttu-id="c6954-125">일반적으로 매개 변수를 통해 전달 되는 Storages Cservice 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="c6954-125">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="c6954-126">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="c6954-126">-ParentResourceId</span></span>
<span data-ttu-id="c6954-127">Storages Cservice 부모 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="c6954-127">StorageSyncService Parent Resource Id</span></span>

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

### <span data-ttu-id="c6954-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6954-128">-ResourceGroupName</span></span>
<span data-ttu-id="c6954-129">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c6954-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="c6954-130">-Storages Cservicename</span><span class="sxs-lookup"><span data-stu-id="c6954-130">-StorageSyncServiceName</span></span>
<span data-ttu-id="c6954-131">Storages Cservice의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c6954-131">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="c6954-132">-확인</span><span class="sxs-lookup"><span data-stu-id="c6954-132">-Confirm</span></span>
<span data-ttu-id="c6954-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6954-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6954-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6954-134">-WhatIf</span></span>
<span data-ttu-id="c6954-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c6954-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c6954-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c6954-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6954-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6954-137">CommonParameters</span></span>
<span data-ttu-id="c6954-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6954-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6954-139">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6954-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6954-140">입력</span><span class="sxs-lookup"><span data-stu-id="c6954-140">INPUTS</span></span>

### <span data-ttu-id="c6954-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c6954-141">System.String</span></span>

### <span data-ttu-id="c6954-142">StorageSync. Psstorages<c13> Cservice</span><span class="sxs-lookup"><span data-stu-id="c6954-142">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="c6954-143">출력</span><span class="sxs-lookup"><span data-stu-id="c6954-143">OUTPUTS</span></span>

### <span data-ttu-id="c6954-144">StorageSync. PSRegisteredServer/.</span><span class="sxs-lookup"><span data-stu-id="c6954-144">Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer</span></span>

## <span data-ttu-id="c6954-145">상속자</span><span class="sxs-lookup"><span data-stu-id="c6954-145">NOTES</span></span>

## <span data-ttu-id="c6954-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c6954-146">RELATED LINKS</span></span>
