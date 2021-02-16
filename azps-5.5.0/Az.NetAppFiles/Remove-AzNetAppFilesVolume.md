---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesVolume.md
ms.openlocfilehash: 9400efa61a98b6eb80b975d4999e03eb872e3b28
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187268"
---
# <span data-ttu-id="7cfff-101">Remove-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="7cfff-101">Remove-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="7cfff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7cfff-102">SYNOPSIS</span></span>
<span data-ttu-id="7cfff-103">ANF(Azure NetApp Files) 볼륨을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="7cfff-103">Deletes an Azure NetApp Files (ANF) volume.</span></span>

## <span data-ttu-id="7cfff-104">구문</span><span class="sxs-lookup"><span data-stu-id="7cfff-104">SYNTAX</span></span>

### <span data-ttu-id="7cfff-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="7cfff-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesVolume -ResourceGroupName <String> -AccountName <String> -PoolName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7cfff-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7cfff-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesVolume -Name <String> -PoolObject <PSNetAppFilesPool> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7cfff-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7cfff-107">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesVolume -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7cfff-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7cfff-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesVolume -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7cfff-109">설명</span><span class="sxs-lookup"><span data-stu-id="7cfff-109">DESCRIPTION</span></span>
<span data-ttu-id="7cfff-110">**Remove-AzNetAppFilesVolume** cmdlet은 ANF 볼륨을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="7cfff-110">The **Remove-AzNetAppFilesVolume** cmdlet deletes an ANF volume.</span></span>

## <span data-ttu-id="7cfff-111">예제</span><span class="sxs-lookup"><span data-stu-id="7cfff-111">EXAMPLES</span></span>

### <span data-ttu-id="7cfff-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="7cfff-112">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesVolume -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -Name "MyAnfVolume"
```

<span data-ttu-id="7cfff-113">이 명령은 ANF 볼륨 "MyAnfVolume"을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="7cfff-113">This command deletes the ANF volume "MyAnfVolume".</span></span>

## <span data-ttu-id="7cfff-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7cfff-114">PARAMETERS</span></span>

### <span data-ttu-id="7cfff-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="7cfff-115">-AccountName</span></span>
<span data-ttu-id="7cfff-116">ANF 계정의 이름</span><span class="sxs-lookup"><span data-stu-id="7cfff-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="7cfff-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cfff-117">-DefaultProfile</span></span>
<span data-ttu-id="7cfff-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7cfff-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7cfff-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7cfff-119">-InputObject</span></span>
<span data-ttu-id="7cfff-120">제거할 볼륨 개체</span><span class="sxs-lookup"><span data-stu-id="7cfff-120">The volume object to remove</span></span>

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

### <span data-ttu-id="7cfff-121">-Name</span><span class="sxs-lookup"><span data-stu-id="7cfff-121">-Name</span></span>
<span data-ttu-id="7cfff-122">ANF 볼륨의 이름</span><span class="sxs-lookup"><span data-stu-id="7cfff-122">The name of the ANF volume</span></span>

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

### <span data-ttu-id="7cfff-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7cfff-123">-PassThru</span></span>
<span data-ttu-id="7cfff-124">지정된 볼륨이 성공적으로 제거됐는지 여부를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="7cfff-124">Return whether the specified volume was successfully removed</span></span>

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

### <span data-ttu-id="7cfff-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="7cfff-125">-PoolName</span></span>
<span data-ttu-id="7cfff-126">ANF 풀의 이름</span><span class="sxs-lookup"><span data-stu-id="7cfff-126">The name of the ANF pool</span></span>

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

### <span data-ttu-id="7cfff-127">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="7cfff-127">-PoolObject</span></span>
<span data-ttu-id="7cfff-128">제거할 볼륨을 포함하는 풀 개체</span><span class="sxs-lookup"><span data-stu-id="7cfff-128">The pool object containing the volume to remove</span></span>

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

### <span data-ttu-id="7cfff-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7cfff-129">-ResourceGroupName</span></span>
<span data-ttu-id="7cfff-130">ANF 볼륨의 리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="7cfff-130">The resource group of the ANF volume</span></span>

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

### <span data-ttu-id="7cfff-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7cfff-131">-ResourceId</span></span>
<span data-ttu-id="7cfff-132">ANF 볼륨의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="7cfff-132">The resource id of the ANF volume</span></span>

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

### <span data-ttu-id="7cfff-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7cfff-133">-Confirm</span></span>
<span data-ttu-id="7cfff-134">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7cfff-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7cfff-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7cfff-135">-WhatIf</span></span>
<span data-ttu-id="7cfff-136">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="7cfff-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7cfff-137">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7cfff-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7cfff-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cfff-138">CommonParameters</span></span>
<span data-ttu-id="7cfff-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7cfff-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cfff-140">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7cfff-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cfff-141">입력</span><span class="sxs-lookup"><span data-stu-id="7cfff-141">INPUTS</span></span>

### <span data-ttu-id="7cfff-142">System.String</span><span class="sxs-lookup"><span data-stu-id="7cfff-142">System.String</span></span>

### <span data-ttu-id="7cfff-143">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="7cfff-143">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

### <span data-ttu-id="7cfff-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="7cfff-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="7cfff-145">출력</span><span class="sxs-lookup"><span data-stu-id="7cfff-145">OUTPUTS</span></span>

### <span data-ttu-id="7cfff-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7cfff-146">System.Boolean</span></span>

## <span data-ttu-id="7cfff-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7cfff-147">NOTES</span></span>

## <span data-ttu-id="7cfff-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7cfff-148">RELATED LINKS</span></span>
