---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/update-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesVolume.md
ms.openlocfilehash: b7947f4224c667ed8332b0f3206588dda49fd1af
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968075"
---
# <span data-ttu-id="c656f-101">Update-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="c656f-101">Update-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="c656f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c656f-102">SYNOPSIS</span></span>
<span data-ttu-id="c656f-103">제공된 선택적 수정자에 따라 ANF(Azure NetApp Files) 볼륨을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="c656f-103">Updates an Azure NetApp Files (ANF) volume according to the optional modifiers provided.</span></span>

## <span data-ttu-id="c656f-104">구문</span><span class="sxs-lookup"><span data-stu-id="c656f-104">SYNTAX</span></span>

### <span data-ttu-id="c656f-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="c656f-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesVolume -ResourceGroupName <String> -Location <String> -AccountName <String>
 -PoolName <String> -Name <String> [-UsageThreshold <Int64>] [-ServiceLevel <String>]
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>] [-Backup <PSNetAppFilesVolumeBackupProperties>]
 [-ThroughputMibps <Double>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c656f-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c656f-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesVolume -Name <String> [-UsageThreshold <Int64>] [-ServiceLevel <String>]
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>] [-Backup <PSNetAppFilesVolumeBackupProperties>]
 [-ThroughputMibps <Double>] [-Tag <Hashtable>] -PoolObject <PSNetAppFilesPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c656f-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c656f-107">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesVolume [-UsageThreshold <Int64>] [-ServiceLevel <String>]
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>] [-Backup <PSNetAppFilesVolumeBackupProperties>]
 [-ThroughputMibps <Double>] [-Tag <Hashtable>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c656f-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c656f-108">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesVolume [-UsageThreshold <Int64>] [-ServiceLevel <String>]
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>] [-Backup <PSNetAppFilesVolumeBackupProperties>]
 [-ThroughputMibps <Double>] [-Tag <Hashtable>] -InputObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c656f-109">설명</span><span class="sxs-lookup"><span data-stu-id="c656f-109">DESCRIPTION</span></span>
<span data-ttu-id="c656f-110">**Update-AzNetAppFilesVolume** cmdlet은 ANF 볼륨을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="c656f-110">The **Update-AzNetAppFilesVolume** cmdlet updates an ANF volume.</span></span>

## <span data-ttu-id="c656f-111">예제</span><span class="sxs-lookup"><span data-stu-id="c656f-111">EXAMPLES</span></span>

### <span data-ttu-id="c656f-112">예제 1: ANF 볼륨 업데이트</span><span class="sxs-lookup"><span data-stu-id="c656f-112">Example 1: Update an ANF volume</span></span>
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

<span data-ttu-id="c656f-113">이 명령은 새 UsageThreshold 크기로 ANF 볼륨 "MyAnfVolume"을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="c656f-113">This command updates the ANF volume "MyAnfVolume" with the new UsageThreshold size.</span></span>

## <span data-ttu-id="c656f-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="c656f-114">PARAMETERS</span></span>

### <span data-ttu-id="c656f-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c656f-115">-AccountName</span></span>
<span data-ttu-id="c656f-116">ANF 계정의 이름</span><span class="sxs-lookup"><span data-stu-id="c656f-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="c656f-117">-Backup</span><span class="sxs-lookup"><span data-stu-id="c656f-117">-Backup</span></span>
<span data-ttu-id="c656f-118">백업 개체를 나타내는 해시테이블 배열</span><span class="sxs-lookup"><span data-stu-id="c656f-118">A hashtable array which represents the backup object</span></span>

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

### <span data-ttu-id="c656f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c656f-119">-DefaultProfile</span></span>
<span data-ttu-id="c656f-120">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c656f-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c656f-121">-ExportPolicy</span><span class="sxs-lookup"><span data-stu-id="c656f-121">-ExportPolicy</span></span>
<span data-ttu-id="c656f-122">내보내기 정책을 나타내는 해시테이블 배열</span><span class="sxs-lookup"><span data-stu-id="c656f-122">A hashtable array which represents the export policy</span></span>

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

### <span data-ttu-id="c656f-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c656f-123">-InputObject</span></span>
<span data-ttu-id="c656f-124">업데이트할 볼륨 개체</span><span class="sxs-lookup"><span data-stu-id="c656f-124">The volume object to update</span></span>

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

