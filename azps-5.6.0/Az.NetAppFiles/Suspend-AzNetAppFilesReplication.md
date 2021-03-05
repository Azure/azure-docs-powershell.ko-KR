---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/suspend-aznetappfilesreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Suspend-AzNetAppFilesReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Suspend-AzNetAppFilesReplication.md
ms.openlocfilehash: 198ec8c67939c3ae01a52f2a9b06982ce8ee8d93
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968171"
---
# <span data-ttu-id="ada18-101">Suspend-AzNetAppFilesReplication</span><span class="sxs-lookup"><span data-stu-id="ada18-101">Suspend-AzNetAppFilesReplication</span></span>

## <span data-ttu-id="ada18-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ada18-102">SYNOPSIS</span></span>
<span data-ttu-id="ada18-103">대상 볼륨에서 복제 연결을 일시 중단/중단합니다.</span><span class="sxs-lookup"><span data-stu-id="ada18-103">Suspend/break the replication connection on the destination volume</span></span>

## <span data-ttu-id="ada18-104">구문</span><span class="sxs-lookup"><span data-stu-id="ada18-104">SYNTAX</span></span>

### <span data-ttu-id="ada18-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="ada18-105">ByFieldsParameterSet (Default)</span></span>
```
Suspend-AzNetAppFilesReplication -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> [-ForceBreak] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ada18-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ada18-106">ByResourceIdParameterSet</span></span>
```
Suspend-AzNetAppFilesReplication -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ada18-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ada18-107">ByObjectParameterSet</span></span>
```
Suspend-AzNetAppFilesReplication -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ada18-108">설명</span><span class="sxs-lookup"><span data-stu-id="ada18-108">DESCRIPTION</span></span>
<span data-ttu-id="ada18-109">대상 볼륨에서 복제 연결을 일시 중단/중단합니다.</span><span class="sxs-lookup"><span data-stu-id="ada18-109">Suspend/break the replication connection on the destination volume</span></span>

## <span data-ttu-id="ada18-110">예제</span><span class="sxs-lookup"><span data-stu-id="ada18-110">EXAMPLES</span></span>

### <span data-ttu-id="ada18-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="ada18-111">Example 1</span></span>
```powershell
PS C:\> Suspend-AnfReplication -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyDestinationAnfVolume"
```

<span data-ttu-id="ada18-112">이 명령은 볼륨 "MyDestinationAnfVolume"에서 ANF 복제 연결을 일시 중단합니다.</span><span class="sxs-lookup"><span data-stu-id="ada18-112">This command suspends the ANF Replication connection on volume "MyDestinationAnfVolume".</span></span>

## <span data-ttu-id="ada18-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="ada18-113">PARAMETERS</span></span>

### <span data-ttu-id="ada18-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ada18-114">-AccountName</span></span>
<span data-ttu-id="ada18-115">복제 볼륨의 ANF 계정 이름</span><span class="sxs-lookup"><span data-stu-id="ada18-115">The name of the ANF account of the replication volume</span></span>

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

### <span data-ttu-id="ada18-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ada18-116">-DefaultProfile</span></span>
<span data-ttu-id="ada18-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ada18-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ada18-118">-ForceBreak</span><span class="sxs-lookup"><span data-stu-id="ada18-118">-ForceBreak</span></span>
<span data-ttu-id="ada18-119">복제가 상태 전송 중이면 복제를 강제로 중단하려는 경우 true로 설정</span><span class="sxs-lookup"><span data-stu-id="ada18-119">If replication is in status transferring and you want to force break the replication, set to true</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ada18-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ada18-120">-InputObject</span></span>
<span data-ttu-id="ada18-121">중단할 복제가 있는 ANF 대상 볼륨 개체</span><span class="sxs-lookup"><span data-stu-id="ada18-121">The ANF destination volume object with the replication to break</span></span>

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

### <span data-ttu-id="ada18-122">-Name</span><span class="sxs-lookup"><span data-stu-id="ada18-122">-Name</span></span>
<span data-ttu-id="ada18-123">ANF 복제 대상 볼륨의 이름</span><span class="sxs-lookup"><span data-stu-id="ada18-123">The name of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="ada18-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ada18-124">-PassThru</span></span>
<span data-ttu-id="ada18-125">지정된 볼륨 복제 중단이 수행된지 여부를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="ada18-125">Return whether the break of the specified volume replication was performed</span></span>

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

### <span data-ttu-id="ada18-126">-PoolName</span><span class="sxs-lookup"><span data-stu-id="ada18-126">-PoolName</span></span>
<span data-ttu-id="ada18-127">복제 볼륨의 ANF 풀 이름</span><span class="sxs-lookup"><span data-stu-id="ada18-127">The name of the ANF pool of the replication volume</span></span>

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

### <span data-ttu-id="ada18-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ada18-128">-ResourceGroupName</span></span>
<span data-ttu-id="ada18-129">ANF 복제 대상 볼륨의 리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="ada18-129">The resource group of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="ada18-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ada18-130">-ResourceId</span></span>
<span data-ttu-id="ada18-131">ANF 복제 대상 볼륨의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="ada18-131">The resource id of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="ada18-132">-확인</span><span class="sxs-lookup"><span data-stu-id="ada18-132">-Confirm</span></span>
<span data-ttu-id="ada18-133">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ada18-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ada18-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ada18-134">-WhatIf</span></span>
<span data-ttu-id="ada18-135">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="ada18-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ada18-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ada18-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ada18-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ada18-137">CommonParameters</span></span>
<span data-ttu-id="ada18-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ada18-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ada18-139">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ada18-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ada18-140">입력</span><span class="sxs-lookup"><span data-stu-id="ada18-140">INPUTS</span></span>

### <span data-ttu-id="ada18-141">System.String</span><span class="sxs-lookup"><span data-stu-id="ada18-141">System.String</span></span>

### <span data-ttu-id="ada18-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="ada18-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="ada18-143">출력</span><span class="sxs-lookup"><span data-stu-id="ada18-143">OUTPUTS</span></span>

### <span data-ttu-id="ada18-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ada18-144">System.Boolean</span></span>

## <span data-ttu-id="ada18-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ada18-145">NOTES</span></span>

## <span data-ttu-id="ada18-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ada18-146">RELATED LINKS</span></span>
