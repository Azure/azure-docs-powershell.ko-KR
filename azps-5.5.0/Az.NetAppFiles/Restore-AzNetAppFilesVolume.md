---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/restore-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Restore-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Restore-AzNetAppFilesVolume.md
ms.openlocfilehash: 6606de1a5d4de6df6ecafa700ac1b93d31399b43
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203291"
---
# <span data-ttu-id="cb594-101">Restore-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="cb594-101">Restore-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="cb594-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb594-102">SYNOPSIS</span></span>
<span data-ttu-id="cb594-103">볼륨을 스냅숏 중 하나로 복원/되감기</span><span class="sxs-lookup"><span data-stu-id="cb594-103">Restore/Revert a volume to one of its snapshots</span></span>

## <span data-ttu-id="cb594-104">구문</span><span class="sxs-lookup"><span data-stu-id="cb594-104">SYNTAX</span></span>

### <span data-ttu-id="cb594-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="cb594-105">ByFieldsParameterSet (Default)</span></span>
```
Restore-AzNetAppFilesVolume -ResourceGroupName <String> -AccountName <String> -PoolName <String> -Name <String>
 [-SnapshotId <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cb594-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cb594-106">ByParentObjectParameterSet</span></span>
```
Restore-AzNetAppFilesVolume -Name <String> -PoolObject <PSNetAppFilesPool> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb594-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cb594-107">ByResourceIdParameterSet</span></span>
```
Restore-AzNetAppFilesVolume -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb594-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cb594-108">ByObjectParameterSet</span></span>
```
Restore-AzNetAppFilesVolume -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb594-109">설명</span><span class="sxs-lookup"><span data-stu-id="cb594-109">DESCRIPTION</span></span>
<span data-ttu-id="cb594-110">SnapshotId paramter에 지정된 스냅숏으로 볼륨 복원/되감기</span><span class="sxs-lookup"><span data-stu-id="cb594-110">Restore/Revert a volume to the snapshot specified in the SnapshotId paramter</span></span>

## <span data-ttu-id="cb594-111">예제</span><span class="sxs-lookup"><span data-stu-id="cb594-111">EXAMPLES</span></span>

### <span data-ttu-id="cb594-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="cb594-112">Example 1</span></span>
```powershell
PS C:\> Restore-AzNetAppFilesVolume -ResourceGroupName "MyRG" -Location "westus2" -AccountName "MyAccount" -PoolName "MyPool" -VolumeName "MyVolume" -SnapshotId 7d6e4069-6c78-6c61-7bf6-c60968e45fbf
```

<span data-ttu-id="cb594-113">이 명령은 7d6e4069-6c78-6c61-7bf6-c60968e45fbf의 snapshotId를 사용하여 볼륨 MyVolume을 해당 스냅숏 중 하나로 복원/되감기</span><span class="sxs-lookup"><span data-stu-id="cb594-113">This command Restores/Reverts the volume MyVolume to one of its snapshots with the snapshotId of 7d6e4069-6c78-6c61-7bf6-c60968e45fbf</span></span>

## <span data-ttu-id="cb594-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cb594-114">PARAMETERS</span></span>

### <span data-ttu-id="cb594-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="cb594-115">-AccountName</span></span>
<span data-ttu-id="cb594-116">ANF 계정의 이름</span><span class="sxs-lookup"><span data-stu-id="cb594-116">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb594-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb594-117">-DefaultProfile</span></span>
<span data-ttu-id="cb594-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cb594-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb594-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cb594-119">-InputObject</span></span>
<span data-ttu-id="cb594-120">제거할 볼륨 개체</span><span class="sxs-lookup"><span data-stu-id="cb594-120">The volume object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cb594-121">-Name</span><span class="sxs-lookup"><span data-stu-id="cb594-121">-Name</span></span>
<span data-ttu-id="cb594-122">ANF 볼륨의 이름</span><span class="sxs-lookup"><span data-stu-id="cb594-122">The name of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: VolumeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb594-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cb594-123">-PassThru</span></span>
<span data-ttu-id="cb594-124">지정된 볼륨이 성공적으로 복원/되감은지 여부를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="cb594-124">Return whether the specified volume was successfully restored/reverted</span></span>

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

### <span data-ttu-id="cb594-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="cb594-125">-PoolName</span></span>
<span data-ttu-id="cb594-126">ANF 풀의 이름</span><span class="sxs-lookup"><span data-stu-id="cb594-126">The name of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb594-127">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="cb594-127">-PoolObject</span></span>
<span data-ttu-id="cb594-128">제거할 볼륨을 포함하는 풀 개체</span><span class="sxs-lookup"><span data-stu-id="cb594-128">The pool object containing the volume to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cb594-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb594-129">-ResourceGroupName</span></span>
<span data-ttu-id="cb594-130">ANF 볼륨의 리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="cb594-130">The resource group of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb594-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cb594-131">-ResourceId</span></span>
<span data-ttu-id="cb594-132">ANF 볼륨의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="cb594-132">The resource id of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb594-133">-SnapshotId</span><span class="sxs-lookup"><span data-stu-id="cb594-133">-SnapshotId</span></span>
<span data-ttu-id="cb594-134">스냅숏의 SnapshotId입니다.</span><span class="sxs-lookup"><span data-stu-id="cb594-134">SnapshotId of the snapshot.</span></span>
<span data-ttu-id="cb594-135">스냅숏을 식별하는 데 사용되는 UUID v4</span><span class="sxs-lookup"><span data-stu-id="cb594-135">UUID v4 used to identify the Snapshot</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb594-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cb594-136">-Confirm</span></span>
<span data-ttu-id="cb594-137">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="cb594-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb594-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb594-138">-WhatIf</span></span>
<span data-ttu-id="cb594-139">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="cb594-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb594-140">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cb594-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb594-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb594-141">CommonParameters</span></span>
<span data-ttu-id="cb594-142">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="cb594-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb594-143">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="cb594-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb594-144">입력</span><span class="sxs-lookup"><span data-stu-id="cb594-144">INPUTS</span></span>

### <span data-ttu-id="cb594-145">System.String</span><span class="sxs-lookup"><span data-stu-id="cb594-145">System.String</span></span>

### <span data-ttu-id="cb594-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="cb594-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

### <span data-ttu-id="cb594-147">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="cb594-147">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="cb594-148">출력</span><span class="sxs-lookup"><span data-stu-id="cb594-148">OUTPUTS</span></span>

### <span data-ttu-id="cb594-149">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="cb594-149">System.Boolean</span></span>

## <span data-ttu-id="cb594-150">참고 사항</span><span class="sxs-lookup"><span data-stu-id="cb594-150">NOTES</span></span>

## <span data-ttu-id="cb594-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cb594-151">RELATED LINKS</span></span>
