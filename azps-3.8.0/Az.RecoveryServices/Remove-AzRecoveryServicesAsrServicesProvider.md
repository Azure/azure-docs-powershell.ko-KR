---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: 9a9fbf8c25eba6206b3852476b5a72a2f96be423
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042636"
---
# <span data-ttu-id="11117-101">Remove-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="11117-101">Remove-AzRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="11117-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11117-102">SYNOPSIS</span></span>
<span data-ttu-id="11117-103">복구 서비스 자격 증명 모음에서 지정 된 Azure Site Recovery recovery services 공급자를 삭제/등록 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="11117-103">Deletes/unregister the specified Azure Site Recovery recovery services provider from the recovery services vault.</span></span>

## <span data-ttu-id="11117-104">구문과</span><span class="sxs-lookup"><span data-stu-id="11117-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrServicesProvider -InputObject <ASRRecoveryServicesProvider> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11117-105">설명은</span><span class="sxs-lookup"><span data-stu-id="11117-105">DESCRIPTION</span></span>
<span data-ttu-id="11117-106">**AzRecoveryServicesAsrServicesProvider** cmdlet은 지정 된 Azure Site Recovery recovery services 공급자를 자격 증명 모음에서 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="11117-106">The **Remove-AzRecoveryServicesAsrServicesProvider** cmdlet removes the specified Azure Site Recovery recovery services provider from the vault.</span></span>

## <span data-ttu-id="11117-107">예제의</span><span class="sxs-lookup"><span data-stu-id="11117-107">EXAMPLES</span></span>

### <span data-ttu-id="11117-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="11117-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrServicesProvider -ServicesProvider $ServicesProvider
```

<span data-ttu-id="11117-109">지정 된 Azure Site Recovery services 공급자의 삭제/등록 취소를 시작 하 고 작업을 추적 하는 데 사용 되는 ASR 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="11117-109">Starts the deletion/unregistration of the specified Azure Site Recovery services provider and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="11117-110">변수</span><span class="sxs-lookup"><span data-stu-id="11117-110">PARAMETERS</span></span>

### <span data-ttu-id="11117-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11117-111">-DefaultProfile</span></span>
<span data-ttu-id="11117-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="11117-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="11117-113">-Force</span><span class="sxs-lookup"><span data-stu-id="11117-113">-Force</span></span>
<span data-ttu-id="11117-114">추가 경고를 제공 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="11117-114">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="11117-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="11117-115">-InputObject</span></span>
<span data-ttu-id="11117-116">Cmdlet에 대 한 입력 개체: 삭제할 ASR recovery services 공급자에 해당 하는 ASR 복구 서비스 공급자 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="11117-116">The input object to the cmdlet: The ASR recovery services provider object corresponding to the ASR recovery services provider to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider
Parameter Sets: (All)
Aliases: ServicesProvider

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="11117-117">-확인</span><span class="sxs-lookup"><span data-stu-id="11117-117">-Confirm</span></span>
<span data-ttu-id="11117-118">확인이 필요한 경우 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11117-118">Specify if confirmation is required.</span></span> <span data-ttu-id="11117-119">확인을 건너뛰려면 confirm 매개 변수 값을 $false으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11117-119">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

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

### <span data-ttu-id="11117-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11117-120">-WhatIf</span></span>
<span data-ttu-id="11117-121">Cmdlet을 실제로 실행 하지 않고 cmdlet을 실행 하는 경우 발생 하는 결과를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="11117-121">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="11117-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11117-122">CommonParameters</span></span>
<span data-ttu-id="11117-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="11117-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11117-124">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="11117-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11117-125">입력</span><span class="sxs-lookup"><span data-stu-id="11117-125">INPUTS</span></span>

### <span data-ttu-id="11117-126">SiteRecovery. r m/RecoveryServices 공급자</span><span class="sxs-lookup"><span data-stu-id="11117-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span></span>

## <span data-ttu-id="11117-127">출력</span><span class="sxs-lookup"><span data-stu-id="11117-127">OUTPUTS</span></span>

### <span data-ttu-id="11117-128">SiteRecovery. r i m m 작업</span><span class="sxs-lookup"><span data-stu-id="11117-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="11117-129">상속자</span><span class="sxs-lookup"><span data-stu-id="11117-129">NOTES</span></span>

## <span data-ttu-id="11117-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="11117-130">RELATED LINKS</span></span>

[<span data-ttu-id="11117-131">Get-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="11117-131">Get-AzRecoveryServicesAsrServicesProvider</span></span>](./Get-AzRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="11117-132">업데이트-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="11117-132">Update-AzRecoveryServicesAsrServicesProvider</span></span>](./Update-AzRecoveryServicesAsrServicesProvider.md)