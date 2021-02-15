---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/suspend-aznetappfilesreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Suspend-AzNetAppFilesReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Suspend-AzNetAppFilesReplication.md
ms.openlocfilehash: ab4d79b4770f438b233e5bfcc740e79364955ea6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184820"
---
# <span data-ttu-id="786a6-101">Suspend-AzNetAppFilesReplication</span><span class="sxs-lookup"><span data-stu-id="786a6-101">Suspend-AzNetAppFilesReplication</span></span>

## <span data-ttu-id="786a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="786a6-102">SYNOPSIS</span></span>
<span data-ttu-id="786a6-103">대상 볼륨에서 복제 연결을 일시 중단/중단합니다.</span><span class="sxs-lookup"><span data-stu-id="786a6-103">Suspend/break the replication connection on the destination volume</span></span>

## <span data-ttu-id="786a6-104">구문</span><span class="sxs-lookup"><span data-stu-id="786a6-104">SYNTAX</span></span>

### <span data-ttu-id="786a6-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="786a6-105">ByFieldsParameterSet (Default)</span></span>
```
Suspend-AzNetAppFilesReplication -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> [-ForceBreak] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="786a6-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="786a6-106">ByResourceIdParameterSet</span></span>
```
Suspend-AzNetAppFilesReplication -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="786a6-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="786a6-107">ByObjectParameterSet</span></span>
```
Suspend-AzNetAppFilesReplication -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="786a6-108">설명</span><span class="sxs-lookup"><span data-stu-id="786a6-108">DESCRIPTION</span></span>
<span data-ttu-id="786a6-109">대상 볼륨에서 복제 연결을 일시 중단/중단합니다.</span><span class="sxs-lookup"><span data-stu-id="786a6-109">Suspend/break the replication connection on the destination volume</span></span>

## <span data-ttu-id="786a6-110">예제</span><span class="sxs-lookup"><span data-stu-id="786a6-110">EXAMPLES</span></span>

### <span data-ttu-id="786a6-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="786a6-111">Example 1</span></span>
```powershell
PS C:\> Suspend-AnfReplication -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyDestinationAnfVolume"
```

<span data-ttu-id="786a6-112">이 명령은 "MyDestinationAnfVolume" 볼륨에서 ANF 복제 연결을 일시 중단합니다.</span><span class="sxs-lookup"><span data-stu-id="786a6-112">This command suspends the ANF Replication connection on volume "MyDestinationAnfVolume".</span></span>

## <span data-ttu-id="786a6-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="786a6-113">PARAMETERS</span></span>

### <span data-ttu-id="786a6-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="786a6-114">-AccountName</span></span>
<span data-ttu-id="786a6-115">복제 볼륨의 ANF 계정 이름</span><span class="sxs-lookup"><span data-stu-id="786a6-115">The name of the ANF account of the replication volume</span></span>

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

### <span data-ttu-id="786a6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="786a6-116">-DefaultProfile</span></span>
<span data-ttu-id="786a6-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="786a6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="786a6-118">-ForceBreak</span><span class="sxs-lookup"><span data-stu-id="786a6-118">-ForceBreak</span></span>
<span data-ttu-id="786a6-119">복제가 전송 중 상태인 경우 복제를 강제로 중단하려는 경우 true로 설정</span><span class="sxs-lookup"><span data-stu-id="786a6-119">If replication is in status transferring and you want to force break the replication, set to true</span></span>

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

### <span data-ttu-id="786a6-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="786a6-120">-InputObject</span></span>
<span data-ttu-id="786a6-121">중단할 복제가 있는 ANF 대상 볼륨 개체</span><span class="sxs-lookup"><span data-stu-id="786a6-121">The ANF destination volume object with the replication to break</span></span>

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

### <span data-ttu-id="786a6-122">-Name</span><span class="sxs-lookup"><span data-stu-id="786a6-122">-Name</span></span>
<span data-ttu-id="786a6-123">ANF 복제 대상 볼륨의 이름</span><span class="sxs-lookup"><span data-stu-id="786a6-123">The name of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="786a6-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="786a6-124">-PassThru</span></span>
<span data-ttu-id="786a6-125">지정된 볼륨 복제의 중단이 수행된 것인지 여부를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="786a6-125">Return whether the break of the specified volume replication was performed</span></span>

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

### <span data-ttu-id="786a6-126">-PoolName</span><span class="sxs-lookup"><span data-stu-id="786a6-126">-PoolName</span></span>
<span data-ttu-id="786a6-127">복제 볼륨의 ANF 풀 이름</span><span class="sxs-lookup"><span data-stu-id="786a6-127">The name of the ANF pool of the replication volume</span></span>

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

### <span data-ttu-id="786a6-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="786a6-128">-ResourceGroupName</span></span>
<span data-ttu-id="786a6-129">ANF 복제 대상 볼륨의 리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="786a6-129">The resource group of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="786a6-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="786a6-130">-ResourceId</span></span>
<span data-ttu-id="786a6-131">ANF 복제 대상 볼륨의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="786a6-131">The resource id of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="786a6-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="786a6-132">-Confirm</span></span>
<span data-ttu-id="786a6-133">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="786a6-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="786a6-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="786a6-134">-WhatIf</span></span>
<span data-ttu-id="786a6-135">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="786a6-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="786a6-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="786a6-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="786a6-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="786a6-137">CommonParameters</span></span>
<span data-ttu-id="786a6-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="786a6-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="786a6-139">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="786a6-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="786a6-140">입력</span><span class="sxs-lookup"><span data-stu-id="786a6-140">INPUTS</span></span>

### <span data-ttu-id="786a6-141">System.String</span><span class="sxs-lookup"><span data-stu-id="786a6-141">System.String</span></span>

### <span data-ttu-id="786a6-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="786a6-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="786a6-143">출력</span><span class="sxs-lookup"><span data-stu-id="786a6-143">OUTPUTS</span></span>

### <span data-ttu-id="786a6-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="786a6-144">System.Boolean</span></span>

## <span data-ttu-id="786a6-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="786a6-145">NOTES</span></span>

## <span data-ttu-id="786a6-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="786a6-146">RELATED LINKS</span></span>
