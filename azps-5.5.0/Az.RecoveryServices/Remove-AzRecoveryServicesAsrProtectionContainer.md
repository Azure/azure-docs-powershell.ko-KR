---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: 36b13334c032304ddb61db04c360a1e310ef0876
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183892"
---
# <span data-ttu-id="d9a94-101">Remove-AzRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="d9a94-101">Remove-AzRecoveryServicesAsrProtectionContainer</span></span>

## <span data-ttu-id="d9a94-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9a94-102">SYNOPSIS</span></span>
<span data-ttu-id="d9a94-103">해당 패브릭에서 지정된 보호 컨테이너를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="d9a94-103">Deletes the specified Protection Container from its Fabric.</span></span>

## <span data-ttu-id="d9a94-104">구문</span><span class="sxs-lookup"><span data-stu-id="d9a94-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrProtectionContainer -InputObject <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9a94-105">설명</span><span class="sxs-lookup"><span data-stu-id="d9a94-105">DESCRIPTION</span></span>
<span data-ttu-id="d9a94-106">이 Remove-AzRecoveryServicesAsrProtectionContainer cmdlet은 지정된 Azure Site Recovery Protection 컨테이너를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="d9a94-106">The Remove-AzRecoveryServicesAsrProtectionContainer cmdlet deletes the specified Azure Site Recovery Protection Container.</span></span>

## <span data-ttu-id="d9a94-107">예제</span><span class="sxs-lookup"><span data-stu-id="d9a94-107">EXAMPLES</span></span>

### <span data-ttu-id="d9a94-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="d9a94-108">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrProtectionContainer -Name xxxxx  -Fabric $fabric
PS C:\> Remove-AzRecoveryServicesAsrProtectionContainer -InputObject $protectionContainer
```

<span data-ttu-id="d9a94-109">지정된 보호 컨테이너 삭제를 시작하고 제거 작업을 추적하는 데 사용되는 ASR 작업을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="d9a94-109">Starts the deletion of specified protection container and returns the ASR job used to track the remove operation.</span></span>

## <span data-ttu-id="d9a94-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d9a94-110">PARAMETERS</span></span>

### <span data-ttu-id="d9a94-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9a94-111">-DefaultProfile</span></span>
<span data-ttu-id="d9a94-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d9a94-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9a94-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d9a94-113">-InputObject</span></span>
<span data-ttu-id="d9a94-114">제거할 보호 컨테이너를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d9a94-114">Specifies the protection container to be removed .</span></span>

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

### <span data-ttu-id="d9a94-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d9a94-115">-Confirm</span></span>
<span data-ttu-id="d9a94-116">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d9a94-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9a94-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9a94-117">-WhatIf</span></span>
<span data-ttu-id="d9a94-118">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="d9a94-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9a94-119">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d9a94-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9a94-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9a94-120">CommonParameters</span></span>
<span data-ttu-id="d9a94-121">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d9a94-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9a94-122">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d9a94-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9a94-123">입력</span><span class="sxs-lookup"><span data-stu-id="d9a94-123">INPUTS</span></span>

### <span data-ttu-id="d9a94-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="d9a94-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="d9a94-125">출력</span><span class="sxs-lookup"><span data-stu-id="d9a94-125">OUTPUTS</span></span>

### <span data-ttu-id="d9a94-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="d9a94-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="d9a94-127">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d9a94-127">NOTES</span></span>

## <span data-ttu-id="d9a94-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d9a94-128">RELATED LINKS</span></span>
