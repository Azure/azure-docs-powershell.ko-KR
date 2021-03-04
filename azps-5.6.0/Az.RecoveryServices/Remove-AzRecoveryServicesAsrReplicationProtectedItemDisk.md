---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrreplicationprotecteditemDisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk.md
ms.openlocfilehash: bee3d9ff2f3e13397afba0cc85ecbb148aedc0cc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953152"
---
# <span data-ttu-id="9f997-101">Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk</span><span class="sxs-lookup"><span data-stu-id="9f997-101">Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk</span></span>

## <span data-ttu-id="9f997-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f997-102">SYNOPSIS</span></span>
<span data-ttu-id="9f997-103">복제로 보호된 항목을 복제하기 위해 디스크를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="9f997-103">Removes disks to replication protected item.</span></span>

## <span data-ttu-id="9f997-104">구문</span><span class="sxs-lookup"><span data-stu-id="9f997-104">SYNTAX</span></span>

### <span data-ttu-id="9f997-105">AzureToAzure(기본값)</span><span class="sxs-lookup"><span data-stu-id="9f997-105">AzureToAzure (Default)</span></span>
```
Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk -InputObject <ASRReplicationProtectedItem>
 -VhdUri <String[]> [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9f997-106">AzureToAzureManagedDisk</span><span class="sxs-lookup"><span data-stu-id="9f997-106">AzureToAzureManagedDisk</span></span>
```
Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk -InputObject <ASRReplicationProtectedItem>
 -DiskId <String[]> [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9f997-107">설명</span><span class="sxs-lookup"><span data-stu-id="9f997-107">DESCRIPTION</span></span>
<span data-ttu-id="9f997-108">**Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk** cmdlet은 ASR 복제 보호 항목에서 디스크를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="9f997-108">The **Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk** cmdlet removes the disk from the ASR replication protected item.</span></span>

## <span data-ttu-id="9f997-109">예제</span><span class="sxs-lookup"><span data-stu-id="9f997-109">EXAMPLES</span></span>

### <span data-ttu-id="9f997-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="9f997-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk -ReplicationProtectedItem $rpi -VhdUri $vhdUri
```

<span data-ttu-id="9f997-111">작업을 시작하여 관리되지 않는 디스크에 대한 보호 VM에서 지정된 디스크를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="9f997-111">Start the operation to remove specified disk from protection VM for unManaged disk.</span></span>

### <span data-ttu-id="9f997-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="9f997-112">Example 2</span></span>
```powershell
PS C:\> Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk -ReplicationProtectedItem $rpi -DiskId $diskId
```

<span data-ttu-id="9f997-113">작업을 시작하여 관리 디스크에 대한 보호 VM에서 지정된 디스크를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="9f997-113">Start the operation to remove specified disk from protection VM for Managed disk.</span></span>

### <span data-ttu-id="9f997-114">예제 3</span><span class="sxs-lookup"><span data-stu-id="9f997-114">Example 3</span></span>
```
PS C:\>  $currentJob = Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk -ReplicationProtectedItem $rpi -DiskId $diskId
PS C:\>  Get-AzRecoveryServicesAsrJob -name $currentJob.id
```

<span data-ttu-id="9f997-115">지정된 디스크를 제거하기 위해 작업을 시작하고 보호된 디스크 제거 작업을 추적하는 데 사용되는 ASR 작업을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="9f997-115">Starts the operation to remove the specified disk and returns the ASR job used to track the remove protected disk operation.</span></span>

## <span data-ttu-id="9f997-116">매개 변수</span><span class="sxs-lookup"><span data-stu-id="9f997-116">PARAMETERS</span></span>

### <span data-ttu-id="9f997-117">-확인</span><span class="sxs-lookup"><span data-stu-id="9f997-117">-Confirm</span></span>
<span data-ttu-id="9f997-118">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="9f997-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f997-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f997-119">-DefaultProfile</span></span>
<span data-ttu-id="9f997-120">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9f997-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f997-121">-DiskId</span><span class="sxs-lookup"><span data-stu-id="9f997-121">-DiskId</span></span>
<span data-ttu-id="9f997-122">관리 디스크 ID 목록을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9f997-122">Specifies the list of managed disk Ids.</span></span>

```yaml
Type: String[]
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f997-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9f997-123">-InputObject</span></span>
<span data-ttu-id="9f997-124">cmdlet에 대한 입력 개체: 제거할 디스크에 해당하는 ASR 복제 보호 항목 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="9f997-124">The input object to the cmdlet: The ASR replication protected item object corresponding to which disk is to be removed.</span></span>

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: ReplicationProtectedItem

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9f997-125">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="9f997-125">-VhdUri</span></span>
<span data-ttu-id="9f997-126">vhd Uri의 목록을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9f997-126">Specifies the list of vhd Uri's.</span></span>

```yaml
Type: String[]
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f997-127">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="9f997-127">-WaitForCompletion</span></span>
<span data-ttu-id="9f997-128">완료 대기</span><span class="sxs-lookup"><span data-stu-id="9f997-128">Wait For Completion</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f997-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f997-129">-WhatIf</span></span>
<span data-ttu-id="9f997-130">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="9f997-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f997-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9f997-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f997-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f997-132">CommonParameters</span></span>
<span data-ttu-id="9f997-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9f997-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f997-134">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9f997-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f997-135">입력</span><span class="sxs-lookup"><span data-stu-id="9f997-135">INPUTS</span></span>

### <span data-ttu-id="9f997-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="9f997-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="9f997-137">출력</span><span class="sxs-lookup"><span data-stu-id="9f997-137">OUTPUTS</span></span>

### <span data-ttu-id="9f997-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="9f997-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="9f997-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9f997-139">NOTES</span></span>

## <span data-ttu-id="9f997-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9f997-140">RELATED LINKS</span></span>
