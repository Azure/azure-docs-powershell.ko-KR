---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/set-aznetAppfilesvolumepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Set-AzNetAppFilesVolumePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Set-AzNetAppFilesVolumePool.md
ms.openlocfilehash: 30d525ebcb7d80a24e11080ee265eb509f575ff6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98372737"
---
# <span data-ttu-id="ef6ca-101">Set-AzNetAppFilesVolumePool</span><span class="sxs-lookup"><span data-stu-id="ef6ca-101">Set-AzNetAppFilesVolumePool</span></span>

## <span data-ttu-id="ef6ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef6ca-102">SYNOPSIS</span></span>
<span data-ttu-id="ef6ca-103">ANF(Azure NetApp Files) 볼륨에 대한 풀을 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="ef6ca-103">Change pool for an Azure NetApp Files (ANF) volume.</span></span>

## <span data-ttu-id="ef6ca-104">구문</span><span class="sxs-lookup"><span data-stu-id="ef6ca-104">SYNTAX</span></span>

### <span data-ttu-id="ef6ca-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="ef6ca-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzNetAppFilesVolumePool -ResourceGroupName <String> -AccountName <String> -PoolName <String> -Name <String>
 [-NewPoolResourceId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ef6ca-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ef6ca-106">ByParentObjectParameterSet</span></span>
```
Set-AzNetAppFilesVolumePool -Name <String> -PoolObject <PSNetAppFilesPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef6ca-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ef6ca-107">ByResourceIdParameterSet</span></span>
```
Set-AzNetAppFilesVolumePool -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef6ca-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ef6ca-108">ByObjectParameterSet</span></span>
```
Set-AzNetAppFilesVolumePool -InputObject <PSNetAppFilesVolume> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef6ca-109">설명</span><span class="sxs-lookup"><span data-stu-id="ef6ca-109">DESCRIPTION</span></span>
<span data-ttu-id="ef6ca-110">**Set-AzNetAppFilesVolumePool** cmdlet은 ANF 볼륨의 풀을 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="ef6ca-110">The **Set-AzNetAppFilesVolumePool** cmdlet changes the pool of an ANF volume.</span></span>

## <span data-ttu-id="ef6ca-111">예제</span><span class="sxs-lookup"><span data-stu-id="ef6ca-111">EXAMPLES</span></span>

### <span data-ttu-id="ef6ca-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="ef6ca-112">Example 1</span></span>
```powershell
PS C:\>Set-AzNetAppFilesVolumePool -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -Name "MyAnfVolume" -NewPoolResourceId 7d6e4069-6c78-6c61-7bf6-c60968e45fbf
```

<span data-ttu-id="ef6ca-113">이렇게 하여 MyVolume 볼륨의 풀이 ID가 7d6e4069-6c78-6c61-7bf6-c60968e45fbf인 풀로 변경됩니다.</span><span class="sxs-lookup"><span data-stu-id="ef6ca-113">This changes the pool for the volume MyVolume to one with the Id of 7d6e4069-6c78-6c61-7bf6-c60968e45fbf</span></span>

## <span data-ttu-id="ef6ca-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ef6ca-114">PARAMETERS</span></span>

### <span data-ttu-id="ef6ca-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ef6ca-115">-AccountName</span></span>
<span data-ttu-id="ef6ca-116">ANF 계정의 이름</span><span class="sxs-lookup"><span data-stu-id="ef6ca-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="ef6ca-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef6ca-117">-DefaultProfile</span></span>
<span data-ttu-id="ef6ca-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ef6ca-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef6ca-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ef6ca-119">-InputObject</span></span>
<span data-ttu-id="ef6ca-120">이동할 볼륨 개체</span><span class="sxs-lookup"><span data-stu-id="ef6ca-120">The volume object to move</span></span>

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

### <span data-ttu-id="ef6ca-121">-Name</span><span class="sxs-lookup"><span data-stu-id="ef6ca-121">-Name</span></span>
<span data-ttu-id="ef6ca-122">ANF 볼륨의 이름</span><span class="sxs-lookup"><span data-stu-id="ef6ca-122">The name of the ANF volume</span></span>

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

### <span data-ttu-id="ef6ca-123">-NewPoolResourceId</span><span class="sxs-lookup"><span data-stu-id="ef6ca-123">-NewPoolResourceId</span></span>
<span data-ttu-id="ef6ca-124">이동할 용량 풀의 ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="ef6ca-124">ResourceId of the capacity pool to move to.</span></span>
<span data-ttu-id="ef6ca-125">풀을 식별하는 데 사용되는 UUID v4</span><span class="sxs-lookup"><span data-stu-id="ef6ca-125">UUID v4 used to identify the pool</span></span>

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

### <span data-ttu-id="ef6ca-126">-PoolName</span><span class="sxs-lookup"><span data-stu-id="ef6ca-126">-PoolName</span></span>
<span data-ttu-id="ef6ca-127">ANF 풀의 이름</span><span class="sxs-lookup"><span data-stu-id="ef6ca-127">The name of the ANF pool</span></span>

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

### <span data-ttu-id="ef6ca-128">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="ef6ca-128">-PoolObject</span></span>
<span data-ttu-id="ef6ca-129">볼륨을 포함하는 풀 개체</span><span class="sxs-lookup"><span data-stu-id="ef6ca-129">The pool object containing the volume</span></span>

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

### <span data-ttu-id="ef6ca-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef6ca-130">-ResourceGroupName</span></span>
<span data-ttu-id="ef6ca-131">ANF 볼륨의 리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="ef6ca-131">The resource group of the ANF volume</span></span>

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

### <span data-ttu-id="ef6ca-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ef6ca-132">-ResourceId</span></span>
<span data-ttu-id="ef6ca-133">ANF 볼륨의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="ef6ca-133">The resource id of the ANF volume</span></span>

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

### <span data-ttu-id="ef6ca-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ef6ca-134">-Confirm</span></span>
<span data-ttu-id="ef6ca-135">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ef6ca-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef6ca-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef6ca-136">-WhatIf</span></span>
<span data-ttu-id="ef6ca-137">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="ef6ca-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef6ca-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ef6ca-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef6ca-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef6ca-139">CommonParameters</span></span>
<span data-ttu-id="ef6ca-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ef6ca-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef6ca-141">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ef6ca-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef6ca-142">입력</span><span class="sxs-lookup"><span data-stu-id="ef6ca-142">INPUTS</span></span>

### <span data-ttu-id="ef6ca-143">System.String</span><span class="sxs-lookup"><span data-stu-id="ef6ca-143">System.String</span></span>

### <span data-ttu-id="ef6ca-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="ef6ca-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

### <span data-ttu-id="ef6ca-145">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="ef6ca-145">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="ef6ca-146">출력</span><span class="sxs-lookup"><span data-stu-id="ef6ca-146">OUTPUTS</span></span>

### <span data-ttu-id="ef6ca-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ef6ca-147">System.Boolean</span></span>

## <span data-ttu-id="ef6ca-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ef6ca-148">NOTES</span></span>

## <span data-ttu-id="ef6ca-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ef6ca-149">RELATED LINKS</span></span>
