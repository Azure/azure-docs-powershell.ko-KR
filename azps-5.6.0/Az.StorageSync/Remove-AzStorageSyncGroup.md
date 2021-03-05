---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/powershell/module/az.storagesync/remove-azstoragesyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncGroup.md
ms.openlocfilehash: 38c6d45c4e49f86d3aacc2774942d15ddd50941e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974043"
---
# <span data-ttu-id="9a595-101">Remove-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="9a595-101">Remove-AzStorageSyncGroup</span></span>

## <span data-ttu-id="9a595-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a595-102">SYNOPSIS</span></span>
<span data-ttu-id="9a595-103">이 명령은 지정된 동기화 그룹을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="9a595-103">This command will delete the specified sync group.</span></span>

## <span data-ttu-id="9a595-104">구문</span><span class="sxs-lookup"><span data-stu-id="9a595-104">SYNTAX</span></span>

### <span data-ttu-id="9a595-105">StringParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="9a595-105">StringParameterSet (Default)</span></span>
```
Remove-AzStorageSyncGroup [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> [-Name] <String>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9a595-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a595-106">InputObjectParameterSet</span></span>
```
Remove-AzStorageSyncGroup [-InputObject] <PSSyncGroup> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a595-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a595-107">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncGroup [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a595-108">설명</span><span class="sxs-lookup"><span data-stu-id="9a595-108">DESCRIPTION</span></span>
<span data-ttu-id="9a595-109">이 명령은 지정된 동기화 그룹을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="9a595-109">This command will delete the specified sync group.</span></span> <span data-ttu-id="9a595-110">포함된 모든 엔드포인트가 먼저 삭제될 때만 동기화 그룹을 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9a595-110">A sync group can only be removed when all of the contained endpoints are deleted first.</span></span>

## <span data-ttu-id="9a595-111">예제</span><span class="sxs-lookup"><span data-stu-id="9a595-111">EXAMPLES</span></span>

### <span data-ttu-id="9a595-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="9a595-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncGroup -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -Name "mySyncGroupName"
```

<span data-ttu-id="9a595-113">이 명령은 동기화 그룹을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="9a595-113">This command will remove the sync group.</span></span>

## <span data-ttu-id="9a595-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="9a595-114">PARAMETERS</span></span>

### <span data-ttu-id="9a595-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9a595-115">-AsJob</span></span>
<span data-ttu-id="9a595-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="9a595-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9a595-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a595-117">-DefaultProfile</span></span>
<span data-ttu-id="9a595-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9a595-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a595-119">-Force</span><span class="sxs-lookup"><span data-stu-id="9a595-119">-Force</span></span>
<span data-ttu-id="9a595-120">이 명령의 확인을 건너뛰기 위해 -Force를 공급합니다.</span><span class="sxs-lookup"><span data-stu-id="9a595-120">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="9a595-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9a595-121">-InputObject</span></span>
<span data-ttu-id="9a595-122">SyncGroup 입력 개체</span><span class="sxs-lookup"><span data-stu-id="9a595-122">SyncGroup Input Object</span></span>

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

### <span data-ttu-id="9a595-123">-Name</span><span class="sxs-lookup"><span data-stu-id="9a595-123">-Name</span></span>
<span data-ttu-id="9a595-124">SyncGroup의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9a595-124">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="9a595-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9a595-125">-PassThru</span></span>
<span data-ttu-id="9a595-126">정상적인 실행에서 이 cmdlet은 성공에 대한 값을 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9a595-126">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="9a595-127">PassThru 매개 변수를 제공하는 경우 cmdlet은 성공적으로 실행된 후 파이프라인에 값을 쓴다.</span><span class="sxs-lookup"><span data-stu-id="9a595-127">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="9a595-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a595-128">-ResourceGroupName</span></span>
<span data-ttu-id="9a595-129">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9a595-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="9a595-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9a595-130">-ResourceId</span></span>
<span data-ttu-id="9a595-131">SyncGroup 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="9a595-131">SyncGroup Resource Id</span></span>

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

### <span data-ttu-id="9a595-132">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="9a595-132">-StorageSyncServiceName</span></span>
<span data-ttu-id="9a595-133">StorageSyncService의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9a595-133">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="9a595-134">-확인</span><span class="sxs-lookup"><span data-stu-id="9a595-134">-Confirm</span></span>
<span data-ttu-id="9a595-135">cmdlet을 실행하기 전에 확인을 요청합니다.</span><span class="sxs-lookup"><span data-stu-id="9a595-135">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a595-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a595-136">-WhatIf</span></span>
<span data-ttu-id="9a595-137">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="9a595-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9a595-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9a595-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a595-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a595-139">CommonParameters</span></span>
<span data-ttu-id="9a595-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9a595-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a595-141">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="9a595-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a595-142">입력</span><span class="sxs-lookup"><span data-stu-id="9a595-142">INPUTS</span></span>

### <span data-ttu-id="9a595-143">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="9a595-143">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

### <span data-ttu-id="9a595-144">System.String</span><span class="sxs-lookup"><span data-stu-id="9a595-144">System.String</span></span>

### <span data-ttu-id="9a595-145">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="9a595-145">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="9a595-146">출력</span><span class="sxs-lookup"><span data-stu-id="9a595-146">OUTPUTS</span></span>

### <span data-ttu-id="9a595-147">System.Object</span><span class="sxs-lookup"><span data-stu-id="9a595-147">System.Object</span></span>
## <span data-ttu-id="9a595-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9a595-148">NOTES</span></span>

## <span data-ttu-id="9a595-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9a595-149">RELATED LINKS</span></span>
