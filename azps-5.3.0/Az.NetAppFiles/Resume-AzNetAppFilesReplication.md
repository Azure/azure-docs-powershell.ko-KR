---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/resume-aznetappfilesreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Resume-AzNetAppFilesReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Resume-AzNetAppFilesReplication.md
ms.openlocfilehash: 95ed2dc354f32229727a3d1b13dbfdfb95fe001a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98380535"
---
# <span data-ttu-id="2717d-101">Resume-AzNetAppFilesReplication</span><span class="sxs-lookup"><span data-stu-id="2717d-101">Resume-AzNetAppFilesReplication</span></span>

## <span data-ttu-id="2717d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2717d-102">SYNOPSIS</span></span>
<span data-ttu-id="2717d-103">대상 볼륨에서 연결을 다시 시작/다시 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="2717d-103">Resume/Resync the connection on the destination volume.</span></span> <span data-ttu-id="2717d-104">작업이 원본 볼륨에서 수행된 경우 연결을 역방향으로 다시 동기화하고 원본에서 대상으로 동기화합니다.</span><span class="sxs-lookup"><span data-stu-id="2717d-104">If the operation is ran on the source volume it will reverse-resync the connection and sync from source to destination.</span></span>

## <span data-ttu-id="2717d-105">구문</span><span class="sxs-lookup"><span data-stu-id="2717d-105">SYNTAX</span></span>

### <span data-ttu-id="2717d-106">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="2717d-106">ByFieldsParameterSet (Default)</span></span>
```
Resume-AzNetAppFilesReplication -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2717d-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2717d-107">ByResourceIdParameterSet</span></span>
```
Resume-AzNetAppFilesReplication -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2717d-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2717d-108">ByObjectParameterSet</span></span>
```
Resume-AzNetAppFilesReplication -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2717d-109">설명</span><span class="sxs-lookup"><span data-stu-id="2717d-109">DESCRIPTION</span></span>
<span data-ttu-id="2717d-110">대상 볼륨에서 연결을 다시 시작/다시 연결</span><span class="sxs-lookup"><span data-stu-id="2717d-110">Resume/Resync the connection on the destination volume</span></span>

## <span data-ttu-id="2717d-111">예제</span><span class="sxs-lookup"><span data-stu-id="2717d-111">EXAMPLES</span></span>

### <span data-ttu-id="2717d-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="2717d-112">Example 1</span></span>
```powershell
PS C:\> Resume-AnfReplication -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyDestinationAnfVolume"
```

<span data-ttu-id="2717d-113">이 명령은 볼륨 "MyDestinationAnfVolume"에서 ANF 복제 연결을 다시 시작됩니다.</span><span class="sxs-lookup"><span data-stu-id="2717d-113">This command resumes the ANF Replication connection on volume "MyDestinationAnfVolume".</span></span>

## <span data-ttu-id="2717d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2717d-114">PARAMETERS</span></span>

### <span data-ttu-id="2717d-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2717d-115">-AccountName</span></span>
<span data-ttu-id="2717d-116">복제 볼륨의 ANF 계정 이름</span><span class="sxs-lookup"><span data-stu-id="2717d-116">The name of the ANF account of the replication volume</span></span>

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

### <span data-ttu-id="2717d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2717d-117">-DefaultProfile</span></span>
<span data-ttu-id="2717d-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2717d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2717d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2717d-119">-InputObject</span></span>
<span data-ttu-id="2717d-120">다시동기화할 ANF 복제 대상 볼륨 개체</span><span class="sxs-lookup"><span data-stu-id="2717d-120">The ANF replication destination volume object to resync</span></span>

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

### <span data-ttu-id="2717d-121">-Name</span><span class="sxs-lookup"><span data-stu-id="2717d-121">-Name</span></span>
<span data-ttu-id="2717d-122">ANF 복제 대상 볼륨의 이름</span><span class="sxs-lookup"><span data-stu-id="2717d-122">The name of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="2717d-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2717d-123">-PassThru</span></span>
<span data-ttu-id="2717d-124">지정된 복제 볼륨의 재동기화가 수행된지 여부를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="2717d-124">Return whether resync of the specified replication volume was performed</span></span>

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

### <span data-ttu-id="2717d-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="2717d-125">-PoolName</span></span>
<span data-ttu-id="2717d-126">복제 볼륨의 ANF 풀 이름</span><span class="sxs-lookup"><span data-stu-id="2717d-126">The name of the ANF pool of the replication volume</span></span>

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

### <span data-ttu-id="2717d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2717d-127">-ResourceGroupName</span></span>
<span data-ttu-id="2717d-128">ANF 복제 대상 볼륨의 리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="2717d-128">The resource group of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="2717d-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2717d-129">-ResourceId</span></span>
<span data-ttu-id="2717d-130">ANF 복제 대상 볼륨의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="2717d-130">The resource id of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="2717d-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2717d-131">-Confirm</span></span>
<span data-ttu-id="2717d-132">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="2717d-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2717d-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2717d-133">-WhatIf</span></span>
<span data-ttu-id="2717d-134">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="2717d-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2717d-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2717d-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2717d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2717d-136">CommonParameters</span></span>
<span data-ttu-id="2717d-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2717d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2717d-138">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2717d-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2717d-139">입력</span><span class="sxs-lookup"><span data-stu-id="2717d-139">INPUTS</span></span>

### <span data-ttu-id="2717d-140">System.String</span><span class="sxs-lookup"><span data-stu-id="2717d-140">System.String</span></span>

### <span data-ttu-id="2717d-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="2717d-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="2717d-142">출력</span><span class="sxs-lookup"><span data-stu-id="2717d-142">OUTPUTS</span></span>

### <span data-ttu-id="2717d-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2717d-143">System.Boolean</span></span>

## <span data-ttu-id="2717d-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2717d-144">NOTES</span></span>

## <span data-ttu-id="2717d-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2717d-145">RELATED LINKS</span></span>
