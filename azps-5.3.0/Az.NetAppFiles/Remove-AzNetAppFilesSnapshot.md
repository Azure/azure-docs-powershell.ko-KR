---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilessnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesSnapshot.md
ms.openlocfilehash: 1d28420e9457826f7c851eb0d3013f36de9edbc2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98380612"
---
# <span data-ttu-id="9b5a9-101">Remove-AzNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="9b5a9-101">Remove-AzNetAppFilesSnapshot</span></span>

## <span data-ttu-id="9b5a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b5a9-102">SYNOPSIS</span></span>
<span data-ttu-id="9b5a9-103">ANF(Azure NetApp Files) 스냅숏을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="9b5a9-103">Deletes an Azure NetApp Files (ANF) snapshot.</span></span>

## <span data-ttu-id="9b5a9-104">구문</span><span class="sxs-lookup"><span data-stu-id="9b5a9-104">SYNTAX</span></span>

### <span data-ttu-id="9b5a9-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="9b5a9-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesSnapshot -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -VolumeName <String> -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b5a9-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b5a9-106">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshot -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b5a9-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b5a9-107">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshot -VolumeObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b5a9-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b5a9-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshot -InputObject <PSNetAppFilesSnapshot> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b5a9-109">설명</span><span class="sxs-lookup"><span data-stu-id="9b5a9-109">DESCRIPTION</span></span>
<span data-ttu-id="9b5a9-110">**Remove-AzNetAppFilesSnapshot** cmdlet은 ANF 스냅숏을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="9b5a9-110">The **Remove-AzNetAppFilesSnapshot** cmdlet deletes an ANF snapshot.</span></span>

## <span data-ttu-id="9b5a9-111">예제</span><span class="sxs-lookup"><span data-stu-id="9b5a9-111">EXAMPLES</span></span>

### <span data-ttu-id="9b5a9-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="9b5a9-112">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesSnapshot -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyAnfVolume" -Name "MyAnfSnapshot"
```

<span data-ttu-id="9b5a9-113">이 명령은 ANF 스냅숏 "MyAnfSnapshot"을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="9b5a9-113">This command deletes the ANF snapshot "MyAnfSnapshot".</span></span>

## <span data-ttu-id="9b5a9-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9b5a9-114">PARAMETERS</span></span>

### <span data-ttu-id="9b5a9-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="9b5a9-115">-AccountName</span></span>
<span data-ttu-id="9b5a9-116">ANF 계정의 이름</span><span class="sxs-lookup"><span data-stu-id="9b5a9-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="9b5a9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b5a9-117">-DefaultProfile</span></span>
<span data-ttu-id="9b5a9-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9b5a9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b5a9-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9b5a9-119">-InputObject</span></span>
<span data-ttu-id="9b5a9-120">제거할 스냅숏 개체</span><span class="sxs-lookup"><span data-stu-id="9b5a9-120">The snapshot object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshot
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9b5a9-121">-Name</span><span class="sxs-lookup"><span data-stu-id="9b5a9-121">-Name</span></span>
<span data-ttu-id="9b5a9-122">ANF 스냅숏의 이름</span><span class="sxs-lookup"><span data-stu-id="9b5a9-122">The name of the ANF snapshot</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: SnapshotName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b5a9-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9b5a9-123">-PassThru</span></span>
<span data-ttu-id="9b5a9-124">지정된 볼륨이 성공적으로 제거됐는지 여부를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="9b5a9-124">Return whether the specified volume was successfully removed</span></span>

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

### <span data-ttu-id="9b5a9-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="9b5a9-125">-PoolName</span></span>
<span data-ttu-id="9b5a9-126">ANF 풀의 이름</span><span class="sxs-lookup"><span data-stu-id="9b5a9-126">The name of the ANF pool</span></span>

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

### <span data-ttu-id="9b5a9-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b5a9-127">-ResourceGroupName</span></span>
<span data-ttu-id="9b5a9-128">ANF 스냅숏의 리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="9b5a9-128">The resource group of the ANF snapshot</span></span>

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

### <span data-ttu-id="9b5a9-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9b5a9-129">-ResourceId</span></span>
<span data-ttu-id="9b5a9-130">ANF 스냅숏의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="9b5a9-130">The resource id of the ANF snapshot</span></span>

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

### <span data-ttu-id="9b5a9-131">-VolumeName</span><span class="sxs-lookup"><span data-stu-id="9b5a9-131">-VolumeName</span></span>
<span data-ttu-id="9b5a9-132">ANF 볼륨의 이름</span><span class="sxs-lookup"><span data-stu-id="9b5a9-132">The name of the ANF volume</span></span>

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

### <span data-ttu-id="9b5a9-133">-VolumeObject</span><span class="sxs-lookup"><span data-stu-id="9b5a9-133">-VolumeObject</span></span>
<span data-ttu-id="9b5a9-134">제거할 스냅숏을 포함하는 볼륨 개체</span><span class="sxs-lookup"><span data-stu-id="9b5a9-134">The volume object containing the snapshot to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9b5a9-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9b5a9-135">-Confirm</span></span>
<span data-ttu-id="9b5a9-136">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="9b5a9-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b5a9-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b5a9-137">-WhatIf</span></span>
<span data-ttu-id="9b5a9-138">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="9b5a9-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b5a9-139">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9b5a9-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b5a9-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b5a9-140">CommonParameters</span></span>
<span data-ttu-id="9b5a9-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9b5a9-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b5a9-142">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9b5a9-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b5a9-143">입력</span><span class="sxs-lookup"><span data-stu-id="9b5a9-143">INPUTS</span></span>

### <span data-ttu-id="9b5a9-144">System.String</span><span class="sxs-lookup"><span data-stu-id="9b5a9-144">System.String</span></span>

### <span data-ttu-id="9b5a9-145">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="9b5a9-145">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

### <span data-ttu-id="9b5a9-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="9b5a9-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshot</span></span>

## <span data-ttu-id="9b5a9-147">출력</span><span class="sxs-lookup"><span data-stu-id="9b5a9-147">OUTPUTS</span></span>

### <span data-ttu-id="9b5a9-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9b5a9-148">System.Boolean</span></span>

## <span data-ttu-id="9b5a9-149">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9b5a9-149">NOTES</span></span>

## <span data-ttu-id="9b5a9-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9b5a9-150">RELATED LINKS</span></span>
