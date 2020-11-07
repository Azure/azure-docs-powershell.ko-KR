---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/unregister-Azstoragesyncserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Unregister-AzStorageSyncServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Unregister-AzStorageSyncServer.md
ms.openlocfilehash: 3752e520c3637ffa1e08bfd89d03c6caeebd4e18
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93871994"
---
# <span data-ttu-id="d3b05-101">Unregister-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="d3b05-101">Unregister-AzStorageSyncServer</span></span>

## <span data-ttu-id="d3b05-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3b05-102">SYNOPSIS</span></span>
<span data-ttu-id="d3b05-103">경고: 서버의 등록을 취소 하면이 서버의 모든 서버 끝점에 대 한 연계 삭제가 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d3b05-103">Warning: Unregistering a server will result in cascading deletes of all server endpoints on this server.</span></span> <span data-ttu-id="d3b05-104">이 명령은 저장소 동기화 서비스에서 서버의 등록을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3b05-104">This command will unregister a server from it's storage sync service.</span></span>

## <span data-ttu-id="d3b05-105">구문과</span><span class="sxs-lookup"><span data-stu-id="d3b05-105">SYNTAX</span></span>

### <span data-ttu-id="d3b05-106">StringParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="d3b05-106">StringParameterSet (Default)</span></span>
```
Unregister-AzStorageSyncServer [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-ServerId] <Guid> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3b05-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d3b05-107">InputObjectParameterSet</span></span>
```
Unregister-AzStorageSyncServer [-InputObject] <PSRegisteredServer> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3b05-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d3b05-108">ResourceIdParameterSet</span></span>
```
Unregister-AzStorageSyncServer [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3b05-109">설명은</span><span class="sxs-lookup"><span data-stu-id="d3b05-109">DESCRIPTION</span></span>
<span data-ttu-id="d3b05-110">이 명령은 저장소 동기화 서비스에서 서버 등록을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3b05-110">This command will unregister a server from the storage sync service.</span></span> <span data-ttu-id="d3b05-111">경고: 서버의 등록을 취소 하면이 서버의 모든 서버 끝점에 대 한 연계 삭제가 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d3b05-111">Warning: Unregistering a server will result in cascading deletes of all server endpoints on this server.</span></span> <span data-ttu-id="d3b05-112">이 서버의 경로가 더 이상 동기화 되지 않는 것이 확실 한 경우에만 호출 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3b05-112">It should only be called when you are certain that no path on this server is to be synced anymore.</span></span>

## <span data-ttu-id="d3b05-113">예제의</span><span class="sxs-lookup"><span data-stu-id="d3b05-113">EXAMPLES</span></span>

### <span data-ttu-id="d3b05-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="d3b05-114">Example 1</span></span>
```powershell
PS C:\> $RegisteredServer = Get-AzStorageSyncServer -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
PS C:\> Unregister-AzStorageSyncServer -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -ServerId $RegisteredServer.ServerId
```

<span data-ttu-id="d3b05-115">이 명령은 서버를 등록 취소 하 고이 서버의 모든 서버 끝점에 대해 단계적으로 삭제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d3b05-115">This command will unregister the server, causing cascading deletes of all server endpoints on this server.</span></span>

## <span data-ttu-id="d3b05-116">변수</span><span class="sxs-lookup"><span data-stu-id="d3b05-116">PARAMETERS</span></span>

### <span data-ttu-id="d3b05-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d3b05-117">-AsJob</span></span>
<span data-ttu-id="d3b05-118">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="d3b05-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d3b05-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3b05-119">-DefaultProfile</span></span>
<span data-ttu-id="d3b05-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d3b05-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3b05-121">-Force</span><span class="sxs-lookup"><span data-stu-id="d3b05-121">-Force</span></span>
<span data-ttu-id="d3b05-122">이 명령에 대 한 확인을 건너뛰기 위해-Force를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3b05-122">Supply -Force to skip confirmation of this command.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3b05-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d3b05-123">-InputObject</span></span>
<span data-ttu-id="d3b05-124">일반적으로 파이프라인을 통해 전달 되는 RegisteredServer Input 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="d3b05-124">RegisteredServer Input Object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d3b05-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d3b05-125">-PassThru</span></span>
<span data-ttu-id="d3b05-126">일반 실행에서이 cmdlet은 성공에 대 한 값을 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d3b05-126">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="d3b05-127">PassThru 매개 변수를 제공 하는 경우 cmdlet은 성공적으로 실행 된 후 파이프라인에 값을 기록 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3b05-127">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="d3b05-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3b05-128">-ResourceGroupName</span></span>
<span data-ttu-id="d3b05-129">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d3b05-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="d3b05-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d3b05-130">-ResourceId</span></span>
<span data-ttu-id="d3b05-131">RegisteredServer 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="d3b05-131">RegisteredServer Resource Id</span></span>

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

### <span data-ttu-id="d3b05-132">-ServerId</span><span class="sxs-lookup"><span data-stu-id="d3b05-132">-ServerId</span></span>
<span data-ttu-id="d3b05-133">RegisteredServer의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d3b05-133">Name of the RegisteredServer.</span></span>

```yaml
Type: System.Guid
Parameter Sets: StringParameterSet
Aliases: RegisteredServerName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3b05-134">-Storages<c13> Cservicename</span><span class="sxs-lookup"><span data-stu-id="d3b05-134">-StorageSyncServiceName</span></span>
<span data-ttu-id="d3b05-135">Storages<c13> Cservice의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d3b05-135">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="d3b05-136">-확인</span><span class="sxs-lookup"><span data-stu-id="d3b05-136">-Confirm</span></span>
<span data-ttu-id="d3b05-137">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3b05-137">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3b05-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3b05-138">-WhatIf</span></span>
<span data-ttu-id="d3b05-139">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d3b05-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d3b05-140">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d3b05-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3b05-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3b05-141">CommonParameters</span></span>
<span data-ttu-id="d3b05-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3b05-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3b05-143">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3b05-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3b05-144">입력</span><span class="sxs-lookup"><span data-stu-id="d3b05-144">INPUTS</span></span>

### <span data-ttu-id="d3b05-145">StorageSync. PSRegisteredServer/.</span><span class="sxs-lookup"><span data-stu-id="d3b05-145">Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer</span></span>

### <span data-ttu-id="d3b05-146">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d3b05-146">System.String</span></span>

### <span data-ttu-id="d3b05-147">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="d3b05-147">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d3b05-148">출력</span><span class="sxs-lookup"><span data-stu-id="d3b05-148">OUTPUTS</span></span>

### <span data-ttu-id="d3b05-149">System. 개체</span><span class="sxs-lookup"><span data-stu-id="d3b05-149">System.Object</span></span>
## <span data-ttu-id="d3b05-150">상속자</span><span class="sxs-lookup"><span data-stu-id="d3b05-150">NOTES</span></span>

## <span data-ttu-id="d3b05-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d3b05-151">RELATED LINKS</span></span>
