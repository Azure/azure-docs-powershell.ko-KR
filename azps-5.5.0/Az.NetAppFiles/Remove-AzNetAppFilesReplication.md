---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilesreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesReplication.md
ms.openlocfilehash: 04ad7f188a2280dcdf84e8b5c1f45e20edf4d07b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179972"
---
# <span data-ttu-id="9a1de-101">Remove-AzNetAppFilesReplication</span><span class="sxs-lookup"><span data-stu-id="9a1de-101">Remove-AzNetAppFilesReplication</span></span>

## <span data-ttu-id="9a1de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a1de-102">SYNOPSIS</span></span>
<span data-ttu-id="9a1de-103">대상 볼륨에서 복제 연결을 제거/삭제하고 원본 복제로 릴리스 보내기</span><span class="sxs-lookup"><span data-stu-id="9a1de-103">Remove/Delete the replication connection on the destination volume, and send release to the source replication</span></span>

## <span data-ttu-id="9a1de-104">구문</span><span class="sxs-lookup"><span data-stu-id="9a1de-104">SYNTAX</span></span>

### <span data-ttu-id="9a1de-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="9a1de-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesReplication -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9a1de-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a1de-106">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesReplication -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a1de-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a1de-107">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesReplication -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a1de-108">설명</span><span class="sxs-lookup"><span data-stu-id="9a1de-108">DESCRIPTION</span></span>
<span data-ttu-id="9a1de-109">대상 볼륨에서 복제 연결을 제거/삭제하고 원본 복제로 릴리스 보내기</span><span class="sxs-lookup"><span data-stu-id="9a1de-109">Remove/Delete the replication connection on the destination volume, and send release to the source replication</span></span>

## <span data-ttu-id="9a1de-110">예제</span><span class="sxs-lookup"><span data-stu-id="9a1de-110">EXAMPLES</span></span>

### <span data-ttu-id="9a1de-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="9a1de-111">Example 1</span></span>
```powershell
PS C:\> Remove-AnfReplication -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyDestinationAnfVolume"
```

<span data-ttu-id="9a1de-112">이 명령은 볼륨 "MyDestinationAnfVolume"에서 ANF 복제 연결을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="9a1de-112">This command removes the ANF Replication connection on volume "MyDestinationAnfVolume".</span></span>

## <span data-ttu-id="9a1de-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9a1de-113">PARAMETERS</span></span>

### <span data-ttu-id="9a1de-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="9a1de-114">-AccountName</span></span>
<span data-ttu-id="9a1de-115">복제 볼륨의 ANF 계정 이름</span><span class="sxs-lookup"><span data-stu-id="9a1de-115">The name of the ANF account of the replication volume</span></span>

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

### <span data-ttu-id="9a1de-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a1de-116">-DefaultProfile</span></span>
<span data-ttu-id="9a1de-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9a1de-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a1de-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9a1de-118">-InputObject</span></span>
<span data-ttu-id="9a1de-119">제거할 복제가 있는 ANF 대상 볼륨</span><span class="sxs-lookup"><span data-stu-id="9a1de-119">The ANF destination volume with the replication to remove</span></span>

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

### <span data-ttu-id="9a1de-120">-Name</span><span class="sxs-lookup"><span data-stu-id="9a1de-120">-Name</span></span>
<span data-ttu-id="9a1de-121">ANF 복제 대상 볼륨의 이름</span><span class="sxs-lookup"><span data-stu-id="9a1de-121">The name of the ANF replication destination volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: VolumeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a1de-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9a1de-122">-PassThru</span></span>
<span data-ttu-id="9a1de-123">지정된 ANF 복제가 성공적으로 제거됐는지 여부를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="9a1de-123">Return whether the specified ANF replication was successfully removed</span></span>

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

### <span data-ttu-id="9a1de-124">-PoolName</span><span class="sxs-lookup"><span data-stu-id="9a1de-124">-PoolName</span></span>
<span data-ttu-id="9a1de-125">복제 볼륨의 ANF 풀 이름</span><span class="sxs-lookup"><span data-stu-id="9a1de-125">The name of the ANF pool of the replication volume</span></span>

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

### <span data-ttu-id="9a1de-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a1de-126">-ResourceGroupName</span></span>
<span data-ttu-id="9a1de-127">ANF 복제 대상 볼륨의 리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="9a1de-127">The resource group of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="9a1de-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9a1de-128">-ResourceId</span></span>
<span data-ttu-id="9a1de-129">ANF 복제 대상 볼륨의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="9a1de-129">The resource id of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="9a1de-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9a1de-130">-Confirm</span></span>
<span data-ttu-id="9a1de-131">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="9a1de-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a1de-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a1de-132">-WhatIf</span></span>
<span data-ttu-id="9a1de-133">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="9a1de-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a1de-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9a1de-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a1de-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a1de-135">CommonParameters</span></span>
<span data-ttu-id="9a1de-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9a1de-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a1de-137">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9a1de-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a1de-138">입력</span><span class="sxs-lookup"><span data-stu-id="9a1de-138">INPUTS</span></span>

### <span data-ttu-id="9a1de-139">System.String</span><span class="sxs-lookup"><span data-stu-id="9a1de-139">System.String</span></span>

### <span data-ttu-id="9a1de-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="9a1de-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="9a1de-141">출력</span><span class="sxs-lookup"><span data-stu-id="9a1de-141">OUTPUTS</span></span>

### <span data-ttu-id="9a1de-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9a1de-142">System.Boolean</span></span>

## <span data-ttu-id="9a1de-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9a1de-143">NOTES</span></span>

## <span data-ttu-id="9a1de-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9a1de-144">RELATED LINKS</span></span>
