---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: 25475bd87579b693555280f3c465f157d69c807a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206200"
---
# <span data-ttu-id="d9d32-101">Remove-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="d9d32-101">Remove-AzRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="d9d32-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9d32-102">SYNOPSIS</span></span>
<span data-ttu-id="d9d32-103">지정된 Azure Site Recovery 보호 컨테이너 매핑을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="d9d32-103">Deletes the specified Azure Site Recovery protection container mapping.</span></span>

## <span data-ttu-id="d9d32-104">구문</span><span class="sxs-lookup"><span data-stu-id="d9d32-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrProtectionContainerMapping -InputObject <ASRProtectionContainerMapping> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9d32-105">설명</span><span class="sxs-lookup"><span data-stu-id="d9d32-105">DESCRIPTION</span></span>
<span data-ttu-id="d9d32-106">**Remove-AzRecoveryServicesAsrProtectionContainerMapping** cmdlet은 지정된 Azure Site Recovery 보호 컨테이너 매핑을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="d9d32-106">The **Remove-AzRecoveryServicesAsrProtectionContainerMapping** cmdlet deletes the specified Azure Site Recovery protection container mapping.</span></span>

## <span data-ttu-id="d9d32-107">예제</span><span class="sxs-lookup"><span data-stu-id="d9d32-107">EXAMPLES</span></span>

### <span data-ttu-id="d9d32-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="d9d32-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrProtectionContainerMapping -ProtectionContainerMapping $ProtectionContainerMapping
```

<span data-ttu-id="d9d32-109">지정된 보호 컨테이너 매핑의 지우기 시작 및 작업을 추적하는 데 사용되는 ASR 작업을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="d9d32-109">Starts the deletion of specified protection container mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="d9d32-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d9d32-110">PARAMETERS</span></span>

### <span data-ttu-id="d9d32-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9d32-111">-DefaultProfile</span></span>
<span data-ttu-id="d9d32-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d9d32-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="d9d32-113">-Force</span><span class="sxs-lookup"><span data-stu-id="d9d32-113">-Force</span></span>
<span data-ttu-id="d9d32-114">추가 경고를 제공하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="d9d32-114">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="d9d32-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d9d32-115">-InputObject</span></span>
<span data-ttu-id="d9d32-116">cmdlet에 대한 입력 개체: 삭제할 보호 컨테이너에 해당하는 ASR 보호 컨테이너 매핑 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="d9d32-116">The input object to the cmdlet: the ASR protection container mapping object corresponding to the protection container to be deleted.</span></span>

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

### <span data-ttu-id="d9d32-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d9d32-117">-Confirm</span></span>
<span data-ttu-id="d9d32-118">확인이 필요한지 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d9d32-118">Specify if confirmation is required.</span></span> <span data-ttu-id="d9d32-119">확인을 건너뛰기 위해 confirm 매개 $false 값으로 설정</span><span class="sxs-lookup"><span data-stu-id="d9d32-119">Set the value of the confirm parameter to $false in order to skip confirmation</span></span>

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

### <span data-ttu-id="d9d32-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9d32-120">-WhatIf</span></span>
<span data-ttu-id="d9d32-121">cmdlet을 실제로 실행하지 않고 cmdlet을 실행하면 어떤 일이 일어나는지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="d9d32-121">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="d9d32-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9d32-122">CommonParameters</span></span>
<span data-ttu-id="d9d32-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d9d32-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9d32-124">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d9d32-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9d32-125">입력</span><span class="sxs-lookup"><span data-stu-id="d9d32-125">INPUTS</span></span>

### <span data-ttu-id="d9d32-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="d9d32-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping</span></span>

## <span data-ttu-id="d9d32-127">출력</span><span class="sxs-lookup"><span data-stu-id="d9d32-127">OUTPUTS</span></span>

### <span data-ttu-id="d9d32-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="d9d32-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="d9d32-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d9d32-129">NOTES</span></span>

## <span data-ttu-id="d9d32-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d9d32-130">RELATED LINKS</span></span>

[<span data-ttu-id="d9d32-131">Get-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="d9d32-131">Get-AzRecoveryServicesAsrProtectionContainerMapping</span></span>](./Get-AzRecoveryServicesAsrProtectionContainerMapping.md)

[<span data-ttu-id="d9d32-132">New-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="d9d32-132">New-AzRecoveryServicesAsrProtectionContainerMapping</span></span>](./New-AzRecoveryServicesAsrProtectionContainerMapping.md)
