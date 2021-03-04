---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: c1b5623e185c10471da674c21995917c169e5ffa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953259"
---
# <span data-ttu-id="83d21-101">Remove-AzRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="83d21-101">Remove-AzRecoveryServicesAsrProtectionContainer</span></span>

## <span data-ttu-id="83d21-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83d21-102">SYNOPSIS</span></span>
<span data-ttu-id="83d21-103">해당 패브릭에서 지정된 보호 컨테이너를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="83d21-103">Deletes the specified Protection Container from its Fabric.</span></span>

## <span data-ttu-id="83d21-104">구문</span><span class="sxs-lookup"><span data-stu-id="83d21-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrProtectionContainer -InputObject <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83d21-105">설명</span><span class="sxs-lookup"><span data-stu-id="83d21-105">DESCRIPTION</span></span>
<span data-ttu-id="83d21-106">Remove-AzRecoveryServicesAsrProtectionContainer cmdlet은 지정된 Azure Site Recovery Protection Container를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="83d21-106">The Remove-AzRecoveryServicesAsrProtectionContainer cmdlet deletes the specified Azure Site Recovery Protection Container.</span></span>

## <span data-ttu-id="83d21-107">예제</span><span class="sxs-lookup"><span data-stu-id="83d21-107">EXAMPLES</span></span>

### <span data-ttu-id="83d21-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="83d21-108">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrProtectionContainer -Name xxxxx  -Fabric $fabric
PS C:\> Remove-AzRecoveryServicesAsrProtectionContainer -InputObject $protectionContainer
```

<span data-ttu-id="83d21-109">지정된 보호 컨테이너의 삭제를 시작하고 제거 작업을 추적하는 데 사용되는 ASR 작업을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="83d21-109">Starts the deletion of specified protection container and returns the ASR job used to track the remove operation.</span></span>

## <span data-ttu-id="83d21-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="83d21-110">PARAMETERS</span></span>

### <span data-ttu-id="83d21-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83d21-111">-DefaultProfile</span></span>
<span data-ttu-id="83d21-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="83d21-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="83d21-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="83d21-113">-InputObject</span></span>
<span data-ttu-id="83d21-114">제거할 보호 컨테이너를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="83d21-114">Specifies the protection container to be removed .</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer
Parameter Sets: (All)
Aliases: ProtectionContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="83d21-115">-확인</span><span class="sxs-lookup"><span data-stu-id="83d21-115">-Confirm</span></span>
<span data-ttu-id="83d21-116">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="83d21-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83d21-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83d21-117">-WhatIf</span></span>
<span data-ttu-id="83d21-118">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="83d21-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83d21-119">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="83d21-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83d21-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83d21-120">CommonParameters</span></span>
<span data-ttu-id="83d21-121">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="83d21-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83d21-122">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="83d21-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83d21-123">입력</span><span class="sxs-lookup"><span data-stu-id="83d21-123">INPUTS</span></span>

### <span data-ttu-id="83d21-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="83d21-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="83d21-125">출력</span><span class="sxs-lookup"><span data-stu-id="83d21-125">OUTPUTS</span></span>

### <span data-ttu-id="83d21-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="83d21-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="83d21-127">참고 사항</span><span class="sxs-lookup"><span data-stu-id="83d21-127">NOTES</span></span>

## <span data-ttu-id="83d21-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="83d21-128">RELATED LINKS</span></span>
