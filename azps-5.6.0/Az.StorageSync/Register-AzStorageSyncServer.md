---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/powershell/module/Az.storagesync/register-Azstoragesyncserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Register-AzStorageSyncServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Register-AzStorageSyncServer.md
ms.openlocfilehash: 62dcefcf48e1d4c685b2a4f4855af41da7d8db75
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011323"
---
# <span data-ttu-id="4dfa1-101">Register-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="4dfa1-101">Register-AzStorageSyncServer</span></span>

## <span data-ttu-id="4dfa1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4dfa1-102">SYNOPSIS</span></span>
<span data-ttu-id="4dfa1-103">이 명령은 신뢰 관계를 만드는 저장소 동기화 서비스에 서버를 등록합니다.</span><span class="sxs-lookup"><span data-stu-id="4dfa1-103">This command registers a server to a storage sync service which creates a trust relationship.</span></span> <span data-ttu-id="4dfa1-104">그런 다음 PowerShell 또는 Azure Portal을 사용하여 이 서버에서 동기화를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4dfa1-104">PowerShell or the Azure portal can then be used to configure sync on this server.</span></span>

## <span data-ttu-id="4dfa1-105">구문</span><span class="sxs-lookup"><span data-stu-id="4dfa1-105">SYNTAX</span></span>

### <span data-ttu-id="4dfa1-106">StringParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="4dfa1-106">StringParameterSet (Default)</span></span>
```
Register-AzStorageSyncServer [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4dfa1-107">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4dfa1-107">ObjectParameterSet</span></span>
```
Register-AzStorageSyncServer [-ParentObject] <PSStorageSyncService> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4dfa1-108">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="4dfa1-108">ParentStringParameterSet</span></span>
```
Register-AzStorageSyncServer [-ParentResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4dfa1-109">설명</span><span class="sxs-lookup"><span data-stu-id="4dfa1-109">DESCRIPTION</span></span>
<span data-ttu-id="4dfa1-110">이 명령은 Azure 파일 동기화의 최상위 리소스인 저장소 동기화 서비스에 서버를 등록합니다. 보안 데이터 전송 및 관리 채널을 보장하는 서버와 저장소 동기화 서비스 간의 신뢰 관계가 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="4dfa1-110">This command registers a server to a storage sync service, the top-level resource for Azure File Sync. A trust relationship between server and storage sync service is created that ensures secure data transfer and management channels.</span></span> <span data-ttu-id="4dfa1-111">그런 다음 PowerShell 또는 Azure Portal을 사용하여 이 서버에서 동기화되는 것을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4dfa1-111">PowerShell or the Azure portal can then be used to configure what syncs on this server.</span></span> <span data-ttu-id="4dfa1-112">서버는 단일 저장소 동기화 서비스에만 등록할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4dfa1-112">A server can only be registered to a single storage sync service.</span></span> <span data-ttu-id="4dfa1-113">서버가 동일한 파일 집합을 동기화하는 데 참여해야 하는 경우 동일한 저장소 동기화 서비스에 등록합니다.</span><span class="sxs-lookup"><span data-stu-id="4dfa1-113">If servers ever need to participate in syncing the same set of files, register them to the same storage sync service.</span></span>
<span data-ttu-id="4dfa1-114">명령은 직접 실행되거나 원격 PowerShell 세션을 통해 등록할 서버에서 로컬로 실행되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4dfa1-114">The command must be run locally on the server that is to be registered - either executed directly or via a remote PowerShell session.</span></span> <span data-ttu-id="4dfa1-115">원격 컴퓨터 개체를 수락할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="4dfa1-115">A remote computer object cannot be accepted.</span></span>

## <span data-ttu-id="4dfa1-116">예제</span><span class="sxs-lookup"><span data-stu-id="4dfa1-116">EXAMPLES</span></span>

### <span data-ttu-id="4dfa1-117">예제 1</span><span class="sxs-lookup"><span data-stu-id="4dfa1-117">Example 1</span></span>
```powershell
PS C:\> Register-AzStorageSyncServer -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
```

<span data-ttu-id="4dfa1-118">이 명령은 이 명령이 실행되는 로컬 서버를 등록합니다.</span><span class="sxs-lookup"><span data-stu-id="4dfa1-118">This command will register the local server this command is run on.</span></span>

## <span data-ttu-id="4dfa1-119">매개 변수</span><span class="sxs-lookup"><span data-stu-id="4dfa1-119">PARAMETERS</span></span>

### <span data-ttu-id="4dfa1-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4dfa1-120">-AsJob</span></span>
<span data-ttu-id="4dfa1-121">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="4dfa1-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4dfa1-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4dfa1-122">-DefaultProfile</span></span>
<span data-ttu-id="4dfa1-123">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4dfa1-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4dfa1-124">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="4dfa1-124">-ParentObject</span></span>
<span data-ttu-id="4dfa1-125">StorageSyncService 개체는 일반적으로 매개 변수를 통과합니다.</span><span class="sxs-lookup"><span data-stu-id="4dfa1-125">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="4dfa1-126">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="4dfa1-126">-ParentResourceId</span></span>
<span data-ttu-id="4dfa1-127">StorageSyncService 부모 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="4dfa1-127">StorageSyncService Parent Resource Id</span></span>

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

### <span data-ttu-id="4dfa1-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4dfa1-128">-ResourceGroupName</span></span>
<span data-ttu-id="4dfa1-129">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4dfa1-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="4dfa1-130">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="4dfa1-130">-StorageSyncServiceName</span></span>
<span data-ttu-id="4dfa1-131">StorageSyncService의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4dfa1-131">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="4dfa1-132">-확인</span><span class="sxs-lookup"><span data-stu-id="4dfa1-132">-Confirm</span></span>
<span data-ttu-id="4dfa1-133">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4dfa1-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4dfa1-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4dfa1-134">-WhatIf</span></span>
<span data-ttu-id="4dfa1-135">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="4dfa1-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4dfa1-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4dfa1-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4dfa1-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4dfa1-137">CommonParameters</span></span>
<span data-ttu-id="4dfa1-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4dfa1-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4dfa1-139">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="4dfa1-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4dfa1-140">입력</span><span class="sxs-lookup"><span data-stu-id="4dfa1-140">INPUTS</span></span>

### <span data-ttu-id="4dfa1-141">System.String</span><span class="sxs-lookup"><span data-stu-id="4dfa1-141">System.String</span></span>

### <span data-ttu-id="4dfa1-142">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="4dfa1-142">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="4dfa1-143">출력</span><span class="sxs-lookup"><span data-stu-id="4dfa1-143">OUTPUTS</span></span>

### <span data-ttu-id="4dfa1-144">Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer</span><span class="sxs-lookup"><span data-stu-id="4dfa1-144">Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer</span></span>

## <span data-ttu-id="4dfa1-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4dfa1-145">NOTES</span></span>

## <span data-ttu-id="4dfa1-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4dfa1-146">RELATED LINKS</span></span>
