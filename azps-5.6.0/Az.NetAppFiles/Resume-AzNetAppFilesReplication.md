---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/resume-aznetappfilesreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Resume-AzNetAppFilesReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Resume-AzNetAppFilesReplication.md
ms.openlocfilehash: 5f5dac2f2028de9b90941ef91c38361c4357fc8d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968235"
---
# <span data-ttu-id="0c921-101">Resume-AzNetAppFilesReplication</span><span class="sxs-lookup"><span data-stu-id="0c921-101">Resume-AzNetAppFilesReplication</span></span>

## <span data-ttu-id="0c921-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c921-102">SYNOPSIS</span></span>
<span data-ttu-id="0c921-103">대상 볼륨에서 연결을 다시 시작/다시 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="0c921-103">Resume/Resync the connection on the destination volume.</span></span> <span data-ttu-id="0c921-104">작업이 원본 볼륨에서 런된 경우 연결을 역방향으로 다시 동기화하고 원본에서 대상으로 동기화합니다.</span><span class="sxs-lookup"><span data-stu-id="0c921-104">If the operation is ran on the source volume it will reverse-resync the connection and sync from source to destination.</span></span>

## <span data-ttu-id="0c921-105">구문</span><span class="sxs-lookup"><span data-stu-id="0c921-105">SYNTAX</span></span>

### <span data-ttu-id="0c921-106">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="0c921-106">ByFieldsParameterSet (Default)</span></span>
```
Resume-AzNetAppFilesReplication -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0c921-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c921-107">ByResourceIdParameterSet</span></span>
```
Resume-AzNetAppFilesReplication -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c921-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c921-108">ByObjectParameterSet</span></span>
```
Resume-AzNetAppFilesReplication -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c921-109">설명</span><span class="sxs-lookup"><span data-stu-id="0c921-109">DESCRIPTION</span></span>
<span data-ttu-id="0c921-110">대상 볼륨의 연결을 다시 시작/다시 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="0c921-110">Resume/Resync the connection on the destination volume</span></span>

## <span data-ttu-id="0c921-111">예제</span><span class="sxs-lookup"><span data-stu-id="0c921-111">EXAMPLES</span></span>

### <span data-ttu-id="0c921-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="0c921-112">Example 1</span></span>
```powershell
PS C:\> Resume-AnfReplication -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyDestinationAnfVolume"
```

<span data-ttu-id="0c921-113">이 명령은 볼륨 "MyDestinationAnfVolume"에서 ANF 복제 연결을 다시 시작됩니다.</span><span class="sxs-lookup"><span data-stu-id="0c921-113">This command resumes the ANF Replication connection on volume "MyDestinationAnfVolume".</span></span>

## <span data-ttu-id="0c921-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="0c921-114">PARAMETERS</span></span>

### <span data-ttu-id="0c921-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="0c921-115">-AccountName</span></span>
<span data-ttu-id="0c921-116">복제 볼륨의 ANF 계정 이름</span><span class="sxs-lookup"><span data-stu-id="0c921-116">The name of the ANF account of the replication volume</span></span>

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

### <span data-ttu-id="0c921-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c921-117">-DefaultProfile</span></span>
<span data-ttu-id="0c921-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0c921-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c921-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0c921-119">-InputObject</span></span>
<span data-ttu-id="0c921-120">재동기할 ANF 복제 대상 볼륨 개체</span><span class="sxs-lookup"><span data-stu-id="0c921-120">The ANF replication destination volume object to resync</span></span>

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

### <span data-ttu-id="0c921-121">-Name</span><span class="sxs-lookup"><span data-stu-id="0c921-121">-Name</span></span>
<span data-ttu-id="0c921-122">ANF 복제 대상 볼륨의 이름</span><span class="sxs-lookup"><span data-stu-id="0c921-122">The name of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="0c921-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0c921-123">-PassThru</span></span>
<span data-ttu-id="0c921-124">지정된 복제 볼륨의 재동기 수행 여부를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="0c921-124">Return whether resync of the specified replication volume was performed</span></span>

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

### <span data-ttu-id="0c921-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="0c921-125">-PoolName</span></span>
<span data-ttu-id="0c921-126">복제 볼륨의 ANF 풀 이름</span><span class="sxs-lookup"><span data-stu-id="0c921-126">The name of the ANF pool of the replication volume</span></span>

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

### <span data-ttu-id="0c921-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c921-127">-ResourceGroupName</span></span>
<span data-ttu-id="0c921-128">ANF 복제 대상 볼륨의 리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="0c921-128">The resource group of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="0c921-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0c921-129">-ResourceId</span></span>
<span data-ttu-id="0c921-130">ANF 복제 대상 볼륨의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="0c921-130">The resource id of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="0c921-131">-확인</span><span class="sxs-lookup"><span data-stu-id="0c921-131">-Confirm</span></span>
<span data-ttu-id="0c921-132">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="0c921-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c921-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c921-133">-WhatIf</span></span>
<span data-ttu-id="0c921-134">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="0c921-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c921-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0c921-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c921-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c921-136">CommonParameters</span></span>
<span data-ttu-id="0c921-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0c921-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c921-138">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0c921-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c921-139">입력</span><span class="sxs-lookup"><span data-stu-id="0c921-139">INPUTS</span></span>

### <span data-ttu-id="0c921-140">System.String</span><span class="sxs-lookup"><span data-stu-id="0c921-140">System.String</span></span>

### <span data-ttu-id="0c921-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="0c921-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="0c921-142">출력</span><span class="sxs-lookup"><span data-stu-id="0c921-142">OUTPUTS</span></span>

### <span data-ttu-id="0c921-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0c921-143">System.Boolean</span></span>

## <span data-ttu-id="0c921-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0c921-144">NOTES</span></span>

## <span data-ttu-id="0c921-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0c921-145">RELATED LINKS</span></span>
