---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/unregister-Azstoragesyncserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Unregister-AzStorageSyncServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Unregister-AzStorageSyncServer.md
ms.openlocfilehash: f6de2bf731bc11a4b0ec8b6c894e6d77569ec9ce
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183065"
---
# <span data-ttu-id="33d15-101">Unregister-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="33d15-101">Unregister-AzStorageSyncServer</span></span>

## <span data-ttu-id="33d15-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="33d15-102">SYNOPSIS</span></span>
<span data-ttu-id="33d15-103">경고: 서버를 등록하지 않은 경우 이 서버의 모든 서버 엔드포인트가 모두 삭제됩니다.</span><span class="sxs-lookup"><span data-stu-id="33d15-103">Warning: Unregistering a server will result in cascading deletes of all server endpoints on this server.</span></span> <span data-ttu-id="33d15-104">이 명령은 저장소 동기화 서비스에서 서버를 등록을 등록하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="33d15-104">This command will unregister a server from it's storage sync service.</span></span>

## <span data-ttu-id="33d15-105">구문</span><span class="sxs-lookup"><span data-stu-id="33d15-105">SYNTAX</span></span>

### <span data-ttu-id="33d15-106">StringParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="33d15-106">StringParameterSet (Default)</span></span>
```
Unregister-AzStorageSyncServer [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-ServerId] <Guid> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33d15-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="33d15-107">InputObjectParameterSet</span></span>
```
Unregister-AzStorageSyncServer [-InputObject] <PSRegisteredServer> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33d15-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="33d15-108">ResourceIdParameterSet</span></span>
```
Unregister-AzStorageSyncServer [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="33d15-109">설명</span><span class="sxs-lookup"><span data-stu-id="33d15-109">DESCRIPTION</span></span>
<span data-ttu-id="33d15-110">이 명령은 저장소 동기화 서비스에서 서버를 등록을 등록하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="33d15-110">This command will unregister a server from the storage sync service.</span></span> <span data-ttu-id="33d15-111">경고: 서버를 등록하지 않은 경우 이 서버의 모든 서버 엔드포인트가 모두 삭제됩니다.</span><span class="sxs-lookup"><span data-stu-id="33d15-111">Warning: Unregistering a server will result in cascading deletes of all server endpoints on this server.</span></span> <span data-ttu-id="33d15-112">이 서버의 경로가 더 이상 동기화되지 않았다고 확실한 경우 호출해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="33d15-112">It should only be called when you are certain that no path on this server is to be synced anymore.</span></span>

## <span data-ttu-id="33d15-113">예제</span><span class="sxs-lookup"><span data-stu-id="33d15-113">EXAMPLES</span></span>

### <span data-ttu-id="33d15-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="33d15-114">Example 1</span></span>
```powershell
PS C:\> $RegisteredServer = Get-AzStorageSyncServer -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
PS C:\> Unregister-AzStorageSyncServer -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -ServerId $RegisteredServer.ServerId
```

<span data-ttu-id="33d15-115">이 명령은 서버의 등록을 등록을 등록하지 않습니다. 그러면 이 서버의 모든 서버 엔드포인트가 모두 삭제됩니다.</span><span class="sxs-lookup"><span data-stu-id="33d15-115">This command will unregister the server, causing cascading deletes of all server endpoints on this server.</span></span>

## <span data-ttu-id="33d15-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="33d15-116">PARAMETERS</span></span>

### <span data-ttu-id="33d15-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="33d15-117">-AsJob</span></span>
<span data-ttu-id="33d15-118">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="33d15-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="33d15-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33d15-119">-DefaultProfile</span></span>
<span data-ttu-id="33d15-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="33d15-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="33d15-121">-Force</span><span class="sxs-lookup"><span data-stu-id="33d15-121">-Force</span></span>
<span data-ttu-id="33d15-122">이 명령의 확인을 건너뛰기 위해 -Force를 공급합니다.</span><span class="sxs-lookup"><span data-stu-id="33d15-122">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="33d15-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="33d15-123">-InputObject</span></span>
<span data-ttu-id="33d15-124">RegisteredServer 입력 개체입니다. 일반적으로 파이프라인을 통해 전달됩니다.</span><span class="sxs-lookup"><span data-stu-id="33d15-124">RegisteredServer Input Object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="33d15-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="33d15-125">-PassThru</span></span>
<span data-ttu-id="33d15-126">정상적인 실행에서 이 cmdlet은 성공 시 값을 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="33d15-126">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="33d15-127">PassThru 매개 변수를 제공하는 경우 cmdlet은 실행에 성공한 후 파이프라인에 값을 쓴다.</span><span class="sxs-lookup"><span data-stu-id="33d15-127">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="33d15-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33d15-128">-ResourceGroupName</span></span>
<span data-ttu-id="33d15-129">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="33d15-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="33d15-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="33d15-130">-ResourceId</span></span>
<span data-ttu-id="33d15-131">RegisteredServer 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="33d15-131">RegisteredServer Resource Id</span></span>

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

### <span data-ttu-id="33d15-132">-ServerId</span><span class="sxs-lookup"><span data-stu-id="33d15-132">-ServerId</span></span>
<span data-ttu-id="33d15-133">RegisteredServer의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="33d15-133">Name of the RegisteredServer.</span></span>

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

### <span data-ttu-id="33d15-134">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="33d15-134">-StorageSyncServiceName</span></span>
<span data-ttu-id="33d15-135">StorageSyncService의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="33d15-135">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="33d15-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="33d15-136">-Confirm</span></span>
<span data-ttu-id="33d15-137">cmdlet을 실행하기 전에 확인을 요청합니다.</span><span class="sxs-lookup"><span data-stu-id="33d15-137">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33d15-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33d15-138">-WhatIf</span></span>
<span data-ttu-id="33d15-139">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="33d15-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="33d15-140">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="33d15-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33d15-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33d15-141">CommonParameters</span></span>
<span data-ttu-id="33d15-142">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="33d15-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33d15-143">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="33d15-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33d15-144">입력</span><span class="sxs-lookup"><span data-stu-id="33d15-144">INPUTS</span></span>

### <span data-ttu-id="33d15-145">Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer</span><span class="sxs-lookup"><span data-stu-id="33d15-145">Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer</span></span>

### <span data-ttu-id="33d15-146">System.String</span><span class="sxs-lookup"><span data-stu-id="33d15-146">System.String</span></span>

### <span data-ttu-id="33d15-147">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="33d15-147">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="33d15-148">출력</span><span class="sxs-lookup"><span data-stu-id="33d15-148">OUTPUTS</span></span>

### <span data-ttu-id="33d15-149">System.Object</span><span class="sxs-lookup"><span data-stu-id="33d15-149">System.Object</span></span>
## <span data-ttu-id="33d15-150">참고 사항</span><span class="sxs-lookup"><span data-stu-id="33d15-150">NOTES</span></span>

## <span data-ttu-id="33d15-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="33d15-151">RELATED LINKS</span></span>
