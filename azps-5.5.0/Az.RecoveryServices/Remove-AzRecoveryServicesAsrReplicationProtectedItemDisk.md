---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrreplicationprotecteditemDisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk.md
ms.openlocfilehash: a5ac137692c8945ba58e848ccca530bd4bc99ed2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186609"
---
# <span data-ttu-id="8d2f4-101">Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk</span><span class="sxs-lookup"><span data-stu-id="8d2f4-101">Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk</span></span>

## <span data-ttu-id="8d2f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d2f4-102">SYNOPSIS</span></span>
<span data-ttu-id="8d2f4-103">복제 보호된 항목에 대한 디스크를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="8d2f4-103">Removes disks to replication protected item.</span></span>

## <span data-ttu-id="8d2f4-104">구문</span><span class="sxs-lookup"><span data-stu-id="8d2f4-104">SYNTAX</span></span>

### <span data-ttu-id="8d2f4-105">AzureToAzure(기본값)</span><span class="sxs-lookup"><span data-stu-id="8d2f4-105">AzureToAzure (Default)</span></span>
```
Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk -InputObject <ASRReplicationProtectedItem>
 -VhdUri <String[]> [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8d2f4-106">AzureToAzureManagedDisk</span><span class="sxs-lookup"><span data-stu-id="8d2f4-106">AzureToAzureManagedDisk</span></span>
```
Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk -InputObject <ASRReplicationProtectedItem>
 -DiskId <String[]> [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8d2f4-107">설명</span><span class="sxs-lookup"><span data-stu-id="8d2f4-107">DESCRIPTION</span></span>
<span data-ttu-id="8d2f4-108">**Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk** cmdlet은 ASR 복제 보호된 항목에서 디스크를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="8d2f4-108">The **Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk** cmdlet removes the disk from the ASR replication protected item.</span></span>

## <span data-ttu-id="8d2f4-109">예제</span><span class="sxs-lookup"><span data-stu-id="8d2f4-109">EXAMPLES</span></span>

### <span data-ttu-id="8d2f4-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="8d2f4-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk -ReplicationProtectedItem $rpi -VhdUri $vhdUri
```

<span data-ttu-id="8d2f4-111">관리되지 않는 디스크에 대한 보호 VM에서 지정된 디스크를 제거하는 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d2f4-111">Start the operation to remove specified disk from protection VM for unManaged disk.</span></span>

### <span data-ttu-id="8d2f4-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="8d2f4-112">Example 2</span></span>
```powershell
PS C:\> Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk -ReplicationProtectedItem $rpi -DiskId $diskId
```

<span data-ttu-id="8d2f4-113">Managed Disk에 대한 보호 VM에서 지정된 디스크를 제거하는 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d2f4-113">Start the operation to remove specified disk from protection VM for Managed disk.</span></span>

### <span data-ttu-id="8d2f4-114">예제 3</span><span class="sxs-lookup"><span data-stu-id="8d2f4-114">Example 3</span></span>
```
PS C:\>  $currentJob = Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk -ReplicationProtectedItem $rpi -DiskId $diskId
PS C:\>  Get-AzRecoveryServicesAsrJob -name $currentJob.id
```

<span data-ttu-id="8d2f4-115">지정된 디스크를 제거하는 작업을 시작하고 보호된 디스크 제거 작업을 추적하는 데 사용되는 ASR 작업을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="8d2f4-115">Starts the operation to remove the specified disk and returns the ASR job used to track the remove protected disk operation.</span></span>

## <span data-ttu-id="8d2f4-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8d2f4-116">PARAMETERS</span></span>

### <span data-ttu-id="8d2f4-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8d2f4-117">-Confirm</span></span>
<span data-ttu-id="8d2f4-118">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="8d2f4-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d2f4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d2f4-119">-DefaultProfile</span></span>
<span data-ttu-id="8d2f4-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8d2f4-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d2f4-121">-DiskId</span><span class="sxs-lookup"><span data-stu-id="8d2f4-121">-DiskId</span></span>
<span data-ttu-id="8d2f4-122">관리 디스크 ID 목록을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8d2f4-122">Specifies the list of managed disk Ids.</span></span>

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

### <span data-ttu-id="8d2f4-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8d2f4-123">-InputObject</span></span>
<span data-ttu-id="8d2f4-124">cmdlet에 대한 입력 개체: 제거할 디스크에 해당하는 ASR 복제 보호된 항목 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="8d2f4-124">The input object to the cmdlet: The ASR replication protected item object corresponding to which disk is to be removed.</span></span>

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

### <span data-ttu-id="8d2f4-125">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="8d2f4-125">-VhdUri</span></span>
<span data-ttu-id="8d2f4-126">vhd Uri의 목록을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8d2f4-126">Specifies the list of vhd Uri's.</span></span>

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

### <span data-ttu-id="8d2f4-127">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="8d2f4-127">-WaitForCompletion</span></span>
<span data-ttu-id="8d2f4-128">완료 대기</span><span class="sxs-lookup"><span data-stu-id="8d2f4-128">Wait For Completion</span></span>

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

### <span data-ttu-id="8d2f4-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d2f4-129">-WhatIf</span></span>
<span data-ttu-id="8d2f4-130">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="8d2f4-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d2f4-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8d2f4-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d2f4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d2f4-132">CommonParameters</span></span>
<span data-ttu-id="8d2f4-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8d2f4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d2f4-134">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8d2f4-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d2f4-135">입력</span><span class="sxs-lookup"><span data-stu-id="8d2f4-135">INPUTS</span></span>

### <span data-ttu-id="8d2f4-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="8d2f4-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="8d2f4-137">출력</span><span class="sxs-lookup"><span data-stu-id="8d2f4-137">OUTPUTS</span></span>

### <span data-ttu-id="8d2f4-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="8d2f4-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="8d2f4-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8d2f4-139">NOTES</span></span>

## <span data-ttu-id="8d2f4-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8d2f4-140">RELATED LINKS</span></span>
