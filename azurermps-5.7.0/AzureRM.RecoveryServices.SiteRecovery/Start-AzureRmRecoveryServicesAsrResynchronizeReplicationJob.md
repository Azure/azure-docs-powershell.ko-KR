---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/start-azurermrecoveryservicesasrresynchronizereplicationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob.md
ms.openlocfilehash: 9c336602aebdb82e4860ee744fb99f3a6fbf5a98
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526643"
---
# <span data-ttu-id="bcd85-101">Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob</span><span class="sxs-lookup"><span data-stu-id="bcd85-101">Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob</span></span>

## <span data-ttu-id="bcd85-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bcd85-102">SYNOPSIS</span></span>
<span data-ttu-id="bcd85-103">복제 다시 동기화를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="bcd85-103">Starts replication resynchronization.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bcd85-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bcd85-104">SYNTAX</span></span>

### <span data-ttu-id="bcd85-105">기본값 (기본값)</span><span class="sxs-lookup"><span data-stu-id="bcd85-105">Default (Default)</span></span>
```
Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bcd85-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="bcd85-106">ByResourceId</span></span>
```
Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bcd85-107">설명은</span><span class="sxs-lookup"><span data-stu-id="bcd85-107">DESCRIPTION</span></span>
<span data-ttu-id="bcd85-108">보호가 필요한 재 동기화 상태에 있는 경우 **AzureRmRecoveryServicesAsrResynchronizeReplicationJob** cmdlet은 지정 된 보호 항목에 대 한 복제의 다시 동기화를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="bcd85-108">The **Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob** cmdlet start resynchronization of replication for the specified protected item if the protected is in a resynchronization required state.</span></span>

## <span data-ttu-id="bcd85-109">예제의</span><span class="sxs-lookup"><span data-stu-id="bcd85-109">EXAMPLES</span></span>

### <span data-ttu-id="bcd85-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="bcd85-110">Example 1</span></span>
```
PS C:\> Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob -ReplicationProtectedItem $rpi
```

<span data-ttu-id="bcd85-111">전달 된 복제 보호 항목에서 복제를 다시 동기화 하는 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="bcd85-111">Starts job to resynchronize replication on passed replication protected item.</span></span>

## <span data-ttu-id="bcd85-112">변수</span><span class="sxs-lookup"><span data-stu-id="bcd85-112">PARAMETERS</span></span>

### <span data-ttu-id="bcd85-113">-확인</span><span class="sxs-lookup"><span data-stu-id="bcd85-113">-Confirm</span></span>
<span data-ttu-id="bcd85-114">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="bcd85-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bcd85-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcd85-115">-DefaultProfile</span></span>
<span data-ttu-id="bcd85-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bcd85-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bcd85-117">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="bcd85-117">-ReplicationProtectedItem</span></span>
<span data-ttu-id="bcd85-118">복제를 다시 동기화 할 ASR 복제 보호 된 항목입니다.</span><span class="sxs-lookup"><span data-stu-id="bcd85-118">ASR replication protected item to resynchronize replication for.</span></span>

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: Default
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bcd85-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bcd85-119">-ResourceId</span></span>
<span data-ttu-id="bcd85-120">다시 동기화 할 복제 보호 된 항목의 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="bcd85-120">Resource Id of replication protected item to resynchronize.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bcd85-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bcd85-121">-WhatIf</span></span>
<span data-ttu-id="bcd85-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="bcd85-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bcd85-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bcd85-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bcd85-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcd85-124">CommonParameters</span></span>
<span data-ttu-id="bcd85-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bcd85-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcd85-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bcd85-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcd85-127">입력</span><span class="sxs-lookup"><span data-stu-id="bcd85-127">INPUTS</span></span>

### <span data-ttu-id="bcd85-128">SiteRecovery. ASRReplicationProtectedItem에 대 한 서비스</span><span class="sxs-lookup"><span data-stu-id="bcd85-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="bcd85-129">출력</span><span class="sxs-lookup"><span data-stu-id="bcd85-129">OUTPUTS</span></span>

### <span data-ttu-id="bcd85-130">SiteRecovery. r i m m 작업</span><span class="sxs-lookup"><span data-stu-id="bcd85-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="bcd85-131">상속자</span><span class="sxs-lookup"><span data-stu-id="bcd85-131">NOTES</span></span>

## <span data-ttu-id="bcd85-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bcd85-132">RELATED LINKS</span></span>
