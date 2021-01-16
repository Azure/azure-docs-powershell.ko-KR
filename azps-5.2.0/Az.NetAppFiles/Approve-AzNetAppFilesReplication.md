---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/approve-aznetappfilesreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Approve-AzNetAppFilesReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Approve-AzNetAppFilesReplication.md
ms.openlocfilehash: 9afa4f22de142dba7608d33ed04c972758911aa9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98360235"
---
# <span data-ttu-id="617e3-101">Approve-AzNetAppFilesReplication</span><span class="sxs-lookup"><span data-stu-id="617e3-101">Approve-AzNetAppFilesReplication</span></span>

## <span data-ttu-id="617e3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="617e3-102">SYNOPSIS</span></span>
<span data-ttu-id="617e3-103">원본 볼륨에서 복제 연결 승인/권한을 승인합니다.</span><span class="sxs-lookup"><span data-stu-id="617e3-103">Approve/Authorize replication connection on the source volume</span></span>

## <span data-ttu-id="617e3-104">구문</span><span class="sxs-lookup"><span data-stu-id="617e3-104">SYNTAX</span></span>

### <span data-ttu-id="617e3-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="617e3-105">ByFieldsParameterSet (Default)</span></span>
```
Approve-AzNetAppFilesReplication -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> -DataProtectionVolumeId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="617e3-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="617e3-106">ByResourceIdParameterSet</span></span>
```
Approve-AzNetAppFilesReplication -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="617e3-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="617e3-107">ByObjectParameterSet</span></span>
```
Approve-AzNetAppFilesReplication -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="617e3-108">설명</span><span class="sxs-lookup"><span data-stu-id="617e3-108">DESCRIPTION</span></span>
<span data-ttu-id="617e3-109">원본 볼륨에서 복제 연결 승인</span><span class="sxs-lookup"><span data-stu-id="617e3-109">Approve the replication connection on the source volume</span></span>

## <span data-ttu-id="617e3-110">예제</span><span class="sxs-lookup"><span data-stu-id="617e3-110">EXAMPLES</span></span>

### <span data-ttu-id="617e3-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="617e3-111">Example 1</span></span>
```powershell
PS C:\> Approve-AzNetAppFilesReplication -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyAnfVolume" -DataProtectionVolumeId "MyDestinationVolumeId"

Output:
remoteVolumeResourceId          : resourceId
```

<span data-ttu-id="617e3-112">이 명령은 MyAnfVolume에서 복제를 승인합니다.</span><span class="sxs-lookup"><span data-stu-id="617e3-112">This command Approves the Replication on MyAnfVolume.</span></span>

## <span data-ttu-id="617e3-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="617e3-113">PARAMETERS</span></span>

### <span data-ttu-id="617e3-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="617e3-114">-AccountName</span></span>
<span data-ttu-id="617e3-115">복제 원본 볼륨의 ANF 계정 이름</span><span class="sxs-lookup"><span data-stu-id="617e3-115">The name of the ANF account of the replication source volume</span></span>

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

### <span data-ttu-id="617e3-116">-DataProtectionVolumeId</span><span class="sxs-lookup"><span data-stu-id="617e3-116">-DataProtectionVolumeId</span></span>
<span data-ttu-id="617e3-117">대상 데이터 보호 볼륨의 파일 시스템 ID</span><span class="sxs-lookup"><span data-stu-id="617e3-117">The file system id of the destination data protection volume</span></span>

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

### <span data-ttu-id="617e3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="617e3-118">-DefaultProfile</span></span>
<span data-ttu-id="617e3-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="617e3-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="617e3-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="617e3-120">-InputObject</span></span>
<span data-ttu-id="617e3-121">복제 대상에 권한을 부여할 ANF 원본 볼륨 개체</span><span class="sxs-lookup"><span data-stu-id="617e3-121">The ANF source volume object to authorized the replication destination</span></span>

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

### <span data-ttu-id="617e3-122">-Name</span><span class="sxs-lookup"><span data-stu-id="617e3-122">-Name</span></span>
<span data-ttu-id="617e3-123">ANF 복제 원본 볼륨의 이름</span><span class="sxs-lookup"><span data-stu-id="617e3-123">The name of the ANF replication source volume</span></span>

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

### <span data-ttu-id="617e3-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="617e3-124">-PassThru</span></span>
<span data-ttu-id="617e3-125">지정된 볼륨의 복제 권한 부여가 수행된지 여부를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="617e3-125">Return whether replication authorization of the specified volume was performed</span></span>

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

### <span data-ttu-id="617e3-126">-PoolName</span><span class="sxs-lookup"><span data-stu-id="617e3-126">-PoolName</span></span>
<span data-ttu-id="617e3-127">복제 원본 볼륨의 ANF 풀 이름</span><span class="sxs-lookup"><span data-stu-id="617e3-127">The name of the ANF pool of the replication source volume</span></span>

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

### <span data-ttu-id="617e3-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="617e3-128">-ResourceGroupName</span></span>
<span data-ttu-id="617e3-129">ANF 복제 원본 볼륨의 리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="617e3-129">The resource group of the ANF replication source volume</span></span>

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

### <span data-ttu-id="617e3-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="617e3-130">-ResourceId</span></span>
<span data-ttu-id="617e3-131">ANF 복제 원본 볼륨의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="617e3-131">The resource id of the ANF replication source volume</span></span>

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

### <span data-ttu-id="617e3-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="617e3-132">-Confirm</span></span>
<span data-ttu-id="617e3-133">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="617e3-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="617e3-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="617e3-134">-WhatIf</span></span>
<span data-ttu-id="617e3-135">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="617e3-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="617e3-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="617e3-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="617e3-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="617e3-137">CommonParameters</span></span>
<span data-ttu-id="617e3-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="617e3-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="617e3-139">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="617e3-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="617e3-140">입력</span><span class="sxs-lookup"><span data-stu-id="617e3-140">INPUTS</span></span>

### <span data-ttu-id="617e3-141">System.String</span><span class="sxs-lookup"><span data-stu-id="617e3-141">System.String</span></span>

### <span data-ttu-id="617e3-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="617e3-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="617e3-143">출력</span><span class="sxs-lookup"><span data-stu-id="617e3-143">OUTPUTS</span></span>

### <span data-ttu-id="617e3-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="617e3-144">System.Boolean</span></span>

## <span data-ttu-id="617e3-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="617e3-145">NOTES</span></span>

## <span data-ttu-id="617e3-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="617e3-146">RELATED LINKS</span></span>
