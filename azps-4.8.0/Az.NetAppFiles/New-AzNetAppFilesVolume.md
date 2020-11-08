---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesVolume.md
ms.openlocfilehash: dce91ee25cac4a716dc604e38f1ac38e5a3f3f1d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048962"
---
# <span data-ttu-id="c46fc-101">New-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="c46fc-101">New-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="c46fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c46fc-102">SYNOPSIS</span></span>
<span data-ttu-id="c46fc-103">새 Azure NetApp Files (ANF) 볼륨을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c46fc-103">Creates a new Azure NetApp Files (ANF) volume.</span></span>

## <span data-ttu-id="c46fc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c46fc-104">SYNTAX</span></span>

### <span data-ttu-id="c46fc-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="c46fc-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesVolume -ResourceGroupName <String> -Location <String> -AccountName <String> -PoolName <String>
 -Name <String> -UsageThreshold <Int64> -SubnetId <String> -CreationToken <String> [-VolumeType <String>]
 -ServiceLevel <String> [-SnapshotId <String>] [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>]
 [-ReplicationObject <PSNetAppFilesReplicationObject>] [-ProtocolType <String[]>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c46fc-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c46fc-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesVolume -Name <String> -UsageThreshold <Int64> -SubnetId <String> -CreationToken <String>
 -ServiceLevel <String> [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>]
 [-ReplicationObject <PSNetAppFilesReplicationObject>] [-ProtocolType <String[]>] [-Tag <Hashtable>]
 -PoolObject <PSNetAppFilesPool> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c46fc-107">설명은</span><span class="sxs-lookup"><span data-stu-id="c46fc-107">DESCRIPTION</span></span>
<span data-ttu-id="c46fc-108">**새 AzNetAppFilesVolume** cmdlet은 anf 볼륨을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c46fc-108">The **New-AzNetAppFilesVolume** cmdlet creates an ANF volume.</span></span>

## <span data-ttu-id="c46fc-109">예제의</span><span class="sxs-lookup"><span data-stu-id="c46fc-109">EXAMPLES</span></span>

### <span data-ttu-id="c46fc-110">예제 1: ANF 볼륨 만들기</span><span class="sxs-lookup"><span data-stu-id="c46fc-110">Example 1: Create an ANF volume</span></span>
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

<span data-ttu-id="c46fc-111">이 명령은 "MyAnfPool" 풀 내에 새 ANF 볼륨 "MyAnfVolume"를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c46fc-111">This command creates the new ANF volume "MyAnfVolume" within the pool "MyAnfPool".</span></span>

## <span data-ttu-id="c46fc-112">변수</span><span class="sxs-lookup"><span data-stu-id="c46fc-112">PARAMETERS</span></span>

### <span data-ttu-id="c46fc-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c46fc-113">-AccountName</span></span>
<span data-ttu-id="c46fc-114">ANF 계정의 이름</span><span class="sxs-lookup"><span data-stu-id="c46fc-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="c46fc-115">-CreationToken</span><span class="sxs-lookup"><span data-stu-id="c46fc-115">-CreationToken</span></span>
<span data-ttu-id="c46fc-116">볼륨에 대 한 고유한 파일 경로</span><span class="sxs-lookup"><span data-stu-id="c46fc-116">A unique file path for the volume</span></span>

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

### <span data-ttu-id="c46fc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c46fc-117">-DefaultProfile</span></span>
<span data-ttu-id="c46fc-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c46fc-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c46fc-119">-ExportPolicy</span><span class="sxs-lookup"><span data-stu-id="c46fc-119">-ExportPolicy</span></span>
<span data-ttu-id="c46fc-120">내보내기 정책을 나타내는 hashtable 배열</span><span class="sxs-lookup"><span data-stu-id="c46fc-120">A hashtable array which represents the export policy</span></span>

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

### <span data-ttu-id="c46fc-121">-위치</span><span class="sxs-lookup"><span data-stu-id="c46fc-121">-Location</span></span>
<span data-ttu-id="c46fc-122">리소스의 위치</span><span class="sxs-lookup"><span data-stu-id="c46fc-122">The location of the resource</span></span>

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

### <span data-ttu-id="c46fc-123">-이름</span><span class="sxs-lookup"><span data-stu-id="c46fc-123">-Name</span></span>
<span data-ttu-id="c46fc-124">ANF 볼륨의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c46fc-124">The name of the ANF volume</span></span>

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

### <span data-ttu-id="c46fc-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="c46fc-125">-PoolName</span></span>
<span data-ttu-id="c46fc-126">ANF 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c46fc-126">The name of the ANF pool</span></span>

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

### <span data-ttu-id="c46fc-127">-Poo</span><span class="sxs-lookup"><span data-stu-id="c46fc-127">-PoolObject</span></span>
<span data-ttu-id="c46fc-128">새 볼륨 개체에 대 한 풀</span><span class="sxs-lookup"><span data-stu-id="c46fc-128">The pool for the new volume object</span></span>

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

### <span data-ttu-id="c46fc-129">ProtocolType</span><span class="sxs-lookup"><span data-stu-id="c46fc-129">-ProtocolType</span></span>
<span data-ttu-id="c46fc-130">내보내기 정책을 나타내는 hashtable 배열</span><span class="sxs-lookup"><span data-stu-id="c46fc-130">A hashtable array which represents the export policy</span></span>

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

### <span data-ttu-id="c46fc-131">-ReplicationObject</span><span class="sxs-lookup"><span data-stu-id="c46fc-131">-ReplicationObject</span></span>
<span data-ttu-id="c46fc-132">복제 개체를 나타내는 hashtable 배열</span><span class="sxs-lookup"><span data-stu-id="c46fc-132">A hashtable array which represents the replication object</span></span>

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

### <span data-ttu-id="c46fc-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c46fc-133">-ResourceGroupName</span></span>
<span data-ttu-id="c46fc-134">ANF 계정의 리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="c46fc-134">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="c46fc-135">-ServiceLevel</span><span class="sxs-lookup"><span data-stu-id="c46fc-135">-ServiceLevel</span></span>
<span data-ttu-id="c46fc-136">ANF 볼륨의 서비스 수준</span><span class="sxs-lookup"><span data-stu-id="c46fc-136">The service level of the ANF volume</span></span>

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

### <span data-ttu-id="c46fc-137">-SnapshotId</span><span class="sxs-lookup"><span data-stu-id="c46fc-137">-SnapshotId</span></span>
<span data-ttu-id="c46fc-138">스냅숏에서 볼륨을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c46fc-138">Create volume from a snapshot.</span></span> <span data-ttu-id="c46fc-139">스냅숏을 식별 하는 데 사용 되는 UUID v4 또는 리소스 식별자</span><span class="sxs-lookup"><span data-stu-id="c46fc-139">UUID v4 or resource identifier used to identify the Snapshot</span></span>

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

### <span data-ttu-id="c46fc-140">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="c46fc-140">-SubnetId</span></span>
<span data-ttu-id="c46fc-141">위임 된 서브넷에 대 한 Azure 리소스 URI</span><span class="sxs-lookup"><span data-stu-id="c46fc-141">The Azure Resource URI for a delegated subnet</span></span>

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

### <span data-ttu-id="c46fc-142">태그</span><span class="sxs-lookup"><span data-stu-id="c46fc-142">-Tag</span></span>
<span data-ttu-id="c46fc-143">리소스 태그를 나타내는 hashtable</span><span class="sxs-lookup"><span data-stu-id="c46fc-143">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="c46fc-144">-UsageThreshold</span><span class="sxs-lookup"><span data-stu-id="c46fc-144">-UsageThreshold</span></span>
<span data-ttu-id="c46fc-145">파일 시스템에 허용 되는 최대 저장소 할당량 (바이트)입니다.</span><span class="sxs-lookup"><span data-stu-id="c46fc-145">The maximum storage quota allowed for a file system in bytes</span></span>

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

### <span data-ttu-id="c46fc-146">-가이 Etype</span><span class="sxs-lookup"><span data-stu-id="c46fc-146">-VolumeType</span></span>
<span data-ttu-id="c46fc-147">ANF 볼륨의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="c46fc-147">The type of the ANF volume</span></span>

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

### <span data-ttu-id="c46fc-148">-확인</span><span class="sxs-lookup"><span data-stu-id="c46fc-148">-Confirm</span></span>
<span data-ttu-id="c46fc-149">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c46fc-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c46fc-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c46fc-150">-WhatIf</span></span>
<span data-ttu-id="c46fc-151">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c46fc-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c46fc-152">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c46fc-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c46fc-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c46fc-153">CommonParameters</span></span>
<span data-ttu-id="c46fc-154">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c46fc-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c46fc-155">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c46fc-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c46fc-156">입력</span><span class="sxs-lookup"><span data-stu-id="c46fc-156">INPUTS</span></span>

### <span data-ttu-id="c46fc-157">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c46fc-157">System.String</span></span>

### <span data-ttu-id="c46fc-158">Microsoft. p. p. p. p i p. p i a p. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="c46fc-158">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="c46fc-159">출력</span><span class="sxs-lookup"><span data-stu-id="c46fc-159">OUTPUTS</span></span>

### <span data-ttu-id="c46fc-160">Microsoft. Azure. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="c46fc-160">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="c46fc-161">상속자</span><span class="sxs-lookup"><span data-stu-id="c46fc-161">NOTES</span></span>

## <span data-ttu-id="c46fc-162">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c46fc-162">RELATED LINKS</span></span>
