---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrresynchronizereplicationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrResynchronizeReplicationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrResynchronizeReplicationJob.md
ms.openlocfilehash: 0429976c64ed6e7989208c28fea1ee0a008436c8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94310097"
---
# <span data-ttu-id="44126-101">Start-AzRecoveryServicesAsrResynchronizeReplicationJob</span><span class="sxs-lookup"><span data-stu-id="44126-101">Start-AzRecoveryServicesAsrResynchronizeReplicationJob</span></span>

## <span data-ttu-id="44126-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44126-102">SYNOPSIS</span></span>
<span data-ttu-id="44126-103">복제 다시 동기화를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="44126-103">Starts replication resynchronization.</span></span>

## <span data-ttu-id="44126-104">구문과</span><span class="sxs-lookup"><span data-stu-id="44126-104">SYNTAX</span></span>

### <span data-ttu-id="44126-105">기본값 (기본값)</span><span class="sxs-lookup"><span data-stu-id="44126-105">Default (Default)</span></span>
```
Start-AzRecoveryServicesAsrResynchronizeReplicationJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44126-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="44126-106">ByResourceId</span></span>
```
Start-AzRecoveryServicesAsrResynchronizeReplicationJob -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44126-107">설명은</span><span class="sxs-lookup"><span data-stu-id="44126-107">DESCRIPTION</span></span>
<span data-ttu-id="44126-108">보호가 필요한 재 동기화 상태에 있는 경우 **AzRecoveryServicesAsrResynchronizeReplicationJob** cmdlet은 지정 된 보호 항목에 대 한 복제의 다시 동기화를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="44126-108">The **Start-AzRecoveryServicesAsrResynchronizeReplicationJob** cmdlet start resynchronization of replication for the specified protected item if the protected is in a resynchronization required state.</span></span>

## <span data-ttu-id="44126-109">예제의</span><span class="sxs-lookup"><span data-stu-id="44126-109">EXAMPLES</span></span>

### <span data-ttu-id="44126-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="44126-110">Example 1</span></span>
```
PS C:\> Start-AzRecoveryServicesAsrResynchronizeReplicationJob -ReplicationProtectedItem $rpi
```

<span data-ttu-id="44126-111">전달 된 복제 보호 항목에서 복제를 다시 동기화 하는 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="44126-111">Starts job to resynchronize replication on passed replication protected item.</span></span>

## <span data-ttu-id="44126-112">변수</span><span class="sxs-lookup"><span data-stu-id="44126-112">PARAMETERS</span></span>

### <span data-ttu-id="44126-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44126-113">-DefaultProfile</span></span>
<span data-ttu-id="44126-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="44126-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="44126-115">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="44126-115">-ReplicationProtectedItem</span></span>
<span data-ttu-id="44126-116">복제를 다시 동기화 할 ASR 복제 보호 된 항목입니다.</span><span class="sxs-lookup"><span data-stu-id="44126-116">ASR replication protected item to resynchronize replication for.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: Default
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="44126-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="44126-117">-ResourceId</span></span>
<span data-ttu-id="44126-118">다시 동기화 할 복제 보호 된 항목의 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="44126-118">Resource Id of replication protected item to resynchronize.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44126-119">-확인</span><span class="sxs-lookup"><span data-stu-id="44126-119">-Confirm</span></span>
<span data-ttu-id="44126-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="44126-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44126-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44126-121">-WhatIf</span></span>
<span data-ttu-id="44126-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="44126-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44126-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="44126-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44126-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44126-124">CommonParameters</span></span>
<span data-ttu-id="44126-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="44126-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44126-126">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="44126-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44126-127">입력</span><span class="sxs-lookup"><span data-stu-id="44126-127">INPUTS</span></span>

### <span data-ttu-id="44126-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="44126-128">System.String</span></span>

### <span data-ttu-id="44126-129">SiteRecovery. ASRReplicationProtectedItem에 대 한 서비스</span><span class="sxs-lookup"><span data-stu-id="44126-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="44126-130">출력</span><span class="sxs-lookup"><span data-stu-id="44126-130">OUTPUTS</span></span>

### <span data-ttu-id="44126-131">SiteRecovery. r i m m 작업</span><span class="sxs-lookup"><span data-stu-id="44126-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="44126-132">상속자</span><span class="sxs-lookup"><span data-stu-id="44126-132">NOTES</span></span>

## <span data-ttu-id="44126-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="44126-133">RELATED LINKS</span></span>
