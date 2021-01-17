---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesVolume.md
ms.openlocfilehash: 2d3b212ea24c9dda665d2e2ec2516f25a59318b2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98380409"
---
# <span data-ttu-id="a82ed-101">Update-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="a82ed-101">Update-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="a82ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a82ed-102">SYNOPSIS</span></span>
<span data-ttu-id="a82ed-103">제공된 선택적 수정자에 따라 ANF(Azure NetApp Files) 볼륨을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="a82ed-103">Updates an Azure NetApp Files (ANF) volume according to the optional modifiers provided.</span></span>

## <span data-ttu-id="a82ed-104">구문</span><span class="sxs-lookup"><span data-stu-id="a82ed-104">SYNTAX</span></span>

### <span data-ttu-id="a82ed-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="a82ed-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesVolume -ResourceGroupName <String> -Location <String> -AccountName <String>
 -PoolName <String> -Name <String> [-UsageThreshold <Int64>] [-ServiceLevel <String>]
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>] [-Backup <PSNetAppFilesVolumeBackupProperties>]
 [-ThroughputMibps <Double>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a82ed-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a82ed-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesVolume -Name <String> [-UsageThreshold <Int64>] [-ServiceLevel <String>]
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>] [-Backup <PSNetAppFilesVolumeBackupProperties>]
 [-ThroughputMibps <Double>] [-Tag <Hashtable>] -PoolObject <PSNetAppFilesPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a82ed-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a82ed-107">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesVolume [-UsageThreshold <Int64>] [-ServiceLevel <String>]
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>] [-Backup <PSNetAppFilesVolumeBackupProperties>]
 [-ThroughputMibps <Double>] [-Tag <Hashtable>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a82ed-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a82ed-108">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesVolume [-UsageThreshold <Int64>] [-ServiceLevel <String>]
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>] [-Backup <PSNetAppFilesVolumeBackupProperties>]
 [-ThroughputMibps <Double>] [-Tag <Hashtable>] -InputObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a82ed-109">설명</span><span class="sxs-lookup"><span data-stu-id="a82ed-109">DESCRIPTION</span></span>
<span data-ttu-id="a82ed-110">**Update-AzNetAppFilesVolume** cmdlet은 ANF 볼륨을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="a82ed-110">The **Update-AzNetAppFilesVolume** cmdlet updates an ANF volume.</span></span>

## <span data-ttu-id="a82ed-111">예제</span><span class="sxs-lookup"><span data-stu-id="a82ed-111">EXAMPLES</span></span>

### <span data-ttu-id="a82ed-112">예제 1: ANF 볼륨 업데이트</span><span class="sxs-lookup"><span data-stu-id="a82ed-112">Example 1: Update an ANF volume</span></span>
```
PS C:\>Update-AzNetAppFilesVolume -ResourceGroupName "MyRG" -l "westus2" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -Name "MyAnfVolume" -UsageThreshold Size

Output:

Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool/volumes/MyAnfVolume
Name              : MyAnfAccount/MyAnfPool/MyAnfVolume
Type              : Microsoft.NetApp/netAppAccounts/capacityPools/volumes
Tags              :
FileSystemId      : 3e2773a7-2a72-d003-0637-1a8b1fa3eaaf
CreationToken     : MyAnfVolume
ServiceLevel      : Premium
UsageThreshold    : 2199023255552
ProvisioningState : Succeeded
SubnetId          : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.Network/virtualNetworks/MyRG-vnet/subnets/default
```

<span data-ttu-id="a82ed-113">이 명령은 ANF 볼륨 "MyAnfVolume"을 새 UsageThreshold 크기로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="a82ed-113">This command updates the ANF volume "MyAnfVolume" with the new UsageThreshold size.</span></span>

## <span data-ttu-id="a82ed-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a82ed-114">PARAMETERS</span></span>

### <span data-ttu-id="a82ed-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a82ed-115">-AccountName</span></span>
<span data-ttu-id="a82ed-116">ANF 계정의 이름</span><span class="sxs-lookup"><span data-stu-id="a82ed-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="a82ed-117">-Backup</span><span class="sxs-lookup"><span data-stu-id="a82ed-117">-Backup</span></span>
<span data-ttu-id="a82ed-118">백업 개체를 나타내는 해시할 수 있는 배열</span><span class="sxs-lookup"><span data-stu-id="a82ed-118">A hashtable array which represents the backup object</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolumeBackupProperties
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a82ed-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a82ed-119">-DefaultProfile</span></span>
<span data-ttu-id="a82ed-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a82ed-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a82ed-121">-ExportPolicy</span><span class="sxs-lookup"><span data-stu-id="a82ed-121">-ExportPolicy</span></span>
<span data-ttu-id="a82ed-122">내보내기 정책을 나타내는 해시할 수 있는 배열</span><span class="sxs-lookup"><span data-stu-id="a82ed-122">A hashtable array which represents the export policy</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolumeExportPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a82ed-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a82ed-123">-InputObject</span></span>
<span data-ttu-id="a82ed-124">업데이트할 볼륨 개체</span><span class="sxs-lookup"><span data-stu-id="a82ed-124">The volume object to update</span></span>

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

