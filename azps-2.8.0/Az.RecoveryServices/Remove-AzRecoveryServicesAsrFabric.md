---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrFabric.md
ms.openlocfilehash: 9a67729b384703ccc102b14d521d4422825bdb6a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873520"
---
# <span data-ttu-id="8673f-101">Remove-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="8673f-101">Remove-AzRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="8673f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8673f-102">SYNOPSIS</span></span>
<span data-ttu-id="8673f-103">복구 서비스 자격 증명 모음에서 지정 된 Azure Site Recovery 패브릭을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="8673f-103">Deletes the specified Azure Site Recovery Fabric from the Recovery Services vault.</span></span>

## <span data-ttu-id="8673f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8673f-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrFabric -InputObject <ASRFabric> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8673f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8673f-105">DESCRIPTION</span></span>
<span data-ttu-id="8673f-106">**AzRecoveryServicesAsrFabric** Cmdlet은 복구 서비스 자격 증명 모음에서 지정 된 Azure Site Recovery 패브릭을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="8673f-106">The **Remove-AzRecoveryServicesAsrFabric** cmdlet removes the specified Azure Site Recovery fabric from the Recovery services vault.</span></span>

## <span data-ttu-id="8673f-107">예제의</span><span class="sxs-lookup"><span data-stu-id="8673f-107">EXAMPLES</span></span>

### <span data-ttu-id="8673f-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="8673f-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrFabric -Fabric $Fabric
```

<span data-ttu-id="8673f-109">지정 된 패브릭의 삭제를 시작 하 고 작업을 추적 하는 데 사용 되는 ASR 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="8673f-109">Starts the deletion of specified fabric and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="8673f-110">변수</span><span class="sxs-lookup"><span data-stu-id="8673f-110">PARAMETERS</span></span>

### <span data-ttu-id="8673f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8673f-111">-DefaultProfile</span></span>
<span data-ttu-id="8673f-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8673f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="8673f-113">-Force</span><span class="sxs-lookup"><span data-stu-id="8673f-113">-Force</span></span>
<span data-ttu-id="8673f-114">추가 경고를 제공 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="8673f-114">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="8673f-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8673f-115">-InputObject</span></span>
<span data-ttu-id="8673f-116">Cmdlet에 대 한 입력 개체: 삭제할 패브릭에 해당 하는 ASR fabric 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="8673f-116">The input object to the cmdlet: The ASR fabric object corresponding to the fabric to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: (All)
Aliases: Fabric

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8673f-117">-확인</span><span class="sxs-lookup"><span data-stu-id="8673f-117">-Confirm</span></span>
<span data-ttu-id="8673f-118">확인이 필요한 경우 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8673f-118">Specify if confirmation is required.</span></span> <span data-ttu-id="8673f-119">확인을 건너뛰려면 confirm 매개 변수 값을 $false으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8673f-119">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

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

### <span data-ttu-id="8673f-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8673f-120">-WhatIf</span></span>
<span data-ttu-id="8673f-121">Cmdlet을 실제로 실행 하지 않고 cmdlet을 실행 하는 경우 발생 하는 결과를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8673f-121">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="8673f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8673f-122">CommonParameters</span></span>
<span data-ttu-id="8673f-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8673f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8673f-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8673f-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8673f-125">입력</span><span class="sxs-lookup"><span data-stu-id="8673f-125">INPUTS</span></span>

### <span data-ttu-id="8673f-126">SiteRecovery. r m m a m</span><span class="sxs-lookup"><span data-stu-id="8673f-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="8673f-127">출력</span><span class="sxs-lookup"><span data-stu-id="8673f-127">OUTPUTS</span></span>

### <span data-ttu-id="8673f-128">SiteRecovery. r i m m 작업</span><span class="sxs-lookup"><span data-stu-id="8673f-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="8673f-129">상속자</span><span class="sxs-lookup"><span data-stu-id="8673f-129">NOTES</span></span>

## <span data-ttu-id="8673f-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8673f-130">RELATED LINKS</span></span>

[<span data-ttu-id="8673f-131">Get-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="8673f-131">Get-AzRecoveryServicesAsrFabric</span></span>](./Get-AzRecoveryServicesAsrFabric.md)

[<span data-ttu-id="8673f-132">새로운 AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="8673f-132">New-AzRecoveryServicesAsrFabric</span></span>](./New-AzRecoveryServicesAsrFabric.md)
