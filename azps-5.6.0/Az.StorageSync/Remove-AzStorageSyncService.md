---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/powershell/module/Az.storagesync/remove-Azstoragesyncservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncService.md
ms.openlocfilehash: 648ef711d030f7600863d286df24cfdf1d2f7927
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974016"
---
# <span data-ttu-id="7e942-101">Remove-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="7e942-101">Remove-AzStorageSyncService</span></span>

## <span data-ttu-id="7e942-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e942-102">SYNOPSIS</span></span>
<span data-ttu-id="7e942-103">이 명령은 지정된 저장소 동기화 서비스를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="7e942-103">This command will delete the specified storage sync service.</span></span>

## <span data-ttu-id="7e942-104">구문</span><span class="sxs-lookup"><span data-stu-id="7e942-104">SYNTAX</span></span>

### <span data-ttu-id="7e942-105">StringParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="7e942-105">StringParameterSet (Default)</span></span>
```
Remove-AzStorageSyncService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e942-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7e942-106">InputObjectParameterSet</span></span>
```
Remove-AzStorageSyncService [-InputObject] <PSStorageSyncService> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e942-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7e942-107">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncService [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e942-108">설명</span><span class="sxs-lookup"><span data-stu-id="7e942-108">DESCRIPTION</span></span>
<span data-ttu-id="7e942-109">이 명령은 지정된 저장소 동기화 서비스를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="7e942-109">This command will delete the specified storage sync service.</span></span> <span data-ttu-id="7e942-110">저장소 동기화 서비스는 포함된 모든 동기화 그룹 및 등록된 서버가 먼저 삭제될 때만 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7e942-110">A storage sync service can only be removed when all of the contained sync groups and registered servers are deleted first.</span></span>

## <span data-ttu-id="7e942-111">예제</span><span class="sxs-lookup"><span data-stu-id="7e942-111">EXAMPLES</span></span>

### <span data-ttu-id="7e942-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="7e942-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncService -Force -ResourceGroupName "myResourceGroup" -Name "myStorageSyncServiceName"
```

<span data-ttu-id="7e942-113">이 명령은 저장소 동기화 서비스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7e942-113">This command will remove the storage sync service.</span></span>

## <span data-ttu-id="7e942-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="7e942-114">PARAMETERS</span></span>

### <span data-ttu-id="7e942-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7e942-115">-AsJob</span></span>
<span data-ttu-id="7e942-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="7e942-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7e942-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e942-117">-DefaultProfile</span></span>
<span data-ttu-id="7e942-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7e942-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e942-119">-Force</span><span class="sxs-lookup"><span data-stu-id="7e942-119">-Force</span></span>
<span data-ttu-id="7e942-120">이 명령의 확인을 건너뛰기 위해 -Force를 공급합니다.</span><span class="sxs-lookup"><span data-stu-id="7e942-120">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="7e942-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7e942-121">-InputObject</span></span>
<span data-ttu-id="7e942-122">StorageSyncService 입력 개체는 일반적으로 파이프라인을 통과합니다.</span><span class="sxs-lookup"><span data-stu-id="7e942-122">StorageSyncService Input Object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="7e942-123">-Name</span><span class="sxs-lookup"><span data-stu-id="7e942-123">-Name</span></span>
<span data-ttu-id="7e942-124">StorageSyncService의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7e942-124">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="7e942-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7e942-125">-PassThru</span></span>
<span data-ttu-id="7e942-126">정상적인 실행에서 이 cmdlet은 성공에 대한 값을 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7e942-126">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="7e942-127">PassThru 매개 변수를 제공하는 경우 cmdlet은 성공적으로 실행된 후 파이프라인에 값을 쓴다.</span><span class="sxs-lookup"><span data-stu-id="7e942-127">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="7e942-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e942-128">-ResourceGroupName</span></span>
<span data-ttu-id="7e942-129">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7e942-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="7e942-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7e942-130">-ResourceId</span></span>
<span data-ttu-id="7e942-131">StorageSyncService 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="7e942-131">StorageSyncService Resource Id</span></span>

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

### <span data-ttu-id="7e942-132">-확인</span><span class="sxs-lookup"><span data-stu-id="7e942-132">-Confirm</span></span>
<span data-ttu-id="7e942-133">cmdlet을 실행하기 전에 확인을 요청합니다.</span><span class="sxs-lookup"><span data-stu-id="7e942-133">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e942-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e942-134">-WhatIf</span></span>
<span data-ttu-id="7e942-135">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="7e942-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7e942-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7e942-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e942-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e942-137">CommonParameters</span></span>
<span data-ttu-id="7e942-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7e942-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e942-139">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="7e942-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e942-140">입력</span><span class="sxs-lookup"><span data-stu-id="7e942-140">INPUTS</span></span>

### <span data-ttu-id="7e942-141">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="7e942-141">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

### <span data-ttu-id="7e942-142">System.String</span><span class="sxs-lookup"><span data-stu-id="7e942-142">System.String</span></span>

### <span data-ttu-id="7e942-143">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="7e942-143">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="7e942-144">출력</span><span class="sxs-lookup"><span data-stu-id="7e942-144">OUTPUTS</span></span>

### <span data-ttu-id="7e942-145">System.Object</span><span class="sxs-lookup"><span data-stu-id="7e942-145">System.Object</span></span>
## <span data-ttu-id="7e942-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7e942-146">NOTES</span></span>

## <span data-ttu-id="7e942-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7e942-147">RELATED LINKS</span></span>
