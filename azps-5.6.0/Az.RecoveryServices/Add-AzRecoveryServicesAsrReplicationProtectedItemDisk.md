---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/add-azrecoveryservicesasrreplicationprotecteditemdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Add-AzRecoveryServicesAsrReplicationProtectedItemDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Add-AzRecoveryServicesAsrReplicationProtectedItemDisk.md
ms.openlocfilehash: 1f69ba390d0cdf3184b876147984c10e79ed423a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987611"
---
# <span data-ttu-id="4e8c4-101">Add-AzRecoveryServicesAsrReplicationProtectedItemDisk</span><span class="sxs-lookup"><span data-stu-id="4e8c4-101">Add-AzRecoveryServicesAsrReplicationProtectedItemDisk</span></span>

## <span data-ttu-id="4e8c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4e8c4-102">SYNOPSIS</span></span>
<span data-ttu-id="4e8c4-103">이미 보호된 Azure 가상 머신에 대한 보호를 위해 디스크를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="4e8c4-103">Add the disk for protection for already protected azure virtual machine.</span></span>

## <span data-ttu-id="4e8c4-104">구문</span><span class="sxs-lookup"><span data-stu-id="4e8c4-104">SYNTAX</span></span>

```
Add-AzRecoveryServicesAsrReplicationProtectedItemDisk -InputObject <ASRReplicationProtectedItem>
 -AzureToAzureDiskReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e8c4-105">설명</span><span class="sxs-lookup"><span data-stu-id="4e8c4-105">DESCRIPTION</span></span>
<span data-ttu-id="4e8c4-106">**Add-AzRecoveryServicesAsrReplicationProtectedItemDisk** cmdlet은 이미 보호된 Azure 가상 머신에 대한 보호를 위해 디스크를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="4e8c4-106">The **Add-AzRecoveryServicesAsrReplicationProtectedItemDisk** cmdlet add the disk for protection for already protected azure virtual machine.</span></span>

## <span data-ttu-id="4e8c4-107">예제</span><span class="sxs-lookup"><span data-stu-id="4e8c4-107">EXAMPLES</span></span>

### <span data-ttu-id="4e8c4-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="4e8c4-108">Example 1</span></span>
```powershell
PS C:> Add-AzRecoveryServicesAsrReplicationProtectedItemDisk -ReplicationProtectedItem $rpi -AzureToAzureDiskReplicationConfiguration $disk1,$disk2
```

<span data-ttu-id="4e8c4-109">보호를 위해 지정된 디스크 구성을 추가하려면 작업을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="4e8c4-109">Start the operation to add specified disk configuration for protection.</span></span>

### <span data-ttu-id="4e8c4-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="4e8c4-110">Example 2</span></span>
```powershell
PS C:> $ReplicationProtectedItem |Add-AzRecoveryServicesAsrReplicationProtectedItemDisk -AzureToAzureDiskReplicationConfiguration $disk1,$disk2
```

<span data-ttu-id="4e8c4-111">보호를 위해 지정된 디스크 구성을 추가하려면 작업을 시작합니다. Piping 입력 복제 보호된 항목입니다.</span><span class="sxs-lookup"><span data-stu-id="4e8c4-111">Start the operation to add specified disk configuration for protection.Piping input replication protected item.</span></span>

## <span data-ttu-id="4e8c4-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="4e8c4-112">PARAMETERS</span></span>

### <span data-ttu-id="4e8c4-113">-AzureToAzureDiskReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="4e8c4-113">-AzureToAzureDiskReplicationConfiguration</span></span>
<span data-ttu-id="4e8c4-114">Azure에서 Azure 재해 복구 시나리오에 대한 디스크 보호에 사용할 디스크 구성을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4e8c4-114">Specifies the disk configuration to used for disk protection for Azure to Azure disaster recovery scenario.</span></span>

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

### <span data-ttu-id="4e8c4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e8c4-115">-DefaultProfile</span></span>
<span data-ttu-id="4e8c4-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4e8c4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e8c4-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4e8c4-117">-InputObject</span></span>
<span data-ttu-id="4e8c4-118">cmdlet에 대한 입력 개체: 새 디스크를 보호해야 하는 ASR 복제 보호 항목 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="4e8c4-118">The input object to the cmdlet: The ASR replication protected item object corresponding to which new disk should be protected.</span></span>

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

### <span data-ttu-id="4e8c4-119">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="4e8c4-119">-WaitForCompletion</span></span>
<span data-ttu-id="4e8c4-120">완료 대기</span><span class="sxs-lookup"><span data-stu-id="4e8c4-120">Wait For Completion</span></span>

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

### <span data-ttu-id="4e8c4-121">-확인</span><span class="sxs-lookup"><span data-stu-id="4e8c4-121">-Confirm</span></span>
<span data-ttu-id="4e8c4-122">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4e8c4-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e8c4-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e8c4-123">-WhatIf</span></span>
<span data-ttu-id="4e8c4-124">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="4e8c4-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e8c4-125">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4e8c4-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e8c4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e8c4-126">CommonParameters</span></span>
<span data-ttu-id="4e8c4-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4e8c4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e8c4-128">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4e8c4-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e8c4-129">입력</span><span class="sxs-lookup"><span data-stu-id="4e8c4-129">INPUTS</span></span>

### <span data-ttu-id="4e8c4-130">없음</span><span class="sxs-lookup"><span data-stu-id="4e8c4-130">None</span></span>

## <span data-ttu-id="4e8c4-131">출력</span><span class="sxs-lookup"><span data-stu-id="4e8c4-131">OUTPUTS</span></span>

### <span data-ttu-id="4e8c4-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="4e8c4-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="4e8c4-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4e8c4-133">NOTES</span></span>

## <span data-ttu-id="4e8c4-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4e8c4-134">RELATED LINKS</span></span>
