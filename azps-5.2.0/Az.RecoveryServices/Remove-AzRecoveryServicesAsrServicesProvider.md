---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: 9a9fbf8c25eba6206b3852476b5a72a2f96be423
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98340682"
---
# <span data-ttu-id="a00a1-101">Remove-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="a00a1-101">Remove-AzRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="a00a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a00a1-102">SYNOPSIS</span></span>
<span data-ttu-id="a00a1-103">복구 서비스 자격 증명 모음에서 지정된 Azure Site Recovery 복구 서비스 공급자를 삭제/등록을 등록하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a00a1-103">Deletes/unregister the specified Azure Site Recovery recovery services provider from the recovery services vault.</span></span>

## <span data-ttu-id="a00a1-104">구문</span><span class="sxs-lookup"><span data-stu-id="a00a1-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrServicesProvider -InputObject <ASRRecoveryServicesProvider> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a00a1-105">설명</span><span class="sxs-lookup"><span data-stu-id="a00a1-105">DESCRIPTION</span></span>
<span data-ttu-id="a00a1-106">**Remove-AzRecoveryServicesAsrServicesProvider** cmdlet은 자격 증명 모음에서 지정된 Azure Site Recovery 복구 서비스 공급자를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="a00a1-106">The **Remove-AzRecoveryServicesAsrServicesProvider** cmdlet removes the specified Azure Site Recovery recovery services provider from the vault.</span></span>

## <span data-ttu-id="a00a1-107">예제</span><span class="sxs-lookup"><span data-stu-id="a00a1-107">EXAMPLES</span></span>

### <span data-ttu-id="a00a1-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="a00a1-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrServicesProvider -ServicesProvider $ServicesProvider
```

<span data-ttu-id="a00a1-109">지정된 Azure Site Recovery 서비스 공급자의 지우기/등록을 시작하고 작업을 추적하는 데 사용되는 ASR 작업을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="a00a1-109">Starts the deletion/unregistration of the specified Azure Site Recovery services provider and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="a00a1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a00a1-110">PARAMETERS</span></span>

### <span data-ttu-id="a00a1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a00a1-111">-DefaultProfile</span></span>
<span data-ttu-id="a00a1-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a00a1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="a00a1-113">-Force</span><span class="sxs-lookup"><span data-stu-id="a00a1-113">-Force</span></span>
<span data-ttu-id="a00a1-114">추가 경고를 제공하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="a00a1-114">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="a00a1-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a00a1-115">-InputObject</span></span>
<span data-ttu-id="a00a1-116">cmdlet에 대한 입력 개체: 삭제할 ASR 복구 서비스 공급자에 해당하는 ASR 복구 서비스 공급자 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="a00a1-116">The input object to the cmdlet: The ASR recovery services provider object corresponding to the ASR recovery services provider to be deleted.</span></span>

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

### <span data-ttu-id="a00a1-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a00a1-117">-Confirm</span></span>
<span data-ttu-id="a00a1-118">확인이 필요한지 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a00a1-118">Specify if confirmation is required.</span></span> <span data-ttu-id="a00a1-119">확인을 건너뛰기 위해 confirm 매개 $false 값으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="a00a1-119">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

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

### <span data-ttu-id="a00a1-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a00a1-120">-WhatIf</span></span>
<span data-ttu-id="a00a1-121">cmdlet을 실제로 실행하지 않고 cmdlet을 실행하면 어떤 일이 일어나는지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="a00a1-121">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="a00a1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a00a1-122">CommonParameters</span></span>
<span data-ttu-id="a00a1-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a00a1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a00a1-124">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a00a1-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a00a1-125">입력</span><span class="sxs-lookup"><span data-stu-id="a00a1-125">INPUTS</span></span>

### <span data-ttu-id="a00a1-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="a00a1-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span></span>

## <span data-ttu-id="a00a1-127">출력</span><span class="sxs-lookup"><span data-stu-id="a00a1-127">OUTPUTS</span></span>

### <span data-ttu-id="a00a1-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="a00a1-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="a00a1-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a00a1-129">NOTES</span></span>

## <span data-ttu-id="a00a1-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a00a1-130">RELATED LINKS</span></span>

[<span data-ttu-id="a00a1-131">Get-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="a00a1-131">Get-AzRecoveryServicesAsrServicesProvider</span></span>](./Get-AzRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="a00a1-132">Update-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="a00a1-132">Update-AzRecoveryServicesAsrServicesProvider</span></span>](./Update-AzRecoveryServicesAsrServicesProvider.md)
