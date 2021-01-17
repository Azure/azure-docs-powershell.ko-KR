---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesVolume.md
ms.openlocfilehash: 2326551a2b6a03e1904e8d0d90663ee796ccaa46
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98359899"
---
# <span data-ttu-id="23164-101">New-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="23164-101">New-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="23164-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23164-102">SYNOPSIS</span></span>
<span data-ttu-id="23164-103">새 ANF(Azure NetApp Files) 볼륨을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="23164-103">Creates a new Azure NetApp Files (ANF) volume.</span></span>

## <span data-ttu-id="23164-104">구문</span><span class="sxs-lookup"><span data-stu-id="23164-104">SYNTAX</span></span>

### <span data-ttu-id="23164-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="23164-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesVolume -ResourceGroupName <String> -Location <String> -AccountName <String> -PoolName <String>
 -Name <String> -UsageThreshold <Int64> -SubnetId <String> -CreationToken <String> [-VolumeType <String>]
 -ServiceLevel <String> [-SnapshotId <String>] [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>]
 [-ReplicationObject <PSNetAppFilesReplicationObject>] [-Snapshot <PSNetAppFilesVolumeSnapshot>]
 [-Backup <PSNetAppFilesVolumeBackupProperties>] [-ProtocolType <String[]>] [-SnapshotDirectoryVisible]
 [-BackupId <String>] [-SecurityStyle <String>] [-ThroughputMibps <Double>] [-KerberosEnabled]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23164-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="23164-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesVolume -Name <String> -UsageThreshold <Int64> -SubnetId <String> -CreationToken <String>
 -ServiceLevel <String> [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>]
 [-ReplicationObject <PSNetAppFilesReplicationObject>] [-Snapshot <PSNetAppFilesVolumeSnapshot>]
 [-Backup <PSNetAppFilesVolumeBackupProperties>] [-ProtocolType <String[]>] [-SnapshotDirectoryVisible]
 [-SecurityStyle <String>] [-ThroughputMibps <Double>] [-KerberosEnabled] [-Tag <Hashtable>]
 -PoolObject <PSNetAppFilesPool> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="23164-107">설명</span><span class="sxs-lookup"><span data-stu-id="23164-107">DESCRIPTION</span></span>
<span data-ttu-id="23164-108">**New-AzNetAppFilesVolume** cmdlet은 ANF 볼륨을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="23164-108">The **New-AzNetAppFilesVolume** cmdlet creates an ANF volume.</span></span>

## <span data-ttu-id="23164-109">예제</span><span class="sxs-lookup"><span data-stu-id="23164-109">EXAMPLES</span></span>

### <span data-ttu-id="23164-110">예제 1: ANF 볼륨 만들기</span><span class="sxs-lookup"><span data-stu-id="23164-110">Example 1: Create an ANF volume</span></span>
```
PS C:\>New-AzNetAppFilesVolume -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -Name "MyAnfVolume" -l "westus2" -CreationToken "MyAnfVolume" -UsageThreshold 1099511627776 -ServiceLevel "Premium" -SubnetId "/subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.Network/virtualNetworks/MyVnetName/subnets/MySubNetName"

Output:

Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool/volumes/MyAnfVolume
Name              : MyAnfAccount/MyAnfPool/MyAnfVolume
Type              : Microsoft.NetApp/netAppAccounts/capacityPools/volumes
Tags              :
FileSystemId      : 3e2773a7-2a72-d003-0637-1a8b1fa3eaaf
CreationToken     : MyAnfVolume
ServiceLevel      : Premium
UsageThreshold    : 1099511627776
ProvisioningState : Succeeded
SubnetId          : /subscriptions/f557b96d-2308-4a18-aae1-b8f7e7e70cc7/resourceGroups/MyRG/providers/Microsoft.Network/virtualNetworks/MyVnetName/subnets/default
```

<span data-ttu-id="23164-111">이 명령은 "MyAnfPool" 풀 내에 새 ANF 볼륨 "MyAnfVolume"을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="23164-111">This command creates the new ANF volume "MyAnfVolume" within the pool "MyAnfPool".</span></span>

## <span data-ttu-id="23164-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="23164-112">PARAMETERS</span></span>

### <span data-ttu-id="23164-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="23164-113">-AccountName</span></span>
<span data-ttu-id="23164-114">ANF 계정의 이름</span><span class="sxs-lookup"><span data-stu-id="23164-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="23164-115">-Backup</span><span class="sxs-lookup"><span data-stu-id="23164-115">-Backup</span></span>
<span data-ttu-id="23164-116">백업 개체를 나타내는 해시할 수 있는 배열</span><span class="sxs-lookup"><span data-stu-id="23164-116">A hashtable array which represents the backup object</span></span>

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

