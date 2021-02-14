---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/remove-Azstoragesyncservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncService.md
ms.openlocfilehash: f64c085f742eeabea235660d4af7ba6bd5970fdf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188812"
---
# <span data-ttu-id="bc307-101">Remove-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="bc307-101">Remove-AzStorageSyncService</span></span>

## <span data-ttu-id="bc307-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc307-102">SYNOPSIS</span></span>
<span data-ttu-id="bc307-103">이 명령은 지정된 저장소 동기화 서비스를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="bc307-103">This command will delete the specified storage sync service.</span></span>

## <span data-ttu-id="bc307-104">구문</span><span class="sxs-lookup"><span data-stu-id="bc307-104">SYNTAX</span></span>

### <span data-ttu-id="bc307-105">StringParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="bc307-105">StringParameterSet (Default)</span></span>
```
Remove-AzStorageSyncService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc307-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bc307-106">InputObjectParameterSet</span></span>
```
Remove-AzStorageSyncService [-InputObject] <PSStorageSyncService> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc307-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bc307-107">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncService [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc307-108">설명</span><span class="sxs-lookup"><span data-stu-id="bc307-108">DESCRIPTION</span></span>
<span data-ttu-id="bc307-109">이 명령은 지정된 저장소 동기화 서비스를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="bc307-109">This command will delete the specified storage sync service.</span></span> <span data-ttu-id="bc307-110">저장소 동기화 서비스는 포함된 모든 동기화 그룹 및 등록된 서버가 먼저 삭제될 때만 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bc307-110">A storage sync service can only be removed when all of the contained sync groups and registered servers are deleted first.</span></span>

## <span data-ttu-id="bc307-111">예제</span><span class="sxs-lookup"><span data-stu-id="bc307-111">EXAMPLES</span></span>

### <span data-ttu-id="bc307-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="bc307-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncService -Force -ResourceGroupName "myResourceGroup" -Name "myStorageSyncServiceName"
```

<span data-ttu-id="bc307-113">이 명령은 저장소 동기화 서비스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="bc307-113">This command will remove the storage sync service.</span></span>

## <span data-ttu-id="bc307-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bc307-114">PARAMETERS</span></span>

### <span data-ttu-id="bc307-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bc307-115">-AsJob</span></span>
<span data-ttu-id="bc307-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="bc307-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bc307-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc307-117">-DefaultProfile</span></span>
<span data-ttu-id="bc307-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bc307-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bc307-119">-Force</span><span class="sxs-lookup"><span data-stu-id="bc307-119">-Force</span></span>
<span data-ttu-id="bc307-120">이 명령의 확인을 건너뛰기 위해 -Force를 공급합니다.</span><span class="sxs-lookup"><span data-stu-id="bc307-120">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="bc307-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bc307-121">-InputObject</span></span>
<span data-ttu-id="bc307-122">StorageSyncService 입력 개체로, 일반적으로 파이프라인을 통해 전달됩니다.</span><span class="sxs-lookup"><span data-stu-id="bc307-122">StorageSyncService Input Object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bc307-123">-Name</span><span class="sxs-lookup"><span data-stu-id="bc307-123">-Name</span></span>
<span data-ttu-id="bc307-124">StorageSyncService의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bc307-124">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: StorageSyncServiceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc307-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bc307-125">-PassThru</span></span>
<span data-ttu-id="bc307-126">정상적인 실행에서 이 cmdlet은 성공 시 값을 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bc307-126">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="bc307-127">PassThru 매개 변수를 제공하는 경우 cmdlet은 실행에 성공한 후 파이프라인에 값을 쓴다.</span><span class="sxs-lookup"><span data-stu-id="bc307-127">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="bc307-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc307-128">-ResourceGroupName</span></span>
<span data-ttu-id="bc307-129">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bc307-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="bc307-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bc307-130">-ResourceId</span></span>
<span data-ttu-id="bc307-131">StorageSyncService 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="bc307-131">StorageSyncService Resource Id</span></span>

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

### <span data-ttu-id="bc307-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bc307-132">-Confirm</span></span>
<span data-ttu-id="bc307-133">cmdlet을 실행하기 전에 확인을 요청합니다.</span><span class="sxs-lookup"><span data-stu-id="bc307-133">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc307-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc307-134">-WhatIf</span></span>
<span data-ttu-id="bc307-135">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="bc307-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bc307-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bc307-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc307-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc307-137">CommonParameters</span></span>
<span data-ttu-id="bc307-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="bc307-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc307-139">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="bc307-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc307-140">입력</span><span class="sxs-lookup"><span data-stu-id="bc307-140">INPUTS</span></span>

### <span data-ttu-id="bc307-141">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="bc307-141">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

### <span data-ttu-id="bc307-142">System.String</span><span class="sxs-lookup"><span data-stu-id="bc307-142">System.String</span></span>

### <span data-ttu-id="bc307-143">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="bc307-143">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="bc307-144">출력</span><span class="sxs-lookup"><span data-stu-id="bc307-144">OUTPUTS</span></span>

### <span data-ttu-id="bc307-145">System.Object</span><span class="sxs-lookup"><span data-stu-id="bc307-145">System.Object</span></span>
## <span data-ttu-id="bc307-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="bc307-146">NOTES</span></span>

## <span data-ttu-id="bc307-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bc307-147">RELATED LINKS</span></span>
