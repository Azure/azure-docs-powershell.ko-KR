---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/remove-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesVolume.md
ms.openlocfilehash: f53ca76da23620a37020a14877059aae4f4c9808
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968267"
---
# <span data-ttu-id="9fbbf-101">Remove-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="9fbbf-101">Remove-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="9fbbf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9fbbf-102">SYNOPSIS</span></span>
<span data-ttu-id="9fbbf-103">ANF(Azure NetApp Files) 볼륨을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="9fbbf-103">Deletes an Azure NetApp Files (ANF) volume.</span></span>

## <span data-ttu-id="9fbbf-104">구문</span><span class="sxs-lookup"><span data-stu-id="9fbbf-104">SYNTAX</span></span>

### <span data-ttu-id="9fbbf-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="9fbbf-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesVolume -ResourceGroupName <String> -AccountName <String> -PoolName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9fbbf-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9fbbf-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesVolume -Name <String> -PoolObject <PSNetAppFilesPool> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9fbbf-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9fbbf-107">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesVolume -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9fbbf-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9fbbf-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesVolume -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9fbbf-109">설명</span><span class="sxs-lookup"><span data-stu-id="9fbbf-109">DESCRIPTION</span></span>
<span data-ttu-id="9fbbf-110">**Remove-AzNetAppFilesVolume** cmdlet은 ANF 볼륨을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="9fbbf-110">The **Remove-AzNetAppFilesVolume** cmdlet deletes an ANF volume.</span></span>

## <span data-ttu-id="9fbbf-111">예제</span><span class="sxs-lookup"><span data-stu-id="9fbbf-111">EXAMPLES</span></span>

### <span data-ttu-id="9fbbf-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="9fbbf-112">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesVolume -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -Name "MyAnfVolume"
```

<span data-ttu-id="9fbbf-113">이 명령은 ANF 볼륨 "MyAnfVolume"을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="9fbbf-113">This command deletes the ANF volume "MyAnfVolume".</span></span>

## <span data-ttu-id="9fbbf-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="9fbbf-114">PARAMETERS</span></span>

### <span data-ttu-id="9fbbf-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="9fbbf-115">-AccountName</span></span>
<span data-ttu-id="9fbbf-116">ANF 계정의 이름</span><span class="sxs-lookup"><span data-stu-id="9fbbf-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="9fbbf-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fbbf-117">-DefaultProfile</span></span>
<span data-ttu-id="9fbbf-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9fbbf-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9fbbf-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9fbbf-119">-InputObject</span></span>
<span data-ttu-id="9fbbf-120">제거할 볼륨 개체</span><span class="sxs-lookup"><span data-stu-id="9fbbf-120">The volume object to remove</span></span>

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

### <span data-ttu-id="9fbbf-121">-Name</span><span class="sxs-lookup"><span data-stu-id="9fbbf-121">-Name</span></span>
<span data-ttu-id="9fbbf-122">ANF 볼륨의 이름</span><span class="sxs-lookup"><span data-stu-id="9fbbf-122">The name of the ANF volume</span></span>

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

### <span data-ttu-id="9fbbf-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9fbbf-123">-PassThru</span></span>
<span data-ttu-id="9fbbf-124">지정된 볼륨이 성공적으로 제거된지 여부를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="9fbbf-124">Return whether the specified volume was successfully removed</span></span>

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

### <span data-ttu-id="9fbbf-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="9fbbf-125">-PoolName</span></span>
<span data-ttu-id="9fbbf-126">ANF 풀의 이름</span><span class="sxs-lookup"><span data-stu-id="9fbbf-126">The name of the ANF pool</span></span>

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

### <span data-ttu-id="9fbbf-127">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="9fbbf-127">-PoolObject</span></span>
<span data-ttu-id="9fbbf-128">제거할 볼륨이 포함된 풀 개체</span><span class="sxs-lookup"><span data-stu-id="9fbbf-128">The pool object containing the volume to remove</span></span>

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

### <span data-ttu-id="9fbbf-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9fbbf-129">-ResourceGroupName</span></span>
<span data-ttu-id="9fbbf-130">ANF 볼륨의 리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="9fbbf-130">The resource group of the ANF volume</span></span>

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

### <span data-ttu-id="9fbbf-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9fbbf-131">-ResourceId</span></span>
<span data-ttu-id="9fbbf-132">ANF 볼륨의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="9fbbf-132">The resource id of the ANF volume</span></span>

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

### <span data-ttu-id="9fbbf-133">-확인</span><span class="sxs-lookup"><span data-stu-id="9fbbf-133">-Confirm</span></span>
<span data-ttu-id="9fbbf-134">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="9fbbf-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9fbbf-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9fbbf-135">-WhatIf</span></span>
<span data-ttu-id="9fbbf-136">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="9fbbf-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9fbbf-137">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9fbbf-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9fbbf-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fbbf-138">CommonParameters</span></span>
<span data-ttu-id="9fbbf-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9fbbf-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fbbf-140">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9fbbf-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fbbf-141">입력</span><span class="sxs-lookup"><span data-stu-id="9fbbf-141">INPUTS</span></span>

### <span data-ttu-id="9fbbf-142">System.String</span><span class="sxs-lookup"><span data-stu-id="9fbbf-142">System.String</span></span>

### <span data-ttu-id="9fbbf-143">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="9fbbf-143">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

### <span data-ttu-id="9fbbf-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="9fbbf-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="9fbbf-145">출력</span><span class="sxs-lookup"><span data-stu-id="9fbbf-145">OUTPUTS</span></span>

### <span data-ttu-id="9fbbf-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9fbbf-146">System.Boolean</span></span>

## <span data-ttu-id="9fbbf-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9fbbf-147">NOTES</span></span>

## <span data-ttu-id="9fbbf-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9fbbf-148">RELATED LINKS</span></span>
