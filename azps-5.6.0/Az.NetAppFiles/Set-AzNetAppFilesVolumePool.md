---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/set-aznetAppfilesvolumepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Set-AzNetAppFilesVolumePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Set-AzNetAppFilesVolumePool.md
ms.openlocfilehash: 2b3cf6588f32fd958073ced8d3347733416037ac
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968176"
---
# <span data-ttu-id="7d91c-101">Set-AzNetAppFilesVolumePool</span><span class="sxs-lookup"><span data-stu-id="7d91c-101">Set-AzNetAppFilesVolumePool</span></span>

## <span data-ttu-id="7d91c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d91c-102">SYNOPSIS</span></span>
<span data-ttu-id="7d91c-103">ANF(Azure NetApp Files) 볼륨에 대한 풀을 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="7d91c-103">Change pool for an Azure NetApp Files (ANF) volume.</span></span>

## <span data-ttu-id="7d91c-104">구문</span><span class="sxs-lookup"><span data-stu-id="7d91c-104">SYNTAX</span></span>

### <span data-ttu-id="7d91c-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="7d91c-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzNetAppFilesVolumePool -ResourceGroupName <String> -AccountName <String> -PoolName <String> -Name <String>
 [-NewPoolResourceId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7d91c-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d91c-106">ByParentObjectParameterSet</span></span>
```
Set-AzNetAppFilesVolumePool -Name <String> -PoolObject <PSNetAppFilesPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d91c-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d91c-107">ByResourceIdParameterSet</span></span>
```
Set-AzNetAppFilesVolumePool -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d91c-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d91c-108">ByObjectParameterSet</span></span>
```
Set-AzNetAppFilesVolumePool -InputObject <PSNetAppFilesVolume> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d91c-109">설명</span><span class="sxs-lookup"><span data-stu-id="7d91c-109">DESCRIPTION</span></span>
<span data-ttu-id="7d91c-110">**Set-AzNetAppFilesVolumePool** cmdlet은 ANF 볼륨의 풀을 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="7d91c-110">The **Set-AzNetAppFilesVolumePool** cmdlet changes the pool of an ANF volume.</span></span>

## <span data-ttu-id="7d91c-111">예제</span><span class="sxs-lookup"><span data-stu-id="7d91c-111">EXAMPLES</span></span>

### <span data-ttu-id="7d91c-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="7d91c-112">Example 1</span></span>
```powershell
PS C:\>Set-AzNetAppFilesVolumePool -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -Name "MyAnfVolume" -NewPoolResourceId 7d6e4069-6c78-6c61-7bf6-c60968e45fbf
```

<span data-ttu-id="7d91c-113">이렇게 하여 볼륨 MyVolume의 풀이 7d6e4069-6c78-6c61-7bf6-c60968e45fbf로 변경됩니다.</span><span class="sxs-lookup"><span data-stu-id="7d91c-113">This changes the pool for the volume MyVolume to one with the Id of 7d6e4069-6c78-6c61-7bf6-c60968e45fbf</span></span>

## <span data-ttu-id="7d91c-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="7d91c-114">PARAMETERS</span></span>

### <span data-ttu-id="7d91c-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="7d91c-115">-AccountName</span></span>
<span data-ttu-id="7d91c-116">ANF 계정의 이름</span><span class="sxs-lookup"><span data-stu-id="7d91c-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="7d91c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d91c-117">-DefaultProfile</span></span>
<span data-ttu-id="7d91c-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7d91c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7d91c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7d91c-119">-InputObject</span></span>
<span data-ttu-id="7d91c-120">이동할 볼륨 개체</span><span class="sxs-lookup"><span data-stu-id="7d91c-120">The volume object to move</span></span>

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

### <span data-ttu-id="7d91c-121">-Name</span><span class="sxs-lookup"><span data-stu-id="7d91c-121">-Name</span></span>
<span data-ttu-id="7d91c-122">ANF 볼륨의 이름</span><span class="sxs-lookup"><span data-stu-id="7d91c-122">The name of the ANF volume</span></span>

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

### <span data-ttu-id="7d91c-123">-NewPoolResourceId</span><span class="sxs-lookup"><span data-stu-id="7d91c-123">-NewPoolResourceId</span></span>
<span data-ttu-id="7d91c-124">이동할 용량 풀의 ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="7d91c-124">ResourceId of the capacity pool to move to.</span></span>
<span data-ttu-id="7d91c-125">풀을 식별하는 데 사용되는 UUID v4</span><span class="sxs-lookup"><span data-stu-id="7d91c-125">UUID v4 used to identify the pool</span></span>

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

### <span data-ttu-id="7d91c-126">-PoolName</span><span class="sxs-lookup"><span data-stu-id="7d91c-126">-PoolName</span></span>
<span data-ttu-id="7d91c-127">ANF 풀의 이름</span><span class="sxs-lookup"><span data-stu-id="7d91c-127">The name of the ANF pool</span></span>

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

### <span data-ttu-id="7d91c-128">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="7d91c-128">-PoolObject</span></span>
<span data-ttu-id="7d91c-129">볼륨을 포함하는 풀 개체</span><span class="sxs-lookup"><span data-stu-id="7d91c-129">The pool object containing the volume</span></span>

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

### <span data-ttu-id="7d91c-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d91c-130">-ResourceGroupName</span></span>
<span data-ttu-id="7d91c-131">ANF 볼륨의 리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="7d91c-131">The resource group of the ANF volume</span></span>

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

### <span data-ttu-id="7d91c-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7d91c-132">-ResourceId</span></span>
<span data-ttu-id="7d91c-133">ANF 볼륨의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="7d91c-133">The resource id of the ANF volume</span></span>

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

### <span data-ttu-id="7d91c-134">-확인</span><span class="sxs-lookup"><span data-stu-id="7d91c-134">-Confirm</span></span>
<span data-ttu-id="7d91c-135">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7d91c-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d91c-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d91c-136">-WhatIf</span></span>
<span data-ttu-id="7d91c-137">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="7d91c-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d91c-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7d91c-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d91c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d91c-139">CommonParameters</span></span>
<span data-ttu-id="7d91c-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7d91c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d91c-141">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7d91c-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d91c-142">입력</span><span class="sxs-lookup"><span data-stu-id="7d91c-142">INPUTS</span></span>

### <span data-ttu-id="7d91c-143">System.String</span><span class="sxs-lookup"><span data-stu-id="7d91c-143">System.String</span></span>

### <span data-ttu-id="7d91c-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="7d91c-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

### <span data-ttu-id="7d91c-145">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="7d91c-145">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="7d91c-146">출력</span><span class="sxs-lookup"><span data-stu-id="7d91c-146">OUTPUTS</span></span>

### <span data-ttu-id="7d91c-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7d91c-147">System.Boolean</span></span>

## <span data-ttu-id="7d91c-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7d91c-148">NOTES</span></span>

## <span data-ttu-id="7d91c-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7d91c-149">RELATED LINKS</span></span>