### <span data-ttu-id="c656f-125">-Location</span><span class="sxs-lookup"><span data-stu-id="c656f-125">-Location</span></span>
<span data-ttu-id="c656f-126">리소스의 위치</span><span class="sxs-lookup"><span data-stu-id="c656f-126">The location of the resource</span></span>

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

### <span data-ttu-id="c656f-127">-Name</span><span class="sxs-lookup"><span data-stu-id="c656f-127">-Name</span></span>
<span data-ttu-id="c656f-128">ANF 볼륨의 이름</span><span class="sxs-lookup"><span data-stu-id="c656f-128">The name of the ANF volume</span></span>

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

### <span data-ttu-id="c656f-129">-PoolName</span><span class="sxs-lookup"><span data-stu-id="c656f-129">-PoolName</span></span>
<span data-ttu-id="c656f-130">ANF 풀의 이름</span><span class="sxs-lookup"><span data-stu-id="c656f-130">The name of the ANF pool</span></span>

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

### <span data-ttu-id="c656f-131">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="c656f-131">-PoolObject</span></span>
<span data-ttu-id="c656f-132">업데이트할 볼륨을 포함하는 풀 개체</span><span class="sxs-lookup"><span data-stu-id="c656f-132">The pool object containing the volume to update</span></span>

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

### <span data-ttu-id="c656f-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c656f-133">-ResourceGroupName</span></span>
<span data-ttu-id="c656f-134">ANF 계정의 리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="c656f-134">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="c656f-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c656f-135">-ResourceId</span></span>
<span data-ttu-id="c656f-136">ANF 볼륨의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="c656f-136">The resource id of the ANF volume</span></span>

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

### <span data-ttu-id="c656f-137">-ServiceLevel</span><span class="sxs-lookup"><span data-stu-id="c656f-137">-ServiceLevel</span></span>
<span data-ttu-id="c656f-138">ANF 볼륨의 서비스 수준</span><span class="sxs-lookup"><span data-stu-id="c656f-138">The service level of the ANF volume</span></span>

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

### <span data-ttu-id="c656f-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="c656f-139">-Tag</span></span>
<span data-ttu-id="c656f-140">리소스 태그를 나타내는 해시테이블</span><span class="sxs-lookup"><span data-stu-id="c656f-140">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="c656f-141">-ThroughputMibps</span><span class="sxs-lookup"><span data-stu-id="c656f-141">-ThroughputMibps</span></span>
<span data-ttu-id="c656f-142">이 볼륨에서 달성할 수 있는 Mibps의 최대 사용량</span><span class="sxs-lookup"><span data-stu-id="c656f-142">Maximum throughput in Mibps that can be achieved by this volume</span></span>

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

### <span data-ttu-id="c656f-143">-UsageThreshold</span><span class="sxs-lookup"><span data-stu-id="c656f-143">-UsageThreshold</span></span>
<span data-ttu-id="c656f-144">파일 시스템에 허용되는 최대 저장소 할당량(byte)입니다.</span><span class="sxs-lookup"><span data-stu-id="c656f-144">The maximum storage quota allowed for a file system in bytes</span></span>

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

### <span data-ttu-id="c656f-145">-확인</span><span class="sxs-lookup"><span data-stu-id="c656f-145">-Confirm</span></span>
<span data-ttu-id="c656f-146">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c656f-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c656f-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c656f-147">-WhatIf</span></span>
<span data-ttu-id="c656f-148">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="c656f-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c656f-149">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c656f-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c656f-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c656f-150">CommonParameters</span></span>
<span data-ttu-id="c656f-151">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c656f-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c656f-152">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c656f-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c656f-153">입력</span><span class="sxs-lookup"><span data-stu-id="c656f-153">INPUTS</span></span>

### <span data-ttu-id="c656f-154">System.String</span><span class="sxs-lookup"><span data-stu-id="c656f-154">System.String</span></span>

### <span data-ttu-id="c656f-155">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="c656f-155">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

### <span data-ttu-id="c656f-156">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="c656f-156">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="c656f-157">출력</span><span class="sxs-lookup"><span data-stu-id="c656f-157">OUTPUTS</span></span>

### <span data-ttu-id="c656f-158">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="c656f-158">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="c656f-159">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c656f-159">NOTES</span></span>

## <span data-ttu-id="c656f-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c656f-160">RELATED LINKS</span></span>
