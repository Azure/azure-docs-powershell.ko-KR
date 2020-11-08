---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrreplicationprotecteditemDisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk.md
ms.openlocfilehash: a5ac137692c8945ba58e848ccca530bd4bc99ed2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042635"
---
# <span data-ttu-id="4705b-101">Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk</span><span class="sxs-lookup"><span data-stu-id="4705b-101">Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk</span></span>

## <span data-ttu-id="4705b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4705b-102">SYNOPSIS</span></span>
<span data-ttu-id="4705b-103">복제 보호 항목에 대 한 디스크를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4705b-103">Removes disks to replication protected item.</span></span>

## <span data-ttu-id="4705b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4705b-104">SYNTAX</span></span>

### <span data-ttu-id="4705b-105">AzureToAzure (기본값)</span><span class="sxs-lookup"><span data-stu-id="4705b-105">AzureToAzure (Default)</span></span>
```
Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk -InputObject <ASRReplicationProtectedItem>
 -VhdUri <String[]> [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4705b-106">AzureToAzureManagedDisk</span><span class="sxs-lookup"><span data-stu-id="4705b-106">AzureToAzureManagedDisk</span></span>
```
Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk -InputObject <ASRReplicationProtectedItem>
 -DiskId <String[]> [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4705b-107">설명은</span><span class="sxs-lookup"><span data-stu-id="4705b-107">DESCRIPTION</span></span>
<span data-ttu-id="4705b-108">**AzRecoveryServicesAsrReplicationProtectedItemDisk** CMDLET은 ASR 복제 보호 항목에서 디스크를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4705b-108">The **Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk** cmdlet removes the disk from the ASR replication protected item.</span></span>

## <span data-ttu-id="4705b-109">예제의</span><span class="sxs-lookup"><span data-stu-id="4705b-109">EXAMPLES</span></span>

### <span data-ttu-id="4705b-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="4705b-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk -ReplicationProtectedItem $rpi -VhdUri $vhdUri
```

<span data-ttu-id="4705b-111">관리 되지 않는 디스크의 보호 VM에서 지정 된 디스크를 제거 하려면 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="4705b-111">Start the operation to remove specified disk from protection VM for unManaged disk.</span></span>

### <span data-ttu-id="4705b-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="4705b-112">Example 2</span></span>
```powershell
PS C:\> Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk -ReplicationProtectedItem $rpi -DiskId $diskId
```

<span data-ttu-id="4705b-113">관리 디스크에 대 한 보호 VM에서 지정 된 디스크를 제거 하려면 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="4705b-113">Start the operation to remove specified disk from protection VM for Managed disk.</span></span>

### <span data-ttu-id="4705b-114">예제 3</span><span class="sxs-lookup"><span data-stu-id="4705b-114">Example 3</span></span>
```
PS C:\>  $currentJob = Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk -ReplicationProtectedItem $rpi -DiskId $diskId
PS C:\>  Get-AzRecoveryServicesAsrJob -name $currentJob.id
```

<span data-ttu-id="4705b-115">지정 된 디스크를 제거 하 고 보호 된 디스크 제거 작업을 추적 하는 데 사용 되는 ASR 작업을 반환 하는 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="4705b-115">Starts the operation to remove the specified disk and returns the ASR job used to track the remove protected disk operation.</span></span>

## <span data-ttu-id="4705b-116">변수</span><span class="sxs-lookup"><span data-stu-id="4705b-116">PARAMETERS</span></span>

### <span data-ttu-id="4705b-117">-확인</span><span class="sxs-lookup"><span data-stu-id="4705b-117">-Confirm</span></span>
<span data-ttu-id="4705b-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4705b-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4705b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4705b-119">-DefaultProfile</span></span>
<span data-ttu-id="4705b-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4705b-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4705b-121">-DiskId</span><span class="sxs-lookup"><span data-stu-id="4705b-121">-DiskId</span></span>
<span data-ttu-id="4705b-122">관리 되는 디스크 Id의 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4705b-122">Specifies the list of managed disk Ids.</span></span>

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

### <span data-ttu-id="4705b-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4705b-123">-InputObject</span></span>
<span data-ttu-id="4705b-124">Cmdlet에 대 한 입력 개체: 제거할 디스크에 해당 하는 ASR 복제 보호 항목 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="4705b-124">The input object to the cmdlet: The ASR replication protected item object corresponding to which disk is to be removed.</span></span>

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

### <span data-ttu-id="4705b-125">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="4705b-125">-VhdUri</span></span>
<span data-ttu-id="4705b-126">Vhd Uri의 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4705b-126">Specifies the list of vhd Uri's.</span></span>

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

### <span data-ttu-id="4705b-127">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="4705b-127">-WaitForCompletion</span></span>
<span data-ttu-id="4705b-128">완료 대기</span><span class="sxs-lookup"><span data-stu-id="4705b-128">Wait For Completion</span></span>

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

### <span data-ttu-id="4705b-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4705b-129">-WhatIf</span></span>
<span data-ttu-id="4705b-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4705b-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4705b-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4705b-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4705b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4705b-132">CommonParameters</span></span>
<span data-ttu-id="4705b-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4705b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4705b-134">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="4705b-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4705b-135">입력</span><span class="sxs-lookup"><span data-stu-id="4705b-135">INPUTS</span></span>

### <span data-ttu-id="4705b-136">SiteRecovery. ASRReplicationProtectedItem에 대 한 서비스</span><span class="sxs-lookup"><span data-stu-id="4705b-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="4705b-137">출력</span><span class="sxs-lookup"><span data-stu-id="4705b-137">OUTPUTS</span></span>

### <span data-ttu-id="4705b-138">SiteRecovery. r i m m 작업</span><span class="sxs-lookup"><span data-stu-id="4705b-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="4705b-139">상속자</span><span class="sxs-lookup"><span data-stu-id="4705b-139">NOTES</span></span>

## <span data-ttu-id="4705b-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4705b-140">RELATED LINKS</span></span>
