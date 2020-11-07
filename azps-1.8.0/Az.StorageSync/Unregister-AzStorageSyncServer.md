---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/unregister-Azstoragesyncserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Unregister-AzStorageSyncServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Unregister-AzStorageSyncServer.md
ms.openlocfilehash: 87734d63d28785282ad3285ef8cce0a574ba30e3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698468"
---
# <span data-ttu-id="84e07-101">Unregister-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="84e07-101">Unregister-AzStorageSyncServer</span></span>

## <span data-ttu-id="84e07-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="84e07-102">SYNOPSIS</span></span>
<span data-ttu-id="84e07-103">경고: 서버의 등록을 취소 하면이 서버의 모든 서버 끝점에 대 한 연계 삭제가 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="84e07-103">Warning: Unregistering a server will result in cascading deletes of all server endpoints on this server.</span></span> <span data-ttu-id="84e07-104">이 명령은 저장소 동기화 서비스인 서버의 등록을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="84e07-104">This command will unregister a server it's the storage sync service.</span></span>

## <span data-ttu-id="84e07-105">구문과</span><span class="sxs-lookup"><span data-stu-id="84e07-105">SYNTAX</span></span>

### <span data-ttu-id="84e07-106">InputObjectParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="84e07-106">InputObjectParameterSet (Default)</span></span>
```
Unregister-AzStorageSyncServer [-InputObject] <PSRegisteredServer> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84e07-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="84e07-107">ResourceIdParameterSet</span></span>
```
Unregister-AzStorageSyncServer [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84e07-108">StringParameterSet</span><span class="sxs-lookup"><span data-stu-id="84e07-108">StringParameterSet</span></span>
```
Unregister-AzStorageSyncServer [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-ServerId] <Guid> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84e07-109">설명은</span><span class="sxs-lookup"><span data-stu-id="84e07-109">DESCRIPTION</span></span>
<span data-ttu-id="84e07-110">이 명령은 저장소 동기화 서비스에서 서버 등록을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="84e07-110">This command will unregister a server from the storage sync service.</span></span> <span data-ttu-id="84e07-111">경고: 서버의 등록을 취소 하면이 서버의 모든 서버 끝점에 대 한 연계 삭제가 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="84e07-111">Warning: Unregistering a server will result in cascading deletes of all server endpoints on this server.</span></span> <span data-ttu-id="84e07-112">이 서버의 경로가 더 이상 동기화 되지 않는 것이 확실 한 경우에만 호출 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="84e07-112">It should only be called when you are certain that no path on this server is to be synced anymore.</span></span>

## <span data-ttu-id="84e07-113">예제의</span><span class="sxs-lookup"><span data-stu-id="84e07-113">EXAMPLES</span></span>

### <span data-ttu-id="84e07-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="84e07-114">Example 1</span></span>
```powershell
PS C:\> $RegisteredServer = Get-AzStorageSyncServer -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
PS C:\> Unregister-AzStorageSyncServer -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -ServerId $RegisteredServer.ServerId
```

<span data-ttu-id="84e07-115">이 명령은 서버를 등록 취소 하 고이 서버의 모든 서버 끝점에 대해 단계적으로 삭제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="84e07-115">This command will unregister the server, causing cascading deletes of all server endpoints on this server.</span></span>

## <span data-ttu-id="84e07-116">변수</span><span class="sxs-lookup"><span data-stu-id="84e07-116">PARAMETERS</span></span>

### <span data-ttu-id="84e07-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="84e07-117">-AsJob</span></span>
<span data-ttu-id="84e07-118">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="84e07-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="84e07-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84e07-119">-DefaultProfile</span></span>
<span data-ttu-id="84e07-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="84e07-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84e07-121">-Force</span><span class="sxs-lookup"><span data-stu-id="84e07-121">-Force</span></span>
<span data-ttu-id="84e07-122">이 명령에 대 한 확인을 건너뛰기 위해-Force를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="84e07-122">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="84e07-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="84e07-123">-InputObject</span></span>
<span data-ttu-id="84e07-124">일반적으로 파이프라인을 통해 전달 되는 RegisteredServer Input 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="84e07-124">RegisteredServer Input Object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="84e07-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="84e07-125">-PassThru</span></span>
<span data-ttu-id="84e07-126">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="84e07-126">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="84e07-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84e07-127">-ResourceGroupName</span></span>
<span data-ttu-id="84e07-128">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="84e07-128">Resource Group Name.</span></span>

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

### <span data-ttu-id="84e07-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="84e07-129">-ResourceId</span></span>
<span data-ttu-id="84e07-130">RegisteredServer 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="84e07-130">RegisteredServer Resource Id</span></span>

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

### <span data-ttu-id="84e07-131">-ServerId</span><span class="sxs-lookup"><span data-stu-id="84e07-131">-ServerId</span></span>
<span data-ttu-id="84e07-132">RegisteredServer의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="84e07-132">Name of the RegisteredServer.</span></span>

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

### <span data-ttu-id="84e07-133">-Storages Cservicename</span><span class="sxs-lookup"><span data-stu-id="84e07-133">-StorageSyncServiceName</span></span>
<span data-ttu-id="84e07-134">Storages Cservice의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="84e07-134">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="84e07-135">-확인</span><span class="sxs-lookup"><span data-stu-id="84e07-135">-Confirm</span></span>
<span data-ttu-id="84e07-136">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="84e07-136">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84e07-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84e07-137">-WhatIf</span></span>
<span data-ttu-id="84e07-138">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="84e07-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="84e07-139">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="84e07-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84e07-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84e07-140">CommonParameters</span></span>
<span data-ttu-id="84e07-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="84e07-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84e07-142">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84e07-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84e07-143">입력</span><span class="sxs-lookup"><span data-stu-id="84e07-143">INPUTS</span></span>

### <span data-ttu-id="84e07-144">StorageSync. PSRegisteredServer/.</span><span class="sxs-lookup"><span data-stu-id="84e07-144">Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer</span></span>

### <span data-ttu-id="84e07-145">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="84e07-145">System.String</span></span>

### <span data-ttu-id="84e07-146">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="84e07-146">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="84e07-147">출력</span><span class="sxs-lookup"><span data-stu-id="84e07-147">OUTPUTS</span></span>

### <span data-ttu-id="84e07-148">System. 개체</span><span class="sxs-lookup"><span data-stu-id="84e07-148">System.Object</span></span>
## <span data-ttu-id="84e07-149">상속자</span><span class="sxs-lookup"><span data-stu-id="84e07-149">NOTES</span></span>

## <span data-ttu-id="84e07-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="84e07-150">RELATED LINKS</span></span>
