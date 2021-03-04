---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: f3c18813cd3c002270d655b88fbc9285338a4338
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953147"
---
# <span data-ttu-id="b5838-101">Remove-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="b5838-101">Remove-AzRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="b5838-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5838-102">SYNOPSIS</span></span>
<span data-ttu-id="b5838-103">복구 서비스 자격 증명 모음에서 지정된 Azure Site Recovery 복구 서비스 공급자를 삭제/등록을 등록하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b5838-103">Deletes/unregister the specified Azure Site Recovery recovery services provider from the recovery services vault.</span></span>

## <span data-ttu-id="b5838-104">구문</span><span class="sxs-lookup"><span data-stu-id="b5838-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrServicesProvider -InputObject <ASRRecoveryServicesProvider> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5838-105">설명</span><span class="sxs-lookup"><span data-stu-id="b5838-105">DESCRIPTION</span></span>
<span data-ttu-id="b5838-106">**Remove-AzRecoveryServicesAsrServicesProvider** cmdlet은 자격 증명 모음에서 지정된 Azure Site Recovery 복구 서비스 공급자를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="b5838-106">The **Remove-AzRecoveryServicesAsrServicesProvider** cmdlet removes the specified Azure Site Recovery recovery services provider from the vault.</span></span>

## <span data-ttu-id="b5838-107">예제</span><span class="sxs-lookup"><span data-stu-id="b5838-107">EXAMPLES</span></span>

### <span data-ttu-id="b5838-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="b5838-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrServicesProvider -ServicesProvider $ServicesProvider
```

<span data-ttu-id="b5838-109">지정된 Azure Site Recovery 서비스 공급자의 지우기/미지정을 시작하고 작업을 추적하는 데 사용되는 ASR 작업을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="b5838-109">Starts the deletion/unregistration of the specified Azure Site Recovery services provider and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="b5838-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="b5838-110">PARAMETERS</span></span>

### <span data-ttu-id="b5838-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5838-111">-DefaultProfile</span></span>
<span data-ttu-id="b5838-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b5838-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="b5838-113">-Force</span><span class="sxs-lookup"><span data-stu-id="b5838-113">-Force</span></span>
<span data-ttu-id="b5838-114">추가 경고를 제공하지 않고 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="b5838-114">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="b5838-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b5838-115">-InputObject</span></span>
<span data-ttu-id="b5838-116">cmdlet에 대한 입력 개체: 삭제할 ASR 복구 서비스 공급자에 해당하는 ASR 복구 서비스 공급자 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="b5838-116">The input object to the cmdlet: The ASR recovery services provider object corresponding to the ASR recovery services provider to be deleted.</span></span>

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

### <span data-ttu-id="b5838-117">-확인</span><span class="sxs-lookup"><span data-stu-id="b5838-117">-Confirm</span></span>
<span data-ttu-id="b5838-118">확인이 필요한지 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b5838-118">Specify if confirmation is required.</span></span> <span data-ttu-id="b5838-119">확인을 건너뛰기 위해 확인 매개 변수의 $false 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="b5838-119">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

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

### <span data-ttu-id="b5838-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5838-120">-WhatIf</span></span>
<span data-ttu-id="b5838-121">cmdlet을 실제로 실행하지 않고 cmdlet을 실행하면 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="b5838-121">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="b5838-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5838-122">CommonParameters</span></span>
<span data-ttu-id="b5838-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b5838-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5838-124">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b5838-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5838-125">입력</span><span class="sxs-lookup"><span data-stu-id="b5838-125">INPUTS</span></span>

### <span data-ttu-id="b5838-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="b5838-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span></span>

## <span data-ttu-id="b5838-127">출력</span><span class="sxs-lookup"><span data-stu-id="b5838-127">OUTPUTS</span></span>

### <span data-ttu-id="b5838-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="b5838-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="b5838-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b5838-129">NOTES</span></span>

## <span data-ttu-id="b5838-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b5838-130">RELATED LINKS</span></span>

[<span data-ttu-id="b5838-131">Get-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="b5838-131">Get-AzRecoveryServicesAsrServicesProvider</span></span>](./Get-AzRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="b5838-132">Update-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="b5838-132">Update-AzRecoveryServicesAsrServicesProvider</span></span>](./Update-AzRecoveryServicesAsrServicesProvider.md)
