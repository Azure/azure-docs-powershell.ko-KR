---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrFabric.md
ms.openlocfilehash: 45979620ea4067af3fc906dfd7348d27b4850f06
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531685"
---
# <span data-ttu-id="88367-101">Remove-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="88367-101">Remove-AzureRmRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="88367-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88367-102">SYNOPSIS</span></span>
<span data-ttu-id="88367-103">복구 서비스 자격 증명 모음에서 지정 된 Azure Site Recovery 패브릭을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="88367-103">Deletes the specified Azure Site Recovery Fabric from the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="88367-104">구문과</span><span class="sxs-lookup"><span data-stu-id="88367-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrFabric -InputObject <ASRFabric> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88367-105">설명은</span><span class="sxs-lookup"><span data-stu-id="88367-105">DESCRIPTION</span></span>
<span data-ttu-id="88367-106">**AzureRmRecoveryServicesAsrFabric** Cmdlet은 복구 서비스 자격 증명 모음에서 지정 된 Azure Site Recovery 패브릭을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="88367-106">The **Remove-AzureRmRecoveryServicesAsrFabric** cmdlet removes the specified Azure Site Recovery fabric from the Recovery services vault.</span></span>

## <span data-ttu-id="88367-107">예제의</span><span class="sxs-lookup"><span data-stu-id="88367-107">EXAMPLES</span></span>

### <span data-ttu-id="88367-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="88367-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrFabric -Fabric $Fabric
```

<span data-ttu-id="88367-109">지정 된 패브릭의 삭제를 시작 하 고 작업을 추적 하는 데 사용 되는 ASR 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="88367-109">Starts the deletion of specified fabric and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="88367-110">변수</span><span class="sxs-lookup"><span data-stu-id="88367-110">PARAMETERS</span></span>

### <span data-ttu-id="88367-111">-확인</span><span class="sxs-lookup"><span data-stu-id="88367-111">-Confirm</span></span>
<span data-ttu-id="88367-112">확인이 필요한 경우 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="88367-112">Specify if confirmation is required.</span></span> <span data-ttu-id="88367-113">확인을 건너뛰려면 confirm 매개 변수 값을 $false으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="88367-113">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

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

### <span data-ttu-id="88367-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88367-114">-DefaultProfile</span></span>
<span data-ttu-id="88367-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="88367-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="88367-116">-Force</span><span class="sxs-lookup"><span data-stu-id="88367-116">-Force</span></span>
<span data-ttu-id="88367-117">추가 경고를 제공 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="88367-117">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="88367-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="88367-118">-InputObject</span></span>
<span data-ttu-id="88367-119">Cmdlet에 대 한 입력 개체: 삭제할 패브릭에 해당 하는 ASR fabric 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="88367-119">The input object to the cmdlet: The ASR fabric object corresponding to the fabric to be deleted.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: (All)
Aliases: Fabric

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="88367-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88367-120">-WhatIf</span></span>
<span data-ttu-id="88367-121">Cmdlet을 실제로 실행 하지 않고 cmdlet을 실행 하는 경우 발생 하는 결과를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="88367-121">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="88367-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88367-122">CommonParameters</span></span>
<span data-ttu-id="88367-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="88367-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88367-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88367-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88367-125">입력</span><span class="sxs-lookup"><span data-stu-id="88367-125">INPUTS</span></span>

### <span data-ttu-id="88367-126">SiteRecovery. r m m a m</span><span class="sxs-lookup"><span data-stu-id="88367-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="88367-127">출력</span><span class="sxs-lookup"><span data-stu-id="88367-127">OUTPUTS</span></span>

### <span data-ttu-id="88367-128">SiteRecovery. r i m m 작업</span><span class="sxs-lookup"><span data-stu-id="88367-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="88367-129">상속자</span><span class="sxs-lookup"><span data-stu-id="88367-129">NOTES</span></span>

## <span data-ttu-id="88367-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="88367-130">RELATED LINKS</span></span>

[<span data-ttu-id="88367-131">Get-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="88367-131">Get-AzureRmRecoveryServicesAsrFabric</span></span>](./Get-AzureRmRecoveryServicesAsrFabric.md)

[<span data-ttu-id="88367-132">새로운 AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="88367-132">New-AzureRmRecoveryServicesAsrFabric</span></span>](./New-AzureRmRecoveryServicesAsrFabric.md)