### <span data-ttu-id="a82ed-125">-Location</span><span class="sxs-lookup"><span data-stu-id="a82ed-125">-Location</span></span>
<span data-ttu-id="a82ed-126">리소스의 위치</span><span class="sxs-lookup"><span data-stu-id="a82ed-126">The location of the resource</span></span>

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

### <span data-ttu-id="a82ed-127">-Name</span><span class="sxs-lookup"><span data-stu-id="a82ed-127">-Name</span></span>
<span data-ttu-id="a82ed-128">ANF 볼륨의 이름</span><span class="sxs-lookup"><span data-stu-id="a82ed-128">The name of the ANF volume</span></span>

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

### <span data-ttu-id="a82ed-129">-PoolName</span><span class="sxs-lookup"><span data-stu-id="a82ed-129">-PoolName</span></span>
<span data-ttu-id="a82ed-130">ANF 풀의 이름</span><span class="sxs-lookup"><span data-stu-id="a82ed-130">The name of the ANF pool</span></span>

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

### <span data-ttu-id="a82ed-131">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="a82ed-131">-PoolObject</span></span>
<span data-ttu-id="a82ed-132">업데이트할 볼륨을 포함하는 풀 개체</span><span class="sxs-lookup"><span data-stu-id="a82ed-132">The pool object containing the volume to update</span></span>

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

### <span data-ttu-id="a82ed-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a82ed-133">-ResourceGroupName</span></span>
<span data-ttu-id="a82ed-134">ANF 계정의 리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="a82ed-134">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="a82ed-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a82ed-135">-ResourceId</span></span>
<span data-ttu-id="a82ed-136">ANF 볼륨의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="a82ed-136">The resource id of the ANF volume</span></span>

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

### <span data-ttu-id="a82ed-137">-ServiceLevel</span><span class="sxs-lookup"><span data-stu-id="a82ed-137">-ServiceLevel</span></span>
<span data-ttu-id="a82ed-138">ANF 볼륨의 서비스 수준</span><span class="sxs-lookup"><span data-stu-id="a82ed-138">The service level of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a82ed-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="a82ed-139">-Tag</span></span>
<span data-ttu-id="a82ed-140">리소스 태그를 나타내는 해시테이블</span><span class="sxs-lookup"><span data-stu-id="a82ed-140">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="a82ed-141">-ThroughputMibps</span><span class="sxs-lookup"><span data-stu-id="a82ed-141">-ThroughputMibps</span></span>
<span data-ttu-id="a82ed-142">이 볼륨으로 달성할 수 있는 최대 Mibps의 최대량</span><span class="sxs-lookup"><span data-stu-id="a82ed-142">Maximum throughput in Mibps that can be achieved by this volume</span></span>

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a82ed-143">-UsageThreshold</span><span class="sxs-lookup"><span data-stu-id="a82ed-143">-UsageThreshold</span></span>
<span data-ttu-id="a82ed-144">파일 시스템에 허용되는 최대 저장소 할당량(byte)입니다.</span><span class="sxs-lookup"><span data-stu-id="a82ed-144">The maximum storage quota allowed for a file system in bytes</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a82ed-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a82ed-145">-Confirm</span></span>
<span data-ttu-id="a82ed-146">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a82ed-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a82ed-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a82ed-147">-WhatIf</span></span>
<span data-ttu-id="a82ed-148">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="a82ed-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a82ed-149">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a82ed-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a82ed-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a82ed-150">CommonParameters</span></span>
<span data-ttu-id="a82ed-151">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a82ed-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a82ed-152">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a82ed-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a82ed-153">입력</span><span class="sxs-lookup"><span data-stu-id="a82ed-153">INPUTS</span></span>

### <span data-ttu-id="a82ed-154">System.String</span><span class="sxs-lookup"><span data-stu-id="a82ed-154">System.String</span></span>

### <span data-ttu-id="a82ed-155">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="a82ed-155">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

### <span data-ttu-id="a82ed-156">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="a82ed-156">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="a82ed-157">출력</span><span class="sxs-lookup"><span data-stu-id="a82ed-157">OUTPUTS</span></span>

### <span data-ttu-id="a82ed-158">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="a82ed-158">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="a82ed-159">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a82ed-159">NOTES</span></span>

## <span data-ttu-id="a82ed-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a82ed-160">RELATED LINKS</span></span>