### <span data-ttu-id="23164-117">-BackupId</span><span class="sxs-lookup"><span data-stu-id="23164-117">-BackupId</span></span>
<span data-ttu-id="23164-118">Backup ID입니다.</span><span class="sxs-lookup"><span data-stu-id="23164-118">Backup ID.</span></span> <span data-ttu-id="23164-119">백업을 식별하는 데 사용되는 UUID v4 또는 리소스 식별자</span><span class="sxs-lookup"><span data-stu-id="23164-119">UUID v4 or resource identifier used to identify the Backup</span></span>

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

### <span data-ttu-id="23164-120">-CreationToken</span><span class="sxs-lookup"><span data-stu-id="23164-120">-CreationToken</span></span>
<span data-ttu-id="23164-121">볼륨에 대한 고유한 파일 경로</span><span class="sxs-lookup"><span data-stu-id="23164-121">A unique file path for the volume</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23164-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23164-122">-DefaultProfile</span></span>
<span data-ttu-id="23164-123">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="23164-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23164-124">-ExportPolicy</span><span class="sxs-lookup"><span data-stu-id="23164-124">-ExportPolicy</span></span>
<span data-ttu-id="23164-125">내보내기 정책을 나타내는 해시할 수 있는 배열</span><span class="sxs-lookup"><span data-stu-id="23164-125">A hashtable array which represents the export policy</span></span>

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

### <span data-ttu-id="23164-126">-KerberosEnabled</span><span class="sxs-lookup"><span data-stu-id="23164-126">-KerberosEnabled</span></span>
<span data-ttu-id="23164-127">볼륨이 Kerberos를 사용하도록 설정되어 있는지 설명</span><span class="sxs-lookup"><span data-stu-id="23164-127">Describe if a volume is Kerberos Enabled</span></span>

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

### <span data-ttu-id="23164-128">-Location</span><span class="sxs-lookup"><span data-stu-id="23164-128">-Location</span></span>
<span data-ttu-id="23164-129">리소스의 위치</span><span class="sxs-lookup"><span data-stu-id="23164-129">The location of the resource</span></span>

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

### <span data-ttu-id="23164-130">-Name</span><span class="sxs-lookup"><span data-stu-id="23164-130">-Name</span></span>
<span data-ttu-id="23164-131">ANF 볼륨의 이름</span><span class="sxs-lookup"><span data-stu-id="23164-131">The name of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: VolumeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23164-132">-PoolName</span><span class="sxs-lookup"><span data-stu-id="23164-132">-PoolName</span></span>
<span data-ttu-id="23164-133">ANF 풀의 이름</span><span class="sxs-lookup"><span data-stu-id="23164-133">The name of the ANF pool</span></span>

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

### <span data-ttu-id="23164-134">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="23164-134">-PoolObject</span></span>
<span data-ttu-id="23164-135">새 볼륨 개체에 대한 풀</span><span class="sxs-lookup"><span data-stu-id="23164-135">The pool for the new volume object</span></span>

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

### <span data-ttu-id="23164-136">-ProtocolType</span><span class="sxs-lookup"><span data-stu-id="23164-136">-ProtocolType</span></span>
<span data-ttu-id="23164-137">내보내기 정책을 나타내는 해시할 수 있는 배열</span><span class="sxs-lookup"><span data-stu-id="23164-137">A hashtable array which represents the export policy</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23164-138">-ReplicationObject</span><span class="sxs-lookup"><span data-stu-id="23164-138">-ReplicationObject</span></span>
<span data-ttu-id="23164-139">복제 개체를 나타내는 해시테이블 배열</span><span class="sxs-lookup"><span data-stu-id="23164-139">A hashtable array which represents the replication object</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesReplicationObject
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23164-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23164-140">-ResourceGroupName</span></span>
<span data-ttu-id="23164-141">ANF 계정의 리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="23164-141">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="23164-142">-SecurityStyle</span><span class="sxs-lookup"><span data-stu-id="23164-142">-SecurityStyle</span></span>
<span data-ttu-id="23164-143">볼륨의 보안 스타일입니다.</span><span class="sxs-lookup"><span data-stu-id="23164-143">The security style of volume.</span></span> <span data-ttu-id="23164-144">가능한 값은 'ntfs', 'unix'입니다.</span><span class="sxs-lookup"><span data-stu-id="23164-144">Possible values include: 'ntfs', 'unix'</span></span>

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

