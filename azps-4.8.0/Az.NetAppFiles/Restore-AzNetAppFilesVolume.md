---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/restore-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Restore-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Restore-AzNetAppFilesVolume.md
ms.openlocfilehash: 486bd44d3f48213fde6fb9b6c1d15a5683c1fd82
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204062"
---
# <span data-ttu-id="7b45b-101">Restore-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="7b45b-101">Restore-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="7b45b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7b45b-102">SYNOPSIS</span></span>
<span data-ttu-id="7b45b-103">볼륨을 해당 스냅숏 중 하나로 복원/되돌리기</span><span class="sxs-lookup"><span data-stu-id="7b45b-103">Restore/Revert a volume to one of its snapshots</span></span>

## <span data-ttu-id="7b45b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7b45b-104">SYNTAX</span></span>

### <span data-ttu-id="7b45b-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="7b45b-105">ByFieldsParameterSet (Default)</span></span>
```
Revert-AzNetAppFilesVolume -ResourceGroupName <String> -AccountName <String> -PoolName <String> -Name <String>
 [-SnapshotId <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7b45b-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7b45b-106">ByParentObjectParameterSet</span></span>
```
Restore-AzNetAppFilesVolume -Name <String> -PoolObject <PSNetAppFilesPool> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b45b-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7b45b-107">ByResourceIdParameterSet</span></span>
```
Restore-AzNetAppFilesVolume -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b45b-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7b45b-108">ByObjectParameterSet</span></span>
```
Restore-AzNetAppFilesVolume -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b45b-109">설명은</span><span class="sxs-lookup"><span data-stu-id="7b45b-109">DESCRIPTION</span></span>
<span data-ttu-id="7b45b-110">볼륨을 SnapshotId 매개 변수에 지정 된 스냅숏으로 복원/되돌리기</span><span class="sxs-lookup"><span data-stu-id="7b45b-110">Restore/Revert a volume to the snapshot specified in the SnapshotId paramter</span></span>

## <span data-ttu-id="7b45b-111">예제의</span><span class="sxs-lookup"><span data-stu-id="7b45b-111">EXAMPLES</span></span>

### <span data-ttu-id="7b45b-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="7b45b-112">Example 1</span></span>
```powershell
PS C:\> Restore-AzNetAppFilesVolume -ResourceGroupName "MyRG" -Location "westus2" -AccountName "MyAccount" -PoolName "MyPool" -VolumeName "MyVolume" -SnapshotId 7d6e4069-6c78-6c61-7bf6-c60968e45fbf
```

<span data-ttu-id="7b45b-113">이 명령은 볼륨 MyVolume을 7d6e4069-6c78-6c61-7bf6-c60968e45fbf snapshotId의 스냅숏 중 하나로 복원/되돌립니다.</span><span class="sxs-lookup"><span data-stu-id="7b45b-113">This command Restores/Reverts the volume MyVolume to one of its snapshots with the snapshotId of 7d6e4069-6c78-6c61-7bf6-c60968e45fbf</span></span>

## <span data-ttu-id="7b45b-114">변수</span><span class="sxs-lookup"><span data-stu-id="7b45b-114">PARAMETERS</span></span>

### <span data-ttu-id="7b45b-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="7b45b-115">-AccountName</span></span>
<span data-ttu-id="7b45b-116">ANF 계정의 이름</span><span class="sxs-lookup"><span data-stu-id="7b45b-116">The name of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b45b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b45b-117">-DefaultProfile</span></span>
<span data-ttu-id="7b45b-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7b45b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b45b-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7b45b-119">-InputObject</span></span>
<span data-ttu-id="7b45b-120">제거할 볼륨 개체</span><span class="sxs-lookup"><span data-stu-id="7b45b-120">The volume object to remove</span></span>

```yaml
Type: PSNetAppFilesVolume
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7b45b-121">-이름</span><span class="sxs-lookup"><span data-stu-id="7b45b-121">-Name</span></span>
<span data-ttu-id="7b45b-122">ANF 볼륨의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7b45b-122">The name of the ANF volume</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: VolumeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b45b-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7b45b-123">-PassThru</span></span>
<span data-ttu-id="7b45b-124">지정 된 볼륨을 성공적으로 복원/되돌리지 여부 반환</span><span class="sxs-lookup"><span data-stu-id="7b45b-124">Return whether the specified volume was successfully restored/reverted</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b45b-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="7b45b-125">-PoolName</span></span>
<span data-ttu-id="7b45b-126">ANF 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7b45b-126">The name of the ANF pool</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b45b-127">-Poo</span><span class="sxs-lookup"><span data-stu-id="7b45b-127">-PoolObject</span></span>
<span data-ttu-id="7b45b-128">제거할 볼륨을 포함 하는 pool 개체</span><span class="sxs-lookup"><span data-stu-id="7b45b-128">The pool object containing the volume to remove</span></span>

```yaml
Type: PSNetAppFilesPool
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7b45b-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b45b-129">-ResourceGroupName</span></span>
<span data-ttu-id="7b45b-130">ANF 볼륨의 리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="7b45b-130">The resource group of the ANF volume</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b45b-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7b45b-131">-ResourceId</span></span>
<span data-ttu-id="7b45b-132">ANF 볼륨의 리소스 id</span><span class="sxs-lookup"><span data-stu-id="7b45b-132">The resource id of the ANF volume</span></span>

```yaml
Type: String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b45b-133">-SnapshotId</span><span class="sxs-lookup"><span data-stu-id="7b45b-133">-SnapshotId</span></span>
<span data-ttu-id="7b45b-134">스냅샷의 SnapshotId.</span><span class="sxs-lookup"><span data-stu-id="7b45b-134">SnapshotId of the snapshot.</span></span>
<span data-ttu-id="7b45b-135">스냅숏을 식별 하는 데 사용 되는 UUID v4</span><span class="sxs-lookup"><span data-stu-id="7b45b-135">UUID v4 used to identify the Snapshot</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b45b-136">-확인</span><span class="sxs-lookup"><span data-stu-id="7b45b-136">-Confirm</span></span>
<span data-ttu-id="7b45b-137">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b45b-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b45b-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b45b-138">-WhatIf</span></span>
<span data-ttu-id="7b45b-139">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7b45b-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b45b-140">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7b45b-140">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b45b-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b45b-141">CommonParameters</span></span>
<span data-ttu-id="7b45b-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b45b-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b45b-143">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7b45b-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b45b-144">입력</span><span class="sxs-lookup"><span data-stu-id="7b45b-144">INPUTS</span></span>

### <span data-ttu-id="7b45b-145">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7b45b-145">System.String</span></span>

### <span data-ttu-id="7b45b-146">Microsoft. p. p. p. p i p. p i a p. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="7b45b-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

### <span data-ttu-id="7b45b-147">Microsoft. Azure. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="7b45b-147">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="7b45b-148">출력</span><span class="sxs-lookup"><span data-stu-id="7b45b-148">OUTPUTS</span></span>

### <span data-ttu-id="7b45b-149">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="7b45b-149">System.Boolean</span></span>

## <span data-ttu-id="7b45b-150">상속자</span><span class="sxs-lookup"><span data-stu-id="7b45b-150">NOTES</span></span>

## <span data-ttu-id="7b45b-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7b45b-151">RELATED LINKS</span></span>
