---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilessnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesSnapshot.md
ms.openlocfilehash: 1fe8da5c9ee899b7aa1a77a9fbb0ac7a2bf3b35c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98385659"
---
# <span data-ttu-id="3fe59-101">New-AzNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="3fe59-101">New-AzNetAppFilesSnapshot</span></span>

## <span data-ttu-id="3fe59-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3fe59-102">SYNOPSIS</span></span>
<span data-ttu-id="3fe59-103">새 ANF(Azure NetApp Files) 스냅숏을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3fe59-103">Creates a new Azure NetApp Files (ANF) snapshot.</span></span>

## <span data-ttu-id="3fe59-104">구문</span><span class="sxs-lookup"><span data-stu-id="3fe59-104">SYNTAX</span></span>

### <span data-ttu-id="3fe59-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="3fe59-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesSnapshot -ResourceGroupName <String> -Location <String> -AccountName <String>
 -PoolName <String> -VolumeName <String> -Name <String> [-FileSystemId <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3fe59-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3fe59-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesSnapshot -Name <String> [-Tag <Hashtable>] -VolumeObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3fe59-107">설명</span><span class="sxs-lookup"><span data-stu-id="3fe59-107">DESCRIPTION</span></span>
<span data-ttu-id="3fe59-108">**New-AzNetAppFilesSnapshot** cmdlet은 ANF 스냅숏을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3fe59-108">The **New-AzNetAppFilesSnapshot** cmdlet creates an ANF snapshot.</span></span>

## <span data-ttu-id="3fe59-109">예제</span><span class="sxs-lookup"><span data-stu-id="3fe59-109">EXAMPLES</span></span>

### <span data-ttu-id="3fe59-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="3fe59-110">Example 1</span></span>
```
PS C:\>New-AzNetAppFilesSnapshot -ResourceGroupName "MyRG" -l "westus2" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyAnfVolume" -SnapshotName "MyAnfSnapshot" -FileSystemId "3e2773a7-2a72-d003-0637-1a8b1fa3eaaf"

Output:

Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool/volumes/MyAnfVolume/snapshots/MyAnfSnapshot
Name              : MyAnfAccount/MyAnfPool/MyAnfVolume/MyAnfSnapshot
Type              : Microsoft.NetApp/netAppAccounts/capacityPools/volumes/snapshots
Tags              :
SnapshotId        : ca7c4ebd-91cb-0e30-91f5-9154050033df
FileSystemId      : 3e2773a7-2a72-d003-0637-1a8b1fa3eaaf
Created           :
ProvisioningState : Succeeded
```

<span data-ttu-id="3fe59-111">이 명령은 "MyAnfVolume" 볼륨 내에 새 ANF 스냅숏 "MyAnfSnapshot"을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3fe59-111">This command creates the new ANF snapshot "MyAnfSnapshot" within the volume "MyAnfVolume".</span></span>

## <span data-ttu-id="3fe59-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3fe59-112">PARAMETERS</span></span>

### <span data-ttu-id="3fe59-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="3fe59-113">-AccountName</span></span>
<span data-ttu-id="3fe59-114">ANF 계정의 이름</span><span class="sxs-lookup"><span data-stu-id="3fe59-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="3fe59-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fe59-115">-DefaultProfile</span></span>
<span data-ttu-id="3fe59-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3fe59-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3fe59-117">-FileSystemId</span><span class="sxs-lookup"><span data-stu-id="3fe59-117">-FileSystemId</span></span>
<span data-ttu-id="3fe59-118">파일 시스템 ID</span><span class="sxs-lookup"><span data-stu-id="3fe59-118">The file system id</span></span>

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

### <span data-ttu-id="3fe59-119">-Location</span><span class="sxs-lookup"><span data-stu-id="3fe59-119">-Location</span></span>
<span data-ttu-id="3fe59-120">리소스의 위치</span><span class="sxs-lookup"><span data-stu-id="3fe59-120">The location of the resource</span></span>

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

### <span data-ttu-id="3fe59-121">-Name</span><span class="sxs-lookup"><span data-stu-id="3fe59-121">-Name</span></span>
<span data-ttu-id="3fe59-122">ANF 스냅숏의 이름</span><span class="sxs-lookup"><span data-stu-id="3fe59-122">The name of the ANF snapshot</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SnapshotName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fe59-123">-PoolName</span><span class="sxs-lookup"><span data-stu-id="3fe59-123">-PoolName</span></span>
<span data-ttu-id="3fe59-124">ANF 풀의 이름</span><span class="sxs-lookup"><span data-stu-id="3fe59-124">The name of the ANF pool</span></span>

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

### <span data-ttu-id="3fe59-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3fe59-125">-ResourceGroupName</span></span>
<span data-ttu-id="3fe59-126">ANF 계정의 리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="3fe59-126">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="3fe59-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="3fe59-127">-Tag</span></span>
<span data-ttu-id="3fe59-128">리소스 태그를 나타내는 해시테이블</span><span class="sxs-lookup"><span data-stu-id="3fe59-128">A hashtable which represents resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fe59-129">-VolumeName</span><span class="sxs-lookup"><span data-stu-id="3fe59-129">-VolumeName</span></span>
<span data-ttu-id="3fe59-130">ANF 볼륨의 이름</span><span class="sxs-lookup"><span data-stu-id="3fe59-130">The name of the ANF volume</span></span>

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

### <span data-ttu-id="3fe59-131">-VolumeObject</span><span class="sxs-lookup"><span data-stu-id="3fe59-131">-VolumeObject</span></span>
<span data-ttu-id="3fe59-132">새 스냅숏 개체의 볼륨</span><span class="sxs-lookup"><span data-stu-id="3fe59-132">The volume for the new snapshot object</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3fe59-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3fe59-133">-Confirm</span></span>
<span data-ttu-id="3fe59-134">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="3fe59-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3fe59-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3fe59-135">-WhatIf</span></span>
<span data-ttu-id="3fe59-136">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="3fe59-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3fe59-137">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3fe59-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3fe59-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fe59-138">CommonParameters</span></span>
<span data-ttu-id="3fe59-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3fe59-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fe59-140">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3fe59-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fe59-141">입력</span><span class="sxs-lookup"><span data-stu-id="3fe59-141">INPUTS</span></span>

### <span data-ttu-id="3fe59-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="3fe59-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="3fe59-143">출력</span><span class="sxs-lookup"><span data-stu-id="3fe59-143">OUTPUTS</span></span>

### <span data-ttu-id="3fe59-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="3fe59-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshot</span></span>

## <span data-ttu-id="3fe59-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3fe59-145">NOTES</span></span>

## <span data-ttu-id="3fe59-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3fe59-146">RELATED LINKS</span></span>
