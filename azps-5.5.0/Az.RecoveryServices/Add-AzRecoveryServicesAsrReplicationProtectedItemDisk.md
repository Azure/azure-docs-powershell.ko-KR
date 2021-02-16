---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/add-azrecoveryservicesasrreplicationprotecteditemdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Add-AzRecoveryServicesAsrReplicationProtectedItemDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Add-AzRecoveryServicesAsrReplicationProtectedItemDisk.md
ms.openlocfilehash: ab8c2bb74f381be898dc243ddd010462f8158ed2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179004"
---
# <span data-ttu-id="e9e77-101">Add-AzRecoveryServicesAsrReplicationProtectedItemDisk</span><span class="sxs-lookup"><span data-stu-id="e9e77-101">Add-AzRecoveryServicesAsrReplicationProtectedItemDisk</span></span>

## <span data-ttu-id="e9e77-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9e77-102">SYNOPSIS</span></span>
<span data-ttu-id="e9e77-103">이미 보호된 Azure 가상 머신에 대한 보호를 위해 디스크를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="e9e77-103">Add the disk for protection for already protected azure virtual machine.</span></span>

## <span data-ttu-id="e9e77-104">구문</span><span class="sxs-lookup"><span data-stu-id="e9e77-104">SYNTAX</span></span>

```
Add-AzRecoveryServicesAsrReplicationProtectedItemDisk -InputObject <ASRReplicationProtectedItem>
 -AzureToAzureDiskReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e9e77-105">설명</span><span class="sxs-lookup"><span data-stu-id="e9e77-105">DESCRIPTION</span></span>
<span data-ttu-id="e9e77-106">**Add-AzRecoveryServicesAsrReplicationProtectedItemDisk** cmdlet은 이미 보호된 Azure 가상 머신에 대한 보호를 위해 디스크를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="e9e77-106">The **Add-AzRecoveryServicesAsrReplicationProtectedItemDisk** cmdlet add the disk for protection for already protected azure virtual machine.</span></span>

## <span data-ttu-id="e9e77-107">예제</span><span class="sxs-lookup"><span data-stu-id="e9e77-107">EXAMPLES</span></span>

### <span data-ttu-id="e9e77-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="e9e77-108">Example 1</span></span>
```powershell
PS C:> Add-AzRecoveryServicesAsrReplicationProtectedItemDisk -ReplicationProtectedItem $rpi -AzureToAzureDiskReplicationConfiguration $disk1,$disk2
```

<span data-ttu-id="e9e77-109">보호를 위해 지정된 디스크 구성을 추가하는 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9e77-109">Start the operation to add specified disk configuration for protection.</span></span>

### <span data-ttu-id="e9e77-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="e9e77-110">Example 2</span></span>
```powershell
PS C:> $ReplicationProtectedItem |Add-AzRecoveryServicesAsrReplicationProtectedItemDisk -AzureToAzureDiskReplicationConfiguration $disk1,$disk2
```

<span data-ttu-id="e9e77-111">보호를 위해 지정된 디스크 구성을 추가하는 작업을 시작 합니다. 입력 복제 보호된 항목을 파이핑합니다.</span><span class="sxs-lookup"><span data-stu-id="e9e77-111">Start the operation to add specified disk configuration for protection.Piping input replication protected item.</span></span>

## <span data-ttu-id="e9e77-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e9e77-112">PARAMETERS</span></span>

### <span data-ttu-id="e9e77-113">-AzureToAzureDiskReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="e9e77-113">-AzureToAzureDiskReplicationConfiguration</span></span>
<span data-ttu-id="e9e77-114">Azure에서 Azure로의 재해 복구 시나리오에 대한 디스크 보호에 사용할 디스크 구성을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e9e77-114">Specifies the disk configuration to used for disk protection for Azure to Azure disaster recovery scenario.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzuretoAzureDiskReplicationConfig[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9e77-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9e77-115">-DefaultProfile</span></span>
<span data-ttu-id="e9e77-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e9e77-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e9e77-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e9e77-117">-InputObject</span></span>
<span data-ttu-id="e9e77-118">cmdlet에 대한 입력 개체: 새 디스크를 보호해야 하는 ASR 복제 보호된 항목 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="e9e77-118">The input object to the cmdlet: The ASR replication protected item object corresponding to which new disk should be protected.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: ReplicationProtectedItem

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e9e77-119">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="e9e77-119">-WaitForCompletion</span></span>
<span data-ttu-id="e9e77-120">완료 대기</span><span class="sxs-lookup"><span data-stu-id="e9e77-120">Wait For Completion</span></span>

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

### <span data-ttu-id="e9e77-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e9e77-121">-Confirm</span></span>
<span data-ttu-id="e9e77-122">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e9e77-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9e77-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9e77-123">-WhatIf</span></span>
<span data-ttu-id="e9e77-124">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="e9e77-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9e77-125">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e9e77-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9e77-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9e77-126">CommonParameters</span></span>
<span data-ttu-id="e9e77-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e9e77-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9e77-128">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e9e77-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9e77-129">입력</span><span class="sxs-lookup"><span data-stu-id="e9e77-129">INPUTS</span></span>

### <span data-ttu-id="e9e77-130">없음</span><span class="sxs-lookup"><span data-stu-id="e9e77-130">None</span></span>

## <span data-ttu-id="e9e77-131">출력</span><span class="sxs-lookup"><span data-stu-id="e9e77-131">OUTPUTS</span></span>

### <span data-ttu-id="e9e77-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="e9e77-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="e9e77-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e9e77-133">NOTES</span></span>

## <span data-ttu-id="e9e77-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e9e77-134">RELATED LINKS</span></span>