### <span data-ttu-id="23164-145">-ServiceLevel</span><span class="sxs-lookup"><span data-stu-id="23164-145">-ServiceLevel</span></span>
<span data-ttu-id="23164-146">ANF 볼륨의 서비스 수준</span><span class="sxs-lookup"><span data-stu-id="23164-146">The service level of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23164-147">-Snapshot</span><span class="sxs-lookup"><span data-stu-id="23164-147">-Snapshot</span></span>
<span data-ttu-id="23164-148">스냅숏 개체를 나타내는 해시블 배열</span><span class="sxs-lookup"><span data-stu-id="23164-148">A hashtable array which represents the snapshot object</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolumeSnapshot
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23164-149">-SnapshotDirectoryVisible</span><span class="sxs-lookup"><span data-stu-id="23164-149">-SnapshotDirectoryVisible</span></span>
<span data-ttu-id="23164-150">활성화된 경우(true) 볼륨에는 각 볼륨의 스냅숏에 대한 액세스를 제공하는 읽기 전용 .snapshot 디렉터리가 포함됩니다(기본값: true).</span><span class="sxs-lookup"><span data-stu-id="23164-150">If enabled (true) the volume will contain a read-only .snapshot directory which provides access to each of the volume's snapshots (default to true)</span></span>

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

### <span data-ttu-id="23164-151">-SnapshotId</span><span class="sxs-lookup"><span data-stu-id="23164-151">-SnapshotId</span></span>
<span data-ttu-id="23164-152">스냅숏에서 볼륨을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="23164-152">Create volume from a snapshot.</span></span> <span data-ttu-id="23164-153">스냅숏을 식별하는 데 사용되는 UUID v4 또는 리소스 식별자</span><span class="sxs-lookup"><span data-stu-id="23164-153">UUID v4 or resource identifier used to identify the Snapshot</span></span>

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

### <span data-ttu-id="23164-154">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="23164-154">-SubnetId</span></span>
<span data-ttu-id="23164-155">위임된 서브넷에 대한 Azure 리소스 URI</span><span class="sxs-lookup"><span data-stu-id="23164-155">The Azure Resource URI for a delegated subnet</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23164-156">-Tag</span><span class="sxs-lookup"><span data-stu-id="23164-156">-Tag</span></span>
<span data-ttu-id="23164-157">리소스 태그를 나타내는 해시테이블</span><span class="sxs-lookup"><span data-stu-id="23164-157">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="23164-158">-ThroughputMibps</span><span class="sxs-lookup"><span data-stu-id="23164-158">-ThroughputMibps</span></span>
<span data-ttu-id="23164-159">이 볼륨으로 달성할 수 있는 최대 Mibps의 최대량</span><span class="sxs-lookup"><span data-stu-id="23164-159">Maximum throughput in Mibps that can be achieved by this volume</span></span>

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

### <span data-ttu-id="23164-160">-UsageThreshold</span><span class="sxs-lookup"><span data-stu-id="23164-160">-UsageThreshold</span></span>
<span data-ttu-id="23164-161">파일 시스템에 허용되는 최대 저장소 할당량(byte)입니다.</span><span class="sxs-lookup"><span data-stu-id="23164-161">The maximum storage quota allowed for a file system in bytes</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23164-162">-VolumeType</span><span class="sxs-lookup"><span data-stu-id="23164-162">-VolumeType</span></span>
<span data-ttu-id="23164-163">ANF 볼륨의 유형</span><span class="sxs-lookup"><span data-stu-id="23164-163">The type of the ANF volume</span></span>

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

### <span data-ttu-id="23164-164">-Confirm</span><span class="sxs-lookup"><span data-stu-id="23164-164">-Confirm</span></span>
<span data-ttu-id="23164-165">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="23164-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23164-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23164-166">-WhatIf</span></span>
<span data-ttu-id="23164-167">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="23164-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23164-168">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="23164-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23164-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23164-169">CommonParameters</span></span>
<span data-ttu-id="23164-170">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="23164-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23164-171">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="23164-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23164-172">입력</span><span class="sxs-lookup"><span data-stu-id="23164-172">INPUTS</span></span>

### <span data-ttu-id="23164-173">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="23164-173">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="23164-174">출력</span><span class="sxs-lookup"><span data-stu-id="23164-174">OUTPUTS</span></span>

### <span data-ttu-id="23164-175">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="23164-175">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="23164-176">참고 사항</span><span class="sxs-lookup"><span data-stu-id="23164-176">NOTES</span></span>

## <span data-ttu-id="23164-177">관련 링크</span><span class="sxs-lookup"><span data-stu-id="23164-177">RELATED LINKS</span></span>
