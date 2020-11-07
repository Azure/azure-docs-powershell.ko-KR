---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/az.storagesync/remove-azstoragesyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncGroup.md
ms.openlocfilehash: f7c1f129d9a5f6f6bdd117597a2943567fb4001d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698481"
---
# <span data-ttu-id="18ccc-101">Remove-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="18ccc-101">Remove-AzStorageSyncGroup</span></span>

## <span data-ttu-id="18ccc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18ccc-102">SYNOPSIS</span></span>
<span data-ttu-id="18ccc-103">이 명령은 지정 된 동기화 그룹을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="18ccc-103">This command will delete the specified sync group.</span></span>

## <span data-ttu-id="18ccc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="18ccc-104">SYNTAX</span></span>

### <span data-ttu-id="18ccc-105">StringParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="18ccc-105">StringParameterSet (Default)</span></span>
```
Remove-AzStorageSyncGroup [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> [-Name] <String>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="18ccc-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="18ccc-106">InputObjectParameterSet</span></span>
```
Remove-AzStorageSyncGroup [-InputObject] <PSSyncGroup> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18ccc-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="18ccc-107">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncGroup [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="18ccc-108">설명은</span><span class="sxs-lookup"><span data-stu-id="18ccc-108">DESCRIPTION</span></span>
<span data-ttu-id="18ccc-109">이 명령은 지정 된 동기화 그룹을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="18ccc-109">This command will delete the specified sync group.</span></span> <span data-ttu-id="18ccc-110">동기화 그룹은 포함 된 모든 끝점이 먼저 삭제 된 경우에만 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="18ccc-110">A sync group can only be removed when all of the contained endpoints are deleted first.</span></span>

## <span data-ttu-id="18ccc-111">예제의</span><span class="sxs-lookup"><span data-stu-id="18ccc-111">EXAMPLES</span></span>

### <span data-ttu-id="18ccc-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="18ccc-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncGroup -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -Name "mySyncGroupName"
```

<span data-ttu-id="18ccc-113">이 명령은 동기화 그룹을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="18ccc-113">This command will remove the sync group.</span></span>

## <span data-ttu-id="18ccc-114">변수</span><span class="sxs-lookup"><span data-stu-id="18ccc-114">PARAMETERS</span></span>

### <span data-ttu-id="18ccc-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="18ccc-115">-AsJob</span></span>
<span data-ttu-id="18ccc-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="18ccc-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="18ccc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18ccc-117">-DefaultProfile</span></span>
<span data-ttu-id="18ccc-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="18ccc-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="18ccc-119">-Force</span><span class="sxs-lookup"><span data-stu-id="18ccc-119">-Force</span></span>
<span data-ttu-id="18ccc-120">이 명령에 대 한 확인을 건너뛰기 위해-Force를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="18ccc-120">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="18ccc-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="18ccc-121">-InputObject</span></span>
<span data-ttu-id="18ccc-122">SyncGroup 입력 개체</span><span class="sxs-lookup"><span data-stu-id="18ccc-122">SyncGroup Input Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="18ccc-123">-이름</span><span class="sxs-lookup"><span data-stu-id="18ccc-123">-Name</span></span>
<span data-ttu-id="18ccc-124">SyncGroup의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="18ccc-124">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: SyncGroupName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18ccc-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="18ccc-125">-PassThru</span></span>
<span data-ttu-id="18ccc-126">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="18ccc-126">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="18ccc-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18ccc-127">-ResourceGroupName</span></span>
<span data-ttu-id="18ccc-128">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="18ccc-128">Resource Group Name.</span></span>

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

### <span data-ttu-id="18ccc-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="18ccc-129">-ResourceId</span></span>
<span data-ttu-id="18ccc-130">SyncGroup 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="18ccc-130">SyncGroup Resource Id</span></span>

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

### <span data-ttu-id="18ccc-131">-Storages<c13> Cservicename</span><span class="sxs-lookup"><span data-stu-id="18ccc-131">-StorageSyncServiceName</span></span>
<span data-ttu-id="18ccc-132">Storages<c13> Cservice의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="18ccc-132">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="18ccc-133">-확인</span><span class="sxs-lookup"><span data-stu-id="18ccc-133">-Confirm</span></span>
<span data-ttu-id="18ccc-134">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="18ccc-134">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18ccc-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18ccc-135">-WhatIf</span></span>
<span data-ttu-id="18ccc-136">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="18ccc-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="18ccc-137">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="18ccc-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18ccc-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18ccc-138">CommonParameters</span></span>
<span data-ttu-id="18ccc-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="18ccc-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18ccc-140">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18ccc-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18ccc-141">입력</span><span class="sxs-lookup"><span data-stu-id="18ccc-141">INPUTS</span></span>

### <span data-ttu-id="18ccc-142">StorageSync. a m m Syncgroup</span><span class="sxs-lookup"><span data-stu-id="18ccc-142">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

### <span data-ttu-id="18ccc-143">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="18ccc-143">System.String</span></span>

### <span data-ttu-id="18ccc-144">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="18ccc-144">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="18ccc-145">출력</span><span class="sxs-lookup"><span data-stu-id="18ccc-145">OUTPUTS</span></span>

### <span data-ttu-id="18ccc-146">System. 개체</span><span class="sxs-lookup"><span data-stu-id="18ccc-146">System.Object</span></span>
## <span data-ttu-id="18ccc-147">상속자</span><span class="sxs-lookup"><span data-stu-id="18ccc-147">NOTES</span></span>

## <span data-ttu-id="18ccc-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="18ccc-148">RELATED LINKS</span></span>
