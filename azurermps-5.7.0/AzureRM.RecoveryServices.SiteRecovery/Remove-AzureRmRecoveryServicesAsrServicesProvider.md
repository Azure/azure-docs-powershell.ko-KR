---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: 2aa8855365ea74a00df875fb62bfec49a8c591ba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529774"
---
# <span data-ttu-id="fd9e2-101">Remove-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="fd9e2-101">Remove-AzureRmRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="fd9e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd9e2-102">SYNOPSIS</span></span>
<span data-ttu-id="fd9e2-103">복구 서비스 자격 증명 모음에서 지정 된 Azure Site Recovery recovery services 공급자를 삭제/등록 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd9e2-103">Deletes/unregister the specified Azure Site Recovery recovery services provider from the recovery services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fd9e2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fd9e2-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrServicesProvider -InputObject <ASRRecoveryServicesProvider> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd9e2-105">설명은</span><span class="sxs-lookup"><span data-stu-id="fd9e2-105">DESCRIPTION</span></span>
<span data-ttu-id="fd9e2-106">**AzureRmRecoveryServicesAsrServicesProvider** cmdlet은 지정 된 Azure Site Recovery recovery services 공급자를 자격 증명 모음에서 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd9e2-106">The **Remove-AzureRmRecoveryServicesAsrServicesProvider** cmdlet removes the specified Azure Site Recovery recovery services provider from the vault.</span></span>

## <span data-ttu-id="fd9e2-107">예제의</span><span class="sxs-lookup"><span data-stu-id="fd9e2-107">EXAMPLES</span></span>

### <span data-ttu-id="fd9e2-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="fd9e2-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrServicesProvider -ServicesProvider $ServicesProvider
```

<span data-ttu-id="fd9e2-109">지정 된 Azure Site Recovery services 공급자의 삭제/등록 취소를 시작 하 고 작업을 추적 하는 데 사용 되는 ASR 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd9e2-109">Starts the deletion/unregistration of the specified Azure Site Recovery services provider and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="fd9e2-110">변수</span><span class="sxs-lookup"><span data-stu-id="fd9e2-110">PARAMETERS</span></span>

### <span data-ttu-id="fd9e2-111">-확인</span><span class="sxs-lookup"><span data-stu-id="fd9e2-111">-Confirm</span></span>
<span data-ttu-id="fd9e2-112">확인이 필요한 경우 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd9e2-112">Specify if confirmation is required.</span></span> <span data-ttu-id="fd9e2-113">확인을 건너뛰려면 confirm 매개 변수 값을 $false으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd9e2-113">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

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

### <span data-ttu-id="fd9e2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd9e2-114">-DefaultProfile</span></span>
<span data-ttu-id="fd9e2-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fd9e2-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="fd9e2-116">-Force</span><span class="sxs-lookup"><span data-stu-id="fd9e2-116">-Force</span></span>
<span data-ttu-id="fd9e2-117">추가 경고를 제공 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd9e2-117">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="fd9e2-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fd9e2-118">-InputObject</span></span>
<span data-ttu-id="fd9e2-119">Cmdlet에 대 한 입력 개체: 삭제할 ASR recovery services 공급자에 해당 하는 ASR 복구 서비스 공급자 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="fd9e2-119">The input object to the cmdlet: The ASR recovery services provider object corresponding to the ASR recovery services provider to be deleted.</span></span>

```yaml
Type: ASRRecoveryServicesProvider
Parameter Sets: (All)
Aliases: ServicesProvider

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fd9e2-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd9e2-120">-WhatIf</span></span>
<span data-ttu-id="fd9e2-121">Cmdlet을 실제로 실행 하지 않고 cmdlet을 실행 하는 경우 발생 하는 결과를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="fd9e2-121">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="fd9e2-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd9e2-122">CommonParameters</span></span>
<span data-ttu-id="fd9e2-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd9e2-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd9e2-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd9e2-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd9e2-125">입력</span><span class="sxs-lookup"><span data-stu-id="fd9e2-125">INPUTS</span></span>

### <span data-ttu-id="fd9e2-126">SiteRecovery. r m/RecoveryServices 공급자</span><span class="sxs-lookup"><span data-stu-id="fd9e2-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span></span>

## <span data-ttu-id="fd9e2-127">출력</span><span class="sxs-lookup"><span data-stu-id="fd9e2-127">OUTPUTS</span></span>

### <span data-ttu-id="fd9e2-128">System.webserver. t e r ' 1 [[SiteRecovery Rjob], [[Microsoft Azure. SiteRecovery, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = null]])</span><span class="sxs-lookup"><span data-stu-id="fd9e2-128">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="fd9e2-129">상속자</span><span class="sxs-lookup"><span data-stu-id="fd9e2-129">NOTES</span></span>

## <span data-ttu-id="fd9e2-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fd9e2-130">RELATED LINKS</span></span>

[<span data-ttu-id="fd9e2-131">Get-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="fd9e2-131">Get-AzureRmRecoveryServicesAsrServicesProvider</span></span>](./Get-AzureRmRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="fd9e2-132">업데이트-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="fd9e2-132">Update-AzureRmRecoveryServicesAsrServicesProvider</span></span>](./Update-AzureRmRecoveryServicesAsrServicesProvider.md)
