---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/start-azurermrecoveryservicesasrswitchprocessserverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrSwitchProcessServerJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrSwitchProcessServerJob.md
ms.openlocfilehash: be16ff2145a4442861fd985dfbb55da63f010e94
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526632"
---
# <span data-ttu-id="55089-101">Start-AzureRmRecoveryServicesAsrSwitchProcessServerJob</span><span class="sxs-lookup"><span data-stu-id="55089-101">Start-AzureRmRecoveryServicesAsrSwitchProcessServerJob</span></span>

## <span data-ttu-id="55089-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55089-102">SYNOPSIS</span></span>
<span data-ttu-id="55089-103">부하 분산을 위해 한 프로세스 서버에서 다른 프로세스로 복제를 전환 합니다.</span><span class="sxs-lookup"><span data-stu-id="55089-103">Switch replication from one Process server to another for load balancing.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="55089-104">구문과</span><span class="sxs-lookup"><span data-stu-id="55089-104">SYNTAX</span></span>

```
Start-AzureRmRecoveryServicesAsrSwitchProcessServerJob -Fabric <ASRFabric>
 -SourceProcessServer <ASRProcessServer> -TargetProcessServer <ASRProcessServer>
 [-ReplicationProtectedItem <ASRReplicationProtectedItem[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55089-105">설명은</span><span class="sxs-lookup"><span data-stu-id="55089-105">DESCRIPTION</span></span>
<span data-ttu-id="55089-106">**AzureRmRecoveryServicesAsrSwitchProcessServerJob** 는 지정 된 가상 머신 또는 지정 된 프로세스 서버에 대 한 복제 데이터 이동을 지정 된 대상 프로세스 서버로 전환 합니다.</span><span class="sxs-lookup"><span data-stu-id="55089-106">The **Start-AzureRmRecoveryServicesAsrSwitchProcessServerJob** switches replication data movement for the specified virtual machines or a specified Process server to the specified target Process server.</span></span> <span data-ttu-id="55089-107">부하 분산 또는 프로세스 서버 간 복제 전환에 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="55089-107">Used for load balancing or switching replication between Process servers.</span></span>

## <span data-ttu-id="55089-108">예제의</span><span class="sxs-lookup"><span data-stu-id="55089-108">EXAMPLES</span></span>

### <span data-ttu-id="55089-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="55089-109">Example 1</span></span>
```
PS C:\> Start-AzureRmRecoveryServicesAsrSwitchProcessServerJob -Fabric $fabric -SourceProcessServer $sourceProcessServer  -TargetProcessServer $TargetProcessServer
```

<span data-ttu-id="55089-110">원본에서 대상 프로세스 서버로 모든 복제 보호 된 항목의 전환 프로세스 서버를 추적 하는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="55089-110">Job to track switching process server for all replication protected item from source to target process server.</span></span>

### <span data-ttu-id="55089-111">예제 2</span><span class="sxs-lookup"><span data-stu-id="55089-111">Example 2</span></span>
```
PS C:\> Start-AzureRmRecoveryServicesAsrSwitchProcessServerJob -Fabric $fabric -SourceProcessServer $sourceProcessServer  -TargetProcessServer $TargetProcessServer -ReplicatedItem $rpList
```

<span data-ttu-id="55089-112">원본에서 대상 프로세스 서버로 복제 보호 된 항목을 전달 하기 위한 전환 프로세스 서버를 추적 하는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="55089-112">Job to track switching process server for passed replication protected item from source to target process server.</span></span>

## <span data-ttu-id="55089-113">변수</span><span class="sxs-lookup"><span data-stu-id="55089-113">PARAMETERS</span></span>

### <span data-ttu-id="55089-114">-확인</span><span class="sxs-lookup"><span data-stu-id="55089-114">-Confirm</span></span>
<span data-ttu-id="55089-115">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="55089-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55089-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55089-116">-DefaultProfile</span></span>
<span data-ttu-id="55089-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="55089-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55089-118">-패브릭</span><span class="sxs-lookup"><span data-stu-id="55089-118">-Fabric</span></span>
<span data-ttu-id="55089-119">구성 서버에 해당 하는 사이트 복구 패브릭</span><span class="sxs-lookup"><span data-stu-id="55089-119">Site recovery fabric corresponding to the Configuration Server.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: (All)
Aliases: ConfigServer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55089-120">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="55089-120">-ReplicationProtectedItem</span></span>
<span data-ttu-id="55089-121">프로세스 서버를 전환할 복제 보호 항목의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="55089-121">List of replication protected item whose process server to be switched.</span></span>

```yaml
Type: ASRReplicationProtectedItem[]
Parameter Sets: (All)
Aliases: ReplicatedItem

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55089-122">-SourceProcessServer</span><span class="sxs-lookup"><span data-stu-id="55089-122">-SourceProcessServer</span></span>
<span data-ttu-id="55089-123">복제를 전환할 원본 프로세스 서버입니다.</span><span class="sxs-lookup"><span data-stu-id="55089-123">The Process server to switch replication out from.</span></span>

```yaml
Type: ASRProcessServer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55089-124">-TargetProcessServer</span><span class="sxs-lookup"><span data-stu-id="55089-124">-TargetProcessServer</span></span>
<span data-ttu-id="55089-125">복제를 전환할 프로세스 서버입니다.</span><span class="sxs-lookup"><span data-stu-id="55089-125">The Process server to switch replication to.</span></span>

```yaml
Type: ASRProcessServer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55089-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55089-126">-WhatIf</span></span>
<span data-ttu-id="55089-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="55089-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55089-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="55089-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55089-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55089-129">CommonParameters</span></span>
<span data-ttu-id="55089-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="55089-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55089-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55089-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55089-132">입력</span><span class="sxs-lookup"><span data-stu-id="55089-132">INPUTS</span></span>

### <span data-ttu-id="55089-133">않아야</span><span class="sxs-lookup"><span data-stu-id="55089-133">None</span></span>

## <span data-ttu-id="55089-134">출력</span><span class="sxs-lookup"><span data-stu-id="55089-134">OUTPUTS</span></span>

### <span data-ttu-id="55089-135">SiteRecovery. r i m m 작업</span><span class="sxs-lookup"><span data-stu-id="55089-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="55089-136">상속자</span><span class="sxs-lookup"><span data-stu-id="55089-136">NOTES</span></span>

## <span data-ttu-id="55089-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="55089-137">RELATED LINKS</span></span>
