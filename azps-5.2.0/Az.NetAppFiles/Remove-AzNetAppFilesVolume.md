---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesVolume.md
ms.openlocfilehash: 9400efa61a98b6eb80b975d4999e03eb872e3b28
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98361103"
---
# <span data-ttu-id="65e98-101">Remove-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="65e98-101">Remove-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="65e98-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65e98-102">SYNOPSIS</span></span>
<span data-ttu-id="65e98-103">ANF(Azure NetApp Files) 볼륨을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="65e98-103">Deletes an Azure NetApp Files (ANF) volume.</span></span>

## <span data-ttu-id="65e98-104">구문</span><span class="sxs-lookup"><span data-stu-id="65e98-104">SYNTAX</span></span>

### <span data-ttu-id="65e98-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="65e98-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesVolume -ResourceGroupName <String> -AccountName <String> -PoolName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65e98-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="65e98-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesVolume -Name <String> -PoolObject <PSNetAppFilesPool> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65e98-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="65e98-107">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesVolume -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65e98-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="65e98-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesVolume -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65e98-109">설명</span><span class="sxs-lookup"><span data-stu-id="65e98-109">DESCRIPTION</span></span>
<span data-ttu-id="65e98-110">**Remove-AzNetAppFilesVolume** cmdlet은 ANF 볼륨을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="65e98-110">The **Remove-AzNetAppFilesVolume** cmdlet deletes an ANF volume.</span></span>

## <span data-ttu-id="65e98-111">예제</span><span class="sxs-lookup"><span data-stu-id="65e98-111">EXAMPLES</span></span>

### <span data-ttu-id="65e98-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="65e98-112">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesVolume -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -Name "MyAnfVolume"
```

<span data-ttu-id="65e98-113">이 명령은 ANF 볼륨 "MyAnfVolume"을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="65e98-113">This command deletes the ANF volume "MyAnfVolume".</span></span>

## <span data-ttu-id="65e98-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="65e98-114">PARAMETERS</span></span>

### <span data-ttu-id="65e98-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="65e98-115">-AccountName</span></span>
<span data-ttu-id="65e98-116">ANF 계정의 이름</span><span class="sxs-lookup"><span data-stu-id="65e98-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="65e98-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65e98-117">-DefaultProfile</span></span>
<span data-ttu-id="65e98-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="65e98-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65e98-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="65e98-119">-InputObject</span></span>
<span data-ttu-id="65e98-120">제거할 볼륨 개체</span><span class="sxs-lookup"><span data-stu-id="65e98-120">The volume object to remove</span></span>

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

### <span data-ttu-id="65e98-121">-Name</span><span class="sxs-lookup"><span data-stu-id="65e98-121">-Name</span></span>
<span data-ttu-id="65e98-122">ANF 볼륨의 이름</span><span class="sxs-lookup"><span data-stu-id="65e98-122">The name of the ANF volume</span></span>

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

### <span data-ttu-id="65e98-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="65e98-123">-PassThru</span></span>
<span data-ttu-id="65e98-124">지정된 볼륨이 성공적으로 제거됐는지 여부를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="65e98-124">Return whether the specified volume was successfully removed</span></span>

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

### <span data-ttu-id="65e98-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="65e98-125">-PoolName</span></span>
<span data-ttu-id="65e98-126">ANF 풀의 이름</span><span class="sxs-lookup"><span data-stu-id="65e98-126">The name of the ANF pool</span></span>

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

### <span data-ttu-id="65e98-127">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="65e98-127">-PoolObject</span></span>
<span data-ttu-id="65e98-128">제거할 볼륨을 포함하는 풀 개체</span><span class="sxs-lookup"><span data-stu-id="65e98-128">The pool object containing the volume to remove</span></span>

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

### <span data-ttu-id="65e98-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65e98-129">-ResourceGroupName</span></span>
<span data-ttu-id="65e98-130">ANF 볼륨의 리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="65e98-130">The resource group of the ANF volume</span></span>

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

### <span data-ttu-id="65e98-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="65e98-131">-ResourceId</span></span>
<span data-ttu-id="65e98-132">ANF 볼륨의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="65e98-132">The resource id of the ANF volume</span></span>

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

### <span data-ttu-id="65e98-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="65e98-133">-Confirm</span></span>
<span data-ttu-id="65e98-134">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="65e98-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65e98-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65e98-135">-WhatIf</span></span>
<span data-ttu-id="65e98-136">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="65e98-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65e98-137">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="65e98-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65e98-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65e98-138">CommonParameters</span></span>
<span data-ttu-id="65e98-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="65e98-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65e98-140">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="65e98-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65e98-141">입력</span><span class="sxs-lookup"><span data-stu-id="65e98-141">INPUTS</span></span>

### <span data-ttu-id="65e98-142">System.String</span><span class="sxs-lookup"><span data-stu-id="65e98-142">System.String</span></span>

### <span data-ttu-id="65e98-143">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="65e98-143">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

### <span data-ttu-id="65e98-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="65e98-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="65e98-145">출력</span><span class="sxs-lookup"><span data-stu-id="65e98-145">OUTPUTS</span></span>

### <span data-ttu-id="65e98-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="65e98-146">System.Boolean</span></span>

## <span data-ttu-id="65e98-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="65e98-147">NOTES</span></span>

## <span data-ttu-id="65e98-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="65e98-148">RELATED LINKS</span></span>
