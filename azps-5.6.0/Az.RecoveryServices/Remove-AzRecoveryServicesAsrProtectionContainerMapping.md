---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: f7d71d0e69f83633d02832bd3f54554be1fa0ba0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953248"
---
# <span data-ttu-id="49228-101">Remove-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="49228-101">Remove-AzRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="49228-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49228-102">SYNOPSIS</span></span>
<span data-ttu-id="49228-103">지정된 Azure Site Recovery 보호 컨테이너 매핑을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="49228-103">Deletes the specified Azure Site Recovery protection container mapping.</span></span>

## <span data-ttu-id="49228-104">구문</span><span class="sxs-lookup"><span data-stu-id="49228-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrProtectionContainerMapping -InputObject <ASRProtectionContainerMapping> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49228-105">설명</span><span class="sxs-lookup"><span data-stu-id="49228-105">DESCRIPTION</span></span>
<span data-ttu-id="49228-106">**Remove-AzRecoveryServicesAsrProtectionContainerMapping** cmdlet은 지정된 Azure Site Recovery 보호 컨테이너 매핑을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="49228-106">The **Remove-AzRecoveryServicesAsrProtectionContainerMapping** cmdlet deletes the specified Azure Site Recovery protection container mapping.</span></span>

## <span data-ttu-id="49228-107">예제</span><span class="sxs-lookup"><span data-stu-id="49228-107">EXAMPLES</span></span>

### <span data-ttu-id="49228-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="49228-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrProtectionContainerMapping -ProtectionContainerMapping $ProtectionContainerMapping
```

<span data-ttu-id="49228-109">지정된 보호 컨테이너 매핑의 지우기 시작하고 작업을 추적하는 데 사용되는 ASR 작업을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="49228-109">Starts the deletion of specified protection container mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="49228-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="49228-110">PARAMETERS</span></span>

### <span data-ttu-id="49228-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49228-111">-DefaultProfile</span></span>
<span data-ttu-id="49228-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="49228-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="49228-113">-Force</span><span class="sxs-lookup"><span data-stu-id="49228-113">-Force</span></span>
<span data-ttu-id="49228-114">추가 경고를 제공하지 않고 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="49228-114">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="49228-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="49228-115">-InputObject</span></span>
<span data-ttu-id="49228-116">cmdlet에 대한 입력 개체: 삭제할 보호 컨테이너에 해당하는 ASR 보호 컨테이너 매핑 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="49228-116">The input object to the cmdlet: the ASR protection container mapping object corresponding to the protection container to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping
Parameter Sets: (All)
Aliases: ProtectionContainerMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="49228-117">-확인</span><span class="sxs-lookup"><span data-stu-id="49228-117">-Confirm</span></span>
<span data-ttu-id="49228-118">확인이 필요한지 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="49228-118">Specify if confirmation is required.</span></span> <span data-ttu-id="49228-119">확인을 건너뛰기 위해 확인 매개 변수의 $false 설정</span><span class="sxs-lookup"><span data-stu-id="49228-119">Set the value of the confirm parameter to $false in order to skip confirmation</span></span>

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

### <span data-ttu-id="49228-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49228-120">-WhatIf</span></span>
<span data-ttu-id="49228-121">cmdlet을 실제로 실행하지 않고 cmdlet을 실행하면 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="49228-121">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="49228-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49228-122">CommonParameters</span></span>
<span data-ttu-id="49228-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="49228-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49228-124">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="49228-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49228-125">입력</span><span class="sxs-lookup"><span data-stu-id="49228-125">INPUTS</span></span>

### <span data-ttu-id="49228-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="49228-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping</span></span>

## <span data-ttu-id="49228-127">출력</span><span class="sxs-lookup"><span data-stu-id="49228-127">OUTPUTS</span></span>

### <span data-ttu-id="49228-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="49228-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="49228-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="49228-129">NOTES</span></span>

## <span data-ttu-id="49228-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="49228-130">RELATED LINKS</span></span>

[<span data-ttu-id="49228-131">Get-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="49228-131">Get-AzRecoveryServicesAsrProtectionContainerMapping</span></span>](./Get-AzRecoveryServicesAsrProtectionContainerMapping.md)

[<span data-ttu-id="49228-132">New-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="49228-132">New-AzRecoveryServicesAsrProtectionContainerMapping</span></span>](./New-AzRecoveryServicesAsrProtectionContainerMapping.md)
