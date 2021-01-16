---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/az.storagesync/remove-azstoragesyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncGroup.md
ms.openlocfilehash: dad4af4f954fae03a68728de928614a81eed5e5a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98366584"
---
# <span data-ttu-id="493fb-101">Remove-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="493fb-101">Remove-AzStorageSyncGroup</span></span>

## <span data-ttu-id="493fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="493fb-102">SYNOPSIS</span></span>
<span data-ttu-id="493fb-103">이 명령은 지정된 동기화 그룹을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="493fb-103">This command will delete the specified sync group.</span></span>

## <span data-ttu-id="493fb-104">구문</span><span class="sxs-lookup"><span data-stu-id="493fb-104">SYNTAX</span></span>

### <span data-ttu-id="493fb-105">StringParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="493fb-105">StringParameterSet (Default)</span></span>
```
Remove-AzStorageSyncGroup [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> [-Name] <String>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="493fb-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="493fb-106">InputObjectParameterSet</span></span>
```
Remove-AzStorageSyncGroup [-InputObject] <PSSyncGroup> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="493fb-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="493fb-107">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncGroup [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="493fb-108">설명</span><span class="sxs-lookup"><span data-stu-id="493fb-108">DESCRIPTION</span></span>
<span data-ttu-id="493fb-109">이 명령은 지정된 동기화 그룹을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="493fb-109">This command will delete the specified sync group.</span></span> <span data-ttu-id="493fb-110">포함된 모든 엔드포인트가 먼저 삭제될 때만 동기화 그룹을 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="493fb-110">A sync group can only be removed when all of the contained endpoints are deleted first.</span></span>

## <span data-ttu-id="493fb-111">예제</span><span class="sxs-lookup"><span data-stu-id="493fb-111">EXAMPLES</span></span>

### <span data-ttu-id="493fb-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="493fb-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncGroup -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -Name "mySyncGroupName"
```

<span data-ttu-id="493fb-113">이 명령은 동기화 그룹을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="493fb-113">This command will remove the sync group.</span></span>

## <span data-ttu-id="493fb-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="493fb-114">PARAMETERS</span></span>

### <span data-ttu-id="493fb-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="493fb-115">-AsJob</span></span>
<span data-ttu-id="493fb-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="493fb-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="493fb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="493fb-117">-DefaultProfile</span></span>
<span data-ttu-id="493fb-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="493fb-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="493fb-119">-Force</span><span class="sxs-lookup"><span data-stu-id="493fb-119">-Force</span></span>
<span data-ttu-id="493fb-120">이 명령의 확인을 건너뛰기 위해 -Force를 공급합니다.</span><span class="sxs-lookup"><span data-stu-id="493fb-120">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="493fb-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="493fb-121">-InputObject</span></span>
<span data-ttu-id="493fb-122">SyncGroup 입력 개체</span><span class="sxs-lookup"><span data-stu-id="493fb-122">SyncGroup Input Object</span></span>

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

### <span data-ttu-id="493fb-123">-Name</span><span class="sxs-lookup"><span data-stu-id="493fb-123">-Name</span></span>
<span data-ttu-id="493fb-124">SyncGroup의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="493fb-124">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="493fb-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="493fb-125">-PassThru</span></span>
<span data-ttu-id="493fb-126">정상적인 실행에서 이 cmdlet은 성공 시 값을 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="493fb-126">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="493fb-127">PassThru 매개 변수를 제공하는 경우 cmdlet은 실행에 성공한 후 파이프라인에 값을 쓴다.</span><span class="sxs-lookup"><span data-stu-id="493fb-127">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="493fb-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="493fb-128">-ResourceGroupName</span></span>
<span data-ttu-id="493fb-129">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="493fb-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="493fb-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="493fb-130">-ResourceId</span></span>
<span data-ttu-id="493fb-131">SyncGroup 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="493fb-131">SyncGroup Resource Id</span></span>

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

### <span data-ttu-id="493fb-132">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="493fb-132">-StorageSyncServiceName</span></span>
<span data-ttu-id="493fb-133">StorageSyncService의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="493fb-133">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="493fb-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="493fb-134">-Confirm</span></span>
<span data-ttu-id="493fb-135">cmdlet을 실행하기 전에 확인을 요청합니다.</span><span class="sxs-lookup"><span data-stu-id="493fb-135">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="493fb-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="493fb-136">-WhatIf</span></span>
<span data-ttu-id="493fb-137">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="493fb-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="493fb-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="493fb-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="493fb-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="493fb-139">CommonParameters</span></span>
<span data-ttu-id="493fb-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="493fb-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="493fb-141">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="493fb-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="493fb-142">입력</span><span class="sxs-lookup"><span data-stu-id="493fb-142">INPUTS</span></span>

### <span data-ttu-id="493fb-143">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="493fb-143">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

### <span data-ttu-id="493fb-144">System.String</span><span class="sxs-lookup"><span data-stu-id="493fb-144">System.String</span></span>

### <span data-ttu-id="493fb-145">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="493fb-145">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="493fb-146">출력</span><span class="sxs-lookup"><span data-stu-id="493fb-146">OUTPUTS</span></span>

### <span data-ttu-id="493fb-147">System.Object</span><span class="sxs-lookup"><span data-stu-id="493fb-147">System.Object</span></span>
## <span data-ttu-id="493fb-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="493fb-148">NOTES</span></span>

## <span data-ttu-id="493fb-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="493fb-149">RELATED LINKS</span></span>
