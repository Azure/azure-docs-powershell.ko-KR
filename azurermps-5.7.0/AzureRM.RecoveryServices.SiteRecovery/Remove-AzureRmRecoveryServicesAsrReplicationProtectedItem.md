---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: 1df32bfcf049346b3f434b252a413eef020d0b77
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529775"
---
# <span data-ttu-id="fdfec-101">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="fdfec-101">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="fdfec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fdfec-102">SYNOPSIS</span></span>
<span data-ttu-id="fdfec-103">Azure Site Recovery 복제 보호 항목의 복제를 중지 하거나 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdfec-103">Stops/Disables replication for an Azure Site Recovery replication protected item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fdfec-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fdfec-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject <ASRReplicationProtectedItem>
 [-WaitForCompletion] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fdfec-105">설명은</span><span class="sxs-lookup"><span data-stu-id="fdfec-105">DESCRIPTION</span></span>
<span data-ttu-id="fdfec-106">**AzureRmRecoveryServicesAsrReplicationProtectedItem** cmdlet은 지정 된 Azure Site Recovery 복제 보호 항목의 복제를 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdfec-106">The **Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem** cmdlet disables replication of the specified Azure Site Recovery replication protected item.</span></span>
<span data-ttu-id="fdfec-107">이 작업을 수행 하면 보호 된 항목에 대 한 복제가 중지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fdfec-107">This operation causes replication to stop for the protected item.</span></span>

## <span data-ttu-id="fdfec-108">예제의</span><span class="sxs-lookup"><span data-stu-id="fdfec-108">EXAMPLES</span></span>

### <span data-ttu-id="fdfec-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="fdfec-109">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem -ReplicationProtectedItem $ReplicationProtectedItem
```

<span data-ttu-id="fdfec-110">지정 된 복제 보호 항목에 대 한 복제 사용 안 함 작업을 시작 하 고 작업을 추적 하는 데 사용 되는 ASR 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdfec-110">Starts the disable replication operation for the specified replication protected item and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="fdfec-111">변수</span><span class="sxs-lookup"><span data-stu-id="fdfec-111">PARAMETERS</span></span>

### <span data-ttu-id="fdfec-112">-확인</span><span class="sxs-lookup"><span data-stu-id="fdfec-112">-Confirm</span></span>
<span data-ttu-id="fdfec-113">확인이 필요한 경우 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdfec-113">Specify if confirmation is required.</span></span> <span data-ttu-id="fdfec-114">확인을 건너뛰려면 confirm 매개 변수 값을 $false으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdfec-114">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

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

### <span data-ttu-id="fdfec-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdfec-115">-DefaultProfile</span></span>
<span data-ttu-id="fdfec-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fdfec-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdfec-117">-Force</span><span class="sxs-lookup"><span data-stu-id="fdfec-117">-Force</span></span>
<span data-ttu-id="fdfec-118">추가 경고를 제공 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdfec-118">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="fdfec-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fdfec-119">-InputObject</span></span>
<span data-ttu-id="fdfec-120">Cmdlet에 대 한 입력 개체: 복제를 사용 하지 않도록 설정할 복제 보호 항목에 해당 하는 ASR 복제 보호 항목 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="fdfec-120">The input object to the cmdlet: The ASR replication protected item object corresponding to the replication protected item for which replication is to be disabled.</span></span>

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

### <span data-ttu-id="fdfec-121">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="fdfec-121">-WaitForCompletion</span></span>
<span data-ttu-id="fdfec-122">Cmdlet이 반환 하기 전에 작업이 완료 될 때까지 대기 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="fdfec-122">Indicates that the cmdlet should wait for the operation to complete before returning.</span></span>

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

### <span data-ttu-id="fdfec-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fdfec-123">-WhatIf</span></span>
<span data-ttu-id="fdfec-124">Cmdlet을 실제로 실행 하지 않고 cmdlet을 실행 하는 경우 발생 하는 결과를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="fdfec-124">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="fdfec-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdfec-125">CommonParameters</span></span>
<span data-ttu-id="fdfec-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdfec-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdfec-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fdfec-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdfec-128">입력</span><span class="sxs-lookup"><span data-stu-id="fdfec-128">INPUTS</span></span>

### <span data-ttu-id="fdfec-129">SiteRecovery. ASRReplicationProtectedItem에 대 한 서비스</span><span class="sxs-lookup"><span data-stu-id="fdfec-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="fdfec-130">출력</span><span class="sxs-lookup"><span data-stu-id="fdfec-130">OUTPUTS</span></span>

### <span data-ttu-id="fdfec-131">SiteRecovery. r i m m 작업</span><span class="sxs-lookup"><span data-stu-id="fdfec-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="fdfec-132">상속자</span><span class="sxs-lookup"><span data-stu-id="fdfec-132">NOTES</span></span>

## <span data-ttu-id="fdfec-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fdfec-133">RELATED LINKS</span></span>

[<span data-ttu-id="fdfec-134">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="fdfec-134">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="fdfec-135">새로운 AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="fdfec-135">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="fdfec-136">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="fdfec-136">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)
