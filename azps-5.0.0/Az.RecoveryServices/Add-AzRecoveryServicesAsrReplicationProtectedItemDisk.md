---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/add-azrecoveryservicesasrreplicationprotecteditemdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Add-AzRecoveryServicesAsrReplicationProtectedItemDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Add-AzRecoveryServicesAsrReplicationProtectedItemDisk.md
ms.openlocfilehash: ab8c2bb74f381be898dc243ddd010462f8158ed2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94311141"
---
# <span data-ttu-id="ac2dd-101">Add-AzRecoveryServicesAsrReplicationProtectedItemDisk</span><span class="sxs-lookup"><span data-stu-id="ac2dd-101">Add-AzRecoveryServicesAsrReplicationProtectedItemDisk</span></span>

## <span data-ttu-id="ac2dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ac2dd-102">SYNOPSIS</span></span>
<span data-ttu-id="ac2dd-103">이미 보호 된 azure 가상 머신에 대 한 보호를 위해 디스크를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac2dd-103">Add the disk for protection for already protected azure virtual machine.</span></span>

## <span data-ttu-id="ac2dd-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ac2dd-104">SYNTAX</span></span>

```
Add-AzRecoveryServicesAsrReplicationProtectedItemDisk -InputObject <ASRReplicationProtectedItem>
 -AzureToAzureDiskReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac2dd-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ac2dd-105">DESCRIPTION</span></span>
<span data-ttu-id="ac2dd-106">**AzRecoveryServicesAsrReplicationProtectedItemDisk** cmdlet은 이미 보호 된 azure 가상 머신에 대 한 보호를 위해 디스크를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac2dd-106">The **Add-AzRecoveryServicesAsrReplicationProtectedItemDisk** cmdlet add the disk for protection for already protected azure virtual machine.</span></span>

## <span data-ttu-id="ac2dd-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ac2dd-107">EXAMPLES</span></span>

### <span data-ttu-id="ac2dd-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="ac2dd-108">Example 1</span></span>
```powershell
PS C:> Add-AzRecoveryServicesAsrReplicationProtectedItemDisk -ReplicationProtectedItem $rpi -AzureToAzureDiskReplicationConfiguration $disk1,$disk2
```

<span data-ttu-id="ac2dd-109">보호를 위해 지정 된 디스크 구성을 추가 하는 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac2dd-109">Start the operation to add specified disk configuration for protection.</span></span>

### <span data-ttu-id="ac2dd-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="ac2dd-110">Example 2</span></span>
```powershell
PS C:> $ReplicationProtectedItem |Add-AzRecoveryServicesAsrReplicationProtectedItemDisk -AzureToAzureDiskReplicationConfiguration $disk1,$disk2
```

<span data-ttu-id="ac2dd-111">보호를 위해 지정 된 디스크 구성을 추가 하는 작업을 시작 합니다. 파이핑 입력 복제 보호 된 항목입니다.</span><span class="sxs-lookup"><span data-stu-id="ac2dd-111">Start the operation to add specified disk configuration for protection.Piping input replication protected item.</span></span>

## <span data-ttu-id="ac2dd-112">변수</span><span class="sxs-lookup"><span data-stu-id="ac2dd-112">PARAMETERS</span></span>

### <span data-ttu-id="ac2dd-113">-AzureToAzureDiskReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="ac2dd-113">-AzureToAzureDiskReplicationConfiguration</span></span>
<span data-ttu-id="ac2dd-114">Azure에서 Azure 재해 복구 시나리오의 디스크 보호에 사용할 디스크 구성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac2dd-114">Specifies the disk configuration to used for disk protection for Azure to Azure disaster recovery scenario.</span></span>

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

### <span data-ttu-id="ac2dd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac2dd-115">-DefaultProfile</span></span>
<span data-ttu-id="ac2dd-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ac2dd-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac2dd-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ac2dd-117">-InputObject</span></span>
<span data-ttu-id="ac2dd-118">Cmdlet에 대 한 입력 개체: 새 디스크에 대해 보호 되어야 하는 ASR 복제 보호 항목 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="ac2dd-118">The input object to the cmdlet: The ASR replication protected item object corresponding to which new disk should be protected.</span></span>

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

### <span data-ttu-id="ac2dd-119">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="ac2dd-119">-WaitForCompletion</span></span>
<span data-ttu-id="ac2dd-120">완료 대기</span><span class="sxs-lookup"><span data-stu-id="ac2dd-120">Wait For Completion</span></span>

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

### <span data-ttu-id="ac2dd-121">-확인</span><span class="sxs-lookup"><span data-stu-id="ac2dd-121">-Confirm</span></span>
<span data-ttu-id="ac2dd-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac2dd-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac2dd-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac2dd-123">-WhatIf</span></span>
<span data-ttu-id="ac2dd-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ac2dd-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac2dd-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ac2dd-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac2dd-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac2dd-126">CommonParameters</span></span>
<span data-ttu-id="ac2dd-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac2dd-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac2dd-128">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ac2dd-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac2dd-129">입력</span><span class="sxs-lookup"><span data-stu-id="ac2dd-129">INPUTS</span></span>

### <span data-ttu-id="ac2dd-130">않아야</span><span class="sxs-lookup"><span data-stu-id="ac2dd-130">None</span></span>

## <span data-ttu-id="ac2dd-131">출력</span><span class="sxs-lookup"><span data-stu-id="ac2dd-131">OUTPUTS</span></span>

### <span data-ttu-id="ac2dd-132">SiteRecovery. r i m m 작업</span><span class="sxs-lookup"><span data-stu-id="ac2dd-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="ac2dd-133">상속자</span><span class="sxs-lookup"><span data-stu-id="ac2dd-133">NOTES</span></span>

## <span data-ttu-id="ac2dd-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ac2dd-134">RELATED LINKS</span></span>
